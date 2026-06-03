---
date: 2026-01-09
description: 学习如何使用 Aspose.Imaging for Java 对图像进行二值化。本指南涵盖了 DICOM 转 BMP 的 Java 图像处理技术。
linktitle: Bradley's Adaptive Threshold Binarization
second_title: Aspose.Imaging Java Image Processing API
title: 如何使用 Aspose.Imaging for Java 将图像二值化
url: /zh/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Imaging for Java 将图像二值化

图像在数字世界中扮演着至关重要的角色，无论是在网站、文档还是各种应用程序中。如果你想了解 **如何高效地二值化图像**，尤其是针对医学格式如 DICOM，那么你来对地方了。图像二值化通过将图片转换为黑白表示来简化图像，非常适合后续分析、OCR 或存储优化。在本教程中，我们将使用 Aspose.Imaging for Java 的 Bradley 自适应阈值二值化完整演示整个过程。

## 快速答案
- **二值化的作用是什么？** 它根据阈值将每个像素转换为黑色或白色。
- **哪个库是 Java 图像处理的最佳选择？** Aspose.Imaging for Java 提供强大且免费试用的功能。
- **可以直接处理 DICOM 文件吗？** 可以，Aspose.Imaging 能加载 DICOM 并输出 BMP、PNG 等格式。
- **生产环境需要许可证吗？** 非试用使用需购买商业许可证。
- **支持的 Java 版本是？** 完全兼容 Java 8 及以上版本。

## 什么是图像二值化？
图像二值化是将灰度或彩色图像转换为二进制图像的过程，图像中的每个像素要么是 0（黑色），要么是 255（白色）。此步骤通常是医学图像处理流水线、文档扫描和计算机视觉任务的第一阶段。

## 为什么选择 Aspose.Imaging for Java？
Aspose.Imaging 提供纯 Java API，**加载 DICOM**，并应用诸如 **Bradley 自适应阈值** 等高级算法，随后可将结果保存为常见格式，无需外部本地库。它非常适合 **医学图像处理**、**将 DICOM 转换为 BMP** 以及其他基于 Java 的工作流。

## 前置条件

在编写代码之前，请确保已具备以下条件：

- **Java 开发环境** – 已安装 JDK 8 或更高版本。
- **Aspose.Imaging for Java** – 从官方站点下载：[Download Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/)。
- **DICOM 图像** – 任意你想二值化的 DICOM 示例文件。

准备工作完成后，接下来进入实现步骤。

## 如何二值化图像 – 步骤指南

### 导入包
首先，导入所需的 Aspose.Imaging 类。此代码片段还定义了输入和输出文件路径。

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// Load a DICOM image in an instance of DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Binarize image with Bradley's adaptive threshold.
    image.binarizeBradley(10);
    // Save the resultant image.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

### 步骤 1：定义路径
设置源 DICOM 文件和目标 BMP 文件的位置。将 `"Your Document Directory"` 替换为系统中实际的文件夹路径。

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

### 步骤 2：加载 DICOM 图像
使用 Aspose.Imaging **加载 dicom 图像** 到 `DicomImage` 对象中。该对象可让你完全访问像素数据和处理方法。

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // The image processing steps will go here.
}
```

### 步骤 3：执行二值化
应用 Bradley 自适应阈值算法。参数（本例中的 `10`）控制阈值的灵敏度；你可以尝试不同的数值以获得最佳效果。

```java
image.binarizeBradley(10);
```

### 步骤 4：保存二值化图像
最后，导出处理后的图像。这里使用 BMP 格式，但 Aspose.Imaging 还支持 PNG、JPEG、TIFF 等多种格式。

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## 常见问题与故障排除

- **FileNotFoundException** – 确认 `dataDir` 路径以斜杠结尾，且 DICOM 文件名完全匹配。
- **OutOfMemoryError** – 大型 DICOM 文件可能需要增大 JVM 堆内存 (`-Xmx2g` 或更高)。
- **阈值不正确** – 如果输出过暗或过亮，请调整传递给 `binarizeBradley()` 的整数值（例如 5‑15）。

## 常见问答

### Q1: 什么是 DICOM，为什么在医学成像中重要？
**A:** DICOM 代表 Digital Imaging and Communications in Medicine（医学数字成像与通信）。它是存储、传输和处理医学图像的通用标准，能够实现设备和系统之间的互操作性。

### Q2: 我可以在商业项目中使用 Aspose.Imaging for Java 吗？
**A:** 可以，Aspose.Imaging for Java 提供免费试用和商业许可证。你可以在 [Aspose 的网站](https://purchase.aspose.com/buy) 上了解并获取相应许可证。

### Q3: 是否有用于测试的临时许可证？
**A:** 有，你可以获取临时许可证用于测试和评估 Aspose.Imaging for Java。详情请访问 [此链接](https://purchase.aspose.com/temporary-license/)。

### Q4: 我可以在哪里寻求帮助或讨论 Aspose.Imaging for Java 相关问题？
**A:** 可前往 [Aspose.Imaging 论坛](https://forum.aspose.com/) 获取社区支持和讨论，这是获取答案并与其他用户交流的好地方。

### Q5: Aspose.Imaging for Java 适用于其他基于 Java 的图像处理应用吗？
**A:** 绝对适用。该库在 Web 应用、桌面软件、批处理工具等多种场景中表现出色，提供跨平台一致的 API。

## 结论
现在，你已经掌握了使用 Aspose.Imaging for Java 通过 Bradley 自适应阈值 **二值化图像** 的方法。这一技术在 **医学图像处理** 中尤为有价值，能够将 DICOM 文件转换为轻量级的 BMP（或其他）格式，以便后续分析或存储。继续尝试不同的阈值，并探索 Aspose.Imaging 丰富的功能集。

欲深入了解图像操作，请查阅官方文档：[Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/)。

---

**最后更新：** 2026-01-09  
**测试环境：** Aspose.Imaging for Java 24.12（撰写时的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}