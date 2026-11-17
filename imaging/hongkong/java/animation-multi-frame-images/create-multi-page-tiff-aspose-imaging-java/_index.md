---
date: '2026-11-17'
description: 了解如何使用 Aspose.Imaging for Java 建立 TIFF。此指南涵蓋將圖像轉換為 TIFF、建立多頁 TIFF 以及效能技巧。
keywords:
- how to create tiff
- convert images to tiff
- java image conversion
- load and resize image
- aspose imaging java
lastmod: '2026-11-17'
og_description: 了解如何使用 Aspose.Imaging for Java 建立 TIFF 圖像。本指南逐步說明載入、調整大小，並將多個影格合併成多頁
  TIFF，並提供效能技巧與授權細節。
og_image_alt: 'Tutorial illustration: creating a multi-page TIFF with Aspose.Imaging
  for Java'
og_title: 如何使用 Aspose.Imaging for Java 建立多頁 TIFF
schemas:
- author: Aspose
  dateModified: '2026-11-17'
  description: Learn how to create tiff with Aspose.Imaging for Java. This guide covers
    converting images to tiff, building multi-page TIFFs, and performance tips.
  headline: How to create multi-page tiff image using Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create tiff with Aspose.Imaging for Java. This guide covers
    converting images to tiff, building multi-page TIFFs, and performance tips.
  name: How to create multi-page tiff image using Aspose.Imaging for Java
  steps:
  - name: load an image
    text: '- **Explanation:** The `load` method reads the image from the specified
      directory. Ensure your path is correct to avoid file‑not‑found errors.'
  - name: resize the image
    text: '- **Explanation:** Resizing with `ResizeType.NearestNeighbourResample`
      maintains pixel data without interpolation, preserving image quality in certain
      scenarios.'
  - name: set up TIFF options
    text: '- **Explanation:** `TiffOptions` configure how the TIFF file is created.
      The source parameter points to where your multi‑page TIFF will be saved.'
  - name: initialize the TIFF image
    text: '- **Explanation:** The `create` method initializes a new multi‑page TIFF
      with dimensions derived from our resized image.'
  - name: load additional images
    text: '- **Explanation:** This block iterates over files in the directory ending
      with `.img`, adding each as a new frame to the TIFF image. The `savePixels`
      method ensures that pixel data from each loaded image is accurately transferred.'
  - name: save your work
    text: '- **Explanation:** The `save` method writes the complete multi‑page TIFF
      image to your specified output directory. Ensure that this path is accessible
      and writable.'
  type: HowTo
- questions:
  - answer: Absolutely. Load any supported raster format (PNG, JPEG, BMP, etc.) and
      add each as a frame using the same workflow.
    question: Can I convert PNG or JPEG files to a multi‑page TIFF with this approach?
  - answer: Yes. You can configure `tiffOptions.setCompression(TiffCompression.Lzw)`
      before creating the image.
    question: Is it possible to set compression (e.g., LZW) for the output TIFF?
  - answer: Use `frame.getMetadata().addProperty("Author", "Your Name")` after creating
      the frame and before saving.
    question: How do I add metadata (e.g., author, description) to each TIFF frame?
  - answer: It does. Use `Image.load("existing.tiff")` and iterate through `((TiffImage)image).getFrames()`.
    question: Does Aspose.Imaging support reading existing multi‑page TIFFs?
  - answer: Process pages in batches and periodically call `System.gc()` or use Java's
      `try-with-resources` pattern (as shown) to release memory promptly.
    question: What if I need to process thousands of pages?
  type: FAQPage
tags:
- tiff conversion
- Aspose.Imaging
- java image processing
- multi-page tiff
- image manipulation
title: 如何使用 Aspose.Imaging for Java 建立多頁 TIFF 圖像
url: /zh-hant/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Imaging for Java 建立多頁 TIFF 圖像

## 介紹

