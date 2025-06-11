---
"date": "2025-06-02"
"description": ".NETでAspose.Imagingを使用してマルチフレームTIFF画像を作成する方法を学びます。環境の設定、TiffOptionsの設定、JPEGのサイズ変更、フレームの追加などを習得します。"
"title": "Aspose.Imaging for .NET でマルチフレーム TIFF 画像を作成する方法"
"url": "/ja/net/animation-multi-frame-images/create-multi-frame-tiff-images-aspose-imaging-dotnet/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging for .NET でマルチフレーム TIFF 画像を作成する方法

## 導入

Aspose.Imaging for .NET を使ってマルチフレーム TIFF 画像を作成する方法を習得したいとお考えですか？この包括的なチュートリアルでは、環境設定、TiffOptions の設定、JPEG ファイルのサイズ変更、TIFF 画像へのフレームの追加など、すべて簡単に行えます。ドキュメントアーカイブの管理でも、高品質な画像をソフトウェアアプリケーションに統合する場合でも、このガイドはワークフローの強化に役立ちます。

**学習内容:**
- Aspose.Imaging for .NET のセットアップ方法
- CCITT Fax Group 3圧縮を使用した白黒画像のTiffOptionsの設定
- ディレクトリからJPEGファイルを読み込み、サイズを変更する
- TIFF画像にフレームを追加する
- マルチフレームTIFF画像の保存

始める前に前提条件を確認しましょう。

## 前提条件

Aspose.Imaging を使用して TIFF 画像を作成する前に、次のものを用意してください。

### 必要なライブラリと依存関係
- **Aspose.Imaging .NET 版**NuGet またはお好みのパッケージ マネージャーを使用してこのライブラリをインストールします。
  
### 環境設定要件
- C#と.NET Core/5+をサポートする開発環境
  
### 知識の前提条件
- C#プログラミング概念の基本的な理解
- .NET での画像ファイルの処理に関する知識

## Aspose.Imaging for .NET のセットアップ

まず、Aspose.Imaging をインストールする必要があります。手順は以下のとおりです。

**.NET CLI**
```shell
dotnet add package Aspose.Imaging
```

**パッケージマネージャー**
```powershell
Install-Package Aspose.Imaging
```

**NuGet パッケージ マネージャー UI**
「Aspose.Imaging」を検索し、最新バージョンをインストールします。

