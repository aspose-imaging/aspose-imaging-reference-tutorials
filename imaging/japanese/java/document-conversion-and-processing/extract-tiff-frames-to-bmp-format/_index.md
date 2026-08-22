---
date: 2026-05-03
description: Aspose.Imaging を使用して Java でマルチページ TIFF を BMP 形式に変換する方法を学びましょう。効率的に TIFF
  を変換するためのステップバイステップガイドをご覧ください。
keywords:
- convert multi page tiff
- how to convert tiff
- Aspose.Imaging Java
- TIFF to BMP conversion
- image processing Java
linktitle: TIFFフレームをBMP形式に抽出
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java を使用してマルチページTIFFをBMPに変換する
url: /ja/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java を使用したマルチページTIFFからBMPへの変換

Java環境で作業しながら、**マルチページTIFFを変換**ファイルを個別のBMP画像に変換する必要がある場合、ここが適切な場所です。このチュートリアルでは、強力な Aspose.Imaging for Java ライブラリを使用して、各TIFFフレームを抽出しBMPファイルとして保存する正確な手順を説明します。最後までに、プログラムで*tiffを変換する方法*だけでなく、このアプローチがバッチ画像処理タスクに信頼できる理由も理解できるようになります。

## クイック回答
- **TIFFからBMPへの変換に最適なライブラリは何ですか？** Aspose.Imaging for Java  
- **必要なコード行数は？** 約30行、5つの論理ステップにわたります  
- **本番環境でライセンスが必要ですか？** はい、商用ライセンスが必要です（無料トライアル利用可能）  
- **大きなマルチページTIFFを処理できますか？** はい、APIはフレームを効率的にストリーミングします  
- **サポートされているJavaバージョンは何ですか？** Java 8以降  

## 「マルチページTIFFを変換」とは何ですか？

マルチページTIFFを変換するとは、単一のTIFFコンテナ内に保存された各ページ（またはフレーム）を取り出し、独立した画像ファイル（ここではBMP）としてエクスポートすることを意味します。これは、文書アーカイブ、医療画像、またはラスタ画像が必要なあらゆるワークフローに役立ちます。

## なぜ Aspose.Imaging for Java を使用するのですか？

- **フルフォーマットサポート** – TIFF、BMP、JPEG、PNG、その他多数に対応。  
- **外部依存なし** – 純粋なJavaで、ネイティブライブラリは不要です。  
- **高性能** – フレームへのストリーミングアクセスによりメモリ使用量が削減されます。  
- **リッチAPI** – ピクセルデータ、カラーデプス、メタデータに対する細かな制御を提供します。

## 前提条件

1. **Java開発環境** – JDK 8以上とお好みのIDE。  
2. **Aspose.Imaging for Java** – 公式サイトから最新のJARをダウンロードしてください **[こちら](https://releases.aspose.com/imaging/java/)**。  
3. **サンプルマルチページTIFF** – TIFFファイル（例：`sample.tiff`）をコードが読み取れる既知のディレクトリに配置してください。

## パッケージのインポート

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## Aspose.Imaging を使用したマルチページTIFFからBMPへの変換方法

### ステップ1: TIFF画像をロードし、フレームカウンタを初期化する

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // Create an instance of int to keep track of frames in TiffImage
    int frameCounter = 0;
```

### ステップ2: TIFFフレームを反復処理する

```java
    // Iterate over the TiffFrames in TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

### ステップ3: TiffFrameのピクセルをカラー配列にロードする

```java
        // Load Pixels of TiffFrame into an array of Colors
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

### ステップ4: BMPオプションを作成し、ビット深度を設定する

```java
        // Create an instance of bmpCreateOptions
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

### ステップ5: BMP画像を保存する

```java
            // Set the Source of bmpCreateOptions as FileCreateSource by specifying the location where output will be saved
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // Create a new bmpImage
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // Save the bmpImage with pixels from TiffFrame
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## 一般的な落とし穴とヒント

- **メモリ使用量:** 非常に大きなTIFFファイルを扱う場合、画像全体をメモリにロードするのではなく、フレームを1つずつ処理すること（上記のように）を検討してください。  
- **ファイル命名:** `String.format` 呼び出しは各フレームに対してユニークなファイル名（`...out0.bmp`、`...out1.bmp` など）を作成します。別の命名規則が必要な場合はパターンを調整してください。  
- **ビット深度:** BMPはさまざまなビット深度をサポートしています。24ビット（フルカラー）はほとんどのシナリオで機能します。8ビットグレースケール出力が必要な場合は `setBitsPerPixel` を変更してください。

## FAQ

### Q1: Aspose.Imaging for Java とは何ですか？

A1: Aspose.Imaging for Java は、さまざまな画像フォーマットを扱い、変換、編集、操作などのタスクを実行できる豊富な画像処理機能を提供するJavaライブラリです。

### Q2: Aspose.Imaging for Java を異なる画像フォーマットで使用できますか？

A2: はい、Aspose.Imaging for Java はTIFF、BMP、JPEG、PNG など多数の画像フォーマットをサポートしており、画像関連タスクに汎用的に使用できます。

### Q3: Aspose.Imaging for Java のドキュメントはどこで見つけられますか？

A3: Aspose.Imaging for Java の詳細なドキュメントは **[こちら](https://reference.aspose.com/imaging/java/)** で見つけられます。

### Q4: Aspose.Imaging for Java の無料トライアルは利用可能ですか？

A4: はい、無料トライアルは **[こちら](https://releases.aspose.com/)** で利用できます。

### Q5: Aspose.Imaging for Java のサポートはどのように受けられますか？

A5: Aspose.Imaging for Java に関する質問、問題、サポートは、サポートフォーラム **[こちら](https://forum.aspose.com/)** でご利用ください。

## よくある質問

**Q: 同じアプローチでマルチページTIFFを他のフォーマット（例：PNG）に変換できますか？**  
A: もちろんです。`BmpOptions` を適切なオプションクラス（例：`PngOptions`）に置き換え、`FileCreateSource` パスのファイル拡張子を調整してください。

**Q: Aspose.Imaging は圧縮TIFF（LZW、CCITT）を処理しますか？**  
A: はい、ライブラリはフレーム抽出時にサポートされているTIFF圧縮方式を透過的にデコードします。

**Q: BMPに変換する際にEXIFメタデータを保持できますか？**  
A: BMPはEXIFメタデータをサポートしていません。メタデータを保持したい場合は、対応フォーマット（例：PNG）に変換するか、変換後に手動でメタデータをコピーしてください。

**Q: フォルダ内の複数のTIFFファイルをバッチ処理するにはどうすればよいですか？**  
A: 上記コードをディレクトリ内の `File` オブジェクトを反復するループでラップし、各ファイルの `dataDir` とソースファイル名を更新してください。

**Q: 商用展開にはどのライセンスが必要ですか？**  
A: 本番環境で使用するには有料の Aspose.Imaging for Java ライセンスが必要です。開発中は一時的なトライアルライセンスを使用できます。

**最終更新日:** 2026-05-03  
**テスト環境:** Aspose.Imaging for Java 24.12（執筆時点での最新）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}