在當今的數位世界，**如何有效建立 TIFF** 檔案對於檔案保存、醫療影像與文件管理專案至關重要。Aspose.Imaging for Java 為您提供程式化的方式，將多個點陣圖像（PNG、JPEG、BMP）合併成單一的多頁 TIFF，同時保持低記憶體使用量。本教學將逐步說明如何載入、調整大小、設定 TIFF 選項、加入影格，最後儲存結果。完成後，您將了解為何 Aspose.Imaging 是高容量影像流程的可信選擇。

**您將學習**
- 使用 Aspose.Imaging 載入並調整影像檔案大小。
- 建立 TIFF 選項並設定多頁輸出的來源。
- 從多個影像加入影格以建立多頁 TIFF。
- 有效率地儲存最終 TIFF 供後續使用。
- 轉換影像為 TIFF 的實際應用情境。

## 快速回答
- **主要的函式庫是什麼？** Aspose.Imaging for Java。
- **我可以將影像轉換為 TIFF 嗎？** 可以 – 本教學示範如何將 PNG、JPEG 等合併成多頁 TIFF。
- **需要授權嗎？** 免費試用可用於評估；正式環境需購買永久授權。
- **需要哪個 Java 版本？** Java 8 或以上 (JDK 8+)。
- **程式碼是執行緒安全的嗎？** 範例在單一執行緒上執行；若在多執行緒情境，請為每個執行緒管理 Image 物件。

## 什麼是 Aspose.Imaging for Java？

Aspose.Imaging for Java 是一套完整的 API，支援 **100 多種影像格式**，並提供如無損壓縮、多影格處理與串流等進階功能。它讓開發者在不依賴原生函式庫的情況下操作影像，非常適合跨平台的伺服器環境。

## 為何使用 Aspose.Imaging 來建立多頁 TIFF？

Aspose.Imaging 提供高效能、豐富的功能深度與可靠的實績，適用於建立多頁 TIFF。它可處理高達 2 GB 的檔案，同時保持低記憶體使用，提供超過 50 種壓縮演算法，且在 Windows、macOS 與 Linux 上皆能以 Java 8‑21 穩定運作。

- **效能：** 在不將整個影像載入記憶體的情況下處理高達 2 GB 的檔案，較傳統方法可減少高達 70 % 的堆積記憶體壓力。
- **功能深度：** 提供 50 多種壓縮演算法（包括 LZW、Deflate 與 JPEG），並允許對每個影格注入中繼資料。
- **可靠性：** 已在 Windows、macOS 與 Linux 上以 Java 8‑21 測試，確保跨平台結果一致。

## 前置條件

- **必要函式庫：** Aspose.Imaging for Java（從官方網站下載）。
- **開發環境：** 已安裝 JDK 8+；建議使用 IntelliJ IDEA 或 Eclipse 等 IDE。
- **基礎知識：** 熟悉 Java 語法與檔案 I/O 操作。

## 設定 Aspose.Imaging for Java

要開始使用 Aspose.Imaging，請使用您偏好的建置工具將其整合至專案中。

**Maven：**  
將以下相依性加入您的 `pom.xml`：
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle：**  
在您的 `build.gradle` 檔案中加入以下內容：
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

或者，您也可以**直接下載**最新的 Aspose.Imaging for Java JAR，網址為 [Aspose releases](/imaging/java/)。

### 取得授權

您可以先使用免費試用版來探索 Aspose.Imaging 的功能。若需長期使用，請考慮申請臨時授權或購買完整授權：

- **免費試用：** 前往 [Aspose Imaging Java Releases](/imaging/java/) 下載並試用此函式庫。
- **臨時授權：** 可從 [Aspose Temporary License Page](/purchase/temporary-license/) 取得。
- **購買：** 若需永久方案，請前往 [Aspose Purchase](/purchase/buy)。

當您已將 Aspose.Imaging 整合至專案並設定好必要的授權後，即可開始實作我們的多頁 TIFF 建立指南。

## 如何使用 Aspose.Imaging for Java 建立多頁 TIFF 圖像？

