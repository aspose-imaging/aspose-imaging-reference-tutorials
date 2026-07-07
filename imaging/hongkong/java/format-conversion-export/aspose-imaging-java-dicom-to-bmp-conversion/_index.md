---
date: '2026-03-28'
description: 學習如何使用 Aspose Imaging Java 將 DICOM 轉換為 BMP 並儲存圖像為 BMP，適用於醫療影像轉換與網頁顯示。
keywords:
- convert DICOM to BMP
- Aspose.Imaging Java
- resize DICOM image
- medical image conversion with Aspose
- format conversion & export
title: Aspose Imaging Java：將 DICOM 轉換為 BMP – 完整指南
url: /zh-hant/java/format-conversion-export/aspose-imaging-java-dicom-to-bmp-conversion/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 如何使用 Aspose.Imaging Java 載入並重新儲存 DICOM 影像為 BMP

## 介紹

在數位影像領域，管理醫療影像至關重要，而 **aspose imaging java** 讓工作變得更簡單。無論您需要歸檔 DICOM 檔案、在 Web 入口網站上顯示，或整合到醫療工作流程中，將 DICOM 轉換為 BMP 並保留品質是常見需求。在本教學中，您將學會如何載入 DICOM 影像、轉換為 BMP，並按比例調整高度——全部使用乾淨、可投入生產的 Java 程式碼。

**您將學到**

- 如何使用 **aspose imaging java** 將 DICOM 影像轉換為 BMP  
- 調整 DICOM 影像尺寸同時保持比例的技巧  
- 在開發環境中設定 Aspose.Imaging for Java 的方法  

在深入實作之前，先確保已滿足前置條件。

## 快速答覆
- **需要哪個函式庫？** Aspose.Imaging for Java (aspose imaging java)  
- **可以一行程式碼完成 DICOM 轉 BMP 嗎？** 不行，必須先載入影像，再儲存。  
- **生產環境需要授權嗎？** 需要，有效的 Aspose.Imaging 授權是必須的。  
- **調整尺寸是可選的嗎？** 可以，若只需要格式轉換，可跳過調整尺寸步驟。  
- **可以批次處理大量檔案嗎？** 當然可以──將相同程式碼包在迴圈或使用 Java streams。

## Aspose Imaging Java 是什麼？
Aspose.Imaging Java 是一套功能強大、跨平台的函式庫，讓您能讀取、編輯與寫入超過 100 種影像格式，包含醫療等級的 DICOM 格式。它抽象化了影像處理的底層細節，讓您專注於業務邏輯，而非像素操作。

## 為何在醫療影像轉換中使用 Aspose Imaging Java？
- **完整的 DICOM 支援** ─ 讀取像素資料、metadata 與多影格檔案，無需額外外掛。  
- **高品質 BMP 輸出** ─ 無損 BMP 檔保留診斷細節。  
- **內建調整尺寸** ─ 以自適應重新取樣保持長寬比，產出清晰結果。  
- **執行緒安全且記憶體效率高** ─ 適合伺服器端批次工作。

## 前置條件

- **Aspose.Imaging 函式庫**：版本 25.5 或更新（建議使用最新版本）。  
- **Java Development Kit (JDK)**：版本 8 以上。  
- **IDE**：IntelliJ IDEA、Eclipse，或您慣用的任何編輯器。  

## 設定 Aspose.Imaging for Java

首先，使用 Maven 或 Gradle 將函式庫加入專案。

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

或者，直接從 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下載函式庫。

### 取得授權

要開始使用 Aspose.Imaging，您可以：

- **免費試用** ─ 使用限時授權測試完整功能。  
- **臨時授權** ─ 取得短期專案的臨時金鑰。  
- **購買授權** ─ 為正式上線購買永久授權。

取得授權檔後，於應用程式啟動時載入：

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.License;

License license = new License();
license.setLicense("Aspose.Imaging.Java.lic");
```

## 實作指南

我們將示範兩個實務情境：

1. **載入 DICOM 檔案並儲存為 BMP**（核心的「save image bmp」操作）。  
2. **在儲存前按比例調整影像高度**，適用於網頁縮圖。

### 載入並重新儲存 DICOM 影像為 BMP

#### 概觀
此程式碼片段示範讀取 DICOM 檔案並寫出為 BMP 檔的最小步驟。

#### 步驟說明

1. **定義輸入與輸出路徑** ─ 請依您的環境調整。  
2. **使用 `DicomImage` 載入 DICOM 影像**。  
3. **以預設 `BmpOptions` 儲存為 BMP**。

```java
String dataDir = "YOUR_DOCUMENT_DIRECTORY";
String inputFile = dataDir + "image.dcm";
String outputFile = "YOUR_OUTPUT_DIRECTORY" + "ResizedOutput.bmp";

