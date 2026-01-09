---
date: 2026-01-09
description: 學習如何使用 Aspose.Imaging for Java 進行影像二值化。本指南涵蓋 DICOM 轉 BMP 的影像處理 Java 技術。
linktitle: Bradley's Adaptive Threshold Binarization
second_title: Aspose.Imaging Java Image Processing API
title: 如何使用 Aspose.Imaging for Java 進行圖像二值化
url: /zh-hant/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Imaging for Java 進行影像二值化

影像在數位世界中扮演關鍵角色，無論是網站、文件，或是各種應用程式的一部份。如果你在尋找 **如何有效地二值化影像**，尤其是醫學格式如 DICOM，這裡就是正確的地方。影像二值化透過將圖片轉換為黑白表示，簡化了後續分析、OCR 或儲存最佳化的工作。在本教學中，我們將使用 Aspose.Imaging for Java 的 Bradley 自適應閾值二值化，完整示範整個流程。

## 快速答覆
- **二值化的作用是什麼？** 依據閾值將每個像素轉換為黑或白。
- **哪個函式庫最適合 Java 影像處理？** Aspose.Imaging for Java 提供功能完整、可免費試用的版本。
- **可以直接處理 DICOM 檔案嗎？** 可以，Aspose.Imaging 能載入 DICOM 並輸出 BMP、PNG 等格式。
- **正式環境需要授權嗎？** 非試用用途需購買商業授權。
- **支援哪個 Java 版本？** 完全相容於 Java 8 及更新版本。

## 什麼是影像二值化？
影像二值化是將灰階或彩色影像轉換為二元影像的過程，每個像素的值僅為 0（黑）或 255（白）。此步驟常是醫學影像處理、文件掃描與電腦視覺工作流程的第一階段。

## 為什麼選擇 Aspose.Imaging for Java？
Aspose.Imaging 提供純 Java API，**可載入 DICOM**、套用如 **Bradley 自適應閾值** 等先進演算法，並將結果儲存為常見格式，無需外部原生函式庫。它非常適合 **醫學影像處理**、**將 DICOM 轉換為 BMP** 以及其他基於 Java 的工作流程。

## 前置需求

在開始撰寫程式碼之前，請先確保具備以下項目：

- **Java 開發環境** – 已安裝 JDK 8 或更新版本。
- **Aspose.Imaging for Java** – 從官方網站下載：[下載 Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/)。
- **DICOM 影像** – 任意你想要二值化的 DICOM 範例檔案。

準備工作完成後，我們即可進入實作階段。

## 如何二值化影像 – 步驟說明

### 匯入套件
首先匯入必要的 Aspose.Imaging 類別。此程式碼片段同時定義了輸入與輸出檔案路徑。

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// Load a DICOM image in an instance of DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Binarize image with Bradley's adaptive threshold.
    image.binarizeBradley(10);
    // Save the resultant image.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

### 步驟 1：定義路徑
設定來源 DICOM 檔案與目標 BMP 檔案的位置。將 `"Your Document Directory"` 替換為實際的資料夾路徑。

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

### 步驟 2：載入 DICOM 影像
使用 Aspose.Imaging **載入 dicom 影像** 為 `DicomImage` 物件。此物件讓你完整存取像素資料與處理方法。

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // The image processing steps will go here.
}
```

### 步驟 3：執行二值化
套用 Bradley 自適應閾值演算法。參數（本例為 `10`）控制閾值的靈敏度；你可以依需求調整不同數值以取得最佳效果。

```java
image.binarizeBradley(10);
```

### 步驟 4：儲存二值化後的影像
最後將處理完的影像匯出。此處使用 BMP 格式，Aspose.Imaging 亦支援 PNG、JPEG、TIFF 等多種格式。

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## 常見問題與除錯

- **FileNotFoundException** – 確認 `dataDir` 路徑以斜線結尾，且 DICOM 檔名完全相符。
- **OutOfMemoryError** – 大型 DICOM 檔案可能需要增加 JVM 堆積大小（例如 `-Xmx2g` 或更高）。
- **閾值不正確** – 若輸出過暗或過亮，請調整傳入 `binarizeBradley()` 的整數值（建議 5‑15 之間）。

## 常見問答

### Q1：什麼是 DICOM，為何在醫學影像中如此重要？
**A:** DICOM 代表 Digital Imaging and Communications in Medicine（醫學影像與通訊標準）。它是儲存、傳輸與處理醫學影像的通用標準，確保不同設備與系統之間的互通性。

### Q2：我可以在商業專案中使用 Aspose.Imaging for Java 嗎？
**A:** 可以，Aspose.Imaging for Java 同時提供免費試用與商業授權。你可以於 [Aspose 官方網站](https://purchase.aspose.com/buy) 探索方案並取得授權。

### Q3：是否提供暫時授權供測試使用？
**A:** 有的，你可以取得暫時授權以測試與評估 Aspose.Imaging for Java。詳情請參閱 [此連結](https://purchase.aspose.com/temporary-license/)。

### Q4：我可以到哪裡尋求協助或討論 Aspose.Imaging for Java 的相關問題？
**A:** 可前往 [Aspose.Imaging 論壇](https://forum.aspose.com/) 取得社群支援與討論，這裡聚集了許多使用者與開發者，能協助解決問題。

### Q5：Aspose.Imaging for Java 是否適用於其他 Java 應用程式的影像處理？
**A:** 絕對適用。此函式庫在 Web 應用、桌面軟體、批次處理工具等多種 Java 環境中皆表現穩定，提供跨平台一致的 API。

## 結論
現在你已掌握 **如何使用 Aspose.Imaging for Java 進行影像二值化**，並了解 Bradley 自適應閾值的應用。此技術對 **醫學影像處理** 尤其有價值，能將 DICOM 檔案轉換為輕量的 BMP（或其他）格式，以供分析或儲存。持續嘗試不同的閾值，並探索 Aspose.Imaging 更多強大功能。

欲深入了解影像操作，請參考官方文件：[Aspose.Imaging for Java 文件](https://reference.aspose.com/imaging/java/)。

---

**最後更新：** 2026-01-09  
**測試環境：** Aspose.Imaging for Java 24.12（撰寫時最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}