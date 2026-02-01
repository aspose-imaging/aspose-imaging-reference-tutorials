---
date: 2026-02-01
description: 学习如何在 Aspose.Imaging for .NET 中使用 RLE4 压缩来压缩 BMP 图像，并在不损失质量的情况下减小 BMP
  大小。
linktitle: BMP RLE4 in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: 在 Aspose.Imaging for .NET 中使用 RLE4 压缩 BMP 图像
url: /zh/net/advanced-features/bmp-rle4/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 使用 RLE4 在 Aspose.Imaging for .NET 中压缩 BMP 图像

如果您需要在保持视觉保真度的同时**压缩 BMP 图像**文件，RLE4 压缩方法是一种轻量级、无损的解决方案，特别适用于 4 位图像。在本教程中，我们将逐步讲目到使用 Aspose.Imaging 保存带 RLE4 压缩的 BMP 文件。完成后，您将能够显著**减小 BMP 大小**并将此技术集成到任何 C# 应用程序中。

## 快速答案
- **主要库是什么？** Aspose.Imaging for .NET  
- **本指南覆盖哪种压缩？** BMP RLE4（4 位）  
- **我可以在 .NET Core 中使用吗？** 可以，API 完全兼容  
- **测试需要许可证吗？** 临时许可证足以进行评估  
- **典型的尺寸缩减？** 对于具有重复模式的 4 位 BMP，可降低至最高 60 %  

## 什么是 BMP RLE4 压缩？
RLE4（4 位运行长度编码）将连续具有相同颜色的像素存储为单个计数/值对。此方式在不牺牲任何像素数据的前提下降小文件大小，非常适合图标、简易图形或任何使用 4 位 图像？
- **无损** – 原始像素数据可以完全恢复。  
- **快速处理** – CPU 开销极小，适用于实时场景。  
- **跨平台** – 在 Windows、Linux 和 macOS 上均可使用 .NET 5/6/7。  
- **与 Aspose.Imaging 集成** – 除压缩外，您还能获得丰富的图像处理功能。  

## 前置条件
1. **Aspose.Imaging for .NET** – 从[官方网站](https://releases.aspose.com/imaging/net/)下载最新包。  
2. **.NET 开发环境 知识** – 您需要编写几行 C# 代码来加载和保存图像。  
4. **文档目录** – 在代码片段中将 `"Your Document Directory"` 替换为 BMP 文件所在的路径。  

## 导入命名空间
在开始使用 BMP RLE4 压缩之前，您需要从 Aspose.Imaging 导入必要的命名名空间
```csharp
using Aspose.Imaging;
```
此指令让您能够访问核心图像类，包括 `Image`、`BmpOptions` 和辅助工具。

## 在 Aspose.Imaging for .NET 中进行 BMP RLE4 压缩
以下是完整工作流的逐步演示。

### 步骤 2：初始化数据目录
```csharp
string dataDir = "Your Document Directory";
```
将 `dataDir` 设置为包含源 BMP（`Rle4.bmp`）且输出文件将写入的文件夹。

### 步骤 3：加载图像
```csharp
using (Image image = Image.Load(Path.Combine(dataDir, "Rle4.bmp")))
{
    // Your code for image processing goes here
}
```
`Image.Load` 会自动检测 BMP 格式并为后续操作做好准备。

### 步骤 4：应用 BMP RLE4 压缩
```csharp
image.Save(
    System.IO.Path.Combine(dataDir, "output.bmp"),
    new BmpOptions()
    {
        Compression = BitmapCompression.Rle4,
        BitsPerPixel = 4,
        Palette = ColorPaletteHelper.Create4Bit()
    });
```
这里我们：
- 将 `Compression` 设置为 `BitmapCompression.Rle4`。  
- 强制使用 4 位深度（`BitsPerPixel = 4`）。  
- 使用 `ColorPaletteHelper.Create4Bit()` 提供 4 位颜色调色板。

### 步骤 5：清理（可选）
```csharp
File.Delete(System.IO.Path.Combine(dataDir, "output.bmp"));
```
如果仅用于测试，请删除临时文件。在生产环境中通常会保留压缩后的输出。

## 如何在其他场景中压缩 BMP 图像？
- **转换 BMP 格式** – 通过将 `BmpOptions` 替换为 `PngOptions` 或 `JpegOptions`，即可更改输出格式（例如 PNG、JPEG）。  
- **在 .NET 中压缩图像** – Aspose.Imaging 还支持 JPEG、TIFF 和 WebP 压缩，为所有常见图像类型提供统一 API。  
- **BMP 压缩 C#** – 如果需要对 8 位图像使用 `BitmapCompression.Rle8`，同样的模式适用，只需相应调整 `BitsPerPixel` 和调色板。  

## 常见问题与故障排除
| 问题 | 原因 | 解决方案 |
|-------|-------|-----|
| 输出文件大于源文件 | 使用了比实际需要更多颜色的调色板 | 确保 `BitsPerPixel` 与实际调色板大小匹配（RLE4 为 4）。 |
| `Save` 时出现 `ArgumentException` | 缺少 `using System.IO;` | 在文件顶部添加 `using System.IO;`。 |
| 没有压缩效果 | 源图像已是 4 位且重复像素少 | RLE 在像素模式重复的情况下效果最佳；请使用图标或简易图形进行测试。 |

## 常见问答

**问：什么是 BMP RLE4 压缩，何时使用它？**  
**答：** BMP RLE4 压缩将连续相同颜色的像素编码为单个计数/值对。它最适用于具有大量重复颜色的 4 位图像，如图标或简易图形。

**问：我可以使用 Aspose.Imaging for .NET 将 BMP 图像转换为其他格式吗？**  
**答：** 可以，库支持转换为 JPEG、PNG、TIFF 等多种格式。只需加载 BMP 并使用所需的选项保存即可。

**问：Aspose.Imaging for .NET 是否适用于 Windows 和 .NET Core 应用程序？**  
**答：** 当然可以。该 API 在 .NET Framework、.NET Core 以及 .NET 5/6/7 上均可运行，支持所有主流操作系统。

**问：我在哪里可以获取 Aspose.Imaging for .NET 的支持或帮助？**  
**答：** 请访问 [Aspose.Imaging 支持论坛](https://forum.aspose.com/)，与社区和 Aspose 专家交流。

**问：如何获取 Aspose.Imaging for .NET 的临时许可证？**  
**答：** 您可以在 Aspose 网站的[临时许可证页面](https://purchase.aspose.com/temporary-license/)申请临时许可证。

## 结论
您现在已经学习了如何使用 Aspose.Imaging for .NET 的 RLE4 方法**压缩 BMP 图像**文件。此方法可在不牺牲质量的前提下**减小 BMP 大小**，并可无缝集成到任何 C# 项目中——无论是针对 .NET Framework 还是 .NET Core。尝试不同的调色板和图像来源，以获得针对您特定使用场景的最佳效果。

欲了解更深入的细节，请查阅完整的 [Aspose.Imaging for .NET 文档](https://reference.aspose.com/imaging/net/)。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最后更新：** 2026-02-01  
**测试环境：** Aspose.Imaging for .NET 24.11（撰写时的最新版本）  
**作者：** Aspose