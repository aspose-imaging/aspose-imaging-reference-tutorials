---
title: 使用 Aspose.Imaging for .NET 將 DICOM 轉換為 PNG
linktitle: 在 Aspose.Imaging for .NET 中將 DICOM 轉換為 PNG
second_title: Aspose.Imaging .NET 映像處理 API
description: 使用 Aspose.Imaging for .NET 輕鬆將 DICOM 轉換為 PNG。簡化醫學影像共享。
type: docs
weight: 21
url: /zh-hant/net/dicom-image-processing/convert-dicom-to-png/
---
在醫學影像領域，DICOM（醫學數位成像和通訊）是一種廣泛使用的用於儲存和共享醫學影像的格式。然而，當您需要將 DICOM 檔案轉換為更常見的映像格式（如 PNG）時，Aspose.Imaging for .NET 可以助您一臂之力。本教學將引導您完成使用 Aspose.Imaging for .NET 將 DICOM 檔案轉換為 PNG 的過程。

## 先決條件

在我們深入了解轉換過程之前，您需要滿足以下先決條件：

1.  Aspose.Imaging for .NET：確保您已安裝此程式庫。您可以從[下載頁面](https://releases.aspose.com/imaging/net/).

2. DICOM 檔案：準備轉換為 PNG 的 DICOM 檔案。如果您沒有，您可以在網路上找到範例 DICOM 檔案或向您的醫學影像部門索取。

滿足這些先決條件後，您就可以開始使用 Aspose.Imaging for .NET 將 DICOM 轉換為 PNG。

## 第 1 步：導入命名空間

首先，您需要匯入使用 Aspose.Imaging 所需的命名空間。在您的 C# 程式碼中，包含以下命名空間：

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
```

## 轉換過程

現在，讓我們將轉換過程分解為多個步驟。

### 步驟2.1：載入DICOM文件

```csharp
string dataDir = "Your Document Directory";
string inputFile = Path.Combine(dataDir, "MultiframePage1.dicom");

using (Aspose.Imaging.FileFormats.Dicom.DicomImage image = (Aspose.Imaging.FileFormats.Dicom.DicomImage)Image.Load(inputFile))
{
    //您的轉換代碼將位於此處。
}
```

在此步驟中，您定義 DICOM 檔案的路徑並使用 Aspose.Imaging 載入它。

### 步驟2.2：配置PNG選項

```csharp
PngOptions options = new PngOptions();
```

在這裡，您建立一個實例`PngOptions`，它允許您指定要建立的 PNG 映像的設定。

### 步驟2.3：另存為PNG

```csharp
image.Save(dataDir + @"MultiframePage1.png", options);
```

這是實際轉換發生的地方。您使用`Save`方法使用指定的選項將載入的 DICOM 映像轉換為 PNG 映像。

### 步驟 2.4：清理（可選）

```csharp
File.Delete(dataDir + "MultiframePage1.png");
```

如果要清理中間文件，可以刪除轉換過程中建立的 PNG 檔案。

## 結論

將 DICOM 轉換為 PNG 是醫療領域的常見需求，Aspose.Imaging for .NET 簡化了此任務。只需幾行程式碼，您就可以將 DICOM 檔案轉換為 PNG 格式，使它們更易於存取和共用。 Aspose.Imaging for .NET 提供了強大且靈活的解決方案，用於處理 .NET 應用程式中的各種影像格式。

如果您遇到任何問題或對 Aspose.Imaging for .NET 有疑問，可以在[Aspose.Imaging 論壇](https://forum.aspose.com/).

## 常見問題解答

### Q1：Aspose.Imaging for .NET 可以免費使用嗎？

A1：Aspose.Imaging for .NET 是一個商業庫，需要有效的許可證才能使用。您可以獲得[臨時執照](https://purchase.aspose.com/temporary-license/)出於評估目的。有關定價和許可的更多信息，請訪問[購買頁面](https://purchase.aspose.com/buy).

### Q2: 我可以批次轉換多個 DICOM 檔案嗎？

A2：是的，Aspose.Imaging for .NET 支援批次。您可以循環遍歷多個 DICOM 檔案並將它們一次轉換為 PNG。

### Q3: DICOM 到 PNG 轉換過程有限制嗎？

A3：限制（如果有）將取決於 DICOM 檔案本身和您選擇的 PNG 選項。 Aspose.Imaging for .NET 提供了處理各種場景的彈性，但具體情況可能有所不同。

### Q4：轉換過程中出現錯誤如何處理？

 A4：您可以在 C# 程式碼中實作錯誤處理來擷取和管理異常。請參閱[文件](https://reference.aspose.com/imaging/net/)取得詳細的錯誤處理指南。

### Q5: 我可以將 DICOM 檔案轉換為 PNG 以外的其他影像格式嗎？

A5：是的，Aspose.Imaging for .NET 支援各種圖像格式。您可以根據需要將 DICOM 檔案轉換為 JPEG、BMP、TIFF 等格式。