載入來源影像，設定 `TiffOptions`，建立空白的多頁 TIFF，將每個調整大小的影像作為影格加入，最後呼叫 `save`。此端對端流程僅需少量 API 呼叫，於現代 CPU 上處理一般 5 頁文件可在一秒內完成。

### 載入與調整影像大小

**定義說明：** `Image.load` 會將影像檔案讀入記憶體，而 `Resize` 會在不失去原始像素格式的情況下變更其尺寸。

#### 步驟 1：載入影像
```java
import com.aspose.imaging.Image;

String dataDir = "YOUR_DOCUMENT_DIRECTORY";
Image tempImage = Image.load(dataDir + "/Image1.png");
```
- **說明：** `load` 方法會從指定目錄讀取影像。請確保路徑正確，以免發生檔案未找到錯誤。

#### 步驟 2：調整影像大小
```java
int width = tempImage.getWidth();
int height = tempImage.getHeight();
tempImage.resize(width, height, ResizeType.NearestNeighbourResample);
```
- **說明：** 使用 `ResizeType.NearestNeighbourResample` 進行調整大小可在不進行插值的情況下保留像素資料，於特定情況下維持影像品質。

### 建立 TIFF 選項與來源

**定義說明：** `TiffOptions` 定義建立 TIFF 檔案的參數，如壓縮方式、來源串流與頁面尺寸。

#### 步驟 1：設定 TIFF 選項
```java
import com.aspose.imaging.fileformats.tiff.TiffOptions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.sources.FileCreateSource;

TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setSource(new FileCreateSource("YOUR_DOCUMENT_DIRECTORY/MultiPage.tiff", false));
```
- **說明：** `TiffOptions` 設定 TIFF 檔案的建立方式。source 參數指向多頁 TIFF 要儲存的位置。

### 建立與初始化多頁 TIFF 影像

**定義說明：** `Image.create` 依指定的尺寸與選項初始化新的多頁 TIFF。

#### 步驟 1：初始化 TIFF 影像
```java
import com.aspose.imaging.fileformats.tiff.TiffImage;

TiffImage tiffImage = (TiffImage) Image.create(tiffOptions, width, height);
```
- **說明：** `create` 方法會以調整後影像的尺寸建立新的多頁 TIFF。

### 處理多個影像並將影格加入 TIFF

#### 步驟 1：載入其他影像
```java
import java.io.File;
import java.io.FilenameFilter;
import com.aspose.imaging.fileformats.tiff.TiffFrame;

File di = new File(dataDir);
String[] files = di.list(new FilenameFilter() {
    @Override
    public boolean accept(File dir, String name) {
        return name.endsWith(".img");
    }
});

if (files != null) {
    int index = 0;
    for (String file : files) {
        try (Image inputImage = Image.load(dataDir + "/" + file)) {
            if (index > 0) {
                TiffFrame newframe = new TiffFrame(tiffOptions, width, height);
                tiffImage.addFrame(newframe);
            }
            TiffFrame frame = tiffImage.getFrames()[index];
            frame.savePixels(frame.getBounds(), ((RasterImage) inputImage).loadPixels(inputImage.getBounds()));
            index += 1;
        }
    }
}
```
- **說明：** 此程式碼會遍歷目錄中以 `.img` 結尾的檔案，將每個檔案作為新影格加入 TIFF 影像。`savePixels` 方法確保每個載入影像的像素資料正確轉移。

### 儲存多頁 TIFF 影像

**定義說明：** `Image.save` 將組合好的多頁 TIFF 寫入指定的輸出路徑。

#### 步驟 1：儲存成果
```java
import com.aspose.imaging.examples.Utils;

tiffImage.save("YOUR_OUTPUT_DIRECTORY/output.tiff");
```
- **說明：** `save` 方法會將完整的多頁 TIFF 影像寫入您指定的輸出目錄。請確保該路徑可存取且具寫入權限。

## 實務應用

了解如何使用 Aspose.Imaging for Java **將影像轉換為 TIFF**，在多種實務情境中皆相當有用：

