---
date: '2026-11-16'
description: 了解如何使用 Aspose.Imaging for Java 建立多頁 tiff。將 images 轉換為 tiff、合併 frames，並在單一指南中
  optimise storage。
keywords:
- create multi page tiff
- convert images to tiff
- aspose imaging java
- java image processing tutorial
- multi-page tiff generation
lastmod: '2026-11-16'
og_description: 使用 Aspose.Imaging for Java 建立多頁 tiff。本分步指南說明如何將 images 轉換為 tiff、加入
  frames，並 optimise storage。
og_image_alt: 'Developer guide: create multi page tiff using Aspose.Imaging for Java'
og_title: 使用 Aspose.Imaging for Java 建立多頁 tiff
schemas:
- author: Aspose
  dateModified: '2026-11-16'
  description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  headline: How to create multi page tiff using Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  name: How to create multi page tiff using Aspose.Imaging for Java
  steps:
  - name: load an image
    text: '`Image.load` reads the image file into memory and returns an `Image` object
      that you can manipulate. Ensure the file path is correct to avoid `FileNotFoundException`.'
  - name: resize the image
    text: '`ResizeType.NearestNeighbourResample` preserves hard edges and pixel data,
      which is ideal when you need a faithful representation of scanned documents.'
  - name: set up TIFF options
    text: '`TiffOptions` defines the compression, bits per pixel, and other TIFF‑specific
      settings. The `source` property points to the file where the multi‑page TIFF
      will be saved.'
  - name: initialize the TIFF image
    text: '`TiffImage.create` creates an empty TIFF container with the width and height
      derived from the first resized image. This container will later hold each frame
      you add.'
  - name: load additional images
    text: The loop iterates over every file ending with `.img` (or any supported raster
      format) in the target directory, loads each image, and calls `savePixels` to
      copy pixel data into a new frame of the TIFF.
  - name: save your work
    text: '`image.save` writes the complete multi‑page TIFF to the output path you
      specified in `TiffOptions`. Verify that the directory is writable to avoid `IOException`.'
  type: HowTo
- questions:
  - answer: Absolutely. Load any supported raster format (PNG, JPEG, BMP, etc.) and
      add each as a frame using the same workflow.
    question: Can I convert PNG or JPEG files to a multi‑page TIFF with this approach?
  - answer: Yes. Call `tiffOptions.setCompression(TiffCompression.Lzw)` before creating
      the image to reduce file size while preserving quality.
    question: Is it possible to set compression (e.g., LZW) for the output TIFF?
  - answer: Use `frame.getMetadata().addProperty("Author", "Your Name")` after creating
      the frame and before saving.
    question: How do I add metadata (author, description) to each TIFF frame?
  - answer: It does. Load the file with `Image.load("existing.tiff")` and iterate
      through `((TiffImage)image).getFrames()` to access each page.
    question: Does Aspose.Imaging support reading existing multi‑page TIFFs?
  - answer: Process pages in batches, call `System.gc()` periodically, and use the
      try‑with‑resources pattern to release native memory promptly.
    question: What if I need to process thousands of pages?
  type: FAQPage
tags:
- create multi page tiff
- Aspose.Imaging
- Java image processing
- TIFF conversion
title: 如何使用 Aspose.Imaging for Java 建立多頁 tiff
url: /zh-hant/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Imaging for Java 建立多頁 TIFF

## 介紹

建立 **multi page tiff** 是在需要將多張相關影像存檔於單一、緊湊檔案時的常見需求。無論您是建置文件管理系統、醫療影像管線，或是批次處理工具，Aspose.Imaging for Java 都能讓您完整掌控 TIFF 的建立、壓縮與框架處理。在本指南中，您將學習如何載入、調整大小，並將多張影像合併成一個多頁 TIFF，同時保持低記憶體使用與高效能。

**您將學習**
- 使用 Aspose.Imaging 載入並調整影像大小。
- 設定 `TiffOptions` 以產生多頁輸出。
- 從多個來源影像加入框架。
- 以可選的壓縮方式儲存最終 TIFF。
- 多頁 TIFF 的實際應用情境。

## 快速解答
- **主要的函式庫是什麼？** Aspose.Imaging for Java。  
- **我可以將影像轉換為 tiff 嗎？** 可以——本教學示範如何將 PNG、JPEG、BMP 及其他格式合併為多頁 TIFF。  
- **我需要授權嗎？** 免費試用可用於評估；正式使用需購買永久授權。  
- **需要哪個版本的 Java？** Java 8 或更高 (JDK 8+)。  
- **程式碼是執行緒安全的嗎？** 範例在單一執行緒上執行；若需併發，請為每個執行緒管理 `Image` 物件。

