---
date: 2026-05-18
description: Java 画像処理ライブラリ Aspose.Imaging を使用して、画像に XMP メタデータを埋め込んだり取得したりする方法を、ステップバイステップのコードとともに学びましょう。
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: 画像における XMP データ処理
schemas:
- author: Aspose
  dateModified: '2026-05-18'
  description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  headline: 'Java Image Processing Library: XMP with Aspose.Imaging'
  type: TechArticle
- description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  name: 'Java Image Processing Library: XMP with Aspose.Imaging'
  steps:
  - name: Specify Image Size and Tiff Options
    text: First, define the directory where your image will be stored and create a
      `Rectangle` to specify the size of the image. In this example, we use a TIFF
      image with certain options. `TiffOptions` configures format‑specific settings
      for the TIFF image.
  - name: Create a New Image
    text: Now, create a new image with the specified options. This image will be used
      to store the XMP metadata. `TiffImage` represents a TIFF image object, and `TiffFrame`
      defines an individual frame within it.
  - name: Create XMP Header and Trailer
    text: Create instances of XMP‑Header and XMP‑Trailer for your XMP metadata. These
      headers and trailers help define the metadata structure. `XmpHeaderPi` and `XmpTrailerPi`
      represent the XMP packet’s opening and closing sections.
  - name: Create XMP Meta Information
    text: Now, create an instance of XMP meta to set different attributes. You can
      add information like the author and description. `XmpMeta` holds the core metadata
      fields such as author and description.
  - name: Create XMP Packet Wrapper
    text: '`XmpPacketWrapper` is the container that holds the XMP header, trailer,
      and meta information in a single packet. It ensures the packet conforms to the
      XMP specification. `XmpPacketWrapper` packages the header, meta, and trailer
      into a single XMP packet.'
  - name: Add Photoshop Package
    text: To store Photoshop‑specific information, create a Photoshop package and
      set its attributes, such as city, country, and color mode. Then, add this package
      to the XMP metadata. `PhotoshopPackage` stores Photoshop‑specific metadata like
      city, country, and color mode.
  - name: Add Dublin Core Package
    text: For more general information, like author, title, and additional values,
      create a DublinCore package and set its attributes. Add this package to the
      XMP metadata as well. `DublinCorePackage` contains standard Dublin Core fields
      such as title, creator, and keywords.
  - name: Update XMP Metadata in the Image
    text: Update the XMP metadata into the image using the `setXmpData` method. This
      call writes the XMP packet into the image’s metadata section. `setXmpData` writes
      the XMP packet into the image’s metadata section.
  - name: Save the Image
    text: You can now save the image with the embedded XMP metadata on the disk or
      in a memory stream.
  - name: Load the Image and Retrieve XMP Metadata
    text: To retrieve the XMP metadata from the image, load the image from the memory
      stream or disk and access the XMP data via the `getXmpData` method. `getXmpData`
      reads the embedded XMP packet from the image. Congratulations! You've successfully
      learned how to handle XMP data in images using Aspose.Imagin
  type: HowTo
