---
title: Gambar Gambar Vektor ke Gambar Raster di Aspose.Imaging untuk .NET
linktitle: Gambar Gambar Vektor ke Gambar Raster di Aspose.Imaging untuk .NET
second_title: Aspose.Imaging .NET API Pemrosesan Gambar
description: Pelajari cara mengonversi gambar vektor menjadi gambar raster di .NET menggunakan Aspose.Imaging. Panduan langkah demi langkah untuk pemrosesan gambar yang efisien.
type: docs
weight: 13
url: /id/net/vector-image-processing/draw-vector-image-to-raster-image/
---

Apakah Anda ingin mengonversi gambar vektor menjadi gambar raster dengan mudah di aplikasi .NET Anda? Aspose.Imaging untuk .NET memberikan solusi efisien untuk tugas ini. Dalam panduan langkah demi langkah ini, kami akan memandu Anda melalui proses menggambar gambar vektor ke gambar raster menggunakan Aspose.Imaging untuk .NET. 

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

### 1. Aspose.Imaging untuk .NET

 Anda harus menginstal Aspose.Imaging untuk .NET. Jika Anda belum memilikinya, Anda dapat mengunduhnya dari situs web di[Unduh Aspose.Imaging untuk .NET](https://releases.aspose.com/imaging/net/).

### 2. Lingkungan Pengembangan .NET

Pastikan Anda telah menyiapkan lingkungan pengembangan .NET di komputer Anda. Anda dapat menggunakan Visual Studio atau alat pengembangan .NET lainnya.

Sekarang, mari kita uraikan proses menggambar gambar vektor ke gambar raster menjadi langkah-langkah sederhana dan mudah diikuti:

## Langkah 1: Inisialisasi Proyek Anda

Mulailah dengan membuat proyek .NET baru di lingkungan pengembangan Anda. Pastikan Anda memiliki Aspose.Imaging for .NET yang terintegrasi ke dalam proyek Anda.

## Langkah 2: Muat Gambar Vektor

Pada langkah ini, kita memuat gambar vektor (dalam format SVG) yang ingin Anda ubah menjadi gambar raster.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## Langkah 3: Rasterisasi Gambar Vektor

Sekarang, kita perlu melakukan rasterisasi gambar SVG ke format PNG. Di sinilah terjadi konversi dari vektor ke raster.

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## Langkah 4: Muat Gambar Raster

Setelah rasterisasi, muat gambar PNG dari aliran untuk menggambar lebih lanjut.

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## Langkah 5: Gambar Gambar Raster

Sekarang, kita bisa menggambar gambar raster pada gambar SVG yang ada.

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## Langkah 6: Simpan Hasilnya

Terakhir, simpan gambar hasilnya. Anda sekarang memiliki gambar raster yang menyertakan gambar vektor Anda.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## Kesimpulan

Dalam tutorial ini, kami telah mendemonstrasikan cara mengonversi gambar vektor menjadi gambar raster menggunakan Aspose.Imaging untuk .NET. Dengan langkah sederhana ini, Anda dapat dengan mudah mengintegrasikan fungsi ini ke dalam aplikasi .NET Anda.

### Pertanyaan yang Sering Diajukan

### Apa itu Aspose.Imaging untuk .NET?
Aspose.Imaging for .NET adalah pustaka .NET yang menyediakan fitur pemrosesan gambar canggih, termasuk kemampuan untuk bekerja dengan berbagai format gambar, mengonversi gambar, dan melakukan tugas manipulasi gambar tingkat lanjut.

### Di mana saya dapat menemukan dokumentasi Aspose.Imaging untuk .NET?
 Anda dapat menemukan dokumentasi Aspose.Imaging untuk .NET[Di Sini](https://reference.aspose.com/imaging/net/).

### Apakah ada versi uji coba gratis yang tersedia?
 Ya, Anda dapat mengakses uji coba gratis Aspose.Imaging untuk .NET[Di Sini](https://releases.aspose.com/).

### Bagaimana cara mendapatkan lisensi sementara untuk Aspose.Imaging untuk .NET?
 Jika Anda memerlukan lisensi sementara, Anda bisa mendapatkannya[Di Sini](https://purchase.aspose.com/temporary-license/).

### Di mana saya bisa mendapatkan dukungan untuk Aspose.Imaging untuk .NET?
 Untuk dukungan atau pertanyaan apa pun, Anda dapat mengunjungi[Aspose.Forum pencitraan](https://forum.aspose.com/).
