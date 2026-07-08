---
date: '2026-07-08'
description: 了解如何使用 Aspose.Imaging for Java 從 DjVu 匯出 TIFF。逐步指南涵蓋載入、頁面選取與匯出選項。
keywords:
- how to export tiff
- java image processing
- maven aspose imaging
- how to load djvu
lastmod: '2026-07-08'
og_description: 探索如何在 Java 中使用 Aspose.Imaging 從 DjVu 匯出 TIFF。遵循我們的逐步教學，快速且可靠地進行影像轉換。
og_image_alt: Guide showing Java code to convert DjVu pages to TIFF with Aspose.Imaging
og_title: 如何匯出 TIFF – Aspose.Imaging Java 指南
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: Learn how to export TIFF from DjVu using Aspose.Imaging for Java. Step-by-step
    guide covering loading, page selection, and export options.
  headline: How to Export TIFF – Load and Export DjVu Pages in Java with Aspose.Imaging
  type: TechArticle
- description: Learn how to export TIFF from DjVu using Aspose.Imaging for Java. Step-by-step
    guide covering loading, page selection, and export options.
  name: How to Export TIFF – Load and Export DjVu Pages in Java with Aspose.Imaging
  steps:
  - name: '**Archival Systems** – Preserve scanned documents in a universally accepted
      format.'
    text: '**Archival Systems** – Preserve scanned documents in a universally accepted
      format.'
  - name: '**Document Review Workflows** – Pull out only the pages that need annotation.'
    text: '**Document Review Workflows** – Pull out only the pages that need annotation.'
  - name: '**Integration with DMS** – Feed TIFF images into existing document‑management
      pipelines that do not understand DjVu.'
    text: '**Integration with DMS** – Feed TIFF images into existing document‑management
      pipelines that do not understand DjVu.'
  type: HowTo
- questions:
  - answer: '`DjvuImage` represents a DjVu document in memory.'
    question: What is the main class for DjVu handling?
  - answer: Just two lines after loading the image.
    question: How many lines of code are needed to export a page to TIFF?
  - answer: '`com.aspose:aspose-imaging` (version 25.5+).'
    question: Which Maven artifact provides DjVu support?
  - answer: Yes, use `IntRange` to specify a range.
    question: Can I export multiple pages at once?
  - answer: A full license is required; a temporary trial is available.
    question: Do I need a license for production?
  type: FAQPage
tags:
- convert DjVu
- Aspose.Imaging
- Java image conversion
title: 如何匯出 TIFF – 在 Java 中使用 Aspose.Imaging 載入並匯出 DjVu 頁面
url: /zh-hant/java/format-conversion-export/load-export-djvu-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 如何匯出 TIFF – 在 Java 中載入與匯出 DjVu 頁面使用 Aspose.Imaging

## 簡介

如果您需要在 Java 應用程式中 **如何匯出 TIFF** 從 DjVu 文件，您來對地方了。DjVu 是一種用於掃描文件的緊湊格式，但許多下游系統需要 TIFF。本教學將指導您載入 DjVu 檔案、挑選所需頁面，並使用 Aspose.Imaging for Java 將它們匯出為高品質的 TIFF 影像。完成後，您將擁有可重複使用的程式碼片段，能夠整合到任何基於 Java 的影像處理管線中。

**您將學習**
- 使用 Aspose.Imaging 在 Java 中載入 DjVu 影像  
- 將特定 DjVu 頁面匯出為 TIFF 格式  
- 設定匯出選項並了解關鍵參數  

在深入之前，請確保您的開發環境符合以下先決條件。

## 快速答覆
- **處理 DjVu 的主要類別是什麼？** `DjvuImage` 代表記憶體中的 DjVu 文件。  
- **匯出頁面為 TIFF 需要多少行程式碼？** 載入影像後只需兩行。  
- **哪個 Maven 套件提供 DjVu 支援？** `com.aspose:aspose-imaging`（版本 25.5+）。  
- **我可以一次匯出多個頁面嗎？** 可以，使用 `IntRange` 指定範圍。  
- **生產環境需要授權嗎？** 需要完整授權；亦提供臨時試用版。

