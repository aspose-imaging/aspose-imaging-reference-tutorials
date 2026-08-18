---
date: 2026-02-09
description: 學習如何使用 Aspose.Imaging for .NET 繪製弧線，包括如何儲存 BMP 檔案、設定圖像大小以及設定圖形背景。一步一步的
  BMP 圖像生成指南。
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: 如何使用 Aspose.Imaging for .NET 繪製弧形
url: /zh-hant/net/basic-drawing/draw-arc/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Imaging for .NET 繪製弧線

在影像處理的世界中，**如何繪製弧線** 是一項常見的工作，能為任何圖形增添視覺效果。使用 Aspose.Imaging for .NET，你可以產生 BMP 圖片、設定圖片尺寸，並僅用幾行 C# 程式碼以筆刷繪製弧線。完成本教學後，你將能精確地繪製弧線、設定圖形背景，並輕鬆儲存產生的 BMP 檔案。

## 快速解答
- **程式碼產生什麼？** 產生一個 100 × 100 像素的 BMP 圖片，背景為黃色，且有一條黑色弧線。  
- **使用哪個函式庫？** Aspose.Imaging for .NET。  
- **需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買商業授權。  
- **可以更改圖片尺寸嗎？** 可以——在 `Image.Create` 呼叫中調整 width 與 height 參數。  
- **輸出格式是否固定？** 範例儲存為 BMP 檔，但可使用 Aspose.Imaging 支援的任何格式。

## 在 Aspose.Imaging 中什麼是「繪製弧線」？
繪製弧線是指根據一個邊界矩形、起始角度與掃描角度來渲染曲線段。Aspose.Imaging 提供 `Graphics.DrawArc` 方法，讓你 **使用筆刷繪製弧線** 並控制所有視覺細節。

## 為什麼使用 Aspose.Imaging 來完成此任務？
- **完整控制** 圖片尺寸、色深與檔案格式。  
- **無外部相依性**——全部在純 .NET 環境執行。  
- **高效能**，可在伺服器端產生大量圖形。  

## 前置條件

在深入程式碼之前，請確保你已具備以下項目：

1. **Aspose.Imaging for .NET** – 從官方網站[此處](https://releases.aspose.com/imaging/net/)下載。  
2. **.NET 開發環境**（Visual Studio、VS Code 或任何 C# 編譯器）。  

現在前置條件已備妥，讓我們開始繪圖吧！

## 匯入必要的命名空間

要使用 Aspose.Imaging 必須先將相關命名空間匯入程式範圍：

### 步驟 1：匯入命名空間

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

這些 `using` 陳述式讓你可以存取影像建立、圖形處理與檔案 I/O 類別。

## 如何使用 Aspose.Imaging for .NET 繪製弧線

我們將整個流程分為三個清晰步驟：建立影像、準備圖形表面，最後繪製弧線。

### 步驟 1：設定圖片（設定圖片尺寸與產生 BMP 圖片）

```csharp
// Specify the directory where you want to save the image
string dataDir = "Your Document Directory";

// Create an instance of FileStream to save the image
using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
{
    // Create an instance of BmpOptions and set its properties
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;

    // Set the source for BmpOptions and create an instance of Image
    saveOptions.Source = new StreamSource(stream);
    using (Image image = Image.Create(saveOptions, 100, 100))
    {
```

此處我們 **設定圖片尺寸** 為 100 × 100 像素，並配置 BMP 選項。`FileStream` 確保我們 **將 BMP 檔案儲存** 到指定位置。

### 步驟 2：初始化 Graphics 並設定圖形背景

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

`Graphics` 物件讓我們可以在影像上繪圖。透過呼叫 `Clear(Color.Yellow)`，我們 **設定圖形背景** 為亮黃色，使弧線更為突出。

### 步驟 3：定義弧線參數並使用 Pen 繪製弧線

```csharp
        // Define the parameters for the arc
        int width = 100;
        int height = 200;
        int startAngle = 45;
        int sweepAngle = 270;

        // Draw the arc
        graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);

        // Save the changes
        image.Save();
    }
    stream.Close();
}
```

- `width` 與 `height` 定義邊界矩形，實際上 **設定弧線的圖片尺寸**。  
- `Pen` 物件讓我們能以黑色 **使用筆刷繪製弧線**。  
- 繪製完成後，`image.Save()` 會將 **BMP 檔** 寫入磁碟。

## 常見問題與技巧

- **弧線看不見？** 確認筆的顏色與背景形成對比（例如黑色在黃色上）。  
- **尺寸不正確？** 請記得弧線的邊界矩形可能大於圖片本身；請相應調整 `width`/`height` 或圖片尺寸。  
- **效能提示：** 若需在同一圖片上繪製多個形狀，請重複使用同一個 `Graphics` 實例。

## 常見問答

### Q1: Where can I find the documentation for Aspose.Imaging for .NET?

A1: 你可以在[此處](https://reference.aspose.com/imaging/net/)參考 Aspose.Imaging for .NET 的完整文件說明。

### Q2: How can I download Aspose.Imaging for .NET?

A2: 你可以從網站[此處](https://releases.aspose.com/imaging/net/)下載 Aspose.Imaging for .NET。

### Q3: Is there a free trial available for Aspose.Imaging for .NET?

A3: 有的，你可以在[此處](https://releases.aspose.com/)取得免費試用版，體驗 Aspose.Imaging for .NET。

### Q4: Do I need a temporary license for Aspose.Imaging for .NET?

A4: 若需要臨時授權，可於[此處](https://purchase.aspose.com/temporary-license/)取得。

### Q5: Where can I seek support or ask questions about Aspose.Imaging for .NET?

A5: 你可以前往 Aspose.Imaging 論壇[此處](https://forum.aspose.com/)尋求支援與討論。

**最後更新：** 2026-02-09  
**測試環境：** Aspose.Imaging 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}