---
title: Aspose.Imaging for .NET を使用して DICOM 画像をトリミングする
linktitle: Aspose.Imaging for .NET のシフトによる DICOM クロップ
second_title: Aspose.Imaging .NET 画像処理 API
description: Aspose.Imaging for .NET を使用して DICOM 画像をトリミングする方法を学びます。このステップバイステップのガイドを使用して、医療画像処理を強化します。
weight: 18
url: /ja/net/dicom-image-processing/dicom-cropping-by-shifts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET を使用して DICOM 画像をトリミングする

医療画像、特に DICOM 画像のトリミングは、医療業界では重要な作業です。これにより、医療専門家は特定の関心領域に焦点を当て、不要な要素を削除し、診断データの視覚的表現を強化できます。このチュートリアルでは、.NET アプリケーションでの画像処理タスクを簡素化する強力なライブラリである Aspose.Imaging for .NET を使用して DICOM 画像をトリミングする方法を検討します。

## 前提条件

DICOM トリミング プロセスに入る前に、次の前提条件が満たされていることを確認する必要があります。

1. .NET開発環境

Visual Studio またはその他の任意の .NET IDE を含む、動作する .NET 開発環境が必要です。

2. .NET ライブラリ用の Aspose.Imaging

必ず Aspose.Imaging for .NET をダウンロードしてインストールしてください。ライブラリは Aspose Web サイトから入手できます。[ここ](https://releases.aspose.com/imaging/net/).

3. DICOM画像

トリミングしたい DICOM 画像が必要です。お持ちでない場合は、テスト用のサンプル DICOM 画像をオンラインで見つけることができます。

4. C# の基礎知識

このチュートリアルは、C# プログラミングの基本を理解していることを前提としています。

すべての前提条件が準備できたので、Aspose.Imaging for .NET を使用して DICOM 画像をトリミングする手順に進みましょう。

## 名前空間のインポート

まず、Aspose.Imaging を使用するために必要な名前空間をインポートする必要があります。

```csharp
using System;
using System.IO;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.FileFormats.Bmp;
```

## ステップ 1: DICOM イメージをロードする

このステップでは、ファイルから DICOM 画像をロードします。

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
{
    //コードはここに入力します
}
```

## ステップ 2: DICOM 画像をトリミングする

このステップでは、`Crop`メソッドを選択し、4 つの値を指定してトリミング領域を定義します。ここ、`1, 1, 1, 1`をサンプル値として使用します。これらの値を、トリミングに使用する実際の座標と寸法に置き換える必要があります。

```csharp
image.Crop(1, 1, 1, 1);
```

## ステップ 3: 切り取った画像を保存する

画像をトリミングしたら、希望の形式でディスクに保存できます。この例では、BMP 画像として保存していますが、必要に応じて別の形式を選択することもできます。

```csharp
image.Save(dataDir + "DICOMCroppingByShifts_out.bmp", new BmpOptions());
```

これで、Aspose.Imaging for .NET を使用して DICOM 画像が切り取られました。さらに、このコードを .NET アプリケーションに統合して医療画像処理を行うことができます。

## 結論

DICOM 画像のトリミングは医療画像処理の重要な部分であり、医療専門家が関心のある特定の領域に集中できるようになります。 Aspose.Imaging for .NET はこのプロセスを簡素化し、DICOM 画像を効率的にトリミングすることを容易にします。

 Aspose.Imaging for .NET とその機能について詳しく知りたい場合は、ドキュメントを参照してください。[ここ](https://reference.aspose.com/imaging/net/). 

## よくある質問

### Q1: DICOM画像フォーマットとは何ですか?

A1: DICOM は、Digital Imaging and Communications in Medicine の略です。 X 線、MRI、CT スキャンなどの医療画像を保存および送信するための標準です。

### Q2: Aspose.Imaging を他の画像処理タスクに使用できますか?

A2: はい、Aspose.Imaging for .NET は、形式変換やサイズ変更などのさまざまな画像処理タスクを処理できる多用途ライブラリです。

### Q3: Aspose.Imaging for .NET のライセンス オプションはありますか?

 A3: はい、Aspose.Imaging for .NET のライセンスは次のサイトから取得できます。[ここ](https://purchase.aspose.com/buy) 。評価目的の一時ライセンスも提供しています[ここ](https://purchase.aspose.com/temporary-license/).

### Q4: Aspose.Imaging for .NET のサポートはどこで受けられますか?

 A4: 次の URL で、Aspose.Imaging for .NET に関するサポートを求めたり、ディスカッションに参加したりできます。[アスペスフォーラム](https://forum.aspose.com/).

### Q5: Aspose.Imaging for .NET を医療以外の画像処理アプリケーションで使用できますか?

A5：もちろんです！ Aspose.Imaging for .NET は医療画像処理に最適ですが、さまざまなドメインの幅広い画像処理タスクに使用できます。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