### ライセンス取得手順
- **無料トライアル**機能をテストするために、機能が制限されたバージョンにアクセスします。
- **一時ライセンス**評価制限のない延長トライアルをご希望の方は、こちらにアクセスしてください。 [一時ライセンス](https://purchase。aspose.com/temporary-license/).
- **購入**フルアクセスをご希望の場合は、ライセンスの購入をご検討ください。 [Aspose.Imaging を購入](https://purchase。aspose.com/buy).

### 基本的な初期化とセットアップ

```csharp
// ライセンスを使用してライブラリを初期化します
Aspose.Imaging.License license = new Aspose.Imaging.License();
license.SetLicense("Path to your license file");
```

## 実装ガイド

実装を管理しやすいセクションに分割してみましょう。

### TIFF イメージの TiffOptions の作成と設定

#### 概要
作成する `TiffOptions` オブジェクトを使用すると、TIFF ファイルのカスタマイズに不可欠な圧縮や測光解釈などの設定を定義できます。

#### ステップバイステップの実装

**1. 必要な名前空間をインポートする**
ファイルに次の名前空間が含まれていることを確認してください。

```csharp
using Aspose.Imaging.FileFormats.Tiff;
using Aspose.Imaging.FileFormats.Tiff.Enums;
using Aspose.Imaging.ImageOptions;
```

**2. TiffOptionsを設定する**
セットアップ `TiffOptions` CCITT Fax Group 3 圧縮を使用した白黒画像用の特定の構成を持つオブジェクト。

```csharp
// デフォルト設定でTiffOptionsを作成する
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);

// サンプルあたりのビット数を1（白黒）に設定する
outputSettings.BitsPerSample = new ushort[] { 1 };

// CCITT FAXグループ3圧縮を使用する
outputSettings.Compression = TiffCompressions.CcittFax3;

// 測光解釈をMinIsWhiteとして定義する
outputSettings.Photometric = TiffPhotometrics.MinIsWhite;

// 最初から新しいTIFFを作成するために、ソースを空のストリームに設定します
outputSettings.Source = new Aspose.Imaging.Sources.StreamSource(new System.IO.MemoryStream());
```

### 特定の寸法の TiffImage を作成および構成する

#### 概要
作成する `TiffImage` 各 TIFF フレームのサイズを定義するときに重要となるカスタム寸法の設定が含まれます。

**1. 画像の寸法を定義する**

```csharp
int newWidth = 500; // 各TIFFフレームの幅
int newHeight = 500; // 各TIFFフレームの高さ
string path = "@YOUR_OUTPUT_DIRECTORY\\AddFramesToTIFFImage_out.tif";
```

**2. TiffImageインスタンスを作成する**
初期化する `TiffImage` 指定された寸法と出力設定で。

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    // フレームを追加するロジックがここに追加されます。
}
```

### ディレクトリからJPEGファイルを読み込み、サイズを変更する

#### 概要
Aspose.Imaging を使用すると、JPEG イメージの読み込み、サイズ変更、TIFF ファイルへの組み込みの準備が効率化されます。

**1. JPEG画像を読み込む**

```csharp
string dataDir = "@YOUR_DOCUMENT_DIRECTORY"; // 入力画像を含むディレクトリ

foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
{
    using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
    {
        // TIFFフレームの寸法に合わせて画像のサイズを変更する
        ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
        
        // 複数のフレームを処理するための追加ロジックがここに追加されます。
    }
}
```

### TiffImage にフレームを追加して保存する

#### 概要
TIFF 画像にフレームを追加するには、サイズ変更された JPEG ピクセルを各フレームにコピーし、完全なマルチフレーム TIFF を保存します。

**1. TiffImageインスタンスを初期化する**

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    int index = 0; // フレームインデックストラッカー
    
    foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
    {
        using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
        {
            ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
            
            TiffFrame frame = tiffImage.ActiveFrame;
            if (index > 0)
            {
                // 後続の画像ごとに新しいフレームを作成します
                frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            }
            
            // サイズ変更されたJPEGのピクセルをTIFFフレームにコピーします
            frame.SavePixels(frame.Bounds, ri.LoadPixels(ri.Bounds));
            if (index > 0)
            {
                tiffImage.AddFrame(frame); // 最初のフレームの後にのみTIFF画像に追加します
            }
            index++;
        }
    }
    
    tiffImage.Save(path); // すべてのフレームを含む最終的なTIFFを保存します
}
```

## 実用的なアプリケーション

マルチフレーム TIFF 画像を作成する実際の使用例をいくつか示します。

1. **文書アーカイブ**スキャンしたドキュメントを単一の TIFF ファイルとして保存し、データの整合性とアクセスの容易さを確保します。
2. **医療画像**MRI や CT などの医療スキャンを保存するには、高品質の圧縮 TIFF 形式を使用します。
3. **グラフィックデザイン**複数のデザイン レイヤーを 1 つのファイルに結合して、グラフィック ソフトウェアで効率的に処理します。
4. **写真**複数ページのフォトアルバムを単一のファイルとしてアーカイブし、簡単に共有および保存できます。
5. **産業品質管理**TIFF 画像を使用して、複数のフレームにわたる詳細な検査データを記録します。

## パフォーマンスに関する考慮事項

### パフォーマンスを最適化するためのヒント
- **メモリ管理**使用後はイメージ オブジェクトを適切に破棄してリソースを解放します。
- **バッチ処理**大規模なデータセットを扱う場合は、メモリ使用量を効率的に管理するために、画像をバッチで処理します。
- **効率的な圧縮**品質とパフォーマンスの要件に基づいて適切な圧縮設定を選択します。

## 結論

このチュートリアルでは、Aspose.Imaging for .NETを使用してマルチフレームTIFF画像を作成するための基本的な手順を説明しました。 `TiffOptions` フレームを追加するだけでなく、高品質のイメージングをアプリケーションに統合するための強固な基盤も構築できます。

**次のステップ:**
- さまざまな圧縮設定と画像形式を試してください。
- Aspose.Imagingの追加機能については、 [公式文書](https://reference。aspose.com/imaging/net/).

これらの手順をプロジェクトに実装し、マルチフレーム TIFF 画像によってワークフローがどのように強化されるかを確認してください。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}