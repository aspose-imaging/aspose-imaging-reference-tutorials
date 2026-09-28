---
date: '2026-09-28'
description: Aspose.Imaging を使用して ccittfax3 compression java によりマルチページ TIFF ファイルを作成する方法を学びます。文書ワークフローにおいて、効率的にスキャン、アーカイブし、ファイルサイズを削減します。
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Aspose.Imaging と ccittfax3 compression java を使用して、スキャンとアーカイブ向けの効率的なマルチページ
  TIFF ファイルを構築する手順をステップバイステップで紹介します。
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: ccittfax3 compression java を使用してマルチページ TIFF を作成する方法
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: ccittfax3 compression java を使用してマルチページ TIFF を作成する方法
url: /ja/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging を使用した ccittfax3 圧縮 Java によるマルチページ TIFF 作成の習得

## はじめに

もし、スキャンした文書を大量にアーカイブしつつファイルサイズを小さく保ちたい場合、**ccittfax3 compression java** が最適なソリューションです。このチュートリアルでは、Aspose.Imaging を使用して Java で CCITTFAX3 圧縮を施したマルチページ TIFF ファイルを生成する方法を示します。モノクロスキャンにこの圧縮が非常に効果的な理由、ライブラリの設定方法、各ページをフレームとして追加する方法を学びます。

**学べること**
- Aspose.Imaging を Java プロジェクトに追加する方法。
- CCITTFAX3 圧縮用に `TiffOptions` を設定する方法。
- `TiffImage` を作成し、ソース画像をリサイズしてフレームとして追加する方法。
- 最終的なマルチページ TIFF を効率的に保存する方法。

完全な実装手順を見ていきましょう。

## 簡単な回答
- **CCITTFAX3 圧縮の主な利点は何ですか？** 白黒スキャンでファイルサイズを最大 80 % 縮小できます。  
- **どのライブラリが組み込みサポートを提供していますか？** Aspose.Imaging for Java、バージョン 25.5+。  
- **開発にライセンスは必要ですか？** 無料のトライアルライセンスで全機能が利用可能です。商用利用には有料ライセンスが必要です。  
- **数百ページを処理できますか？** はい—Aspose.Imaging はページをストリーム処理するため、メモリ使用量が低く抑えられます。  
- **コードは Java 11 以降と互換性がありますか？** 完全に対応しています；API は Java 8+ を対象としています。

## ccittfax3 compression java とは何ですか？

`CCITTFAX3` は、ファックスやスキャン文書画像向けに設計されたロスレスのモノクロ圧縮アルゴリズムです。各ピクセルを 1 ビットでエンコードし、高品質な出力を維持しながらファイルサイズを大幅に縮小します—非圧縮 TIFF と比較して 70‑80 % 程度削減されることが多いです。このため、忠実度を保つ必要がある白黒文書のアーカイブに最適です。

## このタスクに Aspose.Imaging を使用する理由は？

Aspose.Imaging は PDF、PNG、JPEG、TIFF などを含む **100+** の入力・出力フォーマットをサポートしています。そのストリーミングアーキテクチャにより、**数百ページ** の TIFF ファイルでもドキュメント全体をメモリに読み込むことなく処理でき、大規模なアーカイブプロジェクトに最適です。

## 前提条件

- **Java Development Kit (JDK)** 8 以上がインストールされていること。
- **IDE**（IntelliJ IDEA や Eclipse など）。
- 依存関係管理のための **Maven** または **Gradle**。
- 基本的な Java の知識（クラス、オブジェクト、コレクション）。

## Aspose.Imaging の Java への設定

