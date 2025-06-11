---
"date": "2025-06-03"
"description": "掌握使用 Aspose.Imaging .NET 将 SVG 转换为 PDF 并保持字体质量的方法。学习目录设置、字体嵌入等。"
"title": "使用 Aspose.Imaging .NET 字体管理和技术实现高效的 SVG 到 PDF 转换"
"url": "/zh/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 使用 Aspose.Imaging .NET 实现高效的 SVG 到 PDF 转换

## 介绍

在当今的数字时代，将矢量图形转换为 PDF 等多功能格式对于文档共享和打印至关重要。在转换过程中保持字体完整性可能颇具挑战性。本教程演示了如何使用 Aspose.Imaging for .NET 将 SVG 无缝转换为 PDF，同时保持字体质量。

**您将学到什么：**
- 设置目录并将 SVG 文件导出为 PDF。
- 在 SVG 文件中嵌入或导出字体的技术。
- 实现自定义回调处理程序以在保存过程中管理 SVG 字体。

掌握这些技能，您就可以确保您的文档在不同平台上看起来专业且一致。让我们开始设置环境吧！

## 先决条件

在深入研究代码之前，请确保您已具备以下条件：

### 所需库
- **Aspose.Imaging for .NET**：处理图像转换必不可少。
- **System.IO 命名空间**：用于文件和目录操作。

### 环境设置
确保您拥有兼容的开发环境，例如 Visual Studio 或任何支持 .NET 项目的 IDE。熟悉基本的 C# 编程知识将大有裨益。

## 设置 Aspose.Imaging for .NET

要在您的项目中使用 Aspose.Imaging，请按照以下安装步骤操作：

**使用 .NET CLI：**
```bash
dotnet add package Aspose.Imaging
```

**使用包管理器：**
```powershell
Install-Package Aspose.Imaging
```

**通过 NuGet 包管理器 UI：**
搜索“Aspose.Imaging”并安装最新版本。

### 许可证获取
- **免费试用**：从免费试用开始测试功能。
- **临时执照**：获取临时许可证以进行延长评估。
- **购买**：如果 Aspose.Imaging 满足您的需求，请考虑购买。

#### 初始化和设置
要使用 Aspose.Imaging，请将其添加为项目的依赖项。基本设置如下：

```csharp
using Aspose.Imaging;
```

确保 `Aspose.Imaging` 命名空间包含在文件顶部以访问其类和方法。

## 实施指南

本节将每个功能分解为易于管理的步骤。

### 目录设置和 SVG 导出为 PDF

#### 概述
将 SVG 文件转换为 PDF，同时确保正确设置输出的目录路径。

**步骤 1：确保输出目录存在**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*解释*：此代码片段检查输出目录是否存在，并在必要时创建它。

**步骤 2：加载 SVG 并导出为 PDF**
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
*解释*： 这 `PdfOptions` 允许配置 SVG 内容的光栅化，确保页面大小与原始图像尺寸相匹配。

### 使用字体嵌入选项保存 SVG

#### 概述
保存 SVG 文件，同时控制字体嵌入设置以保持字体保真度。

**步骤 1：定义输出和字体目录**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*解释*：确保在保存文件之前设置目录。

**步骤 2：使用自定义字体选项保存 SVG**
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
*解释*：此方法允许您指定字体是否应嵌入或流式传输，从而影响字体的存储和访问方式。

### 自定义 SVG 字体回调处理程序

#### 概述
实现自定义处理程序以在 SVG 保存期间管理字体资源。

**步骤 1：实现 SvgCallbackFontTest 类**
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
*解释*：此类处理字体资源，决定是直接嵌入还是单独存储。它确保在 SVG 导出过程中正确引用和保存字体。

## 实际应用

1. **自动生成报告**：使用 Aspose.Imaging 将设计稿转换为 PDF 以便进行一致分发。
2. **数字出版**：将嵌入图形的文章从 SVG 转换为 PDF 时，确保高质量的字体呈现。
3. **跨平台文档共享**：维护不同操作系统之间共享的文档的视觉完整性。

## 性能考虑

### 优化性能的技巧
- 使用高效的文件处理方法，例如在使用后及时处理流。
- 处理完成后，清除未使用的对象和目录，以最大限度地减少内存使用。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}