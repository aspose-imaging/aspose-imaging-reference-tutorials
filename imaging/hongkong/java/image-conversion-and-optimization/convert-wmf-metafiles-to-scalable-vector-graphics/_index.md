---
date: 2025-12-30
description: 學習如何將 WMF 轉換為 SVG，並使用 Aspose.Imaging for Java 儲存 SVG 檔案。請跟隨我們的逐步指南，實現高效的圖像格式轉換。
linktitle: Convert WMF Metafiles to Scalable Vector Graphics
second_title: Aspose.Imaging Java Image Processing API
title: 將 WMF 轉換為 SVG – 將 WMF 中繼檔轉換為可縮放向量圖形
url: /zh-hant/java/image-conversion-and-optimization/convert-wmf-metafiles-to-scalable-vector-graphics/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 將 WMF 轉換為 SVG – 將 WMF 中繪圖檔轉換為可縮放向量圖形

## Introduction

歡迎閱讀我們的逐步指南，說明如何使用 Aspose.Imaging for Java **將 WMF 轉換為 SVG**。無論您是資深開發人員還是剛入門，本教學都會提供完成轉換所需的一切，讓您快速且可靠地執行。

## Quick Answers
- **此轉換的功能是什麼？** 它將 Windows Metafile (WMF) 圖形轉換為可縮放的 SVG 標記。  
- **需要哪個函式庫？** Aspose.Imaging for Java（可從官方網站下載）。  
- **是否需要授權？** 開發階段可使用免費試用版；正式上線則需商業授權。  
- **可以自訂輸出尺寸嗎？** 可以——透過光柵化選項可設定頁面寬度與高度。  
- **Java 8 足夠嗎？** 足夠，函式庫支援 Java 8 及更高版本。

## What is “convert wmf to svg”?

將 WMF 轉換為 SVG 意味著將基於向量的 Windows Metafile 重新寫成可縮放向量圖形（Scalable Vector Graphics），這是一種基於 XML 的格式，可在不失真情況下縮放，且可在瀏覽器與裝置間通用。

## Why use Aspose.Imaging for this conversion?
- **高保真度** – 保留向量資料與視覺品質。  
- **無外部相依性** – 純 Java，無需本機二進位檔。  
- **細緻控制** – 光柵化選項可讓您自訂尺寸、 DPI 等參數。  
- **跨平台** – 可在 Windows、Linux 與 macOS 上執行。

## Prerequisites

在開始轉換流程之前，請確保已具備以下前置條件：

1. **Java 開發環境** – 在機器上安裝 Java 8 或更新版本。  
2. **Aspose.Imaging 函式庫** – 需要 Aspose.Imaging for Java 函式庫。可從 [here](https://releases.aspose.com/imaging/java/) 下載。  
3. **開發工具 (IDE)** – Eclipse、IntelliJ IDEA 或 NetBeans 均適用於本教學。

現在，讓我們一步步走過實作流程。

## How to convert WMF to SVG using Aspose.Imaging

### Step 1: Import Packages

在 Java 程式碼中，匯入處理 WMF 與 SVG 檔案所需的 Aspose.Imaging 套件。請在 Java 檔案的最上方加入以下匯入語句：

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.SvgOptions;
import com.aspose.imaging.imageoptions.WmfRasterizationOptions;
```

### Step 2: Load the WMF Image

接著，載入欲轉換的 WMF 圖像。將佔位路徑替換為實際 WMF 檔案的位置：

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Create an instance of Image class by loading an existing WMF file.
try (Image image = Image.load(dataDir + "input.wmf")) {
    // Your code goes here...
}
```

### Step 3: Set Rasterization Options

建立 `WmfRasterizationOptions` 的實例以定義輸出尺寸。此步驟可讓您控制產生之 SVG 的頁面寬度與高度：

```java
final WmfRasterizationOptions options = new WmfRasterizationOptions();
options.setPageWidth(image.getWidth()); // Set the page width
options.setPageHeight(image.getHeight()); // Set the page height
```

### Step 4: Save as SVG

最後，將 WMF 圖像儲存為 SVG 檔案。此呼叫使用 `SvgOptions` 並結合先前設定的光柵化選項。檔名即為 **save svg file java** 操作的示例：

```java
image.save("Your Document Directory" + "ConvertWMFMetaFileToSVG_out.svg", new SvgOptions() {{ setVectorRasterizationOptions(options); }});
```

完成！您已成功 **將 WMF 轉換為 SVG**，並使用 Java 儲存了 SVG 檔案。

## Common Issues and Solutions

- **找不到檔案** – 請確認 `dataDir` 指向正確的資料夾，且 `input.wmf` 確實存在。  
- **SVG 輸出為空白** – 請確保光柵化選項與來源圖像尺寸相符；尺寸不匹配可能導致內容為空。  
- **授權例外** – 試用授權可用於評估，但正式上線時需購買授權。

## Frequently Asked Questions

**Q: Aspose.Imaging for Java 是免費的嗎？**  
A: 不是，Aspose.Imaging 為商業函式庫。您可從 [here](https://releases.aspose.com/) 取得免費試用，或從 [here](https://purchase.aspose.com/buy) 購買授權。

**Q: 我可以在商業專案中使用 Aspose.Imaging for Java 嗎？**  
A: 可以，您只需取得有效授權即可在商業專案中使用 Aspose.Imaging for Java。

**Q: Aspose.Imaging for Java 還支援哪些影像格式的轉換？**  
A: Aspose.Imaging 支援多種影像格式，包括 BMP、JPEG、PNG、TIFF 等。

**Q: 有 Aspose.Imaging 的社群論壇可供支援嗎？**  
A: 有，您可在 [Aspose.Imaging Forum](https://forum.aspose.com/) 找到支援與討論的社群論壇。

**Q: 哪個版本的 Java 與 Aspose.Imaging for Java 相容？**  
A: Aspose.Imaging for Java 相容於 Java 8 及更高版本。

## Conclusion

在本教學中，我們完整示範了使用 Aspose.Imaging for Java **將 WMF 轉換為 SVG** 的流程。只要環境設定妥當、寫幾行程式碼，即可輕鬆將 WMF 中繪圖檔轉換為可縮放的 SVG 圖形，供現代網站與 UI 應用使用。

如需進一步資訊，請參考官方 API 文件： [Aspose.Imaging for Java documentation](https://reference.aspose.com/imaging/java/).

---

**最後更新：** 2025-12-30  
**測試環境：** Aspose.Imaging for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}