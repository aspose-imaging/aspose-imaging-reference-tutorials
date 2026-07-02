---
date: 2026-02-12
description: 學習如何使用 Aspose 建立空白圖像以及如何在 .NET 中使用 Aspose.Imaging 繪製矩形——為您的 .NET 應用程式提供的圖像處理快速指南。
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: 建立空白圖像 Aspose – 在 .NET 中繪製矩形
url: /zh-hant/net/basic-drawing/draw-rectangle/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 建立空白圖像 Aspose – 在 .NET 中繪製矩形

在 .NET 應用程式中建立與操作圖像可能讓人感到困難，但使用 Aspose.Imaging 您只需幾行程式碼即可 **建立空白圖像 Aspose**，然後在其上繪製形狀。在本教學中，我們將完整說明從設定空白畫布到繪製矩形的每個步驟，讓您立即在 .NET 專案中加入圖形。

## 快速回答
- **「create blank image Aspose」是什麼意思？** 代表使用 Aspose.Imaging API 產生一個空的 bitmap。  
- **如何在 .NET 中使用 Aspose 繪製矩形？** 在初始化 `Graphics` 物件後，呼叫 `Graphics.DrawRectangle` 方法。  
- **需要哪個 NuGet 套件？** `Aspose.Imaging`（最新版本）。  
- **可以將圖像儲存為 PNG、JPEG 或 BMP 嗎？** 可以，只要更改圖像選項（例如 `BmpOptions`、`JpegOptions`）。  
- **開發時需要授權嗎？** 免費試用可用於評估；正式上線須購買商業授權。

## 什麼是「create blank image Aspose」？
建立空白圖像表示配置一個具有特定寬度、高度與像素格式的像素緩衝區。Aspose.Imaging 會處理底層細節，為您提供一個可直接繪圖的畫布，無需使用 GDI+ 或 System.Drawing。

## 為什麼在 .NET 中使用 Aspose.Imaging 繪製矩形？
- **跨平台** – 支援 Windows、Linux 與 macOS。  
- **無原生相依性** – 完全以受管理程式碼實作，適合伺服器環境。  
- **豐富的繪圖 API** – 支援筆刷、抗鋸齒與多種形狀類型。  
- **高效能** – 為大尺寸圖像與批次處理進行最佳化。

## 先決條件

1. **Aspose.Imaging for .NET** – 從 [download page](https://releases.aspose.com/imaging/net/) 下載。  
2. **開發環境** – Visual Studio、VS Code 或任何相容 .NET 的 IDE。  
3. **.NET 執行環境** – .NET 6+ 或 .NET Framework 4.7.2+。  

現在一切就緒，讓我們深入程式碼。

## 如何在 .NET 中建立空白圖像 Aspose？

### 步驟 1：匯入必要的命名空間

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

這些命名空間讓您可以使用核心影像類別、筆刷類型以及圖像儲存選項。

### 步驟 2：建立空白圖像（畫布）

```csharp
string dataDir = "Your Document Directory";  // Set the path to your document directory
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Your drawing code will go here
        image.Save();
    }
}
```

在此程式區塊中，我們：

* 定義輸出位置 (`dataDir`)。  
* 設定 `BmpOptions` 以使用 32 位元像素格式。  
* 建立一個 **空白圖像**，尺寸為 100 × 100 像素。  

### 步驟 3：如何使用 Aspose.Imaging 在 .NET 中繪製矩形

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` 會以背景色（本例為黃色）填滿畫布。  
* `DrawRectangle` 繪製兩個矩形——一個使用簡單的紅色筆，另一個使用藍色實心筆刷，以產生視覺對比。

### 步驟 4：儲存圖像

```csharp
image.Save();
```

呼叫 `Save` 會依先前設定的選項將 bitmap 寫入檔案系統。

## 常見問題與技巧

| 問題 | 原因 | 解決方法 |
|-------|--------|-----|
| **空白圖像顯示為黑色** | 背景未清除 | 在繪圖前呼叫 `graphic.Clear(Color.YourColor)`。 |
| **找不到檔案例外** | `dataDir` 指向不存在的資料夾 | 確認目錄已建立，或使用 `Path.Combine` 搭配 `Environment.CurrentDirectory`。 |
| **顏色不正確** | 使用 `System.Drawing.Color` 而非 `Aspose.Imaging.Color` | 始終匯入 `Aspose.Imaging.Color`。 |
| **大型圖像效能延遲** | 使用預設 `BmpOptions` 且位元深度過高 | 改用 `JpegOptions` 或 `PngOptions` 以壓縮圖像。 |

## 常見問答（延伸）

**問：我可以繪製除矩形之外的其他形狀嗎？**  
**答：** 當然可以。Aspose.Imaging 提供 `DrawEllipse`、`DrawLine`、`DrawPolygon` 等方法。

**問：此函式庫可免費用於商業用途嗎？**  
**答：** 不行，Aspose.Imaging 為商業產品，但您可透過此處的免費試用版進行評估 [here](https://releases.aspose.com/)。  

**問：這能同時在 Windows 與 Web 應用程式上運作嗎？**  
**答：** 可以，相同程式碼可在 ASP.NET、Blazor 以及主控台應用程式中執行。

**問：如何將輸出格式改為 PNG？**  
**答：** 將 `BmpOptions` 改為 `PngOptions`，並相應調整檔案副檔名。

**問：在哪裡可以找到更詳細的文件說明？**  
**答：** 參閱完整 API 參考 [here](https://reference.aspose.com/imaging/net/) 並加入 [Aspose.Imaging forum](https://forum.aspose.com/) 社群。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-02-12  
**測試環境：** Aspose.Imaging 24.12 for .NET  
**作者：** Aspose