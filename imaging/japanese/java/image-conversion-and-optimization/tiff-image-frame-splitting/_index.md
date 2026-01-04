---
date: 2026-01-04
description: Aspose.Imaging for Java を使用してマルチページ TIFF フレームを分割する方法を学びましょう。このステップバイステップガイドでは、前提条件、コード例、開発者向け
  FAQ をカバーしています。
linktitle: TIFF Image Frame Splitting
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java を使用してマルチページ TIFF フレームを分割する
url: /ja/java/image-conversion-and-optimization/tiff-image-frame-splitting/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java を使用したマルチページ TIFF フレームの分割

## はじめに

このチュートリアルでは、Aspose.Imaging for Java を使用して **マルチページ TIFF を分割** する方法を学びます。**Java 画像処理チュートリアル** を作成したり、スキャンした文書から個々のページを抽出したり、単に **TIFF からフレームを抽出** したい場合でも、本ガイドはすべての手順を丁寧に解説します。前提条件の確認、必要なパッケージのインポート、そして Java プロジェクトでマルチページ TIFF ファイルを分割する完全な実行可能サンプルを順に見ていきましょう。

## Quick Answers
- **主な目的は何ですか？** マルチページ TIFF フレームを個別の TIFF ファイルに分割することです。  
- **使用するライブラリは？** Aspose.Imaging for Java。  
- **ライセンスは必要ですか？** トライアル版は利用可能ですが、商用利用には製品ライセンスが必要です。  
- **必要な Java バージョンは？** JDK 8 以上。  
- **コード行数は？** コアの分割ロジックは 30 行未満です。

## 前提条件

Aspose.Imaging for Java を使用する前に、以下の環境が整っていることを確認してください。

### Java 開発環境
マシンにインストールされた最新の JDK（8 以上）。まだインストールしていない場合は、Oracle の公式サイトからダウンロードできます。

### Aspose.Imaging for Java
Aspose.Imaging for Java ライブラリ。入手は [Aspose.Imaging for Java documentation](https://reference.aspose.com/imaging/java/) のページをご参照ください。

### サンプル TIFF 画像
実験用のマルチページ TIFF ファイル。ご自身の画像を使用するか、テスト用にダウンロードしてください。

## パッケージのインポート

前提条件が整ったら、Java プロジェクトに必要なクラスをインポートします。

### 手順 1: Aspose.Imaging JAR をダウンロード

最新の JAR は [Aspose.Imaging for Java download page](https://releases.aspose.com/imaging/java/) から取得してください。

### 手順 2: JAR をプロジェクトに追加

ダウンロードした JAR をプロジェクトのビルドパスに追加します（IDE → Project Structure → Libraries）。

### 手順 3: 必要なクラスをインポート

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.imageoptions.TiffOptions;
```

## マルチページ TIFF フレームの分割方法

以下は **TIFF ファイルを個別ページに分割** する完全なステップバイステップのコード例です。

### 手順 1: プロジェクトの初期化
Aspose.Imaging JAR と上記のインポートがプロジェクトに含まれていることを確認してください。

### 手順 2: TIFF 画像を読み込む
```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Create an instance of TiffImage and load the file from disc
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

`"Your Document Directory"` を TIFF ファイルが格納されている実際のフォルダーに、`"SampleTiff1.tiff"` を処理したいファイル名に置き換えてください。

### 手順 3: フレームを分割して保存
```java
    // Initialize a variable to keep track of the frames in the image
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.tiff", new TiffOptions(TiffExpectedFormat.TiffJpegRgb));
        i++;
    }
}
```

このループは **TIFF からフレームを抽出** し、`0_out.tiff`、`1_out.tiff` … といった個別の TIFF ファイルとして保存します。命名規則や出力形式は、**Java での TIFF 分割** ワークフローに合わせて調整してください。

## よくある問題とヒント

- **ファイルパスエラー:** 絶対パスを使用するか、作業ディレクトリが正しく設定されていることを確認してください。  
- **メモリ消費:** 大容量のマルチページ TIFF はメモリを大量に使用します。上記のようにフレームごとに処理することを推奨します。  
- **出力形式:** `TiffOptions` で圧縮タイプを指定できます。`TiffJpegRgb` は多くのケースでうまく機能します。

## 結論

Aspose.Imaging for Java を使えば、**マルチページ TIFF** ファイルの分割がシンプルに実現できます。複雑なマルチフレーム文書を個別の管理しやすい画像に変換できるため、TIFF 操作を含む **Java 画像処理チュートリアル** の基礎として最適です。さまざまな `TiffOptions` を試したり、バッチ処理パイプラインに組み込んでみてください。

## よくある質問

**Q1: Aspose.Imaging for Java はどこからダウンロードできますか？**  
A1: ダウンロードは [download page](https://releases.aspose.com/imaging/java/) から行えます。

**Q2: Aspose.Imaging for Java は無料で使用できますか？**  
A2: Aspose.Imaging for Java は商用ライブラリです。価格やライセンス情報は [purchase page](https://purchase.aspose.com/buy) で確認してください。

**Q3: 購入前に Aspose.Imaging for Java を試すことはできますか？**  
A3: はい、[trial download page](https://releases.aspose.com/) から無料トライアルを取得できます。

**Q4: Aspose.Imaging for Java に関するサポートやコミュニティディスカッションはどこで行えますか？**  
A4: サポートやディスカッションは [Aspose.Imaging for Java forum](https://forum.aspose.com/) をご利用ください。

**Q5: Aspose.Imaging for Java は TIFF 以外の画像形式もサポートしていますか？**  
A5: はい、JPEG、PNG、BMP など多数の画像形式をサポートしています。

---

**最終更新日:** 2026-01-04  
**テスト環境:** Aspose.Imaging for Java 24.12（執筆時点での最新バージョン）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}