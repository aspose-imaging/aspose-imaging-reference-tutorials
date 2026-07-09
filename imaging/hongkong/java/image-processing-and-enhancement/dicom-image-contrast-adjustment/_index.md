---
date: 2026-01-12
description: 學習如何在 DICOM 圖像中調整對比度——使用 Aspose.Imaging for Java 進行對比度調整的逐步指南，並將 DICOM
  轉換為 BMP。
linktitle: DICOM Image Contrast Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: 如何使用 Aspose.Imaging for Java 調整 DICOM 圖像的對比度
url: /zh-hant/java/image-processing-and-enhancement/dicom-image-contrast-adjustment/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Imaging for Java 調整 DICOM 影像的對比度

## 快速解答
- **對比度調整的作用是什麼？** 它會擴大暗部與亮部像素之間的範圍，使結構更突出。  
- **需要哪個函式庫？** Aspose.Imaging for Java。  
- **可以輸出為 BMP 嗎？** 可以 – 調整對比度後即可將 DICOM 轉換為 BMP。  
- **生產環境需要授權嗎？** 非評估用途必須購買商業授權。  
- **支援哪個 Java 版本？** Java 8 及更新版本。

## 什麼是對比度調整以及為何重要？

對比度調整可提升解剖特徵之間的視覺差異，協助放射科醫師更快速發現異常。在 DICOM 工作流程中，於轉換前先調整對比度，可確保 BMP 輸出保有報告或存檔所需的診斷品質。

## 先決條件

在深入程式碼之前，請確認您已具備以下項目：

1. **Aspose.Imaging for Java** – 從官方網站下載 [此處](https://releases.aspose.com/imaging/java/)。  
2. **Java 開發環境** – JDK 8 以上以及您喜愛的 IDE（IntelliJ、Eclipse、VS Code 等）。  
3. **DICOM 影像** – 任意您想要增強的 .dcm 檔案；範例檔案可於線上取得，或使用您自己的臨床資料。

## 匯入套件

以下匯入可讓您使用 DICOM 處理與 BMP 儲存功能。

```java
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
```

## 如何調整 DICOM 影像的對比度

以下為完整的逐步工作流程。每一步皆以簡明語言說明，即使您是 Aspose.Imaging 新手也能輕鬆跟隨。

### 步驟 1：指定檔案路徑

設定輸入 DICOM 的位置與欲輸出的 BMP 路徑。請將佔位符替換為您機器上的實際目錄。

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingContrast_out.bmp";
```

### 步驟 2：載入 DICOM 影像

我們使用 `FileInputStream` 開啟 DICOM 檔案。`try‑with‑resources` 區塊可確保串流自動關閉。

```java
File file = new File(inputFile);

try (FileInputStream fis = new FileInputStream(file)) {
    try (DicomImage image = (DicomImage) Image.load(fis)) {
        // All further processing happens inside this block
    }
} catch (IOException ex) {
    Logger.println(ex.getMessage());
    ex.printStackTrace();
}
```

### 步驟 3：調整對比度

在內層 `try` 區塊中呼叫 `adjustContrast`。數值範圍為 **‑100**（降低）至 **+100**（提升）。本例中我們將對比度提升 50 單位。

```java
image.adjustContrast(50);
```

### 步驟 4：將 DICOM 轉換為 BMP 並儲存影像

調整完對比度後，我們建立 `BmpOptions` 實例，並將結果儲存為 BMP 檔案。此步驟 **將 DICOM 轉換為 BMP**，提供廣受支援的點陣圖格式。

```java
image.save(outputFile, new BmpOptions());
```

## 常見問題與技巧

- **無效的 DICOM 檔案** – 確認 .dcm 檔案未使用不支援的傳輸語法壓縮。Aspose.Imaging 支援大多數標準 DICOM 編碼。  
- **對比度數值超出範圍** – 超過 ±100 的數值會被限制；請選擇適合影像直方圖的數值。  
- **記憶體使用量** – 大型 DICOM 序列可能佔用大量記憶體。若遇到 `OutOfMemoryError`，請一次處理單一切片。

## 結論

您現在已學會使用 Aspose.Imaging for Java **調整 DICOM 影像的對比度**，以及 **將 DICOM 轉換為 BMP** 以供後續使用。此工作流程快速且可靠，能整合至更大的醫學影像管線，無論是建置 PACS 檢視器、研究工具，或自動化報告系統。

Aspose.Imaging for Java 抽象化低階 DICOM 處理，讓您專注於影像的臨床價值。

## 常見問答

**Q: 什麼是 DICOM，為何它是醫學影像的標準？**  
A: DICOM（Digital Imaging and Communications in Medicine）是用於儲存、傳輸與分享醫學影像的通用格式，確保不同設備與機構之間的互通性。

**Q: 我可以同時調整亮度與對比度嗎？**  
A: 可以，`adjustBrightness(int value)` 方法的使用方式相同，且可在儲存前串接使用。

**Q: Aspose.Imaging 除了 BMP 外還支援其他輸出格式嗎？**  
A: 當然可以 – 只要使用相對應的 `*Options` 類別，即可匯出為 PNG、JPEG、TIFF 等多種格式。

**Q: 生產環境是否需要商業授權？**  
A: 需要。您可於 [此處](https://purchase.aspose.com/buy) 購買授權，或在 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時評估授權。

**Q: 我可以在哪裡找到更多協助與範例？**  
A: Aspose.Imaging for Java 社群論壇提供豐富的文件與範例程式碼：[Aspose.Imaging for Java 論壇](https://forum.aspose.com/)。

---

**最後更新：** 2026-01-12  
**測試版本：** Aspose.Imaging for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}