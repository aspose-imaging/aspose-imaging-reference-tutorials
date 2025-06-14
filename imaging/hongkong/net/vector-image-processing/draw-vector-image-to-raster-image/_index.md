---
"description": "學習如何在 .NET 中使用 Aspose.Imaging 將向量圖像轉換為光柵圖像。高效影像處理的分步指南。"
"linktitle": "在 Aspose.Imaging for .NET 中將向量圖像繪製為光柵圖像"
"second_title": "Aspose.Imaging .NET映像處理API"
"title": "在 Aspose.Imaging for .NET 中將向量圖像繪製為光柵圖像"
"url": "/zh-hant/net/vector-image-processing/draw-vector-image-to-raster-image/"
"weight": 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.Imaging for .NET 中將向量圖像繪製為光柵圖像


您是否希望在 .NET 應用程式中輕鬆地將向量影像轉換為光柵影像？ Aspose.Imaging for .NET 為這項任務提供了高效率的解決方案。在本逐步指南中，我們將引導您完成使用 Aspose.Imaging for .NET 將向量影像繪製為光柵影像的過程。 

## 先決條件

在深入學習本教程之前，請確保您已滿足以下先決條件：

### 1. Aspose.Imaging for .NET

您應該已安裝 Aspose.Imaging for .NET。如果沒有，您可以從以下網站下載： [下載 Aspose.Imaging for .NET](https://releases。aspose.com/imaging/net/).

### 2. .NET開發環境

確保您的電腦上已設定 .NET 開發環境。您可以使用 Visual Studio 或任何其他 .NET 開發工具。

現在，讓我們將向量影像繪製為光柵影像的過程分解為簡單、易於遵循的步驟：

## 步驟 1：初始化您的項目

首先在您的開發環境中建立一個新的.NET專案。確保您已將 Aspose.Imaging for .NET 整合到您的專案中。

## 第 2 步：載入向量圖像

在此步驟中，我們載入您想要轉換為光柵影像的向量影像（SVG 格式）。

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // …
}
```

## 步驟 3：柵格化向量圖像

現在，我們需要將 SVG 影像柵格化為 PNG 格式。這就是向量到柵格的轉換過程。

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## 步驟4：載入光柵影像

光柵化後，從流中載入 PNG 圖像以進行進一步繪製。

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // …
}
```

## 步驟5：繪製光柵影像

現在，我們可以在現有的 SVG 影像上繪製光柵影像。

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## 步驟6：保存結果

最後，儲存結果影像。現在，您擁有了包含向量圖像的光柵圖像。

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## 結論

在本教學中，我們示範如何使用 Aspose.Imaging for .NET 將向量影像轉換為光柵影像。透過這些簡單的步驟，您可以輕鬆地將此功能整合到您的 .NET 應用程式中。

### 常見問題

### 什麼是 Aspose.Imaging for .NET？
Aspose.Imaging for .NET 是一個 .NET 函式庫，提供強大的影像處理功能，包括處理各種影像格式、轉換影像和執行進階影像處理任務的能力。

### 在哪裡可以找到 Aspose.Imaging for .NET 的文檔？
您可以找到 Aspose.Imaging for .NET 的文檔 [這裡](https://reference。aspose.com/imaging/net/).

### 有免費試用版嗎？
是的，您可以免費試用 Aspose.Imaging for .NET [這裡](https://releases。aspose.com/).

### 如何取得 Aspose.Imaging for .NET 的臨時授權？
如果您需要臨時駕照，您可以申請一個 [這裡](https://purchase。aspose.com/temporary-license/).

### 在哪裡可以獲得 Aspose.Imaging for .NET 的支援？
如需任何支援或疑問，您可以訪問 [Aspose.Imaging 論壇](https://forum。aspose.com/).


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}