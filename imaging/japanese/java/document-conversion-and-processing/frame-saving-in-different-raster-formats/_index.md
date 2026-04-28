---
date: 2026-04-28
description: Aspose.Imaging for Java を使用して、TIFF を PNG に変換する方法と、TIFF を他のラスタ形式に変換する方法を学びます。画像操作のステップバイステップガイドです。
keywords:
- tiff to png java
- how to convert tiff
- Aspose.Imaging Java
linktitle: 異なるラスタ形式でのフレーム保存
second_title: Aspose.Imaging Java Image Processing API
title: tiff to png java – TIFF を PNG に変換し、フレームを異なるラスタ形式で保存
url: /ja/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# tiff to png java – TIFF を PNG に変換し、異なるラスタ形式でフレームを保存

マルチページTIFFファイルの取り扱いは、文書中心のアプリケーションで一般的なシナリオです。**convert tiff to png** が必要な場合や、個々のフレームを抽出して他のラスタ形式で保存したい場合、Aspose.Imaging for Java がプロセスをシンプルかつ高性能にします。このチュートリアルでは、TIFF をロードし、フレームを反復処理し、各フレームを PNG として保存する手順を詳しく解説します（後で BMP や GIF に簡単に切り替え可能です）。最後には、数行のコードでサポートされている任意のラスタ形式に **how to convert tiff** できる方法も示します。

## クイック回答
- **What does “convert tiff to png” mean?** それは、TIFF ファイルの各ページを抽出し、PNG ラスタ画像として書き出すことを意味します。  
- **Which library handles this?** Aspose.Imaging for Java は TIFF フレーム抽出とラスタ形式変換をフルサポートします。  
- **Do I need a license?** 開発には無料トライアルで十分ですが、本番環境ではフルライセンスが必要です。  
- **Can I save to BMP or GIF instead of PNG?** はい、`PngOptions` を `BmpOptions` または `GifOptions` に置き換えるだけです。  
- **What Java version is required?** Java 8 以上が推奨されます。

## “convert tiff to png” とは何ですか？
TIFF を PNG に変換するには、マルチページ TIFF をデコードし、各フレームにアクセスし、そのフレームを PNG 形式（ロスレスでウェブフレンドリー、広くサポート）にエンコードします。

## なぜ Aspose.Imaging for Java を使用するのか？
- **Broad format support** – TIFF、PNG、JPEG、BMP、GIF など多数を扱えます。  
- **No native dependencies** – 純粋な Java で、任意の JVM プロジェクトに簡単に統合できます。  
- **High performance** – 大きな画像やマルチページ文書に最適化されています。  
- **Simple API** – 複雑な変換を行うのに必要なコードが最小限です。

## なぜこれが重要なのか
多くのレガシーシステムは、アーカイブに適した形式であるためスキャン文書をマルチページ TIFF として保存しています。一方、最新のウェブやモバイルアプリケーションは、迅速な描画やサムネイル生成のために PNG、BMP、GIF などを好みます。TIFF フレームをリアルタイムで変換することで、ストレージコストを削減し、ロード時間を短縮し、ブラウザやデバイス間の互換性を向上させます。

## 前提条件

1. **Java Development Environment** – JDK がインストールされていることを確認してください。まだの場合は、[Oracle website](https://www.oracle.com/java/technologies/javase-downloads) からダウンロードしてください。  
2. **Aspose.Imaging for Java Library** – API リファレンスは [documentation](https://reference.aspose.com/imaging/java/) で確認できます。ライブラリは [download page](https://releases.aspose.com/imaging/java/) から取得してください。無料トライアルは [here](https://releases.aspose.com/) で利用可能で、フルライセンスは [here](https://purchase.aspose.com/buy) から購入できます。  
3. **Sample TIFF Image** – 処理用のマルチページ TIFF を用意してください。

前提条件が整ったので、コードに入りましょう。

## Aspose.Imaging for Java を使用して TIFF を PNG に変換する方法

### パッケージのインポート
まず、必要な Aspose.Imaging クラスをインポートします。

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

### 手順 1: TIFF 画像のロード
データディレクトリを初期化し、ソース TIFF ファイルをロードします。

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

### 手順 2: 異なるラスタ形式でフレームを保存
各フレームを反復処理し、**save image as png** します。**convert tiff to bmp** や **tiff to gif conversion** を行う場合は、`PngOptions` を `BmpOptions` または `GifOptions` に置き換えるだけです。

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **Pro tip:** `try‑with‑resources` ブロックをそのまま保持し、処理後に TIFF ファイルが適切に破棄されるようにしてください。

## 一般的なユースケース
- **Document archiving:** スキャンした TIFF 文書を PNG に変換し、ウェブプレビュー用に使用します。  
- **Thumbnail generation:** TIFF の最初のフレームを抽出し、小さな PNG サムネイルとして保存します。  
- **Format migration:** レガシーな TIFF 資産を BMP や GIF などのモダンな形式に移行し、古いシステムとの互換性を確保します。

## トラブルシューティングとヒント
- **Missing frames:** ソース TIFF に実際に複数ページが含まれているか確認してください。デバッグには `multiImage.getFrames().size()` を使用します。  
- **Out‑of‑memory errors:** 大きな TIFF をメモリに全体読み込みせず、示したようにページ単位で処理してください。  
- **Quality control:** PNG はロスレスです。より小さいファイルが必要な場合は、品質設定可能な JPEG オプションの使用を検討してください。

## よくある質問

**Q1: What are the supported raster formats for frame saving in Aspose.Imaging for Java?**  
A1: Aspose.Imaging for Java は PNG、JPEG、BMP、GIF など多数のラスタ形式をサポートしています。アプリケーションの要件に最適な形式を選択できます。

**Q2: Can I perform other image operations using Aspose.Imaging for Java?**  
A2: はい、Aspose.Imaging for Java はリサイズ、クロップ、各種フィルタやエフェクトの適用など、画像操作全般の豊富な機能を提供します。あらゆる画像処理ニーズに対応できる汎用ツールです。

**Q3: How can I obtain a full license for Aspose.Imaging for Java?**  
A: フルライセンスの購入は [purchase page](https://purchase.aspose.com/buy) から行えます。プロジェクトに合わせたライセンスオプションが用意されています。

**Q4: Is there a free trial available for Aspose.Imaging for Java?**  
A: はい、[releases page](https://releases.aspose.com/) から無料トライアルを取得でき、ライセンス購入前に機能を試すことができます。

**Q5: Where can I seek support or get assistance with Aspose.Imaging for Java?**  
A: 質問や問題がある場合は、[Aspose Imaging forum](https://forum.aspose.com/) をご利用ください。コミュニティとサポートチームが対応します。

---

**最終更新日:** 2026-04-28  
**テスト済み:** Aspose.Imaging for Java 24.11  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}