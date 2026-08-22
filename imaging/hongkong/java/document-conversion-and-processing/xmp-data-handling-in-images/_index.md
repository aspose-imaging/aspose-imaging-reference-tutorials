---
date: 2026-05-18
description: 了解如何使用 Java 圖像處理函式庫 Aspose.Imaging 在影像中嵌入與擷取 XMP 中繼資料，並提供逐步程式碼示例。
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: 影像中的 XMP 資料處理
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
title: Java 圖像處理函式庫：XMP 與 Aspose.Imaging
url: /zh-hant/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Imaging for Java 處理圖像中的 XMP 資料

Aspose.Imaging 是一個 **java image processing library**，讓您能夠處理數十種點陣圖與向量格式。在本教學中，您將學會如何使用 Aspose.Imaging for Java 在圖像中嵌入與取得 XMP（Extensible Metadata Platform）資料。完成後，您即可將作者、說明與自訂中繼資料直接儲存於圖像檔案內，使其具備可搜尋且自我描述的特性。

## 快速解答
- **什麼是 XMP？** XMP 是一種標準化的基於 XML 的格式，用於在圖像、PDF 和影片等檔案中嵌入中繼資料。  
- **哪個函式庫在 Java 中處理 XMP？** Aspose.Imaging for Java 提供完整的 API 以讀寫 XMP 封包。  
- **我需要授權嗎？** 免費試用可用於開發；商業授權則是正式上線的必要條件。  
- **支援多少種圖像格式？** 超過 150 種，包括 TIFF、JPEG、PNG、PSD 以及 RAW。  
- **我可以處理大型圖像嗎？** 可以 — 函式庫能在不將整張圖像載入記憶體的情況下處理高達 2 GB 的檔案。

## 什麼是 XMP 中繼資料？
XMP 中繼資料是一種基於 XML 的標準，直接將描述性資訊嵌入數位檔案中。它能在不同應用程式間一致地儲存作者、版權、關鍵字與自訂資料。由於採用 XML，XMP 可透過自訂命名空間擴充，讓開發者加入專屬欄位，同時仍與支援核心結構的工具相容。此特性使 XMP 成為長期資產管理與跨應用程式互通的理想選擇。

## 為什麼要使用 Java 圖像處理函式庫來處理 XMP？
Aspose.Imaging for Java 支援 **150+ 圖像格式**，且能以串流方式處理多 GB 的檔案，較傳統一次載入整張圖像的作法可降低高達 80 % 的記憶體使用量。API 亦保證 XMP 封包符合標準，確保與 Adobe Photoshop、Lightroom 等工具的相容性。

## 前置條件

在開始之前，請確保您已具備以下條件：

