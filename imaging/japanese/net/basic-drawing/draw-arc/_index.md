---
date: 2026-02-09
description: Aspose.Imaging for .NET を使用して円弧を描く方法を学び、BMP ファイルの保存、画像サイズの設定、グラフィックの背景設定を含めます。BMP
  画像を生成するためのステップバイステップガイドです。
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: .NET 用 Aspose.Imaging で円弧を描く方法
url: /ja/net/basic-drawing/draw-arc/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET で円弧を描く方法

画像処理の世界では、**円弧の描き方**は、どんなグラフィックにも視覚的なアクセントを加える一般的なタスクです。Aspose.Imaging for .NET を使用すれば、BMP 画像を生成し、画像サイズを設定し、C# の数行でペンを使って円弧を描くことができます。このチュートリアルの最後までに、円弧の描き方、グラフィックの背景設定、そして結果の BMP ファイルを簡単に保存する方法が正確に分かります。

## クイック回答
- **コードは何を生成しますか？** 背景が黄色で黒い円弧が描かれた 100 × 100 ピクセルの BMP 画像です。  
- **使用されているライブラリは？** Aspose.Imaging for .NET。  
- **ライセンスは必要ですか？** 開発には無料トライアルで動作しますが、製品版には商用ライセンスが必要です。  
- **画像サイズを変更できますか？** はい – `Image.Create` 呼び出しの幅と高さのパラメータを変更してください。  
- **出力形式は固定ですか？** この例では BMP ファイルを保存しますが、Aspose.Imaging がサポートする任意の形式を使用できます。

## Aspose.Imaging における「円弧の描き方」とは？

円弧を描くとは、外接矩形、開始角度、掃引角度で定義された曲線セグメントを描画することです。Aspose.Imaging は `Graphics.DrawArc` メソッドを提供しており、**ペンで円弧を描く**ことや、すべての視覚的側面を制御できます。

## このタスクに Aspose.Imaging を使用する理由

- **フルコントロール** 画像の寸法、カラーデプス、ファイル形式に対して。  
- **外部依存なし** – すべて純粋な .NET 上で動作します。  
- **高性能** サーバー側で大量のグラフィックを生成する際に有効です。  

## 前提条件

コードに入る前に、以下が揃っていることを確認してください：

1. **Aspose.Imaging for .NET** – 公式サイトからダウンロードしてください [here](https://releases.aspose.com/imaging/net/)。  
2. **.NET 開発環境**（Visual Studio、VS Code、または任意の C# コンパイラ）。

前提条件が揃ったので、描画を始めましょう！

## 必要な名前空間のインポート

Aspose.Imaging を使用するには、関連する名前空間をスコープに持ち込む必要があります：

### 手順 1: 名前空間のインポート

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

これらの `using` 文により、画像作成、グラフィック処理、ファイル I/O のクラスにアクセスできます。

## Aspose.Imaging for .NET で円弧を描く方法

プロセスは 3 つの明確なステップに分けます：画像の作成、グラフィックサーフェスの準備、そして円弧の描画です。

### 手順 1: 画像の設定（画像サイズの設定と BMP 画像の生成）

```csharp
// Specify the directory where you want to save the image
string dataDir = "Your Document Directory";

// Create an instance of FileStream to save the image
using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
{
    // Create an instance of BmpOptions and set its properties
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;

    // Set the source for BmpOptions and create an instance of Image
    saveOptions.Source = new StreamSource(stream);
    using (Image image = Image.Create(saveOptions, 100, 100))
    {
```

ここでは画像サイズを 100 × 100 ピクセルに **設定**し、BMP オプションを構成しています。`FileStream` は目的の場所に **BMP ファイルを保存**することを保証します。

### 手順 2: Graphics の初期化とグラフィック背景の設定

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

`Graphics` オブジェクトを使用して画像に描画できます。`Clear(Color.Yellow)` を呼び出すことで、背景を明るい黄色に **設定**し、円弧が際立つようにします。

### 手順 3: 円弧パラメータの定義とペンで円弧を描く

```csharp
        // Define the parameters for the arc
        int width = 100;
        int height = 200;
        int startAngle = 45;
        int sweepAngle = 270;

        // Draw the arc
        graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);

        // Save the changes
        image.Save();
    }
    stream.Close();
}
```

- `width` と `height` は外接矩形を定義し、実質的に円弧の **画像サイズを設定**します。  
- `Pen` オブジェクトは、黒で **ペンで円弧を描く**ことを可能にします。  
- 描画後、`image.Save()` が **BMP ファイル** をディスクに書き込みます。

## よくある問題とヒント

- **円弧が見えませんか？** ペンの色が背景とコントラストがあることを確認してください（例: 黄色の上に黒）。  
- **寸法が正しくありませんか？** 円弧の外接矩形は画像より大きくなることがあります。`width`/`height` または画像サイズを適宜調整してください。  
- **パフォーマンスのヒント:** 同じ画像に複数の形状を描く場合は、`Graphics` インスタンスを再利用してください。

## FAQ

### Q1: Aspose.Imaging for .NET のドキュメントはどこで見つけられますか？

A1: Aspose.Imaging for .NET に関する包括的な情報は、ドキュメント [here](https://reference.aspose.com/imaging/net/) を参照してください。

### Q2: Aspose.Imaging for .NET をダウンロードするには？

A2: Aspose.Imaging for .NET はウェブサイト [here](https://releases.aspose.com/imaging/net/) からダウンロードできます。

### Q3: Aspose.Imaging for .NET の無料トライアルはありますか？

A3: はい、無料トライアル版は [here](https://releases.aspose.com/) から入手でき、Aspose.Imaging for .NET を試すことができます。

### Q4: Aspose.Imaging for .NET に一時ライセンスは必要ですか？

A4: 一時ライセンスが必要な場合は、[here](https://purchase.aspose.com/temporary-license/) から取得できます。

### Q5: Aspose.Imaging for .NET のサポートや質問はどこで受けられますか？

A5: サポートやディスカッションは Aspose.Imaging フォーラム [here](https://forum.aspose.com/) をご利用ください。

**最終更新日:** 2026-02-09  
**テスト環境:** Aspose.Imaging 24.11 for .NET  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}