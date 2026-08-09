---
date: '2026-07-08'
description: 了解如何使用 Aspose.Imaging for Java 从 DjVu 导出 TIFF。一步步指南，涵盖加载、页面选择和导出选项。
keywords:
- how to export tiff
- java image processing
- maven aspose imaging
- how to load djvu
lastmod: '2026-07-08'
og_description: 了解如何在 Java 中使用 Aspose.Imaging 从 DjVu 导出 TIFF。遵循我们的分步教程，实现快速可靠的图像转换。
og_image_alt: Guide showing Java code to convert DjVu pages to TIFF with Aspose.Imaging
og_title: 如何导出 TIFF – Aspose.Imaging Java 指南
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: Learn how to export TIFF from DjVu using Aspose.Imaging for Java. Step-by-step
    guide covering loading, page selection, and export options.
  headline: How to Export TIFF – Load and Export DjVu Pages in Java with Aspose.Imaging
  type: TechArticle
- description: Learn how to export TIFF from DjVu using Aspose.Imaging for Java. Step-by-step
    guide covering loading, page selection, and export options.
  name: How to Export TIFF – Load and Export DjVu Pages in Java with Aspose.Imaging
  steps:
  - name: '**Archival Systems** – Preserve scanned documents in a universally accepted
      format.'
    text: '**Archival Systems** – Preserve scanned documents in a universally accepted
      format.'
  - name: '**Document Review Workflows** – Pull out only the pages that need annotation.'
    text: '**Document Review Workflows** – Pull out only the pages that need annotation.'
  - name: '**Integration with DMS** – Feed TIFF images into existing document‑management
      pipelines that do not understand DjVu.'
    text: '**Integration with DMS** – Feed TIFF images into existing document‑management
      pipelines that do not understand DjVu.'
  type: HowTo
- questions:
  - answer: '`DjvuImage` represents a DjVu document in memory.'
    question: What is the main class for DjVu handling?
  - answer: Just two lines after loading the image.
    question: How many lines of code are needed to export a page to TIFF?
  - answer: '`com.aspose:aspose-imaging` (version 25.5+).'
    question: Which Maven artifact provides DjVu support?
  - answer: Yes, use `IntRange` to specify a range.
    question: Can I export multiple pages at once?
  - answer: A full license is required; a temporary trial is available.
    question: Do I need a license for production?
  type: FAQPage
tags:
- convert DjVu
- Aspose.Imaging
- Java image conversion
title: 如何导出 TIFF – 在 Java 中使用 Aspose.Imaging 加载并导出 DjVu 页面
url: /zh/java/format-conversion-export/load-export-djvu-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 如何导出 TIFF – 在 Java 中使用 Aspose.Imaging 加载并导出 DjVu 页面

## 介绍

如果您需要在 Java 应用程序中**导出 TIFF**（从 DjVu 文档），您来对地方了。DjVu 是一种用于扫描文档的紧凑格式，但许多下游系统需要 TIFF。本教程将指导您加载 DjVu 文件，挑选所需页面，并使用 Aspose.Imaging for Java 将其导出为高质量的 TIFF 图像。完成后，您将拥有一个可重用的代码片段，可嵌入任何基于 Java 的图像处理流水线。

**您将学习**
- 如何在 Java 中使用 Aspose.Imaging 加载 DjVu 图像  
- 将特定 DjVu 页面导出为 TIFF 格式  
- 配置导出选项并了解关键参数  

在深入之前，请确保您的开发环境满足以下列出的先决条件。

## 快速答案
- **DjVu 处理的主类是什么？** `DjvuImage` 表示内存中的 DjVu 文档。  
- **导出页面为 TIFF 需要多少行代码？** 加载图像后只需两行代码。  
- **哪个 Maven 构件提供 DjVu 支持？** `com.aspose:aspose-imaging`（版本 25.5+）。  
- **我可以一次导出多个页面吗？** 可以，使用 `IntRange` 指定范围。  
- **生产环境需要许可证吗？** 需要完整许可证；提供临时试用版。

## 什么是“导出 TIFF”？
**“导出 TIFF”** 是指将图像或文档页面转换为标记图像文件格式（TIFF）的过程，这是一种广泛用于归档和印刷的无损格式。Aspose.Imaging 在一次 API 调用中完成此转换，同时保留分辨率和压缩设置。该转换保留所有视觉细节，使其适用于高质量的归档存储和下游处理。

## 为什么在 Java 图像处理时使用 Aspose.Imaging？
Aspose.Imaging 支持 **150+** 种输入和输出格式，能够处理高达 **5,000 页** 的文件而无需将整个文档加载到内存中，并提供线程安全的操作。这些量化的能力使其成为高吞吐量 Java 图像处理工作负载的可靠选择，尤其是在处理需要批量转换且内存开销最小的大型文档集时。

## 先决条件

- **Aspose.Imaging for Java 库** – 版本 25.5 或更高。  
- **Java 开发工具包 (JDK)** – 8 或更高，已在您的机器上正确配置。  
- **基本的 Java 知识** – 您应熟悉文件 I/O 和异常处理。

## 如何设置 Maven Aspose Imaging？

要在 Maven 项目中包含 Aspose.Imaging，请将依赖项添加到项目的 `pom.xml` 中。Maven 将下载该库及其传递依赖，使 API 可用于编译和运行时。添加代码片段后，运行 `mvn clean install` 以确保构件已解析并成功构建项目。

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

## 如何设置 Gradle Aspose Imaging？

