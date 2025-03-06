---
title: Aspose.Imaging for Java を使用した画像内の XMP データ処理
linktitle: 画像内の XMP データ処理
second_title: Aspose.Imaging Java 画像処理 API
description: Aspose.Imaging for Java を使用して画像内の XMP メタデータを処理する方法を学習します。メタデータを埋め込み、取得して画像ファイルを強化します。
weight: 16
url: /ja/java/document-conversion-and-processing/xmp-data-handling-in-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java を使用した画像内の XMP データ処理

Aspose.Imaging for Java は、さまざまな形式の画像を操作するための多用途で強力なライブラリです。このチュートリアルでは、Aspose.Imaging for Java を使用して画像内の XMP (Extensible Metadata Platform) データを処理するプロセスについて説明します。 XMP は画像ファイルにメタデータを埋め込むための標準で、作成者や説明などの貴重な情報を保存できます。

## 前提条件

始める前に、次の前提条件が満たされていることを確認してください。

- コンピュータ上にセットアップされた Java 開発環境。
-  Java ライブラリ用の Aspose.Imaging がインストールされています。からダウンロードできます。[Aspose.Imaging for Java Web サイト](https://releases.aspose.com/imaging/java/).
- Java プログラミングの基本的な理解。

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。コードの先頭に次のインポート ステートメントを追加できます。

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

次に、この例をステップバイステップのガイドに分解してみましょう。

## ステップ 1: 画像サイズと Tiff オプションを指定する

まず、画像を保存するディレクトリを定義し、画像のサイズを指定する Rectangle を作成します。この例では、特定のオプションを備えた Tiff イメージを使用します。

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## ステップ 2: 新しいイメージを作成する

ここで、指定されたオプションを使用して新しいイメージを作成します。このイメージは、XMP メタデータを保存するために使用されます。

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## ステップ 3: XMP ヘッダーとトレーラーを作成する

XMP メタデータの XMP-Header および XMP-Trailer のインスタンスを作成します。これらのヘッダーとトレーラーは、メタデータ構造を定義するのに役立ちます。

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## ステップ 4: XMP メタ情報を作成する

次に、XMP メタのインスタンスを作成して、さまざまな属性を設定します。作成者や説明などの情報を追加できます。

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## ステップ 5: XMP パケット ラッパーを作成する

XMP ヘッダー、トレーラー、メタ情報を含む XmpPacketWrapper のインスタンスを作成します。

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## ステップ 6: Photoshop パッケージを追加する

Photoshop 固有の情報を保存するには、Photoshop パッケージを作成し、都市、国、カラー モードなどの属性を設定します。次に、このパッケージを XMP メタデータに追加します。

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## ステップ 7: Dublin Core パッケージを追加する

著者、タイトル、追加の値などのより一般的な情報を得るには、DublinCore パッケージを作成し、その属性を設定します。このパッケージを XMP メタデータにも追加します。

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## ステップ 8: イメージ内の XMP メタデータを更新する

を使用して、XMP メタデータをイメージに更新します。`setXmpData`方法。

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## ステップ 9: 画像を保存する

XMP メタデータが埋め込まれたイメージをディスクまたはメモリ ストリームに保存できるようになりました。

```java
    image.save(ms);
```

## ステップ 10: 画像をロードして XMP メタデータを取得する

イメージから XMP メタデータを取得するには、メモリ ストリームまたはディスクからイメージをロードし、XMP データにアクセスします。

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            //パッケージデータを使用します...
        }
    }
}
```

おめでとう！ Aspose.Imaging for Java を使用して画像内の XMP データを処理する方法を学習しました。これにより、画像ファイル内に貴重なメタデータを保存および取得できるようになります。

## 結論

このチュートリアルでは、Aspose.Imaging for Java を使用して画像内の XMP メタデータを操作する方法を検討しました。ステップバイステップのガイドに従うことで、画像ファイル内にメタデータを簡単に埋め込んだり取得したりすることができ、情報と使いやすさが向上します。

## よくある質問

### Q1: XMP メタデータとは何ですか?

A1: XMP (Extensible Metadata Platform) は、画像を含むさまざまな種類のファイルにメタデータを埋め込むための標準です。これにより、作成者、タイトル、説明などの情報をファイル自体に保存できます。

### Q2: XMP メタデータはなぜ重要ですか?

A2: XMP メタデータは、デジタル資産を整理および分類するために不可欠です。これは、所有権の帰属、コンテンツの説明、画像などのファイルへのコンテキストの追加に役立ち、ファイルをよりアクセスしやすく意味のあるものにします。

### Q3: XMP メタデータを画像に埋め込んだ後に編集できますか?

A3: はい、XMP メタデータを画像に埋め込んだ後、編集することができます。 Aspose.Imaging for Java は、必要に応じてメタデータ属性を変更および更新するためのツールを提供します。

### Q4: Aspose.Imaging for Java は無料のツールですか?

 A4: Aspose.Imaging for Java は無料の試用版を提供していますが、全機能を使用して拡張して使用するには、有料ライセンスが必要です。でオプションを検討できます。[Aspose.Imaging for Java Web サイト](https://purchase.aspose.com/buy).

### Q5: Aspose.Imaging for Java のヘルプとサポートはどこで入手できますか?

 A5: Aspose.Imaging for Java に関して問題が発生したり、質問がある場合は、次のサイトにアクセスしてください。[Aspose.Imaging フォーラム](https://forum.aspose.com/)コミュニティのサポートと指導のために。



## 完全なソースコード
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
//Rectangle を定義して画像のサイズを指定します
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
//サンプル目的のためだけに新しいイメージを作成します
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	//XMP-Headerのインスタンスを作成する
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	//Xmp-TrailerPi のインスタンスを作成する
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	//XMP メタクラスのインスタンスを作成してさまざまな属性を設定します
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	//すべてのメタデータを含む XmpPacketWrapper のインスタンスを作成します
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	//Photoshop パッケージのインスタンスを作成し、Photoshop 属性を設定する
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	//Photoshop パッケージを XMP メタデータに追加する
	xmpData.addPackage(photoshopPackage);
	//DublinCore パッケージのインスタンスを作成し、dublinCore 属性を設定します
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	//dublinCore パッケージを XMP メタデータに追加
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	//XMP メタデータをイメージに更新する
	image.setXmpData(xmpData);
	//画像をディスクまたはメモリ ストリームに保存します
	image.save(ms);
	//メモリ ストリームまたはディスクから画像をロードしてメタデータを読み取り/取得します
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		//XMPメタデータの取得
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			//パッケージデータを使用します...
		}
	}
}
        
```
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
