---
"date": "2025-06-03"
"description": "Aspose.Imaging .NET を使って、フォントの品質を保ちながら SVG から PDF への変換をマスターしましょう。ディレクトリの設定、フォントの埋め込みなど、様々な方法を学習します。"
"title": "Aspose.Imaging .NET のフォント管理とテクニックを使用した効率的な SVG から PDF への変換"
"url": "/ja/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging .NET を使用した効率的な SVG から PDF への変換

## 導入

ベクターグラフィックをPDFなどの汎用フォーマットに変換することは、今日のデジタル時代においてドキュメントの共有や印刷に不可欠です。しかし、この変換中にフォントの整合性を維持するのは容易ではありません。このチュートリアルでは、Aspose.Imaging for .NETを使用して、フォントの品質を維持しながらSVGからPDFへのシームレスな変換を行う方法を紹介します。

**学習内容:**
- ディレクトリを設定し、SVG ファイルを PDF としてエクスポートします。
- SVG ファイル内にフォントを埋め込んだりエクスポートしたりするテクニック。
- 保存プロセス中に SVG フォントを管理するためのカスタム コールバック ハンドラーを実装します。

これらのスキルを身に付ければ、ドキュメントの見栄えをプロフェッショナルに保ち、異なるプラットフォーム間で一貫性を保つことができます。まずは環境設定から始めましょう！

## 前提条件

コードに進む前に、次のものを用意してください。

### 必要なライブラリ
- **Aspose.Imaging .NET 版**画像変換の処理に不可欠です。
- **System.IO 名前空間**ファイルおよびディレクトリの操作用。

### 環境設定
Visual Studioや.NETプロジェクトをサポートするIDEなど、互換性のある開発環境があることを確認してください。基本的なC#プログラミングの知識があれば有利です。

## Aspose.Imaging for .NET のセットアップ

プロジェクトで Aspose.Imaging を使用するには、次のインストール手順に従います。

**.NET CLI の使用:**
```bash
dotnet add package Aspose.Imaging
```

**パッケージマネージャーの使用:**
```powershell
Install-Package Aspose.Imaging
```

**NuGet パッケージ マネージャー UI 経由:**
「Aspose.Imaging」を検索し、最新バージョンをインストールします。

### ライセンス取得
- **無料トライアル**無料トライアルで機能を試してみましょう。
- **一時ライセンス**拡張評価用の一時ライセンスを取得します。
- **購入**Aspose.Imaging がニーズを満たす場合は、購入を検討してください。

#### 初期化とセットアップ
Aspose.Imagingを使用するには、プロジェクトに依存関係として追加します。基本的な設定は次のとおりです。

```csharp
using Aspose.Imaging;
```

確実に `Aspose.Imaging` クラスとメソッドにアクセスするために、ファイルの先頭に名前空間が含まれます。

## 実装ガイド

このセクションでは、各機能を管理しやすい手順に分解します。

### ディレクトリの設定とSVGからPDFへのエクスポート

#### 概要
出力用のディレクトリ パスが正しく設定されていることを確認しながら、SVG ファイルを PDF に変換します。

**ステップ1: 出力ディレクトリが存在することを確認する**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*説明*このコード スニペットは、出力ディレクトリが存在するかどうかを確認し、必要に応じて作成します。

**ステップ2: SVGを読み込み、PDFにエクスポートする**
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
*説明*：その `PdfOptions` SVG コンテンツのラスタライズを構成して、ページ サイズが元の画像の寸法と一致するようにします。

### フォント埋め込みオプション付きSVG保存

#### 概要
フォントの忠実度を維持するためにフォント埋め込み設定を制御しながら SVG ファイルを保存します。

**ステップ1: 出力ディレクトリとフォントディレクトリを定義する**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*説明*ファイルを保存する前にディレクトリが設定されていることを確認してください。

**ステップ2: カスタムフォントオプションでSVGを保存する**
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
*説明*このメソッドを使用すると、フォントを埋め込むかストリーミングするかを指定して、フォントの保存方法とアクセス方法を決めることができます。

### カスタム SVG フォント コールバック ハンドラー

#### 概要
SVG の保存中にフォント リソースを管理するためのカスタム ハンドラーを実装します。

**ステップ1: SvgCallbackFontTestクラスを実装する**
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
*説明*このクラスは、フォントリソースを直接埋め込むか、別途保存するかを決定することで、フォントリソースを処理します。これにより、SVGエクスポートプロセス中にフォントが正しく参照され、保存されることが保証されます。

## 実用的なアプリケーション

1. **自動レポート生成**Aspose.Imaging を使用して、設計ドラフトを PDF に変換し、一貫した配布を実現します。
2. **デジタル出版**埋め込みグラフィックを含む記事を SVG から PDF に変換するときに、高品質のフォント レンダリングを保証します。
3. **クロスプラットフォームドキュメント共有**異なるオペレーティング システム間で共有されるドキュメントの視覚的な整合性を維持します。

## パフォーマンスに関する考慮事項

### パフォーマンスを最適化するためのヒント
- 使用後はすぐにストリームを破棄するなど、効率的なファイル処理方法を使用します。
- 処理が完了したら、未使用のオブジェクトとディレクトリをクリアして、メモリ使用量を最小限に抑えます。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}