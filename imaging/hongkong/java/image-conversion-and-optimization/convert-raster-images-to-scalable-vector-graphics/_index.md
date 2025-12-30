---
date: 2025-12-30
description: 學習如何使用 Aspose.Imaging for Java 將光柵圖像轉換為 SVG，將圖像儲存為 SVG 並保留圖像品質。
linktitle: Convert Raster Images to Scalable Vector Graphics
second_title: Aspose.Imaging Java Image Processing API
title: 使用 Aspose.Imaging for Java 將光柵圖轉換為 SVG
url: /zh-hant/java/image-conversion-and-optimization/convert-raster-images-to-scalable-vector-graphics/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Imaging for Java 將點陣圖轉換為 SVG

如果您需要在 Java 環境中快速且可靠地 **convert raster to svg**，您來對地方了。在本教學中，我們將完整說明整個流程——從設定專案、載入點陣圖檔案，到最終將每張圖片儲存為 SVG 向量。完成後，您將能夠 **save image as svg**，同時保留原始品質，讓圖形在任何螢幕尺寸或列印解析度下皆可無損放大。

## 快速解答
- **「convert raster to svg」是什麼意思？** 它會將以像素為基礎的圖片（PNG、JPEG、GIF 等）轉換為基於 XML 的向量圖形，縮放時不會失去細節。  
- **哪個函式庫負責轉換？** Aspose.Imaging for Java 提供簡易的 API 進行點陣圖到向量圖的轉換。  
- **需要授權嗎？** 開發階段可使用試用版；正式上線需購買商業授權。  
- **可以批次處理多個檔案嗎？** 可以——只要如程式碼範例所示，對檔名陣列進行迴圈即可。  
- **需要哪個 Java 版本？** 完全支援 Java 8 以上版本。

## 「convert raster to svg」是什麼？
點陣圖會為每個像素儲存顏色資訊，限制了可擴展性。將它們轉換為 SVG 後，即可得到與解析度無關的表示方式，非常適合需要在任何尺寸下保持銳利的商標、圖示與插圖。

## 為什麼選擇 Aspose.Imaging for Java？
- **高保真度** – 轉換過程中保留顏色深度與細節。  
- **批次處理** – 只要簡單的迴圈，即可在數秒內處理數十個檔案。  
- **跨平台** – 在支援 Java 的任何作業系統上皆可執行。  
- **廣泛的格式支援** – 支援 GIF、JPEG、PNG、TIFF、WebP 等多種格式。

## 前置作業

在開始進行圖像轉換之前，請先確保具備以下條件：

- Java 開發環境：確保已在系統上安裝 Java Development Kit (JDK)。  
- Aspose.Imaging for Java：下載並安裝 Aspose.Imaging for Java。您可以在[此處](https://releases.aspose.com/imaging/java/)取得下載連結。  
- 範例點陣圖：將欲轉換為 SVG 的點陣圖收集起來，並放置於同一目錄中。

## 匯入套件

要開始圖像轉換流程，必須先匯入所需的套件。以下示範如何操作：

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.SvgOptions;
import com.aspose.imaging.imageoptions.SvgRasterizationOptions;
```

現在您已具備前置作業與套件，接下來將把轉換流程拆解為多個步驟說明。

## 如何使用 Aspose.Imaging 進行 raster to svg 轉換

### 步驟 1：初始化資料目錄

請先定義存放範例圖片的目錄路徑。將 `"Your Document Directory"` 替換為實際的圖片路徑：

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

### 步驟 2：定義圖片路徑

建立一個圖片路徑陣列，列出所有要轉換的點陣圖檔名：

```java
String[] paths = new String[]
    {
        "butterfly.gif",
        "33715-cmyk.jpeg",
        "3.JPG",
        "test.j2k",
        "Rings.png",
        "img4.TIF",
        "Lossy5.webp"
    };
```

### 步驟 3：執行轉換 – 儲存為 SVG

接著，對每個圖片路徑進行迴圈，將點陣圖轉換為 SVG。以下程式碼片段示範此過程：

```java
for (String path : paths)
{
    String destPath = "Your Document Directory" + path + ".svg";
    Image image = Image.load(dataDir + path);
    try
    {
        SvgOptions svgOptions = new SvgOptions();
        SvgRasterizationOptions svgRasterizationOptions = new SvgRasterizationOptions();
        svgRasterizationOptions.setPageWidth(image.getWidth());
        svgRasterizationOptions.setPageHeight(image.getHeight());
        svgOptions.setVectorRasterizationOptions(svgRasterizationOptions);
        image.save(destPath, svgOptions);
    }
    finally
    {
        image.dispose();
    }
}
```

重複上述程式碼，即可對 `paths` 陣列中的每張圖片執行轉換。完成後，您將成功 **convert raster images to SVG**，使用 Aspose.Imaging for Java 完成。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **Output SVG is blank** | `destPath` 錯誤或缺少寫入權限 | 確認目標資料夾已存在且具備寫入權限 |
| **Distorted dimensions** | `setPageWidth/Height` 未與來源圖片尺寸相符 | 如範例所示，使用 `image.getWidth()` 與 `image.getHeight()` |
| **Out‑of‑memory errors** | 處理極大點陣圖檔案時未釋放資源 | 確保在 `finally` 區塊中呼叫 `image.dispose()`（範例已包含） |

## 常見問答

**Q: 為什麼要將點陣圖轉換為 SVG？**  
A: 轉換為 SVG 後可在不同尺寸下保持品質不變，特別適用於需要在各種大小下仍保持銳利的商標、圖示與插圖。

**Q: 可以一次批次轉換多張圖片嗎？**  
A: 可以，您只需使用迴圈或自動化腳本，像本教學中示範的方式一次批次轉換多張圖片為 SVG。

**Q: Aspose.Imaging for Java 可以免費使用嗎？**  
A: Aspose.Imaging for Java 為商業函式庫，使用時需購買授權。您可在[此處](https://purchase.aspose.com/buy)取得授權與價格資訊。

**Q: 在哪裡可以取得 Aspose.Imaging for Java 的支援？**  
A: 如有任何問題或需求，請前往支援論壇[此處](https://forum.aspose.com/)尋求協助。

**Q: 有其他替代方案嗎？**  
A: 市面上確實有其他圖像轉換工具與函式庫，但 Aspose.Imaging for Java 提供功能完整且穩定的影像處理與轉換解決方案。

## 結論

本教學說明了如何使用 Aspose.Imaging for Java **convert raster to svg**。此流程不僅能保留圖像品質，還能讓您的資產具備向量圖的彈性，未來無論在任何顯示或列印需求下皆能保持最佳效果。歡迎嘗試不同的點陣圖格式，並將此工作流程整合至更大型的影像處理管線中。

---

**最後更新：** 2025-12-30  
**測試環境：** Aspose.Imaging for Java 24.12（撰寫時最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}