## 什麼是「如何匯出 TIFF」？
**「如何匯出 TIFF」** 指的是將影像或文件頁面轉換為標記影像檔案格式 (TIFF) 的過程，這是一種廣泛用於檔案保存與列印的無損格式。Aspose.Imaging 透過單一 API 呼叫完成此轉換，並保留解析度與壓縮設定。此轉換保留所有視覺細節，適合高品質的檔案保存與後續處理。

## 為何在 Java 影像處理中使用 Aspose.Imaging？
Aspose.Imaging 支援 **150+** 種輸入與輸出格式，能處理高達 **5,000 頁** 的檔案而無需將整個文件載入記憶體，並提供執行緒安全的操作。這些具體的能力使其成為高吞吐量 Java 影像處理工作負載的可靠選擇，特別是在處理需要批次轉換且記憶體開銷極低的大量文件時。

## 先決條件

- **Aspose.Imaging for Java Library** – 版本 25.5 或更新。  
- **Java Development Kit (JDK)** – 8 或更新，已在您的機器上正確設定。  
- **Basic Java knowledge** – 您應該熟悉檔案 I/O 與例外處理。

## 如何設定 Maven Aspose Imaging？

要在 Maven 專案中加入 Aspose.Imaging，請將相依性加入專案的 `pom.xml`。Maven 會下載此函式庫及其傳遞相依性，讓 API 可於編譯與執行時使用。加入程式碼片段後，執行 `mvn clean install` 以確保套件已解析且專案成功建置。

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

## 如何設定 Gradle Aspose Imaging？

對於 Gradle 建置，請在 `build.gradle` 檔案中宣告 Aspose.Imaging 相依性。Gradle 會從 Maven Central 取得函式庫，讓您在 Java 程式碼中使用 API。更新腳本後，重新整理專案以下載 JAR 並同步相依性。

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

## 直接下載

