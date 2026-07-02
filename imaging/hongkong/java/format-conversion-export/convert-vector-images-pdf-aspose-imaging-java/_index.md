---
date: '2026-05-29'
description: 了解如何使用 Aspose.Imaging for Java 從向量圖像建立多頁 PDF。將 CDR、SVG、EPS 轉換為 PDF，並可設定光柵化選項。
keywords:
- create multi page pdf
- convert vector to pdf
- export vector graphics pdf
- how to convert cdr pdf
- aspose imaging maven setup
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to create multi page PDF from vector images using Aspose.Imaging
    for Java. Convert CDR, SVG, EPS to PDF with rasterization options.
  headline: Create multi page PDF from vector images – Aspose.Imaging
  type: TechArticle
- description: Learn how to create multi page PDF from vector images using Aspose.Imaging
    for Java. Convert CDR, SVG, EPS to PDF with rasterization options.
  name: Create multi page PDF from vector images – Aspose.Imaging
  steps:
  - name: '**Free Trial** – Download a trial from [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).'
    text: '**Free Trial** – Download a trial from [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).'
  - name: '**Temporary License** – Obtain a short‑term key from [here](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Obtain a short‑term key from [here](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a full license at [Aspose''s official site](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a full license at [Aspose''s official site](https://purchase.aspose.com/buy).'
  - name: '**Archiving Design Assets** – Preserve original vector fidelity while storing
      in a universally viewable PDF.'
    text: '**Archiving Design Assets** – Preserve original vector fidelity while storing
      in a universally viewable PDF.'
  - name: '**Presentation Decks** – Convert multi‑page design files into PDF slides
      that render consistently across devices.'
    text: '**Presentation Decks** – Convert multi‑page design files into PDF slides
      that render consistently across devices.'
  - name: '**Document Management Systems** – Automate conversion pipelines to ingest
      vector graphics into ECM platforms.'
    text: '**Document Management Systems** – Automate conversion pipelines to ingest
      vector graphics into ECM platforms.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java is a comprehensive library that enables developers
      to create, edit, convert, and render raster and vector images without relying
      on native OS components.
    question: What is Aspose.Imaging for Java?
  - answer: Yes, the library also supports SVG, EPS, WMF, EMF, and many others—covering
      over 50 vector and raster formats.
    question: Can I convert other vector formats besides CDR?
  - answer: Use `PdfOptions.setEncryptionOptions()` to set a user password and permissions
      before calling `save`.
    question: How do I handle password‑protected PDFs when exporting?
  - answer: Absolutely. It is thread‑safe, can process multi‑hundred‑page documents,
      and offers streaming APIs to minimise memory footprint.
    question: Is the library suitable for high‑throughput server environments?
  - answer: Process pages individually, dispose of `Image` objects promptly, and consider
      increasing the JVM heap only when necessary.
    question: What are the best practices for memory management?
  type: FAQPage
title: 從向量圖像建立多頁 PDF – Aspose.Imaging
url: /zh-hant/java/format-conversion-export/convert-vector-images-pdf-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 如何使用 Aspose.Imaging for Java 將向量圖像轉換為 PDF

## 簡介

從向量圖形建立 **多頁 PDF** 是在需要高解析度、可搜尋的文件以供簡報、存檔或自動化工作流程時的常見需求。在本指南中，您將學習如何 **將向量轉換為 PDF**——包括 CDR、SVG 和 EPS 檔案——透過 Aspose.Imaging for Java。 我們將逐步說明載入向量檔案、對每頁進行光柵化、設定 PDF 匯出選項，最後儲存保留所有細節的多頁 PDF。

## 快速解答
- **什麼函式庫負責向量轉 PDF 轉換？** Aspose.Imaging for Java。  
- **我可以將 CDR 檔案轉換為 PDF 嗎？** 可以，CDR 與 SVG、EPS 以及其他向量格式皆受支援。  
- **生產環境需要授權嗎？** 需要商業授權；可使用免費試用版進行評估。  
- **建議使用哪種建置工具？** Maven（請參閱「aspose imaging maven setup」章節）。  
- **PDF 會自動成為多頁嗎？** 會，當來源向量圖像包含多個頁面時。

## 前置條件

在開始之前，請確保您已具備以下條件：

- **Java Development Kit (JDK) 8+** 已安裝。  
- **Maven** 或 **Gradle** 用於相依性管理（以下示範 Maven 設定）。  
- **有效的 Aspose.Imaging 授權** 用於生產環境（開發可使用試用版）。

### 必需的函式庫與相依性

使用以下任一方式將 Aspose.Imaging 加入您的專案：

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

