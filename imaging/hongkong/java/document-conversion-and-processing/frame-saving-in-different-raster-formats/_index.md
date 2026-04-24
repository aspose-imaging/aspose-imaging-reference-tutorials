---
date: 2025-12-20
description: 學習如何使用 Aspose.Imaging for Java 將 TIFF 轉換為 PNG，並將圖像儲存為 PNG、BMP 或 GIF。一步一步的圖像處理指南。
linktitle: Frame Saving in Different Raster Formats
second_title: Aspose.Imaging Java Image Processing API
title: 如何將 TIFF 轉換為 PNG 並以不同光柵格式儲存影格
url: /zh-hant/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 將 TIFF 轉換為 PNG 並以不同點陣格式儲存影格

在文件密集的應用程式中，處理多頁 TIFF 檔案是常見情境。若您需要 **convert tiff to png**——或是擷取單一影格並儲存為其他點陣格式——Aspose.Imaging for Java 可讓此流程變得簡單且高效。本教學將逐步說明如何載入 TIFF、遍歷其影格，並將每一影格儲存為 PNG（之後也可輕鬆切換為 BMP 或 GIF）。

## 快速解答
- **「convert tiff to png」是什麼意思？** 即將 TIFF 檔案的每一頁提取出來，寫入為 PNG 點陣圖像。  
- **哪個函式庫負責此功能？** Aspose.Imaging for Java 完整支援 TIFF 影格提取與點陣格式轉換。  
- **需要授權嗎？** 開發階段可使用免費試用版；正式上線則需購買完整授權。  
- **可以改存為 BMP 或 GIF 而不是 PNG 嗎？** 可以——只要將 `PngOptions` 換成 `BmpOptions` 或 `GifOptions` 即可。  
- **需要哪個 Java 版本？** 建議使用 Java 8 或以上。

## 什麼是「convert tiff to png」？
將 TIFF 轉換為 PNG 需要解碼多頁 TIFF、存取每個影格，並將該影格編碼為 PNG 格式。PNG 為無損、適合網路使用且廣受支援的影像格式。

## 為什麼選擇 Aspose.Imaging for Java？
- **廣泛的格式支援** – 支援 TIFF、PNG、JPEG、BMP、GIF 等多種格式。  
- **無原生相依** – 完全純 Java，可輕鬆整合至任何 JVM 專案。  
- **高效能** – 為大型影像與多頁文件進行最佳化。  
- **簡易 API** – 只需少量程式碼即可完成複雜的轉換工作。

## 前置條件

1. **Java 開發環境** – 確認已安裝 JDK。若尚未安裝，可從 [Oracle website](https://www.oracle.com/java/technologies/javase-downloads) 下載。  
2. **Aspose.Imaging for Java 函式庫** – 參考 API 文件於 [documentation](https://reference.aspose.com/imaging/java/)。可從 [download page](https://releases.aspose.com/imaging/java/) 取得函式庫。免費試用版請點擊 [here](https://releases.aspose.com/)，完整授權可於 [here](https://purchase.aspose.com/buy) 購買。  
3. **範例 TIFF 影像** – 準備好一個多頁 TIFF 供處理。

完成上述前置作業後，讓我們進入程式碼示範。

## 如何使用 Aspose.Imaging for Java 將 TIFF 轉換為 PNG

### 匯入套件
首先，匯入所需的 Aspose.Imaging 類別。

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

### 步驟 1：載入 TIFF 影像
設定資料目錄並載入來源 TIFF 檔案。

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

### 步驟 2：以不同點陣格式儲存影格
遍歷每個影格並 **save image as png**。若要 **convert tiff to bmp** 或執行 **tiff to gif conversion**，只需將 `PngOptions` 換成 `BmpOptions` 或 `GifOptions`。

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **專業提示：** 請保留如範例所示的 `try‑with‑resources` 區塊，以確保 TIFF 檔案在處理完畢後能正確釋放資源。

## 常見使用情境
- **文件封存：** 將掃描的 TIFF 文件轉換為 PNG，以供網頁預覽。  
- **縮圖產生：** 擷取 TIFF 的第一頁並存為小尺寸 PNG 縮圖。  
- **格式遷移：** 將舊有的 TIFF 資產搬移至 BMP 或 GIF 等現代格式，以相容較舊的系統。

## 疑難排解與技巧
- **影格遺失：** 確認來源 TIFF 確實包含多頁；可使用 `multiImage.getFrames().size()` 進行除錯。  
- **記憶體不足：** 如範例所示，逐頁處理大型 TIFF，而非一次載入整個檔案。  
- **品質控制：** PNG 為無損格式；若需要較小的檔案，可考慮使用 JPEG 並設定品質參數。

## 常見問答

**Q1: Aspose.Imaging for Java 支援哪些點陣格式可用於影格儲存？**  
A1: 支援多種點陣格式，包括 PNG、JPEG、BMP、GIF 等，您可依需求選擇最適合的格式。

**Q2: 我可以使用 Aspose.Imaging for Java 執行其他影像操作嗎？**  
A2: 可以，Aspose.Imaging for Java 提供完整的影像處理功能，包含調整大小、裁切、套用各種濾鏡與特效，是您所有影像需求的多功能工具。

**Q3: 我要如何取得 Aspose.Imaging for Java 的完整授權？**  
A: 前往 [purchase page](https://purchase.aspose.com/buy) 購買授權，網站上提供多種授權方案以符合您的專案需求。

**Q4: Aspose.Imaging for Java 有提供免費試用嗎？**  
A: 有，您可從 [releases page](https://releases.aspose.com/) 下載免費試用版，先行體驗函式庫功能再決定是否購買。

**Q5: 若需要支援或協助，該向哪裡尋求？**  
A: 您可前往 [Aspose Imaging forum](https://forum.aspose.com/) 尋求社群與官方支援團隊的協助。

---

**Last Updated:** 2025-12-20  
**Tested With:** Aspose.Imaging for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}