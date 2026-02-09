---
date: '2026-02-09'
description: 學習如何使用 Aspose.Imaging for .NET 將 JPEG 轉換為 TIFF，並建立多幀 TIFF 圖像。內容包括環境設定、TiffOptions
  配置、從目錄載入圖像以及幀處理。
keywords:
- create multi-frame tiff images
- Aspose.Imaging for .NET tutorial
- configure TiffOptions in .NET
title: 如何使用 Aspose.Imaging for .NET 將 JPEG 轉換為 TIFF 並建立多幀 TIFF 圖像
url: /zh-hant/net/animation-multi-frame-images/create-multi-frame-tiff-images-aspose-imaging-dotnet/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 如何將 JPEG 轉換為 TIFF 並使用 Aspose.Imaging for .NET 建立多畫格 TIFF 影像

## 介紹

您是否想精通 **convert JPEG to TIFF**，同時使用 Aspose.Imaging for .NET 建立多畫格 TIFF 檔案？本完整教學將指引您設定開發環境、配置 `TiffOptions`、調整 JPEG 檔案大小，並將畫格加入 TIFF 影像，全部輕鬆完成。無論您是管理文件歸檔，或是將高品質影像整合至軟體應用，本指南都能提升您的工作流程。

**您將學會：**
- 如何設定 Aspose.Imaging for .NET
- 為黑白影像使用 CCITT Fax Group 3 壓縮配置 `TiffOptions`
- 從目錄載入並調整 JPEG 檔案大小
- 為 TIFF 影像新增畫格
- 儲存多畫格 TIFF 影像

讓我們先了解前置需求，開始動手吧。

## 快速回答
- **「convert JPEG to TIFF」是什麼意思？** 意指將 JPEG 點陣圖轉存為 TIFF 格式，通常會搭配自訂壓縮或多畫格。  
- **哪個 .NET 函式庫最適合此工作？** Aspose.Imaging for .NET 提供完整的 API，支援轉換、調整大小與多畫格建立。  
- **需要授權嗎？** 免費試用版可用於評估；正式授權會移除所有評估限制。  
- **可以自動從目錄載入影像嗎？** 可以——本教學示範如何列舉 JPEG 檔案並逐一處理。  
- **程式碼相容於 .NET 6+ 嗎？** 完全相容——範例使用 .NET Core/5+ API，可在 .NET 6 及更新版本執行。

## 什麼是「convert JPEG to TIFF」？
將 JPEG 轉換為 TIFF 包含解碼 JPEG 檔案、（可選）進行轉換（如調整大小或變更色深），再以 TIFF 格式重新編碼。TIFF 支援多畫格、無損壓縮與 JPEG 所沒有的豐富中繼資料，因而非常適合檔案保存與多頁情境。

## 為什麼選擇 Aspose.Imaging 進行此轉換？
- **完整控制**：可自行設定壓縮方式、光度解釋與像素格式。  
- **多畫格支援**：可將多個 JPEG 頁面合併成單一 TIFF 文件。  
- **跨平台**：支援 Windows、Linux 與 macOS，適用於 .NET Core/5+。  
- **無外部相依**：純受管理程式碼，無需本機 DLL。

## 前置需求

在開始使用 Aspose.Imaging 建立 TIFF 影像前，請先確認以下項目：

### 必要的函式庫與相依性
- **Aspose.Imaging for .NET**：可透過 NuGet 或您慣用的套件管理工具安裝此函式庫。

### 環境設定需求
- 支援 C# 與 .NET Core/5+ 的開發環境  

### 知識前提
- 基本的 C# 程式概念  
- 熟悉在 .NET 中處理影像檔案  

## 設定 Aspose.Imaging for .NET

首先，您需要安裝 Aspose.Imaging。以下提供三種安裝方式：

**.NET CLI**
```shell
dotnet add package Aspose.Imaging
```

**Package Manager**
```powershell
Install-Package Aspose.Imaging
```

**NuGet Package Manager UI**  
在 UI 中搜尋「Aspose.Imaging」並安裝最新版本。

