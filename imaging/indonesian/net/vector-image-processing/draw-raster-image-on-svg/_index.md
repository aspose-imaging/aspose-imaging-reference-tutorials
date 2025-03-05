---
title: Cara Menggambar Gambar Raster di SVG di Aspose.Imaging untuk .NET
linktitle: Gambar Gambar Raster pada SVG di Aspose.Imaging untuk .NET
second_title: Aspose.Imaging .NET API Pemrosesan Gambar
description: Pelajari cara menggambar gambar raster di SVG menggunakan Aspose.Imaging untuk .NET. Sempurnakan aplikasi .NET Anda dengan gambar dinamis.
type: docs
weight: 11
url: /id/net/vector-image-processing/draw-raster-image-on-svg/
---

Dalam dunia pemrograman .NET, Aspose.Imaging berdiri sebagai perpustakaan yang andal dan serbaguna untuk menangani berbagai tugas terkait gambar. Salah satu kemampuan menarik yang ditawarkannya adalah kemampuan menggambar gambar raster pada kanvas SVG. Dalam panduan langkah demi langkah ini, kami akan memandu Anda melalui proses menggambar gambar raster pada SVG menggunakan Aspose.Imaging untuk .NET.

## Prasyarat

Sebelum kita mendalami detailnya, pastikan Anda memiliki prasyarat berikut:

-  Aspose.Imaging untuk .NET: Anda harus menginstal perpustakaan. Jika belum, Anda dapat mendownloadnya dari[Aspose.Imaging untuk halaman unduhan .NET](https://releases.aspose.com/imaging/net/).

-  Direktori Dokumen Anda: Ganti`"Your Document Directory"` dengan jalur sebenarnya ke direktori kerja Anda.

Sekarang, mari kita bagi prosesnya menjadi langkah-langkah yang mudah diikuti:

## Langkah 1: Impor Namespace yang Diperlukan

Anda perlu mengimpor namespace yang diperlukan untuk bekerja dengan Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Langkah 2: Muat Gambar

- Pertama, muat gambar raster yang ingin Anda gambar di kanvas SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Selanjutnya, muat gambar kanvas SVG tempat Anda ingin menggambar gambar raster.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Langkah 3: Menggambar pada Gambar SVG

Sekarang, Anda bisa mulai menggambar pada gambar SVG yang sudah ada. Untuk melakukan ini, Anda perlu membuat sebuah instance dari`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Langkah 4: Gambar Gambar Raster

- Tentukan batas tempat Anda ingin menggambar gambar raster dan tentukan wilayah sumber dari gambar raster.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Langkah 5: Simpan Hasilnya

Setelah menggambar gambar raster pada kanvas SVG, Anda dapat menyimpan gambar yang dihasilkan:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Kesimpulan

Selamat! Anda telah berhasil menggambar gambar raster pada kanvas SVG menggunakan Aspose.Imaging untuk .NET. Ini bisa sangat berguna untuk membuat gambar yang kaya dan dinamis dalam aplikasi .NET Anda.

 Untuk informasi lebih lanjut dan dokumentasi terperinci, kunjungi[Aspose.Imaging untuk dokumentasi .NET](https://reference.aspose.com/imaging/net/).

## Pertanyaan yang Sering Diajukan

### Apa itu Aspose.Imaging untuk .NET?
   Aspose.Imaging for .NET adalah pustaka pemrosesan gambar canggih yang memungkinkan pengembang membuat, memanipulasi, dan mengonversi gambar dalam berbagai format dalam aplikasi .NET.

### Bisakah saya menggunakan Aspose.Imaging untuk .NET dalam proyek komersial?
    Ya, Anda dapat menggunakan Aspose.Imaging untuk .NET di proyek komersial dan non-komersial. Detail perizinan dapat ditemukan di[halaman pembelian](https://purchase.aspose.com/buy).

### Apakah ada uji coba gratis yang tersedia?
    Ya, Anda bisa mendapatkan uji coba gratis Aspose.Imaging untuk .NET dari[Di Sini](https://releases.aspose.com/).

### Di mana saya bisa mendapatkan dukungan atau mengajukan pertanyaan?
    Jika Anda memiliki pertanyaan atau memerlukan dukungan, Anda dapat mengunjungi[Aspose.Forum pencitraan](https://forum.aspose.com/).

### Bagaimana saya bisa mendapatkan lisensi sementara untuk Aspose.Imaging untuk .NET?
    Anda bisa mendapatkan lisensi sementara dari[Di Sini](https://purchase.aspose.com/temporary-license/).


