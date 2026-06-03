---
date: 2026-01-09
description: 了解如何使用 Aspose.Imaging for Java 為圖像添加水印。本 Java 圖像處理教學將逐步示範如何快速製作斜角水印。
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: 如何添加水印 – 對角線圖像水印 (Java)
url: /zh-hant/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 如何添加水印 – 斜向影像水印 (Java)

如果你想 **how to add watermark** 到圖片，並以時尚的斜向方式呈現，Aspose.Imaging for Java 讓這件事變得輕而易舉。在本步驟教學中，我們將示範如何在 JPG（或任何支援格式）影像上加入 45 度旋轉的文字水印。即使你不是 Java 大師，也能在幾分鐘內照著說明完成。

## 快速回答
- **使用的函式庫是？** Aspose.Imaging for Java  
- **涵蓋的主要關鍵字是？** how to add watermark  
- **支援的影像格式？** JPEG, PNG, BMP, TIFF, GIF 以及其他  
- **需要多少程式碼？** 只需七個簡潔的程式碼區塊  
- **測試需要授權嗎？** 提供免費試用版；正式環境需購買授權  

## 什麼是影像處理中的「how to add watermark」？
添加水印是指在影像上覆蓋半透明的文字或圖形，以保護版權或傳達品牌訊息。斜向水印特別有效，因為它橫跨整張圖片，較難被裁剪掉。

## 為什麼選擇 Aspose.Imaging for Java？
Aspose.Imaging 提供高階 API，抽象掉低階像素操作，支援數十種格式，且可在任何 Java 執行環境上執行。它讓你專注於 *想要達成的目標*（例如加入斜向水印），而不必擔心影像格式的細節。

## 前置條件

在開始之前，請確保已具備以下項目：

1. **Aspose.Imaging for Java** – 從官方網站 **[此處](https://releases.aspose.com/imaging/java/)** 下載最新版本。  
2. **Java 開發環境** – JDK 8 以上，並使用你慣用的 IDE（IntelliJ、Eclipse、VS Code 等）。  
3. **要加水印的影像** – 將範例 JPG/TIFF/PNG 放在程式碼會參照的資料夾中。

## 匯入套件

首先匯入所需的類別。將匯入語句集中放置，可提升程式碼的可讀性與維護性。

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## 步驟 1：載入現有影像

使用 `Image.load` 方法載入來源圖片，該方法會自動偵測檔案格式。

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **小技巧：** 如範例所示，將 `Image` 物件放在 try‑with‑resources 區塊中，能自動釋放資源，避免記憶體泄漏。

## 步驟 2：準備水印文字與圖形

建立與已載入影像關聯的 `Graphics` 物件，並取得影像尺寸以供後續計算使用。

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## 步驟 3：定義字型與筆刷

選擇醒目的字型與筆刷，筆刷決定水印的顏色與不透明度。調整不透明度即可讓水印呈半透明效果。

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## 步驟 4：格式化文字

設定對齊與格式旗標，使文字在繪製時置中。

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## 步驟 5：套用變換

變換矩陣讓我們先將原點移至影像中心，然後將文字順時針旋轉 ‑45°。

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## 步驟 6：繪製並儲存

最後將字串繪製到影像上，並將結果寫入磁碟。

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

開啟 `AddDiagonalWatermarkToImage_out.jpg` 後，你會看到紅色、半透明的文字斜斜地覆蓋在圖片中心。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| 水印太淡 | 不透明度設定為 0（完全透明） | 提高不透明度，例如 `brush.setOpacity(0.5f);` |
| 文字在邊緣被裁切 | 非正方形影像的平移未置中 | 如範例使用 `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);`，必要時調整旋轉角度 |
| 不支援的影像格式錯誤 | 使用較舊的 Aspose.Imaging 版本 | 更新至最新的 Aspose.Imaging 版本 |

## 常見問答

### Q1：Aspose.Imaging for Java 適合初學者嗎？

**A：** 絕對適合！API 直觀，文件提供清晰範例。即使是剛接觸影像處理的開發者，也能依照本教學快速產出專業成果。

### Q2：我可以自訂水印文字與樣式嗎？

**A：** 可以。修改 `theString` 變數、換用不同的 `Font`、調整 `brush.setColor(...)`，或在矩陣中改變旋轉角度，即可符合品牌需求。

### Q3：Aspose.Imaging for Java 支援除 JPG 之外的其他影像格式嗎？

**A：** 支援。函式庫可處理 BMP、PNG、GIF、TIFF、PSD 等多種格式，只要將 `Image.load` 指向相應檔案即可。

### Q4：Aspose.Imaging for Java 有免費試用版嗎？

**A：** 有，您可以在 **[此處](https://releases.aspose.com/)** 取得免費試用版。

### Q5：在哪裡可以取得 Aspose.Imaging for Java 的支援或協助？

**A：** 如需提問、回報錯誤或尋求最佳實踐建議，請前往 Aspose.Imaging for Java 支援論壇 **[此處](https://forum.aspose.com/)**。

---

**最後更新：** 2026-01-09  
**測試環境：** Aspose.Imaging for Java 24.11（撰寫時最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}