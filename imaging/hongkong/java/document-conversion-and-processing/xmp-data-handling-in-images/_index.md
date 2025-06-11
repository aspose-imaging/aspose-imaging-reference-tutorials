---
"description": "學習如何使用 Aspose.Imaging for Java 處理影像中的 XMP 元資料。嵌入和檢索元資料以增強您的影像檔案。"
"linktitle": "影像中的 XMP 資料處理"
"second_title": "Aspose.Imaging Java映像處理API"
"title": "使用 Aspose.Imaging for Java 處理影像中的 XMP 數據"
"url": "/zh-hant/java/document-conversion-and-processing/xmp-data-handling-in-images/"
"weight": 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Imaging for Java 處理影像中的 XMP 數據

Aspose.Imaging for Java 是一個功能強大、功能多樣的函式庫，可用於處理各種格式的圖片。本教學將指導您使用 Aspose.Imaging for Java 處理圖像中的 XMP（可擴展元資料平台）資料。 XMP 是一種將元資料嵌入圖像檔案的標準，可讓您儲存作者、描述等有價值的資訊。

## 先決條件

在開始之前，請確保您已滿足以下先決條件：

- 您的電腦上設定的 Java 開發環境。
- 已安裝 Aspose.Imaging for Java 函式庫。您可以從 [Aspose.Imaging for Java網站](https://releases。aspose.com/imaging/java/).
- 對 Java 程式設計有基本的了解。

## 導入包

首先將必要的套件匯入到你的 Java 專案中。你可以在程式碼開頭加入以下 import 語句：

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

現在，讓我們將範例分解為逐步指南：

## 步驟 1：指定影像大小和 Tiff 選項

首先，定義圖片的儲存目錄，並建立一個矩形來指定圖片的大小。在本例中，我們使用特定選項的 Tiff 格式圖片。

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## 第 2 步：建立新映像

現在，使用指定的選項建立新映像。該影像將用於儲存 XMP 元資料。

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## 步驟 3：建立 XMP 標頭和標尾

為您的 XMP 元資料建立 XMP-Header 和 XMP-Trailer 實例。這些標頭和標尾有助於定義元資料結構。

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## 步驟4：建立XMP元訊息

現在，建立一個 XMP 元實例來設定不同的屬性。您可以新增作者和描述等資訊。

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## 步驟 5：建立 XMP 封包包裝器

建立包含 XMP 標頭、尾部和元資訊的 XmpPacketWrapper 實例。

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## 步驟6：新增Photoshop包

要儲存 Photoshop 的特定訊息，請建立一個 Photoshop 套件並設定其屬性，例如城市、國家和顏色模式。然後，將此套件新增至 XMP 元資料。

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## 步驟 7：新增都柏林核心包

如需取得更多常規資訊（例如作者、標題和其他值），請建立一個 DublinCore 套件並設定其屬性。將此套件也加入到 XMP 元資料中。

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## 步驟 8：更新影像中的 XMP 元數據

使用 `setXmpData` 方法。

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## 步驟9：儲存影像

現在您可以將嵌入 XMP 元資料的映像保存在磁碟或記憶體流中。

```java
    image.save(ms);
```

## 步驟 10：載入影像並檢索 XMP 元數據

若要從映像中檢索 XMP 元數據，請從記憶體流或磁碟載入映像並存取 XMP 資料。

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // 使用套件資料...
        }
    }
}
```

恭喜！您已成功學習如何使用 Aspose.Imaging for Java 處理圖像中的 XMP 資料。這允許您在圖像檔案中儲存和檢索有價值的元資料。

## 結論

在本教程中，我們探索如何使用 Aspose.Imaging for Java 處理圖像中的 XMP 元資料。按照逐步指南，您可以輕鬆地在圖像檔案中嵌入和檢索元數據，從而增強其資訊量和可用性。

## 常見問題解答

### Q1：什麼是XMP元資料？

A1：XMP（可擴充元資料平台）是將元資料嵌入各種類型檔案（包括影像）的標準。它允許您在文件本身中儲存作者、標題、描述等資訊。

### 問題 2：為什麼 XMP 元資料很重要？

A2：XMP 元資料對於組織和分類數位資產至關重要。它有助於歸屬所有權、描述內容以及為圖像等文件添加上下文，使其更易於存取且更有意義。

### 問題 3：將 XMP 元資料嵌入圖像後我可以編輯它嗎？

答3：是的，您可以在將 XMP 元資料嵌入影像後進行編輯。 Aspose.Imaging for Java 提供了根據需要修改和更新元資料屬性的工具。

### 問題4：Aspose.Imaging for Java 是免費工具嗎？

A4：Aspose.Imaging for Java 提供免費試用版，但如需完整功能和擴充使用，則需要付費授權。您可以在 [Aspose.Imaging for Java網站](https://purchase。aspose.com/buy).

### 問題5：在哪裡可以獲得 Aspose.Imaging for Java 的幫助和支援？

A5：如果您遇到任何問題或對 Aspose.Imaging for Java 有疑問，您可以訪問 [Aspose.Imaging 論壇](https://forum.aspose.com/) 尋求社區支持和指導。



## 完整的原始碼
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// 透過定義矩形來指定影像的大小
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// 建立全新影像僅用於範例目的
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// 建立 XMP-Header 實例
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// 建立 Xmp-TrailerPi 的實例
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// 建立 XMP 元類別的實例來設定不同的屬性
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// 建立包含所有元資料的 XmpPacketWrapper 實例
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// 建立 Photoshop 套件實例並設定 photoshop 屬性
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// 將 photoshop 套件加入到 XMP 元資料中
	xmpData.addPackage(photoshopPackage);
	// 建立 DublinCore 套件的實例並設定 dublinCore 屬性
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// 將 dublinCore 套件加入 XMP 元資料中
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// 將 XMP 元資料更新到影像中
	image.setXmpData(xmpData);
	// 將影像保存在磁碟或記憶體流中
	image.save(ms);
	// 從內存流或磁碟加載圖像以讀取/獲取元數據
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// 取得 XMP 元數據
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// 使用套件資料...
		}
	}
}
        
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}