您亦可從 [Aspose.Imaging releases](https://releases.aspose.com/imaging/java/) 下載最新的 JAR。

### 授權取得

- **Free Trial** – 取得臨時授權以供評估。  
- **Purchase** – 考慮購買完整授權以供生產使用。

## 初始化與設定

在使用任何 API 之前，必須先初始化函式庫。`License` 是用來將您的 Aspose.Imaging 授權檔套用至函式庫的類別，確保在無評估限制的情況下完整功能。

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path/to/your/license.lic");
```

## 如何載入 DjVu？

DjvuImage 是代表記憶體中 DjVu 檔案的頂層物件。要讀取 DjVu 文件，請使用檔案路徑呼叫靜態的 `Image.load()` 方法；此方法會回傳一個 `Image` 實例，您可將其轉型為 `DjvuImage`。`Image.load()` 為靜態方法，讀取影像檔並回傳代表已載入內容的 `Image` 物件。

```java
   String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "/Sample.djvu";
   ```

```java
   try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
       // The image is now loaded and ready for further processing.
   }
   ```

### 故障排除

- 確認檔案路徑正確且可存取。  
- 將載入呼叫包在 try‑catch 區塊中，以處理 `IOException` 或 `ImageLoadException`。

## 如何匯出 TIFF？

將 DjVu 頁面匯出為 TIFF 需要建立一個 `TiffOptions` 物件，以指定壓縮、解析度及其他設定，然後在目標頁面上呼叫 `save()` 方法。`TiffOptions` 是用來保存 TIFF 輸出設定的類別，例如壓縮類型與色彩深度。使用 `IntRange` 來選取要轉換的頁面，接著逐一迭代並將每頁另存為單獨的 TIFF 檔案。

建立輸出目錄，設定 `TiffOptions`，使用 `IntRange` 選取頁面，最後將每頁另存為 TIFF 檔案。

```java
   String outputDir = "YOUR_OUTPUT_DIRECTORY" + "/ConvertDjvuPagesToTiff_out.tiff";
   ```

```java
   TiffOptions exportOptions = new TiffOptions(TiffExpectedFormat.TiffDeflateBw);
   ```

```java
   IntRange range = new IntRange(0, 2); // Export the first three pages.
   exportOptions.setMultiPageOptions(new DjvuMultiPageOptions(range));
   ```

```java
   try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
       image.save(outputDir, exportOptions);
   }
   ```

### 常見陷阱

- 確保 `outputDir` 已存在；否則 `save()` 會拋出例外。  
- 記住頁面索引是 **零基** 的；第 1 頁的索引為 0。

## 實務應用

將 DjVu 頁面匯出為 TIFF 在多種情境下都很有用：

1. **Archival Systems** – 以通用接受的格式保存掃描文件。  
2. **Document Review Workflows** – 只提取需要註解的頁面。  
3. **Integration with DMS** – 將 TIFF 影像輸入不支援 DjVu 的現有文件管理流程中。

## 效能考量

處理大型 DjVu 檔案時：

- 使用 **try‑with‑resources** 以自動關閉串流並釋放記憶體。  
- 將檔案分批處理（例如一次 10 頁），以降低堆積記憶體佔用。  
- 對於黑白掃描，建議使用 `TiffCompression.CCITT4` 以在不失真情況下降低檔案大小。

## 常見問題

**Q:** 我該如何在專案中安裝 Aspose.Imaging for Java？  
**A:** 如上所示使用 Maven 或 Gradle，或直接從 [Aspose's releases page](https://releases.aspose.com/imaging/java/) 下載。

**Q:** 我可以將 DjVu 影像匯出為除 TIFF 之外的其他格式嗎？  
**A:** 可以，Aspose.Imaging 亦支援 PNG、JPEG、BMP 以及許多其他格式。

**Q:** 若授權檔未被識別，我該怎麼辦？  
**A:** 請確認授權路徑正確，且在使用任何其他 API 之前呼叫 `License.setLicense()`。

**Q:** 如何有效處理非常大的 DjVu 檔案？  
**A:** 將文件分成較小的頁面範圍處理，並及時釋放每個 `DjvuImage` 實例，以避免記憶體壓力。

**Q:** Aspose.Imaging 可免費用於商業用途嗎？  
**A:** 臨時試用授權是免費的，但生產環境需購買授權。

## 資源

- **文件說明**: [Aspose.Imaging Java API Reference](https://reference.aspose.com/imaging/java/)  
- **下載**: [Aspose.Imaging for Java Releases](https://releases.aspose.com/imaging/java/)  
- **購買**: [Buy Aspose.Imaging](https://purchase.aspose.com/buy)  
- **免費授權**: [Get a Free License](https://releases.aspose.com/imaging/java/)  
- **臨時授權**: [Request a Temporary License](https://purchase.aspose.com/temporary-license/)  
- **支援**: [Aspose Community Forum](https://forum.aspose.com/c/imaging/14)

透過熟悉上述步驟，您即可在任何基於 Java 的解決方案中可靠地 **如何匯出 TIFF** 從 DjVu 檔案。祝程式開發愉快！

---

**最後更新：** 2026-07-08  
**測試環境：** Aspose.Imaging 25.5 for Java  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [使用 Aspose.Imaging for Java 建立多頁 TIFF：完整指南](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [使用 Aspose.Imaging for Java 將 DjVu 轉換為 PDF – 步驟說明](/imaging/java/image-loading-saving/convert-djvu-to-pdf-aspose-imaging-java/)
- [使用 Aspose.Imaging 在 Java 中將 DJVU 轉換為 BMP：步驟說明](/imaging/java/format-conversion-export/export-djvu-pages-bmp-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}