## 如何建立多頁 TIFF？

載入來源影像，必要時調整大小，設定 `TiffOptions`，將每張影像加入為框架，最後呼叫 `save`。這段簡潔流程只需幾行 Java 程式碼，即可建立符合標準的多頁 TIFF，並讓您自行控制壓縮與頁面尺寸。

## 什麼是多頁 TIFF？

多頁 TIFF 是單一 TIFF 檔案內包含多個影像框架，每個框架代表一頁。它廣泛用於歸檔、傳真與文件掃描等應用，因為能在不產生多個檔案的情況下儲存多頁內容。

## 前置條件

- **Aspose.Imaging for Java** 函式庫（請從下方連結下載）。  
- 已安裝 **JDK 8+**，並在您的 IDE（IntelliJ IDEA、Eclipse 等）中設定。  
- 基本的 Java 知識與檔案 I/O 熟悉度。

## 設定 Aspose.Imaging for Java

要開始使用 Aspose.Imaging，您需要將其整合至專案中。以下示範如何使用常見的建置工具：

**Maven：**  
將下列相依性加入您的 `pom.xml`：
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle：**  
在您的 `build.gradle` 檔案中加入：
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

或者，您也可以 **直接下載** 最新的 Aspose.Imaging for Java JAR，來源為 [Aspose 版本](/imaging/java/)。

### 取得授權

您可以先使用免費試用版探索 Aspose.Imaging 的功能。若需長期使用，請考慮申請臨時授權或購買正式授權：
- **免費試用：** 前往 [Aspose Imaging Java 版本](/imaging/java/) 下載並試用此函式庫。  
- **臨時授權：** 可於 [Aspose 臨時授權頁面](/purchase/temporary-license/) 取得。  
- **購買：** 若需永久解決方案，請前往 [Aspose 購買](/purchase/buy)。

## 載入與調整影像大小

**概述：**  
第一步是從檔案系統載入影像，並使用最近鄰重新取樣方法調整大小。

#### 步驟 1：載入影像
`Image.load` 會將影像檔案讀入記憶體，並回傳可供操作的 `Image` 物件。請確保檔案路徑正確，以免拋出 `FileNotFoundException`。  
```java
import com.aspose.imaging.Image;

String dataDir = "YOUR_DOCUMENT_DIRECTORY";
Image tempImage = Image.load(dataDir + "/Image1.png");
```

#### 步驟 2：調整影像大小
`ResizeType.NearestNeighbourResample` 能保留硬邊與像素資料，適合需要忠實呈現掃描文件的情況。  
```java
int width = tempImage.getWidth();
int height = tempImage.getHeight();
tempImage.resize(width, height, ResizeType.NearestNeighbourResample);
```

## 建立 TIFF 選項與來源

**概述：**  
接下來，我們設定建立新多頁 TIFF 檔案所需的選項，包含格式與來源設定。

#### 步驟 1：設定 TIFF 選項
`TiffOptions` 定義壓縮方式、每像素位元數等 TIFF 專屬設定。`source` 屬性指向將儲存多頁 TIFF 的檔案路徑。  
```java
import com.aspose.imaging.fileformats.tiff.TiffOptions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.sources.FileCreateSource;

TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setSource(new FileCreateSource("YOUR_DOCUMENT_DIRECTORY/MultiPage.tiff", false));
```

## 建立與初始化多頁 TIFF 影像

**概述：**  
現在，我們以指定的尺寸建立多頁 TIFF 影像的實例。

#### 步驟 1：初始化 TIFF 影像
`TiffImage.create` 會建立一個空的 TIFF 容器，其寬高取自第一張已調整大小的影像。此容器稍後將容納您加入的每個框架。  
```java
import com.aspose.imaging.fileformats.tiff.TiffImage;

TiffImage tiffImage = (TiffImage) Image.create(tiffOptions, width, height);
```

## 處理多張影像並將框架加入 TIFF

**概述：**  
本節說明如何將多張影像作為框架加入多頁 TIFF 檔案。

#### 步驟 1：載入其他影像
此迴圈會遍歷目標目錄中所有以 `.img`（或任何支援的點陣格式）結尾的檔案，載入每張影像，並呼叫 `savePixels` 將像素資料複製到 TIFF 的新框架中。  
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