- questions:
  - answer: XMP is an XML‑based standard for embedding descriptive information directly
      inside files, enabling consistent metadata across applications.
    question: What is XMP metadata?
  - answer: It lets you tag images with author, copyright, keywords, and custom data,
      improving searchability and asset management without external databases.
    question: Why is XMP metadata important?
  - answer: Yes, Aspose.Imaging for Java provides methods to modify existing XMP packets
      and write them back to the file.
    question: Can I edit XMP metadata after embedding it in an image?
  - answer: A free trial is available for evaluation, but a paid license is required
      for production use. You can explore options on the [Aspose.Imaging for Java
      website](https://purchase.aspose.com/buy).
    question: Is Aspose.Imaging for Java a free tool?
  - answer: Visit the [Aspose.Imaging forums](https://forum.aspose.com/) for community
      assistance, or contact Aspose support directly for paid‑license customers.
    question: Where can I get help and support for Aspose.Imaging for Java?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: 'Java 画像処理ライブラリ: Aspose.Imaging を使用した XMP'
url: /ja/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java を使用した画像の XMP データ処理

Aspose.Imaging は **java image processing library** で、数十種類のラスタおよびベクタ形式を扱えます。このチュートリアルでは、Aspose.Imaging for Java を使用して画像に XMP (Extensible Metadata Platform) データを埋め込んだり取得したりする方法を学びます。最後まで読むと、作者、説明、カスタムメタデータを画像ファイル内に直接保存でき、検索可能で自己記述的になります。

## クイック回答
- **XMP とは何ですか？** XMP は画像、PDF、動画などのファイル内にメタデータを埋め込むための標準化された XML ベースのフォーマットです。  
- **Java で XMP を扱うライブラリはどれですか？** Aspose.Imaging for Java は XMP パケットの読み書き用の完全な API を提供します。  
- **ライセンスは必要ですか？** 開発には無料トライアルが使用できますが、本番環境では商用ライセンスが必要です。  
- **サポートされている画像形式は何種類ですか？** TIFF、JPEG、PNG、PSD、RAW など、150 以上の形式がサポートされています。  
- **大きな画像を処理できますか？** はい。ライブラリは画像全体をメモリに読み込まずに、最大 2 GB のファイルを処理できます。

## XMP メタデータとは何ですか？

XMP メタデータは XML ベースの標準で、デジタルファイルに記述情報を直接埋め込みます。作者、著作権、キーワード、カスタムデータなどをアプリケーション間で一貫して保存できるようにします。XML であるため、カスタム名前空間で拡張でき、コアスキーマを理解するツールと互換性を保ちながら独自フィールドを追加できます。これにより、長期的な資産管理やアプリケーション間の相互運用性に最適です。

## なぜ Java の画像処理ライブラリで XMP を使用するのですか？

Aspose.Imaging for Java は **150+ image formats** をサポートし、ストリーミング方式でマルチギガバイトファイルを処理でき、従来のロード方式に比べメモリ消費を最大 80 % 削減します。API は XMP パケットが標準準拠であることを保証し、Adobe Photoshop、Lightroom などのツールとの互換性を確保します。

## 前提条件

開始する前に、以下の前提条件を満たしていることを確認してください。

- コンピュータに Java 開発環境がセットアップされていること。  
- Aspose.Imaging for Java ライブラリがインストールされていること。[Aspose.Imaging for Java website](https://releases.aspose.com/imaging/java/) からダウンロードできます。  
- Java プログラミングの基本的な理解があること。

## パッケージのインポート

必要なパッケージを Java プロジェクトにインポートします。コードの先頭に以下のインポート文を追加してください。

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.xmp.XmpPackage;
import com.aspose.imaging.xmp.XmpPacketWrapper;
import com.aspose.imaging.xmp.XmpMeta;
import com.aspose.imaging.xmp.photoshop.ColorMode;
import com.aspose.imaging.xmp.photoshop.PhotoshopPackage;
import com.aspose.imaging.xmp.dc.DublinCorePackage;
import com.aspose.imaging.xmp.header.XmpHeaderPi;
import com.aspose.imaging.xmp.trailer.XmpTrailerPi;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

さあ、例をステップバイステップで分解してみましょう：

## Java の画像処理ライブラリを使用して XMP メタデータを埋め込む方法

画像を読み込み、XMP パケットを作成し、画像に添付して保存します。Aspose.Imaging の `setXmpData` メソッドは、別途メタデータファイルを必要とせずにパケットを直接ファイルに書き込みます。このプロセスはファイルベースとストリームベースの画像の両方で動作し、Web サービスやバッチジョブに適しています。

### 手順 1: 画像サイズと TIFF オプションの指定

まず、画像を保存するディレクトリを定義し、`Rectangle` を作成して画像サイズを指定します。この例では特定のオプションを持つ TIFF 画像を使用します。`TiffOptions` は TIFF 画像固有の設定を構成します。

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### 手順 2: 新しい画像の作成

次に、指定したオプションで新しい画像を作成します。この画像は XMP メタデータを格納するために使用されます。`TiffImage` は TIFF 画像オブジェクトを表し、`TiffFrame` はその中の個々のフレームを定義します。

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### 手順 3: XMP ヘッダーとトレーラーの作成

XMP メタデータ用に XMP ヘッダーとトレーラーのインスタンスを作成します。これらはメタデータ構造を定義するのに役立ちます。`XmpHeaderPi` と `XmpTrailerPi` は XMP パケットの開始部と終了部を表します。

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### 手順 4: XMP メタ情報の作成

次に、XMP メタ情報のインスタンスを作成し、さまざまな属性を設定します。作者や説明などの情報を追加できます。`XmpMeta` は作者や説明といったコアメタデータフィールドを保持します。

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### 手順 5: XMP パケットラッパーの作成

`XmpPacketWrapper` はヘッダー、トレーラー、メタ情報を単一のパケットにまとめるコンテナです。パケットが XMP 仕様に準拠していることを保証します。`XmpPacketWrapper` はヘッダー、メタ、トレーラーを一つの XMP パケットにパッケージ化します。

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### 手順 6: Photoshop パッケージの追加

Photoshop 固有の情報を格納するために Photoshop パッケージを作成し、都市、国、カラーモードなどの属性を設定します。その後、このパッケージを XMP メタデータに追加します。`PhotoshopPackage` は都市、国、カラーモードなどの Photoshop 固有メタデータを保存します。

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### 手順 7: Dublin Core パッケージの追加

作者、タイトル、追加の値など、より一般的な情報のために DublinCore パッケージを作成し、属性を設定します。このパッケージも XMP メタデータに追加します。`DublinCorePackage` にはタイトル、作成者、キーワードなどの標準的な Dublin Core フィールドが含まれます。

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### 手順 8: 画像内の XMP メタデータを更新

`setXmpData` メソッドを使用して画像内の XMP メタデータを更新します。この呼び出しは XMP パケットを画像のメタデータセクションに書き込みます。`setXmpData` は XMP パケットを画像のメタデータセクションに書き込みます。

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### 手順 9: 画像の保存

埋め込んだ XMP メタデータを含む画像をディスクまたはメモリストリームに保存できます。

```java
    image.save(ms);
```

### 手順 10: 画像を読み込み XMP メタデータを取得

メモリストリームまたはディスクから画像を読み込み、`getXmpData` メソッドで XMP メタデータを取得します。`getXmpData` は画像から埋め込まれた XMP パケットを読み取ります。

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

おめでとうございます！Aspose.Imaging for Java を使用して画像内の XMP データを扱う方法を習得しました。これにより、画像ファイル内に貴重なメタデータを保存・取得できるようになります。

## よくある問題と解決策

- **Photoshop にメタデータが表示されない:** XMP パケットが正しい XML スキーマに従っていることを確認してください。Aspose.Imaging は自動的に検証しますが、カスタム名前空間は登録が必要な場合があります。  
- **大きな TIFF ファイルで OutOfMemoryError が発生する:** `Compression` を `LZW` に設定した `TiffOptions` を使用し、ストリーミングを有効に（`loadOptions.setBufferSize`）してメモリ使用量を抑えてください。  
- **予期しない文字エンコーディング:** XMP は UTF‑8 を期待します。文字化けを防ぐため、常に `StandardCharsets.UTF_8` を使用して文字列を渡してください。

## よくある質問

**Q: XMP メタデータとは何ですか？**  
A: XMP は XML ベースの標準で、ファイル内に記述情報を直接埋め込むことで、アプリケーション間で一貫したメタデータ管理を可能にします。

**Q: XMP メタデータはなぜ重要ですか？**  
A: 作者、著作権、キーワード、カスタムデータなどを画像にタグ付けでき、外部データベースなしで検索性と資産管理が向上します。

**Q: 画像に埋め込んだ後、XMP メタデータを編集できますか？**  
A: はい。Aspose.Imaging for Java は既存の XMP パケットを変更し、再度ファイルに書き込むメソッドを提供します。

**Q: Aspose.Imaging for Java は無料ツールですか？**  
A: 評価用の無料トライアルは利用可能ですが、本番環境で使用するには有料ライセンスが必要です。詳細は [Aspose.Imaging for Java website](https://purchase.aspose.com/buy) をご覧ください。

**Q: Aspose.Imaging for Java のサポートやヘルプはどこで得られますか？**  
A: コミュニティ支援は [Aspose.Imaging forums](https://forum.aspose.com/) で受けられます。有料ライセンスのお客様は直接 Aspose のサポートにお問い合わせください。

## 結論

このチュートリアルでは、主要な **java image processing library** である Aspose.Imaging for Java を使用して画像の XMP メタデータを操作する方法を紹介しました。ステップバイステップの手順に従うことで、XMP データの埋め込み、更新、取得が簡単に行え、検索可能で標準準拠のメタデータでデジタル資産を強化できます。

---

**最終更新日:** 2026-05-18  
**テスト環境:** Aspose.Imaging for Java 24.12  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [Java 画像処理マスター: Aspose.Imaging で EXIF データを変更](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [Aspose.Imaging を使用した Java 画像処理: 画像の読み込み、強化、保存](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [Aspose.Imaging ライブラリによる高度な Java 画像処理](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Specify the size of image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// create the brand new image just for sample purposes
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// create an instance of XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// create an instance of Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// create an instance of XMP meta class to set different attributes
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// create an instance of XmpPacketWrapper that contains all metadata
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// create an instance of Photoshop package and set photoshop attributes
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// add photoshop package into XMP metadata
	xmpData.addPackage(photoshopPackage);
	// create an instance of DublinCore package and set dublinCore attributes
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// add dublinCore Package into XMP metadata
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// update XMP metadata into image
	image.setXmpData(xmpData);
	// Save image on the disk or in memory stream
	image.save(ms);
	// Load the image from memory stream or from disk to read/get the metadata
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Getting the XMP metadata
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Use package data ...
		}
	}
}
        
```