---
date: '2026-03-28'
description: 学习如何使用 Aspose Imaging Java 将 DICOM 转换为 BMP 并保存为 BMP 图像。非常适合医学图像转换和网页显示。
keywords:
- convert DICOM to BMP
- Aspose.Imaging Java
- resize DICOM image
- medical image conversion with Aspose
- format conversion & export
title: Aspose Imaging Java：将 DICOM 转换为 BMP – 完整指南
url: /zh/java/format-conversion-export/aspose-imaging-java-dicom-to-bmp-conversion/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 如何使用 Aspose.Imaging Java 加载并重新保存 DICOM 图像为 BMP

## 介绍

在数字成像领域，管理医学图像至关重要，**aspose imaging java** 让工作变得更加轻松。无论您是需要归档 DICOM 文件、在 Web 门户上显示，还是将其集成到医疗工作流中，将 DICOM 转换为 BMP 并保持质量是常见需求。在本教程中，您将学习如何加载 DICOM 图像、将其转换为 BMP，并按比例调整其高度——全部使用干净、可用于生产的 Java 代码。

**您将学习**
- 如何使用 **aspose imaging java** 将 DICOM 图像转换为 BMP
- 在保持比例的同时调整 DICOM 图像大小的技术
- 在开发环境中设置 Aspose.Imaging for Java

在深入实现之前，让我们确保您已满足前置条件。

## 快速答案
- **需要的库是什么？** Aspose.Imaging for Java (aspose imaging java)  
- **我能在一行代码中将 DICOM 转换为 BMP 吗？** 不可以，您需要先加载图像，然后再保存。  
- **生产环境需要许可证吗？** 是的，需要有效的 Aspose.Imaging 许可证。  
- **调整大小是可选的吗？** 是的，如果只需要格式转换，可以跳过调整大小步骤。  
- **我可以批量处理多个文件吗？** 当然——可以在循环中包装相同的代码或使用 Java streams。

## Aspose Imaging Java 是什么？
Aspose.Imaging Java 是一个强大、跨平台的库，能够读取、编辑和写入超过 100 种图像格式，包括医疗级 DICOM 格式。它抽象了图像处理的底层细节，让您可以专注于业务逻辑，而不是像素操作。

## 为什么在医学图像转换中使用 Aspose Imaging Java？
- **完整的 DICOM 支持** – 在无需额外插件的情况下读取像素数据、元数据和多帧文件。  
- **高质量 BMP 输出** – 无损 BMP 文件保留诊断细节。  
- **内置调整大小** – 使用自适应重采样保持宽高比，获得清晰结果。  
- **线程安全且内存高效** – 适用于服务器端批处理任务。

## 前置条件

- **Aspose.Imaging 库**：版本 25.5 或更高（始终建议使用最新版本）。  
- **Java Development Kit (JDK)**：版本 8 或更高。  
- **IDE**：IntelliJ IDEA、Eclipse 或您喜欢的任何编辑器。  

## 为 Java 设置 Aspose.Imaging
首先，使用 Maven 或 Gradle 将库添加到项目中。

**Maven**
```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

**Gradle**
```gradle
implementation 'com.aspose:aspose-imaging:25.5'
```

或者，您可以直接从 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下载库。

### 许可证获取

要开始使用 Aspose.Imaging，您可以：

- **免费试用** – 使用限时许可证测试完整功能集。  
- **临时许可证** – 为短期项目获取临时密钥。  
- **购买** – 为生产使用购买永久许可证。

获取许可证文件后，在应用程序启动时加载它：

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.License;

License license = new License();
license.setLicense("Aspose.Imaging.Java.lic");
```

## 实现指南

我们将演示两个实用场景：

1. **加载 DICOM 文件并保存为 BMP**（核心的 “save image bmp” 操作）。  
2. **在保存前按比例调整图像高度**，这对网页缩略图很有用。

### 加载并重新保存 DICOM 图像为 BMP

#### 概述
此代码片段展示了读取 DICOM 文件并将其写出为 BMP 文件的最小步骤。

#### 步骤说明

1. **定义输入和输出路径** – 根据您的环境进行调整。  
2. 使用 `DicomImage` **加载 DICOM 图像**。  
3. 使用默认的 `BmpOptions` **将其保存为 BMP**。

```java
String dataDir = "YOUR_DOCUMENT_DIRECTORY";
String inputFile = dataDir + "image.dcm";
String outputFile = "YOUR_OUTPUT_DIRECTORY" + "ResizedOutput.bmp";

try (DicomImage image = (DicomImage) Image.load(inputFile)) {
    // Save the image as a BMP file.
    image.save(outputFile, new BmpOptions());
}
```

**关键参数**

- `inputFile`：源 DICOM 文件的完整路径。  
- `outputFile`：目标 BMP 文件路径。  
- `BmpOptions()`：使用默认 BMP 设置；如有需要，您可以自定义压缩或像素格式。

