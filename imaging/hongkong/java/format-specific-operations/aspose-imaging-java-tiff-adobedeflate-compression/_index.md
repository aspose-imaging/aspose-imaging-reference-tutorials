---
date: '2026-08-27'
description: 了解在使用 Aspose.Imaging for Java 將圖像轉換為 TIFF 時，如何套用 deflate 壓縮，以確保高品質且高效的儲存。
keywords:
- how to apply deflate
- convert to tiff java
- convert png tiff java
- Aspose.Imaging Java TIFF conversion
- AdobeDeflate compression TIFF
lastmod: '2026-08-27'
og_description: 了解在使用 Aspose.Imaging for Java 將圖像轉換為 TIFF 時，如何套用 deflate 壓縮。一步一步的高品質圖像儲存指南。
og_image_alt: Guide showing Java code converting images to TIFF with AdobeDeflate
  compression using Aspose.Imaging
og_title: 如何在 Java 中對 TIFF 圖像套用 deflate 壓縮
schemas:
- author: Aspose
  dateModified: '2026-08-27'
  description: Learn how to apply deflate compression when converting images to TIFF
    using Aspose.Imaging for Java, ensuring high‑quality, efficient storage.
  headline: How to apply deflate compression to TIFF images in Java
  type: TechArticle
- description: Learn how to apply deflate compression when converting images to TIFF
    using Aspose.Imaging for Java, ensuring high‑quality, efficient storage.
  name: How to apply deflate compression to TIFF images in Java
  steps:
  - name: '**Archiving:** Preserve high‑resolution scans while keeping storage costs
      low.'
    text: '**Archiving:** Preserve high‑resolution scans while keeping storage costs
      low.'
  - name: '**Publishing:** Deliver print‑ready assets that meet industry‑standard
      TIFF specifications.'
    text: '**Publishing:** Deliver print‑ready assets that meet industry‑standard
      TIFF specifications.'
  - name: '**Medical imaging:** Transfer DICOM‑derived images without losing diagnostic
      detail.'
    text: '**Medical imaging:** Transfer DICOM‑derived images without losing diagnostic
      detail.'
  - name: '**Graphic design:** Store layered artwork in a single, lossless container
      for version control.'
    text: '**Graphic design:** Store layered artwork in a single, lossless container
      for version control.'
  type: HowTo
- questions:
  - answer: AdobeDeflate is a lossless TIFF compression algorithm that reduces file
      size by roughly 30‑50 % while keeping every pixel intact.
    question: What is AdobeDeflate compression?
  - answer: Yes—while the evaluation version works for testing, a purchased license
      unlocks full performance and removes evaluation watermarks.
    question: Do I need a license for production use?
  - answer: Absolutely. Aspose.Imaging supports PNG, JPEG, BMP, and many other raster
      formats as input for TIFF conversion.
    question: Can I convert PNG files to TIFF with this method?
  - answer: LZW typically yields similar size reductions but can be slower on very
      large images; AdobeDeflate often offers a better speed‑to‑size ratio.
    question: How does this compare to LZW compression?
  - answer: Aspose.Imaging for Java supports JDK 8 and higher; we recommend JDK 11
      or newer for optimal performance.
    question: What Java version is required?
  type: FAQPage
tags:
- image conversion
- Aspose.Imaging
- Java TIFF
- deflate compression
title: 如何在 Java 中對 TIFF 圖像套用 deflate 壓縮
url: /zh-hant/java/format-specific-operations/aspose-imaging-java-tiff-adobedeflate-compression/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 精通 Aspose.Imaging Java 圖像轉換：使用 AdobeDeflate 壓縮將圖像轉為 TIFF

在現代數位工作流程中，**如何套用 deflate** 壓縮在將圖像轉換為 TIFF 時是一項常見需求。無論您是要歸檔醫療掃描、準備列印就緒的圖形，或是透過網路傳送大量照片，TIFF 結合 AdobeDeflate 能以較小的容量提供無損品質。本教學將帶您完整了解從設定 Aspose.Imaging for Java、載入點陣圖、配置 TIFF 選項，到最終儲存壓縮檔案的全過程。

