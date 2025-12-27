---
date: '2025-12-27'
description: 學習如何使用 Aspose.Imaging Java 旋轉圖像，以及如何高效匯出 JPEG、PNG 和 TIFF。為影像處理 Java 開發人員提供的逐步指南。
keywords:
- Aspose.Imaging Java
- image processing Java
- exporting images Java
- rotate flip image Java
- Java image handling
title: 使用 Aspose.Imaging Java 旋轉圖像：載入、處理與匯出完整指南
url: /zh-hant/java/getting-started/aspose-imaging-java-image-processing-guide/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 精通 Aspose.Imaging Java：如何高效旋轉圖像與匯出

## 介紹

如果您需要在 Java 應用程式中 **how to rotate image** 且保持低記憶體使用量，您來對地方了。在本教學中，我們將示範如何使用自訂緩衝區載入圖像、旋轉與翻轉，然後將結果匯出為 JPEG、PNG 或 TIFF。完成後，您將了解 **image processing Java** 專案的最佳實踐，並能將這些技術整合到實際解決方案中。

**您將學習**
- **How to set buffer** 大小以獲得最佳載入效能。  
- **How to rotate image** 並套用翻轉變換。  
- **How to export JPEG**、**how to export PNG**，以及如何控制 **png bit depth**。  
- 這些技術發揮效益的實務情境。

讓我們先確認您已具備先決條件，然後深入程式碼。

### 先決條件

1. **Java Development Kit (JDK)** – 近期且相容的版本。  
2. **Maven or Gradle** – 用於相依性管理。  
3. **IDE** – IntelliJ IDEA、Eclipse 或任何支援 Java 的編輯器。  

### 設定 Aspose.Imaging for Java

使用以下任一程式碼片段將 Aspose.Imaging 加入您的專案。

**Maven**

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle**

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

您也可以從 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下載最新的 JAR。

