---
date: '2026-02-22'
description: 學習如何使用 Aspose.Imaging for Java 建立 TIFF 圖像。本教學示範如何將圖像轉換為 TIFF、將多個影格合併成多頁
  TIFF，並優化儲存空間。
keywords:
- multi-page TIFF creation
- Aspose.Imaging for Java
- Java image processing tutorial
- create TIFF with Aspose in Java
- animation & multi-frame images
title: 如何使用 Aspose.Imaging for Java 建立多頁 TIFF – 完整指南
url: /zh-hant/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/
weight: 1
---

 unchanged.

So:

**最後更新：** 2026-02-22  
**測試環境：** Aspose.Imaging for Java 25.5  
**作者：** Aspose

Make sure bold formatting preserved.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 如何使用 Aspose.Imaging for Java 建立多頁 TIFF 圖像

## 簡介

在當今的數位世界，學習 **如何建立 tiff** 圖像的高效方法對企業與開發者都至關重要。無論您是處理檔案保存專案，或是開發需要進階影像處理的應用程式，精通多頁 TIFF 產生可節省時間與儲存空間。本教學將使用 Aspose.Imaging for Java，從載入與調整影像大小，到組合成單一多頁 TIFF 檔案，完整說明整個流程。

**您將學習**
- 如何 **載入與調整影像** 檔案與 Aspose.Imaging。
- 建立 TIFF 選項並設定多頁輸出的來源。
- 從多張影像加入框架以建構多頁 TIFF。
- 有效率地儲存最終 TIFF 供後續使用。
- 實務情境中，將影像轉換為 TIFF 的價值。

在深入實作之前，我們先說明一些先決條件，確保您具備所有必要的環境，以順利跟隨本教學。

## 快速答覆
- **主要的函式庫是什麼？** Aspose.Imaging for Java。
- **我可以將影像轉換為 tiff 嗎？** 可以 – 本教學示範如何將 PNG、JPEG 等合併成多頁 TIFF。
- **我需要授權嗎？** 免費試用可用於評估；正式環境需購買永久授權。
- **需要哪個版本的 Java？** Java 8 或以上 (JDK 8+)。
- **程式碼是執行緒安全的嗎？** 範例在單一執行緒上執行；若在多執行緒情境，請為每個執行緒管理 Image 物件。

## 先決條件

要成功執行本教學提供的程式碼範例，您需要：

- **必要的函式庫**：Aspose.Imaging for Java 函式庫。
- **環境設定**：確保開發環境已安裝 JDK（Java Development Kit）。建議使用 IntelliJ IDEA 或 Eclipse 等 IDE，以提升使用便利性。
- **知識先備**：具備 Java 程式設計的基本概念，並熟悉 Java 的檔案 I/O 操作。

## 設定 Aspose.Imaging for Java

要開始使用 Aspose.Imaging，您需要將其整合至專案中。以下說明如何使用常見的建置工具完成此步驟：

**Maven:**  
將以下相依性加入您的 `pom.xml`：
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle:**  
在您的 `build.gradle` 檔案中加入以下內容：
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