## 快速解答
- **第一步是什麼？** 透過 Maven、Gradle 或直接下載 JAR，將 Aspose.Imaging for Java 加入您的專案。  
- **AdobeDeflate 提供哪種壓縮？** 無損壓縮，通常可將 TIFF 大小減少 30‑50 % ，且不會失去畫質。  
- **需要授權嗎？** 需要，試用版可用於評估，但正式授權可解鎖完整效能。  
- **可以將 PNG 轉為 TIFF 嗎？** 當然可以——任何 Aspose.Imaging 支援的點陣圖格式皆可轉換。  
- **適用於大圖像嗎？** 是的；AdobeDeflate 能處理多百萬像素檔案，同時保持記憶體使用量適中。

## 什麼是「如何套用 deflate」？
*How to apply deflate* 指的是使用 AdobeDeflate 演算法壓縮 TIFF 圖像資料而不犧牲視覺品質的過程。此演算法內建於 Aspose.Imaging 的 `TiffOptions` 類別中。選擇此壓縮方式可保留每一個像素，同時達到約 30‑50 % 的檔案大小縮減，使產生的 TIFF 適用於存檔、列印與傳輸等情境。

## 為什麼在 TIFF 中使用 AdobeDeflate 壓縮？
Aspose.Imaging 支援 **50+ 輸入與輸出格式**，且可在不將整個文件載入記憶體的情況下處理 **多百頁的 TIFF 檔案**。AdobeDeflate 特別提供 **30‑50 % 的檔案大小縮減**，同時保留每一個像素，十分適合歸檔與列印流程。此外，此演算法具備快速的編碼與解碼速度，有助於在批次處理環境中維持高吞吐量。

## 前置條件

- **必備函式庫：** Aspose.Imaging for Java（最新版本）。  
- **開發環境：** IntelliJ IDEA、Eclipse，或任何支援 JDK 11 或更高版本的 Java IDE。  
- **基礎知識：** 熟悉 Java 檔案 I/O 與例外處理。

## 設定 Aspose.Imaging for Java

將函式庫加入您的建置設定。以下程式碼區塊僅為佔位符，請以官方網站提供的實際 Maven/Gradle 片段取代。

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

如果您偏好手動下載，請從 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 取得最新 JAR。

