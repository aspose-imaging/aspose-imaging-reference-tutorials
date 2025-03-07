---
title: Aspose.Imaging for .NET での DICOM 圧縮
linktitle: Aspose.Imaging for .NET での DICOM 圧縮
second_title: Aspose.Imaging .NET 画像処理 API
description: Aspose.Imaging for .NET を使用して DICOM 圧縮を実行する方法を学習します。このステップバイステップのガイドに従って、高品質の診断品質で医療画像を効率的に保存および送信します。
weight: 17
url: /ja/net/dicom-image-processing/dicom-compression/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET での DICOM 圧縮

医用画像の世界では、DICOM (Digital Imaging and Communications in Medicine) 標準が医用画像の保存と共有にとって最も重要です。強力な .NET ライブラリである Aspose.Imaging for .NET は、DICOM 画像を操作するための包括的なサポートを提供します。このチュートリアルでは、Aspose.Imaging for .NET を使用した DICOM 圧縮のプロセスについて説明します。各ステップに分けて、プロセスを詳しく説明します。

## 前提条件

Aspose.Imaging for .NET を使用した DICOM 圧縮に入る前に、次の前提条件が満たされていることを確認する必要があります。

1. ビジュアルスタジオ

システムに Visual Studio がインストールされていることを確認してください。そうでない場合は、Web サイトからダウンロードできます。

2. .NET 用 Aspose.Imaging

Aspose.Imaging for .NET ライブラリが必要です。このライブラリは、以下のリンクから入手できます。

- [.NET 用 Aspose.Imaging をダウンロード](https://releases.aspose.com/imaging/net/)
- [Aspose.Imaging for .NET を購入する](https://purchase.aspose.com/buy)
- [無料トライアルライセンスを取得する](https://releases.aspose.com/)
- [仮免許](https://purchase.aspose.com/temporary-license/)

これらの前提条件を整えたら、Aspose.Imaging for .NET を使用して DICOM 圧縮を実行する方法に関するステップバイステップ ガイドに進みましょう。

## 名前空間のインポート

先に進む前に、必要なクラスとメソッドにアクセスするために必要な名前空間をインポートする必要があります。 Visual Studio プロジェクトを開き、C# ファイルの先頭に次のコードを追加します。

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

これで、DICOM 圧縮プロセスを開始する準備が整いました。

## ステップ 1: 元の画像をロードする

まず、DICOM 形式に変換する元の画像をロードします。必ず交換してください`"Your Document Directory"`イメージディレクトリへの実際のパスを指定します。

```csharp
string dataDir = "Your Document Directory";
string inputFile = Path.Combine(dataDir, "original.jpg");

using (var inputImage = Image.Load(inputFile))
{
    // DICOM 圧縮のコードはここに入力します。
}
```

## ステップ 2: 非圧縮 DICOM 圧縮を実行する

このステップでは、非圧縮の DICOM 圧縮を実行します。そのコードは次のとおりです。

```csharp
string output1 = Path.Combine(dataDir, "original_Uncompressed.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.None }
};

inputImage.Save(output1, options);
```

## ステップ 3: JPEG DICOM 圧縮を実行する

次に、JPEG 形式を使用した DICOM 圧縮の実行に移りましょう。

```csharp
string output2 = Path.Combine(dataDir, "original_JPEG.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Jpeg }
};

inputImage.Save(output2, options);
```

## ステップ 4: JPEG2000 DICOM 圧縮を実行する

このステップでは、JPEG2000 形式を使用して DICOM 圧縮を実行します。その方法は次のとおりです。

```csharp
string output3 = Path.Combine(dataDir, "original_JPEG2000.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression
    {
        Type = CompressionType.Jpeg2000,
        Jpeg2000 = new Jpeg2000Options
        {
            Codec = Jpeg2000Codec.Jp2,
            Irreversible = false
        }
    }
};

inputImage.Save(output3, options);
```

## ステップ 5: RLE DICOM 圧縮を実行する

最後に、RLE (Run-Length Encoding) 形式を使用して DICOM 圧縮を実行しましょう。

```csharp
string output4 = Path.Combine(dataDir, "original_RLE.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Rle }
};

inputImage.Save(output4, options);
```

## 結論

このステップバイステップ ガイドでは、Aspose.Imaging for .NET を使用して DICOM 圧縮を実行する方法を学習しました。このライブラリは、医療画像を操作するための強力なツールのセットを提供しており、以下を参照してその機能をさらに調べることができます。[ドキュメンテーション](https://reference.aspose.com/imaging/net/).

## よくある質問

### Q1: DICOM圧縮とは何ですか?

A1: DICOM 圧縮は、診断品質を維持しながら医療画像のサイズを縮小するプロセスです。医療データの効率的な保管と送信には不可欠です。

### Q2: DICOM 圧縮に Aspose.Imaging for .NET を使用するのはなぜですか?

A2: Aspose.Imaging for .NET は、DICOM 画像を操作するための堅牢な機能セットとユーザー フレンドリーな API を提供するため、医療画像アプリケーションに最適です。

### Q3: Aspose.Imaging for .NET を使用して、DICOM 圧縮と組み合わせて他の画像処理操作を適用できますか?

A3: はい、Aspose.Imaging for .NET は、特定の要件を満たすために DICOM 圧縮と組み合わせることができる幅広い画像処理機能を提供します。

### Q4: Aspose.Imaging for .NET に関連するサポートや質問はどこで受けられますか?

 A4: にアクセスできます。[Aspose.Imaging フォーラム](https://forum.aspose.com/)サポートを受けたり、質問したり、Aspose.Imaging コミュニティに参加したりできます。

### Q5: テストに利用できる Aspose.Imaging for .NET の試用版はありますか?

 A5: はい、入手できます。[無料トライアルライセンス](https://releases.aspose.com/)購入する前に Aspose.Imaging for .NET をテストしてください。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
