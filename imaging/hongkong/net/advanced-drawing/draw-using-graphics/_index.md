---
date: 2026-02-06
description: 學習如何使用 Aspose.Imaging for .NET 繪製圖形，包括如何設定影像選項、清除影像表面、套用線性漸層，以及在 C# 中繪製形狀。
linktitle: Draw Using Graphics in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: 如何使用 Aspose.Imaging for .NET 繪製圖形 – 圖像繪製精通
url: /zh-hant/net/advanced-drawing/draw-using-graphics/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Imaging for .NET 繪製圖形

在影像處理與操作的領域中，**如何繪製圖形** 使用 Aspose.Imaging for .NET 是 .NET 開發者常見的問題。本教學將帶領您建立位圖、設定影像選項、清除影像表面、套用線性漸層，並在 C# 中繪製形狀。完成後，您將擁有一個可直接套用於自己專案的完整實作範例。

## 快速回答
- **需要哪個函式庫？** Aspose.Imaging for .NET（從官方連結下載）。  
- **支援哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買商業授權。  
- **可以套用線性漸層嗎？** 可以 – `LinearGradientBrush` 可讓您以平滑的顏色過渡填滿形狀。  
- **如何清除影像表面？** 使用 `graphics.Clear(Color.White)`（或其他背景顏色）。

## 什麼是 Aspose.Imaging 中的「繪製圖形」？
繪製圖形是指使用 `Graphics` 類別在影像畫布上渲染向量形狀、文字與填色區域。它類似於 GDI+，但支援跨平台，且可處理多種影像格式。

## 為什麼要使用 Aspose.Imaging 來繪製圖形？
- **功能豐富的繪圖 API** – 內建筆刷、漸層、抗鋸齒等。  
- **無外部相依性** – 所有功能皆內建於函式庫中。  
- **支援超過 100 種影像格式** – 從 BMP、PNG 到 RAW、PSD。  
- **企業級** – 高效能、執行緒安全，且文件完整。

## 前置條件

在開始之前，請先確保您具備以下項目：

1. **Aspose.Imaging for .NET** – 從 [download link](https://releases.aspose.com/imaging/net/) 下載。  
2. **.NET 開發環境** – Visual Studio、VS Code 或 Rider。  
3. **基本的 C# 知識** – 需要熟悉類別、方法與 `using` 陳述式。

## 匯入命名空間

首先，將所需的命名空間加入作用域：

```csharp
using Aspose.Imaging;
```

此行程式碼讓您可以使用所有 Aspose.Imaging 類別，包括 `Image`、`Graphics`、`BmpOptions` 以及各種筆刷與筆的類型。

## 如何使用 Aspose.Imaging 繪製圖形

以下為逐步說明。每一步皆包含簡短說明，並附上原始程式碼區塊（保持不變）。

### 步驟 1：設定影像選項並建立畫布  

我們先配置位圖選項 – 這是 **設定影像選項** 的部分。`BitsPerPixel` 屬性定義顏色深度，而 `FileCreateSource` 則指向輸出資料夾。

```csharp
public static void Run()
{
    Console.WriteLine("Running example DrawingUsingGraphics");
    string dataDir = "Your Document Directory";
    BmpOptions imageOptions = new BmpOptions();
    imageOptions.BitsPerPixel = 24;
    imageOptions.Source = new FileCreateSource(dataDir, false);
    
    // Create an image with the specified options
    using (var image = Image.Create(imageOptions, 500, 500))
    {
        var graphics = new Graphics(image);
        // Continue with drawing operations
    }
    Console.WriteLine("Finished example DrawingUsingGraphics");
}
```

### 步驟 2：清除影像表面  

在繪製任何內容之前，先 **清除影像表面** 以確保背景乾淨。

```csharp
graphics.Clear(Color.White);
```

您可以將 `Color.White` 替換為其他 `Color` 值，以設定不同的背景顏色。

### 步驟 3：定義筆刷並繪製形狀  

現在我們 **以 C# 方式繪製形狀**。`Pen` 定義輪廓顏色與寬度，而 `Graphics` 物件負責繪製幾何圖形。

```csharp
var pen = new Pen(Color.Blue);
graphics.DrawEllipse(pen, new Rectangle(10, 10, 150, 100));

using (var linearGradientBrush = new LinearGradientBrush(image.Bounds, Color.Red, Color.White, 45f))
{
    graphics.FillPolygon(
        linearGradientBrush,
        new[] { new Point(200, 200), new Point(400, 200), new Point(250, 350) });
}
```

在上述程式碼中，我們同時 **套用線性漸層** 給多邊形，讓顏色從紅色平滑過渡至白色，角度為 45 度。

### 步驟 4：儲存影像  

最後，將位圖寫入磁碟。`Image.Save()` 會依照選項中定義的格式（此例為 BMP）寫入檔案。

```csharp
image.Save();
```

## 常見問題與解決方案

| 問題 | 為何會發生 | 解決方式 |
|------|------------|----------|
| **影像未儲存** | `dataDir` 指向不存在的資料夾。 | 確認資料夾已建立，或使用 `Path.Combine` 搭配 `Environment.CurrentDirectory`。 |
| **漸層呈單色** | `LinearGradientBrush` 的角度超出範圍。 | 使用 0‑360 度之間的角度；45f 為常用的對角線漸層。 |
| **筆寬過細** | 預設筆寬為 1 像素。 | 建立筆時指定寬度，例如 `new Pen(Color.Blue, 3)`。 |
| **記憶體不足例外** | 影像尺寸過大。 | 減少寬高或將影像分塊處理。 |

## 常見問答

### Q: 什麼是 Aspose.Imaging for .NET？  
A: Aspose.Imaging for .NET 是一套功能強大的影像處理函式庫，讓開發者能以 .NET 建立、編輯與操作各種格式的影像。

### Q: 從哪裡可以下載 Aspose.Imaging for .NET？  
A: 您可從 [download link](https://releases.aspose.com/imaging/net/) 下載。

### Q: 可以在購買前試用 Aspose.Imaging for .NET 嗎？  
A: 可以，請前往 [this link](https://releases.aspose.com/) 取得免費試用版。

### Q: 如何取得 Aspose.Imaging for .NET 的臨時授權？  
A: 請前往 [this link](https://purchase.aspose.com/temporary-license/) 申請臨時授權。

### Q: Aspose.Imaging for .NET 的主要功能有哪些？  
A: 主要功能包括影像建立、編輯與轉換，支援多種影像格式，以及進階的繪圖能力。

## 結論

現在您已掌握一個完整、可投入生產環境的範例，說明 **如何使用 Aspose.Imaging for .NET 繪製圖形**。透過設定影像選項、清除表面、套用線性漸層與繪製形狀，您可以從簡單圖表到複雜的程式產生藝術作品皆得以實作。若遇到任何問題，Aspose 社群是尋求協助的好地方。

如有任何疑問或需要協助，歡迎前往 [Aspose.Imaging 支援論壇](https://forum.aspose.com/) 取得支援。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-02-06  
**測試環境：** Aspose.Imaging for .NET（最新發行版）  
**作者：** Aspose