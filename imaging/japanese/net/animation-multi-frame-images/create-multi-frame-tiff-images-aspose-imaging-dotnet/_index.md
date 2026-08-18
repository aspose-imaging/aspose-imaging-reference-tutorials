---
date: '2026-02-09'
description: Aspose.Imaging for .NET を使用して JPEG を TIFF に変換し、マルチフレーム TIFF 画像を作成する方法を学びます。セットアップ、TiffOptions
  の構成、ディレクトリからの画像読み込み、フレーム処理が含まれます。
keywords:
- create multi-frame tiff images
- Aspose.Imaging for .NET tutorial
- configure TiffOptions in .NET
title: Aspose.Imaging for .NET を使用して JPEG を TIFF に変換し、マルチフレーム TIFF 画像を作成する方法
url: /ja/net/animation-multi-frame-images/create-multi-frame-tiff-images-aspose-imaging-dotnet/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# JPEG を TIFF に変換し、Aspose.Imaging for .NET でマルチフレーム TIFF 画像を作成する方法

## Introduction

Aspose.Imaging for .NET を使用して **convert JPEG to TIFF** の技術を習得し、さらにマルチフレーム TIFF ファイルを作成したいですか？本包括的チュートリアルでは、環境設定、`TiffOptions` の構成、JPEG ファイルのリサイズ、TIFF 画像へのフレーム追加までを簡単に案内します。文書アーカイブの管理や、ソフトウェアアプリケーションへの高品質イメージング統合など、ワークフローの向上に役立つ内容です。

**学べること:**
- Aspose.Imaging for .NET のセットアップ方法
- CCITT Fax Group 3 圧縮を使用した白黒画像用 `TiffOptions` の設定
- ディレクトリから JPEG を読み込みリサイズする方法
- TIFF 画像へのフレーム追加手順
- マルチフレーム TIFF の保存方法

それでは、前提条件を確認して始めましょう。

## Quick Answers
- **“convert JPEG to TIFF” とは何ですか？**  
  JPEG ラスタ画像を TIFF 形式で保存することを指し、カスタム圧縮や複数フレームを付加できる場合があります。  
- **.NET でこれを実現する最適なライブラリは？**  
  Aspose.Imaging for .NET は変換、リサイズ、マルチフレーム作成のための豊富な API を提供します。  
- **ライセンスは必要ですか？**  
  無料トライアルで評価可能です。永続ライセンスを取得すれば評価制限はすべて解除されます。  
- **ディレクトリから画像を自動的に読み込めますか？**  
  はい – 本チュートリアルでは JPEG ファイルを列挙し、順次処理する方法を示します。  
- **コードは .NET 6+ と互換性がありますか？**  
  もちろんです – サンプルは .NET Core/5+ API を使用しており、.NET 6 以降でも動作します。

## What is “convert JPEG to TIFF”?
JPEG を TIFF に変換するとは、JPEG ファイルをデコードし、必要に応じてリサイズや色深度変更などの変換を行った上で、TIFF ファイルとしてエンコードすることです。TIFF は複数フレーム、ロスレス圧縮、メタデータをサポートしており、アーカイブやマルチページシナリオに最適です。

## Why use Aspose.Imaging for this conversion?
- **圧縮やフォトメトリック解釈、ピクセル形式をフルコントロール**  
- **マルチフレームサポート** – 複数の JPEG ページを 1 つの TIFF ドキュメントにまとめられます  
- **クロスプラットフォーム** – Windows、Linux、macOS で .NET Core/5+ 上で動作  
- **外部依存なし** – 純粋なマネージドコードで、ネイティブ DLL が不要  

## Prerequisites

Aspose.Imaging を使用して TIFF 画像を作成する前に、以下を確認してください。

### Required Libraries and Dependencies
- **Aspose.Imaging for .NET**: NuGet またはお好みのパッケージマネージャーでインストールします。

### Environment Setup Requirements
- C# と .NET Core/5+ に対応した開発環境  

### Knowledge Prerequisites
- C# の基本的なプログラミング概念の理解  
- .NET での画像ファイル操作に関する基礎知識  

## Setting Up Aspose.Imaging for .NET

まずは Aspose.Imaging をインストールします。手順は以下の通りです。

**.NET CLI**
```shell
dotnet add package Aspose.Imaging
```

**Package Manager**
```powershell
Install-Package Aspose.Imaging
```

**NuGet Package Manager UI**  
「Aspose.Imaging」を検索し、最新バージョンをインストールします。

