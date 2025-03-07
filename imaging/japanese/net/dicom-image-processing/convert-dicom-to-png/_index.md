---
title: Aspose.Imaging for .NET を使用して DICOM を PNG に変換する
linktitle: Aspose.Imaging for .NET で DICOM を PNG に変換する
second_title: Aspose.Imaging .NET 画像処理 API
description: Aspose.Imaging for .NET を使用して、DICOM を PNG に簡単に変換します。医療画像の共有を合理化します。
weight: 21
url: /ja/net/dicom-image-processing/convert-dicom-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET を使用して DICOM を PNG に変換する

医用画像の世界では、DICOM (Digital Imaging and Communications in Medicine) は医用画像の保存と共有に広く使用されている形式です。ただし、DICOM ファイルを PNG などのより一般的な画像形式に変換する必要がある場合は、Aspose.Imaging for .NET が役に立ちます。このチュートリアルでは、Aspose.Imaging for .NET を使用して DICOM ファイルを PNG に変換するプロセスを説明します。

## 前提条件

変換プロセスに入る前に、次の前提条件を満たしている必要があります。

1.  Aspose.Imaging for .NET: このライブラリがインストールされていることを確認してください。から入手できます。[ダウンロードページ](https://releases.aspose.com/imaging/net/).

2. DICOM ファイル: PNG に変換したい DICOM ファイルを準備します。 DICOM ファイルをお持ちでない場合は、インターネットでサンプル DICOM ファイルを見つけるか、医療画像部門にリクエストしてください。

これらの前提条件が満たされていれば、Aspose.Imaging for .NET を使用して DICOM から PNG への変換を開始する準備が整いました。

## ステップ 1: 名前空間をインポートする

まず、Aspose.Imaging を操作するために必要な名前空間をインポートする必要があります。 C# コードに次の名前空間を含めます。

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
```

## 変換プロセス

ここで、変換プロセスを複数のステップに分けてみましょう。

### ステップ 2.1: DICOM ファイルをロードする

```csharp
string dataDir = "Your Document Directory";
string inputFile = Path.Combine(dataDir, "MultiframePage1.dicom");

using (Aspose.Imaging.FileFormats.Dicom.DicomImage image = (Aspose.Imaging.FileFormats.Dicom.DicomImage)Image.Load(inputFile))
{
    //変換用のコードがここに入力されます。
}
```

このステップでは、DICOM ファイルへのパスを定義し、Aspose.Imaging を使用してそれを読み込みます。

### ステップ 2.2: PNG オプションを構成する

```csharp
PngOptions options = new PngOptions();
```

ここでは、次のインスタンスを作成します。`PngOptions`を使用すると、作成する PNG 画像の設定を指定できます。

### ステップ 2.3: PNG として保存

```csharp
image.Save(dataDir + @"MultiframePage1.png", options);
```

ここで実際の変換が行われます。あなたが使用するのは、`Save`ロードされた DICOM 画像を、指定されたオプションを使用して PNG 画像に変換するメソッド。

### ステップ 2.4: クリーンアップ (オプション)

```csharp
File.Delete(dataDir + "MultiframePage1.png");
```

中間ファイルをクリーンアップしたい場合は、変換プロセス中に作成された PNG ファイルを削除できます。

## 結論

DICOM から PNG への変換は医療分野では一般的なニーズであり、Aspose.Imaging for .NET を使用するとこのタスクが簡素化されます。わずか数行のコードで DICOM ファイルを PNG 形式に変換し、アクセスしやすく共有しやすくします。 Aspose.Imaging for .NET は、.NET アプリケーションでさまざまな画像形式を処理するための強力で柔軟なソリューションを提供します。

 Aspose.Imaging for .NET に関して問題が発生したり質問がある場合は、次のサイトでサポートを求めることができます。[Aspose.Imaging フォーラム](https://forum.aspose.com/).

## よくある質問

### Q1: Aspose.Imaging for .NET は無料で使用できますか?

A1: Aspose.Imaging for .NET は商用ライブラリであり、使用するには有効なライセンスが必要です。を取得できます。[仮免許](https://purchase.aspose.com/temporary-license/)評価目的のため。価格とライセンスの詳細については、次のサイトを参照してください。[購入ページ](https://purchase.aspose.com/buy).

### Q2: 複数の DICOM ファイルをバッチ モードで変換できますか?

A2: はい、Aspose.Imaging for .NET はバッチ処理をサポートしています。複数の DICOM ファイルをループして、一度に PNG に変換できます。

### Q3: DICOM から PNG への変換プロセスに制限はありますか?

A3: 制限がある場合は、DICOM ファイル自体と選択した PNG オプションによって異なります。 Aspose.Imaging for .NET は、さまざまなシナリオを柔軟に処理できますが、詳細は異なる場合があります。

### Q4: 変換プロセス中のエラーはどのように処理すればよいですか?

 A4: C# コードにエラー処理を実装して、例外をキャッチして管理できます。を参照してください。[ドキュメンテーション](https://reference.aspose.com/imaging/net/)詳細なエラー処理ガイドラインについては、こちらを参照してください。

### Q5: DICOM ファイルを PNG 以外の画像形式に変換できますか?

A5: はい、Aspose.Imaging for .NET はさまざまな画像形式をサポートしています。ニーズに応じて、DICOM ファイルを JPEG、BMP、TIFF などの形式に変換できます。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
