---
date: '2026-09-13'
description: 了解如何在 Java 中使用 Aspose.Imaging 建立 TIFF 圖片，涵蓋壓縮、解析度與顏色設定，以產生高品質的 TIFF 檔案。
keywords:
- create tiff java
- maven aspose imaging dependency
- tiff options java
- aspose imaging tiff
- java image processing
lastmod: '2026-09-13'
og_description: 在 Java 中使用 Aspose.Imaging 建立 TIFF 圖片。了解如何使用 Maven Aspose Imaging 相依套件設定壓縮、解析度與顏色選項。
og_image_alt: Tutorial guide showing Java code to create and configure TIFF images
  with Aspose.Imaging
og_title: 如何在 Java 中使用 Aspose.Imaging 函式庫建立 TIFF 圖片
schemas:
- author: Aspose
  dateModified: '2026-09-13'
  description: Learn how to create TIFF images in Java with Aspose.Imaging, covering
    compression, resolution, and color settings to produce high‑quality TIFF files.
  headline: How to create TIFF in Java using Aspose.Imaging library
  type: TechArticle
- description: Learn how to create TIFF images in Java with Aspose.Imaging, covering
    compression, resolution, and color settings to produce high‑quality TIFF files.
  name: How to create TIFF in Java using Aspose.Imaging library
  steps:
  - name: '**Free trial** – download and evaluate without restrictions. See the **[Free
      Trial](https://releases.aspose.com/imaging/java/)** page.'
    text: '**Free trial** – download and evaluate without restrictions. See the **[Free
      Trial](https://releases.aspose.com/imaging/java/)** page.'
  - name: '**Temporary license** – request from Aspose for extended evaluation via
      the **[Temporary License Request](https://purchase.aspose.com/temporary-license/)**.'
    text: '**Temporary license** – request from Aspose for extended evaluation via
      the **[Temporary License Request](https://purchase.aspose.com/temporary-license/)**.'
  - name: '**Purchase license** – obtain a permanent license via the **[Purchase License](https://purchase.aspose.com/buy)**
      or the **[purchase page](https://purchase.aspose.com/buy)**.'
    text: '**Purchase license** – obtain a permanent license via the **[Purchase License](https://purchase.aspose.com/buy)**
      or the **[purchase page](https://purchase.aspose.com/buy)**.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Imaging supports over 150 formats, including PNG, JPEG, BMP,
      and GIF. See the **[Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)**
      for details.
    question: Can I use this code with other image formats?
  - answer: No, Gradle users can add the same coordinates in their `build.gradle`
      file; the underlying library is identical.
    question: Do I need the Maven Aspose Imaging dependency for Gradle projects?
  - answer: The library can stream TIFF files up to several gigabytes, limited only
      by available disk space, because it never loads the whole image into RAM.
    question: How large a TIFF can Aspose.Imaging process?
  - answer: Enable `LoadOptions` with `useMemoryCache = true` or process the image
      in tiles to keep memory usage low.
    question: What if I encounter an `OutOfMemoryError`?
  - answer: A free trial works for development, but a licensed version removes evaluation
      watermarks and unlocks full performance optimisations.
    question: Is a license required for development builds?
  type: FAQPage
tags:
- create tiff
- Aspose.Imaging
- Java image processing
title: 如何在 Java 中使用 Aspose.Imaging 函式庫建立 TIFF 圖片
url: /zh-hant/java/format-specific-operations/create-tiff-images-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中使用 Aspose.Imaging 建立 TIFF

## 介紹

以程式方式建立 TIFF 檔案可能相當具挑戰性，尤其當您需要對壓縮、解析度與色彩詮釋進行細緻控制時。在本教學中，您將學習如何使用 Aspose.Imaging **create TIFF in Java**，設定最常見的 TIFF 選項，並操作像素資料。無論您是構建數位保存系統、列印流程，或醫學影像應用程式，下列步驟皆提供可直接投入生產的做法。

**您將學到**

- 如何設定 TIFF 選項，例如壓縮、解析度與色彩詮釋。  
- 在 Java 中建立新 TIFF 影像並操作其像素的流程。  
- Aspose.Imaging 處理 TIFF 檔案的實務應用。

## 快速答案
- **哪個函式庫支援在 Java 中建立 TIFF？** Aspose.Imaging for Java。  
- **我需要授權才能投入生產嗎？** 是，購買的授權會移除評估限制。  
- **我可以使用哪種建置工具？** 透過 Maven Aspose Imaging 相依性使用 Maven 或 Gradle。  
- **我可以設定壓縮與解析度嗎？** 當然可以——使用 `TiffOptions` 屬性。  
- **此程式碼相容於 JDK 8 以上嗎？** 是，支援 JDK 8 及更新版本。

## 前置條件

- 已安裝 **Java Development Kit (JDK)** 8 或以上。  
- 用於相依性管理的 **Maven** 或 **Gradle**。  
- 具備 Java 及影像處理概念的基本熟悉度。

## 設定 Aspose.Imaging for Java

在開始編寫程式碼之前，請將 Aspose.Imaging 函式庫加入您的專案。

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
implementation(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

如果您偏好手動下載，可從 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 取得最新發行版。您也可以使用通用連結 **[Download Latest Version](https://releases.aspose.com/imaging/java/)**。

### 取得授權

免費試用版可用於開發，但生產環境部署需使用授權版本。

1. **Free trial** – 下載並無限制地評估。請參閱 **[Free Trial](https://releases.aspose.com/imaging/java/)** 頁面。  
2. **Temporary license** – 向 Aspose 申請延長評估，透過 **[Temporary License Request](https://purchase.aspose.com/temporary-license/)**。  
3. **Purchase license** – 透過 **[Purchase License](https://purchase.aspose.com/buy)** 或 **[purchase page](https://purchase.aspose.com/buy)** 取得永久授權。

### 初始化

匯入所需類別並初始化函式庫：

```java
import com.aspose.imaging.imageoptions.TiffOptions;
```

## TiffOptions 是什麼？

`TiffOptions` 是 Aspose.Imaging 中的類別，用於定義 TIFF 檔案的編碼方式，包含壓縮、解析度與色彩設定。它允許您在儲存之前指定輸出檔案的精確特性。

您在儲存影像之前會先配置 `TiffOptions` 實例；這確保產生的檔案符合您對品質與相容性的精確要求。透過調整其屬性，您可以將 TIFF 量身打造，以符合保存、列印或醫學影像的標準。

## 如何在 Java 中設定 TIFF 選項？

要設定 TIFF 選項，您需要建立一個 `TiffOptions` 物件，並為其屬性（如 `bitsPerSample`、`photometric`、`resolutionUnit`、`xResolution`、`yResolution`、`compression`）指派值。此配置會在影像寫入磁碟時套用，確保檔案符合所需規格。

### 設定 TiffOptions 屬性

此功能示範如何配置各種屬性，以建立符合規格的 TIFF 檔案。

#### 概述

配置 `TiffOptions` 讓您可依照保存、列印或醫學影像的行業標準，客製化 TIFF 輸出。

##### 設定每樣本位元數

```java
// Create an instance of TiffOptions
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);

// Set bits per sample for RGB configuration
options.setBitsPerSample(new int[] { 8, 8, 8 });
```

此程式碼將色彩深度設定為 24 位元 RGB，為高品質影像的標準。

##### 設定 photometric 詮釋

```java
// Use RGB photometric interpretation
options.setPhotometric(TiffPhotometrics.Rgb);
```

`setPhotometric` 方法指定影像使用 RGB 調色盤。

##### 定義解析度與單位

```java
// Set resolution to 72 DPI for both X and Y axes
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));

// Specify resolution unit as inches
options.setResolutionUnit(TiffResolutionUnits.Inch);
```

這些設定確保影像在不同裝置上具有一致的顯示尺寸。

##### 壓縮設定

```java
// Set compression to AdobeDeflate for efficient storage
options.setCompression(TiffCompressions.AdobeDeflate);
```

使用 `AdobeDeflate` 可在不失真的情況下降低檔案大小，適合保存用途。

## TiffImage 是什麼？

`TiffImage` 是 Aspose.Imaging 的類別，代表記憶體中的 TIFF 文件，允許在儲存前進行像素層級的操作。它提供存取與修改單一像素、圖層與中繼資料的方法。

使用已配置的 `TiffOptions` 建立 `TiffImage`，即可完整掌控影像內容與中繼資料，從而以程式方式產生自訂的 TIFF 檔案。

## 如何建立與操作 TIFF 影像？

要建立與操作 TIFF 影像，您需要實例化 `TiffImage`、將像素緩衝區填入所需資料，然後使用先前定義的 `TiffOptions` 進行儲存。此工作流程確保影像完全依照選項規範建構。

### 建立與操作 TiffImage

現在選項已設定，讓我們使用這些配置建立影像。

#### 概述

建立 TIFF 影像的過程包括初始化 `TiffImage`、設定像素，最後儲存結果。使用 Aspose.Imaging，此流程相當簡單。

##### 初始化新的 TiffImage

```java
try (TiffImage tiffImage = new TiffImage(new TiffFrame(options, 100, 100))) {
    // Loop over each pixel to set it to red color
    for (int i = 0; i < 100; i++) {
        tiffImage.getActiveFrame().setPixel(i, i, Color.getRed());
    }
    
    // Save the image to your desired output directory
    tiffImage.save("YOUR_OUTPUT_DIRECTORY" + "/CreatingTIFFImageWithCompression.tiff");
}
```

在此程式碼片段中，我們建立一個 100 × 100 像素的 TIFF 影像，並使用預先定義的設定將其填滿紅色像素。

## 實務應用

了解如何設定 TIFF 選項與程式化建立影像，在以下情境中相當寶貴：

- **Digital archiving** – 以高品質格式保存文件或藝術品。  
- **Professional printing** – 確保列印品符合業界色彩準確度標準。  
- **Medical imaging** – 處理需要特定設定的詳細影像資料。

## 效能考量

在影像處理工作中，效能是關鍵。Aspose.Imaging 能處理 **150+ 影像格式**，且可在不將整個檔案載入記憶體的情況下處理 **多百頁 TIFF**，降低 OutOfMemory 錯誤的風險。

- **Optimize memory usage** – 利用 Aspose.Imaging 的串流 API 處理大型檔案。  
- **Batch processing** – 在一次執行中處理多張影像，以減少開銷。  
- **Efficient compression** – 選擇 `AdobeDeflate` 以取得良好的品質與檔案大小平衡。

## 常見問題

**Q: 我可以將此程式碼用於其他影像格式嗎？**  
A: 是的，Aspose.Imaging 支援超過 150 種格式，包括 PNG、JPEG、BMP 與 GIF。詳情請參閱 **[Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)**。

**Q: 我需要 Maven Aspose Imaging 相依性才能在 Gradle 專案中使用嗎？**  
A: 不需要，Gradle 使用者可在 `build.gradle` 檔案中加入相同的座標；底層函式庫相同。

**Q: Aspose.Imaging 能處理多大的 TIFF？**  
A: 此函式庫可串流處理高達數 GB 的 TIFF 檔案，唯一受限於可用磁碟空間，因為它從不將整張影像載入 RAM。

**Q: 若遇到 `OutOfMemoryError` 該怎麼辦？**  
A: 啟用 `LoadOptions` 並將 `useMemoryCache = true`，或以瓦片方式處理影像，以降低記憶體使用量。

**Q: 開發版是否需要授權？**  
A: 免費試用版可用於開發，但授權版會移除評估水印並解鎖完整效能最佳化。

**Q: 若遇到問題該向何處尋求協助？**  
A: 可前往 **[Aspose Support Forum](https://forum.aspose.com/c/imaging/14)** 取得社群協助與官方支援。

## 結論

您現在已掌握使用 Aspose.Imaging **create TIFF in Java** 的完整生產就緒指南。透過配置 `TiffOptions` 並使用 `TiffImage`，即可產生符合嚴格保存、列印或醫學影像標準的高品質 TIFF 檔案。

**接下來的步驟**

- 探索其他 `TiffOptions`（如 `extraSamples`、`predictor`）以因應特殊使用情境。  
- 嘗試 Aspose.Imaging API，進行格式轉換、加入浮水印或擷取中繼資料。

---

**Last Updated:** 2026-09-13  
**Tested With:** Aspose.Imaging 24.12 for Java  
**Author:** Aspose

## 相關教學

- [掌握 Java 中的 TIFF 影像處理與 Aspose.Imaging](/imaging/java/image-loading-saving/load-save-tiff-images-aspose-imaging-java/)
- [進階 Java TIFF 影像處理與 Aspose.Imaging](/imaging/java/format-specific-operations/mastering-tiff-image-processing-java-aspose-imaging/)
- [Java 影像處理與 Aspose.Imaging：載入、增強與儲存影像](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}