- 在電腦上已設定 Java 開發環境。  
- 已安裝 Aspose.Imaging for Java 函式庫。您可從 [Aspose.Imaging for Java 網站](https://releases.aspose.com/imaging/java/) 下載。  
- 具備基本的 Java 程式設計知識。

## 匯入套件

先將必要的套件匯入您的 Java 專案。您可以在程式碼開頭加入以下 import 陳述式：

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

現在，讓我們將範例拆解為逐步說明：

## 如何使用 Java 圖像處理函式庫嵌入 XMP 中繼資料？

載入圖像、建立 XMP 封包、將封包附加至圖像，最後儲存——全部只需幾行簡潔程式碼。Aspose.Imaging 的 `setXmpData` 方法會直接將封包寫入檔案，無需額外的中繼資料檔。此流程同時支援檔案型與串流型圖像，適合 Web 服務與批次作業。

### 步驟 1：指定圖像尺寸與 Tiff 選項

首先定義圖像儲存的目錄，並建立 `Rectangle` 以指定圖像尺寸。此範例使用 TIFF 圖像並設定特定選項。`TiffOptions` 用於配置 TIFF 圖像的格式專屬設定。

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### 步驟 2：建立新圖像

接著使用先前指定的選項建立新圖像。此圖像將用來儲存 XMP 中繼資料。`TiffImage` 代表 TIFF 圖像物件，`TiffFrame` 定義其中的單一影格。

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### 步驟 3：建立 XMP 標頭與尾部

為您的 XMP 中繼資料建立 XMP‑Header 與 XMP‑Trailer 實例。這些標頭與尾部協助定義中繼資料的結構。`XmpHeaderPi` 與 `XmpTrailerPi` 分別代表 XMP 封包的開頭與結尾區段。

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### 步驟 4：建立 XMP 中繼資訊

現在建立 XMP 中繼資訊實例，以設定各種屬性。您可以加入作者、說明等資訊。`XmpMeta` 保存核心的中繼資料欄位，如作者與說明。

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### 步驟 5：建立 XMP 封包包裝器

`XmpPacketWrapper` 是容納 XMP 標頭、尾部與中繼資訊的封裝器，確保封包符合 XMP 規範。`XmpPacketWrapper` 會將標頭、內容與尾部打包成單一 XMP 封包。

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### 步驟 6：加入 Photoshop 套件

若要儲存 Photoshop 專屬資訊，建立 Photoshop 套件並設定其屬性，例如城市、國家與色彩模式。然後將此套件加入 XMP 中繼資料。`PhotoshopPackage` 儲存 Photoshop 專屬的中繼資料，如城市、國家與色彩模式。

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### 步驟 7：加入 Dublin Core 套件

為了提供更一般性的資訊（如作者、標題與其他值），建立 DublinCore 套件並設定其屬性。亦將此套件加入 XMP 中繼資料。`DublinCorePackage` 包含標準的 Dublin Core 欄位，如標題、創作者與關鍵字。

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### 步驟 8：在圖像中更新 XMP 中繼資料

使用 `setXmpData` 方法將 XMP 中繼資料寫入圖像。此呼叫會將 XMP 封包寫入圖像的中繼資料區段。

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### 步驟 9：儲存圖像

現在您可以將帶有嵌入 XMP 中繼資料的圖像儲存至磁碟或記憶體串流。

```java
    image.save(ms);
```

### 步驟 10：載入圖像並取得 XMP 中繼資料

若要從圖像取得 XMP 中繼資料，從記憶體串流或磁碟載入圖像，並透過 `getXmpData` 方法存取 XMP 資料。`getXmpData` 會讀取圖像中嵌入的 XMP 封包。

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

恭喜！您已成功學會如何使用 Aspose.Imaging for Java 處理圖像中的 XMP 資料。這讓您能在圖像檔案內儲存與取得寶貴的中繼資料。

## 常見問題與解決方案

- **中繼資料未在 Photoshop 中顯示：** 確認 XMP 封包符合正確的 XML 架構；Aspose.Imaging 會自動驗證，但自訂命名空間可能需要註冊。  
- **大型 TIFF 檔案導致 OutOfMemoryError：** 使用 `TiffOptions` 並將 `Compression` 設為 `LZW`，同時啟用串流 (`loadOptions.setBufferSize`) 以降低記憶體使用。  
- **意外的字元編碼：** XMP 需要 UTF‑8；請始終使用 `StandardCharsets.UTF_8` 傳遞字串，以避免資料亂碼。

## 常見問答

**Q：什麼是 XMP 中繼資料？**  
A：XMP 是一種基於 XML 的標準，用於直接在檔案內嵌入描述性資訊，從而在不同應用程式間提供一致的中繼資料。

**Q：為什麼 XMP 中繼資料很重要？**  
A：它讓您能為圖像標記作者、版權、關鍵字與自訂資料，提升搜尋能⼒與資產管理，且無需外部資料庫。

**Q：在圖像中嵌入 XMP 後，我可以編輯它嗎？**  
A：可以，Aspose.Imaging for Java 提供方法可修改既有的 XMP 封包並寫回檔案。

**Q：Aspose.Imaging for Java 是免費工具嗎？**  
A：提供免費試用供評估使用，但正式上線須購買授權。您可於 [Aspose.Imaging for Java 網站](https://purchase.aspose.com/buy) 探索授權方案。

**Q：我可以從哪裡取得 Aspose.Imaging for Java 的協助與支援？**  
A：請造訪 [Aspose.Imaging 論壇](https://forum.aspose.com/) 取得社群協助，或直接聯繫 Aspose 支援團隊（付費授權客戶專屬）。

## 結論

在本教學中，我們探討了如何使用 Aspose.Imaging for Java 這套領先的 **java image processing library** 來操作圖像中的 XMP 中繼資料。透過逐步指南，您可以輕鬆嵌入、更新與取得 XMP 資料，為數位資產賦予可搜尋、符合標準的中繼資訊。

---

**最後更新：** 2026-05-18  
**測試環境：** Aspose.Imaging for Java 24.12  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [精通 Java 圖像處理：使用 Aspose.Imaging 修改 EXIF 資料](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [Java 圖像處理與 Aspose.Imaging：載入、增強與儲存圖像](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [進階 Java 圖像處理與 Aspose.Imaging 函式庫](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)


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