或者，您也可以 **直接下載** 最新的 Aspose.Imaging for Java JAR，來源請見 [Aspose releases](https://releases.aspose.com/imaging/java/)。

### 授權取得

您可以先使用免費試用版來探索 Aspose.Imaging 的功能。若需長期使用，請考慮申請臨時授權或購買正式授權：

- **免費試用**：前往 [Aspose Imaging Java Releases](https://releases.aspose.com/imaging/java/) 下載並試用此函式庫。
- **臨時授權**：可於 [Aspose Temporary License Page](https://purchase.aspose.com/temporary-license/) 取得。
- **購買**：若需永久授權，請前往 [Aspose Purchase](https://purchase.aspose.com/buy)。

完成 Aspose.Imaging 的整合與授權設定後，即可開始實作本多頁 TIFF 建立指南。

## 如何使用 Aspose.Imaging for Java 建立多頁 TIFF 圖像

### 載入與調整影像大小

**概述：**  
第一步是從檔案系統載入影像，並使用最近鄰重新取樣方法調整大小。

#### 步驟 1：載入影像
```java
import com.aspose.imaging.Image;

String dataDir = "YOUR_DOCUMENT_DIRECTORY";
Image tempImage = Image.load(dataDir + "/Image1.png");
```
- **說明**：`load` 方法會從指定目錄讀取影像。請確認路徑正確，以免發生找不到檔案的錯誤。

#### 步驟 2：調整影像大小
```java
int width = tempImage.getWidth();
int height = tempImage.getHeight();
tempImage.resize(width, height, ResizeType.NearestNeighbourResample);
```
- **說明**：使用 `ResizeType.NearestNeighbourResample` 進行調整，可在不進行插值的情況下保留像素資料，於特定情境下維持影像品質。

### 建立 TIFF 選項與來源

**概述：**  
接下來，我們設定建立新多頁 TIFF 檔案所需的選項。這包括指定預期的格式與來源設定。

#### 步驟 1：設定 TIFF 選項
```java
import com.aspose.imaging.fileformats.tiff.TiffOptions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.sources.FileCreateSource;

TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setSource(new FileCreateSource("YOUR_DOCUMENT_DIRECTORY/MultiPage.tiff", false));
```
- **說明**：`TiffOptions` 用於配置 TIFF 檔案的建立方式。source 參數指向多頁 TIFF 將被儲存的位置。

### 建立與初始化多頁 TIFF 影像

**概述：**  
現在，我們以指定的尺寸建立多頁 TIFF 影像的實例。

#### 步驟 1：初始化 TIFF 影像
```java
import com.aspose.imaging.fileformats.tiff.TiffImage;

TiffImage tiffImage = (TiffImage) Image.create(tiffOptions, width, height);
```
- **說明**：`create` 方法會以調整後影像的尺寸建立新的多頁 TIFF。

### 處理多張影像並將框架加入 TIFF

**概述：**  
本節說明如何將多張影像作為框架加入多頁 TIFF 檔案。

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
- **說明**：此程式碼會遍歷目錄中以 `.img` 結尾的檔案，將每個檔案作為新框架加入 TIFF 影像。`savePixels` 方法確保每個載入影像的像素資料正確傳遞。

### 儲存多頁 TIFF 影像

**概述：**  
最後，將多頁 TIFF 檔案儲存，以保留處理過程中所有的變更。

#### 步驟 1：儲存成果
```java
import com.aspose.imaging.examples.Utils;

tiffImage.save("YOUR_OUTPUT_DIRECTORY/output.tiff");
```
- **說明**：`save` 方法會將完整的多頁 TIFF 影像寫入您指定的輸出目錄。請確保該路徑可存取且具寫入權限。

## 實務應用

了解如何使用 Aspose.Imaging for Java **將影像轉換為 tiff**，在多種實務情境中皆相當有用：

1. **檔案保存專案**：將多張影像有效率地存放於單一檔案，以供歷史資料保存。
2. **醫學影像**：將不同的掃描結果合併為一份完整文件，便於分析與共享。
3. **文件管理系統**：使用多頁 TIFF 以維護組織內部系統的文件版本。

此功能可整合至雲端儲存服務，如 AWS S3 或 Azure Blob Storage，實現自動化的檔案保存流程。

## 效能考量

在 Java 中使用影像處理函式庫時：

- 在加入框架前先調整影像大小，以降低記憶體使用量與處理時間。
- 使用適當的資料結構，以有效處理大量框架。
- 謹慎管理 Java 記憶體，特別是處理高解析度影像或大量框架時。

## 結論

使用 Aspose.Imaging for Java 建立多頁 TIFF 是處理複雜影像處理任務的強大方法。透過本指南，您已學會如何載入與調整影像、設定 TIFF 選項、將多張影像處理為框架，並有效地儲存最終輸出。

接下來可探索 Aspose.Imaging 的其他功能，例如進階影像操作，或與其他 API 結合，以擴展應用範圍。

## 常見問答

1. **什麼是 Aspose.Imaging for Java？**  
   - 它是一套完整的函式庫，用於在 Java 應用程式中管理各種影像格式，提供廣泛的操作與轉換功能。

2. **如何有效處理大型 TIFF 檔案？**  
   - 可考慮使用串流技術，以分塊方式處理影像，而非一次載入整個檔案至記憶體。

3. **Aspose.Imaging 可用於商業專案嗎？**  
   - 可以，需取得商業授權。請前往 [Aspose Purchase](https://purchase.aspose.com/buy) 了解授權方案。

4. **執行 Aspose.Imaging 的系統需求為何？**  
   - 請確保使用相容的 Java Development Kit (JDK) 版本。此函式庫與平台無關，應可在 Windows、macOS 與 Linux 上運作。

5. **使用 Aspose.Imaging 建立多頁 TIFF 有什麼限制嗎？**  
   - 雖然功能強大，但需留意系統記憶體限制，處理大型影像或大量框架時可能會消耗大量記憶體。

## 常見問題

**Q: 我可以使用此方法將 PNG 或 JPEG 檔案轉換為多頁 TIFF 嗎？**  
A: 當然可以。載入任何支援的點陣格式（PNG、JPEG、BMP 等），並以相同流程將每個檔案加入為框架。

**Q: 能否為輸出 TIFF 設定壓縮（例如 LZW）？**  
A: 可以。在建立影像前，可設定 `tiffOptions.setCompression(TiffCompression.Lzw)`。

**Q: 如何為每個 TIFF 框架加入中繼資料（如作者、描述）？**  
A: 在建立框架後、儲存前，使用 `frame.getMetadata().addProperty("Author", "Your Name")`。

**Q: Aspose.Imaging 支援讀取已存在的多頁 TIFF 嗎？**  
A: 支援。使用 `Image.load("existing.tiff")`，並遍歷 `((TiffImage)image).getFrames()`。

**Q: 若需處理上千頁該怎麼辦？**  
A: 可分批處理頁面，並定期呼叫 `System.gc()`，或使用 Java 的 `try-with-resources` 模式（如範例所示）即時釋放記憶體。

## 資源

- [Aspose.Imaging for Java 文件說明](https://reference.aspose.com/imaging/java/)
- [下載最新版本](https://releases.aspose.com/imaging/java/)
- [購買授權方案](https://purchase.aspose.com/buy)
- [開始免費試用](https://releases.aspose.com/imaging/java/)
- [臨時授權資訊](https://purchase.aspose.com/temporary-license/)
- [社群支援與論壇](https://forum.aspose.com/c/imaging/14)

透過這些資源，您可以深入了解 Aspose.Imaging for Java，並在專案中有效運用。祝程式開發愉快！

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-02-22  
**測試環境：** Aspose.Imaging for Java 25.5  
**作者：** Aspose