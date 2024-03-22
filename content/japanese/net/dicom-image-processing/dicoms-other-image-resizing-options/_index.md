---
title: Aspose.Imaging for .NET の DICOM のその他の画像サイズ変更オプション
linktitle: Aspose.Imaging for .NET の DICOM のその他の画像サイズ変更オプション
second_title: Aspose.Imaging .NET 画像処理 API
description: Aspose.Imaging for .NET を使用して DICOM 画像のサイズを変更する方法を学びます。効率的な医用画像操作のためのステップバイステップのガイド。
type: docs
weight: 20
url: /ja/net/dicom-image-processing/dicoms-other-image-resizing-options/
---
.NET アプリケーションで DICOM (Digital Imaging and Communications in Medicine) 画像を操作したいと考えていますか? Aspose.Imaging for .NET は、DICOM 画像を効率的に操作するための強力なツール セットを提供します。このチュートリアルでは、Aspose.Imaging for .NET を使用した「DICOM のその他の画像サイズ変更オプション」について詳しく説明します。前提条件を説明し、名前空間をインポートし、DICOM 画像のサイズ変更を効果的に理解して実装するのに役立つステップバイステップのガイドを提供します。

## 前提条件

始める前に、次の前提条件が満たされていることを確認してください。

1. Aspose.Imaging for .NET をインストールする
Aspose.Imaging for .NET を使用して DICOM イメージを操作するには、ライブラリをインストールする必要があります。ウェブサイトからダウンロードできます。

[.NET 用 Aspose.Imaging をダウンロード](https://releases.aspose.com/imaging/net/)

2. 開発環境をセットアップする
Visual Studio またはその他の互換性のある IDE を含む .NET 開発環境がセットアップされていることを確認してください。

3. DICOM画像
Aspose.Imaging for .NET を使用してサイズを変更したい DICOM 画像ファイル (例: 「file.dcm」) が必要です。

## 名前空間のインポート

C# コードでは、Aspose.Imaging を使用するために必要な名前空間をインポートする必要があります。その方法は次のとおりです。

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
```

ここで、画像のサイズ変更プロセスを複数のステップに分けて見てみましょう。

## ステップ 1: DICOM イメージをロードする
まず、ファイル システムから DICOM イメージをロードする必要があります。

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
{
    //コードはここにあります
}
```

## ステップ 2: 高さに比例してサイズを変更する
高さをピクセル単位で指定し、サイズ変更のタイプを指定することで、DICOM 画像のサイズを比例的に変更できます。この例では、サイズ変更タイプとして「AdaptiveResample」を使用します。

```csharp
image.ResizeHeightProportionally(100, ResizeType.AdaptiveResample);
```

## ステップ 3: サイズ変更した画像を保存する
画像のサイズを変更した後、希望の形式で保存できます。ここではBMP画像として保存します。

```csharp
image.Save(dataDir + "DICOMSOtherImageResizingOptions_out.bmp", new BmpOptions());
```

## ステップ 4: 幅に応じてサイズを変更する
幅をピクセル単位で指定し、サイズ変更タイプを指定することで、DICOM 画像を比例的にサイズ変更することもできます。

```csharp
image1.ResizeWidthProportionally(150, ResizeType.AdaptiveResample);
```

## ステップ 5: サイズ変更した画像を保存する
前の手順と同様に、サイズ変更した画像を BMP 画像として保存します。

```csharp
image1.Save(dataDir + "DICOMSOtherImageResizingOptions1_out.bmp", new BmpOptions());
```

おめでとう！ Aspose.Imaging for .NET を使用して DICOM 画像のサイズを変更することに成功しました。このライブラリは、DICOM 画像を操作するためのさまざまなオプションを提供し、ヘルスケアおよび医療画像アプリケーションにとって貴重なツールとなります。

## 結論

このチュートリアルでは、Aspose.Imaging for .NET を使用した「DICOM のその他の画像サイズ変更オプション」を検討しました。前提条件、インポートされた名前空間について説明し、DICOM 画像のサイズを変更するためのステップバイステップのガイドを提供しました。 Aspose.Imaging for .NET は、医療画像を扱うプロセスを簡素化し、医療アプリケーションに幅広い機能を提供します。

Aspose.Imaging for .NET に関してさらに質問がある場合、またはサポートが必要な場合は、ドキュメントを確認するか、サポートについては Aspose コミュニティ フォーラムにアクセスしてください。

- [Aspose.Imaging for .NET ドキュメント](https://reference.aspose.com/imaging/net/)
- [Aspose.Imaging for .NET のサポート](https://forum.aspose.com/)

## よくある質問

### Q1: DICOMとは何ですか?

A1: DICOM は、Digital Imaging and Communications in Medicine の略です。 X 線、MRI、CT スキャンなどの医療画像をデジタル形式で送信、保存、共有するための規格です。

### Q2: Aspose.Imaging for .NET を無料で使用できますか?

A2: Aspose.Imaging for .NET は商用ライブラリです。無料の試用版をダウンロードして機能を評価できますが、完全に使用するにはライセンスが必要です。

### Q3: Aspose.Imaging for .NET は他にどのような画像操作オプションを提供していますか?

A3: Aspose.Imaging for .NET は、形式変換、画像強化、画像上での描画など、幅広い画像処理オプションを提供します。ドキュメントで機能の完全なセットを確認できます。

### Q4: Aspose.Imaging for .NET はヘルスケア アプリケーションに適していますか?

A4: はい。Aspose.Imaging for .NET は、医療アプリケーションで DICOM 画像を処理するためによく使用されており、医療画像ソフトウェア開発にとって貴重なツールとなっています。

### Q5: Aspose.Imaging for .NET の一時ライセンスを取得できますか?
w
 A5: はい、テストと評価の目的で一時ライセンスを取得できます。訪問[Aspose の一時ライセンス ページ](https://purchase.aspose.com/temporary-license/)詳細については。