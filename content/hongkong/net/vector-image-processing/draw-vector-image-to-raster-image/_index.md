---
title: 在 Aspose.Imaging for .NET 中將向量圖像繪製為光柵圖像
linktitle: 在 Aspose.Imaging for .NET 中將向量圖像繪製為光柵圖像
second_title: Aspose.Imaging .NET 映像處理 API
description: 了解如何使用 Aspose.Imaging 在 .NET 中將向量影像轉換為光柵影像。高效影像處理的分步指南。
type: docs
weight: 13
url: /zh-hant/net/vector-image-processing/draw-vector-image-to-raster-image/
---

您是否希望在 .NET 應用程式中輕鬆地將向量影像轉換為光柵影像？ Aspose.Imaging for .NET 為此任務提供了有效的解決方案。在本逐步指南中，我們將引導您完成使用 Aspose.Imaging for .NET 將向量影像繪製為光柵影像的過程。 

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

### 1. .NET 的 Aspose.Imaging

您應該安裝 Aspose.Imaging for .NET。如果沒有，您可以從以下網站下載：[下載 .NET 版 Aspose.Imaging](https://releases.aspose.com/imaging/net/).

### 2..NET開發環境

確保您的電腦上設定了 .NET 開發環境。您可以使用 Visual Studio 或任何其他 .NET 開發工具。

現在，讓我們將向量影像繪製為光柵影像的過程分解為簡單、易於遵循的步驟：

## 第 1 步：初始化您的項目

首先在開發環境中建立一個新的 .NET 專案。確保您已將 Aspose.Imaging for .NET 整合到您的專案中。

## 第 2 步：載入向量圖像

在此步驟中，我們載入要轉換為光柵影像的向量影像（SVG 格式）。

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ……
}
```

## 第 3 步：光柵化向量圖像

現在，我們需要將 SVG 影像柵格化為 PNG 格式。這是從向量到柵格的轉換發生的地方。

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## 第 4 步：載入光柵圖像

光柵化後，從流中載入 PNG 圖像以進行進一步繪製。

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ……
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

## 第 6 步：儲存結果

最後，儲存結果影像。您現在擁有包含向量圖像的光柵圖像。

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## 結論

在本教學中，我們示範如何使用 Aspose.Imaging for .NET 將向量影像轉換為光柵影像。透過這些簡單的步驟，您可以輕鬆地將此功能整合到您的 .NET 應用程式中。

### 經常問的問題

### 什麼是 Aspose.Imaging for .NET？
Aspose.Imaging for .NET 是一個 .NET 函式庫，提供強大的影像處理功能，包括處理各種影像格式、轉換影像和執行進階影像處理任務的能力。

### 在哪裡可以找到 Aspose.Imaging for .NET 的文檔？
您可以找到 Aspose.Imaging for .NET 的文檔[這裡](https://reference.aspose.com/imaging/net/).

### 有免費試用版嗎？
是的，您可以免費試用 Aspose.Imaging for .NET[這裡](https://releases.aspose.com/).

### 如何取得 Aspose.Imaging for .NET 的臨時授權？
如果您需要臨時許可證，您可以獲得一個[這裡](https://purchase.aspose.com/temporary-license/).

### 在哪裡可以獲得 Aspose.Imaging for .NET 的支援？
如需任何支援或疑問，您可以訪問[Aspose.Imaging 論壇](https://forum.aspose.com/).
