---
"date": "2025-06-03"
"description": "掌握使用 Aspose.Imaging .NET 將 SVG 轉換為 PDF 並保持字體品質的方法。學習目錄設定、字體嵌入等。"
"title": "使用 Aspose.Imaging .NET 字體管理和技術實現高效的 SVG 到 PDF 轉換"
"url": "/zh-hant/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 使用 Aspose.Imaging .NET 實現高效的 SVG 到 PDF 轉換

## 介紹

在當今的數位時代，將向量圖形轉換為 PDF 等多功能格式對於文件共享和列印至關重要。在轉換過程中保持字體完整性可能頗具挑戰性。本教學示範如何使用 Aspose.Imaging for .NET 將 SVG 無縫轉換為 PDF，同時保持字體品質。

**您將學到什麼：**
- 設定目錄並將 SVG 檔案匯出為 PDF。
- 在 SVG 檔案中嵌入或匯出字體的技術。
- 實作自訂回呼處理程序以在儲存過程中管理 SVG 字體。

掌握這些技能，您就可以確保您的文件在不同平台上看起來專業且一致。讓我們開始設定環境吧！

## 先決條件

在深入研究程式碼之前，請確保您已具備以下條件：

### 所需庫
- **Aspose.Imaging for .NET**：處理影像轉換不可少。
- **System.IO 命名空間**：用於檔案和目錄操作。

### 環境設定
確保您擁有相容的開發環境，例如 Visual Studio 或任何支援 .NET 專案的 IDE。熟悉基本的 C# 程式設計知識將大有裨益。

## 設定 Aspose.Imaging for .NET

若要在您的專案中使用 Aspose.Imaging，請按照以下安裝步驟操作：

**使用 .NET CLI：**
```bash
dotnet add package Aspose.Imaging
```

**使用套件管理器：**
```powershell
Install-Package Aspose.Imaging
```

**透過 NuGet 套件管理器 UI：**
搜尋“Aspose.Imaging”並安裝最新版本。

### 許可證獲取
- **免費試用**：從免費試用開始測試功能。
- **臨時執照**：取得臨時許可證以進行延長評估。
- **購買**：如果 Aspose.Imaging 滿足您的需求，請考慮購買。

#### 初始化和設定
若要使用 Aspose.Imaging，請將其新增為專案的依賴項。基本設定如下：

```csharp
using Aspose.Imaging;
```

確保 `Aspose.Imaging` 命名空間包含在文件頂部以存取其類別和方法。

## 實施指南

本節將每個功能分解為易於管理的步驟。

### 目錄設定和 SVG 導出為 PDF

#### 概述
將 SVG 檔案轉換為 PDF，同時確保正確設定輸出的目錄路徑。

**步驟 1：確保輸出目錄存在**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*解釋*：此程式碼片段檢查輸出目錄是否存在，並在必要時建立它。

**步驟 2：載入 SVG 並匯出為 PDF**
```csharp
public void ReadAndExportToPdf(string inputFileName)
{
    string inputFile = Path.Combine(SourceFolder, inputFileName);
    string outFile = Path.Combine(OutFolder, inputFileName + ".pdf");
    
    using (Image image = Image.Load(inputFile))
    {
        image.Save(outFile,
            new PdfOptions { VectorRasterizationOptions = new SvgRasterizationOptions { PageSize = image.Size } });
    }
}
```
*解釋*： 這 `PdfOptions` 允許配置 SVG 內容的光柵化，確保頁面大小與原始影像尺寸相符。

### 使用字體嵌入選項儲存 SVG

#### 概述
儲存 SVG 文件，同時控製字體嵌入設定以保持字體保真度。

**步驟 1：定義輸出和字型目錄**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*解釋*：確保在儲存檔案之前設定目錄。

**步驟 2：使用自訂字體選項儲存 SVG**
```csharp
public void Save(bool useEmbedded, string fileName, int expectedCountFonts)
{
    string fontStoreType = useEmbedded ? "Embedded" : "Stream";
    string inputFile = Path.Combine(SourceFolder, fileName);
    string outFileName = $"{Path.GetFileNameWithoutExtension(fileName)}_{fontStoreType}.svg";
    string outputFile = Path.Combine(OutFolder, outFileName);

    using (Image image = Image.Load(inputFile))
    {
        EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions
        {
            BackgroundColor = Color.White,
            PageWidth = image.Width,
            PageHeight = image.Height
        };

        string testingFileName = Path.GetFileNameWithoutExtension(inputFile);
        string fontFolder = Path.Combine(FontFolder, testingFileName);

        image.Save(outputFile,
            new SvgOptions
            {
                VectorRasterizationOptions = emfRasterizationOptions,
                Callback = new SvgCallbackFontTest(useEmbedded, fontFolder)
                {
                    Link = FontFolderName + "/" + testingFileName
                }
            });
    }

    if (!useEmbedded)
    {
        string[] files = Directory.GetFiles(fontFolder);
        if (files.Length != expectedCountFonts)
        {
            throw new Exception($"Expected count font files = {expectedCountFonts}, Current count font files = {files.Length}");
        }
    }
}
```
*解釋*：此方法可讓您指定字體是否應嵌入或串流傳輸，從而影響字體的儲存和存取方式。

### 自訂 SVG 字型回呼處理程序

#### 概述
實作自訂處理程序以在 SVG 保存期間管理字體資源。

**步驟 1：實作 SvgCallbackFontTest 類**
```csharp
public class SvgCallbackFontTest : SvgResourceKeeperCallback
{
    private readonly string outFolder;
    private readonly bool useEmbeddedFont;
    private int fontCounter = 0;

    public string Link { get; set; }

    public SvgCallbackFontTest(bool useEmbeddedFont, string outFolder)
    {
        this.useEmbeddedFont = useEmbeddedFont;
        this.outFolder = outFolder;
        
        if (Directory.Exists(outFolder))
        {
            Directory.Delete(this.outFolder, true);
        }
    }

    public override void OnFontResourceReady(FontStoringArgs args)
    {
        if (this.useEmbeddedFont)
        {
            args.FontStoreType = FontStoreType.Embedded;
        }
        else
        {
            args.FontStoreType = FontStoreType.Stream;
            string fontFolder = this.outFolder;

            if (!Directory.Exists(fontFolder))
            {
                Directory.CreateDirectory(fontFolder);
            }

            string fName = args.SourceFontFileName;
            if (!File.Exists(fName))
            {
                fName = $"font_{this.fontCounter++}.ttf";
            }

            string fileName = Path.Combine(fontFolder, Path.GetFileName(fName));
            
            args.DestFontStream = new FileStream(fileName, FileMode.OpenOrCreate);
            args.DisposeStream = true;
            args.FontFileUri = $".{this.Link}/{Path.GetFileName(fName)}";
        }
    }
}
```
*解釋*：此類處理字體資源，決定直接嵌入或單獨儲存。它確保在 SVG 匯出過程中正確引用和保存字體。

## 實際應用

1. **自動產生報告**：使用 Aspose.Imaging 將設計稿轉換為 PDF 以便進行一致分發。
2. **數位出版**：將嵌入圖形的文章從 SVG 轉換為 PDF 時，確保高品質的字體呈現。
3. **跨平台文件共享**：維護不同作業系統之間共享的文件的視覺完整性。

## 性能考慮

### 優化效能的技巧
- 使用高效率的文件處理方法，例如在使用後及時處理流程。
- 處理完成後，清除未使用的物件和目錄，以最大限度地減少記憶體使用。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}