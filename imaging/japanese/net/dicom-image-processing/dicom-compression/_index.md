---
"description": "Aspose.Imaging for .NET を使用してDICOM圧縮を実行する方法を学びましょう。このステップバイステップガイドに従って、高い診断品質の医療画像を効率的に保存・転送しましょう。"
"linktitle": "Aspose.Imaging for .NET における DICOM 圧縮"
"second_title": "Aspose.Imaging .NET 画像処理 API"
"title": "Aspose.Imaging for .NET における DICOM 圧縮"
"url": "/ja/net/dicom-image-processing/dicom-compression/"
"weight": 17
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET における DICOM 圧縮

医用画像の世界では、DICOM（Digital Imaging and Communications in Medicine：医療におけるデジタル画像と通信）規格が医用画像の保存と共有において極めて重要です。強力な.NETライブラリであるAspose.Imaging for .NETは、DICOM画像の操作を包括的にサポートします。このチュートリアルでは、Aspose.Imaging for .NETを用いたDICOM圧縮のプロセスを解説します。各ステップを細かく分解し、プロセスを詳細に解説します。

## 前提条件

Aspose.Imaging for .NET を使用した DICOM 圧縮について説明する前に、次の前提条件が満たされていることを確認する必要があります。

1. ビジュアルスタジオ

システムにVisual Studioがインストールされていることを確認してください。インストールされていない場合は、ウェブサイトからダウンロードできます。

2. Aspose.Imaging .NET 版

Aspose.Imaging for .NET ライブラリが必要です。このライブラリは、以下のリンクから入手できます。

- [Aspose.Imaging for .NET をダウンロード](https://releases.aspose.com/imaging/net/)
- [Aspose.Imaging for .NET を購入](https://purchase.aspose.com/buy)
- [無料トライアルライセンスを入手する](https://releases.aspose.com/)
- [一時ライセンス](https://purchase.aspose.com/temporary-license/)

これらの前提条件が整ったら、Aspose.Imaging for .NET を使用して DICOM 圧縮を実行する方法についてのステップバイステップ ガイドに進みましょう。

## 名前空間のインポート

先に進む前に、必要なクラスとメソッドにアクセスするために必要な名前空間をインポートする必要があります。Visual Studioプロジェクトを開き、C#ファイルの先頭に以下のコードを追加してください。

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

これで、DICOM 圧縮プロセスを開始する準備が整いました。

## ステップ1：元の画像を読み込む

まず、DICOM形式に変換したい元の画像を読み込みます。 `"Your Document Directory"` 画像ディレクトリへの実際のパスを入力します。

```csharp
string dataDir = "Your Document Directory";
string inputFile = Path.Combine(dataDir, "original.jpg");

using (var inputImage = Image.Load(inputFile))
{
    // DICOM 圧縮のコードをここに記述します。
}
```

## ステップ2: 非圧縮DICOM圧縮を実行する

このステップでは、非圧縮のDICOM圧縮を実行します。コードは次のとおりです。

```csharp
string output1 = Path.Combine(dataDir, "original_Uncompressed.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.None }
};

inputImage.Save(output1, options);
```

## ステップ3: JPEG DICOM圧縮を実行する

次に、JPEG 形式を使用して DICOM 圧縮を実行する手順に進みます。

```csharp
string output2 = Path.Combine(dataDir, "original_JPEG.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Jpeg }
};

inputImage.Save(output2, options);
```

## ステップ4: JPEG2000 DICOM圧縮を実行する

このステップでは、JPEG2000形式を使用してDICOM圧縮を実行します。手順は以下のとおりです。

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

## ステップ5: RLE DICOM圧縮を実行する

最後に、RLE (Run-Length Encoding) 形式を使用して DICOM 圧縮を実行します。

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

このステップバイステップガイドでは、Aspose.Imaging for .NETを使用してDICOM圧縮を行う方法を学習しました。このライブラリは、医用画像を扱うための強力なツールセットを提供します。詳細については、 [ドキュメント](https://reference。aspose.com/imaging/net/).

## よくある質問

### Q1: DICOM 圧縮とは何ですか?

A1: DICOM圧縮とは、診断品質を維持しながら医用画像のサイズを縮小するプロセスです。医療データの効率的な保存と伝送に不可欠です。

### Q2: DICOM 圧縮に Aspose.Imaging for .NET を使用する理由は何ですか?

A2: Aspose.Imaging for .NET は、DICOM 画像を操作するための強力な機能セットとユーザーフレンドリーな API を提供するため、医療用画像処理アプリケーションに最適です。

### Q3: Aspose.Imaging for .NET を使用して、DICOM 圧縮と組み合わせて他の画像処理操作を適用できますか?

A3: はい、Aspose.Imaging for .NET は、特定の要件を満たすために DICOM 圧縮と組み合わせることができる幅広い画像処理機能を提供します。

### Q4: Aspose.Imaging for .NET に関するサポートや質問はどこで受けられますか?

A4: [Aspose.Imaging フォーラム](https://forum.aspose.com/) サポートを受けたり、質問したり、Aspose.Imaging コミュニティに参加したりできます。

### Q5: テスト用に利用できる Aspose.Imaging for .NET の試用版はありますか?

A5: はい、取得できます [無料試用ライセンス](https://releases.aspose.com/) 購入前に Aspose.Imaging for .NET をテストできます。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}