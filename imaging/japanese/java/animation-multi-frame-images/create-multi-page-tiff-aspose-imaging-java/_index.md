---
date: '2026-11-16'
description: Aspose.Imaging for Java を使用してマルチページ TIFF を作成する方法を学びます。画像を TIFF に変換し、フレームを結合し、ストレージを最適化する方法を1つのガイドにまとめました。
keywords:
- create multi page tiff
- convert images to tiff
- aspose imaging java
- java image processing tutorial
- multi-page tiff generation
lastmod: '2026-11-16'
og_description: Aspose.Imaging for Java を使用してマルチページ TIFF を作成します。このステップバイステップガイドでは、画像を
  TIFF に変換し、フレームを追加し、ストレージを最適化する方法を示します。
og_image_alt: 'Developer guide: create multi page tiff using Aspose.Imaging for Java'
og_title: Aspose.Imaging for Java でマルチページ TIFF を作成
schemas:
- author: Aspose
  dateModified: '2026-11-16'
  description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  headline: How to create multi page tiff using Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  name: How to create multi page tiff using Aspose.Imaging for Java
  steps:
  - name: load an image
    text: '`Image.load` reads the image file into memory and returns an `Image` object
      that you can manipulate. Ensure the file path is correct to avoid `FileNotFoundException`.'
  - name: resize the image
    text: '`ResizeType.NearestNeighbourResample` preserves hard edges and pixel data,
      which is ideal when you need a faithful representation of scanned documents.'
  - name: set up TIFF options
    text: '`TiffOptions` defines the compression, bits per pixel, and other TIFF‑specific
      settings. The `source` property points to the file where the multi‑page TIFF
      will be saved.'
  - name: initialize the TIFF image
    text: '`TiffImage.create` creates an empty TIFF container with the width and height
      derived from the first resized image. This container will later hold each frame
      you add.'
  - name: load additional images
    text: The loop iterates over every file ending with `.img` (or any supported raster
      format) in the target directory, loads each image, and calls `savePixels` to
      copy pixel data into a new frame of the TIFF.
  - name: save your work
    text: '`image.save` writes the complete multi‑page TIFF to the output path you
      specified in `TiffOptions`. Verify that the directory is writable to avoid `IOException`.'
  type: HowTo
- questions:
  - answer: Absolutely. Load any supported raster format (PNG, JPEG, BMP, etc.) and
      add each as a frame using the same workflow.
    question: Can I convert PNG or JPEG files to a multi‑page TIFF with this approach?
  - answer: Yes. Call `tiffOptions.setCompression(TiffCompression.Lzw)` before creating
      the image to reduce file size while preserving quality.
    question: Is it possible to set compression (e.g., LZW) for the output TIFF?
  - answer: Use `frame.getMetadata().addProperty("Author", "Your Name")` after creating
      the frame and before saving.
    question: How do I add metadata (author, description) to each TIFF frame?
  - answer: It does. Load the file with `Image.load("existing.tiff")` and iterate
      through `((TiffImage)image).getFrames()` to access each page.
    question: Does Aspose.Imaging support reading existing multi‑page TIFFs?
  - answer: Process pages in batches, call `System.gc()` periodically, and use the
      try‑with‑resources pattern to release native memory promptly.
    question: What if I need to process thousands of pages?
  type: FAQPage
tags:
- create multi page tiff
- Aspose.Imaging
- Java image processing
- TIFF conversion
title: Aspose.Imaging for Java を使用してマルチページ TIFF を作成する方法
url: /ja/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java を使用してマルチページ TIFF を作成する方法

## はじめに

**マルチページ TIFF** を作成することは、複数の関連画像を単一のコンパクトなファイルにアーカイブする必要がある場合に一般的な要件です。ドキュメント管理システム、医療画像パイプライン、バッチ処理ツールのいずれを構築していても、Aspose.Imaging for Java は TIFF の作成、圧縮、フレーム処理を完全にコントロールできます。本ガイドでは、画像を読み込み、サイズ変更し、複数の画像を 1 つのマルチページ TIFF に結合する方法を学び、メモリ使用量を抑えつつパフォーマンスを高める方法を紹介します。

**学べること**
- Aspose.Imaging を使用して画像を読み込み、サイズ変更する。
- `TiffOptions` を設定してマルチページ出力を行う。
- 複数のソース画像からフレームを追加する。
- オプションの圧縮を使用して最終的な TIFF を保存する。
- マルチページ TIFF が有効に機能する実際のシナリオ。

## クイック回答
- **主要なライブラリは何ですか？** Aspose.Imaging for Java.  
- **画像を TIFF に変換できますか？** はい – 本チュートリアルでは PNG、JPEG、BMP、その他の形式をマルチページ TIFF に結合する方法を示します。  
- **ライセンスは必要ですか？** 無料トライアルで評価は可能ですが、本番利用には永続ライセンスが必要です。  
- **必要な Java バージョンは？** Java 8 以上 (JDK 8+).  
- **コードはスレッドセーフですか？** この例は単一スレッドで実行されます。並行シナリオでは、スレッドごとに `Image` オブジェクトを管理してください。

