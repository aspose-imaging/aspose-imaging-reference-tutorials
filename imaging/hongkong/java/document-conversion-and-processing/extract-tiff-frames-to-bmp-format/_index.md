---
date: 2026-05-03
description: 了解如何使用 Aspose.Imaging 在 Java 中將多頁 TIFF 轉換為 BMP 格式。請參考此一步一步的指南，高效地轉換 TIFF。
keywords:
- convert multi page tiff
- how to convert tiff
- Aspose.Imaging Java
- TIFF to BMP conversion
- image processing Java
linktitle: 提取 TIFF 影格為 BMP 格式
second_title: Aspose.Imaging Java Image Processing API
title: 使用 Aspose.Imaging for Java 將多頁 TIFF 轉換為 BMP
url: /zh-hant/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Imaging for Java 將多頁 TIFF 轉換為 BMP

如果您需要在 Java 環境中將 **轉換多頁 TIFF** 檔案轉換為單獨的 BMP 圖像，您來對地方了。在本教學中，我們將逐步說明如何提取每個 TIFF 幀並使用功能強大的 Aspose.Imaging for Java 函式庫將其保存為 BMP 檔案。完成後，您不僅能了解 *如何轉換 TIFF* 檔案，還能明白此方法為批量影像處理任務提供的可靠性。

## 快速答案
- **哪個函式庫最適合 TIFF 轉 BMP 轉換？** Aspose.Imaging for Java  
- **需要多少行程式碼？** 大約 30 行，分為五個邏輯步驟  
- **生產環境是否需要授權？** 是，需要商業授權（提供免費試用）  
- **能處理大型多頁 TIFF 嗎？** 能，API 能有效串流幀  
- **支援哪個 Java 版本？** Java 8 及以上  

## 什麼是「轉換多頁 TIFF」？
將多頁 TIFF 轉換為其他格式，指的是將單一 TIFF 容器內的每一頁（或幀）取出，並匯出為獨立的圖像檔案——此處為 BMP。此操作對於文件歸檔、醫學影像或任何需要光柵圖像進一步處理的工作流程都很有用。

## 為何使用 Aspose.Imaging for Java？
- **完整格式支援** – 支援 TIFF、BMP、JPEG、PNG 等多種格式。  
- **無外部相依性** – 純 Java，無需本機函式庫。  
- **高效能** – 串流存取幀可降低記憶體使用。  
- **豐富 API** – 提供對像素資料、色彩深度與中繼資料的細緻控制。  

## 前置條件

1. **Java 開發環境** – JDK 8 以上及您喜愛的 IDE。  
2. **Aspose.Imaging for Java** – 從官方網站下載最新 JAR **[here](https://releases.aspose.com/imaging/java/)**。  
3. **範例多頁 TIFF** – 將 TIFF 檔案（例如 `sample.tiff`）放置於程式可讀取的已知目錄中。  

## 匯入套件

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## 使用 Aspose.Imaging 將多頁 TIFF 轉換為 BMP 的方法

### 步驟 1：載入 TIFF 圖像並初始化幀計數器

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // Create an instance of int to keep track of frames in TiffImage
    int frameCounter = 0;
```

### 步驟 2：遍歷 TIFF 幀

```java
    // Iterate over the TiffFrames in TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

### 步驟 3：將 TiffFrame 的像素載入顏色陣列

```java
        // Load Pixels of TiffFrame into an array of Colors
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

### 步驟 4：建立 BMP 選項並設定每像素位元數

```java
        // Create an instance of bmpCreateOptions
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

### 步驟 5：儲存 BMP 圖像

```java
            // Set the Source of bmpCreateOptions as FileCreateSource by specifying the location where output will be saved
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // Create a new bmpImage
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // Save the bmpImage with pixels from TiffFrame
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## 常見陷阱與技巧

- **記憶體使用量：** 處理極大 TIFF 檔案時，建議如範例般一次處理單一幀，而非一次載入整張圖像至記憶體。  
- **檔案命名：** `String.format` 會為每個幀建立唯一檔名（`...out0.bmp`、`...out1.bmp` 等）。若需不同命名規則，請調整此模式。  
- **位元深度：** BMP 支援多種位元深度；24 位元（真彩色）適用於大多數情況。若需 8 位元灰階輸出，請修改 `setBitsPerPixel`。  

## 常見問答

### Q1：什麼是 Aspose.Imaging for Java？

A1：Aspose.Imaging for Java 是一個提供廣泛影像處理功能的 Java 函式庫，讓您能處理各種影像格式，並執行如轉換、編輯與操作等工作。

### Q2：我可以在 Aspose.Imaging for Java 中使用不同的影像格式嗎？

A2：是的，Aspose.Imaging for Java 支援多種影像格式，包括 TIFF、BMP、JPEG、PNG 等等，是影像相關任務的多功能工具。

### Q3：在哪裡可以找到 Aspose.Imaging for Java 的文件？

A3：您可在 **[here](https://reference.aspose.com/imaging/java/)** 找到 Aspose.Imaging for Java 的詳細文件。

### Q4：Aspose.Imaging for Java 有提供免費試用嗎？

A4：是的，您可在 **[here](https://releases.aspose.com/)** 取得 Aspose.Imaging for Java 的免費試用版。

### Q5：如何取得 Aspose.Imaging for Java 的支援？

A5：若有任何關於 Aspose.Imaging for Java 的問題、疑慮或需要支援，請前往支援論壇 **[here](https://forum.aspose.com/)**。

## 常見問題

**Q：我可以使用相同方法將多頁 TIFF 轉換為其他格式（例如 PNG）嗎？**  
A：當然可以。將 `BmpOptions` 替換為相應的選項類別（例如 `PngOptions`），並在 `FileCreateSource` 路徑中調整檔案副檔名。

**Q：Aspose.Imaging 能處理壓縮的 TIFF（LZW、CCITT）嗎？**  
A：可以，函式庫會在提取幀時自動解壓支援的 TIFF 壓縮方式。

**Q：轉換為 BMP 時能保留 EXIF 中繼資料嗎？**  
A：BMP 不支援 EXIF 中繼資料。若需保留中繼資料，請考慮轉換為支援的格式（如 PNG）或在轉換後手動複製中繼資料。

**Q：如何批次處理資料夾中的多個 TIFF 檔案？**  
A：將上述程式碼包在迴圈中，遍歷目錄中的 `File` 物件，為每個檔案更新 `dataDir` 及來源檔名。

**Q：商業部署需要什麼授權？**  
A：生產環境需要付費的 Aspose.Imaging for Java 授權。開發期間可使用臨時試用授權。

**最後更新：** 2026-05-03  
**測試環境：** Aspose.Imaging for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}