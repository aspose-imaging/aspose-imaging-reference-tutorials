---
date: '2026-09-28'
description: 了解如何使用 ccittfax3 compression java 与 Aspose.Imaging 创建多页 TIFF 文件。高效地扫描、归档，并在文档工作流中减小文件大小。
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: 一步步了解如何使用 ccittfax3 compression java 与 Aspose.Imaging 构建高效的多页 TIFF
  文件，以用于扫描和归档。
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: 如何使用 ccittfax3 compression java 创建多页 TIFF
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: 如何使用 ccittfax3 compression java 创建多页 TIFF
url: /zh/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 掌握使用 Aspose.Imaging 的 ccittfax3 压缩 Java 创建多页 TIFF

## 简介

如果您需要在保持文件大小低的同时归档大量扫描文档，**ccittfax3 compression java** 是首选解决方案。本教程将向您展示如何使用 Aspose.Imaging 在 Java 中生成带有 CCITTFAX3 压缩的多页 TIFF 文件。您将了解为何此压缩对单色扫描效果极佳，如何配置库，以及如何将每页添加为帧。

**您将学习**
- 如何将 Aspose.Imaging 添加到 Java 项目中。
- 如何为 CCITTFAX3 压缩配置 `TiffOptions`。
- 如何创建 `TiffImage`，调整源图像大小，并将其添加为帧。
- 如何高效保存最终的多页 TIFF。

让我们一起走完整个实现过程。

## 快速答案
- **CCITTFAX3 压缩的主要优势是什么？** 黑白扫描的文件大小可减少高达 80%。  
- **哪个库提供内置支持？** Aspose.Imaging for Java，版本 25.5+。  
- **开发是否需要许可证？** 免费试用许可证可用于所有功能；生产环境需要付费许可证。  
- **我可以处理数百页吗？** 可以——Aspose.Imaging 会流式处理页面，保持低内存使用。  
- **代码是否兼容 Java 11 及更高版本？** 完全兼容；API 目标为 Java 8+。

## 什么是 ccittfax3 compression java？
`CCITTFAX3` 是一种无损的单色压缩算法，专为传真和扫描文档图像设计。它将每个像素编码为单个位，在提供高质量输出的同时显著缩小文件大小——相较未压缩的 TIFF，通常可减少 70‑80%。这使其非常适合归档必须保持原始质量的黑白文档。

## 为什么在此任务中使用 Aspose.Imaging？
Aspose.Imaging 支持 **100+** 输入和输出格式，包括 PDF、PNG、JPEG 和 TIFF。其流式架构能够处理 **数百页** 的 TIFF 文件，而无需将整个文档加载到内存中，非常适合大规模归档项目。

## 前提条件

- **Java Development Kit (JDK)** 8 或更高版本已安装。
- **IDE** 如 IntelliJ IDEA 或 Eclipse。
- **Maven** 或 **Gradle** 用于依赖管理。
- 基本的 Java 知识（类、对象、集合）。

## 为 Java 设置 Aspose.Imaging

