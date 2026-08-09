---
date: '2026-06-28'
description: Aspose.Imaging for Java を使用して ODP を PNG に変換し、カスタムフォントを設定し、正確なレンダリングのためにシステムフォントを無効にする方法を学びます。
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: Aspose.Imaging for Java を使用して ODP を PNG に変換する方法 – カスタムフォントとエクスポートガイド
url: /ja/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging for Java を使用した ODP から PNG への変換方法 – カスタムフォントとエクスポートガイド

最新の Java アプリケーションでは、OpenDocument Presentation（ODP）ファイルを高品質な PNG 画像に変換することが一般的な要件です。特に、カスタムフォントでブランドを保持する必要がある場合に重要です。このチュートリアルでは、Aspose.Imaging for Java を使用して **ODP を PNG に変換する方法** を示し、カスタムフォントフォルダーの設定、システムフォントのフォールバック無効化、そして最適なパフォーマンスのためのラスタライズオプションの微調整について解説します。

**学べること**
- ODP 変換のためにカスタムフォントディレクトリを設定する方法。  
- システム代替フォントを無効化し、選択したフォントのみを使用する方法。  
- 正確なサイズとフォント設定で ODP ファイルを PNG にエクスポートする方法。  
- 大規模なプレゼンテーションを処理する際の速度とメモリ使用量を改善するヒント。

## クイック回答
- **Maven を使用して Aspose.Imaging を追加できますか？** はい、Maven 依存関係を追加して `mvn install` を実行してください。  
- **本番環境でライセンスが必要ですか？** 無制限に使用するには有効な Aspose.Imaging ライセンスが必要です。  
- **カスタムフォントは尊重されますか？** フォントフォルダーを設定し、システム代替フォントを無効化すれば適用されます。  
- **サポートされている画像形式は何ですか？** Aspose.Imaging は PNG、JPEG、TIFF、WebP など 120 以上のラスタ・ベクタ形式をサポートしています。  
- **API はスレッドセーフですか？** はい、ほとんどの Aspose.Imaging クラスはスレッドごとに別インスタンスを作成すれば同時使用が安全です。

## 「how to convert odp」とは何ですか？
*「How to convert odp」* は、OpenDocument Presentation ファイルを別の形式（主に PNG）に変換し、レイアウト、フォント、視覚的忠実度を保持するプロセスを指します。Aspose.Imaging for Java は、外部ツールを必要とせずにこの変換を処理する単一メソッドのワークフローを提供し、開発者が最小限のコードで変換機能をアプリケーションに統合できるようにします。

## なぜ Aspose.Imaging for Java を使用するのか？
Aspose.Imaging は **120 以上の出力形式** をサポートし、マルチページ ODP ファイルをメモリ全体にロードせずにラスタライズできるため、大規模なプレゼンテーションでピーク RAM 使用量を最大 70 % 削減できます。また、組み込みのフォント管理機能によりサードパーティのレンダリングエンジンが不要です。

## 前提条件
- **Libraries**: Aspose.Imaging for Java ≥ 25.5。  
- **JDK**: バージョン 8 以上。  
- **IDE**: IntelliJ IDEA、Eclipse、または任意の Java 対応エディタ。  
- **Basic Knowledge**: Java I/O、オブジェクト指向プログラミング、画像概念。

## インストール手順

### Maven
`pom.xml` に以下の依存関係を追加し、`mvn clean install` を実行してください：

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
`build.gradle` ファイルにライブラリを含め、プロジェクトをリフレッシュしてください：

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### 直接ダウンロード
最新の JAR は [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) からダウンロードできます。

## ライセンス取得手順
フル機能を有効にするには、一時または永続ライセンスを適用してください：

