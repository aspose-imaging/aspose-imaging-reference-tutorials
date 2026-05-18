---
date: 2026-05-18
description: 了解如何使用 Java 图像处理库 Aspose.Imaging 在图像中嵌入和检索 XMP 元数据，并提供逐步代码示例。
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: 图像中的 XMP 数据处理
schemas:
- author: Aspose
  dateModified: '2026-05-18'
  description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  headline: 'Java Image Processing Library: XMP with Aspose.Imaging'
  type: TechArticle
- description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  name: 'Java Image Processing Library: XMP with Aspose.Imaging'
  steps:
  - name: Specify Image Size and Tiff Options
    text: First, define the directory where your image will be stored and create a
      `Rectangle` to specify the size of the image. In this example, we use a TIFF
      image with certain options. `TiffOptions` configures format‑specific settings
      for the TIFF image.
  - name: Create a New Image
    text: Now, create a new image with the specified options. This image will be used
      to store the XMP metadata. `TiffImage` represents a TIFF image object, and `TiffFrame`
      defines an individual frame within it.
  - name: Create XMP Header and Trailer
    text: Create instances of XMP‑Header and XMP‑Trailer for your XMP metadata. These
      headers and trailers help define the metadata structure. `XmpHeaderPi` and `XmpTrailerPi`
      represent the XMP packet’s opening and closing sections.
  - name: Create XMP Meta Information
    text: Now, create an instance of XMP meta to set different attributes. You can
      add information like the author and description. `XmpMeta` holds the core metadata
      fields such as author and description.
  - name: Create XMP Packet Wrapper
    text: '`XmpPacketWrapper` is the container that holds the XMP header, trailer,
      and meta information in a single packet. It ensures the packet conforms to the
      XMP specification. `XmpPacketWrapper` packages the header, meta, and trailer
      into a single XMP packet.'
  - name: Add Photoshop Package
    text: To store Photoshop‑specific information, create a Photoshop package and
      set its attributes, such as city, country, and color mode. Then, add this package
      to the XMP metadata. `PhotoshopPackage` stores Photoshop‑specific metadata like
      city, country, and color mode.
  - name: Add Dublin Core Package
    text: For more general information, like author, title, and additional values,
      create a DublinCore package and set its attributes. Add this package to the
      XMP metadata as well. `DublinCorePackage` contains standard Dublin Core fields
      such as title, creator, and keywords.
  - name: Update XMP Metadata in the Image
    text: Update the XMP metadata into the image using the `setXmpData` method. This
      call writes the XMP packet into the image’s metadata section. `setXmpData` writes
      the XMP packet into the image’s metadata section.
  - name: Save the Image
    text: You can now save the image with the embedded XMP metadata on the disk or
      in a memory stream.
  - name: Load the Image and Retrieve XMP Metadata
    text: To retrieve the XMP metadata from the image, load the image from the memory
      stream or disk and access the XMP data via the `getXmpData` method. `getXmpData`
      reads the embedded XMP packet from the image. Congratulations! You've successfully
      learned how to handle XMP data in images using Aspose.Imagin
  type: HowTo
