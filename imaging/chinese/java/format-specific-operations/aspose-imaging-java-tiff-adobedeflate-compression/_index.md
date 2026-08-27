---
date: '2026-08-27'
description: 了解在使用 Aspose.Imaging for Java 将图像转换为 TIFF 时如何应用 deflate 压缩，以确保高质量、高效存储。
keywords:
- how to apply deflate
- convert to tiff java
- convert png tiff java
- Aspose.Imaging Java TIFF conversion
- AdobeDeflate compression TIFF
lastmod: '2026-08-27'
og_description: 了解在使用 Aspose.Imaging for Java 将图像转换为 TIFF 时如何应用 deflate 压缩。针对高质量图像存储的分步指南。
og_image_alt: Guide showing Java code converting images to TIFF with AdobeDeflate
  compression using Aspose.Imaging
og_title: 如何在 Java 中对 TIFF 图像应用 deflate 压缩
schemas:
- author: Aspose
  dateModified: '2026-08-27'
  description: Learn how to apply deflate compression when converting images to TIFF
    using Aspose.Imaging for Java, ensuring high‑quality, efficient storage.
  headline: How to apply deflate compression to TIFF images in Java
  type: TechArticle
- description: Learn how to apply deflate compression when converting images to TIFF
    using Aspose.Imaging for Java, ensuring high‑quality, efficient storage.
  name: How to apply deflate compression to TIFF images in Java
  steps:
  - name: '**Archiving:** Preserve high‑resolution scans while keeping storage costs
      low.'
    text: '**Archiving:** Preserve high‑resolution scans while keeping storage costs
      low.'
  - name: '**Publishing:** Deliver print‑ready assets that meet industry‑standard
      TIFF specifications.'
    text: '**Publishing:** Deliver print‑ready assets that meet industry‑standard
      TIFF specifications.'
  - name: '**Medical imaging:** Transfer DICOM‑derived images without losing diagnostic
      detail.'
    text: '**Medical imaging:** Transfer DICOM‑derived images without losing diagnostic
      detail.'
  - name: '**Graphic design:** Store layered artwork in a single, lossless container
      for version control.'
    text: '**Graphic design:** Store layered artwork in a single, lossless container
      for version control.'
  type: HowTo
- questions:
  - answer: AdobeDeflate is a lossless TIFF compression algorithm that reduces file
      size by roughly 30‑50 % while keeping every pixel intact.
    question: What is AdobeDeflate compression?
  - answer: Yes—while the evaluation version works for testing, a purchased license
      unlocks full performance and removes evaluation watermarks.
    question: Do I need a license for production use?
  - answer: Absolutely. Aspose.Imaging supports PNG, JPEG, BMP, and many other raster
      formats as input for TIFF conversion.
    question: Can I convert PNG files to TIFF with this method?
  - answer: LZW typically yields similar size reductions but can be slower on very
      large images; AdobeDeflate often offers a better speed‑to‑size ratio.
    question: How does this compare to LZW compression?
  - answer: Aspose.Imaging for Java supports JDK 8 and higher; we recommend JDK 11
      or newer for optimal performance.
    question: What Java version is required?
  type: FAQPage
tags:
- image conversion
- Aspose.Imaging
- Java TIFF
- deflate compression
title: 如何在 Java 中对 TIFF 图像应用 deflate 压缩
url: /zh/java/format-specific-operations/aspose-imaging-java-tiff-adobedeflate-compression/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 掌握使用 Aspose.Imaging Java 进行图像转换：使用 AdobeDeflate 压缩将图像转换为 TIFF

在现代数字工作流中，**如何应用 deflate** 压缩在将图像转换为 TIFF 时是一个常见需求。无论您是归档医学扫描、准备可打印的图形，还是在网络上发送大量照片，TIFF 与 AdobeDeflate 结合可提供无损质量且占用更小的空间。本教程将带您完整了解整个过程——从设置 Aspose.Imaging for Java、加载光栅图像、配置 TIFF 选项，到最终保存压缩文件。

