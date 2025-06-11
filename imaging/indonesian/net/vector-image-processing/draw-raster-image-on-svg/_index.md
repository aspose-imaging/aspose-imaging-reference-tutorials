---
"description": "Pelajari cara menggambar gambar raster pada SVG menggunakan Aspose.Imaging untuk .NET. Sempurnakan aplikasi .NET Anda dengan gambar dinamis."
"linktitle": "Menggambar Gambar Raster pada SVG di Aspose.Imaging untuk .NET"
"second_title": "API Pemrosesan Gambar Aspose.Imaging .NET"
"title": "Cara Menggambar Gambar Raster pada SVG di Aspose.Imaging untuk .NET"
"url": "/id/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Cara Menggambar Gambar Raster pada SVG di Aspose.Imaging untuk .NET


Dalam dunia pemrograman .NET, Aspose.Imaging merupakan pustaka yang andal dan serbaguna untuk menangani berbagai tugas terkait gambar. Salah satu kemampuan menarik yang ditawarkannya adalah kemampuan untuk menggambar gambar raster pada kanvas SVG. Dalam panduan langkah demi langkah ini, kami akan memandu Anda melalui proses menggambar gambar raster pada SVG menggunakan Aspose.Imaging untuk .NET.

## Prasyarat

Sebelum kita membahas detailnya, pastikan Anda telah memenuhi prasyarat berikut:

- Aspose.Imaging untuk .NET: Anda harus menginstal pustaka tersebut. Jika belum, Anda dapat mengunduhnya dari [Halaman unduhan Aspose.Imaging untuk .NET](https://releases.aspose.com/imaging/net/).

- Direktori Dokumen Anda: Ganti `"Your Document Directory"` dengan jalur sebenarnya ke direktori kerja Anda.

Sekarang, mari kita uraikan prosesnya menjadi langkah-langkah yang mudah diikuti:

## Langkah 1: Impor Namespace yang Diperlukan

Anda perlu mengimpor namespace yang diperlukan untuk bekerja dengan Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Langkah 2: Muat Gambar

- Pertama, muat gambar raster yang ingin Anda gambar pada kanvas SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Berikutnya, muat gambar kanvas SVG tempat Anda ingin menggambar gambar raster.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Langkah 3: Menggambar pada Gambar SVG

Sekarang, Anda dapat mulai menggambar pada gambar SVG yang ada. Untuk melakukan ini, Anda perlu membuat contoh `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Langkah 4: Gambar Gambar Raster

- Tentukan batas di mana Anda ingin menggambar gambar raster dan tentukan wilayah sumber dari gambar raster.

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

Selamat! Anda telah berhasil menggambar gambar raster pada kanvas SVG menggunakan Aspose.Imaging untuk .NET. Ini dapat sangat berguna untuk membuat gambar yang kaya dan dinamis dalam aplikasi .NET Anda.

Untuk informasi lebih lanjut dan dokumentasi terperinci, kunjungi [Dokumentasi Aspose.Imaging untuk .NET](https://reference.aspose.com/imaging/net/).

## Pertanyaan yang Sering Diajukan

### Apa itu Aspose.Imaging untuk .NET?
   Aspose.Imaging untuk .NET adalah pustaka pemrosesan gambar canggih yang memungkinkan pengembang untuk membuat, memanipulasi, dan mengonversi gambar dalam berbagai format dalam aplikasi .NET.

### Dapatkah saya menggunakan Aspose.Imaging untuk .NET dalam proyek komersial?
   Ya, Anda dapat menggunakan Aspose.Imaging untuk .NET dalam proyek komersial dan non-komersial. Detail lisensi dapat ditemukan di [halaman pembelian](https://purchase.aspose.com/buy).

### Apakah ada uji coba gratis yang tersedia?
   Ya, Anda bisa mendapatkan uji coba gratis Aspose.Imaging untuk .NET dari [Di Sini](https://releases.aspose.com/).

### Di mana saya bisa mendapatkan dukungan atau mengajukan pertanyaan?
   Jika Anda memiliki pertanyaan atau memerlukan dukungan, Anda dapat mengunjungi [Forum Aspose.Imaging](https://forum.aspose.com/).

### Bagaimana cara memperoleh lisensi sementara untuk Aspose.Imaging for .NET?
   Anda bisa mendapatkan lisensi sementara dari [Di Sini](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}