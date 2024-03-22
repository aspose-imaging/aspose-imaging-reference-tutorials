---
title: Konversi Rentang Halaman DJVU menjadi Gambar Terpisah di Aspose.Imaging untuk .NET
linktitle: Konversi Rentang Halaman DJVU menjadi Gambar Terpisah di Aspose.Imaging untuk .NET
second_title: Aspose.Imaging .NET API Pemrosesan Gambar
description: Temukan cara mengonversi halaman DJVU menjadi gambar terpisah dengan Aspose.Imaging untuk .NET. Panduan langkah demi langkah, contoh kode, dan FAQ disediakan.
type: docs
weight: 19
url: /id/net/image-format-conversion/convert-range-of-djvu-pages-to-separate-images/
---
Jika Anda mencari perpustakaan .NET yang kuat untuk menangani tugas konversi dan manipulasi gambar, Aspose.Imaging untuk .NET adalah pilihan yang tepat. Dalam tutorial ini, kami akan memandu Anda melalui proses mengubah serangkaian halaman DJVU menjadi gambar terpisah menggunakan Aspose.Imaging. Anda akan menemukan petunjuk langkah demi langkah dan cuplikan kode untuk membantu Anda mencapai tugas ini.

## Prasyarat

Sebelum kita mendalami proses konversi, pastikan Anda memiliki prasyarat berikut:

1. Aspose.Imaging untuk Perpustakaan .NET

 Anda harus menginstal Aspose.Imaging untuk .NET. Jika Anda belum melakukannya, Anda dapat mengunduhnya dari[Aspose.Imaging untuk halaman .NET](https://releases.aspose.com/imaging/net/).

2. Pengembangan lingkungan

Untuk mengikutinya, Anda harus menyiapkan lingkungan pengembangan dengan Visual Studio atau .NET IDE lainnya.

## Mengimpor Namespace yang Diperlukan

Pertama, Anda perlu menyertakan namespace yang diperlukan dalam kode Anda agar berfungsi dengan Aspose.Imaging. Inilah cara Anda melakukannya:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Djvu;
using Aspose.Imaging.FileFormats.Djvu.Options;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.RasterImage;
```

## Mengonversi Halaman DJVU

Sekarang, mari kita uraikan proses konversi serangkaian halaman DJVU menjadi gambar terpisah menggunakan Aspose.Imaging untuk .NET menjadi serangkaian langkah yang mudah diikuti.

### Langkah 1: Muat Gambar DJVU

 Untuk memulai, Anda harus memuat gambar DJVU yang ingin Anda konversi. Mengganti`"Your Document Directory"` dengan jalur sebenarnya ke file DJVU Anda.

```csharp
string dataDir = "Your Document Directory";

// Muat gambar DjVu
using (DjvuImage image = (DjvuImage)Image.Load(dataDir + "Sample.djvu"))
{
    // Kode Anda untuk diproses lebih lanjut akan ditempatkan di sini.
}
```

### Langkah 2: Tetapkan Opsi Ekspor

Sekarang, buat sebuah instance dari`BmpOptions` dan konfigurasikan opsi yang diinginkan untuk gambar yang dihasilkan. Dalam contoh ini, kami menetapkan`BitsPerPixel` ke 32.

```csharp
BmpOptions exportOptions = new BmpOptions();
exportOptions.BitsPerPixel = 32;
```

### Langkah 3: Tentukan Rentang Halaman

 Untuk menentukan rentang halaman yang ingin Anda ekspor, buatlah sebuah instance`IntRange` dan inisialisasi dengan rentang halaman. Dalam hal ini, kami mengekspor halaman 0 ke 2.

```csharp
IntRange range = new IntRange(0, 2);
```

### Langkah 4: Ulangi Halaman

Sekarang, telusuri halaman-halaman dalam rentang yang ditentukan dan simpan setiap halaman sebagai gambar BMP terpisah. File DJVU tidak mendukung pelapisan, jadi kami menyimpan setiap halaman satu per satu.

```csharp
int counter = 0;
foreach (var i in range.Range)
{
    exportOptions.MultiPageOptions = new DjvuMultiPageOptions(range.GetArrayOneItemFromIndex(counter));
    image.Save(dataDir + string.Format("{0}_out.bmp", counter++), exportOptions);
}
```

Dan itu saja! Anda telah berhasil mengonversi serangkaian halaman DJVU menjadi gambar terpisah menggunakan Aspose.Imaging untuk .NET.

## Kesimpulan

Aspose.Imaging untuk .NET menyederhanakan tugas konversi gambar, menjadikannya pilihan yang sangat baik bagi pengembang. Dalam tutorial ini, kami memandu Anda melalui proses mengonversi halaman DJVU menjadi gambar terpisah langkah demi langkah. Dengan kode dan pustaka yang tepat, konversi gambar menjadi mudah.

## FAQ

### Q1: Apakah Aspose.Imaging untuk .NET merupakan perpustakaan gratis?

 A1: Tidak, ini adalah perpustakaan komersial, tetapi Anda dapat mengunduh a[uji coba gratis](https://releases.aspose.com/) untuk menguji kemampuannya.

### Q2: Dapatkah saya membeli lisensi sementara untuk Aspose.Imaging untuk .NET?

 A2: Ya, Anda bisa mendapatkan lisensi sementara dari[halaman pembelian](https://purchase.aspose.com/temporary-license/).

### Q3: Di mana saya dapat menemukan dokumentasi Aspose.Imaging untuk .NET?

 A3: Anda dapat menjelajahi dokumentasi yang komprehensif[Di Sini](https://reference.aspose.com/imaging/net/).

### Q4: Format gambar apa yang didukung Aspose.Imaging untuk .NET?

A4: Aspose.Imaging untuk .NET mendukung berbagai format gambar, termasuk BMP, JPEG, PNG, TIFF, dan banyak lagi.

### Q5: Bisakah saya mendapatkan dukungan dan bantuan jika saya mengalami masalah?

 A5: Ya, Anda dapat mencari bantuan dan terhubung dengan komunitas di[Aspose.Forum pencitraan](https://forum.aspose.com/).