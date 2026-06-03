---
date: 2026-01-09
description: Aspose.Imaging for Java を使用して画像に透かしを追加する方法を学びましょう。この Java 画像処理チュートリアルでは、対角線上の透かしを素早く作成する手順をステップバイステップで示します。
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: 透かしの追加方法 – 斜め画像透かし (Java)
url: /ja/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 透かしの追加方法 – 斜め画像透かし (Java)

画像にスタイリッシュな斜め方向の **透かしを追加する方法** を探しているなら、Aspose.Imaging for Java が手間なく実現します。このステップバイステップのチュートリアルでは、JPG（またはサポートされている任意の形式）の画像に 45 度回転したテキスト透かしを追加する手順を解説します。Java の達人である必要はありません – 各ブロックは平易な言葉で説明しているので、数分で結果を再現できます。

## クイック回答
- **使用ライブラリは？** Aspose.Imaging for Java  
- **対象の主要キーワードは？** how to add watermark  
- **サポートされている画像形式は？** JPEG、PNG、BMP、TIFF、GIF など多数  
- **必要なコード量は？** たった 7 つの簡潔なコードブロック  
- **テストにライセンスは必要？** 無料トライアルが利用可能；本番環境ではライセンスが必要  

## 画像処理における「透かしの追加」とは？
透かしを追加するとは、所有権保護やブランディングのために、画像上に半透明のテキストやグラフィックを重ねることです。斜めの透かしは画像全体に広がり、切り取られにくいため特に効果的です。

## Aspose.Imaging for Java を選ぶ理由
Aspose.Imaging は低レベルのピクセル操作を抽象化したハイレベル API を提供し、数十種類のフォーマットをサポート、あらゆる Java ランタイムで動作します。画像フォーマット固有の問題を気にせず、*斜め透かしの追加* といった目的に集中できます。

## 前提条件

作業を始める前に以下を用意してください。

1. **Aspose.Imaging for Java** – 公式サイト **[こちら](https://releases.aspose.com/imaging/java/)** から最新バージョンをダウンロード。  
2. **Java 開発環境** – JDK 8 以上とお好みの IDE（IntelliJ、Eclipse、VS Code など）。  
3. **透かしを付ける画像** – サンプルの JPG/TIFF/PNG をコードで参照するフォルダーに配置。

## パッケージのインポート

まず、必要なクラスをインポートします。インポートをまとめておくとコードが読みやすく、保守もしやすくなります。

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## 手順 1: 既存画像の読み込み

ソース画像を読み込みます。`Image.load` メソッドはフォーマットを自動判別します。

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **プロのコツ:** `Image` オブジェクトを try‑with‑resources ブロックで囲む（下記参照）ことで、メモリリークを防ぎ自動的に破棄されます。

## 手順 2: 透かしテキストとグラフィックの準備

ロードした画像に紐付く `Graphics` オブジェクトを作成し、後の計算に使う画像サイズを取得します。

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## 手順 3: フォントとブラシの定義

目立つフォントと、透かしの色・不透明度を決めるブラシを選びます。不透明度を調整して半透明にします。

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## 手順 4: テキストの書式設定

テキストを描画する際に中央揃えになるよう、配置フラグと書式フラグを設定します。

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## 手順 5: 変換の適用

変換行列を使って原点を画像の中心に移動し、‑45°（時計回り）に回転させます。

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## 手順 6: 描画と保存

文字列を画像に描画し、結果をディスクに書き出します。

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

`AddDiagonalWatermarkToImage_out.jpg` を開くと、画像の中心を斜めに横切る赤い半透明テキストが表示されます。

## よくある問題と対策

| 問題 | 原因 | 対策 |
|------|------|------|
| 透かしが薄すぎる | 不透明度が 0（完全に透明）に設定されている | 不透明度を上げる例: `brush.setOpacity(0.5f);` |
| テキストが端で切れる | 非正方形画像で平行移動が中心に合わせられていない | 表示例のように `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` を使用し、必要に応じて回転角度を調整 |
| 未サポート形式エラー | 古い Aspose.Imaging バージョンを使用している | 最新の Aspose.Imaging リリースに更新 |

## FAQ（よくある質問）

### Q1: Aspose.Imaging for Java は初心者に向いていますか？

**A:** はい！ API は直感的で、ドキュメントも分かりやすい例を提供しています。画像処理が初めての開発者でも本チュートリアルに従えば、すぐにプロフェッショナルな結果が得られます。

### Q2: 透かしのテキストやスタイルはカスタマイズできますか？

**A:** 可能です。`theString` 変数を変更したり、別の `Font` を選んだり、`brush.setColor(...)` で色を変えたり、行列の回転角度を調整したりして、ブランドに合わせたデザインにできます。

### Q3: JPG 以外の画像形式もサポートしていますか？

**A:** はい。BMP、PNG、GIF、TIFF、PSD など多数の形式に対応しています。`Image.load` メソッドに対象ファイルを指定するだけです。

### Q4: Aspose.Imaging for Java の無料トライアルはありますか？

**A:** あります。無料トライアル版を **[こちら](https://releases.aspose.com/)** から入手できます。

### Q5: Aspose.Imaging for Java のサポートやヘルプはどこで受けられますか？

**A:** 質問、バグ報告、ベストプラクティスの相談は Aspose.Imaging for Java サポートフォーラム **[こちら](https://forum.aspose.com/)** で受け付けています。

---

**最終更新日:** 2026-01-09  
**テスト環境:** Aspose.Imaging for Java 24.11（執筆時点の最新）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}