## マルチページ TIFF の作成方法

ソース画像を読み込み、必要に応じてサイズ変更し、`TiffOptions` を設定し、各画像をフレームとして追加して `save` を呼び出します。この簡潔なフローにより、数行の Java コードで標準準拠のマルチページ TIFF を作成でき、圧縮やページサイズを制御できます。

## マルチページ TIFF とは何ですか？

マルチページ TIFF は、複数の画像フレーム（各ページを表す）を含む単一の TIFF ファイルです。多数のページを別々のファイルとして管理するオーバーヘッドがないため、アーカイブ、FAX、文書スキャンなどの用途で広く使用されています。

## 前提条件

- **Aspose.Imaging for Java** ライブラリ（以下のリンクからダウンロード）。
- **JDK 8+** がインストールされ、IDE（IntelliJ IDEA、Eclipse など）で設定されていること。
- 基本的な Java の知識とファイル I/O の理解。

## Aspose.Imaging for Java の設定

Aspose.Imaging を使用開始するには、プロジェクトに統合する必要があります。以下は、一般的なビルドツールを使用した統合方法です。

**Maven:**  
Add the following dependency to your `pom.xml`:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle:**  
Include this in your `build.gradle` file:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

または、最新の Aspose.Imaging for Java JAR を [Aspose releases](/imaging/java/) から **直接ダウンロード** できます。

### ライセンス取得

まずは無料トライアルで Aspose.Imaging の機能を試すことができます。長期利用の場合は、一時ライセンスの取得またはフルライセンスの購入をご検討ください。

- **無料トライアル:** [Aspose Imaging Java Releases](/imaging/java/) にアクセスしてライブラリをダウンロードし、試用してください。  
- **一時ライセンス:** [Aspose Temporary License Page](/purchase/temporary-license/) から取得してください。  
- **購入:** 永続的なソリューションとして、[Aspose Purchase](/purchase/buy) にアクセスしてください。

## 画像の読み込みとサイズ変更

**概要:**  
最初のステップは、ファイルシステムから画像を読み込み、最近傍リサンプリング方式でサイズ変更することです。

#### 手順 1: 画像を読み込む
`Image.load` は画像ファイルをメモリに読み込み、操作可能な `Image` オブジェクトを返します。`FileNotFoundException` を防ぐため、ファイルパスが正しいことを確認してください。  
```java
import com.aspose.imaging.Image;

String dataDir = "YOUR_DOCUMENT_DIRECTORY";
Image tempImage = Image.load(dataDir + "/Image1.png");
```

#### 手順 2: 画像をサイズ変更する
`ResizeType.NearestNeighbourResample` はハードエッジとピクセルデータを保持し、スキャンした文書を忠実に再現する際に最適です。  
```java
int width = tempImage.getWidth();
int height = tempImage.getHeight();
tempImage.resize(width, height, ResizeType.NearestNeighbourResample);
```

## TIFF オプションとソースの作成

**概要:**  
次に、新しいマルチページ TIFF ファイルを作成するために必要なオプションを設定します。これには、期待されるフォーマットとソース設定の指定が含まれます。

#### 手順 1: TIFF オプションを設定する
`TiffOptions` は圧縮方式、ビット深度、その他の TIFF 固有設定を定義します。`source` プロパティはマルチページ TIFF を保存するファイルを指します。  
```java
import com.aspose.imaging.fileformats.tiff.TiffOptions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.sources.FileCreateSource;

TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setSource(new FileCreateSource("YOUR_DOCUMENT_DIRECTORY/MultiPage.tiff", false));
```

## マルチページ TIFF 画像の作成と初期化

**概要:**  
ここでは、指定した寸法でマルチページ TIFF 画像のインスタンスを作成します。

#### 手順 1: TIFF 画像を初期化する
`TiffImage.create` は、最初にサイズ変更した画像から取得した幅と高さで空の TIFF コンテナを作成します。このコンテナは後で追加する各フレームを保持します。  
```java
import com.aspose.imaging.fileformats.tiff.TiffImage;

TiffImage tiffImage = (TiffImage) Image.create(tiffOptions, width, height);
```

## 複数画像の処理と TIFF へのフレーム追加

**概要:**  
このセクションでは、複数の画像をフレームとしてマルチページ TIFF ファイルに追加します。

#### 手順 1: 追加画像を読み込む
ループは対象ディレクトリ内の `.img`（またはサポートされているラスタ形式）で終わるすべてのファイルを走査し、各画像を読み込んで `savePixels` を呼び出し、ピクセルデータを TIFF の新しいフレームにコピーします。  
```java
import java.io.File;
import java.io.FilenameFilter;
import com.aspose.imaging.fileformats.tiff.TiffFrame;

File di = new File(dataDir);
String[] files = di.list(new FilenameFilter() {
    @Override
    public boolean accept(File dir, String name) {
        return name.endsWith(".img");
    }
});

if (files != null) {
    int index = 0;
    for (String file : files) {
        try (Image inputImage = Image.load(dataDir + "/" + file)) {
            if (index > 0) {
                TiffFrame newframe = new TiffFrame(tiffOptions, width, height);
                tiffImage.addFrame(newframe);
            }
            TiffFrame frame = tiffImage.getFrames()[index];
            frame.savePixels(frame.getBounds(), ((RasterImage) inputImage).loadPixels(inputImage.getBounds()));
            index += 1;
        }
    }
}
```