## 快速答案
- **第一步是什么？** 通过 Maven、Gradle 或直接下载 JAR 将 Aspose.Imaging for Java 添加到项目中。  
- **AdobeDeflate 提供哪种压缩？** 无损压缩，通常可将 TIFF 大小降低 30‑50 % 且不损失质量。  
- **我需要许可证吗？** 是的，试用版可用于评估，但永久许可证可解锁全部性能。  
- **我可以将 PNG 转换为 TIFF 吗？** 当然——任何 Aspose.Imaging 支持的光栅格式都可以转换。  
- **这适用于大图像吗？** 是的；AdobeDeflate 能处理多兆像素文件，同时保持内存使用适度。

## 什么是如何应用 deflate？
*如何应用 deflate* 是指使用 AdobeDeflate 算法压缩 TIFF 图像数据而不牺牲视觉保真度的过程。该算法内置于 Aspose.Imaging 的 `TiffOptions` 类中。通过选择此压缩，您可以保留每个像素，同时实现典型的 30‑50 % 文件大小缩减，使生成的 TIFF 适用于归档、打印和传输场景。

## 为什么在 TIFF 中使用 AdobeDeflate 压缩？
Aspose.Imaging 支持 **50+ 种输入和输出格式**，并且能够在不将整个文档加载到内存中的情况下处理 **多百页的 TIFF 文件**。AdobeDeflate 特别提供 **30‑50 % 的文件大小缩减**，同时保留每个像素，使其成为归档和打印流程的理想选择。此外，该算法提供快速的编码和解码速度，有助于在批处理环境中保持高吞吐量。

## 前提条件

- **必需的库：** Aspose.Imaging for Java（最新版本）。  
- **开发环境：** IntelliJ IDEA、Eclipse，或任何兼容 Java 的 IDE，使用 JDK 11 或更高版本。  
- **基础知识：** 熟悉 Java 文件 I/O 和异常处理。

## 设置 Aspose.Imaging for Java

将库添加到构建配置中。下面的代码块是占位符，您应将其替换为官方站点提供的实际 Maven/Gradle 代码片段。

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
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

如果您更喜欢手动下载，请从 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 获取最新的 JAR。

