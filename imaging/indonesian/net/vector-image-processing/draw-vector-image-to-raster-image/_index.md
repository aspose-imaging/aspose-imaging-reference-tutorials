---
"description": "Pelajari cara mengonversi gambar vektor ke gambar raster di .NET menggunakan Aspose.Imaging. Panduan langkah demi langkah untuk pemrosesan gambar yang efisien."
"linktitle": "Mengubah Gambar Vektor Menjadi Gambar Raster di Aspose.Imaging untuk .NET"
"second_title": "API Pemrosesan Gambar Aspose.Imaging .NET"
"title": "Mengubah Gambar Vektor Menjadi Gambar Raster di Aspose.Imaging untuk .NET"
"url": "/id/net/vector-image-processing/draw-vector-image-to-raster-image/"
"weight": 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Mengubah Gambar Vektor Menjadi Gambar Raster di Aspose.Imaging untuk .NET


Apakah Anda ingin mengonversi gambar vektor ke gambar raster dengan mudah di aplikasi .NET Anda? Aspose.Imaging for .NET menyediakan solusi efisien untuk tugas ini. Dalam panduan langkah demi langkah ini, kami akan memandu Anda melalui proses menggambar gambar vektor ke gambar raster menggunakan Aspose.Imaging for .NET. 

## Prasyarat

Sebelum kita masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

### 1. Aspose.Imaging untuk .NET

Anda harus sudah menginstal Aspose.Imaging for .NET. Jika Anda belum memilikinya, Anda dapat mengunduhnya dari situs web di [Unduh Aspose.Imaging untuk .NET](https://releases.aspose.com/imaging/net/).

### 2. Lingkungan Pengembangan .NET

Pastikan Anda telah menyiapkan lingkungan pengembangan .NET di komputer Anda. Anda dapat menggunakan Visual Studio atau alat pengembangan .NET lainnya.

Sekarang, mari kita uraikan proses mengubah gambar vektor menjadi gambar raster menjadi beberapa langkah sederhana dan mudah diikuti:

## Langkah 1: Inisialisasi Proyek Anda

Mulailah dengan membuat proyek .NET baru di lingkungan pengembangan Anda. Pastikan Anda telah mengintegrasikan Aspose.Imaging for .NET ke dalam proyek Anda.

## Langkah 2: Muat Gambar Vektor

Pada langkah ini, kami memuat gambar vektor (dalam format SVG) yang ingin Anda ubah menjadi gambar raster.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## Langkah 3: Rasterisasi Gambar Vektor

Sekarang, kita perlu mengubah gambar SVG menjadi format PNG. Di sinilah konversi dari vektor ke raster terjadi.

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## Langkah 4: Muat Gambar Raster

Setelah rasterisasi, muat gambar PNG dari aliran untuk penggambaran lebih lanjut.

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## Langkah 5: Gambar Gambar Raster

Sekarang, kita dapat menggambar gambar raster pada gambar SVG yang ada.

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

Terakhir, simpan gambar hasil. Sekarang Anda memiliki gambar raster yang menyertakan gambar vektor.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## Kesimpulan

Dalam tutorial ini, kami telah menunjukkan cara mengonversi gambar vektor ke gambar raster menggunakan Aspose.Imaging for .NET. Dengan langkah-langkah sederhana ini, Anda dapat dengan mudah mengintegrasikan fungsionalitas ini ke dalam aplikasi .NET Anda.

### Pertanyaan yang Sering Diajukan

### Apa itu Aspose.Imaging untuk .NET?
Aspose.Imaging untuk .NET adalah pustaka .NET yang menyediakan fitur pemrosesan gambar canggih, termasuk kemampuan untuk bekerja dengan berbagai format gambar, mengonversi gambar, dan melakukan tugas manipulasi gambar tingkat lanjut.

### Di mana saya dapat menemukan dokumentasi untuk Aspose.Imaging for .NET?
Anda dapat menemukan dokumentasi untuk Aspose.Imaging untuk .NET [Di Sini](https://reference.aspose.com/imaging/net/).

### Apakah ada versi uji coba gratis yang tersedia?
Ya, Anda dapat mengakses uji coba gratis Aspose.Imaging untuk .NET [Di Sini](https://releases.aspose.com/).

### Bagaimana cara mendapatkan lisensi sementara untuk Aspose.Imaging untuk .NET?
Jika Anda memerlukan lisensi sementara, Anda dapat memperolehnya [Di Sini](https://purchase.aspose.com/temporary-license/).

### Di mana saya bisa mendapatkan dukungan untuk Aspose.Imaging untuk .NET?
Untuk dukungan atau pertanyaan apa pun, Anda dapat mengunjungi [Forum Aspose.Imaging](https://forum.aspose.com/).


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}