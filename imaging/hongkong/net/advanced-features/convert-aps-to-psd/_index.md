---
title: 使用 Aspose.Imaging for .NET 將 APS 轉換為 PSD
linktitle: 在 Aspose.Imaging for .NET 中將 APS 轉換為 PSD
second_title: Aspose.Imaging .NET 映像處理 API
description: 使用 Aspose.Imaging for .NET 將 APS 轉換為 PSD。在轉換過程中保留向量屬性。
weight: 11
url: /zh-hant/net/advanced-features/convert-aps-to-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Imaging for .NET 將 APS 轉換為 PSD

您是否希望輕鬆地將 APS 檔案轉換為 PSD 格式，同時保留向量屬性？ Aspose.Imaging for .NET 可以簡化您的任務。在本逐步指南中，我們將向您展示如何實現此轉換。 

## 先決條件

在我們深入了解流程之前，請確保您具備以下先決條件：

1.  Aspose.Imaging for .NET 函式庫：您需要下載並安裝 Aspose.Imaging for .NET 函式庫。您可以從[下載頁面](https://releases.aspose.com/imaging/net/).

2. 您的文件目錄：確保您已準備好文件目錄的路徑。這是 APS 檔案所在的位置。

3. C# 基礎知識：熟悉 C# 程式語言對於實現轉換過程至關重要。

## 導入命名空間

讓我們先匯入必要的命名空間以使用 Aspose.Imaging for .NET。確保您已在專案中新增對 Aspose.Imaging 庫的引用。

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Vectorization;
```

## 第 1 步：載入 APS 文件

首先載入要轉換為 PSD 的 APS 檔案。您也會指定 APS 檔案所在文件目錄的路徑。

```csharp
string dataDir = "Your Document Directory";
string inputFileName = dataDir + "SimpleShapes.cdr";

using (Image image = Image.Load(inputFileName))
{
    //你的程式碼放在這裡
}
```

## 第 2 步：配置轉換選項

在此步驟中，您需要設定將 APS 檔案匯出為 PSD 格式的轉換選項。 Aspose.Imaging 提供了多種向量圖像轉換選項。

```csharp
PsdOptions imageOptions = new PsdOptions()
{
    VectorRasterizationOptions = new VectorRasterizationOptions(),
    VectorizationOptions = new PsdVectorizationOptions()
    {
        VectorDataCompositionMode = VectorDataCompositionMode.SeparateLayers
    }
};

imageOptions.VectorRasterizationOptions.PageWidth = image.Width;
imageOptions.VectorRasterizationOptions.PageHeight = image.Height;
```

## 第 3 步：儲存 PSD 文件

現在，是時候將轉換後的 PSD 檔案儲存到您想要的位置了。

```csharp
image.Save(dataDir + "result.psd", imageOptions);
```

## 第四步：清理

轉換完成後，您可能需要刪除在此過程中建立的臨時 PSD 檔案。

```csharp
File.Delete(dataDir + "result.psd");
```

## 結論

使用 Aspose.Imaging for .NET 將 APS 轉換為 PSD 格式既簡單又有效率。這個強大的程式庫允許您在轉換過程中維護向量屬性，使其成為圖形設計師和開發人員的寶貴工具。

## 常見問題解答

### Q1：Aspose.Imaging for .NET 是免費函式庫嗎？

 A1：Aspose.Imaging for .NET 是一個商業庫。您可以探索授權選項[購買頁面](https://purchase.aspose.com/buy).

### Q2：我可以在購買之前試用 Aspose.Imaging for .NET 嗎？

 A2：是的，您可以從 Aspose.Imaging for .NET 取得免費試用版[試用頁](https://releases.aspose.com/imaging/net/).

### Q3：支援哪些向量影像格式轉換為 PSD？

A3：Aspose.Imaging for .NET支援將CDR、EMF、EPS、ODG、SVG和WMF等向量影像格式轉換為PSD格式。

### Q4：轉換時形狀的複雜度有限制嗎？

A4：目前，Aspose.Imaging 支援匯出沒有紋理畫筆的不太複雜的形狀或帶有描邊的開放形狀。不過，這可能會在即將發布的版本中得到改進。

### Q5：我可以在哪裡獲得與 Aspose.Imaging for .NET 相關的支援或提出問題？

 A5：如果您有任何疑問或需要支持，您可以訪問[Aspose.Imaging 論壇](https://forum.aspose.com/)尋求幫助。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
