---
title: Aspose.Imaging for .NET で SVG 上にラスター イメージを描画する方法
linktitle: Aspose.Imaging for .NET で SVG 上にラスター イメージを描画する
second_title: Aspose.Imaging .NET 画像処理 API
description: Aspose.Imaging for .NET を使用して SVG 上にラスター イメージを描画する方法を学びます。動的なイメージを使用して .NET アプリケーションを強化します。
type: docs
weight: 11
url: /ja/net/vector-image-processing/draw-raster-image-on-svg/
---

.NET プログラミングの世界では、Aspose.Imaging は、さまざまな画像関連のタスクを処理するための信頼できる多用途ライブラリとして機能します。それが提供する魅力的な機能の 1 つは、SVG キャンバス上にラスター イメージを描画する機能です。このステップバイステップ ガイドでは、Aspose.Imaging for .NET を使用して SVG 上にラスター イメージを描画するプロセスを説明します。

## 前提条件

詳細に入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.Imaging for .NET: ライブラリがインストールされている必要があります。そうでない場合は、からダウンロードできます。[Aspose.Imaging for .NET ダウンロード ページ](https://releases.aspose.com/imaging/net/).

- ドキュメント ディレクトリ: 置換`"Your Document Directory"`作業ディレクトリへの実際のパスを指定します。

ここで、プロセスをわかりやすい手順に分割してみましょう。

## ステップ 1: 必要な名前空間をインポートする

Aspose.Imaging を使用するには、必要な名前空間をインポートする必要があります。

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## ステップ 2: 画像をロードする

- まず、SVGキャンバスに描画したいラスター画像を読み込みます。

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- 次に、ラスター画像を描画したい場所にSVGキャンバス画像を読み込みます。

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## ステップ 3: SVG 画像上に描画する

これで、既存の SVG 画像上で描画を開始できます。これを行うには、次のインスタンスを作成する必要があります。`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## ステップ 4: ラスター イメージを描画する

- ラスター イメージを描画する境界を定義し、ラスター イメージからソース領域を指定します。

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## ステップ 5: 結果を保存する

SVG キャンバスにラスター イメージを描画した後、結果のイメージを保存できます。

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## 結論

おめでとう！ Aspose.Imaging for .NET を使用して、SVG キャンバスにラスター イメージを描画することに成功しました。これは、.NET アプリケーション内でリッチで動的なイメージを作成する場合に非常に役立ちます。

詳細と詳細なドキュメントについては、次のサイトを参照してください。[Aspose.Imaging for .NET ドキュメント](https://reference.aspose.com/imaging/net/).

## よくある質問

### Aspose.Imaging for .NET とは何ですか?
   Aspose.Imaging for .NET は、開発者が .NET アプリケーション内でさまざまな形式の画像を作成、操作、変換できるようにする強力な画像処理ライブラリです。

### Aspose.Imaging for .NET を商用プロジェクトで使用できますか?
   はい、Aspose.Imaging for .NET は商用プロジェクトと非商用プロジェクトの両方で使用できます。ライセンスの詳細については、[購入ページ](https://purchase.aspose.com/buy).

### 無料トライアルはありますか?
   はい、Aspose.Imaging for .NET の無料トライアルを次のサイトから入手できます。[ここ](https://releases.aspose.com/).

### どこでサポートを受けたり、質問したりできますか?
   ご質問がある場合、またはサポートが必要な場合は、次のサイトにアクセスしてください。[Aspose.Imaging フォーラム](https://forum.aspose.com/).

### Aspose.Imaging for .NET の一時ライセンスを取得するにはどうすればよいですか?
   一時ライセンスは次から取得できます。[ここ](https://purchase.aspose.com/temporary-license/).


