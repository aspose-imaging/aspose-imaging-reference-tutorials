---
date: 2026-01-04
description: 學習如何在 Java 中從光柵來源建立 TIFF 圖像檔案。本指南涵蓋圖像格式轉換、Java 圖像處理，以及如何使用 Aspose.Imaging
  以獲得無縫的結果。
linktitle: Raster Image TIFF Conversion
second_title: Aspose.Imaging Java Image Processing API
title: 如何在 Java 中使用 Aspose.Imaging 從光柵檔案建立 TIFF 圖像
url: /zh-hant/java/image-conversion-and-optimization/raster-image-tiff-conversion/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中使用 Aspose.Imaging 從光柵檔案建立 TIFF 圖像

如果您需要在 Java 應用程式中 **建立 TIFF 圖像** 檔案，Aspose.Imaging for Java 可讓此工作變得簡單。本文將逐步說明整個流程——從環境設定、載入光柵圖像、配置 TIFF 選項，到最終將結果儲存為 TIFF 檔案。完成後，您不僅了解如何 **將光柵轉換為 TIFF**，還能微調壓縮、解析度以及其他 TIFF 專屬設定。

## 快速答覆
- **哪個函式庫簡化 TIFF 建立？** Aspose.Imaging for Java  
- **主要任務是？** 從光柵來源建立 TIFF 圖像  
- **關鍵前置條件？** JDK 8+ 以及 Aspose.Imaging JAR 放在 classpath 中  
- **一般實作時間？** 基本轉換約 10‑15 分鐘  
- **可以自訂壓縮方式嗎？** 可以 – 使用 `TiffCompressions` 於 `TiffOptions`

## 什麼是 create tiff image?
建立 TIFF 圖像是指將現有光柵格式（如 PNG、JPEG 或 BMP）的像素資料編碼為標記圖像檔案格式（TIFF）。TIFF 支援多頁、無損壓縮與豐富的中繼資料，適合保存、列印與科學影像等用途。

## 為什麼使用 Aspose.Imaging 進行此影像格式轉換？
Aspose.Imaging 提供純 Java API，將 TIFF 規範的複雜性抽象化。您可獲得：

* **完整控制** 位元深度、光度解釋與壓縮方式。  
* **無原生相依** – 只要能執行 Java 的環境皆可運行。  
* **豐富文件** 與範例，協助完成各種 Java 影像處理任務。  

## 前置條件

在開始將光柵影像轉換為 TIFF 之前，請確保已具備以下條件：

### 1. Java 開發環境

請確認系統已安裝 Java Development Kit (JDK)。可從 Oracle 官方網站下載。

### 2. Aspose.Imaging for Java

您需要取得 Aspose.Imaging for Java，該套件提供處理各種影像格式的 API。可從 [此處](https://releases.aspose.com/imaging/java/) 下載。

### 3. 基礎 Java 知識

本教學假設您具備基本的 Java 程式概念，了解類別、物件與方法呼叫等。

## 匯入套件

開始之前，先將 Aspose.Imaging for Java 所需的套件匯入您的 Java 程式。操作方式如下：

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.imageoptions.TiffExpectedFormat;
import com.aspose.imaging.imageoptions.TiffPhotometrics;
import com.aspose.imaging.imageoptions.TiffRational;
import com.aspose.imaging.imageoptions.TiffResolutionUnits;
import com.aspose.imaging.imageoptions.TiffPlanarConfigs;
import com.aspose.imaging.imageoptions.TiffCompressions;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

## 步驟 1：設定環境

首先建立專案資料夾，並將欲轉換為 TIFF 的光柵圖像放入其中。您可以將 `"Your Document Directory"` 替換為實際的專案路徑。

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
```

## 步驟 2：建立 TiffOptions

接著，建立 `TiffOptions` 實例，並設定 TIFF 格式的各項屬性。可依需求自行調整這些選項。

```java
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
options.setBitsPerSample(new int[] { 8, 8, 8 });
options.setPhotometric(TiffPhotometrics.Rgb);
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));
options.setResolutionUnit(TiffResolutionUnits.Inch);
options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);
options.setCompression(TiffCompressions.AdobeDeflate);
```

## 步驟 3：載入圖像

將欲轉換的圖像載入為 `RasterImage` 實例，記得指定圖像檔案的路徑。

```java
try (RasterImage image = (RasterImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

## 步驟 4：建立 TiffImage 並儲存

從 `RasterImage` 建立新的 `TiffImage`，並在傳入 `TiffOptions` 後儲存結果。您亦可指定欲儲存的 TIFF 檔案路徑。

```java
    try (TiffImage tiffImage = new TiffImage(new TiffFrame(image))) {
        tiffImage.save("Your Document Directory" + "SavingRasterImage_out.tiff", options);
    }
}
```

完成！您已成功使用 Aspose.Imaging for Java 從光柵來源 **建立 TIFF 圖像**。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| `java.lang.NoClassDefFoundError` | Classpath 缺少 Aspose.Imaging JAR | 將 Aspose.Imaging JAR（或 Maven 依賴）加入專案 |
| 輸出品質低 | 壓縮方式使用了有損類型 | 改用 `TiffCompressions.Lzw` 或 `None` 以取得無損壓縮 |
| 顏色空間不正確 | `Photometric` 未與來源匹配 | 對於 YUV 影像使用 `TiffPhotometrics.Ycbcr` |

## 常見問答

**Q: Aspose.Imaging for Java 支援哪些影像格式？**  
A: 支援多種影像格式，包括 JPEG、PNG、TIFF、BMP、GIF 等，完整列表請參考官方文件。

**Q: 可以使用 Aspose.Imaging for Java 進行影像編輯嗎？**  
A: 可以，支援調整大小、裁切、旋轉等多種編輯操作。

**Q: 如何取得 Aspose.Imaging for Java 的臨時授權？**  
A: 前往 [Aspose 臨時授權](https://purchase.aspose.com/temporary-license/) 取得。

**Q: 有提供免費試用版嗎？**  
A: 有，請至 [Aspose.Imaging 免費試用](https://releases.aspose.com/) 下載。

**Q: 若需支援或提問，該去哪裡？**  
A: 可加入 [Aspose.Imaging 論壇](https://forum.aspose.com/) 取得協助。

## 結論

本教學說明了如何使用 Aspose.Imaging for Java 從光柵來源 **建立 TIFF 圖像**。此函式庫簡化了影像格式轉換，讓您能細緻控制壓縮、解析度與中繼資料。建議探索完整 API，以實作多頁 TIFF、元資料操作與批次處理等進階功能。

欲取得更多資訊，請參閱官方文件：[Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/)。

---

**最後更新：** 2026-01-04  
**測試環境：** Aspose.Imaging for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}