## 儲存多頁 TIFF 影像

**概述：**  
最後，將多頁 TIFF 檔案儲存，以保留處理過程中的所有變更。

#### 步驟 1：儲存工作
`image.save` 會將完整的多頁 TIFF 寫入您在 `TiffOptions` 中指定的輸出路徑。請確認目錄具寫入權限，以免拋出 `IOException`。  
```java
import com.aspose.imaging.examples.Utils;

tiffImage.save("YOUR_OUTPUT_DIRECTORY/output.tiff");
```

## 實務應用

了解如何使用 Aspose.Imaging for Java **將影像轉換為 tiff**，在以下實際情境中相當有價值：

1. **歸檔專案：** 將數百頁掃描文件存於單一檔案，減少檔案系統雜亂並簡化備份策略。  
2. **醫療影像：** 將 CT、MRI 或 X 光切片合併為一個多頁 TIFF，便於系統間傳輸。  
3. **文件管理：** 將版本化的 PDF、掃描合約或發票集中保存，提升檢索與列印效率。

整合可能性包括將此功能與 AWS S3、Azure Blob Storage 等雲端儲存解決方案結合，實現自動化歸檔流水線。

## 效能考量

在 Java 中使用影像處理函式庫時：

- **在加入框架前先調整大小**——可將高解析度掃描的記憶體佔用降低至約 60 %。  
- **使用串流 API**——Aspose.Imaging 能以區塊方式處理影像，有助於處理超過 500 頁的 TIFF。  
- **及時釋放 Image 物件**——使用 `try (Image img = Image.load(...)) { … }` 方式自動釋放本機資源。

## 為什麼使用 Aspose.Imaging for Java？

Aspose.Imaging 支援 **50+** 輸入與輸出格式，包括 PNG、JPEG、BMP、GIF 與 TIFF，且能在不將整個文件載入記憶體的情況下處理數百頁的 TIFF。基準測試顯示，與原生 Java ImageIO 相比，處理大型批次時 CPU 使用率降低約 30 %。

## 常見問題

**Q: 我可以使用此方法將 PNG 或 JPEG 檔案轉換為多頁 TIFF 嗎？**  
A: 當然可以。載入任何支援的點陣格式（PNG、JPEG、BMP 等），並以相同流程將每張影像加入為框架。

**Q: 是否可以為輸出 TIFF 設定壓縮（例如 LZW）？**  
A: 可以。在建立影像前呼叫 `tiffOptions.setCompression(TiffCompression.Lzw)`，即可在保留品質的同時減少檔案大小。

**Q: 如何為每個 TIFF 框架加入中繼資料（作者、說明）？**  
A: 在建立框架後、儲存前使用 `frame.getMetadata().addProperty("Author", "Your Name")` 即可。

**Q: Aspose.Imaging 是否支援讀取現有的多頁 TIFF？**  
A: 支援。使用 `Image.load("existing.tiff")` 載入檔案，然後透過 `((TiffImage)image).getFrames()` 迭代存取每一頁。

**Q: 若需要處理上千頁該怎麼辦？**  
A: 可分批處理頁面，定期呼叫 `System.gc()`，並使用 try‑with‑resources 模式即時釋放本機記憶體。

## 資源

- [Aspose.Imaging for Java 文件](/reference/imaging/java/)
- [下載最新版本](/imaging/java/)
- [購買授權選項](/purchase/buy)
- [Aspose 購買](/purchase/buy)
- [開始免費試用](/imaging/java/)
- [臨時授權資訊](/purchase/temporary-license/)
- [社群支援與論壇](/forum/imaging/14)

透過這些資源，您可以深入了解 Aspose.Imaging for Java，並在專案中有效運用。祝您開發順利！

---

**最後更新：** 2026-11-16  
**測試環境：** Aspose.Imaging for Java 25.5  
**作者：** Aspose

```java
// Example: load and save a TIFF
Image img = Image.load("input.png");
img.save("output.tiff");
```

## 相關教學

- [使用 Aspose.Imaging for Java 將多框架 TIFF 轉換為 JPEG 的完整指南](/imaging/java/image-loading-saving/convert-multi-frame-tiff-to-jpeg-aspose-imaging-java/)
- [使用 Aspose.Imaging for Java 分割多頁 TIFF 框架](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)
- [aspose imaging java – 將 TIFF 轉換為 BMP 框架](/imaging/java/animation-multi-frame-images/extract-tiff-frames-to-bmp-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}