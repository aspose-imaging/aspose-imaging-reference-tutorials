---
"description": "Aspose.Imaging for .NET を使用して SVG 上にラスター画像を描画する方法を学びます。動的な画像で .NET アプリケーションを強化します。"
"linktitle": "Aspose.Imaging for .NET で SVG にラスター イメージを描画する"
"second_title": "Aspose.Imaging .NET 画像処理 API"
"title": "Aspose.Imaging for .NET で SVG にラスター イメージを描画する方法"
"url": "/ja/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET で SVG にラスター イメージを描画する方法


.NETプログラミングの世界では、Aspose.Imagingは、様々な画像関連タスクを処理するための信頼性と汎用性に優れたライブラリとして知られています。中でも魅力的な機能の一つは、SVGキャンバスにラスター画像を描画できることです。このステップバイステップガイドでは、Aspose.Imaging for .NETを使用してSVGにラスター画像を描画する手順を解説します。

## 前提条件

詳細に入る前に、次の前提条件が満たされていることを確認してください。

- Aspose.Imaging for .NET: ライブラリがインストールされている必要があります。インストールされていない場合は、以下のリンクからダウンロードできます。 [Aspose.Imaging for .NET のダウンロード ページ](https://releases。aspose.com/imaging/net/).

- ドキュメントディレクトリ: 置換 `"Your Document Directory"` 作業ディレクトリへの実際のパスを入力します。

それでは、プロセスをわかりやすい手順に分解してみましょう。

## ステップ1: 必要な名前空間をインポートする

Aspose.Imaging を使用するには、必要な名前空間をインポートする必要があります。

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## ステップ2: 画像を読み込む

- まず、SVG キャンバスに描画するラスター イメージを読み込みます。

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- 次に、ラスター イメージを描画する場所に SVG キャンバス イメージを読み込みます。

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## ステップ3: SVG画像に描画する

これで、既存のSVG画像に描画を開始できます。これを行うには、インスタンスを作成する必要があります。 `SvgGraphics2D`：

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## ステップ4：ラスターイメージを描く

- ラスター イメージを描画する境界を定義し、ラスター イメージからソース領域を指定します。

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## ステップ5: 結果を保存する

SVG キャンバスにラスター イメージを描画した後、結果のイメージを保存できます。

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## 結論

おめでとうございます！Aspose.Imaging for .NET を使って、SVG キャンバスにラスター画像を描画できました。これは、.NET アプリケーション内でリッチでダイナミックな画像を作成するのに非常に役立ちます。

詳しい情報と詳細なドキュメントについては、 [Aspose.Imaging for .NET ドキュメント](https://reference。aspose.com/imaging/net/).

## よくある質問

### Aspose.Imaging for .NET とは何ですか?
   Aspose.Imaging for .NET は、開発者が .NET アプリケーション内でさまざまな形式の画像を作成、操作、変換できるようにする強力な画像処理ライブラリです。

### Aspose.Imaging for .NET を商用プロジェクトで使用できますか?
   はい、Aspose.Imaging for .NETは商用・非商用を問わずご利用いただけます。ライセンスの詳細は、 [購入ページ](https://purchase。aspose.com/buy).

### 無料トライアルはありますか？
   はい、Aspose.Imaging for .NETの無料トライアルは以下から入手できます。 [ここ](https://releases。aspose.com/).

### サポートを受けたり質問したりするにはどこに行けばいいですか?
   ご質問やサポートが必要な場合は、 [Aspose.Imagingフォーラム](https://forum。aspose.com/).

### Aspose.Imaging for .NET の一時ライセンスを取得するにはどうすればよいですか?
   臨時免許証は以下から取得できます。 [ここ](https://purchase。aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}