### License Acquisition Steps
- **Free Trial**: 機能制限付きのバージョンで機能をテストできます。  
- **Temporary License**: 評価制限なしで長期間試用できる一時ライセンスです。詳細は [Temporary License](https://purchase.aspose.com/temporary-license/) をご覧ください。  
- **Purchase**: フルアクセスが必要な場合は、[Purchase Aspose.Imaging](https://purchase.aspose.com/buy) からライセンスをご購入ください。

### Basic Initialization and Setup

```csharp
// Initialize the library with your license
Aspose.Imaging.License license = new Aspose.Imaging.License();
license.SetLicense("Path to your license file");
```

## How to Convert JPEG to TIFF and Add Multiple Frames

実装をいくつかのセクションに分割して解説します。

### Create and Configure TiffOptions for TIFF Image

#### Overview
`TiffOptions` オブジェクトを作成すると、圧縮方式やフォトメトリック解釈など、TIFF ファイルのカスタマイズ設定が可能になります。

#### Step‑by‑Step Implementation

**1. Import Necessary Namespaces**  
以下の名前空間をファイルにインポートしてください。

```csharp
using Aspose.Imaging.FileFormats.Tiff;
using Aspose.Imaging.FileFormats.Tiff.Enums;
using Aspose.Imaging.ImageOptions;
```

**2. Configure TiffOptions**  
CCITT Fax Group 3 圧縮を使用した白黒画像用に `TiffOptions` を設定します。

```csharp
// Create TiffOptions with default settings
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);

// Set bits per sample to 1 (black and white)
outputSettings.BitsPerSample = new ushort[] { 1 };

// Use CCITT Fax Group 3 compression
outputSettings.Compression = TiffCompressions.CcittFax3;

// Define photometric interpretation as MinIsWhite
outputSettings.Photometric = TiffPhotometrics.MinIsWhite;

// Set source to an empty stream for creating new TIFF from scratch
outputSettings.Source = new Aspose.Imaging.Sources.StreamSource(new System.IO.MemoryStream());
```

### Create and Configure TiffImage with Specific Dimensions

#### Overview
`TiffImage` を作成する際にカスタム寸法を指定することで、各 TIFF フレームのサイズを明確に定義できます。

**1. Define Image Dimensions**

```csharp
int newWidth = 500; // Width for each TIFF frame
int newHeight = 500; // Height for each TIFF frame
string path = "@YOUR_OUTPUT_DIRECTORY\\AddFramesToTIFFImage_out.tif";
```

**2. Create a TiffImage Instance**  
指定した寸法と出力設定で `TiffImage` を初期化します。

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    // Logic to add frames will be added here.
}
```

### Load JPEG Files from Directory and Resize Them

#### Overview
Aspose.Imaging を使えば、JPEG 画像の読み込み、リサイズ、TIFF への組み込みがシンプルに行えます。

**1. Load JPEG Images**

```csharp
string dataDir = "@YOUR_DOCUMENT_DIRECTORY"; // Directory containing input images

foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
{
    using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
    {
        // Resize image to match TIFF frame dimensions
        ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
        
        // Additional logic for handling multiple frames will be added here.
    }
}
```

> **Pro tip:** フレーズ **load images from directory** は、上記ループが正確に行っていることを示しています – 対象フォルダー内のすべての JPEG ファイルを列挙します。

### Add Frame to TiffImage and Save It

#### Overview
リサイズした JPEG ピクセルを各フレームにコピーし、マルチフレーム TIFF として保存する手順です。

**1. Initialize the TiffImage Instance**

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    int index = 0; // Frame index tracker
    
    foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
    {
        using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
        {
            ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
            
            TiffFrame frame = tiffImage.ActiveFrame;
            if (index > 0)
            {
                // Create a new frame for each subsequent image
                frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            }
            
            // Copy pixels from the resized JPEG into the TIFF frame
            frame.SavePixels(frame.Bounds, ri.LoadPixels(ri.Bounds));
            if (index > 0)
            {
                tiffImage.AddFrame(frame); // Add to TIFF image only after the first frame
            }
            index++;
        }
    }
    
    tiffImage.Save(path); // Save the final TIFF with all frames
}
```

## Practical Applications

マルチフレーム TIFF 画像作成の実際のユースケース例:

1. **Document Archiving** – スキャンした文書を単一の TIFF ファイルに保存し、データ整合性とアクセス性を確保。  
2. **Medical Imaging** – MRI や CT などの高品質スキャンを圧縮 TIFF 形式で保存。  
3. **Graphic Design** – 複数のデザインレイヤーを 1 ファイルにまとめ、グラフィックソフトでの取り扱いを効率化。  
4. **Photography** – 複数ページのフォトアルバムを単一ファイルでアーカイブし、共有と保存を簡素化。  
5. **Industrial Quality Control** – 検査データを複数フレームに記録し、TIFF 画像として管理。

## Performance Considerations

### Tips for Optimizing Performance
- **Memory Management** – 画像オブジェクトは `using` 文で速やかに破棄し、リソースを解放します。  
- **Batch Processing** – 大量データを扱う場合はバッチ単位で処理し、メモリ使用量を予測可能に保ちます。  
- **Efficient Compression** – シナリオに合わせて品質と速度のバランスが取れた圧縮設定を選択します。

## Frequently Asked Questions

**Q: Can I convert JPEG to TIFF without losing quality?**  
A: はい。LZW や CCITT Fax などのロスレス圧縮オプションを使用し、元のピクセルデータを保持すれば変換はロスレスです。

**Q: Do I need to resize images before adding them as frames?**  
A: すべてのフレームは同一サイズである必要があるため、各 JPEG を対象の幅・高さにリサイズする必要があります。

**Q: How many frames can a TIFF file contain?**  
A: 実質的に無制限です。制限はファイルサイズと利用可能メモリに依存します。

**Q: Is the generated TIFF compatible with common viewers?**  
A: 本サンプルは標準的な CCITT Fax Group 3 圧縮を使用しており、ほとんどの TIFF ビューアやエディタで広くサポートされています。

**Q: What if I want to add a different compression for color images?**  
A: `TiffCompressions.CcittFax3` を `TiffCompressions.Lzw` または `TiffCompressions.Jpeg` に置き換え、`BitsPerSample` を適切に調整してください。

## Conclusion

本チュートリアルでは **convert JPEG to TIFF** の基本手順と、Aspose.Imaging for .NET を使用したマルチフレーム TIFF 画像の作成方法を解説しました。`TiffOptions` の設定からフレーム追加まで、一通りの流れを習得したことで、アプリケーションに高品質イメージングを組み込む土台ができました。

**Next Steps**  
- 他の圧縮タイプやカラーデプスで実験してみましょう。  
- メタデータ操作や PDF 変換など、Aspose.Imaging の追加機能を探求してください。  
- 詳細は [公式ドキュメント](https://reference.aspose.com/imaging/net/) を参照してください。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-02-09  
**Tested With:** Aspose.Imaging for .NET (latest stable version)  
**Author:** Aspose