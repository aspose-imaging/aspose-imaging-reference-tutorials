---
title: 使用 Aspose.Imaging for .NET 調整 DICOM 影像大小
linktitle: Aspose.Imaging for .NET 中的 DICOM 簡單調整大小
second_title: Aspose.Imaging .NET 映像處理 API
description: 了解如何使用 Aspose.Imaging for .NET（醫學影像處理的強大工具）調整 DICOM 影像的大小。簡單的步驟即可獲得精確的結果。
weight: 19
url: /zh-hant/net/dicom-image-processing/dicom-simple-resizing/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Imaging for .NET 調整 DICOM 影像大小

在不斷發展的醫學影像領域，處理 DICOM（醫學數位影像和通訊）文件時的靈活性和精確度至關重要。 Aspose.Imaging for .NET 作為一個強大的解決方案出現，提供了一整套用於處理醫學影像的工具。在本教學中，我們將探索使用 Aspose.Imaging for .NET 調整 DICOM 影像大小的簡單流程。 

## 先決條件

在我們深入了解逐步指南之前，請確保您具備以下先決條件：

1.  Aspose.Imaging for .NET：您必須在開發環境中安裝 Aspose.Imaging for .NET 程式庫。如果您還沒有，您可以從以下位置下載[這裡](https://releases.aspose.com/imaging/net/).

2. .NET 開發環境：需要 C# 和 .NET 開發環境的應用知識。

3. DICOM 映像檔：您應該有一個要調整大小的 DICOM 映像檔。如果您需要樣本 DICOM 影像進行測試，您可以輕鬆地在網路上找到一個。

4. Visual Studio（可選）：雖然不是強制性的，但在本教學中使用 Visual Studio 將增強您的開發體驗。

現在，讓我們將調整 DICOM 影像大小的過程分解為簡單、可操作的步驟。

## 第 1 步：導入命名空間

第一步是匯入使用 Aspose.Imaging 所需的命名空間。在您的 C# 專案中，包含以下命名空間：

```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

透過匯入這些命名空間，您可以存取處理 DICOM 影像所需的功能。

## 第 2 步：調整 DICOM 影像大小

現在，讓我們將 DICOM 影像調整大小流程分解為幾個易於管理的步驟。

### 步驟2.1：設定文檔目錄

在 C# 程式碼中，指定 DICOM 檔案所在的目錄。你應該更換`"Your Document Directory"`與檔案目錄的實際路徑。

```csharp
string dataDir = "Your Document Directory";
```

### 步驟2.2：開啟DICOM文件

接下來，使用開啟 DICOM 文件`FileStream`。確保更換`"file.dcm"`與您的 DICOM 檔案的名稱。

```csharp
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
{
    //您的影像處理程式碼位於此處
}
```

### 步驟2.3：載入DICOM影像

從以下位置載入 DICOM 映像`fileStream`。這允許您存取圖像並對其執行操作。

```csharp
using (DicomImage image = new DicomImage(fileStream))
{
    //您的影像處理程式碼位於此處
}
```

### 步驟 2.4：調整 DICOM 影像大小

加載 DICOM 映像後，您現在可以將其調整為所需的尺寸。在此範例中，我們將其大小調整為 200x200 像素。

```csharp
image.Resize(200, 200);
```

### 步驟2.5：儲存調整大小的影像

最後，將調整大小的 DICOM 影像儲存到指定的輸出目錄。在此範例中，我們將其另存為 BMP 檔案。

```csharp
image.Save(dataDir + "DICOMSimpleResizing_out.bmp", new BmpOptions());
```

## 結論

恭喜！您已使用 Aspose.Imaging for .NET 成功調整了 DICOM 影像的大小。透過這些簡單的步驟，您可以有效地處理醫學影像以滿足您的特定要求。

如果您遇到任何問題或對 Aspose.Imaging for .NET 有疑問，請隨時向支援社群尋求協助：[Aspose論壇](https://forum.aspose.com/).

## 常見問題解答

### Q1：什麼是DICOM？

A1：DICOM 代表醫學數位成像和通訊。它是儲存、傳輸和分享醫學影像及相關資訊的標準。

### Q2：我也可以將 Aspose.Imaging 用於其他圖像格式嗎？

A2：是的，Aspose.Imaging for .NET 支援 DICOM 以外的多種影像格式，包括 BMP、JPEG、PNG 等。

### Q3：開啟調整大小的影像是否需要 DICOM 檢視器？

A3：不需要，一旦您使用Aspose.Imaging調整了DICOM圖像的大小，生成的圖像就是標準圖像格式（例如BMP），並且可以使用常見的圖像檢視器來查看。

### Q4：Aspose.Imaging for .NET 是否與所有版本的 .NET Framework 相容？

A4：Aspose.Imaging for .NET 與.NET Framework 的各個版本相容，包括.NET Core 和.NET Standard。請務必檢查文件以了解詳細資訊。

### Q5：在哪裡可以找到更多 Aspose.Imaging for .NET 教學？

 A5：您可以探索[Aspose.Imaging for .NET 文檔](https://reference.aspose.com/imaging/net/)取得廣泛的教學和範例。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