### 按比例调整高度

#### 概述
有时您需要更小的图像以加快网页加载。以下代码将高度调整为 100 像素，同时保持宽高比。

#### 步骤说明

```java
String inputFile = dataDir + "image.dcm";
String outputFile = "YOUR_OUTPUT_DIRECTORY" + "ResizeHeightProportionally_out.bmp";

try (DicomImage image = (DicomImage) Image.load(inputFile)) {
    // Resize the height proportionally to 100 pixels.
    image.resizeHeightProportionally(100, ResizeType.AdaptiveResample);
    
    // Save the resized image in BMP format.
    image.save(outputFile, new BmpOptions());
}
```

**重要细节**

- `resizeHeightProportionally(100, ResizeType.AdaptiveResample)` – 第一个参数是目标高度（像素），第二个参数指示 Aspose.Imaging 使用高质量自适应重采样。  
- 该方法会自动计算新的宽度，确保图像不会被拉伸。

## 实际应用

以下是这些代码片段发挥作用的几个真实场景：

| 使用场景 | 好处 |
|----------|---------|
| **医学图像归档** | 将 DICOM 转换为 BMP，以存储在通用文件系统中，降低供应商锁定。 |
| **放射图像的网页显示** | BMP 文件被浏览器和 UI 框架广泛支持，便于在门户中嵌入扫描图像。 |
| **跨平台数据交换** | BMP 是一种简单的光栅格式，几乎所有成像工具都能读取，促进协作。 |
| **批处理流水线** | 将代码包装在循环或 Java Stream 中，自动转换数百个文件。 |

## 性能考虑

- **在转换前调整大小**：提前缩小尺寸可降低内存使用并加快保存操作。  
- **使用 try‑with‑resources**（如示例所示）以确保及时释放图像，防止内存泄漏。  
- **批处理模式**：对于大批量文件，可使用 `ExecutorService` 并行处理，但需监控堆大小。

## 常见问题及解决方案

| 症状 | 可能原因 | 解决办法 |
|---------|--------------|-----|
| `Unsupported format` 错误 | 使用不支持 DICOM 的旧版 Aspose.Imaging | 升级到最新版本（≥ 25.5）。 |
| 大 DICOM 文件的内存不足异常 | 图像未释放或太大，无法放入堆内存 | 增加 JVM 堆内存（`-Xmx2g`），并保持 `try (DicomImage …)` 模式。 |
| BMP 输出为黑色或空白 | DICOM 文件仅包含元数据（无像素数据） | 验证源 DICOM 包含图像帧；使用 `image.getFramesCount()` 检查。 |
| 调整大小后的图像模糊 | 使用低质量的调整大小类型 | 切换到 `ResizeType.AdaptiveResample`（如示例所示）或 `ResizeType.HighQualityBicubic`。 |

## 常见问答

**Q: `save image bmp` 与 `save image png` 有何区别？**  
A: BMP 是无压缩的无损格式，保留每个像素，而 PNG 使用无损压缩以减小文件大小。需要精确像素保真度时使用 BMP。

**Q: 我能在一次运行中转换多个 DICOM 文件吗？**  
A: 可以，只需遍历 `.dcm` 文件目录，并在循环中应用相同的加载‑保存逻辑。

**Q: aspose imaging java 是否支持多帧 DICOM 序列？**  
A: 完全支持——您可以通过 `image.getFrames()` 访问每帧，并单独保存或合并为单个 BMP。

**Q: 开发阶段需要许可证吗？**  
A: 您可以使用免费试用或临时许可证进行评估，但生产部署需要购买许可证。

**Q: 转换后如何处理 DICOM 元数据（患者姓名、研究 ID）？**  
A: Aspose.Imaging 允许通过 `image.getMetaData()` 读取 DICOM 标签。然后您可以将这些信息嵌入 BMP 元数据或单独的数据库中。

## 结论

您现在拥有一个完整、端到端的解决方案，可使用 **aspose imaging java** 加载 DICOM 图像、将其转换为 BMP 并调整大小。这些构建块可以组合成批处理作业、集成到 Web 服务，或用于桌面工具，以简化医学图像工作流。

## 后续步骤

- 尝试其他 `ResizeType` 选项，以获得不同的质量‑速度平衡。  
- 探索其他 Aspose.Imaging 功能，如水印、转换为 PNG/JPEG，或元数据操作。  
- 将代码集成到现有的医疗应用或微服务中。

## 资源

- [文档](https://reference.aspose.com/imaging/java/)
- [下载库](https://releases.aspose.com/imaging/java/)
- [购买选项](https://purchase.aspose.com/buy)
- [免费试用](https://releases.aspose.com/imaging/java/)
- [临时许可证](https://purchase.aspose.com/temporary-license/)
- [支持论坛](https://forum.aspose.com/c/imaging/14)

---

**最后更新：** 2026-03-28  
**测试环境：** Aspose.Imaging 25.5 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}