您也可以直接從 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下載最新的 JAR。欲了解更多細節，請參閱 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 頁面。

### 環境設定

您的 IDE（IntelliJ IDEA、Eclipse 或 VS Code）必須設定為能解析 Maven/Gradle 相依性。請確保 `JAVA_HOME` 環境變數指向您的 JDK 安裝目錄。

### 知識前提

具備基本的 Java 語法與檔案 I/O 知識即可跟隨本教學。無需事先了解 Aspose.Imaging。

## 設定 Aspose.Imaging for Java

### 安裝資訊

將上述 Maven 或 Gradle 片段加入您的 `pom.xml` 或 `build.gradle` 檔案，然後執行相應的建置指令以下載函式庫。

### 取得授權步驟

1. **免費試用** – 從 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下載試用版。  
2. **臨時授權** – 從 [here](https://purchase.aspose.com/temporary-license/) 取得短期金鑰。  
3. **購買** – 前往 [Aspose's official site](https://purchase.aspose.com/buy) 購買完整授權。

### 基本初始化

將函式庫加入 classpath 後，在 Java 程式碼中初始化它：

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

Aspose.Imaging 準備就緒，讓我們開始轉換。

## 如何從向量圖像建立多頁 PDF？

首先使用 `Image.load()` 載入來源向量檔案，接著為每頁設定光柵化選項，指定 PDF 匯出參數，最後呼叫 `save` 方法輸出多頁 PDF。此簡潔工作流程確保高品質輸出，同時保持程式碼簡單且易於維護。

### 功能 1：載入 VectorMultipageImage

**定義：** `VectorMultipageImage` 代表 Aspose.Imaging 中的多頁向量文件（例如 CDR 或多頁 EPS）。

**逐步實作**

```java
// Import necessary classes from Aspose.Imaging package
import com.aspose.imaging.Image;
import com.aspose.imaging.VectorMultipageImage;

public class VectorToPDF {
    public static void main(String[] args) {
        // Load a VectorMultipageImage from the specified input file path.
        try (VectorMultipageImage image = (VectorMultipageImage) Image.load("YOUR_DOCUMENT_DIRECTORY/CDR/MultiPage2.cdr")) {
            // Image is now loaded and can be manipulated
            System.out.println("Image Loaded Successfully!");
            
            VectorRasterizationOptions[] pageOptions = createPageOptions(image);
            PdfOptions pdfOptions = configurePdfOptions(pageOptions);
            exportToPdf(image, pdfOptions, "output_directory/output.pdf");
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```  

**說明**

- `Image.load()` 從磁碟讀取向量檔案。  
- `try‑with‑resources` 區塊確保影像自動釋放，避免記憶體洩漏。  
- `VectorMultipageImage` 讓您存取每個單獨頁面以進行後續處理。

### 功能 2：建立頁面光柵化選項

**定義：** `PageOptionsBuilder` 用於建立 `RasterizationOptions`，控制每個向量頁面在 PDF 轉換前如何渲染為光柵圖像。

**逐步實作**

```java
import com.aspose.imaging.VectorRasterizationOptions;
import com.aspose.imaging.imageoptions.CdrRasterizationOptions;
import com.aspose.imaging.examples.ModifyingImages.PageOptionsBuilder;

public static VectorRasterizationOptions[] createPageOptions(VectorMultipageImage image) {
    // Generates rasterization options for each page based on CdrRasterizationOptions class
    return PageOptionsBuilder.createPageOptions(CdrRasterizationOptions.class, image);
}
```  

**說明**

- 您可以設定 DPI、背景色與抗鋸齒，以符合品質需求。  
- 適當的光柵化可確保文字、曲線與漸層在最終 PDF 中保持清晰。

### 功能 3：建立 PDF 匯出選項

**定義：** `PdfOptions` 包含產生 PDF 所需的所有設定，而 `MultiPageOptions` 告訴 Aspose.Imaging 如何處理每個已渲染的頁面。

**逐步實作**

```java
import com.aspose.imaging.imageoptions.MultiPageOptions;
import com.aspose.imaging.imageoptions.PdfOptions;

public static PdfOptions configurePdfOptions(VectorRasterizationOptions[] pageOptions) {
    // Initializes a new instance of PdfOptions
    PdfOptions options = new PdfOptions();
    MultiPageOptions multiPageOptions = new MultiPageOptions();

    // Sets the page rasterization options for each page
    multiPageOptions.setPageRasterizationOptions(pageOptions);

    // Assigns multi-page options to PDF options
    options.setMultiPageOptions(multiPageOptions);
    
    return options;
}
```  

**說明**

- `PdfOptions` 允許您嵌入中繼資料、設定壓縮方式，並控制 PDF 版本。  
- `MultiPageOptions` 確保每個光柵化頁面都成為獨立的 PDF 頁面，從而產生真正的多頁文件。

### 功能 4：將影像匯出為 PDF 格式

**定義：** `Image` 物件的 `save` 方法將處理後的內容寫入指定的輸出格式——本例為 PDF。

**逐步實作**

```java
import com.aspose.imaging.VectorMultipageImage;
import com.aspose.imaging.imageoptions.PdfOptions;

public static void exportToPdf(VectorMultipageImage image, PdfOptions options, String outFile) {
    // Saves the image using the configured PDF options
    image.save(outFile, options);
}
```  

**說明**

- `image.save(outFile, pdfOptions)` 完成轉換。  
- `outFile` 路徑決定 PDF 在磁碟上的儲存位置。

## 為何使用 Aspose.Imaging 進行此轉換？

Aspose.Imaging 支援 **50 多種輸入與輸出格式**——包括 CDR、SVG、EPS、PDF、PNG、JPEG 與 TIFF，且能在不將整個檔案載入記憶體的情況下處理 **最多 500 頁** 的文件。此量化的能力使其成為企業環境中大規模批次轉換的理想選擇。

## 常見使用情境

1. **存檔設計資產** – 在以通用可檢視的 PDF 儲存時，保留原始向量的完整度。  
2. **簡報投影片** – 將多頁設計檔案轉換為 PDF 投影片，確保在各裝置上呈現一致。  
3. **文件管理系統** – 自動化轉換流程，將向量圖形匯入 ECM 平台。

## 效能建議

- **分段處理：** 對於非常大的檔案，逐頁載入與光柵化，以降低記憶體使用量。  
- **調整 DPI：** 較高的 DPI 可產生更銳利的輸出，但會佔用更多記憶體；300 dpi 為大多數列印就緒 PDF 的良好平衡。  
- **平行執行：** 轉換大量檔案時，可在平行執行緒中執行，但需監控 JVM 堆積以避免 OOM 錯誤。

## 疑難排解建議

- 確認檔案路徑正確且應用程式具備讀寫權限。  
- 若遇到 `UnsupportedFormatException`，請確認來源格式列於支援的向量類型中。  
- 意外的視覺異常通常源於 DPI 不足；請在 `PageOptionsBuilder` 中提升光柵化 DPI。

## 常見問答

**Q: Aspose.Imaging for Java 是什麼？**  
A: Aspose.Imaging for Java 是一套完整的函式庫，讓開發人員能在不依賴原生作業系統元件的情況下，建立、編輯、轉換與呈現點陣與向量圖像。

**Q: 除了 CDR，還能轉換其他向量格式嗎？**  
A: 可以，函式庫亦支援 SVG、EPS、WMF、EMF 等多種格式，涵蓋超過 50 種向量與點陣格式。

**Q: 匯出時如何處理受密碼保護的 PDF？**  
A: 在呼叫 `save` 前，使用 `PdfOptions.setEncryptionOptions()` 設定使用者密碼與權限。

**Q: 此函式庫適合高吞吐量的伺服器環境嗎？**  
A: 完全適合。它具備執行緒安全性，可處理數百頁文件，且提供串流 API 以減少記憶體占用。

**Q: 記憶體管理的最佳實踐是什麼？**  
A: 請逐頁處理，及時釋放 `Image` 物件，僅在必要時才增大 JVM 堆積。

## 資源

- [文件說明文件](https://reference.aspose.com/imaging/java/)  
- [下載](https://releases.aspose.com/imaging/java/)  
- [購買](https://purchase.aspose.com/buy)  
- [免費試用](https://releases.aspose.com/imaging/java/)  
- [臨時授權](https://purchase.aspose.com/temporary-license/)  
- [支援](https://forum.aspose.com/c/imaging/14)

---

**最後更新：** 2026-05-29  
**測試環境：** Aspose.Imaging 24.12 for Java  
**作者：** Aspose

## 相關教學

- [使用 Aspose.Imaging for Java 將向量圖像轉換為 PDF&#58; 完整指南](/imaging/java/format-conversion-export/convert-vector-images-pdf-aspose-imaging-java/)
- [使用 Aspose.Imaging 在 Java 中掌握頁面光柵化&#58; 向量圖形指南](/imaging/java/vector-graphics-svg/mastering-page-rasterization-aspose-imaging-java-guide/)
- [使用 Aspose.Imaging for Java 將點陣圖像轉換為 PDF](/imaging/java/document-conversion-and-processing/convert-raster-images-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}