1. **Free Trial** – ライセンス不要、機能は制限付き。  
2. **Temporary License** – [Aspose website](https://purchase.aspose.com/temporary-license/) で申請してください。  
3. **Purchase** – [Aspose purchase page](https://purchase.aspose.com/buy) からサブスクリプションまたは永続ライセンスを購入してください。

ライセンスファイルでライブラリを初期化します：

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## ODP 変換のためにカスタムフォントディレクトリを設定する方法
`FontSettings` は Aspose.Imaging のフォントリソースを管理するクラスです。画像処理を開始する前にカスタムフォントをロードしてください。これにより、すべてのスライドが指定したフォントを正確に使用します。

Aspose.Imaging の `FontSettings` を使用してフォントフォルダーのパスを設定します：

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Definition anchor*: `FontSettings.setFontsFolder` は、ファイルシステム上で TrueType および OpenType フォントを検索する場所を Aspose.Imaging に指示します。

## ODP 変換中にシステム代替フォントを無効化する方法
システム代替フォントを無効化すると、レンダリングエンジンは OS にインストールされているフォントを無視し、提供したフォントのみを使用します。これにより、スライドの外観を変える予期せぬフォント置換が防止されます。

以下の呼び出しでシステム代替フォントを無効化します：

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Definition anchor*: `FontSettings.setGetSystemAlternativeFont(false)` は、定義したフォルダー内のフォントのみを使用させ、予期しない置換を排除します。

## 指定したフォントで ODP ファイルを PNG にエクスポートする方法
`RasterizationOptions` はベクタページをビットマップ画像にラスタライズする方法を定義します。フォント設定とラスタライズ設定を組み合わせることで、DPI、背景色、ページサイズを各 PNG に対して制御できます。

以下の例のようにエクスポートメソッドを実装してください：

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*Definition anchor*: `RasterizationOptions` クラスは生成される PNG ファイルの DPI、ページサイズ、背景色を制御します。

### よくある落とし穴と解決策
- **Missing font files** – ODP で参照されているすべての `.ttf` または `.otf` が設定したフォルダーに存在することを確認してください。  
- **Incorrect file paths** – 絶対パスを使用するか、`System.getProperty("user.dir")` を基準に相対パスを解決してください。  
- **Insufficient permissions** – Java プロセスがフォントディレクトリを読み取り、出力フォルダーに書き込めることを確認してください。

## 実用的な活用例
1. **ブランド一貫性のあるスライドデッキ** – Web 公開用に PNG としてエクスポートし、企業フォントを保持します。  
2. **自動レポート生成** – 各スライドを画像に変換し、PDF レポートやメールニュースレターに組み込みます。  
3. **レガシーアーカイブ作成** – ODP コンテンツを PNG として保存し、ODP ビューアが不要でも将来のアクセスを保証します。

## パフォーマンス上の考慮点
- 最新の Aspose.Imaging バージョンを使用して、マルチスレッドラスタライズの改善（8 コア CPU で最大 2 倍高速化）を活用してください。  
- 画像処理は try‑with‑resources ブロックでラップし、ネイティブリソースの適時破棄を保証してください。  
- 数千枚のスライドを処理する場合は、`RasterizationOptions`（例：DPI を下げる）を調整し、品質とメモリ使用量のバランスを取ってください。

## よくある質問

**Q: 必要最低限の Java バージョンは何ですか？**  
A: Aspose.Imaging for Java は JDK 8 以降で動作します。長期サポートのためには JDK 11 が推奨されます。

**Q: 特定のスライドだけを変換できますか？**  
A: はい、`save` を呼び出す前に `rasterizationOptions.setPageNumber(specificSlideIndex)` を設定してください。

**Q: パスワード保護された ODP ファイルはどう扱いますか？**  
A: パスワードを含む `LoadOptions` でファイルをロードし、同じフォント設定で続行してください。

**Q: システムフォントを無効化するとパフォーマンスに影響しますか？**  
A: 影響は僅かです。エンジンがシステムフォントの検索をスキップするため、特にフォントコレクションが大きいマシンで速度が若干向上します。

**Q: さらにコードサンプルはどこで見つけられますか？**  
A: 公式の [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/) で、バッチ変換や画像変換などのシナリオを確認できます。

## 追加リソース
- [Aspose.Imaging for Java リリース](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/)  
- [無料トライアルを開始](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging ドキュメント](https://reference.aspose.com/imaging/java/)  
- [Aspose.Imaging フォーラム](https://forum.aspose.com/c/imaging/14)  
- [Aspose ライセンス購入](https://purchase.aspose.com/buy)  
- [一時ライセンスの申請](https://purchase.aspose.com/temporary-license/)  

---

**最終更新日:** 2026-06-28  
**テスト対象:** Aspose.Imaging for Java 25.5  
**作者:** Aspose

## 関連チュートリアル

- [Convert ODG to PNG with Aspose.Imaging for Java: A Complete Guide](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Efficient Image Conversion in Java with Aspose.Imaging: A Complete Guide](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}