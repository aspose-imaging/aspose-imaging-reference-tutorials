---
"date": "2025-06-03"
"description": "了解如何使用 Aspose.Imaging for .NET 和 AdobeDeflate 壓縮將光柵圖像儲存為 TIFF 文件，從而優化檔案大小而不犧牲品質。"
"title": "使用 Aspose.Imaging .NET™ AdobeDeflate 壓縮指南將光柵影像儲存為 TIFF"
"url": "/zh-hant/net/format-specific-operations/save-raster-images-tiff-aspose-imaging-net/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 使用 Aspose.Imaging .NET 和 AdobeDeflate 壓縮將光柵圖像儲存為 TIFF

## 介紹

您是否希望有效率地將光柵影像儲存為 TIFF 文件，同時在不犧牲品質的情況下減少文件大小？本指南將指導您使用適用於 .NET 的 Aspose.Imaging 庫，利用 Adobe Deflate 壓縮來優化圖像存儲，並提高處理大量圖像的應用程式的效能。

**您將學到什麼：**
- 使用 Aspose.Imaging 設定 TIFF 選項
- 為 TIFF 檔案設定 AdobeDeflate 壓縮
- 使用 C# 和 .NET 載入和儲存光柵圖像

首先，請確保您已準備好接下來需要的一切。

## 先決條件

在深入研究之前，請確保您已具備以下條件：

### 所需的庫和版本：
- Aspose.Imaging for .NET（建議使用最新版本）

### 環境設定要求：
- Visual Studio 或任何相容的 IDE
- 對 C# 程式設計有基本的了解

### 知識前提：
- 熟悉影像處理概念
- 了解壓縮技術（可選但有幫助）

考慮到這些先決條件，讓我們設定 Aspose.Imaging for .NET 並開始。

## 設定 Aspose.Imaging for .NET

若要開始使用 Aspose.Imaging for .NET，請透過下列方法之一安裝該程式庫：

### 安裝方法

**使用 .NET CLI：**
```bash
dotnet add package Aspose.Imaging
```

**使用套件管理器控制台：**
```powershell
Install-Package Aspose.Imaging
```

**NuGet 套件管理器 UI：**
搜尋“Aspose.Imaging”並直接從您的 IDE 安裝最新版本。

### 許可證獲取

