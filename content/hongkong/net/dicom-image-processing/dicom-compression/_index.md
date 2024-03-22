---
title: Aspose.Imaging for .NET 中的 DICOM 壓縮
linktitle: Aspose.Imaging for .NET 中的 DICOM 壓縮
second_title: Aspose.Imaging .NET 映像處理 API
description: 了解如何使用 Aspose.Imaging for .NET 執行 DICOM 壓縮。請按照此逐步指南有效儲存和傳輸具有高診斷品質的醫學影像。
type: docs
weight: 17
url: /zh-hant/net/dicom-image-processing/dicom-compression/
---
在醫學影像領域，DICOM（醫學數位成像和通訊）標準對於儲存和共享醫學影像至關重要。 Aspose.Imaging for .NET 是一個功能強大的 .NET 函式庫，為處理 DICOM 映像提供全面的支援。本教學將引導您完成使用 Aspose.Imaging for .NET 進行 DICOM 壓縮的過程。我們將分解每個步驟並詳細解釋該過程。

## 先決條件

在我們深入研究使用 Aspose.Imaging for .NET 進行 DICOM 壓縮之前，您需要確保滿足以下先決條件：

1. 視覺工作室

確保您的系統上安裝了 Visual Studio。如果沒有，您可以從網站下載。

2. Aspose.Imaging for .NET

您必須擁有 Aspose.Imaging for .NET 函式庫。您可以透過以下連結取得該庫：

- [下載 .NET 版 Aspose.Imaging](https://releases.aspose.com/imaging/net/)
- [購買 .NET 版 Aspose.Imaging](https://purchase.aspose.com/buy)
- [取得免費試用許可證](https://releases.aspose.com/)
- [臨時執照](https://purchase.aspose.com/temporary-license/)

滿足這些先決條件後，我們就可以開始了解如何使用 Aspose.Imaging for .NET 執行 DICOM 壓縮的逐步指南。

## 導入命名空間

在繼續之前，我們需要導入必要的名稱空間來存取所需的類別和方法。開啟 Visual Studio 項目，然後在 C# 檔案的頂部新增以下內容：

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

現在，我們準備開始 DICOM 壓縮過程。

## 第1步：載入原始圖像

我們首先載入要轉換為 DICOM 格式的原始影像。確保更換`"Your Document Directory"`與影像目錄的實際路徑。

```csharp
string dataDir = "Your Document Directory";
string inputFile = Path.Combine(dataDir, "original.jpg");

using (var inputImage = Image.Load(inputFile))
{
    //您的 DICOM 壓縮程式碼將位於此處。
}
```

## 步驟 2：執行未壓縮的 DICOM 壓縮

在此步驟中，我們將執行未壓縮的 DICOM 壓縮。這是它的程式碼：

```csharp
string output1 = Path.Combine(dataDir, "original_Uncompressed.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.None }
};

inputImage.Save(output1, options);
```

## 步驟 3：執行 JPEG DICOM 壓縮

現在，讓我們繼續使用 JPEG 格式執行 DICOM 壓縮：

```csharp
string output2 = Path.Combine(dataDir, "original_JPEG.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Jpeg }
};

inputImage.Save(output2, options);
```

## 步驟 4：執行 JPEG2000 DICOM 壓縮

在此步驟中，我們將使用 JPEG2000 格式執行 DICOM 壓縮。操作方法如下：

```csharp
string output3 = Path.Combine(dataDir, "original_JPEG2000.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression
    {
        Type = CompressionType.Jpeg2000,
        Jpeg2000 = new Jpeg2000Options
        {
            Codec = Jpeg2000Codec.Jp2,
            Irreversible = false
        }
    }
};

inputImage.Save(output3, options);
```

## 步驟 5：執行 RLE DICOM 壓縮

最後，讓我們使用 RLE（運行長度編碼）格式執行 DICOM 壓縮：

```csharp
string output4 = Path.Combine(dataDir, "original_RLE.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Rle }
};

inputImage.Save(output4, options);
```

## 結論

在本逐步指南中，我們學習如何使用 Aspose.Imaging for .NET 執行 DICOM 壓縮。該庫提供了一組強大的工具來處理醫學影像，您可以透過參考進一步探索其功能[文件](https://reference.aspose.com/imaging/net/).

## 常見問題解答

### Q1：什麼是 DICOM 壓縮？

A1：DICOM 壓縮是在維持診斷品質的同時減少醫學影像大小的過程。它對於醫療數據的有效儲存和傳輸至關重要。

### Q2：為什麼要使用 Aspose.Imaging for .NET 進行 DICOM 壓縮？

A2：Aspose.Imaging for .NET 提供了一組強大的功能和使用者友好的 API，用於處理 DICOM 影像，使其成為醫學影像應用的絕佳選擇。

### Q3：我可以使用 Aspose.Imaging for .NET 將其他影像處理操作與 DICOM 壓縮結合套用嗎？

A3：是的，Aspose.Imaging for .NET 提供了廣泛的影像處理功能，可與 DICOM 壓縮結合以滿足特定要求。

### 問題 4：我可以在哪裡獲得與 Aspose.Imaging for .NET 相關的支援或提出問題？

 A4：您可以訪問[Aspose.Imaging 論壇](https://forum.aspose.com/)獲得支持、提出問題以及參與 Aspose.Imaging 社區。

### Q5：Aspose.Imaging for .NET 有試用版可供測試嗎？

 A5：是的，您可以獲得[免費試用許可證](https://releases.aspose.com/)在購買之前測試 Aspose.Imaging for .NET。