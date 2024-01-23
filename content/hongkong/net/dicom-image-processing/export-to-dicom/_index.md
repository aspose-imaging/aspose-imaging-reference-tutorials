---
title: 在 Aspose.Imaging for .NET 中將映像匯出到 DICOM
linktitle: 在 Aspose.Imaging for .NET 中匯出到 DICOM
second_title: Aspose.Imaging .NET 映像處理 API
description: 了解如何使用 Aspose.Imaging 將影像匯出為 .NET 中的 DICOM 格式。輕鬆轉換醫學影像。
type: docs
weight: 23
url: /zh-hant/net/dicom-image-processing/export-to-dicom/
---
在醫學影像領域，醫學數位影像和通訊 (DICOM) 格式是無可爭議的王者。 DICOM 文件儲存和管理醫學影像及相關訊息，促進不同醫療保健系統之間醫學影像的無縫交換和解釋。如果您希望在 .NET 應用程式中使用 DICOM 文件，那麼您來對地方了。在本教程中，我們將深入研究如何使用 Aspose.Imaging for .NET（一個可簡化流程的強大庫）將圖像匯出到 DICOM。在本指南結束時，您將具備利用 Aspose.Imaging for .NET 潛力並輕鬆建立 DICOM 檔案的知識。

## 先決條件

在我們進入技術方面之前，必須確保您具備以下先決條件：

1. Aspose.Imaging for .NET

您必須在開發環境中安裝 Aspose.Imaging for .NET。如果還沒有，您可以從 Aspose 網站下載。這是[下載連結](https://releases.aspose.com/imaging/net/)為了您的方便。

2. .NET開發環境

要使用 Aspose.Imaging for .NET，您需要 .NET 開發環境。確保您安裝了 Visual Studio 或您選擇的任何其他 .NET 開發工具。

3. 影像檔案

收集要轉換為 DICOM 格式的影像檔案。本教學假設您有一個範例圖片檔案（例如“sample.jpg”）和一個多頁圖片檔案（例如“multipage.tif”）準備轉換。

## 導入命名空間

在您的 C# 程式碼中，請確保導入必要的命名空間以存取 Aspose.Imaging 庫。您可以透過在程式碼開頭新增以下行來完成此操作：

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Dicom;
```

現在，讓我們將使用 Aspose.Imaging for .NET 將映像匯出到 DICOM 的過程分解為一系列可管理的步驟。

## 第 1 步：設定環境

確保您已在開發環境中建立了 .NET 項目，並新增了 Aspose.Imaging for .NET 作為參考。如果還沒有，請參閱 Aspose.Imaging 文檔[這裡](https://reference.aspose.com/imaging/net/)取得入門指導。

## 第 2 步：定義檔路徑

在 C# 程式碼中，定義輸入影像檔案（單頁和多頁）的路徑以及輸出 DICOM 檔案的路徑。您應該將“您的文件目錄”替換為儲存影像檔案的實際目錄路徑。

```csharp
string dataDir = "Your Document Directory";
string fileName = "sample.jpg";
string inputFileNameSingle = Path.Combine(dataDir, fileName);
string inputFileNameMultipage = Path.Combine(dataDir, "multipage.tif");
string outputFileNameSingleDcm = Path.Combine(dataDir, "output.dcm");
string outputFileNameMultipageDcm = Path.Combine(dataDir, "outputMultipage.dcm");
```

## 步驟 3：將單張影像轉換為 DICOM

若要將單一影像（在本例中為「sample.jpg」）轉換為 DICOM，請使用下列程式碼片段：

```csharp
using (var image = Image.Load(inputFileNameSingle))
{
    image.Save(outputFileNameSingleDcm, new DicomOptions());
}
```

此程式碼載入圖像，將其儲存為 DICOM 文件，並套用 DicomOptions 進行轉換。

## 步驟 4：將多頁影像轉換為 DICOM

DICOM 格式支援多頁影像。您可以按照與 JPEG 影像相同的方式將 GIF 或 TIFF 影像轉換為 DICOM。您可以這樣做：

```csharp
using (var image = Image.Load(inputFileNameMultipage))
{
    image.Save(outputFileNameMultipageDcm, new DicomOptions());
}
```

此程式碼對多頁影像執行相同的轉換過程，確保每個頁面都保留在產生的 DICOM 檔案中。

## 結論

將影像匯出為 DICOM 格式對於各種醫療保健和醫學影像應用至關重要。 Aspose.Imaging for .NET 簡化了這個過程，使開發人員能夠有效率地建立 DICOM 檔案。透過遵循此逐步指南，您可以將 DICOM 匯出功能無縫整合到您的 .NET 應用程式中。

如果您遇到任何問題或有特定要求，Aspose.Imaging 社群和支援論壇都是寶貴的資源。您可以找到幫助和指導[這裡](https://forum.aspose.com/).

## 常見問題解答

### Q1：我可以在 Web 應用程式中使用 Aspose.Imaging for .NET 將映像轉換為 DICOM 嗎？

A1：是的，Aspose.Imaging for .NET 可用於 Web 應用程式中將映像轉換為 DICOM。確保將該庫整合到您的 Web 專案中，並遵循本教程中概述的相同步驟。

### 問題 2：Aspose.Imaging for .NET 有任何授權選項嗎？

A2：Aspose 提供各種許可選項，包括用於評估的臨時許可和用於生產用途的商業許可。您可以探索許可詳細信息[這裡](https://purchase.aspose.com/buy)並獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q3：除了 JPEG、GIF 和 TIFF 之外，我還可以將其他影像格式轉換為 DICOM 嗎？

A3：Aspose.Imaging for .NET 支援多種映像格式，因此您也可以將 BMP、PNG 等格式的映像轉換為 DICOM。對於不同的圖像類型，該過程仍然相似。

### Q4：轉換影像時如何處理 DICOM 元資料？

A4：Aspose.Imaging for .NET 可讓您在轉換過程中操作和自訂 DICOM 元資料。您可以參閱文件以取得處理 DICOM 元資料的詳細資訊。

### Q5：Aspose.Imaging for .NET 有試用版嗎？

 A5：是的，您可以存取 Aspose.Imaging for .NET 的免費試用版來評估其功能。您可以下載試用版[這裡](https://releases.aspose.com/).