对于 Gradle 构建，在 `build.gradle` 文件中声明 Aspose.Imaging 依赖。Gradle 将从 Maven Central 获取该库，使您能够在 Java 代码中使用 API。更新脚本后，刷新项目以下载 JAR 并同步依赖。

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

## 直接下载

您也可以从 [Aspose.Imaging releases](https://releases.aspose.com/imaging/java/) 下载最新的 JAR。

### 许可证获取

- **免费试用** – 获取用于评估的临时许可证。  
- **购买** – 考虑购买完整许可证用于生产环境。

## 初始化和设置

在使用任何 API 之前，必须初始化库。`License` 类用于将您的 Aspose.Imaging 许可证文件应用于库，确保在没有评估限制的情况下获得完整功能。

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path/to/your/license.lic");
```

## 如何加载 DjVu？

DjvuImage 是表示内存中 DjVu 文件的顶层对象。要读取 DjVu 文档，调用带有文件路径的静态 `Image.load()` 方法；该方法返回一个 `Image` 实例，您需要将其强制转换为 `DjvuImage`。`Image.load()` 是一个静态方法，用于读取图像文件并返回表示已加载内容的 `Image` 对象。

```java
   String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "/Sample.djvu";
   ```

```java
   try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
       // The image is now loaded and ready for further processing.
   }
   ```

### 故障排除

- 确认文件路径正确且可访问。  
- 将加载调用包装在 try‑catch 块中，以处理 `IOException` 或 `ImageLoadException`。

## 如何导出 TIFF？

将 DjVu 页面导出为 TIFF 包括创建一个 `TiffOptions` 对象以指定压缩、分辨率等设置，然后在目标页面上调用 `save()` 方法。`TiffOptions` 是用于 TIFF 输出的配置类，例如压缩类型和颜色深度。使用 `IntRange` 选择要转换的页面，然后遍历并将每个页面保存为单独的 TIFF 文件。

创建输出目录，设置 `TiffOptions`，使用 `IntRange` 选择页面，最后将每个页面保存为 TIFF 文件。

```java
   String outputDir = "YOUR_OUTPUT_DIRECTORY" + "/ConvertDjvuPagesToTiff_out.tiff";
   ```

```java
   TiffOptions exportOptions = new TiffOptions(TiffExpectedFormat.TiffDeflateBw);
   ```

```java
   IntRange range = new IntRange(0, 2); // Export the first three pages.
   exportOptions.setMultiPageOptions(new DjvuMultiPageOptions(range));
   ```

```java
   try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
       image.save(outputDir, exportOptions);
   }
   ```

### 常见陷阱

- 确保 `outputDir` 存在；否则 `save()` 将抛出异常。  
- 记住页面索引是 **从零开始** 的；第 1 页的索引为 0。  

## 实际应用

1. **归档系统** – 将扫描文档保存在通用接受的格式中。  
2. **文档审阅工作流** – 仅提取需要注释的页面。  
3. **与 DMS 集成** – 将 TIFF 图像输入到不支持 DjVu 的现有文档管理流水线中。

## 性能考虑

- 使用 **try‑with‑resources** 自动关闭流并释放内存。  
- 将文件分块处理（例如，每次 10 页），以保持堆占用低。  
- 对于黑白扫描，首选 `TiffCompression.CCITT4`，以在不损失质量的情况下减小文件大小。

## 常见问题

**Q:** 如何在我的项目中安装 Aspose.Imaging for Java？  
**A:** 如上所示使用 Maven 或 Gradle，或直接从 [Aspose's releases page](https://releases.aspose.com/imaging/java/) 下载。

**Q:** 我可以将 DjVu 图像导出为除 TIFF 之外的其他格式吗？  
**A:** 可以，Aspose.Imaging 还支持 PNG、JPEG、BMP 等多种格式。

**Q:** 如果我的许可证文件未被识别该怎么办？  
**A:** 验证许可证路径是否正确，并确保在使用任何其他 API 之前调用 `License.setLicense()`。

**Q:** 如何高效处理非常大的 DjVu 文件？  
**A:** 将文档分成较小的页面范围处理，并及时释放每个 `DjvuImage` 实例，以避免内存压力。

**Q:** Aspose.Imaging 商业使用免费吗？  
**A:** 临时试用许可证是免费的，但生产部署需要购买许可证。

## 资源

- **文档**: [Aspose.Imaging Java API Reference](https://reference.aspose.com/imaging/java/)  
- **下载**: [Aspose.Imaging for Java Releases](https://releases.aspose.com/imaging/java/)  
- **购买**: [Buy Aspose.Imaging](https://purchase.aspose.com/buy)  
- **免费许可证**: [Get a Free License](https://releases.aspose.com/imaging/java/)  
- **临时许可证**: [Request a Temporary License](https://purchase.aspose.com/temporary-license/)  
- **支持**: [Aspose Community Forum](https://forum.aspose.com/c/imaging/14)

通过掌握上述步骤，您可以在任何基于 Java 的解决方案中可靠地 **导出 TIFF**（从 DjVu 文件）。祝编码愉快！

**最后更新：** 2026-07-08  
**测试环境：** Aspose.Imaging 25.5 for Java  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [使用 Aspose.Imaging for Java 创建多页 TIFF：完整指南](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [使用 Aspose.Imaging for Java 将 DjVu 转换为 PDF - 步骤指南](/imaging/java/image-loading-saving/convert-djvu-to-pdf-aspose-imaging-java/)
- [使用 Aspose.Imaging 将 DJVU 转换为 BMP（Java）：步骤指南](/imaging/java/format-conversion-export/export-djvu-pages-bmp-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}