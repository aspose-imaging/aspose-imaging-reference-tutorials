---
date: 2026-02-14
description: 學習如何在 Aspose.Imaging for .NET 中繪製橢圓，這是一個多功能的圖像處理函式庫。輕鬆打造驚艷的圖形。
linktitle: How to Draw Ellipse in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: 如何在 Aspose.Imaging for .NET 中繪製橢圓
url: /zh-hant/net/basic-drawing/draw-ellipse/
weight: 12
---

 as is.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Imaging for .NET 繪製橢圓

在本教學中，我們將示範 **如何繪製橢圓**，使用 Aspose.Imaging for .NET。Aspose.Imaging 是一個功能強大的函式庫，允許您在 .NET 應用程式中操作與建立各種格式的影像。我們將先介紹概念與先決條件，然後將每個範例分解為多個步驟，以確保清晰易懂。

## 快速解答
- **使用的函式庫是什麼？** Aspose.Imaging for .NET  
- **實作需要多長時間？** 基本橢圓約 10 分鐘  
- **需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買授權  
- **可以設定影像背景嗎？** 可以 – 使用 `Graphics.Clear` 設定任意背景顏色  
- **是否相容於 .NET 6+？** 完全相容，API 可在所有現代 .NET 版本上運作  

## 先決條件

在開始使用 Aspose.Imaging for .NET 繪製橢圓之前，請先確保已具備以下先決條件：

1. Visual Studio：確保您的系統已安裝 Visual Studio，以進行 .NET 開發。  
2. Aspose.Imaging for .NET：必須已安裝 Aspose.Imaging for .NET。如未安裝，可從 [download page](https://releases.aspose.com/imaging/net/) 下載。  
3. 文件目錄：建立一個目錄，用於儲存本教學中產生的影像。  

完成上述先決條件後，我們即可開始。

## 匯入命名空間

在此步驟中，我們將匯入使用 Aspose.Imaging 所需的命名空間。請依照以下步驟操作：

### 步驟 1：開啟您的 Visual Studio 專案

啟動 Visual Studio，並開啟您打算使用 Aspose.Imaging 的 .NET 專案。

### 步驟 2：加入 Using 指令

在程式碼檔案中，加入以下 using 指令以引用所需的命名空間：

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.Colors;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.FileFormats.Bmp.Options;
using Aspose.Imaging.Sources;
```

完成必要的命名空間匯入後，即可開始繪製橢圓。

## 如何使用 Aspose.Imaging 繪製橢圓

以下將提供使用 Aspose.Imaging for .NET **繪製橢圓** 的逐步指南。本範例將帶領您完成整個流程。

### 步驟 1：設定輸出檔案

在繪製橢圓之前，需要先設定輸出檔案。操作方式如下：

```csharp
string dataDir = "Your Document Directory";
using (FileStream stream = new FileStream(dataDir + "DrawingEllipse_out.bmp", FileMode.Create))
{
```

在此程式碼片段中，我們建立 `FileStream` 以指定輸出檔案路徑。

### 步驟 2：設定 BmpOptions

若要設定 BMP 格式及其他屬性，請使用以下程式碼：

```csharp
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
saveOptions.Source = new StreamSource(stream);
```

此處，我們建立 `BmpOptions` 實例，設定位元深度，並指定來源串流。

### 步驟 3：建立 Image

使用指定的選項與尺寸，建立 `Image` 類別的實例：

```csharp
using (Image image = Image.Create(saveOptions, 100, 100))
{
```

此步驟中，我們建立一個尺寸為 100 × 100 像素的影像。

## 如何設定影像背景

乾淨的背景能讓橢圓更為突出。您可在繪製圖形前設定任意背景顏色。

### 步驟 4：初始化 Graphics 並清除表面

初始化 `Graphics` 實例，並清除影像表面：

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
```

此程式碼建立 `Graphics` 物件，並 **將影像背景設定為黃色**，為繪圖準備畫布。

## 使用 Aspose.Imaging 建立自訂圖形

畫布就緒後，您即可開始建立自訂圖形，例如橢圓、線條或多邊形。

### 步驟 5：繪製橢圓

現在，讓我們在影像上繪製橢圓：

```csharp
graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

此處，我們在影像上繪製一個紅色橢圓與一個藍色實心橢圓。

### 步驟 6：儲存影像

最後，將影像儲存：

```csharp
image.Save();
```

## 結論

在 Aspose.Imaging for .NET 中繪製橢圓是一個簡單的流程。透過本教學所列的步驟，您可以輕鬆在 .NET 應用程式中建立與操作影像。Aspose.Imaging 提供廣泛的影像編輯功能，是開發人員的寶貴工具。現在您已了解 **如何繪製橢圓**，並可將此知識延伸至更豐富的圖形製作。

## 常見問答

### Q1：Aspose.Imaging for .NET 的主要功能是什麼？

Aspose.Imaging for .NET 提供多項功能，包括影像建立、操作、轉換與渲染。它支援多種影像格式，並提供進階的影像編輯能力。

### Q2：我可以在 Windows 與 Web 應用程式中使用 Aspose.Imaging for .NET 嗎？

是的，您可在 Windows 桌面與 Web 應用程式中使用 Aspose.Imaging for .NET，具備多樣化的開發情境適用性。

### Q3：是否提供 Aspose.Imaging for .NET 的免費試用？

是的，您可從 [trial page](https://releases.aspose.com/) 取得 Aspose.Imaging for .NET 的免費試用版。

### Q4：在哪裡可以找到 Aspose.Imaging for .NET 的完整文件？

您可於 [documentation page](https://reference.aspose.com/imaging/net/) 取得 Aspose.Imaging for .NET 的詳細文件。

### Q5：若遇到問題，如何取得 Aspose.Imaging for .NET 的支援？

您可在 [forum](https://forum.aspose.com/) 向 Aspose 社群尋求協助與支援。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-02-14  
**測試環境：** Aspose.Imaging for .NET (latest release)  
**作者：** Aspose