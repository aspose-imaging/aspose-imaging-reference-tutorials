---
date: '2026-03-20'
description: 學習如何使用 Aspose.Imaging for Java 以 LZW 壓縮方式壓縮 TIFF 圖像，減少檔案大小同時保持品質。
keywords:
- compress TIFF images Java
- Aspose.Imaging LZW compression
- Java image optimization
- TIFF compression in Java with Aspose
- image compression tutorial
title: 如何使用 Aspose.Imaging 在 Java 中壓縮 TIFF 圖像（LZW 壓縮指南）
url: /zh-hant/java/compression-optimization/compress-tiff-images-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 教學：使用 Aspose.Imaging Java 壓縮 TIFF 圖像

## 簡介

在本教學中，您將學習 **如何使用 Aspose.Imaging for Java** 來有效壓縮 TIFF 圖像。管理大型 TIFF 檔案會迅速佔用儲存空間和頻寬，但使用 LZW（Lempel‑Ziv‑Welch）壓縮，您可以 **減少 TIFF 檔案大小** 而不犧牲圖像品質。我們將示範如何載入 TIFF、設定 **tiff compression LZW**，以及儲存優化後的結果——非常適合對 **java image optimization** 有興趣的讀者。

**您將學到**
- 如何設定 Aspose.Imaging for Java
- 輕鬆載入與處理 TIFF 圖像
- 使用 `TiffOptions` 設定 LZW 壓縮
- 儲存更小且無失真的優化 TIFF 圖像

讓我們先處理先決條件，讓您可以立即開始壓縮。

## 快速解答
- **需要的函式庫是什麼？** Aspose.Imaging for Java  
- **使用哪種壓縮演算法？** LZW（無損）  
- **支援的 Java 版本？** 大多數最新的 JDK（例如 11、17）  
- **需要授權嗎？** 測試可使用試用或臨時授權；正式環境需購買商業授權。  
- **典型的尺寸縮減率？** 適合的圖像可減少 30‑50 %  

## 先決條件

在 Java 專案中實作圖像壓縮之前，請確保具備以下項目：

- **Aspose.Imaging for Java library** – 所有影像處理功能的必要套件。  
- **Java Development Kit (JDK)** – 與 Aspose 套件相容的最新版本。  
- **基本的 Java 知識** – 熟悉檔案 I/O 與物件導向概念會有幫助。  

## 設定 Aspose.Imaging for Java

首先，將 Aspose.Imaging 套件加入您的建置系統。選擇最符合您專案的方式。

### 使用 Maven
在您的 `pom.xml` 中加入以下相依性：

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### 使用 Gradle
在您的 `build.gradle` 檔案中加入此行：

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### 直接下載
或者，從 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下載最新版本。

#### 取得授權
您可以取得免費試用授權或申請臨時授權，以在購買前完整評估 Aspose.Imaging 的功能。

## 如何在 Java 中使用 Aspose.Imaging 進行 TIFF 壓縮

現在讓我們一步步拆解實作細節。每段程式碼保持原樣，我們會在旁邊提供更清晰的說明。

### 載入 TIFF 圖像

**為什麼這很重要：** 正確載入圖像會建立有效的 `Image` 物件，之後的所有操作皆基於此物件。

#### 步驟 1：匯入 Image 類別
```java
import com.aspose.imaging.Image;
```

#### 步驟 2：從磁碟載入圖像
```java
String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "/sample.tiff";
Image image = Image.load(dataDir);
```

### 建立 TiffOptions 以進行圖像壓縮

**為什麼這很重要：** `TiffOptions` 讓您精確定義輸出 TIFF 的編碼方式，包括 **tiff compression LZW** 設定。

#### 步驟 1：匯入必要的列舉與選項類別
```java
import com.aspose.imaging.fileformats.tiff.enums.TiffCompressions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.imaging.imageoptions.TiffOptions;
```

#### 步驟 2：設定壓縮選項
```java
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);
outputSettings.setBitsPerSample(new int[] { 4 });
outputSettings.setCompression(TiffCompressions.Lzw);
outputSettings.setPhotometric(TiffPhotometrics.Palette);
```

### 設定灰階調色盤（可選但有幫助）

套用 4 位元灰階調色盤可進一步 **減少 TIFF 檔案大小**，尤其適用於單色掃描。

