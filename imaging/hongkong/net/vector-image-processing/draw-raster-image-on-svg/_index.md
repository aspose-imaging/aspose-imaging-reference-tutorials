---
title: 如何在 Aspose.Imaging for .NET 中在 SVG 上繪製光柵圖像
linktitle: 在 Aspose.Imaging for .NET 中在 SVG 上繪製光柵圖像
second_title: Aspose.Imaging .NET 映像處理 API
description: 了解如何使用 Aspose.Imaging for .NET 在 SVG 上繪製光柵影像。使用動態影像增強您的 .NET 應用程式。
weight: 11
url: /zh-hant/net/vector-image-processing/draw-raster-image-on-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Imaging for .NET 中在 SVG 上繪製光柵圖像


在 .NET 程式設計領域，Aspose.Imaging 是一個可靠且多功能的函式庫，用於處理各種與影像相關的任務。它提供的一項令人著迷的功能是能夠在 SVG 畫布上繪製光柵圖像。在本逐步指南中，我們將引導您完成使用 Aspose.Imaging for .NET 在 SVG 上繪製光柵影像的過程。

## 先決條件

在我們深入了解細節之前，請確保您具備以下先決條件：

-  Aspose.Imaging for .NET：您必須安裝該程式庫。如果沒有，您可以從以下位置下載[Aspose.Imaging for .NET 下載頁面](https://releases.aspose.com/imaging/net/).

- 您的文件目錄：替換`"Your Document Directory"`與您的工作目錄的實際路徑。

現在，讓我們將該過程分解為易於遵循的步驟：

## 步驟1：導入必要的命名空間

您需要匯入所需的命名空間才能使用 Aspose.Imaging：

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## 第 2 步：載入圖像

- 首先，載入要在 SVG 畫布上繪製的光柵影像。

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- 接下來，在要繪製光柵圖像的位置載入 SVG 畫布圖像。

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## 第 3 步：在 SVG 影像上繪圖

現在，您可以開始在現有的 SVG 圖像上繪圖。為此，您需要建立一個實例`SvgGraphics2D`：

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## 第四步：繪製光柵影像

- 定義要繪製光柵影像的邊界並指定光柵影像的來源區域。

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## 第 5 步：儲存結果

在 SVG 畫布上繪製光柵圖像後，您可以儲存生成的圖像：

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## 結論

恭喜！您已使用 Aspose.Imaging for .NET 在 SVG 畫布上成功繪製了光柵影像。這對於在 .NET 應用程式中創建豐富且動態的映像非常有用。

有關更多資訊和詳細文檔，請訪問[Aspose.Imaging for .NET 文檔](https://reference.aspose.com/imaging/net/).

## 經常問的問題

### 什麼是 Aspose.Imaging for .NET？
   Aspose.Imaging for .NET 是一個功能強大的映像處理庫，可讓開發人員在 .NET 應用程式中建立、操作和轉換各種格式的映像。

### 我可以在商業專案中使用 Aspose.Imaging for .NET 嗎？
   是的，您可以在商業和非商業項目中使用 Aspose.Imaging for .NET。許可詳細資訊可以在[購買頁面](https://purchase.aspose.com/buy).

### 有免費試用嗎？
   是的，您可以從以下位置取得 Aspose.Imaging for .NET 的免費試用版：[這裡](https://releases.aspose.com/).

### 我可以在哪裡獲得支援或提問？
   如果您有任何疑問或需要支持，您可以訪問[Aspose.Imaging 論壇](https://forum.aspose.com/).

### 如何取得 Aspose.Imaging for .NET 的臨時授權？
   您可以從以下地點獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).



{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
