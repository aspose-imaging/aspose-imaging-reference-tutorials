---
"date": "2025-06-04"
"description": "学习如何使用 Aspose.Imaging for Java 轻松将 DICOM 图像转换为 BMP 格式并调整其大小。非常适合医学图像存档和网页显示。"
"title": "使用 Aspose.Imaging 在 Java 中将 DICOM 转换为 BMP —— 完整指南"
"url": "/zh/java/format-conversion-export/aspose-imaging-java-dicom-to-bmp-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 如何使用 Aspose.Imaging Java 加载并重新保存 DICOM 图像为 BMP

## 介绍

在数字成像领域，管理医学图像至关重要。专业人员通常需要将这些图像从一种格式转换为另一种格式，同时保持其完整性。本教程将指导您使用 Aspose.Imaging for Java 加载 DICOM 图像并将其重新保存为 BMP 格式。您还将学习如何按比例调整 DICOM 图像的高度。

**您将学到什么：**

- 如何使用 Aspose.Imaging Java 将 DICOM 图像转换为 BMP
- 保持比例的同时调整 DICOM 图像大小的技术
- 在您的开发环境中设置 Aspose.Imaging for Java

在深入实施之前，让我们确保您已经满足了先决条件。 

## 先决条件

为了有效地遵循本教程，您需要：

- **Aspose.Imaging 库**：确保您拥有 25.5 或更高版本。
- **Java 开发工具包 (JDK)**：建议使用版本 8 或更高版本以确保兼容性。
- **IDE 设置**：使用 IntelliJ IDEA 或 Eclipse 等 IDE 来编写和测试您的 Java 代码。

## 设置 Aspose.Imaging for Java

首先，我们需要在您的项目中设置 Aspose.Imaging。您可以使用 Maven 或 Gradle 作为构建工具。

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

或者，您可以直接从 [Aspose.Imaging for Java 版本](https://releases。aspose.com/imaging/java/).

### 许可证获取

要开始使用 Aspose.Imaging，您可以：

- **免费试用**：通过有限试用来测试其功能。
- **临时执照**：获取临时许可证以探索全部功能。
- **购买**：为了延长使用时间，请考虑购买许可证。

**初始化和设置：**

安装库后，请在 Java 应用程序中对其进行初始化。这包括设置文件目录并确保正确引用 Aspose.Imaging 库。

## 实施指南

我们将把实现分解为两个主要特征：

### 加载并重新保存 DICOM 图像为 BMP

#### 概述

此功能演示如何从磁盘加载 DICOM 图像并将其保存为 BMP 格式，使其可供非医疗应用程序或需要基本图像格式的系统访问。

#### 逐步实施

1. **设置目录**

   定义 DICOM 文件所在的输入和输出目录以及想要保存 BMP 的位置。
   ```java
   String dataDir = "YOUR_DOCUMENT_DIRECTORY";
   String inputFile = dataDir + "image.dcm";
   String outputFile = "YOUR_OUTPUT_DIRECTORY" + "ResizedOutput.bmp";
   ```

2. **加载并保存 DICOM 图像**

   使用 `DicomImage` 从 Aspose.Imaging 加载图像，然后以 BMP 格式保存。
   ```java
   try (DicomImage image = (DicomImage) Image.load(inputFile)) {
       // 将图像保存为 BMP 文件。
       image.save(outputFile, new BmpOptions());
   }
   ```

3. **解释参数**

   - `inputFile`：您的 DICOM 文件的路径。
   - `outputFile`：BMP 输出的目标路径。
   - `BmpOptions()`：BMP格式的配置设置。

### 按比例调整高度

#### 概述

此功能允许您按比例调整 DICOM 图像的高度，保留其纵横比并将其保存为 BMP 文件。

#### 逐步实施

1. **加载 DICOM 图像**

   首先使用 Aspose.Imaging 加载您的 DICOM 图像。
   ```java
   String inputFile = dataDir + "image.dcm";
   String outputFile = "YOUR_OUTPUT_DIRECTORY" + "ResizeHeightProportionally_out.bmp";

   try (DicomImage image = (DicomImage) Image.load(inputFile)) {
       // 按比例调整高度为 100 像素。
       image.resizeHeightProportionally(100, ResizeType.AdaptiveResample);
       
       // 以 BMP 格式保存调整大小的图像。
       image.save(outputFile, new BmpOptions());
   }
   ```

2. **参数和方法**

   - `resizeHeightProportionally(100, ResizeType.AdaptiveResample)`：此方法将高度调整为 100 像素，同时使用自适应重采样保持纵横比以确保质量。

## 实际应用

以下是一些可以应用这些功能的实际场景：

1. **医学图像存档**：转换和调整 DICOM 图像的大小，以便在非医疗系统中更轻松地存储。
2. **医学图像的网页展示**：使用 BMP 格式在网络应用程序上显示医学图像，在保持质量的同时减小文件大小。
3. **跨平台兼容性**：简化可能不支持 DICOM 格式的不同软件之间的图像共享。

## 性能考虑

使用 Aspose.Imaging for Java 时：

- **优化图像尺寸**：在转换大型 DICOM 文件之前，请考虑调整其大小以减少处理时间和内存使用量。
- **高效的内存管理**：处理图像数据时利用try-with-resources有效地管理内存。
- **批处理**：如果处理多张图像，则分批自动化处理以提高效率。

## 结论

在本教程中，您学习了如何使用 Aspose.Imaging for Java 加载 DICOM 图像并将其转换为 BMP 格式。我们还学习了如何在保持图像比例的情况下调整图像大小。掌握这些技能后，您可以更有效地将医学成像解决方案集成到各种应用程序中。

**后续步骤：**

- 尝试 Aspose.Imaging 提供的其他图像处理功能。
- 探索与其他系统（如医疗保健数据库或网络平台）集成的可能性。

## 常见问题解答部分

1. **什么是 Aspose.Imaging？**
   - Aspose.Imaging 是一个强大的 Java 图像处理库，支持包括 DICOM 和 BMP 在内的多种格式。

2. **我可以在不购买许可证的情况下使用 Aspose.Imaging 吗？**
   - 是的，您可以先免费试用，或者获取临时许可证来探索其功能。

3. **Aspose.Imaging 支持哪些图像格式？**
   - 它支持多种格式，包括 JPEG、PNG、GIF、BMP 和 DICOM 等。

4. **如何使用 Aspose.Imaging 处理大型 DICOM 文件？**
   - 考虑在处理之前调整图像大小以有效地管理内存使用。

5. **是否可以将该库集成到现有的 Java 应用程序中？**
   - 是的，Aspose.Imaging 可以使用 Maven 或 Gradle 依赖项无缝集成到您当前的项目中。

## 资源

- [文档](https://reference.aspose.com/imaging/java/)
- [下载库](https://releases.aspose.com/imaging/java/)
- [购买选项](https://purchase.aspose.com/buy)
- [免费试用](https://releases.aspose.com/imaging/java/)
- [临时执照](https://purchase.aspose.com/temporary-license/)
- [支持论坛](https://forum.aspose.com/c/imaging/14)

按照本指南操作，您现在应该能够使用 Aspose.Imaging for Java 处理 DICOM 图像了。祝您编码愉快！

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}