您可以從 [Aspose 的網站](https://releases.aspose.com/imaging/java/) 取得試用版或購買授權。正式授權可解鎖完整效能並移除評估水印。

### 如何在 Java 中對 TIFF 圖像套用 deflate 壓縮？

載入來源圖像、以 `CompressionType.AdobeDeflate` 設定 `TiffOptions`，然後儲存結果。此三步驟模式可在單一、記憶體有效率的流程中完成全部轉換。使用 try‑with‑resources 區塊可確保原生資源自動釋放，這在處理大型圖像或批次檔案時尤為重要。

`RasterImage` 類別是 Aspose.Imaging 的核心物件，代表記憶體中的任何點陣圖（PNG、JPEG、BMP 等）。載入後，您可以操作像素、變更解析度，或僅重新編碼圖像。

`TiffOptions` 類別定義 TIFF 檔寫入時的設定，如壓縮、解析度與色彩模式。設定 `Compression = CompressionType.AdobeDeflate` 即啟用 deflate 演算法。

`TiffFrame` 類別代表 TIFF 檔案中的單一頁面或圖層。呼叫 `save` 時，Aspose.Imaging 會使用您提供的選項寫入該框架。

### 將圖像載入為 RasterImage

```java
try (RasterImage image = (RasterImage) Image.load("YOUR_DOCUMENT_DIRECTORY/SampleTiff1.tiff")) {
    // Additional code will go here
}
```  
*說明：* `Image.load` 方法在 try‑with‑resources 區塊中將檔案讀入 `RasterImage` 實例，確保原生資源自動釋放。

### 設定 TIFF 選項

```java
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
options.setBitsPerSample(new int[] { 8, 8, 8 });
options.setPhotometric(TiffPhotometrics.Rgb);
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));
options.setResolutionUnit(TiffResolutionUnit.Inch);
options.setPlanarConfiguration(TiffPlanarConfig.Contiguous);
options.setCompression(TiffCompression.AdobeDeflate);
```  
*說明：* 透過設定 `TiffOptions`，您可指定 AdobeDeflate 壓縮、設定所需解析度（例如列印用的 300 DPI），以及選擇適當的色彩模式。

### 儲存轉換後的圖像

```java
try (TiffFrame tiffFrame = TiffFrame.fromRasterImage(image)) {
    TiffImage tiffImage = new TiffImage(tiffFrame);
    tiffImage.save("YOUR_OUTPUT_DIRECTORY/SavingRasterImage_out.tiff", options);
}
```  
*說明：* `TiffFrame` 包裝點陣資料，`save` 依先前定義的選項寫入最終的 TIFF 檔案。try‑with‑resources 模式確保檔案句柄正確關閉。

## 實務應用

將圖像轉為使用 AdobeDeflate 的 TIFF 在多個領域都相當有價值：

1. **歸檔：** 在保持高解析度掃描的同時降低儲存成本。  
2. **出版：** 提供符合業界標準 TIFF 規範的列印就緒資產。  
3. **醫學影像：** 傳輸 DICOM 衍生圖像而不失去診斷細節。  
4. **平面設計：** 將分層作品存於單一無損容器，便於版本控制。

## 效能考量

處理大量批次或高解析度檔案時，請遵循以下最佳實踐：

- **記憶體管理：** 圖像大於 10 MP 時，至少配置 **2 GB 堆積**。  
- **批次處理：** 使用迴圈一次處理單一檔案，避免同時載入多張圖像。  
- **最佳化壓縮：** AdobeDeflate 在速度與尺寸之間取得平衡——相較未壓縮的 TIFF，預期可減少 **30‑50 %**。

## 結論

現在您已了解 **如何套用 deflate** 壓縮，將圖像轉換為使用 Aspose.Imaging for Java 的 TIFF。此方法提供無損品質、縮小檔案大小，且在高需求工作流程中具備穩健效能。

**下一步**  

- 嘗試使用 LZW 或 CCITT Group 4 等其他壓縮方式，比較大小與速度。  
- 將轉換邏輯整合至 REST 服務，以實現即時圖像處理。

**行動呼籲：** 在您的下一個專案中實作此解決方案，親自體驗儲存空間的節省！

## 常見問題

**Q: 什麼是 AdobeDeflate 壓縮？**  
A: AdobeDeflate 是一種無損的 TIFF 壓縮演算法，能將檔案大小大約減少 30‑50 %，同時保留每一個像素。

**Q: 生產環境需要授權嗎？**  
A: 需要——雖然評估版可用於測試，但正式授權可解鎖完整效能並移除評估水印。

**Q: 可以使用此方法將 PNG 轉為 TIFF 嗎？**  
A: 當然可以。Aspose.Imaging 支援 PNG、JPEG、BMP 等多種點陣圖格式作為 TIFF 轉換的輸入。

**Q: 這與 LZW 壓縮相比如何？**  
A: LZW 通常可達到相似的尺寸縮減，但在處理極大圖像時速度較慢；AdobeDeflate 常提供更佳的速度‑尺寸比。

**Q: 需要哪個 Java 版本？**  
A: Aspose.Imaging for Java 支援 JDK 8 及以上版本；我們建議使用 JDK 11 或更新版本以獲得最佳效能。

## 資源

- [Documentation](https://reference.aspose.com/imaging/java/)
- [Download](https://releases.aspose.com/imaging/java/)
- [Purchase](https://purchase.aspose.com/buy)
- [Free trial](https://releases.aspose.com/imaging/java/)
- [Temporary license](https://purchase.aspose.com/temporary-license/)
- [Support forum](https://forum.aspose.com/c/imaging/14)

探索這些連結，以加深對 Aspose.Imaging for Java 的了解，並充分發揮其功能。

---

**最後更新：** 2026-08-27  
**測試環境：** Aspose.Imaging 24.11 for Java  
**作者：** Aspose

## 相關教學

- [Learn to Create Multi Page TIFF and Animated GIF Java – Aspose.Imaging Animation Tutorials](/imaging/java/animation-multi-frame-images/)
- [aspose imaging java – Convert TIFF to BMP Frames](/imaging/java/animation-multi-frame-images/extract-tiff-frames-to-bmp-aspose-imaging-java/)
- [How to Convert TIFF to GraphicsPath with Aspose.Imaging Java](/imaging/java/advanced-drawing-graphics/aspose-imaging-java-tiff-graphicspath-conversion/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}