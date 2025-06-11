---
"date": "2025-06-04"
"description": "Aspose.Imagingを使用して、JavaでCCITTFAX3圧縮を使用した複数ページのTIFFファイルを作成する方法を学びます。効率的なドキュメントスキャンとアーカイブ技術を習得します。"
"title": "Aspose.Imaging を使用して Java で CCITTFAX3 圧縮によるマルチページ TIFF を作成する"
"url": "/ja/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging を使用して Java で CCITTFAX3 圧縮によるマルチページ TIFF 作成をマスターする

## 導入

複数ページのTIFFファイルを作成して、ドキュメントのスキャンとアーカイブプロセスを効率的に管理したいとお考えですか？Aspose.Imaging for Javaを使えば、このタスクはシームレスに実現できます。このガイドでは、スキャンしたドキュメントなどのモノクロ画像に最適なCCITTFAX3圧縮方式を用いて、複数ページのTIFFファイルを作成する手順を解説します。これらのテクニックを習得すれば、大量の画像データを効率的に処理できるようになります。

**学習内容:**
- Java プロジェクトで Aspose.Imaging を設定します。
- CCITTFAX3 圧縮を使用して TiffOptions を作成します。
- 新しい TiffImage インスタンスを生成して構成します。
- 画像を読み込み、サイズを変更し、TIFF ファイルにフレームとして追加します。
- 複数ページの TIFF ファイルを保存して最適化します。

これらの機能を Java アプリケーションに実装する方法について詳しく見ていきましょう。

## 前提条件

始める前に、次の前提条件が満たされていることを確認してください。

### 必要なライブラリ
- **Aspose.Imaging for Java**現在のすべての機能にアクセスするには、バージョン 25.5 以降をお勧めします。
  
### 環境設定要件
- マシンに Java 開発キット (JDK) がインストールされていること。
- IntelliJ IDEA や Eclipse のような IDE。

### 知識の前提条件
- Java プログラミングとオブジェクト指向の概念に関する基本的な理解。
- 依存関係管理のための Maven/Gradle に精通していること。

## Aspose.Imaging for Java のセットアップ

プロジェクトでAspose.Imagingを使用するには、依存関係として追加する必要があります。各ビルドツールでこれを行う方法は次のとおりです。

**メイヴン:**
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**グレード:**
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### 直接ダウンロード

または、最新バージョンを直接ダウンロードすることもできます。 [Aspose.Imaging for Java リリース](https://releases。aspose.com/imaging/java/).

### ライセンス取得

下記のサイトにアクセスして、無料トライアルライセンスを取得し、すべての機能を制限なく試すことができます。 [Asposeの無料トライアルページ](https://releases.aspose.com/imaging/java/)長期間の使用には、ライセンスを購入するか、一時的なライセンスを申請することを検討してください。 [Aspose 購入](https://purchase。aspose.com/temporary-license/).

### 基本的な初期化

Aspose.Imaging をプロジェクトに組み込んだら、次のように初期化します。

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```

## 実装ガイド

機能に基づいて実装をいくつかの論理セクションに分割します。

### CCITTFAX3圧縮でTiffOptionsを作成する

#### 概要
作成する `TiffOptions` CCITTFAX3圧縮用に設定されたインスタンスは、TIFF形式のモノクロ画像を扱う際に不可欠です。この機能はストレージを最適化し、画像品質を効果的に維持します。

**手順:**

1. **CCITTFAX3でTiffOptionsを初期化する**
    ```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```

2. **出力ファイルソースを設定する**
    ```java
    // 「YOUR_OUTPUT_DIRECTORY」を実際のディレクトリパスに置き換えます。
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```

### 新しいTiffImageインスタンスを作成する

#### 概要
インスタンスの作成 `TiffImage` 寸法を指定し、以前に設定された `TiffOptions`。

**手順:**

1. **寸法を宣言する**
    ```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```

2. **TiffImageインスタンスを作成する**
    ```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```

### ディレクトリから画像を読み込み、サイズを変更する

#### 概要
画像を読み込むには、ディレクトリからファイルを読み取り、拡張子でフィルタリングし、TIFF のサイズに合わせてサイズを変更することが必要です。

**手順:**

1. **JPGファイルのフィルタリングと読み込み**
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

2. **画像のサイズ変更**
    ```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```

### 複数ページのTIFF画像にフレームを追加する

#### 概要
複数ページのTIFFファイルを作成するには、フレームの追加が不可欠です。各フレームは個々の画像に対応します。

**手順:**

1. **画像を反復処理してフレームを作成する**
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

### 複数ページのTIFF画像を保存する

#### 概要
最後に、リソースを保存して閉じると、すべての変更が保持されます。

**手順:**

1. **変更を保存**
    ```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```

## 実用的なアプリケーション

CCITTFAX3 圧縮を使用して複数ページの TIFF ファイルを作成すると、次のようないくつかのシナリオでメリットがあります。

- **文書アーカイブ**スキャンした文書を効率的に保存およびアーカイブします。
- **医療画像**放射線科向けに高品質の圧縮画像を維持します。
- **印刷サービス**複数の画像ページを必要とする大きな印刷ジョブを準備します。

## パフォーマンスに関する考慮事項

最適なパフォーマンスを確保するには:
- 適切なサイズ変更方法を使用して、処理時間を短縮しながら品質を維持します。
- 使用後はすぐにリソースを閉じることでメモリを効率的に管理します。
- ファイル I/O 操作を最適化し、大規模なデータセットの非同期処理を検討します。

## 結論

このチュートリアルでは、JavaでAspose.Imagingを使用してCCITTFAX3圧縮方式で複数ページのTIFFファイルを作成する方法を学習しました。これらの手順を理解することで、様々なアプリケーションで画像データを効率的に管理できるようになります。スキルをさらに向上させるには、Aspose.Imagingライブラリの追加機能を試し、プロジェクトに統合してみてください。

## FAQセクション

1. **CCITTFAX3 圧縮とは何ですか?**
   - これは、モノクロ画像専用に設計された圧縮方式で、ドキュメントのスキャンでよく使用されます。

2. **大規模な画像データセットを効率的に処理するにはどうすればよいですか?**
   - 非同期処理を実装し、メモリ使用量を最適化して、リソースを効率的に管理します。

3. **Aspose.Imaging は他のシステムと統合できますか?**
   - はい、シームレスな統合のためにさまざまなファイル形式やシステムと対話できる API を提供します。

4. **Aspose.Imaging のライセンス オプションは何ですか?**
   - オプションには、無料トライアル、拡張テスト用の一時ライセンス、またはフルライセンスの購入が含まれます。

5. **TIFF ファイルの操作時によくある問題を解決するにはどうすればよいですか?**
   - Asposeの [ドキュメント](https://reference.aspose.com/imaging/java/) トラブルシューティングのヒントについては、サポート フォーラムをご覧ください。

## リソース

- **ドキュメント**https://reference.aspose.com/imaging/java/
- **ダウンロード**https://releases.aspose.com/imaging/java/
- **購入**https://purchase.aspose.com/buy
- **無料トライアル**https://releases.aspose.com/imaging/java/
- **一時ライセンス**https://purchase.aspose.com/temporary-license/
- **サポート**https://forum.aspose.com/c/imaging/10

これで知識が身についたので、Java プロジェクトでこれらのテクニックを実装し、探索してみましょう。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}