try (DicomImage image = (DicomImage) Image.load(inputFile)) {
    // Save the image as a BMP file.
    image.save(outputFile, new BmpOptions());
}
```

**關鍵參數**

- `inputFile`：來源 DICOM 檔的完整路徑。  
- `outputFile`：目標 BMP 檔的路徑。  
- `BmpOptions()`：使用預設 BMP 設定；如需自訂壓縮或像素格式，可自行調整。

### 按比例調整高度

#### 概觀
有時需要較小的影像以加快網頁載入速度。以下程式碼將高度調整為 100 像素，同時保持長寬比。

#### 步驟說明

```java
String inputFile = dataDir + "image.dcm";
String outputFile = "YOUR_OUTPUT_DIRECTORY" + "ResizeHeightProportionally_out.bmp";

try (DicomImage image = (DicomImage) Image.load(inputFile)) {
    // Resize the height proportionally to 100 pixels.
    image.resizeHeightProportionally(100, ResizeType.AdaptiveResample);
    
    // Save the resized image in BMP format.
    image.save(outputFile, new BmpOptions());
}
```

**重要細節**

- `resizeHeightProportionally(100, ResizeType.AdaptiveResample)` ─ 第一個參數為目標高度（像素），第二個參數指示 Aspose.Imaging 使用高品質自適應重新取樣。  
- 此方法會自動計算新寬度，確保影像不會被拉伸。

## 實務應用

以下列出幾個真實情境，說明這些程式碼的價值：

| 使用情境 | 好處 |
|----------|------|
| **醫療影像歸檔** | 將 DICOM 轉為 BMP 後可存放於一般檔案系統，降低供應商鎖定風險。 |
| **放射影像於 Web 顯示** | BMP 被瀏覽器與 UI 框架廣泛支援，方便在門戶網站嵌入掃描圖。 |
| **跨平台資料交換** | BMP 為簡易光柵格式，幾乎所有影像工具皆能讀取，促進協作。 |
| **批次處理管線** | 將程式碼包在迴圈或 Java Stream 中，可自動轉換數百檔案。 |

## 效能考量

- **先調整尺寸再轉檔**：提前縮小尺寸可減少記憶體使用並加速儲存。  
- **使用 try‑with‑resources**（如範例所示）確保影像即時釋放，防止記憶體洩漏。  
- **批次模式**：大量檔案時，可使用 `ExecutorService` 平行處理，但需監控 JVM heap 大小。

## 常見問題與解決方案

| 症狀 | 可能原因 | 解決方式 |
|------|----------|----------|
| `Unsupported format` 錯誤 | 使用不支援 DICOM 的舊版 Aspose.Imaging | 升級至最新版本（≥ 25.5）。 |
| 大型 DICOM 檔案發生 Out‑of‑memory | 影像未正確釋放或過大無法放入 heap | 增加 JVM heap (`-Xmx2g`) 並使用 `try (DicomImage …)` 模式。 |
| BMP 輸出全黑或空白 | DICOM 檔僅含 metadata，無像素資料 | 確認來源 DICOM 含有影像幀，可使用 `image.getFramesCount()` 檢查。 |
| 調整後影像模糊 | 使用低品質的 resize type | 改用 `ResizeType.AdaptiveResample`（如範例）或 `ResizeType.HighQualityBicubic`。 |

## 常見問答

**Q: `save image bmp` 與 `save image png` 有何差異？**  
A: BMP 為未壓縮、無損格式，保留每個像素；PNG 則使用無損壓縮以減少檔案大小。需要絕對像素忠實度時請使用 BMP。

**Q: 能否一次執行多個 DICOM 檔案的轉換？**  
A: 可以，只要遍歷 `.dcm` 目錄，將相同的載入‑儲存邏輯放入迴圈即可。

**Q: aspose imaging java 是否支援多影格 DICOM 系列？**  
A: 完全支援──可透過 `image.getFrames()` 取得每個幀，單獨或合併儲存為 BMP。

**Q: 開發階段需要授權嗎？**  
A: 評估可使用免費試用或臨時授權，但正式上線必須購買授權。

**Q: 轉檔後如何處理 DICOM metadata（如患者姓名、研究 ID）？**  
A: Aspose.Imaging 可透過 `image.getMetaData()` 讀取 DICOM 標籤，您可將資訊寫入 BMP metadata 或另存至資料庫。

## 結論

現在您已掌握使用 **aspose imaging java** 載入 DICOM 影像、轉換為 BMP，並按比例調整高度的完整解決方案。這些基礎可組合成批次工作、整合至 Web 服務，或用於桌面工具，提升醫療影像工作流程的效率。

**後續建議**

- 嘗試其他 `ResizeType` 以取得不同的品質‑速度平衡。  
- 探索 Aspose.Imaging 的其他功能，如加入浮水印、轉換為 PNG/JPEG，或操作 metadata。  
- 將程式碼整合至既有的醫療應用或微服務中。

## 資源

- [Documentation](https://reference.aspose.com/imaging/java/)
- [Download Library](https://releases.aspose.com/imaging/java/)
- [Purchase Options](https://purchase.aspose.com/buy)
- [Free Trial](https://releases.aspose.com/imaging/java/)
- [Temporary License](https://purchase.aspose.com/temporary-license/)
- [Support Forum](https://forum.aspose.com/c/imaging/14)

---

**最後更新：** 2026-03-28  
**測試環境：** Aspose.Imaging 25.5 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}