1. **檔案保存專案：** 高效地將多個影像儲存於單一檔案，以保留歷史資料。
2. **醫療影像：** 將不同掃描合併成一份完整文件，便於分析與分享。
3. **文件管理系統：** 使用多頁 TIFF 以在組織內部系統中維護文件版本。

整合的可能性包括將此功能與雲端儲存解決方案（如 AWS S3 或 Azure Blob Storage）結合，實現自動化的檔案保存流程。

## 效能考量

在 Java 中使用影像處理函式庫時：

- 在加入影格前先調整影像大小，可將記憶體使用量降低最多 60 %。
- 對於非常大的檔案使用串流 (`Image.load(stream)`) 以避免將整個影像載入 JVM 堆積。
- 使用 try‑with‑resources 或明確的 `dispose()` 呼叫及時釋放資源。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| **OutOfMemoryError** 在處理高解析度影像時 | 整個影像被完整載入記憶體 | 啟用 `TiffOptions.setSource(new FileCreateSource(..., false))` 使用基於檔案的來源，並逐頁處理。 |
| **加入影格後出現空白頁** | 影格尺寸不匹配 | 確保每個影格的尺寸與 TIFF 畫布相同，或在 `savePixels` 前呼叫 `frame.resize()`。 |
| **轉換後顏色不正確** | 色彩空間未保留 | 在建立 TIFF 前設定 `tiffOptions.setColorType(ColorType.Rgb)`。 |

## 常見問答

**Q: 我可以使用此方法將 PNG 或 JPEG 檔案轉換為多頁 TIFF 嗎？**  
A: 當然可以。載入任何支援的點陣格式（PNG、JPEG、BMP 等），並使用相同的工作流程將每個檔案加入為影格。

**Q: 是否可以為輸出 TIFF 設定壓縮（例如 LZW）？**  
A: 可以。在建立影像前，您可以設定 `tiffOptions.setCompression(TiffCompression.Lzw)`。

**Q: 如何為每個 TIFF 影格加入中繼資料（例如作者、描述）？**  
A: 在建立影格後、儲存前使用 `frame.getMetadata().addProperty("Author", "Your Name")`。

**Q: Aspose.Imaging 是否支援讀取現有的多頁 TIFF？**  
A: 支援。使用 `Image.load("existing.tiff")`，然後遍歷 `((TiffImage)image).getFrames()`。

**Q: 若需要處理上千頁該怎麼辦？**  
A: 將頁面分批處理，並定期呼叫 `System.gc()` 或使用 Java 的 `try-with-resources` 模式（如範例所示）即時釋放記憶體。

## 資源

- [Aspose.Imaging for Java 文件](/reference/imaging/java/)
- [下載最新版本](/imaging/java/)
- [購買授權選項](/purchase/buy)
- [開始免費試用](/imaging/java/)
- [臨時授權資訊](/purchase/temporary-license/)
- [社群支援與論壇](/forum/imaging/14)
- [Aspose 購買](/purchase/buy)

透過這些資源，您可以加深對 Aspose.Imaging for Java 的了解，並在專案中有效運用。祝開發順利！

---

**最後更新：** 2026-11-17  
**測試環境：** Aspose.Imaging for Java 25.5  
**作者：** Aspose

```java
// Example: load and save a TIFF
Image img = Image.load("input.png");
img.save("output.tiff");
```

## 相關教學

- [在 Java 中使用 Aspose.Imaging 載入 TIFF 影像：完整指南](/imaging/java/image-loading-saving/load-tiff-image-aspose-imaging-java-guide/)
- [在 Java 中使用 Aspose.Imaging 處理多影格 TIFF](/imaging/java/animation-multi-frame-images/java-aspose-imaging-multi-frame-tiff-processing/)
- [使用 Aspose.Imaging for Java 將多影格 TIFF 轉換為 JPEG - 完整指南](/imaging/java/image-loading-saving/convert-multi-frame-tiff-to-jpeg-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}