您可以先免費試用 Aspose.Imaging。如需長期使用，請考慮取得臨時許可證或購買許可證：
- **免費試用：** [免費下載](https://releases.aspose.com/imaging/net/)
- **臨時執照：** [在此請求](https://purchase.aspose.com/temporary-license/)
- **購買：** [立即購買](https://purchase.aspose.com/buy)

安裝後，在您的專案中初始化 Aspose.Imaging 以確保一切設定正確。

## 實施指南

以下是使用 AdobeDeflate 壓縮將光柵圖像儲存為 TIFF 檔案的方法：

### 步驟 1：設定 TiffOptions

首先，建立一個實例 `TiffOptions` 並配置其屬性：
```csharp
// 建立具有預設格式的 TiffOptions 實例。
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);

// 設定每個樣本的位數來定義影像品質（RGB 為 8 位元）。
options.BitsPerSample = new ushort[] { 8, 8, 8 };

// 將光度解釋定義為 RGB。
options.Photometric = TiffPhotometrics.Rgb;

// 以英吋為單位設定解析度。
options.Xresolution = new TiffRational(72);
options.Yresolution = new TiffRational(72);

// 指定解析度單位（英吋）。
options.ResolutionUnit = TiffResolutionUnits.Inch;

// 選擇連續的平面配置來儲存影像資料儲存。
options.PlanarConfiguration = TiffPlanarConfigs.Contiguous;
```

### 步驟 2：套用 AdobeDeflate 壓縮

將壓縮方法設定為 AdobeDeflate：
```csharp
// 將壓縮設為 AdobeDeflate 以有效減少檔案大小。
options.Compression = TiffCompressions.AdobeDeflate;
```

### 步驟3：載入並儲存影像

載入現有的光柵影像並使用指定的選項將其儲存為 TIFF：
```csharp
string dataDir = "YOUR_DOCUMENT_DIRECTORY"; // 替換為您的文件目錄路徑
string outputDir = "YOUR_OUTPUT_DIRECTORY"; // 替換為您想要的輸出目錄路徑

// 載入現有圖像。
using (RasterImage image = (RasterImage)Image.Load(dataDir + "SampleTiff1.tiff"))
{
    // 從 RasterImage 建立 TiffImage 並使用上面配置的選項來儲存它。
    using (TiffImage tiffImage = new TiffImage(new TiffFrame(image)))
    {
        tiffImage.Save(outputDir + "SavingRasterImage_out.tiff", options);
    }
}
```

**參數解釋：**
- `BitsPerSample`：確定影像品質；每通道 8 位元是 RGB 的標準。
- `Photometric`：指定顏色解釋（在本例中為 RGB）。
- `Compression`：選擇 AdobeDeflate 有效縮小檔案大小。

### 故障排除提示
常見問題包括目錄路徑不正確或缺少依賴項。請確保所有路徑正確且 Aspose.Imaging 已正確安裝。

## 實際應用
使用壓縮保存 TIFF 影像有許多應用：
1. **歸檔：** 在數位檔案中高效率地儲存高品質影像。
2. **醫學影像：** 壓縮大型醫學掃描數據，同時保持影像完整性。
3. **出版：** 為印刷媒體準備圖像，其中品質和文件大小至關重要。

## 性能考慮
為了優化使用 Aspose.Imaging 時的效能：
- 透過適當處置物件來管理記憶體使用。
- 使用高效的壓縮設定來平衡品質和檔案大小。
- 利用 .NET 中的平行處理功能進行批次影像處理任務。

## 結論
透過本指南，您學習如何使用 Aspose.Imaging for .NET 的 Adobe Deflate 壓縮將光柵圖像儲存為 TIFF 格式。此過程有助於減小檔案大小，同時保持適用於各種專業應用程式的高品質圖像。

**後續步驟：**
- 嘗試 Aspose.Imaging 中可用的不同壓縮方法。
- 探索該庫的附加功能，例如圖像轉換和處理。

準備好實施這些技術了嗎？試著將它們應用到你的專案中，親身體驗它們帶來的好處！

## 常見問題部分
1. **什麼是 AdobeDeflate 壓縮？**
   - 一種使用 Lempel-Ziv-Welch (LZW) 壓縮和遊程編碼組合來減少 TIFF 檔案大小同時保持品質的方法。
2. **我可以將 Aspose.Imaging 與其他圖像格式一起使用嗎？**
   - 是的，Aspose.Imaging 支援多種圖片格式，包括 JPEG、PNG、BMP、GIF 等。
3. **如何開始免費試用 Aspose.Imaging？**
   - 下載免費版本 [Aspose 發佈頁面](https://releases。aspose.com/imaging/net/).
4. **在 .NET 應用程式中使用 Aspose.Imaging 有哪些最佳實務？**
   - 始終處置圖像物件以有效管理記憶體並利用.NET 的非同步處理功能。
5. **在哪裡可以找到有關 Aspose.Imaging 的更多資源？**
   - 訪問 [Aspose 文檔](https://reference.aspose.com/imaging/net/) 以獲得詳細的指南和範例。

## 資源
- **文件:** [了解更多](https://reference.aspose.com/imaging/net/)
- **下載：** [開始](https://releases.aspose.com/imaging/net/)
- **購買：** [購買許可證](https://purchase.aspose.com/buy)
- **免費試用：** [立即試用](https://releases.aspose.com/imaging/net/)
- **臨時執照：** [在此請求](https://purchase.aspose.com/temporary-license/)
- **支持：** [提出問題](https://forum.aspose.com/c/imaging/14)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}