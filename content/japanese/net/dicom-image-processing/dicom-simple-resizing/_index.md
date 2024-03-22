---
title: Aspose.Imaging for .NET を使用して DICOM 画像のサイズを変更する
linktitle: Aspose.Imaging for .NET での DICOM の単純なサイズ変更
second_title: Aspose.Imaging .NET 画像処理 API
description: 医療画像処理用の強力なツールである Aspose.Imaging for .NET を使用して DICOM 画像のサイズを変更する方法を学びます。シンプルな手順で正確な結果が得られます。
type: docs
weight: 19
url: /ja/net/dicom-image-processing/dicom-simple-resizing/
---
進化し続ける医用画像処理の分野では、DICOM (Digital Imaging and Communications in Medicine) ファイルを処理する際の柔軟性と精度の必要性が最も重要です。 Aspose.Imaging for .NET は強力なソリューションとして登場し、医療画像を操作するための包括的なツール セットを提供します。このチュートリアルでは、Aspose.Imaging for .NET を使用して DICOM 画像のサイズを変更する簡単なプロセスを説明します。 

## 前提条件

ステップバイステップのガイドに進む前に、次の前提条件が満たされていることを確認してください。

1.  Aspose.Imaging for .NET: 開発環境に Aspose.Imaging for .NET ライブラリがインストールされている必要があります。まだダウンロードしていない場合は、からダウンロードできます[ここ](https://releases.aspose.com/imaging/net/).

2. .NET 開発環境: C# および .NET 開発環境に関する実践的な知識が必要です。

3. DICOM 画像ファイル: サイズを変更したい DICOM 画像ファイルが必要です。テスト用のサンプル DICOM イメージが必要な場合は、オンラインで簡単に見つけることができます。

4. Visual Studio (オプション): 必須ではありませんが、このチュートリアルで Visual Studio を使用すると、開発エクスペリエンスが向上します。

ここで、DICOM 画像のサイズを変更するプロセスを、シンプルで実用的な手順に分けてみましょう。

## ステップ 1: 名前空間をインポートする

最初のステップは、Aspose.Imaging を操作するために必要な名前空間をインポートすることです。 C# プロジェクトに、次の名前空間を含めます。

```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

これらの名前空間をインポートすると、DICOM 画像の処理に必要な機能にアクセスできるようになります。

## ステップ 2: DICOM 画像のサイズ変更

ここで、DICOM 画像のサイズ変更プロセスをいくつかの管理可能なステップに分割してみましょう。

### ステップ 2.1: ドキュメント ディレクトリを設定する

C# コードで、DICOM ファイルが存在するディレクトリを指定します。交換する必要があります`"Your Document Directory"`ファイルディレクトリへの実際のパスを使用します。

```csharp
string dataDir = "Your Document Directory";
```

### ステップ 2.2: DICOM ファイルを開く

次に、次のコマンドを使用して DICOM ファイルを開きます。`FileStream` 。必ず交換してください`"file.dcm"`DICOM ファイルの名前に置き換えます。

```csharp
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
{
    //画像処理のコードはここに入れます
}
```

### ステップ 2.3: DICOM 画像をロードする

DICOM 画像を`fileStream`。これにより、イメージにアクセスして操作を実行できるようになります。

```csharp
using (DicomImage image = new DicomImage(fileStream))
{
    //画像処理のコードはここに入れます
}
```

### ステップ 2.4: DICOM 画像のサイズを変更する

DICOM 画像をロードしたら、希望のサイズにサイズ変更できるようになります。この例では、200x200 ピクセルにサイズ変更します。

```csharp
image.Resize(200, 200);
```

### ステップ 2.5: サイズ変更した画像を保存する

最後に、サイズ変更した DICOM 画像を指定した出力ディレクトリに保存します。この例では、BMP ファイルとして保存しています。

```csharp
image.Save(dataDir + "DICOMSimpleResizing_out.bmp", new BmpOptions());
```

## 結論

おめでとう！ Aspose.Imaging for .NET を使用して DICOM 画像のサイズを変更することに成功しました。これらの簡単な手順で、医療画像を効率的に操作して特定の要件を満たすことができます。

 Aspose.Imaging for .NET に関して問題が発生したり質問がある場合は、遠慮せずに次のサポート コミュニティに助けを求めてください。[アスペス フォーラム](https://forum.aspose.com/).

## よくある質問

### Q1: DICOMとは何ですか?

A1: DICOM は、Digital Imaging and Communications in Medicine の略です。これは、医療画像と関連情報を保存、送信、共有するための標準です。

### Q2: Aspose.Imaging は他の画像形式にも使用できますか?

A2: はい、Aspose.Imaging for .NET は、BMP、JPEG、PNG など、DICOM 以外の幅広い画像形式をサポートしています。

### Q3: サイズ変更された画像を開くには DICOM ビューアが必要ですか?

A3: いいえ、Aspose.Imaging を使用して DICOM 画像のサイズを変更すると、結果の画像は標準画像形式 (BMP など) になり、一般的な画像ビューアで表示できます。

### Q4: Aspose.Imaging for .NET は、.NET Framework のすべてのバージョンと互換性がありますか?

A4: Aspose.Imaging for .NET は、.NET Core や .NET Standard を含む、.NET Framework のさまざまなバージョンと互換性があります。詳細についてはドキュメントを必ずご確認ください。

### Q5: Aspose.Imaging for .NET チュートリアルの詳細はどこで見つけられますか?

 A5: を探索できます。[Aspose.Imaging for .NET ドキュメント](https://reference.aspose.com/imaging/net/)幅広いチュートリアルと例をご覧ください。