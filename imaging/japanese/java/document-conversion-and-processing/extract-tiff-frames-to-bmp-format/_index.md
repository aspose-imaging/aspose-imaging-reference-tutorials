---
date: 2025-12-19
description: Aspose.Imaging を使用して Java で TIFF を BMP に変換する方法を学びましょう。このステップバイステップの Java
  画像処理チュートリアルでは、マルチページ TIFF ファイルの画像変換方法を示します。
linktitle: Extract TIFF Frames to BMP Format
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java を使用して TIFF を BMP に変換する方法
url: /ja/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java を使用した TIFF から BMP への変換

If you need to **convert tiff to bmp** inside a Java application, you’re in the right place. Whether you’re handling a single‑page TIFF or a multi‑page document, Aspose.Imaging for Java makes the process straightforward and reliable. In this tutorial we’ll walk through extracting each frame from a TIFF file and saving it as an individual BMP image—perfect for image conversion java scenarios.

## Quick Answers
- **変換を処理するライブラリは？** Aspose.Imaging for Java  
- **マルチページ TIFF を処理できますか？** はい – 各フレームが個別の BMP として保存されます  
- **本番環境でライセンスが必要ですか？** 商用利用には有効な Aspose ライセンスが必要です  
- **サポートされている Java バージョンは？** Java 8 以上  
- **コードの実行時間はどれくらいですか？** 標準サイズの画像では通常数秒です  

## Prerequisites

Before we get started, make sure you have the following prerequisites in place:

1. **Java 開発環境** – 動作する JDK（8 以上）とお好みの IDE またはビルドツール  
2. **Aspose.Imaging for Java** – ウェブサイトの[こちら](https://releases.aspose.com/imaging/java/)から最新の JAR をダウンロードしてください。  
3. **サンプル TIFF 画像** – プロジェクトの作業ディレクトリに配置した TIFF ファイル（単ページまたはマルチページ）  

## Import Packages

To start the process, you need to import the necessary packages for your Java application:

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## Step‑by‑Step Guide to convert tiff to bmp

### Step 1: Load the TIFF Image and Initialize Frame Counter

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // Create an instance of int to keep track of frames in TiffImage
    int frameCounter = 0;
```

### Step 2: Iterate Over TIFF Frames

```java
    // Iterate over the TiffFrames in TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

### Step 3: Load Pixels of TiffFrame into an Array of Colors

```java
        // Load Pixels of TiffFrame into an array of Colors
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

### Step 4: Create BMP Options and Set Bits Per Pixel

```java
        // Create an instance of bmpCreateOptions
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

### Step 5: Save BMP Image

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

## Why use Aspose.Imaging for Java?

- **堅牢なマルチページサポート** – 余分なコードなしで任意の数の TIFF フレームを処理  
- **純粋な Java 実装** – ネイティブ依存がなく、クロスプラットフォーム展開に最適  
- **高品質な BMP 出力** – ビット/ピクセル、圧縮、カラー深度を制御可能  
- **包括的な画像変換 Java ツールキット** – JPEG、PNG、GIF など多数のフォーマットに対応  

## Common Issues & Troubleshooting

| 症状 | 考えられる原因 | 対策 |
|---------|--------------|-----|
| `OutOfMemoryError` が大きな TIFF の読み込み中に発生 | 画像全体がメモリに読み込まれる | 示したようにフレームを1つずつ処理するか、JVM ヒープサイズ（`-Xmx`）を増やす |
| BMP ファイルが破損している | `BitsPerPixel` の値が不正 | 真彩色 BMP には 24 または 32 を使用 |
| 出力ファイルが作成されない | 出力ディレクトリのパスが間違っている | `Your Document Directory` が既存のフォルダを指しているか確認 |

## Frequently Asked Questions

### Q1: Aspose.Imaging for Java とは何ですか？

A1: Aspose.Imaging for Java は、さまざまな画像フォーマットを扱い、変換、編集、操作などのタスクを実行できる豊富な画像処理機能を提供する Java ライブラリです。

### Q2: 異なる画像フォーマットで Aspose.Imaging for Java を使用できますか？

A2: はい、Aspose.Imaging for Java は TIFF、BMP、JPEG、PNG など多数の画像フォーマットをサポートしており、画像関連のタスクに汎用的に利用できます。

### Q3: Aspose.Imaging for Java のドキュメントはどこで見つけられますか？

A3: Aspose.Imaging for Java の詳細なドキュメントは[こちら](https://reference.aspose.com/imaging/java/)で確認できます。

### Q4: Aspose.Imaging for Java の無料トライアルはありますか？

A4: はい、[こちら](https://releases.aspose.com/)で無料トライアルをご利用いただけます。

### Q5: Aspose.Imaging for Java のサポートはどうすれば受けられますか？

A5: Aspose.Imaging for Java に関する質問や問題、サポートは[こちら](https://forum.aspose.com/)のフォーラムをご利用ください。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日：** 2025-12-19  
**テスト環境：** Aspose.Imaging for Java 24.12 (latest)  
**作者：** Aspose  

---