将库添加到您的构建文件中。

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```  

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

### 直接下载

您也可以从 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下载最新的 JAR。

### 获取许可证

免费试用许可证可在 [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/) 获取。生产使用时，请购买永久许可证或在 [Aspose Purchase](https://purchase.aspose.com/temporary-license/) 申请临时许可证。

有关详细的 API 用法，请参阅 Aspose.Imaging for Java 的 [documentation](https://reference.aspose.com/imaging/java/)。

### 基本初始化

添加依赖后，按如下方式初始化库。

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## 如何为多页 TIFF 配置 ccittfax3 compression java？

`TiffOptions` 是一个定义 TIFF 文件输出格式和压缩设置的类。使用 `CCITTGroup3FaxCompression` 枚举加载 `TiffOptions` 对象，然后设置输出文件源。此两步配置为单色压缩做好准备，并确保随后添加的每页都使用 CCITTFAX3 算法编码，从而在保持图像质量的同时显著减小文件大小。

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## 如何在 Java 中创建 TiffImage 实例？

`TiffImage` 表示内存中的多页 TIFF 文档，并提供操作其帧的方法。首先，定义所有页面共享的宽度和高度。然后使用先前创建的 `TiffOptions` 实例化 `TiffImage`。`TiffImage` 对象充当各帧的容器，允许您在保存最终文件之前添加、删除或重新排序页面。

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## 如何从文件夹加载并调整源图像大小？

过滤目标目录中的 JPEG 文件，读取每张图像，并将其调整为匹配 TIFF 画布的大小。在添加帧之前进行大小调整可降低内存消耗并加快保存操作。通过将每个源图像转换为所需的尺寸和像素格式，您可以保证页面布局一致，并避免在将帧追加到 TIFF 文档时出现运行时错误。

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## 如何将每张图像作为帧添加到多页 TIFF？

`TiffFrame` 是一个在 TIFF 中保存单页图像及其关联元数据的对象。遍历已调整大小的图像，创建新的 `TiffFrame`，并将其追加到 `TiffImage`。每个帧在最终文档中成为单独的页面，库会自动处理必要的元数据更新，如页数和偏移量，确保生成有效的多页 TIFF 结构。

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## 如何保存最终的多页 TIFF 文件？

在 `TiffImage` 实例上调用 `save` 方法，并传入所需的输出路径。库会自动使用 CCITTFAX3 压缩写入所有帧，高效地将数据流式写入磁盘，并关闭任何底层资源。保存操作完成后，生成的文件包含所有页面，并使用指定的压缩，准备好用于分发或归档。

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## 实际应用

- **文档归档：** 以最小的存储开销存储扫描的合同、发票或法律记录。  
- **医学影像：** 在保持诊断细节的同时压缩放射学扫描。  
- **印刷生产：** 生成打印机可直接使用的多页打印作业。

## 性能考虑因素

- 使用保持宽高比的 `ResizeOptions` 以避免失真。  
- 在添加帧后关闭每个 `Image` 对象，以释放本机内存。  
- 对于非常大的批次，使用并行流处理文件，并异步写入每个 TIFF 段。

## 常见陷阱与故障排除

- **Incorrect pixel format:** CCITTFAX3 仅适用于 1 位（黑白）图像。在调整大小之前将彩色图像转换为灰度。  
- **Memory leaks:** 始终对临时 `Image` 对象调用 `dispose()`；否则本机缓冲区将保持分配状态。  
- **File size not reduced:** 确保已设置 `TiffOptions` 的 compression 属性；否则将使用默认（无压缩）。

## 常见问题

**Q: 我可以将此方法用于彩色图像吗？**  
A: CCITTFAX3 仅限于单色数据；彩色图像请改用 JPEG 或 LZW 压缩。

**Q: Aspose.Imaging 是否支持对超大 TIFF 进行流式处理？**  
A: 是的——库会将每个帧直接写入输出流，即使是数千页也能保持低内存使用。

**Q: 如何以编程方式应用临时许可证？**  
A: 使用 `License license = new License(); license.setLicense("Aspose.Total.Java.lic");` 加载 `.lic` 文件。

**Q: 是否有办法在保存前预览 TIFF？**  
A: 您可以将每个 `TiffFrame` 渲染为 `BufferedImage`，并在 Swing 组件中显示。

**Q: 官方支持哪些 Java 版本？**  
A: Aspose.Imaging 支持 Java 8 至 Java 21，包括 LTS 版本。

## 结论

您现在拥有使用 Aspose.Imaging 通过 **ccittfax3 compression java** 创建多页 TIFF 文件的完整、可投入生产的工作流。按照上述步骤，您可以高效地归档海量文档集合，同时保持低存储成本和高图像质量。探索 Aspose.Imaging 的其他功能——如 OCR、元数据处理和格式转换——以进一步提升文档处理流水线。

---

**最后更新：** 2026-09-28  
**测试环境：** Aspose.Imaging 25.5 for Java  
**作者：** Aspose

## 相关教程

- [如何使用 Aspose.Imaging for Java 创建多页 TIFF – 完整指南](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [如何在 Java 中使用 LZW 压缩减小图像文件大小](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [使用 Aspose.Imaging for Java 拆分多页 TIFF 帧](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}