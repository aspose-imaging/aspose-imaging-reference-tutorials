---
title: 使用 Aspose.Imaging for Java 处理图像中的 XMP 数据
linktitle: 图像中的 XMP 数据处理
second_title: Aspose.Imaging Java 图像处理 API
description: 了解如何使用 Aspose.Imaging for Java 处理图像中的 XMP 元数据。嵌入和检索元数据以增强您的图像文件。
type: docs
weight: 16
url: /zh/java/document-conversion-and-processing/xmp-data-handling-in-images/
---
Aspose.Imaging for Java 是一个多功能且功能强大的库，用于处理各种格式的图像。本教程将指导您完成使用 Aspose.Imaging for Java 处理图像中的 XMP（可扩展元数据平台）数据的过程。 XMP 是一种将元数据嵌入图像文件的标准，允许您存储作者、描述等有价值的信息。

## 先决条件

在开始之前，请确保您具备以下先决条件：

- 在您的计算机上设置 Java 开发环境。
-  Aspose.Imaging for Java 库已安装。您可以从[Aspose.Imaging for Java 网站](https://releases.aspose.com/imaging/java/).
- 对 Java 编程有基本的了解。

## 导入包

首先将必要的包导入到您的 Java 项目中。您可以在代码开头添加以下导入语句：

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

现在，让我们将示例分解为分步指南：

## 第 1 步：指定图像大小和 Tiff 选项

首先，定义存储图像的目录并创建一个矩形来指定图像的大小。在此示例中，我们使用带有某些选项的 Tiff 图像。

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## 第 2 步：创建新图像

现在，使用指定的选项创建一个新图像。该图像将用于存储 XMP 元数据。

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## 第 3 步：创建 XMP 标头和标尾

为您的 XMP 元数据创建 XMP-Header 和 XMP-Trailer 的实例。这些标头和标尾有助于定义元数据结构。

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## 步骤 4：创建 XMP 元信息

现在，创建 XMP 元的实例来设置不同的属性。您可以添加作者和描述等信息。

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## 第 5 步：创建 XMP 数据包包装器

创建包含 XMP 标头、尾部和元信息的 XmpPacketWrapper 实例。

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## 第 6 步：添加 Photoshop 包

要存储 Photoshop 特定信息，请创建 Photoshop 包并设置其属性，例如城市、国家/地区和颜色模式。然后，将此包添加到 XMP 元数据中。

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## 第7步：添加都柏林核心包

有关更多一般信息，例如作者、标题和其他值，请创建 DublinCore 包并设置其属性。也将此包添加到 XMP 元数据中。

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## 步骤 8：更新映像中的 XMP 元数据

使用以下命令将 XMP 元数据更新到图像中`setXmpData`方法。

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## 第9步：保存图像

现在，您可以将带有嵌入式 XMP 元数据的图像保存在磁盘或内存流中。

```java
    image.save(ms);
```

## 第 10 步：加载图像并检索 XMP 元数据

要从图像中检索 XMP 元数据，请从内存流或磁盘加载图像并访问 XMP 数据。

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            //使用包数据...
        }
    }
}
```

恭喜！您已经成功学习了如何使用 Aspose.Imaging for Java 处理图像中的 XMP 数据。这允许您在图像文件中存储和检索有价值的元数据。

## 结论

在本教程中，我们探索了如何使用 Aspose.Imaging for Java 处理图像中的 XMP 元数据。通过遵循分步指南，您可以轻松地在图像文件中嵌入和检索元数据，从而增强其信息和可用性。

## 常见问题解答

### Q1：什么是 XMP 元数据？

A1：XMP（可扩展元数据平台）是将元数据嵌入到各种类型文件（包括图像）中的标准。它允许您在文件本身中存储作者、标题、描述等信息。

### 问题 2：为什么 XMP 元数据很重要？

A2：XMP 元数据对于组织和分类数字资产至关重要。它有助于归属所有权、描述内容以及向图像等文件添加上下文，使它们更易于访问和有意义。

### 问题 3：将 XMP 元数据嵌入图像后可以编辑吗？

A3：是的，您可以在将 XMP 元数据嵌入图像后对其进行编辑。 Aspose.Imaging for Java 提供了根据需要修改和更新元数据属性的工具。

### Q4：Aspose.Imaging for Java 是免费工具吗？

 A4：Aspose.Imaging for Java 提供免费试用版，但要获得完整功能和扩展使用，需要付费许可证。您可以探索[Aspose.Imaging for Java 网站](https://purchase.aspose.com/buy).

### Q5：我在哪里可以获得 Aspose.Imaging for Java 的帮助和支持？

 A5：如果您遇到任何问题或有与 Aspose.Imaging for Java 相关的疑问，您可以访问[Aspose.Imaging 论坛](https://forum.aspose.com/)以获得社区的支持和指导。



## 完整的源代码
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
//通过定义矩形指定图像的大小
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
//创建全新图像仅用于示例目的
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	//创建 XMP-Header 的实例
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	//创建 Xmp-TrailerPi 的实例
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	//创建 XMP 元类的实例来设置不同的属性
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	//创建包含所有元数据的 XmpPacketWrapper 实例
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	//创建 Photoshop 包的实例并设置 Photoshop 属性
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	//将 Photoshop 包添加到 XMP 元数据中
	xmpData.addPackage(photoshopPackage);
	//创建 DublinCore 包的实例并设置 dublinCore 属性
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	//将 dublinCore 包添加到 XMP 元数据中
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	//将 XMP 元数据更新到图像中
	image.setXmpData(xmpData);
	//将图像保存在磁盘或内存流中
	image.save(ms);
	//从内存流或磁盘加载图像以读取/获取元数据
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		//获取 XMP 元数据
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			//使用包数据...
		}
	}
}
        
```