---
date: 2026-01-09
description: Aspose.Imaging for Java を使用して画像を二値化する方法を学びましょう。このガイドでは、DICOM から BMP への変換に関する画像処理の
  Java テクニックを取り上げています。
linktitle: Bradley's Adaptive Threshold Binarization
second_title: Aspose.Imaging Java Image Processing API
title: Java 用 Aspose.Imaging で画像を二値化する方法
url: /ja/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java を使用した画像の二値化方法

画像はウェブサイト、文書、さまざまなアプリケーションの中で重要な役割を果たしています。特に **画像を二値化する方法** を効率的に知りたい場合や、医療フォーマットである DICOM などを扱う場合は、ここが最適な場所です。画像の二値化は、画像を白黒の表現に変換し、下流の分析、OCR、または保存の最適化に最適です。このチュートリアルでは、Aspose.Imaging for Java の Bradley の適応的閾値二値化を使用して、プロセス全体を順を追って説明します。

## クイック回答
- **二値化は何をしますか？** 閾値に基づいて各ピクセルを黒または白に変換します。  
- **Java の画像処理に最適なライブラリはどれですか？** Aspose.Imaging for Java は堅牢で、ライセンスフリーのトライアル機能を提供します。  
- **DICOM ファイルを直接処理できますか？** はい、Aspose.Imaging は DICOM を読み込み、BMP、PNG などに出力できます。  
- **本番環境でライセンスが必要ですか？** トライアル以外の使用には商用ライセンスが必要です。  
- **サポートされている Java バージョンは何ですか？** Java 8 以降が完全に互換性があります。

## 画像二値化とは？
画像二値化は、グレースケールまたはカラー画像を各ピクセルが 0（黒）または 255（白）のいずれかになる二値画像に変換するプロセスです。このステップは、医療画像処理パイプライン、文書スキャン、コンピュータビジョンのタスクの最初の段階としてよく使用されます。

## なぜ Aspose.Imaging for Java を使用するのか？
Aspose.Imaging は純粋な Java API を提供し、**DICOM をロード**し、**Bradley の適応的閾値**などの高度なアルゴリズムを適用し、外部のネイティブライブラリを必要とせずに一般的なフォーマットで保存できます。**医療画像処理**、**DICOM を BMP に変換**、およびその他の Java ベースのワークフローに最適です。

## 前提条件

コードに入る前に、以下が揃っていることを確認してください。

- **Java 開発環境** – JDK 8 以上がインストールされていること。  
- **Aspose.Imaging for Java** – 公式サイトからダウンロード: [Aspose.Imaging for Java をダウンロード](https://releases.aspose.com/imaging/java/)。  
- **DICOM 画像** – 二値化したい任意のサンプル DICOM ファイル。

すべて準備できたので、実装に進みましょう。

## 画像を二値化する方法 – ステップバイステップガイド

### パッケージのインポート
まず、必要な Aspose.Imaging クラスをインポートします。このスニペットは入力および出力ファイルパスも定義しています。

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// Load a DICOM image in an instance of DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Binarize image with Bradley's adaptive threshold.
    image.binarizeBradley(10);
    // Save the resultant image.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

### 手順 1: パスの定義
ソース DICOM ファイルと出力 BMP ファイルの場所を設定します。`"Your Document Directory"` を実際のフォルダーに置き換えてください。

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

### 手順 2: DICOM 画像の読み込み
Aspose.Imaging を使用して **dicom 画像をロード**し、`DicomImage` オブジェクトに格納します。このオブジェクトにより、ピクセルデータや処理メソッドへフルアクセスが可能です。

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // The image processing steps will go here.
}
```

### 手順 3: 二値化の実行
Bradley の適応的閾値アルゴリズムを適用します。パラメータ（この例では `10`）は閾値の感度を制御します。最適な結果が得られるよう、まざまな値で実験してみてください。

```java
image.binarizeBradley(10);
```

### 手順 4: 二値化画像の保存
最後に、処理済み画像をエクスポートします。ここでは BMP 形式を使用していますが、Aspose.Imaging は PNG、JPEG、TIFF など多数の形式をサポートしています。

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## よくある問題とトラブルシューティング

- **FileNotFoundException** – `dataDir` パスがスラッシュで終わっていること、DICOM ファイル名が正確に一致していることを確認してください。  
- **OutOfMemoryError** – 大きな DICOM ファイルの場合、JVM ヒープサイズ（`-Xmx2g` 以上）を増やす必要があるかもしれません。  
- **Incorrect Threshold** – 出力が暗すぎるまたは明るすぎる場合、`binarizeBradley()` に渡す整数値（例: 5‑15）を調整してください。

## よくある質問

### Q1: DICOM とは何か、医療画像でなぜ重要なのか？
**A:** DICOM は Digital Imaging and Communications in Medicine の略で、医療画像の保存、送信、取り扱いのための汎用標準です。デバイスやシステム間の相互運用性を実現します。

### Q2: 商用プロジェクトで Aspose.Imaging for Java を使用できますか？
**A:** はい、Aspose.Imaging for Java は無料トライアルと商用ライセンスの両方を提供しています。必要なライセンスは [Aspose のウェブサイト](https://purchase.aspose.com/buy) から取得できます。

### Q3: テスト目的の一時ライセンスはありますか？
**A:** はい、テストおよび評価用の一時ライセンスを取得できます。詳細は [このリンク](https://purchase.aspose.com/temporary-license/) でご確認ください。

### Q4: Aspose.Imaging for Java に関するサポートや議論はどこでできますか？
**A:** コミュニティサポートやディスカッションは、[Aspose.Imaging フォーラム](https://forum.aspose.com/) で行えます。質問への回答や他のユーザーとの交流に最適です。

### Q5: 他の Java ベースのアプリケーションでの画像処理に Aspose.Imaging for Java は適していますか？
**A:** 全くその通りです。このライブラリはウェブアプリケーション、デスクトップソフトウェア、バッチ処理ツールなど、さまざまな環境で一貫した API を提供し、画像処理を容易にします。

## 結論
これで **画像を二値化する方法** を Aspose.Imaging for Java の Bradley の適応的閾値を使って学びました。この手法は特に **医療画像処理** に有用で、DICOM ファイルを軽量な BMP（または他の形式）に変換して分析や保存に活用できます。さまざまな閾値で試行し、Aspose.Imaging の豊富な機能セットもぜひ探ってみてください。

画像操作の詳細については、公式ドキュメントをご覧ください: [Aspose.Imaging for Java ドキュメント](https://reference.aspose.com/imaging/java/)。

---

**最終更新日:** 2026-01-09  
**テスト環境:** Aspose.Imaging for Java 24.12（執筆時点での最新バージョン）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}