#### 步驟 1：匯入調色盤輔助類別
```java
import com.aspose.imaging.ColorPaletteHelper;
```

#### 步驟 2：指派灰階調色盤
```java
outputSettings.setPalette(ColorPaletteHelper.create4BitGrayscale(false));
```

### 儲存壓縮後的 TIFF 圖像

**為什麼這很重要：** `save` 呼叫會依照您設定的所有選項將圖像寫入磁碟，產生更小且經 LZW 壓縮的檔案。

#### 步驟 1：定義輸出路徑
```java
String outputDir = "YOUR_OUTPUT_DIRECTORY" + "/SampleTiff_out.tiff";
```

#### 步驟 2：使用壓縮設定儲存
```java
image.save(outputDir, outputSettings);
```

## 實務應用

以下是一些實際情境，使用 LZW 壓縮 **how to compress tiff** 圖像可帶來顯著效益：

1. **文件歸檔** – 更有效率地儲存掃描的 PDF 或 TIFF。  
2. **醫學影像** – 在保持診斷細節的同時，讓檔案大小易於管理。  
3. **攝影檔案** – 保留高解析度原始檔而不致佔用過多儲存空間。  
4. **Web 應用程式** – 提供較小的圖像以加快頁面載入速度並降低頻寬成本。  

## 效能考量

處理大型圖像時，請留意以下技巧以維持最佳效能：

- **記憶體管理：** 若在迴圈中處理多個檔案，請即時釋放大型 `Image` 物件（`image.dispose()`）。  
- **位元深度最佳化：** 將 `BitsPerSample` 調整至您使用情境可接受的最低值。  
- **批次處理：** 大量作業可考慮多執行緒，但需監控 JVM 堆積使用情況。  

## 常見問題與解決方案

| 症狀 | 可能原因 | 解決方法 |
|---------|--------------|-----|
| 載入大型 TIFF 時發生 OutOfMemoryError | 圖像完整載入記憶體 | 使用 `Image.load(dataDir, new LoadOptions { BufferSize = … })` 或以分塊方式處理。 |
| 儲存的檔案比原始檔案更大 | `BitsPerSample` 設定不正確或調色盤不匹配 | 確認 `setBitsPerSample` 與來源圖像的色深相符。 |
| 灰階調色盤顯示異常 | 儲存前未套用調色盤 | 確保在呼叫 `image.save` 之前 **先** 呼叫 `outputSettings.setPalette(...)`。 |

## 常見問答

**Q：什麼是 LZW 壓縮？**  
A：Lempel‑Ziv‑Welch（LZW）壓縮是一種無損演算法，可在不遺失任何圖像資料的情況下減少檔案大小。

**Q：我可以在商業專案中使用 Aspose.Imaging for Java 嗎？**  
A：可以，您可以購買授權以商業使用。詳情請參閱 [Aspose Purchase](https://purchase.aspose.com/buy)。

**Q：此函式庫相容所有 JDK 版本嗎？**  
A：支援大多數最新的 JDK 版本。請查閱官方文件以確認具體相容版本。

**Q：如何在不耗盡記憶體的情況下處理大型圖像？**  
A：實施有效的記憶體管理，例如即時釋放 `Image` 物件，並在可能時將圖像分成較小的區塊處理。

**Q：Aspose.Imaging 支援哪些其他檔案格式？**  
A：此函式庫支援 BMP、JPEG、PNG、GIF 等多種格式。請於其 [documentation site](https://reference.aspose.com/imaging/java/) 查看完整清單。

## 資源

- **文件：** [Aspose.Imaging Java Reference](https://reference.aspose.com/imaging/java/)  
- **下載：** [Latest Releases](https://releases.aspose.com/imaging/java/)  
- **購買：** [Buy Now](https://purchase.aspose.com/buy)  
- **免費試用：** [Start Here](https://releases.aspose.com/imaging/java/)  
- **臨時授權：** [Request Here](https://purchase.aspose.com/temporary-license/)  
- **支援：** 如需進一步協助，請前往 [Aspose Forum](https://forum.aspose.com/c/imaging/14)

---  

**最後更新：** 2026-03-20  
**測試環境：** Aspose.Imaging 25.5 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}