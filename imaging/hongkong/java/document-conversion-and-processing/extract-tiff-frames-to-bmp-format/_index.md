---
date: 2025-12-19
description: 學習如何在 Java 中使用 Aspose.Imaging 將 TIFF 轉換為 BMP。此一步一步的 Java 圖像處理教學展示了多頁
  TIFF 檔案的圖像轉換。
linktitle: Extract TIFF Frames to BMP Format
second_title: Aspose.Imaging Java Image Processing API
title: 如何使用 Aspose.Imaging for Java 將 tiff 轉換為 bmp
url: /zh-hant/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Imaging for Java 將 tiff 轉換為 bmp

如果您需要在 Java 應用程式中 **將 tiff 轉換為 bmp**，您來對地方了。無論您處理的是單頁 TIFF 還是多頁文件，Aspose.Imaging for Java 都能讓此過程簡單且可靠。在本教學中，我們將逐步說明如何從 TIFF 檔案中提取每一幀，並將其儲存為單獨的 BMP 圖像——非常適合影像轉換 java 場景。

## 快速答案
- **什麼程式庫負責轉換？** Aspose.Imaging for Java  
- **它能處理多頁 TIFF 嗎？** 是 – 每一幀都會儲存為單獨的 BMP  
- **我需要商業授權嗎？** 商業使用需要有效的 Aspose 授權  
- **支援哪個 Java 版本？** Java 8 或更高  
- **程式執行需要多久？** 標準尺寸圖像通常只需幾秒鐘  

## 前置條件

在開始之前，請確保您已具備以下前置條件：

1. **Java 開發環境** – 可運作的 JDK（8 或更新）以及您選擇的 IDE 或建置工具。  
2. **Aspose.Imaging for Java** – 從網站 [here](https://releases.aspose.com/imaging/java/) 下載最新的 JAR。  
3. **範例 TIFF 圖片** – 放置於專案工作目錄中的 TIFF 檔案（單頁或多頁）。  

## 匯入套件

要開始此流程，您需要為 Java 應用程式匯入必要的套件：

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## 逐步指南：將 tiff 轉換為 bmp

### 步驟 1：載入 TIFF 圖片並初始化幀計數器

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

### 步驟 5：儲存 BMP 圖片

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

## 為何使用 Aspose.Imaging for Java？

- **強大的多頁支援** – 無需額外程式碼即可處理任意數量的 TIFF 幀。  
- **純 Java 實作** – 無原生相依性，適合跨平台部署。  
- **高品質 BMP 輸出** – 您可以控制每像素位元數、壓縮與色彩深度。  
- **完整的影像轉換 java 工具組** – 支援 JPEG、PNG、GIF 及其他多種格式。  

## 常見問題與疑難排解

| 症狀 | 可能原因 | 解決方法 |
|---------|--------------|-----|
| `OutOfMemoryError` 在載入大型 TIFF 時發生 | 整張影像一次載入記憶體 | 如範例般逐幀處理，或增加 JVM 堆積大小 (`-Xmx`) |
| BMP 檔案損毀 | `BitsPerPixel` 值不正確 | 使用 24 或 32 以取得真彩色 BMP |
| 未產生輸出檔案 | 輸出目錄路徑錯誤 | 確認 `Your Document Directory` 指向已存在的資料夾 |

## 常見問答

### Q1：什麼是 Aspose.Imaging for Java？

A1: Aspose.Imaging for Java 是一個 Java 程式庫，提供廣泛的影像處理功能，讓您能夠處理各種影像格式並執行如轉換、編輯與操作等工作。

### Q2：我可以使用 Aspose.Imaging for Java 處理不同的影像格式嗎？

A2: 是的，Aspose.Imaging for Java 支援多種影像格式，包括 TIFF、BMP、JPEG、PNG 等，讓它成為影像相關工作的多功能工具。

### Q3：我可以在哪裡找到 Aspose.Imaging for Java 的文件？

A3: 您可以在此處找到 Aspose.Imaging for Java 的詳細文件 [here](https://reference.aspose.com/imaging/java/)。

### Q4：是否提供 Aspose.Imaging for Java 的免費試用？

A4: 是的，您可以在此處取得 Aspose.Imaging for Java 的免費試用版 [here](https://releases.aspose.com/)。

### Q5：如何取得 Aspose.Imaging for Java 的支援？

A5: 如有任何問題、疑慮或需要支援，您可以前往支援論壇 [here](https://forum.aspose.com/)。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-12-19  
**測試環境：** Aspose.Imaging for Java 24.12 (latest)  
**作者：** Aspose