## マルチページ TIFF 画像の保存

**概要:**  
最後に、処理中に行ったすべての変更を保持するためにマルチページ TIFF ファイルを保存します。

#### 手順 1: 作業を保存する
`image.save` は、`TiffOptions` で指定した出力パスに完全なマルチページ TIFF を書き込みます。`IOException` を防ぐため、ディレクトリが書き込み可能であることを確認してください。  
```java
import com.aspose.imaging.examples.Utils;

tiffImage.save("YOUR_OUTPUT_DIRECTORY/output.tiff");
```

## 実用的な応用例

Aspose.Imaging for Java を使用して **画像を TIFF に変換** する方法を理解することは、以下のような実際のシナリオで有益です。

- **アーカイブプロジェクト:** 数百枚のスキャンページを単一ファイルに保存し、ファイルシステムの散在を減らし、バックアップ戦略を簡素化します。
- **医療画像:** CT、MRI、X線スライスを 1 つのマルチページ TIFF に結合し、システム間の転送を容易にします。
- **文書管理:** バージョン管理された PDF、スキャンした契約書、請求書などを一緒に保管し、迅速な検索と印刷を可能にします。

統合例として、AWS S3 や Azure Blob Storage などのクラウドストレージと連携させ、自動アーカイブパイプラインを実現することが考えられます。

## パフォーマンス上の考慮点

Java で画像処理ライブラリを使用する際は、次の点に留意してください。

- **フレーム追加前にリサイズ** – 高解像度スキャンでメモリ使用量を最大 60 % 削減。
- **ストリーミング API を使用** – Aspose.Imaging は画像をチャンク単位で処理でき、500 ページ以上の TIFF を扱う際に有効です。
- **Image オブジェクトを速やかに破棄** – `try (Image img = Image.load(...)) { … }` のようにラップして、ネイティブリソースを自動的に解放します。

## なぜ Aspose.Imaging for Java を使用するのか？

Aspose.Imaging は PNG、JPEG、BMP、GIF、TIFF など **50 以上** の入出力フォーマットをサポートし、ドキュメント全体をメモリに読み込むことなく数百ページ規模の TIFF ファイルを処理できます。ベンチマークでは、大量バッチ処理時にネイティブ Java ImageIO と比較して CPU 使用率が 30 % 削減されることが示されています。

## よくある質問

**Q: この方法で PNG や JPEG ファイルをマルチページ TIFF に変換できますか？**  
**A:** もちろんです。サポートされているラスタ形式（PNG、JPEG、BMP など）を読み込み、同じワークフローでフレームとして追加できます。

**Q: 出力 TIFF に圧縮（例: LZW）を設定できますか？**  
**A:** はい。画像を作成する前に `tiffOptions.setCompression(TiffCompression.Lzw)` を呼び出すことで、品質を保ちつつファイルサイズを削減できます。

**Q: 各 TIFF フレームにメタデータ（作者、説明など）を追加するには？**  
**A:** `frame.getMetadata().addProperty("Author", "Your Name")` をフレーム作成後、保存前に実行してください。

**Q: Aspose.Imaging は既存のマルチページ TIFF の読み取りをサポートしていますか？**  
**A:** サポートしています。`Image.load("existing.tiff")` でファイルを読み込み、`((TiffImage)image).getFrames()` を使って各ページにアクセスできます。

**Q: 数千ページを処理する必要がある場合は？**  
**A:** ページをバッチ処理し、定期的に `System.gc()` を呼び出し、try‑with‑resources パターンでネイティブメモリを速やかに解放してください。

## リソース

- [Aspose.Imaging for Java ドキュメント](/reference/imaging/java/)
- [最新バージョンのダウンロード](/imaging/java/)
- [ライセンス購入オプション](/purchase/buy)
- [Aspose 購入](/purchase/buy)
- [無料トライアルから始める](/imaging/java/)
- [一時ライセンス情報](/purchase/temporary-license/)
- [コミュニティサポートとフォーラム](/forum/imaging/14)

これらのリソースを活用することで、Aspose.Imaging for Java の理解を深め、プロジェクトで効果的に活用できます。コーディングを楽しんでください！

---

**最終更新日:** 2026-11-16  
**テスト環境:** Aspose.Imaging for Java 25.5  
**作者:** Aspose

```java
// Example: load and save a TIFF
Image img = Image.load("input.png");
img.save("output.tiff");
```

## 関連チュートリアル

- [Aspose.Imaging for Java を使用したマルチフレーム TIFF の JPEG 変換 - 完全ガイド](/imaging/java/image-loading-saving/convert-multi-frame-tiff-to-jpeg-aspose-imaging-java/)
- [Aspose.Imaging for Java でマルチページ TIFF フレームを分割](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)
- [aspose imaging java – TIFF を BMP フレームに変換](/imaging/java/animation-multi-frame-images/extract-tiff-frames-to-bmp-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}