---
date: 2025-12-20
description: Aspose.Imaging for Java を使用して、TIFF を PNG に変換し、画像を PNG、BMP、または GIF として保存する方法を学びます。画像操作のステップバイステップガイド。
linktitle: Frame Saving in Different Raster Formats
second_title: Aspose.Imaging Java Image Processing API
title: TIFFをPNGに変換し、フレームを異なるラスタ形式で保存する方法
url: /ja/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# TIFF を PNG に変換し、フレームを別々のラスタ形式で保存する方法

マルチページ TIFF ファイルを扱うことは、文書が多いアプリケーションでよくあるシナリオです。**tiff を png に変換**したり、個々のフレームを抽出して他のラスタ形式で保存したりしたい場合、Aspose.Imaging for Java を使えばプロセスがシンプルかつ高速に行えます。このチュートリアルでは、TIFF を読み込み、フレームを順に処理し、各フレームを PNG として保存する手順を詳しく解説します（後から BMP や GIF に簡単に切り替え可能です）。

## Quick Answers
- **「convert tiff to png」とは何ですか？** TIFF ファイルの各ページを抽出し、PNG ラスタ画像として書き出すことを指します。  
- **どのライブラリがこれを処理しますか？** Aspose.Imaging for Java が TIFF フレーム抽出とラスタ形式変換をフルサポートします。  
- **ライセンスは必要ですか？** 開発目的なら無料トライアルで動作しますが、本番環境ではフルライセンスが必要です。  
- **PNG 以外に BMP や GIF で保存できますか？** はい、`PngOptions` を `BmpOptions` または `GifOptions` に置き換えるだけです。  
- **必要な Java のバージョンは？** Java 8 以上を推奨します。

## 「convert tiff to png」とは？
TIFF を PNG に変換するとは、マルチページ TIFF をデコードし、各フレームにアクセスして、そのフレームをロスレスでウェブフレンドリーな PNG 形式にエンコードすることです。

## なぜ Aspose.Imaging for Java を使うのか？
- **幅広い形式サポート** – TIFF、PNG、JPEG、BMP、GIF など多数に対応。  
- **ネイティブ依存なし** – 純粋な Java 実装で、任意の JVM プロジェクトに簡単に組み込めます。  
- **高性能** – 大容量画像やマルチページ文書に最適化。  
- **シンプルな API** – 複雑な変換も最小限のコードで実現可能。

## 前提条件

1. **Java 開発環境** – JDK がインストールされていることを確認してください。未インストールの場合は [Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-downloads) からダウンロードできます。  
2. **Aspose.Imaging for Java ライブラリ** – API リファレンスは [documentation](https://reference.aspose.com/imaging/java/) にあります。ライブラリは [download page](https://releases.aspose.com/imaging/java/) から取得できます。無料トライアルは [here](https://releases.aspose.com/) で、フルライセンスは [here](https://purchase.aspose.com/buy) から購入できます。  
3. **サンプル TIFF 画像** – 処理対象となるマルチページ TIFF を用意してください。

前提条件が整ったら、コードに入りましょう。

## Aspose.Imaging for Java を使って TIFF を PNG に変換する手順

### パッケージのインポート
まず、必要な Aspose.Imaging クラスをインポートします。

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

### 手順 1: TIFF 画像を読み込む
データディレクトリを初期化し、ソース TIFF ファイルをロードします。

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

### 手順 2: フレームを別々のラスタ形式で保存する
各フレームを走査し、**画像を png として保存**します。**tiff を bmp に変換**したり **tiff を gif に変換**したりしたい場合は、`PngOptions` を `BmpOptions` または `GifOptions` に置き換えるだけです。

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **Pro tip:** 示した通り `try‑with‑resources` ブロックを使用すると、処理後に TIFF ファイルが確実に破棄されます。

## 主なユースケース
- **文書アーカイブ:** スキャンした TIFF 文書を PNG に変換し、ウェブプレビュー用に利用。  
- **サムネイル生成:** TIFF の最初のフレームを抽出し、小さな PNG サムネイルとして保存。  
- **形式移行:** レガシーな TIFF 資産を BMP や GIF などのモダン形式に変換し、古いシステムとの互換性を確保。

## トラブルシューティングとヒント
- **フレームが欠落している:** ソース TIFF に複数ページが含まれているか確認し、`multiImage.getFrames().size()` でデバッグしてください。  
- **メモリ不足エラー:** 大きな TIFF は全体をメモリに読み込むのではなく、ページ単位で処理してください。  
- **品質管理:** PNG はロスレスです。ファイルサイズを小さくしたい場合は、品質設定可能な JPEG オプションの使用を検討してください。

## よくある質問

**Q1: Aspose.Imaging for Java でフレーム保存に対応しているラスタ形式は何ですか？**  
A1: PNG、JPEG、BMP、GIF など、幅広いラスタ形式をサポートしています。アプリケーションの要件に合わせて形式を選択できます。

**Q2: Aspose.Imaging for Java で他の画像操作もできますか？**  
A2: はい、リサイズ、クロップ、各種フィルタやエフェクトの適用など、包括的な画像操作機能を提供しています。画像処理全般に対応できる汎用ツールです。

**Q3: Aspose.Imaging for Java のフルライセンスはどうやって取得できますか？**  
A: フルライセンスの購入は [purchase page](https://purchase.aspose.com/buy) から行えます。プロジェクトに合わせたライセンスオプションが用意されています。

**Q4: Aspose.Imaging for Java の無料トライアルはありますか？**  
A: はい、[releases page](https://releases.aspose.com/) から無料トライアルを入手できます。購入前にライブラリの機能を試すことが可能です。

**Q5: Aspose.Imaging for Java のサポートや支援はどこで受けられますか？**  
A: 質問や問題がある場合は、[Aspose Imaging forum](https://forum.aspose.com/) をご利用ください。コミュニティとサポートチームが対応します。

---

**最終更新日:** 2025-12-20  
**テスト環境:** Aspose.Imaging for Java 24.11  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}