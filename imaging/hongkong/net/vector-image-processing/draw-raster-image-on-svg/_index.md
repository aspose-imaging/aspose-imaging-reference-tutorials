---
"description": "學習如何使用 Aspose.Imaging for .NET 在 SVG 上繪製光柵圖像。使用動態影像增強您的 .NET 應用程式。"
"linktitle": "在 Aspose.Imaging for .NET 中在 SVG 上繪製光柵圖像"
"second_title": "Aspose.Imaging .NET映像處理API"
"title": "如何在 Aspose.Imaging for .NET 中在 SVG 上繪製光柵圖像"
"url": "/zh-hant/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Imaging for .NET 中在 SVG 上繪製光柵圖像


在 .NET 程式設計領域，Aspose.Imaging 是一個可靠且功能強大的函式庫，可用於處理各種影像相關任務。它提供的一項引人入勝的功能是在 SVG 畫布上繪製光柵圖像。在本逐步指南中，我們將引導您完成使用 Aspose.Imaging for .NET 在 SVG 上繪製光柵影像的過程。

## 先決條件

在深入了解細節之前，請確保您已滿足以下先決條件：

- Aspose.Imaging for .NET：您必須安裝該程式庫。如果沒有，您可以從 [Aspose.Imaging for .NET下載頁面](https://releases。aspose.com/imaging/net/).

- 您的文件目錄：替換 `"Your Document Directory"` 使用您的工作目錄的實際路徑。

現在，讓我們將這個過程分解為易於遵循的步驟：

## 步驟 1：導入必要的命名空間

您需要匯入所需的命名空間才能使用 Aspose.Imaging：

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## 第 2 步：載入圖像

- 首先，載入您想要在 SVG 畫布上繪製的光柵圖像。

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- 接下來，在您想要繪製光柵圖像的位置載入 SVG 畫布圖像。

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## 步驟3：在SVG影像上繪圖

現在，您可以開始在現有的 SVG 圖像上繪圖。為此，您需要建立一個 `SvgGraphics2D`：

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## 步驟4：繪製光柵影像

- 定義要繪製光柵影像的邊界並指定光柵影像的來源區域。

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## 步驟5：保存結果

在 SVG 畫布上繪製光柵影像後，可以儲存產生的影像：

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## 結論

恭喜！您已成功使用 Aspose.Imaging for .NET 在 SVG 畫布上繪製光柵影像。這對於在 .NET 應用程式中創建豐富且動態的映像非常有用。

欲了解更多資訊和詳細文檔，請訪問 [Aspose.Imaging for .NET 文檔](https://reference。aspose.com/imaging/net/).

## 常見問題

### 什麼是 Aspose.Imaging for .NET？
   Aspose.Imaging for .NET 是一個強大的映像處理庫，可讓開發人員在 .NET 應用程式內建立、操作和轉換各種格式的映像。

### 我可以在商業專案中使用 Aspose.Imaging for .NET 嗎？
   是的，您可以在商業和非商業項目中使用 Aspose.Imaging for .NET。許可詳情請參閱 [購買頁面](https://purchase。aspose.com/buy).

### 有免費試用嗎？
   是的，您可以從以下位置免費試用 Aspose.Imaging for .NET [這裡](https://releases。aspose.com/).

### 我可以在哪裡獲得支持或提出問題？
   如果您有任何疑問或需要支持，您可以訪問 [Aspose.Imaging 論壇](https://forum。aspose.com/).

### 如何取得 Aspose.Imaging for .NET 的臨時授權？
   您可以從 [這裡](https://purchase。aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}