### 取得授權的步驟
- **免費試用**：取得功能受限的版本以測試功能。  
- **暫時授權**：取得延長試用，免除評估限制。請前往 [Temporary License](https://purchase.aspose.com/temporary-license/)。  
- **購買授權**：若需完整功能，請至 [Purchase Aspose.Imaging](https://purchase.aspose.com/buy) 購買授權。

### 基本初始化與設定

```csharp
// Initialize the library with your license
Aspose.Imaging.License license = new Aspose.Imaging.License();
license.SetLicense("Path to your license file");
```

## 如何將 JPEG 轉換為 TIFF 並加入多個畫格

以下將實作步驟拆解為易於掌握的區塊。

### 建立與設定 TiffOptions 以產生 TIFF 影像

#### 概觀
建立 `TiffOptions` 物件可讓您自訂壓縮方式與光度解釋等設定，這對客製化 TIFF 檔案相當重要。

#### 步驟說明

**1. 匯入必要的命名空間**  
請確保在程式檔案中加入以下命名空間：

```csharp
using Aspose.Imaging.FileFormats.Tiff;
using Aspose.Imaging.FileFormats.Tiff.Enums;
using Aspose.Imaging.ImageOptions;
```

**2. 設定 TiffOptions**  
以 CCITT Fax Group 3 壓縮建立適用於黑白影像的 `TiffOptions` 物件。

```csharp
// Create TiffOptions with default settings
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);

// Set bits per sample to 1 (black and white)
outputSettings.BitsPerSample = new ushort[] { 1 };

// Use CCITT Fax Group 3 compression
outputSettings.Compression = TiffCompressions.CcittFax3;

// Define photometric interpretation as MinIsWhite
outputSettings.Photometric = TiffPhotometrics.MinIsWhite;

// Set source to an empty stream for creating new TIFF from scratch
outputSettings.Source = new Aspose.Imaging.Sources.StreamSource(new System.IO.MemoryStream());
```

### 建立具特定尺寸的 TiffImage

#### 概觀
建立 `TiffImage` 時需指定自訂尺寸，這是定義每個 TIFF 畫格大小的關鍵步驟。

**1. 定義影像尺寸**

```csharp
int newWidth = 500; // Width for each TIFF frame
int newHeight = 500; // Height for each TIFF frame
string path = "@YOUR_OUTPUT_DIRECTORY\\AddFramesToTIFFImage_out.tif";
```

**2. 建立 TiffImage 實例**  
使用先前定義的尺寸與輸出設定初始化 `TiffImage`。

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    // Logic to add frames will be added here.
}
```

### 從目錄載入 JPEG 檔案並調整大小

#### 概觀
使用 Aspose.Imaging 可輕鬆載入 JPEG、調整尺寸，並為加入 TIFF 做好準備。

**1. 載入 JPEG 影像**

```csharp
string dataDir = "@YOUR_DOCUMENT_DIRECTORY"; // Directory containing input images

foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
{
    using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
    {
        // Resize image to match TIFF frame dimensions
        ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
        
        // Additional logic for handling multiple frames will be added here.
    }
}
```

> **專業提示：** **load images from directory** 正是上述迴圈的功能——它會列舉目標資料夾中的每一個 JPEG 檔案。

### 為 TiffImage 新增畫格並儲存

#### 概觀
將調整過的 JPEG 像素複製至每個畫格，最後儲存完整的多畫格 TIFF。

**1. 初始化 TiffImage 實例**

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    int index = 0; // Frame index tracker
    
    foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
    {
        using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
        {
            ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
            
            TiffFrame frame = tiffImage.ActiveFrame;
            if (index > 0)
            {
                // Create a new frame for each subsequent image
                frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            }
            
            // Copy pixels from the resized JPEG into the TIFF frame
            frame.SavePixels(frame.Bounds, ri.LoadPixels(ri.Bounds));
            if (index > 0)
            {
                tiffImage.AddFrame(frame); // Add to TIFF image only after the first frame
            }
            index++;
        }
    }
    
    tiffImage.Save(path); // Save the final TIFF with all frames
}
```

## 實務應用

以下列出建立多畫格 TIFF 影像的常見應用情境：

1. **文件歸檔** – 將掃描文件存成單一 TIFF 檔，以確保資料完整性與易於存取。  
2. **醫學影像** – 使用高品質、壓縮的 TIFF 格式保存 MRI、CT 等掃描圖像。  
3. **平面設計** – 將多層設計合併為單一檔案，提升圖形軟體的處理效率。  
4. **攝影** – 將多頁相簿以單一檔案方式存檔，方便分享與保存。  
5. **工業品質檢測** – 在 TIFF 影像中以多畫格記錄詳細檢測資料。

## 效能考量

### 優化效能的技巧
- **記憶體管理** – 盡快釋放影像物件（使用 `using` 陳述式）以回收資源。  
- **批次處理** – 若處理大量資料，建議分批執行，以維持記憶體使用量可預測。  
- **有效壓縮** – 依需求選擇在品質與速度之間取得平衡的壓縮設定。

## 常見問題

**Q: 能否在不失真的情況下將 JPEG 轉換為 TIFF？**  
A: 可以。使用無損壓縮（如 LZW 或 CCITT Fax）並保留原始像素資料，即可達成無失真轉換。

**Q: 必須先調整影像大小才可加入為畫格嗎？**  
A: 必須。TIFF 中的所有畫格尺寸必須相同，因此需將每個 JPEG 調整至目標寬高。

**Q: TIFF 檔案可以包含多少畫格？**  
A: 實際上幾乎無限制，受限於檔案大小與可用記憶體。

**Q: 產生的 TIFF 能否在常見的檢視器中開啟？**  
A: 範例使用的 CCITT Fax Group 3 壓縮為廣泛支援的標準，大多數 TIFF 檢視器與編輯器皆能正確顯示。

**Q: 若要為彩色影像使用不同的壓縮方式，該怎麼做？**  
A: 將 `TiffCompressions.CcittFax3` 改為 `TiffCompressions.Lzw` 或 `TiffCompressions.Jpeg`，並相應調整 `BitsPerSample`。

## 結論

本教學說明了 **convert JPEG to TIFF** 以及使用 Aspose.Imaging for .NET 建立多畫格 TIFF 影像的關鍵步驟。從配置 `TiffOptions` 到加入畫格，您現在已具備將高品質影像整合至應用程式的堅實基礎。

**後續建議**  
- 嘗試其他壓縮類型與色深設定。  
- 探索 Aspose.Imaging 的其他功能，例如中繼資料處理或 PDF 轉換。  
- 參考 [官方文件](https://reference.aspose.com/imaging/net/) 以取得更深入的資訊。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-02-09  
**Tested With:** Aspose.Imaging for .NET (latest stable version)  
**Author:** Aspose