ライブラリをビルドファイルに追加します。

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```  

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

### 直接ダウンロード

最新の JAR は [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) からダウンロードできます。

### ライセンス取得

無料トライアルライセンスは [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/) から入手できます。商用利用の場合は、永続ライセンスを購入するか、[Aspose Purchase](https://purchase.aspose.com/temporary-license/) で一時ライセンスをリクエストしてください。

詳細な API の使用方法については、Aspose.Imaging for Java の [documentation](https://reference.aspose.com/imaging/java/) を参照してください。

### 基本的な初期化

依存関係を追加したら、以下のようにライブラリを初期化します。

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## マルチページ TIFF のために ccittfax3 compression java を設定する方法は？

`TiffOptions` は TIFF ファイルの出力形式と圧縮設定を定義するクラスです。`CCITTGroup3FaxCompression` 列挙体で `TiffOptions` オブジェクトをロードし、出力ファイルのソースを設定します。この 2 段階の設定により、モノクロ圧縮用のライターが準備され、後で追加されるすべてのページが CCITTFAX3 アルゴリズムでエンコードされるため、画像品質を保ちつつサイズを大幅に削減できます。

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## Java で TiffImage インスタンスを作成する方法は？

`TiffImage` はメモリ内のマルチページ TIFF ドキュメントを表し、フレームを操作するメソッドを提供します。まず、すべてのページが共有する幅と高さを定義します。次に、先に作成した `TiffOptions` を使用して `TiffImage` をインスタンス化します。`TiffImage` オブジェクトは個々のフレームのコンテナとして機能し、最終ファイルを保存する前にページの追加、削除、順序変更が可能です。

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## フォルダーからソース画像を読み込みリサイズする方法は？

対象ディレクトリから JPEG ファイルをフィルタリングし、各画像を読み込んで TIFF キャンバスに合わせてリサイズします。フレームを追加する前にリサイズすることでメモリ消費を抑え、保存処理を高速化します。各ソース画像を必要な寸法とピクセル形式に変換することで、ページレイアウトの一貫性が保証され、フレームを TIFF ドキュメントに追加する際のランタイムエラーを防止できます。

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## 各画像をフレームとしてマルチページ TIFF に追加する方法は？

`TiffFrame` は TIFF 内で単一ページ画像とそのメタデータを保持するオブジェクトです。リサイズ済み画像を反復処理し、新しい `TiffFrame` を作成して `TiffImage` に追加します。各フレームは最終ドキュメントの別々のページとなり、ライブラリはページ数やオフセットなどの必要なメタデータ更新を自動的に処理し、正しいマルチページ TIFF 構造を保証します。

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## 最終的なマルチページ TIFF ファイルを保存する方法は？

`TiffImage` インスタンスの `save` メソッドを呼び出し、目的の出力パスを指定します。ライブラリは CCITTFAX3 圧縮を使用してすべてのフレームを書き込み、データをディスクに効率的にストリームし、基底リソースを閉じます。保存が完了すると、生成されたファイルには指定された圧縮が適用されたすべてのページが含まれ、配布やアーカイブにすぐに使用できます。

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## 実用的な応用例

- **Document archiving:** スキャンした契約書、請求書、法的記録などを最小限のストレージで保存します。  
- **Medical imaging:** 診断情報を保持しながら放射線画像を圧縮します。  
- **Print production:** プリンタが直接処理できるマルチページ印刷ジョブを生成します。

## パフォーマンス上の考慮点

- 歪みを防ぐため、アスペクト比を保持する `ResizeOptions` を使用します。  
- フレームを追加した後は各 `Image` オブジェクトを閉じてネイティブメモリを解放します。  
- 非常に大規模なバッチの場合、ファイルを並列ストリームで処理し、各 TIFF セグメントを非同期で書き込みます。

## 一般的な落とし穴とトラブルシューティング

- **Incorrect pixel format:** CCITTFAX3 は 1 ビット（白黒）画像のみで動作します。リサイズ前にカラー画像をグレースケールに変換してください。  
- **Memory leaks:** 一時的な `Image` オブジェクトには必ず `dispose()` を呼び出し、そうしないとネイティブバッファが解放されません。  
- **File size not reduced:** `TiffOptions` の compression プロパティが設定されているか確認してください。設定されていない場合、デフォルトの（圧縮なし）になります。

## よくある質問

**Q: カラー画像でもこの手法を使用できますか？**  
A: CCITTFAX3 はモノクロデータに限定されます。カラーの場合は JPEG または LZW 圧縮を使用してください。

**Q: Aspose.Imaging は巨大な TIFF のストリーミングをサポートしていますか？**  
A: はい。ライブラリは各フレームを直接出力ストリームに書き込むため、数千ページでもメモリ使用量が低く抑えられます。

**Q: 一時ライセンスをプログラムで適用するには？**  
A: `.lic` ファイルを `License license = new License(); license.setLicense("Aspose.Total.Java.lic");` のようにロードします。

**Q: 保存前に TIFF をプレビューする方法はありますか？**  
A: 各 `TiffFrame` を `BufferedImage` にレンダリングし、Swing コンポーネントで表示できます。

**Q: 公式にサポートされている Java バージョンはどれですか？**  
A: Aspose.Imaging は Java 8 から Java 21（LTS リリースを含む）をサポートしています。

## 結論

これで、Aspose.Imaging を使用した **ccittfax3 compression java** によるマルチページ TIFF ファイル作成の完全な本番対応ワークフローが手に入ります。上記の手順に従うことで、ストレージコストを抑えつつ画像品質を高く保ち、大量の文書コレクションを効率的にアーカイブできます。OCR、メタデータ処理、フォーマット変換など、Aspose.Imaging の追加機能を活用して、文書処理パイプラインをさらに強化しましょう。

---

**最終更新日:** 2026-09-28  
**テスト環境:** Aspose.Imaging 25.5 for Java  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.Imaging for Java を使用したマルチページ TIFF の作成方法 – 完全ガイド](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Java で LZW 圧縮を使用して画像ファイルサイズを削減する方法](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Aspose.Imaging for Java でマルチページ TIFF フレームを分割する方法](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}