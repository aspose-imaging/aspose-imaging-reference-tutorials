---
title: Aspose.Imaging for .NET でベクター画像をラスター画像に描画する
linktitle: Aspose.Imaging for .NET でベクター画像をラスター画像に描画する
second_title: Aspose.Imaging .NET 画像処理 API
description: Aspose.Imaging を使用して .NET でベクター イメージをラスター イメージに変換する方法を学習します。効率的な画像処理のためのステップバイステップのガイド。
type: docs
weight: 13
url: /ja/net/vector-image-processing/draw-vector-image-to-raster-image/
---

.NET アプリケーションでベクター イメージをラスター イメージに簡単に変換したいと考えていますか? Aspose.Imaging for .NET は、このタスクに対する効率的なソリューションを提供します。このステップバイステップ ガイドでは、Aspose.Imaging for .NET を使用してベクター イメージをラスター イメージに描画するプロセスについて説明します。 

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

### 1. .NET 用の Aspose.Imaging

 Aspose.Imaging for .NET がインストールされている必要があります。お持ちでない場合は、次の Web サイトからダウンロードできます。[.NET 用 Aspose.Imaging をダウンロード](https://releases.aspose.com/imaging/net/).

### 2. .NET開発環境

コンピュータに .NET 開発環境がセットアップされていることを確認してください。 Visual Studio またはその他の .NET 開発ツールを使用できます。

ここで、ベクター イメージをラスター イメージに描画するプロセスを、シンプルでわかりやすい手順に分割してみましょう。

## ステップ 1: プロジェクトを初期化する

まず、開発環境で新しい .NET プロジェクトを作成します。 Aspose.Imaging for .NET がプロジェクトに統合されていることを確認してください。

## ステップ 2: ベクター画像をロードする

このステップでは、ラスター イメージに変換するベクター イメージ (SVG 形式) を読み込みます。

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## ステップ 3: ベクター画像をラスタライズする

次に、SVG 画像を PNG 形式にラスタライズする必要があります。ここで、ベクターからラスターへの変換が行われます。

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## ステップ 4: ラスター画像をロードする

ラスタライズ後、さらに描画するためにストリームから PNG 画像をロードします。

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## ステップ 5: ラスター イメージを描画する

これで、既存の SVG 画像上にラスター画像を描画できるようになりました。

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## ステップ 6: 結果を保存する

最後に、結果の画像を保存します。これで、ベクター画像を含むラスター画像が完成しました。

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## 結論

このチュートリアルでは、Aspose.Imaging for .NET を使用してベクター イメージをラスター イメージに変換する方法を説明しました。これらの簡単な手順を使用すると、この機能を .NET アプリケーションに簡単に統合できます。

### よくある質問

### Aspose.Imaging for .NET とは何ですか?
Aspose.Imaging for .NET は、さまざまな画像形式の操作、画像の変換、高度な画像操作タスクの実行など、強力な画像処理機能を提供する .NET ライブラリです。

### Aspose.Imaging for .NET のドキュメントはどこで見つけられますか?
 Aspose.Imaging for .NET のドキュメントを見つけることができます。[ここ](https://reference.aspose.com/imaging/net/).

### 無料の試用版はありますか?
はい、Aspose.Imaging for .NET の無料トライアルにアクセスできます。[ここ](https://releases.aspose.com/).

### Aspose.Imaging for .NET の一時ライセンスを取得するにはどうすればよいですか?
一時ライセンスが必要な場合は、一時ライセンスを取得できます[ここ](https://purchase.aspose.com/temporary-license/).

### Aspose.Imaging for .NET のサポートはどこで受けられますか?
サポートまたは質問がある場合は、次のサイトにアクセスしてください。[Aspose.Imaging フォーラム](https://forum.aspose.com/).
