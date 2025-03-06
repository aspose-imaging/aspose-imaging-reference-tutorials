---
title: 使用 Aspose.Imaging for Java 處理影像中的 XMP 數據
linktitle: 影像中的 XMP 資料處理
second_title: Aspose.Imaging Java 圖像處理 API
description: 了解如何使用 Aspose.Imaging for Java 處理影像中的 XMP 元資料。嵌入和檢索元資料以增強您的影像檔案。
weight: 16
url: /zh-hant/java/document-conversion-and-processing/xmp-data-handling-in-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Imaging for Java 處理影像中的 XMP 數據

Aspose.Imaging for Java 是一個多功能且功能強大的函式庫，用於處理各種格式的映像。本教學將引導您完成使用 Aspose.Imaging for Java 處理影像中的 XMP（可擴充元資料平台）資料的過程。 XMP 是一種將元資料嵌入圖像檔案的標準，可讓您儲存作者、描述等有價值的資訊。

## 先決條件

在開始之前，請確保您具備以下先決條件：

- 在您的電腦上設定 Java 開發環境。
-  Aspose.Imaging for Java 程式庫已安裝。您可以從[Aspose.Imaging for Java 網站](https://releases.aspose.com/imaging/java/).
- 對 Java 程式設計有基本的了解。

## 導入包

首先將必要的套件匯入到您的 Java 專案中。您可以在程式碼開頭新增以下導入語句：

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

## 第 1 步：指定圖像大小和 Tiff 選項

首先，定義儲存影像的目錄並建立一個矩形來指定影像的大小。在此範例中，我們使用帶有某些選項的 Tiff 影像。

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

## 第 3 步：建立 XMP 標頭和標尾

為您的 XMP 元資料建立 XMP-Header 和 XMP-Trailer 的實例。這些標頭和標尾有助於定義元資料結構。

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## 步驟 4：建立 XMP 元訊息

現在，建立 XMP 元的實例來設定不同的屬性。您可以新增作者和描述等資訊。

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## 第 5 步：建立 XMP 封包包裝器

建立包含 XMP 標頭、尾部和元資訊的 XmpPacketWrapper 實例。

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## 第 6 步：新增 Photoshop 包

要儲存 Photoshop 特定訊息，請建立 Photoshop 套件並設定其屬性，例如城市、國家和顏色模式。然後，將此套件新增至 XMP 元資料。

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## 步驟7：新增都柏林核心包

有關更多一般信息，例如作者、標題和其他值，請建立 DublinCore 套件並設定其屬性。也將此套件新增到 XMP 元資料中。

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## 步驟 8：更新映像中的 XMP 元數據

使用以下命令將 XMP 元資料更新到影像中`setXmpData`方法。

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## 第9步：儲存影像

現在，您可以將具有嵌入式 XMP 元資料的映像保存在磁碟或記憶體流中。

```java
    image.save(ms);
```

## 第 10 步：載入影像並檢索 XMP 元數據

若要從映像中檢索 XMP 元數據，請從記憶體流或磁碟載入映像並存取 XMP 資料。

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            //使用套件資料...
        }
    }
}
```

恭喜！您已經成功學習如何使用 Aspose.Imaging for Java 處理影像中的 XMP 資料。這允許您在圖像檔案中儲存和檢索有價值的元資料。

## 結論

在本教程中，我們探索如何使用 Aspose.Imaging for Java 處理圖像中的 XMP 元資料。透過遵循逐步指南，您可以輕鬆地在圖像檔案中嵌入和檢索元數據，從而增強其資訊和可用性。

## 常見問題解答

### Q1：什麼是 XMP 元資料？

A1：XMP（可擴充元資料平台）是將元資料嵌入到各種類型檔案（包括影像）中的標準。它允許您在文件本身中儲存作者、標題、描述等資訊。

### 問題 2：為什麼 XMP 元資料很重要？

A2：XMP 元資料對於組織和分類數位資產至關重要。它有助於歸屬所有權、描述內容以及向圖像等文件添加上下文，使它們更易於存取和有意義。

### 問題 3：將 XMP 元資料嵌入影像後可以編輯嗎？

A3：是的，您可以在將 XMP 元資料嵌入映像後進行編輯。 Aspose.Imaging for Java 提供了根據需要修改和更新元資料屬性的工具。

### Q4：Aspose.Imaging for Java 是免費工具嗎？

 A4：Aspose.Imaging for Java 提供免費試用版，但要獲得完整功能和擴充使用，需要付費授權。您可以探索[Aspose.Imaging for Java 網站](https://purchase.aspose.com/buy).

### Q5：我可以在哪裡獲得 Aspose.Imaging for Java 的幫助和支援？

 A5：如果您遇到任何問題或有與 Aspose.Imaging for Java 相關的疑問，您可以訪問[Aspose.Imaging 論壇](https://forum.aspose.com/)以獲得社區的支持和指導。



## 完整的原始碼
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
//透過定義矩形指定影像的大小
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
//建立全新影像僅用於範例目的
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	//建立 XMP-Header 的實例
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	//建立 Xmp-TrailerPi 的實例
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	//建立 XMP 元類別的實例來設定不同的屬性
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	//建立包含所有元資料的 XmpPacketWrapper 實例
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	//建立 Photoshop 套件的實例並設定 Photoshop 屬性
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	//將 Photoshop 套件加入 XMP 元資料中
	xmpData.addPackage(photoshopPackage);
	//建立 DublinCore 套件的實例並設定 dublinCore 屬性
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	//將 dublinCore 套件加入 XMP 元資料中
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	//將 XMP 元資料更新到影像中
	image.setXmpData(xmpData);
	//將影像保存在磁碟或記憶體流中
	image.save(ms);
	//從內存流或磁碟加載圖像以讀取/獲取元數據
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		//取得 XMP 元數據
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			//使用套件資料...
		}
	}
}
        
```
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
