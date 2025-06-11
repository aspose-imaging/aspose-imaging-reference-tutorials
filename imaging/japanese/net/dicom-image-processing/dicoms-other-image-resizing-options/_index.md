---
"description": "Aspose.Imaging for .NET を使用してDICOM画像のサイズを変更する方法を学びましょう。効率的な医療画像操作のためのステップバイステップガイドです。"
"linktitle": "Aspose.Imaging for .NET における DICOM のその他の画像サイズ変更オプション"
"second_title": "Aspose.Imaging .NET 画像処理 API"
"title": "Aspose.Imaging for .NET における DICOM のその他の画像サイズ変更オプション"
"url": "/ja/net/dicom-image-processing/dicoms-other-image-resizing-options/"
"weight": 20
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET における DICOM のその他の画像サイズ変更オプション

.NETアプリケーションでDICOM（Digital Imaging and Communications in Medicine：医療におけるデジタル画像と通信）画像を扱いたいとお考えですか？Aspose.Imaging for .NETは、DICOM画像を効率的に操作するための強力なツールセットを提供します。このチュートリアルでは、Aspose.Imaging for .NETを用いた「DICOMのその他の画像サイズ変更オプション」について詳しく解説します。前提条件、名前空間のインポート方法、そしてDICOM画像のサイズ変更を効果的に理解し実装するためのステップバイステップガイドを提供します。

## 前提条件

始める前に、次の前提条件が満たされていることを確認してください。

1. Aspose.Imaging for .NET をインストールする
Aspose.Imaging for .NET を使用してDICOM画像を扱うには、ライブラリをインストールする必要があります。ライブラリはウェブサイトからダウンロードできます。

[Aspose.Imaging for .NET をダウンロード](https://releases.aspose.com/imaging/net/)

2. 開発環境をセットアップする
Visual Studio やその他の互換性のある IDE を含む .NET 開発環境が設定されていることを確認してください。

3. DICOM画像
Aspose.Imaging for .NET を使用してサイズを変更する DICOM 画像ファイル (例: 「file.dcm」) が必要です。

## 名前空間のインポート

C#コードでは、Aspose.Imagingを使用するために必要な名前空間をインポートする必要があります。手順は以下のとおりです。

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
```

ここで、画像のサイズ変更プロセスを複数のステップに分解してみましょう。

## ステップ1: DICOM画像を読み込む
まず、ファイル システムから DICOM イメージをロードする必要があります。

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
{
    // ここにあなたのコード
}
```

## ステップ2: 高さに比例してサイズを変更する
DICOM画像のサイズを比例的に変更するには、高さ（ピクセル単位）とサイズ変更の種類を指定します。この例では、サイズ変更の種類として「AdaptiveResample」を使用します。

```csharp
image.ResizeHeightProportionally(100, ResizeType.AdaptiveResample);
```

## ステップ3: サイズ変更した画像を保存する
画像のサイズを変更したら、希望の形式で保存できます。ここではBMP画像として保存します。

```csharp
image.Save(dataDir + "DICOMSOtherImageResizingOptions_out.bmp", new BmpOptions());
```

## ステップ4: 幅に比例してサイズを変更する
ピクセル単位での幅とサイズ変更のタイプを指定して、DICOM 画像のサイズを比例的に変更することもできます。

```csharp
image1.ResizeWidthProportionally(150, ResizeType.AdaptiveResample);
```

## ステップ5: サイズ変更した画像を保存する
前の手順と同様に、サイズ変更した画像を BMP 画像として保存します。

```csharp
image1.Save(dataDir + "DICOMSOtherImageResizingOptions1_out.bmp", new BmpOptions());
```

おめでとうございます！Aspose.Imaging for .NET を使用して DICOM 画像のサイズを変更できました。このライブラリは DICOM 画像を操作するさまざまなオプションを提供しており、医療・医用画像処理アプリケーションにとって貴重なツールとなります。

## 結論

このチュートリアルでは、Aspose.Imaging for .NET を使用して「DICOM のその他の画像サイズ変更オプション」について解説しました。前提条件、名前空間のインポート、そして DICOM 画像のサイズ変更に関するステップバイステップのガイドを提供しました。Aspose.Imaging for .NET は、医療画像の操作プロセスを簡素化し、ヘルスケアアプリケーション向けの幅広い機能を提供します。

Aspose.Imaging for .NET についてご質問やサポートが必要な場合は、ドキュメントをご覧いただくか、Aspose コミュニティ フォーラムでサポートを受けてください。

- [Aspose.Imaging for .NET ドキュメント](https://reference.aspose.com/imaging/net/)
- [Aspose.Imaging for .NET サポート](https://forum.aspose.com/)

## よくある質問

### Q1: DICOM とは何ですか?

A1: DICOMはDigital Imaging and Communications in Medicine（医療におけるデジタル画像と通信）の略称です。X線、MRI、CTスキャンなどの医療画像をデジタル形式で伝送、保存、共有するための規格です。

### Q2: Aspose.Imaging for .NET は無料で使用できますか?

A2: Aspose.Imaging for .NETは商用ライブラリです。機能を評価するには無料試用版をダウンロードできますが、フル機能を使用するにはライセンスが必要です。

### Q3: Aspose.Imaging for .NET では他にどのような画像操作オプションが提供されていますか?

A3: Aspose.Imaging for .NET は、フォーマット変換、画像の補正、画像への描画など、幅広い画像処理オプションを提供します。すべての機能については、ドキュメントをご覧ください。

### Q4: Aspose.Imaging for .NET はヘルスケア アプリケーションに適していますか?

A4: はい、Aspose.Imaging for .NET は DICOM 画像を処理する医療アプリケーションでよく使用されているため、医療用画像処理ソフトウェア開発にとって貴重なツールとなっています。

### Q5: Aspose.Imaging for .NET の一時ライセンスを取得できますか?
わ
A5: はい、テストや評価目的で一時的なライセンスを取得することができます。 [Aspose の一時ライセンスページ](https://purchase.aspose.com/temporary-license/) 詳細についてはこちらをご覧ください。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}