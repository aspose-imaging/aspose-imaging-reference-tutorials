---
date: 2026-04-28
description: 學習如何使用 Aspose.Imaging for Java 將 TIFF 轉換為 PNG，以及將 TIFF 轉換為其他點陣圖格式。一步步的影像處理指南。
keywords:
- tiff to png java
- how to convert tiff
- Aspose.Imaging Java
linktitle: 不同光柵格式的畫格儲存
second_title: Aspose.Imaging Java Image Processing API
title: tiff 轉 png java – 將 TIFF 轉換為 PNG 並將影格儲存於不同的點陣格式
url: /zh-hant/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# tiff to png java – 將 TIFF 轉換為 PNG 並將幀儲存為不同的光柵格式

在文件密集的應用程式中，處理多頁 TIFF 檔案是常見的情況。 如果您需要 **convert tiff to png**——或提取單獨的幀並將其存儲為其他光柵格式——Aspose.Imaging for Java 讓此過程簡單且高效。 在本教學中，我們將逐步說明載入 TIFF、遍歷其幀，並將每個幀儲存為 PNG 的具體步驟（您可以輕鬆切換為 BMP 或 GIF）。 最後，您還將看到如何 **how to convert tiff** 只需幾行程式碼即可轉換為任何受支援的光柵格式。

## 快速解答
- **What does “convert tiff to png” mean?** 它表示將 TIFF 檔案的每一頁提取出來，並寫入為 PNG 光柵圖像。  
- **Which library handles this?** Aspose.Imaging for Java 提供對 TIFF 幀提取和光柵格式轉換的完整支援。  
- **Do I need a license?** 免費試用可用於開發；正式使用則需完整授權。  
- **Can I save to BMP or GIF instead of PNG?** 是的——只需將 `PngOptions` 換成 `BmpOptions` 或 `GifOptions`。  
- **What Java version is required?** 建議使用 Java 8 或更高版本。

## 「convert tiff to png」是什麼？
將 TIFF 轉換為 PNG 包括解碼多頁 TIFF、存取每個幀，並將該幀編碼為 PNG 格式，該格式無失真、適合網路使用且廣受支援。

## 為什麼使用 Aspose.Imaging for Java？
- **Broad format support** – 支援 TIFF、PNG、JPEG、BMP、GIF 等多種格式。  
- **No native dependencies** – 純 Java，易於整合至任何 JVM 專案。  
- **High performance** – 為大型影像與多頁文件進行最佳化。  
- **Simple API** – 只需少量程式碼即可執行複雜的轉換。

## 為什麼這很重要
許多舊有系統將掃描文件儲存為多頁 TIFF，因為此格式適合存檔。然而，現代的網頁與行動應用程式更偏好 PNG、BMP 或 GIF，以便快速渲染與縮圖產生。即時轉換 TIFF 幀可降低儲存成本、提升載入速度，並擴大在瀏覽器與裝置間的相容性。

## 前置條件

1. **Java Development Environment** – 確保已安裝 JDK。若尚未安裝，請從 [Oracle website](https://www.oracle.com/java/technologies/javase-downloads) 下載。  
2. **Aspose.Imaging for Java Library** – 可於 [documentation](https://reference.aspose.com/imaging/java/) 取得 API 參考。從 [download page](https://releases.aspose.com/imaging/java/) 下載程式庫。免費試用可在 [here](https://releases.aspose.com/) 取得，完整授權可於 [here](https://purchase.aspose.com/buy) 購買。  
3. **Sample TIFF Image** – 準備好一個多頁 TIFF 供處理。

現在已完成前置條件，讓我們深入程式碼。

## 使用 Aspose.Imaging for Java 轉換 TIFF 為 PNG 的方法

### 匯入套件
首先，匯入所需的 Aspose.Imaging 類別。

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

### 步驟 1：載入 TIFF 圖像
初始化資料目錄並載入來源 TIFF 檔案。

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

### 步驟 2：以不同光柵格式儲存幀
遍歷每個幀並 **save image as png**。若要 **convert tiff to bmp** 或執行 **tiff to gif conversion**，只需將 `PngOptions` 換成 `BmpOptions` 或 `GifOptions`。

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **Pro tip:** 保持如示範的 `try‑with‑resources` 區塊，以確保在處理完畢後正確釋放 TIFF 檔案。

## 常見使用情境
- **Document archiving:** 將掃描的 TIFF 文件轉換為 PNG，以供網頁預覽。  
- **Thumbnail generation:** 提取 TIFF 的第一幀，並儲存為小尺寸 PNG 縮圖。  
- **Format migration:** 將舊有的 TIFF 資產遷移至 BMP 或 GIF 等現代格式，以提升與舊系統的相容性。

## 疑難排解與技巧
- **Missing frames:** 確認來源 TIFF 確實包含多頁；可使用 `multiImage.getFrames().size()` 進行除錯。  
- **Out‑of‑memory errors:** 如示範般逐頁處理大型 TIFF，而非一次載入整個檔案，以避免記憶體不足。  
- **Quality control:** PNG 為無失真格式；若需較小檔案，可考慮使用具品質設定的 JPEG 選項。

## 常見問題

**Q1: What are the supported raster formats for frame saving in Aspose.Imaging for Java?**  
A1: Aspose.Imaging for Java 支援多種光柵格式，包括 PNG、JPEG、BMP、GIF 等。您可以選擇最符合應用需求的格式。

**Q2: Can I perform other image operations using Aspose.Imaging for Java?**  
A2: 是的，Aspose.Imaging for Java 提供完整的影像處理功能，包括調整大小、裁切以及套用各種濾鏡與特效。它是滿足所有影像處理需求的多功能工具。

**Q3: How can I obtain a full license for Aspose.Imaging for Java?**  
A: 若要購買 Aspose.Imaging for Java 的完整授權，請前往 [purchase page](https://purchase.aspose.com/buy)。您將找到符合專案需求的各種授權方案。

**Q4: Is there a free trial available for Aspose.Imaging for Java?**  
A: 是的，您可從 [releases page](https://releases.aspose.com/) 取得 Aspose.Imaging for Java 的免費試用。此試用版讓您在購買前先行體驗程式庫功能。

**Q5: Where can I seek support or get assistance with Aspose.Imaging for Java?**  
A: 若有任何問題、疑慮或需要協助，請前往 [Aspose Imaging forum](https://forum.aspose.com/)。社群與支援團隊將提供協助。

---

**最後更新：** 2026-04-28  
**測試環境：** Aspose.Imaging for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}