- questions:
  - answer: XMP is an XML‑based standard for embedding descriptive information directly
      inside files, enabling consistent metadata across applications.
    question: What is XMP metadata?
  - answer: It lets you tag images with author, copyright, keywords, and custom data,
      improving searchability and asset management without external databases.
    question: Why is XMP metadata important?
  - answer: Yes, Aspose.Imaging for Java provides methods to modify existing XMP packets
      and write them back to the file.
    question: Can I edit XMP metadata after embedding it in an image?
  - answer: A free trial is available for evaluation, but a paid license is required
      for production use. You can explore options on the [Aspose.Imaging for Java
      website](https://purchase.aspose.com/buy).
    question: Is Aspose.Imaging for Java a free tool?
  - answer: Visit the [Aspose.Imaging forums](https://forum.aspose.com/) for community
      assistance, or contact Aspose support directly for paid‑license customers.
    question: Where can I get help and support for Aspose.Imaging for Java?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: Java 图像处理库：使用 Aspose.Imaging 进行 XMP
url: /zh/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Imaging for Java 处理图像中的 XMP 数据

Aspose.Imaging 是一个 **java image processing library**，让您能够处理数十种光栅和矢量格式。在本教程中，您将学习如何使用 Aspose.Imaging for Java 在图像中嵌入和检索 XMP（可扩展元数据平台）数据。完成后，您将能够将作者、描述和自定义元数据直接存储在图像文件中，使其可搜索且自描述。

## 快速回答
- **What is XMP?** XMP 是一种标准化的基于 XML 的格式，用于在图像、PDF 和视频等文件中嵌入元数据。  
- **Which library handles XMP in Java?** Aspose.Imaging for Java 提供完整的 API 用于读取和写入 XMP 包。  
- **Do I need a license?** 免费试用可用于开发；生产环境需要商业许可证。  
- **How many image formats are supported?** 支持超过 150 种格式，包括 TIFF、JPEG、PNG、PSD 和 RAW。  
- **Can I process large images?** 可以——库能够处理高达 2 GB 的文件，而无需将整个图像加载到内存中。

## 什么是 XMP 元数据？
XMP 元数据是一种基于 XML 的标准，直接将描述性信息嵌入数字文件中。它实现了作者、版权、关键字和自定义数据在不同应用之间的一致存储。由于采用 XML，XMP 可以通过自定义命名空间进行扩展，开发者可以添加专有字段，同时保持与理解核心模式的工具兼容。这使得 XMP 成为长期资产管理和跨应用互操作性的理想选择。

## 为什么使用 Java 图像处理库来处理 XMP？
Aspose.Imaging for Java 支持 **150+ 图像格式**，并且能够以流式方式处理多千兆字节的文件，相比于朴素的全加载方式可将内存消耗降低约 80 %。该 API 还保证 XMP 包符合标准，确保与 Adobe Photoshop、Lightroom 等工具的兼容性。

## 前提条件

在开始之前，请确保具备以下前提条件：

- 在计算机上已设置 Java 开发环境。  
- 已安装 Aspose.Imaging for Java 库。您可以从 [Aspose.Imaging for Java website](https://releases.aspose.com/imaging/java/) 下载。  
- 对 Java 编程有基本了解。

## 导入包

首先在 Java 项目中导入必要的包。您可以在代码开头添加以下 import 语句：

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.xmp.XmpPackage;
import com.aspose.imaging.xmp.XmpPacketWrapper;
import com.aspose.imaging.xmp.XmpMeta;
import com.aspose.imaging.xmp.photoshop.ColorMode;
import com.aspose.imaging.xmp.photoshop.PhotoshopPackage;
import com.aspose.imaging.xmp.dc.DublinCorePackage;
import com.aspose.imaging.xmp.header.XmpHeaderPi;
import com.aspose.imaging.xmp.trailer.XmpTrailerPi;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

现在，让我们将示例拆解为一步步的指南：

## 如何使用 Java 图像处理库嵌入 XMP 元数据？

加载图像，创建 XMP 包，将包附加到图像并保存——全部只需几行简洁代码。Aspose.Imaging 的 `setXmpData` 方法直接将包写入文件，无需单独的元数据文件。该过程支持基于文件和基于流的图像，适用于 Web 服务和批处理作业。

### 步骤 1：指定图像尺寸和 Tiff 选项

首先，定义图像将存储的目录并创建一个 `Rectangle` 来指定图像尺寸。在本例中，我们使用带有特定选项的 TIFF 图像。`TiffOptions` 用于配置 TIFF 图像的格式特定设置。

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### 步骤 2：创建新图像

现在，使用指定的选项创建新图像。该图像将用于存储 XMP 元数据。`TiffImage` 表示 TIFF 图像对象，`TiffFrame` 定义其中的单个帧。

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### 步骤 3：创建 XMP Header 和 Trailer

为您的 XMP 元数据创建 XMP‑Header 和 XMP‑Trailer 实例。这些头部和尾部帮助定义元数据结构。`XmpHeaderPi` 和 `XmpTrailerPi` 分别表示 XMP 包的开头和结尾部分。

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### 步骤 4：创建 XMP 元信息

现在，创建 XMP 元信息实例以设置不同属性。您可以添加作者、描述等信息。`XmpMeta` 保存核心元数据字段，如作者和描述。

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### 步骤 5：创建 XMP Packet Wrapper

`XmpPacketWrapper` 是容器，用于在单个包中保存 XMP 头部、尾部和元信息。它确保包符合 XMP 规范。`XmpPacketWrapper` 将头部、元信息和尾部打包成一个 XMP 包。

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### 步骤 6：添加 Photoshop 包

为了存储 Photoshop 特定信息，创建 Photoshop 包并设置其属性，如城市、国家和颜色模式。随后，将此包添加到 XMP 元数据中。`PhotoshopPackage` 存储 Photoshop 特有的元数据，如城市、国家和颜色模式。

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### 步骤 7：添加 Dublin Core 包

对于更通用的信息，如作者、标题和其他值，创建 DublinCore 包并设置其属性。也将此包添加到 XMP 元数据中。`DublinCorePackage` 包含标准的 Dublin Core 字段，如标题、创建者和关键字。

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### 步骤 8：在图像中更新 XMP 元数据

使用 `setXmpData` 方法将 XMP 元数据写入图像。此调用将 XMP 包写入图像的元数据部分。`setXmpData` 将 XMP 包写入图像的元数据区域。

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### 步骤 9：保存图像

现在，您可以将嵌入 XMP 元数据的图像保存到磁盘或内存流中。

```java
    image.save(ms);
```

### 步骤 10：加载图像并检索 XMP 元数据

要从图像中检索 XMP 元数据，您可以从内存流或磁盘加载图像，并通过 `getXmpData` 方法访问 XMP 数据。`getXmpData` 读取图像中嵌入的 XMP 包。

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

恭喜！您已成功学习如何使用 Aspose.Imaging for Java 处理图像中的 XMP 数据。这使您能够在图像文件中存储和检索有价值的元数据。

## 常见问题及解决方案

- **Metadata not appearing in Photoshop:** 确保 XMP 包遵循正确的 XML 架构；Aspose.Imaging 会自动验证，但自定义命名空间可能需要注册。  
- **Large TIFF files cause OutOfMemoryError:** 使用 `Compression` 设置为 `LZW` 的 `TiffOptions` 并启用流式处理（`loadOptions.setBufferSize`），以保持低内存使用。  
- **Unexpected character encoding:** XMP 需要 UTF‑8；始终使用 `StandardCharsets.UTF_8` 传递字符串，以避免乱码。

## 常见问答

**Q: 什么是 XMP 元数据？**  
A: XMP 是一种基于 XML 的标准，用于将描述性信息直接嵌入文件中，实现跨应用的一致元数据。

**Q: 为什么 XMP 元数据重要？**  
A: 它允许您为图像标记作者、版权、关键字和自定义数据，提高搜索性和资产管理，而无需外部数据库。

**Q: 嵌入图像后我可以编辑 XMP 元数据吗？**  
A: 可以，Aspose.Imaging for Java 提供方法修改现有的 XMP 包并写回文件。

**Q: Aspose.Imaging for Java 是免费工具吗？**  
A: 提供免费试用供评估，但生产环境需要付费许可证。您可以在 [Aspose.Imaging for Java website](https://purchase.aspose.com/buy) 上了解选项。

**Q: 在哪里可以获得 Aspose.Imaging for Java 的帮助和支持？**  
A: 访问 [Aspose.Imaging forums](https://forum.aspose.com/) 获取社区帮助，或直接联系 Aspose 支持（付费许可证客户）。

## 结论

在本教程中，我们探讨了如何使用 Aspose.Imaging for Java 这款领先的 **java image processing library** 在图像中处理 XMP 元数据。通过遵循步骤指南，您可以轻松嵌入、更新和检索 XMP 数据，为数字资产添加可搜索、符合标准的元数据。

---

**最后更新：** 2026-05-18  
**测试环境：** Aspose.Imaging for Java 24.12  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [掌握 Java 图像处理：使用 Aspose.Imaging 修改 EXIF 数据](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [使用 Aspose.Imaging 的 Java 图像处理：加载、增强和保存图像](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [使用 Aspose.Imaging 库的高级 Java 图像处理](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Specify the size of image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// create the brand new image just for sample purposes
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// create an instance of XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// create an instance of Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// create an instance of XMP meta class to set different attributes
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// create an instance of XmpPacketWrapper that contains all metadata
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// create an instance of Photoshop package and set photoshop attributes
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// add photoshop package into XMP metadata
	xmpData.addPackage(photoshopPackage);
	// create an instance of DublinCore package and set dublinCore attributes
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// add dublinCore Package into XMP metadata
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// update XMP metadata into image
	image.setXmpData(xmpData);
	// Save image on the disk or in memory stream
	image.save(ms);
	// Load the image from memory stream or from disk to read/get the metadata
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Getting the XMP metadata
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Use package data ...
		}
	}
}
        
```