---
"date": "2025-06-04"
"description": "學習如何使用 Aspose.Imaging for Java 輕鬆將 DICOM 影像轉換為 BMP 格式並調整其大小。非常適合醫學影像存檔和網頁顯示。"
"title": "使用 Aspose.Imaging 在 Java 中將 DICOM 轉換為 BMP —— 完整指南"
"url": "/zh-hant/java/format-conversion-export/aspose-imaging-java-dicom-to-bmp-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 如何使用 Aspose.Imaging Java 載入並重新儲存 DICOM 映像為 BMP

## 介紹

在數位成像領域，管理醫學影像至關重要。專業人員通常需要將這些影像從一種格式轉換為另一種格式，同時保持其完整性。本教學將指導您使用 Aspose.Imaging for Java 載入 DICOM 映像並將其重新儲存為 BMP 格式。您還將學習如何按比例調整 DICOM 影像的高度。

**您將學到什麼：**

- 如何使用 Aspose.Imaging Java 將 DICOM 映像轉換為 BMP
- 保持比例的同時調整 DICOM 影像大小的技術
- 在您的開發環境中設定 Aspose.Imaging for Java

在深入實施之前，讓我們確保您已經滿足了先決條件。 

## 先決條件

為了有效地遵循本教程，您需要：

- **Aspose.Imaging 庫**：確保您擁有 25.5 或更高版本。
- **Java 開發工具包 (JDK)**：建議使用版本 8 或更高版本以確保相容性。
- **IDE 設定**：使用 IntelliJ IDEA 或 Eclipse 等 IDE 來編寫和測試您的 Java 程式碼。

## 設定 Aspose.Imaging for Java

首先，我們需要在您的專案中設定 Aspose.Imaging。您可以使用 Maven 或 Gradle 作為建置工具。

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
implementation 'com.aspose:aspose-imaging:25.5'
```

或者，您可以直接從 [Aspose.Imaging for Java 版本](https://releases。aspose.com/imaging/java/).

### 許可證獲取

要開始使用 Aspose.Imaging，您可以：

- **免費試用**：透過有限試用來測試其功能。
- **臨時執照**：取得臨時許可證以探索全部功能。
- **購買**：為了延長使用時間，請考慮購買許可證。

**初始化和設定：**

安裝庫後，請在 Java 應用程式中對其進行初始化。這包括設定檔案目錄並確保正確引用 Aspose.Imaging 庫。

## 實施指南

我們將把實現分解為兩個主要特徵：

### 載入並重新儲存 DICOM 映像為 BMP

#### 概述

此功能可示範如何從磁碟載入 DICOM 映像並將其儲存為 BMP 格式，使其可供非醫療應用程式或需要基本映像格式的系統存取。

#### 逐步實施

1. **設定目錄**

   定義 DICOM 檔案所在的輸入和輸出目錄以及想要儲存 BMP 的位置。
   ```java
   String dataDir = "YOUR_DOCUMENT_DIRECTORY";
   String inputFile = dataDir + "image.dcm";
   String outputFile = "YOUR_OUTPUT_DIRECTORY" + "ResizedOutput.bmp";
   ```

2. **載入並儲存 DICOM 映像**

   使用 `DicomImage` 從 Aspose.Imaging 載入圖像，然後以 BMP 格式儲存。
   ```java
   try (DicomImage image = (DicomImage) Image.load(inputFile)) {
       // 將圖像儲存為 BMP 檔案。
       image.save(outputFile, new BmpOptions());
   }
   ```

3. **解釋參數**

   - `inputFile`：您的 DICOM 檔案的路徑。
   - `outputFile`：BMP 輸出的目標路徑。
   - `BmpOptions()`：BMP格式的配置設定。

### 按比例調整高度

#### 概述

此功能可讓您按比例調整 DICOM 影像的高度，保留其縱橫比並將其儲存為 BMP 檔案。

#### 逐步實施

1. **載入 DICOM 映像**

   首先使用 Aspose.Imaging 載入您的 DICOM 映像。
   ```java
   String inputFile = dataDir + "image.dcm";
   String outputFile = "YOUR_OUTPUT_DIRECTORY" + "ResizeHeightProportionally_out.bmp";

   try (DicomImage image = (DicomImage) Image.load(inputFile)) {
       // 按比例調整高度為 100 像素。
       image.resizeHeightProportionally(100, ResizeType.AdaptiveResample);
       
       // 以 BMP 格式儲存調整大小的影像。
       image.save(outputFile, new BmpOptions());
   }
   ```

2. **參數和方法**

   - `resizeHeightProportionally(100, ResizeType.AdaptiveResample)`：此方法將高度調整為 100 像素，同時使用自適應重採樣保持縱橫比以確保品質。

## 實際應用

以下是一些可以應用這些功能的實際場景：

1. **醫學影像存檔**：轉換和調整 DICOM 影像的大小，以便在非醫療系統中更輕鬆地儲存。
2. **醫學影像的網頁展示**：使用 BMP 格式在網路應用程式上顯示醫學影像，在保持品質的同時減少檔案大小。
3. **跨平台相容性**：簡化可能不支援 DICOM 格式的不同軟體之間的影像共享。

## 性能考慮

使用 Aspose.Imaging for Java 時：

- **優化影像尺寸**：在轉換大型 DICOM 檔案之前，請考慮調整其大小以減少處理時間和記憶體使用量。
- **高效率的記憶體管理**：處理影像資料時利用try-with-resources有效管理記憶體。
- **批次處理**：如果處理多張影像，則分批自動化處理以提高效率。

## 結論

在本教程中，您學習如何使用 Aspose.Imaging for Java 載入 DICOM 映像並將其轉換為 BMP 格式。我們也學習如何在保持影像比例的情況下調整影像大小。掌握這些技能後，您可以更有效地將醫學影像解決方案整合到各種應用程式中。

**後續步驟：**

- 嘗試 Aspose.Imaging 提供的其他影像處理功能。
- 探索與其他系統（如醫療保健資料庫或網路平台）整合的可能性。

## 常見問題部分

1. **什麼是 Aspose.Imaging？**
   - Aspose.Imaging 是一個強大的 Java 映像處理庫，支援包括 DICOM 和 BMP 在內的多種格式。

2. **我可以在不購買許可證的情況下使用 Aspose.Imaging 嗎？**
   - 是的，您可以先免費試用，或取得臨時許可證來探索其功能。

3. **Aspose.Imaging 支援哪些圖像格式？**
   - 它支援多種格式，包括 JPEG、PNG、GIF、BMP 和 DICOM 等。

4. **如何使用 Aspose.Imaging 處理大型 DICOM 檔案？**
   - 考慮在處理之前調整圖像大小以有效管理記憶體使用。

5. **是否可以將該庫整合到現有的 Java 應用程式中？**
   - 是的，Aspose.Imaging 可以使用 Maven 或 Gradle 依賴項無縫整合到您目前的專案中。

## 資源

- [文件](https://reference.aspose.com/imaging/java/)
- [下載庫](https://releases.aspose.com/imaging/java/)
- [購買選項](https://purchase.aspose.com/buy)
- [免費試用](https://releases.aspose.com/imaging/java/)
- [臨時執照](https://purchase.aspose.com/temporary-license/)
- [支援論壇](https://forum.aspose.com/c/imaging/10)

按照本指南操作，您現在應該能夠使用 Aspose.Imaging for Java 處理 DICOM 映像了。祝您編碼愉快！

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}