---
date: 2026-01-17
description: Aspose.Imaging を使用した Java のメディアンフィルタの使い方を学び、画像ノイズを除去します。このステップバイステップのチュートリアルでは、画像のノイズ除去のためにメディアンフィルタとウィーナーフィルタの適用方法を解説します。
linktitle: Median Filter Java – Apply Median and Wiener Filters
second_title: Aspose.Imaging Java Image Processing API
title: 中央値フィルタ Java – 中央値フィルタとウィーナーフィルタの適用
url: /ja/java/image-processing-and-enhancement/median-and-wiener-filter-application/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Median Filter Java – メディアンフィルタとウィーナーフィルタを適用

画像処理の世界では、ノイズ除去と画像品質の向上は重要な作業です。**median filter java** を使用すれば、Aspose.Imaging for Java を使ってノイズの多い画像を効果的にクリーンアップできます。このチュートリアルでは、画像のノイズ除去のためにメディアンフィルタとウィーナーフィルタを適用する手順を説明しますので、複雑なコードを書かずにプロフェッショナルな結果を得ることができます。

## クイック回答
- **メディアンフィルタは何をしますか？** 各ピクセルを周囲の近傍の中央値に置き換え、インパルスノイズを除去しつつエッジを保持します。  
- **どのライブラリが median filter java をサポートしていますか？** Aspose.Imaging for Java はすぐに使用できる `MedianFilterOptions` クラスを提供します。  
- **コードを実行するのにライセンスは必要ですか？** 評価目的であれば無料トライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **メディアンフィルタを他のフィルタとチェーンできますか？** はい、メディアン処理の後にウィーナーなどの追加フィルタを適用できます。  
- **サポートされている画像フォーマットは何ですか？** ほとんどのラスターフォーマット（PNG、JPEG、BMP、TIFF など）が完全にサポートされています。

## Median Filter Javaとは？

メディアンフィルタは、画像ノイズを**除去**するために一般的に使用される非線形デジタルフィルタリング手法です。Java では、Aspose.Imaging が `MedianFilterOptions` クラスを通じてこのフィルタを実装しており、隣接ピクセルの数を決定するカーネルサイズを指定できます。

## 画像ノイズ除去に Median Filter Java を使用する理由

- **エッジを保持** は単純な平均フィルタより優れています。  
- **Simple API** – 数行のコードで斑点ノイズや塩胡椒ノイズを除去できます。  
- **任意のラスタ画像** に対して Aspose.Imaging でロードでき、サーバーサイド処理に最適です。

## 前提条件

始める前に、以下が揃っていることを確認してください。

1. **Java Development Environment** – JDK 8 以降がインストールされていること。  
2. **Aspose.Imaging for Java** – ライブラリを[here](https://releases.aspose.com/imaging/java/)からダウンロードしてインストールしてください。  
3. **Sample Noisy Image** – クリーンしたい任意の画像；このガイドでは `your‑noisy‑image.png` を使用します。  

## パッケージのインポート

In your Java project, start by importing the necessary Aspose.Imaging classes:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.imagefilters.filteroptions.MedianFilterOptions;
```

## Median Filter Java の適用方法

以下はステップバイステップの手順です。各ステップには簡単な説明と、コピーすべき正確なコードが含まれています。

### 手順 1: ノイズ画像のロード

まず、ノイズ除去したい画像をロードします。これは Aspose.Imaging の `Image.load` メソッドを使用した **load image java** の例です。

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (Image image = Image.load(dataDir + "your-noisy-image.png"))
{
    // Cast the image into RasterImage
    RasterImage rasterImage = (RasterImage) image;
```

### 手順 2: メディアンフィルタの作成と設定

`MedianFilterOptions` のインスタンスを作成し、カーネルサイズを設定します。サイズが大きいほどノイズは多く除去されますが、ディテールがぼやける可能性があります。

```java
    // Create an instance of MedianFilterOptions class and set the size.
    MedianFilterOptions options = new MedianFilterOptions(4);
```

### 手順 3: メディアンフィルタの適用

画像全体の領域にフィルタを適用します。これがコアとなる **apply median filter** 操作です。

```java
    // Apply Median filter to RasterImage object.
    rasterImage.filter(image.getBounds(), options);
```

### 手順 4: 結果画像の保存

最後に、ノイズ除去された画像をディスクに書き出します。これでメディアンフィルタの効果を確認できます。

```java
    // Save the resultant image
    image.save("Your Document Directory" + "denoised-image.png");
}
```

## よくある問題と解決策
- **Kernel size too large** – 画像が過度にぼやけて見えることがあります。ほとんどの写真では 3〜5 の値を試してください。  
- **Unsupported image format** – ファイルが Aspose.Imaging でサポートされているラスターフォーマットであることを確認してください。  
- **OutOfMemoryError** – フィルタ処理前に `RasterImage` の `crop` メソッドを使用して、画像を小さなタイルに分割して処理してください。  

## 結論

このガイドでは、**median filter java** アプローチを使用して画像ファイルの**ノイズ除去方法**を示しました。上記の手順に従うことで、Java ベースの画像処理パイプラインにノイズ除去を迅速に統合でき、ウィーナーフィルタやその他の高度な手法とチェーンして結果をさらに向上させることも可能です。

## よくある質問

**Q1: Aspose.Imaging for Java とは何ですか？**  
A1: Aspose.Imaging for Java は、開発者が画像を操作し、さまざまな画像処理タスクをプログラムで実行できる Java ライブラリです。

**Q2: Aspose.Imaging for Java を無料で使用できますか？**  
A2: Aspose.Imaging for Java は商用ライブラリですが、[here](https://releases.aspose.com/) から無料トライアル版を入手できます。ただし、長期的に使用する場合は、[here](https://purchase.aspose.com/buy) からライセンスを購入する必要があります。

**Q3: Aspose.Imaging for Java のサポートはどうすれば受けられますか？**  
A3: Aspose.Imaging コミュニティやエキスパートに、[Aspose.Imaging Forum](https://forum.aspose.com/) で問い合わせることで支援を受けられます。

**Q4: 他にどんな画像強調技術がありますか？**  
A4: メディアンフィルタに加えて、ウィーナーフィルタ、ガウシアンブラー、コントラストストレッチングなどの画像強調技術があります。

**Q5: Aspose.Imaging for Java をウェブアプリケーションで使用できますか？**  
A5: はい、Aspose.Imaging for Java をウェブアプリケーションに組み込んでサーバーサイドの画像処理を行うことができます。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2026-01-17  
**テスト環境:** Aspose.Imaging for Java 24.11  
**作者:** Aspose