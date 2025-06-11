---
"description": "Aspose.Imaging for .NET を使えば、DICOM を PNG に簡単に変換できます。医療画像の共有を効率化します。"
"linktitle": "Aspose.Imaging for .NET で DICOM を PNG に変換する"
"second_title": "Aspose.Imaging .NET 画像処理 API"
"title": "Aspose.Imaging for .NET で DICOM を PNG に変換する"
"url": "/ja/net/dicom-image-processing/convert-dicom-to-png/"
"weight": 21
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET で DICOM を PNG に変換する

医用画像の世界では、DICOM（Digital Imaging and Communications in Medicine）は医用画像の保存と共有に広く使用されているフォーマットです。しかし、DICOMファイルをPNGなどのより一般的な画像形式に変換する必要がある場合、Aspose.Imaging for .NETが役立ちます。このチュートリアルでは、Aspose.Imaging for .NETを使用してDICOMファイルをPNGに変換する手順を説明します。

## 前提条件

変換プロセスに進む前に、次の前提条件を満たす必要があります。

1. Aspose.Imaging for .NET: このライブラリがインストールされていることを確認してください。 [ダウンロードページ](https://releases。aspose.com/imaging/net/).

2. DICOMファイル：PNGに変換したいDICOMファイルを用意してください。DICOMファイルをお持ちでない場合は、インターネットでサンプルのDICOMファイルを探すか、医療画像部門に依頼してください。

これらの前提条件が満たされれば、Aspose.Imaging for .NET を使用して DICOM から PNG への変換を開始する準備が整います。

## ステップ1: 名前空間をインポートする

まず、Aspose.Imaging を使用するために必要な名前空間をインポートする必要があります。C# コードに以下の名前空間を含めます。

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
```

## 変換プロセス

ここで、変換プロセスを複数のステップに分解してみましょう。

### ステップ2.1: DICOMファイルを読み込む

```csharp
string dataDir = "Your Document Directory";
string inputFile = Path.Combine(dataDir, "MultiframePage1.dicom");

using (Aspose.Imaging.FileFormats.Dicom.DicomImage image = (Aspose.Imaging.FileFormats.Dicom.DicomImage)Image.Load(inputFile))
{
    // 変換用のコードをここに入力します。
}
```

この手順では、DICOM ファイルへのパスを定義し、Aspose.Imaging を使用して読み込みます。

### ステップ2.2: PNGオプションを設定する

```csharp
PngOptions options = new PngOptions();
```

ここで、インスタンスを作成します `PngOptions`では、作成する PNG 画像の設定を指定できます。

### ステップ2.3: PNGとして保存

```csharp
image.Save(dataDir + @"MultiframePage1.png", options);
```

ここで実際の変換が行われます。 `Save` 読み込まれた DICOM 画像を指定されたオプションを使用して PNG 画像に変換するメソッド。

### ステップ 2.4: クリーンアップ (オプション)

```csharp
File.Delete(dataDir + "MultiframePage1.png");
```

中間ファイルをクリーンアップしたい場合は、変換プロセス中に作成された PNG ファイルを削除できます。

## 結論

DICOMからPNGへの変換は医療分野ではよくあるニーズですが、Aspose.Imaging for .NETはこのタスクを簡素化します。わずか数行のコードでDICOMファイルをPNG形式に変換できるため、アクセスしやすく共有しやすくなります。Aspose.Imaging for .NETは、.NETアプリケーションで様々な画像形式を扱うための強力で柔軟なソリューションを提供します。

Aspose.Imaging for .NET に関して問題や質問がある場合は、 [Aspose.Imagingフォーラム](https://forum。aspose.com/).

## よくある質問

### Q1: Aspose.Imaging for .NET は無料で使用できますか?

A1: Aspose.Imaging for .NETは商用ライブラリであり、使用するには有効なライセンスが必要です。 [一時ライセンス](https://purchase.aspose.com/temporary-license/) 評価目的でのみご利用いただけます。価格とライセンスの詳細については、 [購入ページ](https://purchase。aspose.com/buy).

### Q2: 複数の DICOM ファイルをバッチモードで変換できますか?

A2: はい、Aspose.Imaging for .NET はバッチ処理をサポートしています。複数の DICOM ファイルをループ処理して、一度に PNG に変換できます。

### Q3: DICOM から PNG への変換プロセスには制限がありますか?

A3: 制限事項は、DICOMファイル自体と選択したPNGオプションによって異なります。Aspose.Imaging for .NETは様々なシナリオに対応できる柔軟性を備えていますが、具体的な内容は異なる場合があります。

### Q4: 変換プロセス中にエラーが発生した場合、どのように処理すればよいですか?

A4: C#コードにエラー処理を実装することで、例外をキャッチして管理することができます。 [ドキュメント](https://reference.aspose.com/imaging/net/) 詳細なエラー処理ガイドラインについては、こちらをご覧ください。

### Q5: DICOM ファイルを PNG 以外の画像形式に変換できますか?

A5: はい、Aspose.Imaging for .NET は様々な画像形式をサポートしています。DICOM ファイルを、ニーズに応じて JPEG、BMP、TIFF などの形式に変換できます。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}