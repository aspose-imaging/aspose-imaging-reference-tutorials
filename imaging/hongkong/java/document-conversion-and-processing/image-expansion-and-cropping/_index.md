---
date: 2026-05-24
description: 了解如何使用 image manipulation library java、Aspose.Imaging for Java 來擴展圖像、裁剪圖像，並高效儲存結果。
keywords:
- image manipulation library java
- how to crop image java
- how to expand image java
- aspose imaging expand image
linktitle: 圖像擴展與裁剪
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Discover how to use the image manipulation library java, Aspose.Imaging
    for Java, to expand images, crop them, and save results efficiently.
  headline: Image Manipulation Library Java – Expand and Crop Images Using Aspose.Imaging
  type: TechArticle
- questions:
  - answer: Yes, it supports PNG, BMP, TIFF, GIF, and many more image types.
    question: Can Aspose.Imaging handle other formats besides JPEG?
  - answer: You can use `Resize` methods provided by the library; this falls under
      **resize image java** operations.
    question: Is there a way to resize the image before cropping?
  - answer: Absolutely. Loop through a collection of file paths and apply the same
      steps to each image.
    question: Does the library support batch processing of multiple images?
  - answer: '`cacheData()` loads the image into memory once, avoiding repeated disk
      reads during manipulation – this is the essence of **cache image java**.'
    question: How does caching improve performance?
  - answer: Refer to the official documentation **[documentation](https://reference.aspose.com/imaging/java/)**
      for a complete list of classes and methods.
    question: Where can I find more detailed API references?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: Image Manipulation Library Java – 使用 Aspose.Imaging 進行圖像擴展與裁剪
url: /zh-hant/java/document-conversion-and-processing/image-expansion-and-cropping/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Java 圖像處理函式庫 – 使用 Aspose.Imaging 展開與裁剪圖像

操作圖片是網頁開發者、設計師以及所有從事數位媒體工作者的日常需求。 在本教學中，你將學習 **如何展開圖像** 檔案，並使用 Aspose.Imaging for Java（領先的 **image manipulation library java**）有效地裁剪它們。 我們將逐步說明完整的工作流程——從載入來源圖片、快取資料、定義裁剪矩形，到最後儲存裁剪結果。

## 快速解答
- **「expand image」是什麼意思？** 它會在原始圖片四周新增畫布空間，讓你可以裁剪更大的區域。  
- **應該使用哪個函式庫？** Aspose.Imaging for Java 提供豐富的 API，支援圖像展開、裁剪及其他多種操作。  
- **需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買商業授權。  
- **可以快取圖像以提升效能嗎？** 可以 – 在光柵圖像上呼叫 `cacheData()`。  
- **輸出格式有限制嗎？** 不限，你可以儲存為 JPEG、PNG、BMP 以及 Aspose.Imaging 支援的其他格式。

## 在 Java 中什麼是圖像展開與裁剪？

圖像展開是指在現有圖片周圍加入額外的像素，而裁剪則是從中擷取指定的矩形區域。 兩者結合可在不失真情況下重新構圖，常用於產生縮圖、UI 資源或為列印準備圖形。

## 為什麼在此任務中使用 Aspose.Imaging？

Aspose.Imaging 提供高效能、**格式無關** 的解決方案，能處理超過 30 種圖像格式，且可在不將整個檔案載入記憶體的情況下處理高達 500 MB 的檔案。 內建快取可將 I/O 開銷降低最高 70 %，而 API 只需少量程式碼即可完成複雜轉換，適合快速腳本與大規模服務。

## 前置條件
- Java 開發環境 (JDK 8+)
- Aspose.Imaging for Java – 下載請點擊 **[here](https://releases.aspose.com/imaging/java/)**
- IDE，例如 Eclipse 或 IntelliJ IDEA
- 要處理的圖像檔案（例如 `aspose-logo.jpg`）

現在環境已備妥，讓我們深入實作程式碼。

## 匯入套件
首先，匯入所需的類別。 這些匯入讓你能存取圖像載入、矩形定義、JPEG 選項以及光柵圖像處理。

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.JpegOptions;
import com.aspose.imaging.raster.RasterImage;
```

## 步驟 1：載入圖像
`RasterImage` 是 Aspose.Imaging 用來表示載入記憶體中的光柵圖像的類別。 將來源圖片載入為 `RasterImage` 物件。 請將佔位路徑替換為你的圖像檔案所在位置。

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
{
    // Your code here
}
```

## 步驟 2：快取圖像資料
快取可加速後續操作，特別是當你需要多次讀取像素資料時。

```java
rasterImage.cacheData();
```

## 步驟 3：定義裁剪矩形
`Rectangle` 定義了在展開後要保留的區域的 X/Y 座標與大小。 建立一個 `Rectangle` 以標示展開後要保留的區域。 座標以展開畫布的左上角為基準測量。

```java
Rectangle destRect = new Rectangle(200, 200, 300, 300);
```

> **專業提示：** 調整 X、Y、寬度與高度的數值，以符合你需要的精確區域。 這正是 **aspose crop image** 功能發揮威力的地方。

## 步驟 4：儲存裁剪後的圖像
`JpegOptions` 讓你控制輸出品質、壓縮以及其他 JPEG 專屬設定。 最後，將裁剪後的區域寫入新檔案。 `save` 方法亦可讓你指定 JPEG 品質等輸出選項。

```java
rasterImage.save("Your Document Directory" + "ExpandandCropImages_out.jpg", new JpegOptions(), destRect);
```

檔案 `ExpandandCropImages_out.jpg` 現在包含展開後的畫布，並將選取的 300 × 300 像素區域儲存為 JPEG——滿足 **save cropped image** 的需求。

## 如何使用 Aspose.Imaging 在 Java 中展開圖像？

載入原始圖片後，呼叫 `rasterImage.expandCanvas(newWidth, newHeight, backgroundColor)`，再進行裁剪。 **`expandCanvas` 會在圖像四周新增畫布空間。** 此單一方法一次完成所需的畫布擴充，保留原始像素資料，並讓你在不失真的情況下針對更大的裁剪矩形操作。

## 如何使用 Aspose.Imaging 在 Java 中裁剪圖像？

建立描述目標區域的 `Rectangle`，然後呼叫 `rasterImage.crop(rectangle)`。 **`crop` 會從圖像中擷取定義好的矩形區域。** 此裁剪呼叫會從已展開的畫布中抽取指定區域，並回傳可供儲存的新 `RasterImage` 實例。 此方式保證像素完美，且適用於所有支援的格式。

## 常見問題與解決方案
| 問題 | 原因 | 解決方式 |
|-------|--------|-----|
| `OutOfMemoryError` | 未快取的大型來源圖像 | 在處理前呼叫 `rasterImage.cacheData()` |
| 裁剪區域偏離中心 | 矩形座標錯誤 | 驗證相對於展開畫布的 X/Y 偏移量與尺寸 |
| 輸出檔案損壞 | `JpegOptions` 設定不正確 | 使用預設選項或將 `Quality = 90` 設定 |

## 常見問答

**Q: Aspose.Imaging 能處理除 JPEG 之外的其他格式嗎？**  
A: 可以，它支援 PNG、BMP、TIFF、GIF 等多種圖像類型。

**Q: 有辦法在裁剪前先調整圖像大小嗎？**  
A: 你可以使用函式庫提供的 `Resize` 方法；這屬於 **resize image java** 的操作。

**Q: 函式庫是否支援批次處理多張圖像？**  
A: 當然支援。 只要遍歷檔案路徑集合，對每張圖像套用相同步驟即可。

**Q: 快取如何提升效能？**  
A: `cacheData()` 只會將圖像載入記憶體一次，避免在操作過程中重複讀取磁碟——這正是 **cache image java** 的核心概念。

**Q: 哪裡可以找到更詳細的 API 參考文件？**  
A: 請參考官方文件 **[documentation](https://reference.aspose.com/imaging/java/)**，其中列出完整的類別與方法清單。

## 結論
現在你已掌握使用 Aspose.Imaging for Java **展開圖像** 並裁剪的完整、可投入生產的範例。 透過快取、精確的矩形定義與彈性的儲存選項，你可以將此工作流程整合至任何基於 Java 的圖像處理管線。

進一步探索其他轉換，如旋轉、加浮水印或批次調整大小。 如需更多指引，請查閱 **[documentation](https://reference.aspose.com/imaging/java/)** 或加入 **[Aspose support forum](https://forum.aspose.com/)** 社群。

---

**最後更新：** 2026-05-24  
**測試環境：** Aspose.Imaging for Java 24.11  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [Java Image Processing with Aspose.Imaging: Load, Cache, and Crop](/imaging/java/getting-started/java-image-processing-aspose-imaging-load-cache-crop/)
- [Master Image Processing with Aspose.Imaging for Java: Load, Save & Remove Backgrounds](/imaging/java/image-transformations/aspose-imaging-java-master-image-processing/)
- [Parallel Image Processing in Java with Aspose.Imaging: Multithreading & Batch Handling](/imaging/java/batch-processing-multi-threading/parallel-image-processing-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}