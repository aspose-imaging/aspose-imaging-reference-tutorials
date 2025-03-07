---
title: 使用 Aspose.Imaging for Java 將 TIFF 轉換為 BMP
linktitle: 將 TIFF 幀提取為 BMP 格式
second_title: Aspose.Imaging Java 圖像處理 API
description: 了解如何使用 Aspose.Imaging for Java 在 Java 中將 TIFF 幀提取為 BMP 格式。請遵循我們的逐步指南。
weight: 13
url: /zh-hant/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Imaging for Java 將 TIFF 轉換為 BMP

如果您正在使用 Java 處理圖像文件，特別是 TIFF 圖像，並且需要從中提取幀並將其保存為 BMP 格式，Aspose.Imaging for Java 是實現此目的的強大且多功能的工具。在本逐步指南中，我們將引導您完成使用 Aspose.Imaging for Java 將 TIFF 訊框提取為 BMP 格式的過程。

## 先決條件

在我們開始之前，請確保您具備以下先決條件：

1. Java 開發環境：您的系統上應該設定有一個有效的 Java 開發環境。

2.  Aspose.Imaging for Java：確保您已安裝 Aspose.Imaging for Java 程式庫。您可以從網站下載[這裡](https://releases.aspose.com/imaging/java/).

3. 範例 TIFF 影像：擁有要從中擷取影格的範例 TIFF 影像檔案。確保此圖像在您的工作目錄中可用。

## 導入包

要開始該過程，您需要為 Java 應用程式匯入必要的套件：

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## 第 1 步：載入 TIFF 影像並初始化幀計數器

```java
//文檔目錄的路徑。
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    //建立 int 實例來追蹤 TiffImage 中的幀
    int frameCounter = 0;
```

## 第 2 步：迭代 TIFF 幀

```java
    //迭代 TiffImage 中的 TiffFrame
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

## 步驟 3：將 TiffFrame 的像素載入到顏色數組中

```java
        //將 TiffFrame 的像素載入到顏色數組中
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

## 步驟 4：建立 BMP 選項並設定每像素位數

```java
        //建立 bmpCreateOptions 的實例
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

## 步驟5：儲存BMP影像

```java
            //透過指定保存輸出的位置，將 bmpCreateOptions 的 Source 設定為 FileCreateSource
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            //建立一個新的bmp影像
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                //使用 TiffFrame 中的像素儲存 bmpImage
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## 結論

在本教程中，我們介紹如何使用 Aspose.Imaging for Java 提取 TIFF 幀並將其儲存為 BMP 影像。具備正確的先決條件並遵循逐步指南，您可以在 Java 應用程式中輕鬆執行此影像轉換任務。

## 常見問題解答

### Q1：什麼是 Aspose.Imaging for Java？

A1：Aspose.Imaging for Java 是一個 Java 函式庫，提供廣泛的影像處理功能，可讓您處理各種影像格式並執行轉換、編輯和操作等任務。

### Q2：我可以使用 Aspose.Imaging for Java 處理不同的圖片格式嗎？

A2：是的，Aspose.Imaging for Java 支援多種影像格式，包括 TIFF、BMP、JPEG、PNG 等，使其成為執行影像相關任務的多功能工具。

### Q3：在哪裡可以找到 Aspose.Imaging for Java 的文檔？

 A3：您可以找到Aspose.Imaging for Java的詳細文檔[這裡](https://reference.aspose.com/imaging/java/).

### Q4：Aspose.Imaging for Java 是否有免費試用版？

A4：是的，您可以透過免費試用版探索 Aspose.Imaging for Java[這裡](https://releases.aspose.com/).

### Q5：如何獲得 Aspose.Imaging for Java 的支援？

 A5：對於與 Aspose.Imaging for Java 相關的任何疑問、問題或支持，您可以訪問支持論壇[這裡](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