您可以从 [Aspose's website](https://releases.aspose.com/imaging/java/) 获取试用版或购买许可证。永久许可证可解锁全部性能并去除评估水印。

### 如何在 Java 中对 TIFF 图像应用 deflate 压缩？

加载源图像，使用 `CompressionType.AdobeDeflate` 配置 `TiffOptions`，然后保存结果。此三步模式在单一、内存高效的流程中完成整个转换。通过使用 try‑with‑resources 块，您可以确保本机资源自动释放，这在处理大图像或批量文件时尤为重要。

`RasterImage` 类是 Aspose.Imaging 的核心对象，表示内存中的任何光栅图像（PNG、JPEG、BMP 等）。加载后，您可以操作像素、更改分辨率或仅重新编码图像。

`TiffOptions` 类定义了 TIFF 文件的写入设置，例如压缩、分辨率和颜色模式。将 `Compression = CompressionType.AdobeDeflate` 设置为激活 deflate 算法。

`TiffFrame` 类表示 TIFF 文件中的单页或层。当您调用 `save` 时，Aspose.Imaging 使用您提供的选项写入该帧。

### 将图像加载为 RasterImage

```java
try (RasterImage image = (RasterImage) Image.load("YOUR_DOCUMENT_DIRECTORY/SampleTiff1.tiff")) {
    // Additional code will go here
}
```  
*说明：* `Image.load` 方法在 try‑with‑resources 块中将文件读取到 `RasterImage` 实例，确保本机资源自动释放。

### 配置 TIFF 选项

```java
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
options.setBitsPerSample(new int[] { 8, 8, 8 });
options.setPhotometric(TiffPhotometrics.Rgb);
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));
options.setResolutionUnit(TiffResolutionUnit.Inch);
options.setPlanarConfiguration(TiffPlanarConfig.Contiguous);
options.setCompression(TiffCompression.AdobeDeflate);
```  
*说明：* 通过配置 `TiffOptions`，您指定 AdobeDeflate 压缩，设置所需分辨率（例如，打印用 300 DPI），并选择合适的颜色模式。

### 保存转换后的图像

```java
try (TiffFrame tiffFrame = TiffFrame.fromRasterImage(image)) {
    TiffImage tiffImage = new TiffImage(tiffFrame);
    tiffImage.save("YOUR_OUTPUT_DIRECTORY/SavingRasterImage_out.tiff", options);
}
```  
*说明：* `TiffFrame` 包装光栅数据，`save` 使用先前定义的选项写入最终的 TIFF 文件。try‑with‑resources 模式确保文件句柄正确关闭。

## 实际应用

使用 AdobeDeflate 将图像转换为 TIFF 在许多领域都很有价值：

1. **归档：** 在保持低存储成本的同时保留高分辨率扫描。  
2. **出版：** 提供符合行业标准 TIFF 规范的可打印资产。  
3. **医学影像：** 传输 DICOM 派生的图像而不丢失诊断细节。  
4. **平面设计：** 将分层艺术作品存储在单个无损容器中，以便版本控制。

## 性能考虑

在处理大批量或高分辨率文件时，请遵循以下最佳实践：

- **内存管理：** 为大于 10 MP 的图像分配至少 **2 GB 堆内存**。  
- **批处理：** 使用循环一次处理一个文件；避免同时加载数十个图像。  
- **优化压缩：** AdobeDeflate 在速度和大小之间取得平衡——相较未压缩的 TIFF，预计可实现 **30‑50 % 的缩减**。

## 结论

您现在已经了解在使用 Aspose.Imaging for Java 将图像转换为 TIFF 时 **如何应用 deflate** 压缩。此方法提供无损质量、减小文件大小以及在高要求工作流中的强大性能。

**下一步**
- 尝试使用 LZW 或 CCITT Group 4 等替代压缩，以比较大小与速度。  
- 将转换逻辑集成到 REST 服务中，实现按需图像处理。  

**行动号召：** 在下一个项目中实现此方案，亲自体验存储节省！

## 常见问题

**Q: 什么是 AdobeDeflate 压缩？**  
A: AdobeDeflate 是一种无损 TIFF 压缩算法，可将文件大小大约降低 30‑50 %，同时保持每个像素完整。

**Q: 生产使用需要许可证吗？**  
A: 是的——虽然评估版可用于测试，但购买的许可证可解锁全部性能并去除评估水印。

**Q: 我可以使用此方法将 PNG 文件转换为 TIFF 吗？**  
A: 当然。Aspose.Imaging 支持 PNG、JPEG、BMP 以及许多其他光栅格式作为 TIFF 转换的输入。

**Q: 这与 LZW 压缩相比如何？**  
A: LZW 通常也能实现相似的大小缩减，但在非常大的图像上可能更慢；AdobeDeflate 通常提供更好的速度‑大小比。

**Q: 需要哪个 Java 版本？**  
A: Aspose.Imaging for Java 支持 JDK 8 及以上；我们推荐使用 JDK 11 或更高版本以获得最佳性能。

## 资源

- [文档](https://reference.aspose.com/imaging/java/)
- [下载](https://releases.aspose.com/imaging/java/)
- [购买](https://purchase.aspose.com/buy)
- [免费试用](https://releases.aspose.com/imaging/java/)
- [临时许可证](https://purchase.aspose.com/temporary-license/)
- [支持论坛](https://forum.aspose.com/c/imaging/14)

浏览这些链接以加深了解，充分利用 Aspose.Imaging for Java。

---

**最后更新：** 2026-08-27  
**测试使用：** Aspose.Imaging 24.11 for Java  
**作者：** Aspose

## 相关教程

- [学习在 Java 中创建多页 TIFF 和动画 GIF – Aspose.Imaging 动画教程](/imaging/java/animation-multi-frame-images/)
- [aspose imaging java – 将 TIFF 转换为 BMP 帧](/imaging/java/animation-multi-frame-images/extract-tiff-frames-to-bmp-aspose-imaging-java/)
- [如何使用 Aspose.Imaging Java 将 TIFF 转换为 GraphicsPath](/imaging/java/advanced-drawing-graphics/aspose-imaging-java-tiff-graphicspath-conversion/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}