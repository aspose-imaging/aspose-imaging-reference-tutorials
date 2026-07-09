---
date: 2026-01-14
description: 學習如何在 Java 中使用 Aspose.Imaging 將 DICOM 轉換為 BMP 並調整其伽瑪。本指南展示了如何輕鬆處理 DICOM
  圖像。
linktitle: DICOM Image Gamma Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: 將 DICOM 轉換為 BMP – 使用 Aspose.Imaging for Java 進行伽瑪調整
url: /zh-hant/java/image-processing-and-enhancement/dicom-image-gamma-adjustment/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 將 DICOM 轉換為 BMP – 使用 Aspose.Imaging for Java 進行 Gamma 調整

如果您需要在微調圖像對比度的同時 **將 DICOM 轉換為 BMP**，您來對地方了。在本教學中，我們將逐步說明如何載入 DICOM 檔案、套用 gamma 校正，並使用 Aspose.Imaging for Java 將結果儲存為 BMP 圖像。完成後，您將了解 **如何以程式方式處理 DICOM** 檔案，並產生高品質的點陣圖輸出，以供後續醫學影像工作流程使用。

## 快速解答
- **「將 DICOM 轉換為 BMP」是什麼意思？** 它會將 DICOM 醫學影像轉換為標準 BMP 點陣圖，同時保留像素資料。  
- **哪個函式庫負責轉換？** Aspose.Imaging for Java 提供簡易的 API 來載入 DICOM 並儲存為 BMP。  
- **我需要授權嗎？** 免費試用版可用於開發；商業授權則需於正式環境使用。  
- **程式執行需要多久？** 在現代 CPU 上，對一般 512 × 512 DICOM 檔案執行時間少於一秒。  
- **我可以更改 gamma 值嗎？** 可以——將任意整數（例如 30‑70）傳遞給 `adjustGamma()` 以符合您的對比需求。

## 「將 DICOM 轉換為 BMP」是什麼？
將 DICOM 轉換為 BMP 意指解碼 DICOM 醫學影像格式，並將像素資料重新編碼為 BMP 點陣圖。BMP 被各種影像工具廣泛支援，適合用於目視檢查、報告或進一步處理。

## 為什麼在轉換時要調整 gamma？
Gamma 調整會改變影像的亮度曲線，提升細節的可見度，同時不改變底層資料。這在放射科尤為重要，因為對比度會影響診斷。

## 前置條件

### 1. Java 開發環境
- 已安裝 JDK 8 或更新版本，並在 IDE 或命令列中完成設定。

### 2. Aspose.Imaging for Java 函式庫
- 從 [download link](https://releases.aspose.com/imaging/java/) 下載函式庫。

### 3. 輸入 DICOM 影像
- 準備好 DICOM 檔案。測試用的範例檔案可於線上免費取得。

## 匯入套件
首先，匯入您需要的類別。以下程式碼區塊必須保持原樣：

```java
import com.aspose.imaging.fileformats.dicom.DicomImage;
import com.aspose.imaging.image.Image;
import com.aspose.imaging.imageoptions.BmpOptions;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
```

## 將 DICOM 轉換為 BMP – 步驟說明

### 步驟 1：設定檔案路徑
指定來源 DICOM 檔案的位置以及 BMP 輸出的路徑。

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = dataDir + "AdjustingGamma.bmp";
```

### 步驟 2：載入 DICOM 影像
開啟檔案串流並建立 `DicomImage` 實例。

```java
File file = new File(inputFile);

try (FileInputStream fis = new FileInputStream(file)) {
    // Load a DICOM image in an instance of DicomImage
    try (DicomImage image = (DicomImage) Image.load(fis)) {
```

### 步驟 3：調整 Gamma
在儲存之前套用所需的 gamma 校正（例如 50）。

```java
        // Adjust the gamma
        image.adjustGamma(50);
```

### 步驟 4：儲存產生的 BMP
建立 BMP 選項並將處理後的影像寫入磁碟。catch 區塊會處理任何 I/O 問題。

```java
        // Create an instance of BmpOptions for the resultant image and save the resultant image
        image.save(outputFile, new BmpOptions());
    }
} catch (IOException ex) {
    // Handle any potential exceptions
    com.aspose.imaging.examples.Logger.println(ex.getMessage());
    ex.printStackTrace();
}
```

以上即為在調整 gamma 時 **將 DICOM 轉換為 BMP** 的完整工作流程。

## 常見問題與解決方案
- **不支援的 DICOM 標籤** – 確認 DICOM 檔案包含像素資料；加密或壓縮的串流可能需要額外解碼。  
- **記憶體不足錯誤** – 對於非常大的影像，請增加 JVM 堆積大小（`-Xmx2g`）或以分塊方式處理影像。  
- **gamma 值不正確** – 小於 0 或大於 100 的值可能產生意外結果；請維持在 0‑100 範圍內。

## 常見問答

**Q: 什麼是 DICOM 影像？**  
A: DICOM（Digital Imaging and Communications in Medicine）是用於儲存與傳輸醫學影像（如 X 光、CT 掃描與 MRI）的通用格式。

**Q: 為什麼對 DICOM 影像進行 gamma 調整很重要？**  
A: Gamma 調整提升視覺對比度，使在分析時更容易看清解剖結構。

**Q: 我可以用其他程式語言處理 DICOM 影像嗎？**  
A: 可以——Aspose.Imaging 提供 .NET、Java 以及其他平台的函式庫，支援跨語言開發。

**Q: 處理 DICOM 檔案有什麼限制嗎？**  
A: 某些 DICOM 檔案包含大量中繼資料或專有壓縮；了解 DICOM 標準有助於避免陷阱。

**Q: 我可以在哪裡找到更多 Aspose.Imaging 教學？**  
A: 前往 [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/) 瀏覽更多指南、API 參考與範例專案。

## 結論
透過本指南，您現在已了解 **如何處理 DICOM** 檔案、套用 gamma 校正，並使用 Aspose.Imaging for Java **將 DICOM 轉換為 BMP**。此功能可簡化醫學影像工作流程，讓您能產生點陣圖以供報告、AI 分析或存檔使用。

如果您遇到任何挑戰，請前往 [Aspose.Imaging forum](https://forum.aspose.com/) 社群，這裡是提問與分享見解的好地方。

---

**最後更新：** 2026-01-14  
**測試環境：** Aspose.Imaging for Java 24.11 (latest at time of writing)  
**作者：** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
