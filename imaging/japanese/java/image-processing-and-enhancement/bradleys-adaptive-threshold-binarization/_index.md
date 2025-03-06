---
title: Aspose.Imaging for Java による画像の二値化
linktitle: Bradley の適応しきい値二値化
second_title: Aspose.Imaging Java 画像処理 API
description: Aspose.Imaging for Java を使用して画像の二値化を学習します。 DICOM 画像を簡単に変換します。コード例を含むステップバイステップのガイドを参照してください。
weight: 27
url: /ja/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java による画像の二値化

Web サイト、ドキュメント、さまざまなアプリケーションの一部など、デジタル世界では画像が重要な役割を果たします。これらの分野では画像処理が不可欠なタスクであり、基本的な操作の 1 つが画像の 2 値化です。 2 値化は、画像を 2 値形式に変換することで単純化し、コンピューターでの処理を容易にします。 Aspose.Imaging for Java は、幅広い画像操作機能を提供する強力なツールです。このチュートリアルでは、Aspose.Imaging の Bradley の Adaptive Threshold Binarization を使用して画像の 2 値化を実行する方法を検討します。 

## 前提条件

Aspose.Imaging for Java を使用した画像二値化の世界に飛び込む前に、必要なものがすべて揃っていることを確認してください。

### Java開発環境

システム上に Java 開発環境がセットアップされている必要があります。 Java Development Kit (JDK) をまだダウンロードしていない場合は、Oracle Web サイトからダウンロードしてインストールできます。

### Java 用 Aspose.Imaging

このチュートリアルを進めるには、Aspose.Imaging for Java がインストールされている必要があります。次のリンクを使用して、Aspose Web サイトからダウンロードできます。[Java 用 Aspose.Imaging をダウンロード](https://releases.aspose.com/imaging/java/).

### DICOM 画像

2値化したいDICOM画像が必要です。お持ちでない場合は、オンラインで DICOM 画像サンプルを見つけるか、独自の DICOM 画像を使用できます。

前提条件が整ったので、次のステップに進みましょう。

## パッケージのインポート

このセクションでは、Aspose.Imaging for Java から必要なパッケージをインポートします。これらのパッケージには、DICOM 画像に対して Bradley の適応しきい値二値化を実行するために必要なクラスとメソッドが含まれています。

```java
//ドキュメントディレクトリへのパス。
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// DICOMImage のインスタンスに DICOM 画像をロードします
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    //Bradley の適応しきい値を使用して画像を 2 値化します。
    image.binarizeBradley(10);
    //結果の画像を保存します。
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

## ステップ 1: パスを定義する

まず、入力 DICOM 画像と出力 2 値化画像のパスを定義します。交換する`"Your Document Directory"`ディレクトリへの実際のパスを使用します。

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

## ステップ 2: DICOM イメージをロードする

Aspose.Imaging を使用して、指定された DICOM イメージをロードします。`inputFile` 。この操作により、`DicomImage`クラス。

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    //ここからは画像処理の手順を進めていきます。
}
```

## ステップ 3: 2 値化を実行する

ロードされた DICOM 画像に対して Bradley の適応しきい値二値化を実行します。この例では、しきい値は`10`が適用されます。

```java
image.binarizeBradley(10);
```

## ステップ 4: バイナリ化された画像を保存する

結果の 2 値化イメージを、BMP 形式を使用して指定した出力ファイルに保存します。

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## 結論

おめでとう！ Bradley の Adaptive Threshold Binarization を使用して、Aspose.Imaging for Java で画像の 2 値化を実行する方法を学習しました。この強力なツールを使用すると、画像処理機能を強化できるため、さまざまなアプリケーションで貴重な資産になります。

より多くの画像処理の可能性については、Aspose.Imaging の広範なドキュメントを忘れずに参照してください。[Aspose.Imaging for Java ドキュメント](https://reference.aspose.com/imaging/java/).

## よくある質問

### Q1: DICOM とは何ですか?また、医療画像処理において DICOM が重要なのはなぜですか?

A1: DICOM は、Digital Imaging and Communications in Medicine の略で、医療画像および関連情報の標準形式です。これは医療画像の保存、交換、解釈において重要な役割を果たしており、医療専門家や医療画像システムにとって不可欠なものとなっています。

### Q2: Aspose.Imaging for Java を商用プロジェクトで使用できますか?

 A2: はい、Aspose.Imaging for Java は無料試用版と商用ライセンスの両方を提供しています。オプションを検討し、必要なライセンスを取得できます。[アスポセのウェブサイト](https://purchase.aspose.com/buy).

### Q3: テスト目的で利用できる一時ライセンスはありますか?

 A3: はい、Aspose.Imaging for Java をテストおよび評価するための一時ライセンスを取得できます。訪問[このリンク](https://purchase.aspose.com/temporary-license/)詳細については。

### Q4: Aspose.Imaging for Java に関連する問題について、どこに助けを求めたり議論したりできますか?

 A4: コミュニティのサポートとディスカッションについては、次のサイトにアクセスしてください。[Aspose.Imaging フォーラム](https://forum.aspose.com/)。質問に対する答えを見つけたり、他のユーザーとつながるのに最適な場所です。

### Q5: Aspose.Imaging for Java は、他の Java ベースのアプリケーションでの画像処理に適していますか?

A5: はい、Aspose.Imaging for Java は多用途であり、Web アプリケーション、デスクトップ ソフトウェアなどを含むさまざまな Java ベースのアプリケーションで使用できます。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
