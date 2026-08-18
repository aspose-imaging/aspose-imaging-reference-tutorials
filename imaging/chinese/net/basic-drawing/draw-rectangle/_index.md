---
date: 2026-02-12
description: 学习如何使用 Aspose 创建空白图像以及如何在 .NET 中使用 Aspose.Imaging 绘制矩形——为您的 .NET 应用程序提供的图像处理快速指南。
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: 创建空白图像 Aspose – 在 .NET 中绘制矩形
url: /zh/net/basic-drawing/draw-rectangle/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 创建空白图像 Aspose – 在 .NET 中绘制矩形

在 .NET 应用程序中创建和操作图像可能令人望而生畏，但使用 Aspose.Imaging，您只需几行代码即可 **create blank image Aspose** 并在其上绘制形状。在本教程中，我们将完整演示整个过程——从设置空白画布到绘制矩形——让您能够立即在 .NET 项目中添加图形。

## 快速答案
- **“create blank image Aspose” 是什么意思？** 它表示使用 Aspose.Imaging API 生成一个空的位图。  
- **如何使用 Aspose 在 .NET 中绘制矩形？** 在初始化 `Graphics` 对象后，使用 `Graphics.DrawRectangle` 方法。  
- **需要哪个 NuGet 包？** `Aspose.Imaging`（最新版本）。  
- **我可以将图像保存为 PNG、JPEG 或 BMP 吗？** 可以——只需更改图像选项（例如 `BmpOptions`、`JpegOptions`）。  
- **开发时需要许可证吗？** 免费试用可用于评估；生产环境需要商业许可证。

## 什么是 “create blank image Aspose”？
创建空白图像意味着分配一个具有特定宽度、高度和像素格式的像素缓冲区。Aspose.Imaging 处理底层细节，为您提供一个可直接绘制的画布，无需使用 GDI+ 或 System.Drawing。

## 为什么在 .NET 中使用 Aspose.Imaging 绘制矩形？
- **跨平台** – 在 Windows、Linux 和 macOS 上均可运行。  
- **无本机依赖** – 纯托管代码，适合服务器环境。  
- **丰富的绘图 API** – 支持画笔、刷子、抗锯齿以及多种形状类型。  
- **高性能** – 针对大图像和批处理进行优化。

## 先决条件

1. **Aspose.Imaging for .NET** – 从[下载页面](https://releases.aspose.com/imaging/net/)下载。  
2. **开发环境** – Visual Studio、VS Code 或任何兼容 .NET 的 IDE。  
3. **.NET 运行时** – .NET 6+ 或 .NET Framework 4.7.2+。  

现在我们已经准备好所有内容，让我们深入代码。

## 如何在 .NET 中使用 Aspose 创建空白图像？

### 步骤 1：导入所需的命名空间

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

这些命名空间为您提供对核心成像类、刷子类型以及图像保存选项的访问。

### 步骤 2：创建空白图像（画布）

```csharp
string dataDir = "Your Document Directory";  // Set the path to your document directory
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Your drawing code will go here
        image.Save();
    }
}
```

在此代码块中我们：

* 定义输出位置（`dataDir`）。  
* 配置 `BmpOptions` 使用 32 位像素格式。  
* 创建一个 **blank image**，尺寸为 100 × 100 像素。

### 步骤 3：如何使用 Aspose.Imaging 在 .NET 中绘制矩形

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` 用背景颜色（本例中为黄色）填充画布。  
* `DrawRectangle` 绘制两个矩形——一个使用简单的红色画笔，另一个使用蓝色实心刷子，以形成视觉对比。

### 步骤 4：保存图像

```csharp
image.Save();
```

调用 `Save` 使用前面定义的选项将位图写入文件系统。

## 常见问题与技巧

| 问题 | 原因 | 解决方案 |
|-------|--------|-----|
| **空白图像显示为黑色** | 背景未清除 | 在绘制之前调用 `graphic.Clear(Color.YourColor)`。 |
| **文件未找到异常** | `dataDir` 指向不存在的文件夹 | 确保目录存在，或使用 `Path.Combine` 与 `Environment.CurrentDirectory`。 |
| **颜色不正确** | 使用了 `System.Drawing.Color` 而非 `Aspose.Imaging.Color` | 始终导入 `Aspose.Imaging.Color`。 |
| **大图像性能下降** | 使用默认的高位深度 `BmpOptions` | 切换到 `JpegOptions` 或 `PngOptions` 以进行压缩。 |

## 常见问题（扩展）

**Q: 我可以绘制除矩形之外的其他形状吗？**  
A: 当然可以。Aspose.Imaging 提供了 `DrawEllipse`、`DrawLine` 和 `DrawPolygon` 等方法。

**Q: 该库可免费用于商业用途吗？**  
A: 不能，Aspose.Imaging 是商业产品，但您可以通过[此处](https://releases.aspose.com/)的免费试用进行评估。

**Q: 这在 Windows 和 Web 应用程序上都能工作吗？**  
A: 可以，相同的代码可在 ASP.NET、Blazor 和控制台应用中运行。

**Q: 如何将输出格式改为 PNG？**  
A: 将 `BmpOptions` 替换为 `PngOptions`，并相应地更改文件扩展名。

**Q: 在哪里可以找到更详细的文档？**  
A: 在[此处](https://reference.aspose.com/imaging/net/)访问完整的 API 参考，并在[Aspose.Imaging 论坛](https://forum.aspose.com/)加入社区。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最后更新：** 2026-02-12  
**测试环境：** Aspose.Imaging 24.12 for .NET  
**作者：** Aspose