---
date: 2026-01-17
description: 學習如何在 Aspose.Imaging 中使用 Java 中值濾波器來去除圖像噪點。本分步教學涵蓋應用中值濾波器與 Wiener 濾波器進行圖像去噪。
linktitle: Median Filter Java – Apply Median and Wiener Filters
second_title: Aspose.Imaging Java Image Processing API
title: 中值濾波器 Java – 應用中值與維納濾波器
url: /zh-hant/java/image-processing-and-enhancement/median-and-wiener-filter-application/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Median Filter Java – 套用 Median 與 Wiener 濾波器

在影像處理的領域中，去除雜訊與提升影像品質是關鍵任務。使用 **median filter java**，您可以透過 Aspose.Imaging for Java 有效清理噪點圖像。在本教學中，我們將一步步說明如何套用 Median 與 Wiener 濾波器來去噪，讓您不必編寫複雜程式碼即可取得專業等級的效果。

## Quick Answers
- **What does the median filter do?** 它會將每個像素取代為其周圍鄰域的中位數值，去除脈衝雜訊同時保留邊緣。  
- **Which library supports median filter java?** Aspose.Imaging for Java 提供即用的 `MedianFilterOptions` 類別。  
- **Do I need a license to run the code?** 免費試用版可用於評估；商業授權則需於正式環境使用。  
- **Can I chain the median filter with other filters?** 可以，您可以在中值步驟之後再套用其他濾波器，例如 Wiener。  
- **What image formats are supported?** 大多數點陣圖格式（PNG、JPEG、BMP、TIFF 等）皆完整支援。

## What is Median Filter Java?
中值濾波是一種非線性數位濾波技術，常用於 **remove image noise**。在 Java 中，Aspose.Imaging 透過 `MedianFilterOptions` 類別實作此濾波，您可以自行設定核大小，以決定要考慮多少相鄰像素。

## Why Use Median Filter Java for Image Denoising?
- **Preserves edges** 比簡單的平均濾波更能保留邊緣細節。  
- **Simple API** – 只需數行程式碼即可去除斑點與鹽與胡椒雜訊。  
- **Works on any raster image** 只要是 Aspose.Imaging 能載入的點陣圖，都能直接使用，特別適合伺服器端批次處理。

## Prerequisites
在開始之前，請確保您已具備以下條件：

1. **Java Development Environment** – 已安裝 JDK 8 或更新版本。  
2. **Aspose.Imaging for Java** – 從 [here](https://releases.aspose.com/imaging/java/) 下載並安裝套件。  
3. **Sample Noisy Image** – 任意您想清理的圖像；本教學以 `your‑noisy‑image.png` 為例。

## Import Packages
在您的 Java 專案中，先匯入必要的 Aspose.Imaging 類別：

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.imagefilters.filteroptions.MedianFilterOptions;
```

## How to Apply Median Filter Java
以下提供逐步說明。每一步皆包含簡短說明與可直接複製的程式碼。

### Step 1: Load the Noisy Image
首先，載入您想去噪的圖像。此步驟示範 **load image java**，使用 Aspose.Imaging 的 `Image.load` 方法。

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (Image image = Image.load(dataDir + "your-noisy-image.png"))
{
    // Cast the image into RasterImage
    RasterImage rasterImage = (RasterImage) image;
```

### Step 2: Create and Configure the Median Filter
建立 `MedianFilterOptions` 實例並設定核大小。核越大去噪效果越明顯，但可能會使細節變模糊。

```java
    // Create an instance of MedianFilterOptions class and set the size.
    MedianFilterOptions options = new MedianFilterOptions(4);
```

### Step 3: Apply the Median Filter
將濾波套用至整個圖像範圍，這是 **apply median filter** 的核心操作。

```java
    // Apply Median filter to RasterImage object.
    rasterImage.filter(image.getBounds(), options);
```

### Step 4: Save the Resultant Image
最後，將去噪後的圖像寫入磁碟。您即可看到中值濾波的效果。

```java
    // Save the resultant image
    image.save("Your Document Directory" + "denoised-image.png");
}
```

## Common Issues and Solutions
- **Kernel size too large** – 圖像可能會過度模糊。大多數照片建議使用 3‑5 之間的值。  
- **Unsupported image format** – 請確認檔案為 Aspose.Imaging 支援的點陣圖格式。  
- **OutOfMemoryError** – 處理大型圖像時，可先使用 `RasterImage` 的 `crop` 方法將圖像切割成較小區塊再進行濾波。

## Conclusion
本指南示範了如何使用 Aspose.Imaging 提供的 **median filter java** 方法 **how to denoise image**。依照上述步驟，您可以快速將除噪功能整合至任何基於 Java 的影像處理流程，亦可透過串接 Wiener 濾波或其他進階技術進一步提升效果。

## Frequently Asked Questions

**Q1: What is Aspose.Imaging for Java?**  
A1: Aspose.Imaging for Java 是一套讓開發者以程式方式操作影像、執行各種影像處理任務的 Java 函式庫。

**Q2: Can I use Aspose.Imaging for Java for free?**  
A2: Aspose.Imaging for Java 為商業授權函式庫，但您可從 [here](https://releases.aspose.com/) 取得免費試用版。若需長期使用，必須於 [here](https://purchase.aspose.com/buy) 購買授權。

**Q3: How can I get support for Aspose.Imaging for Java?**  
A3: 您可在 [Aspose.Imaging Forum](https://forum.aspose.com/) 向社群與專家尋求協助。

**Q4: What are some other image enhancement techniques?**  
A4: 除了 Median 濾波外，常見的影像增強技術還包括 Wiener 濾波、Gaussian 模糊與對比拉伸等。

**Q5: Can I use Aspose.Imaging for Java in my web application?**  
A5: 可以，您能將 Aspose.Imaging for Java 整合至 Web 應用程式，實現伺服器端的影像處理。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-01-17  
**測試環境：** Aspose.Imaging for Java 24.11  
**作者：** Aspose