> **專業提示：** 盡早註冊免費試用授權以避免評估水印。永久授權可透過 [purchase portal](https://purchase.aspose.com/buy) 取得。

## 快速解答
- **How to rotate image?** 使用 `RasterImage.rotate(angle)` 或 `rotateFlip(type)`。  
- **How to set buffer?** 設定 `LoadOptions.setBufferSizeHint(int)`。  
- **How to export JPEG?** 建立帶有灰階調色盤的 `JpegOptions`。  
- **How to export PNG?** 使用 `PngOptions` 並設定 `PngColorType.Grayscale`。  
- **What influences PNG file size?** **png bit depth** 設定（8 位元為常見）。

## 設定載入緩衝區大小

載入大型檔案可能會對記憶體造成壓力。Aspose.Imaging 允許您提示緩衝區大小，讓您更精細地控制資源消耗。

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.LoadOptions;
import com.aspose.imaging.RasterImage;

String sourceImagePath = "YOUR_DOCUMENT_DIRECTORY/Png/00020.png";
LoadOptions loadOptions = new LoadOptions();
loadOptions.setBufferSizeHint(450); // how to set buffer size (in KB)

try (RasterImage image = (RasterImage) Image.load(sourceImagePath, loadOptions)) {
    if (!image.isCached()) {
        image.cacheData(); // cache for faster subsequent operations
    }
}
```

**為何重要：** 適當的緩衝區可減少 GC 壓力，並加速後續的轉換。

## 旋轉圖像並套用翻轉

圖像已載入後，您可以變更其方向。

```java
import com.aspose.imaging.RasterImage;

float rotateAngle = 90; // how to rotate image: 90 degrees
Integer rotateFlipType = null; // set to a RotateFlipType enum if flipping is needed

try (RasterImage image = Image.load(sourceImagePath) as RasterImage) {
    if (!image.isCached()) {
        image.cacheData();
    }
    if (rotateAngle != 0) {
        image.rotate(rotateAngle); // rotate image
    }
    if (rotateFlipType != null) {
        image.rotateFlip(rotateFlipType); // optional flip
    }
}
```

**提示：** 當需要同時執行旋轉與翻轉時，使用 `rotateFlip` 只需一次呼叫，效率更高。

## 匯出 JPEG 並進行灰階最佳化

在保持檔案輕量的同時匯出 JPEG 常用於網路傳遞。

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.imaging.imageoptions.JpegOptions;
import com.aspose.imaging.sources.ColorPaletteHelper;

String outputJpegPath = "YOUR_OUTPUT_DIRECTORY/00020_jpeg.jpg";

try (RasterImage image = Image.load(sourceImagePath) as RasterImage) {
    if (!image.isCached()) {
        image.cacheData();
    }
    JpegOptions jpegOptions = new JpegOptions();
    int bitDepth = 8; // typical for JPEG
    if (bitDepth <= 8) {
        jpegOptions.setPalette(ColorPaletteHelper.create8BitGrayscale(true));
        jpegOptions.setColorType(JpegCompressionColorMode.Grayscale);
    }
    image.save(outputJpegPath, jpegOptions); // how to export jpeg
}
```

**結果：** 產生灰階 JPEG，檔案大小減少且視覺清晰度得以保留。

## 匯出 PNG 並設定灰階與位元深度

當必須保留無損品質時，PNG 是首選格式。控制 **png bit depth** 可在檔案大小與畫質之間取得平衡。

```java
import com.aspose.imaging.fileformats.png.PngColorType;
import com.aspose.imaging.imageoptions.PngOptions;

String outputPngPath = "YOUR_OUTPUT_DIRECTORY/00020_png.png";

try (RasterImage image = Image.load(sourceImagePath) as RasterImage) {
    if (!image.isCached()) {
        image.cacheData();
    }
    PngOptions pngOptions = new PngOptions();
    int bitDepth = 8; // how to export png with 8‑bit grayscale
    if (bitDepth <= 8) {
        pngOptions.setColorType(PngColorType.Grayscale);
        pngOptions.setBitDepth((byte) bitDepth); // png bit depth
    }
    image.save(outputPngPath, pngOptions); // how to export png
}
```

**注意：** 將位元深度降至 8 以下可進一步減小檔案大小，但需留意視覺品質。

## 匯出 TIFF 並自訂壓縮與光譜資訊

TIFF 適用於需要彈性的歸檔或印刷工作流程。

```java
import com.aspose.imaging.fileformats.tiff.enums.TiffCompressions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.imaging.imageoptions.TiffOptions;

String outputTiffPath = "YOUR_OUTPUT_DIRECTORY/00020_tiff.tiff";

try (RasterImage image = Image.load(sourceImagePath) as RasterImage) {
    if (!image.isCached()) {
        image.cacheData();
    }
    TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
    int bitDepth = 1; // example: 1‑bit monochrome
    switch (bitDepth) {
        case 1:
            tiffOptions.setPhotometric(TiffPhotometrics.MinIsWhite);
            tiffOptions.setPalette(ColorPaletteHelper.createMonochrome());
            tiffOptions.setCompression(TiffCompressions.CcittFax4);
            tiffOptions.setBitsPerSample(new int[]{1});
            break;
        case 8:
            tiffOptions.setPhotometric(TiffPhotometrics.MinIsWhite);
            tiffOptions.setPalette(ColorPaletteHelper.create8BitGrayscale(true));
            tiffOptions.setCompression(TiffCompressions.Deflate);
            tiffOptions.setBitsPerSample(new int[]{8});
            break;
        default:
            int bitsPerSample = bitDepth / 3;
            tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
            tiffOptions.setCompression(TiffCompressions.Jpeg);
            tiffOptions.setBitsPerSample(new int[]{bitsPerSample, bitsPerSample, bitsPerSample});
            break;
    }
    image.save(outputTiffPath, tiffOptions); // export TIFF with custom settings
}
```

**為何選擇 TIFF？** 它支援多種壓縮方式與光譜解釋，適合高品質的歸檔需求。

## 實務應用

- **Web platforms:** 透過旋轉與匯出為最佳化的 JPEG/PNG 來減少頁面載入時間。  
- **Digital archives:** 使用無損壓縮的 TIFF 保存原始檔案。  
- **CMS pipelines:** 自動化批次處理——旋轉、翻轉與匯出，一站式工作流程。  
- **Photo editing tools:** 為最終使用者提供快速的方向校正，無需外部編輯器。

## 效能考量

- **Cache wisely:** 當對同一圖像執行多項操作時，呼叫 `image.cacheData()`。  
- **Choose the right bit depth:** 8 位元灰階是大多數網頁圖像的最佳選擇；1 位元適用於黑白掃描。  
- **Monitor memory:** 大批次處理可透過 `LoadOptions` 設定適當的緩衝區大小以受益。

## 結論

我們已說明 **how to rotate image**、設定自訂緩衝區，以及以最佳設定匯出至 JPEG、PNG 與 TIFF。實作這些模式即可提升效能，並在任何基於 Java 的解決方案中提供高品質的視覺效果。

欲深入了解，請參考官方指南：[Aspose.Imaging documentation](https://docs.aspose.com/imaging/java/)。

## 常見問答

**Q: 如何安裝 Aspose.Imaging for Java？**  
A: 如前所示加入 Maven 或 Gradle 相依性，或從發行頁面下載 JAR。

**Q: 支援哪些圖像格式？**  
A: JPEG、PNG、TIFF、BMP、GIF 等等——完整列表請參閱產品文件。

**Q: 我可以在商業專案中使用此函式庫嗎？**  
A: 可以，只要透過 purchase portal 取得有效授權。

**Q: 處理非常大型圖像的最佳方法是什麼？**  
A: 使用 `LoadOptions.setBufferSizeHint` 以控制記憶體使用，並在多次操作前先快取圖像。

**Q: 如何進一步減小 PNG 檔案大小？**  
A: 當顏色忠實度不重要時，將 **png bit depth** 降至 4 位元或 2 位元，且盡可能使用灰階。

**最後更新：** 2025-12-27  
**測試環境：** Aspose.Imaging 25.5 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}