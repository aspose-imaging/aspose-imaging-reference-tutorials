---
title: Menggambar Persegi Panjang di Aspose.Imaging untuk .NET
linktitle: Gambar Persegi Panjang di Aspose.Imaging untuk .NET
second_title: Aspose.Imaging .NET API Pemrosesan Gambar
description: Belajar menggambar persegi panjang di Aspose.Imaging untuk .NET - alat serbaguna untuk manipulasi gambar di aplikasi .NET Anda.
type: docs
weight: 14
url: /id/net/basic-drawing/draw-rectangle/
---
Membuat dan memanipulasi gambar dalam aplikasi .NET bisa menjadi tugas yang kompleks, namun dengan kekuatan Aspose.Imaging untuk .NET, semuanya menjadi sangat sederhana. Dalam panduan langkah demi langkah ini, kami akan memandu Anda melalui proses menggambar persegi panjang menggunakan Aspose.Imaging untuk .NET. Anda akan belajar cara membuat gambar, mengatur propertinya, menggambar persegi panjang, dan menyimpan pekerjaan Anda. Ayo selami!

## Prasyarat

Sebelum memulai, pastikan Anda memiliki prasyarat berikut:

1.  Aspose.Imaging for .NET: Pastikan Anda telah menginstal perpustakaan Aspose.Imaging for .NET. Jika Anda belum melakukannya, Anda dapat mengunduhnya dari[Unduh Halaman](https://releases.aspose.com/imaging/net/).

2. Lingkungan Pengembangan: Anda harus menyiapkan lingkungan pengembangan dengan Visual Studio atau alat pengembangan .NET lainnya.

Sekarang, mari kita mulai dengan tutorial langkah demi langkah.

## Mengimpor Namespace

Langkah pertama adalah mengimpor namespace yang diperlukan agar berfungsi dengan Aspose.Imaging untuk .NET. Inilah cara Anda melakukannya:

### Langkah 1: Impor Namespace

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Pada kode di atas, kita mengimpor namespace Aspose.Imaging, yang menyediakan kelas dan metode yang diperlukan untuk manipulasi gambar.

## Menggambar Persegi Panjang

Sekarang, mari kita lanjutkan dengan menggambar persegi panjang pada sebuah gambar.

### Langkah 2: Buat Gambar

```csharp
string dataDir = "Your Document Directory";  // Tetapkan jalur ke direktori dokumen Anda
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Kode Anda untuk menggambar persegi panjang akan ditempatkan di sini
        image.Save();
    }
}
```

 Pada langkah ini, kita membuat sebuah instance dari`Image` kelas dan mengatur berbagai properti untuk pembuatan gambar, seperti`BitsPerPixel` dan aliran keluaran. Kami kemudian membuat gambar kosong berukuran 100x100 piksel.

### Langkah 3: Inisialisasi Grafik dan Gambar Persegi Panjang

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

 Pada langkah ini, kami menginisialisasi a`Graphics` objek, bersihkan permukaan grafis dengan latar belakang kuning, dan gambar dua persegi panjang dengan warna dan posisi berbeda pada gambar.

### Langkah 4: Simpan Gambar

```csharp
image.Save();
```

Terakhir, kami menyimpan gambar dengan persegi panjang yang digambar.

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara menggambar persegi panjang pada gambar menggunakan Aspose.Imaging untuk .NET. Dengan mengikuti langkah-langkah yang diuraikan dalam panduan ini, Anda dapat dengan mudah membuat dan memanipulasi gambar dalam aplikasi .NET Anda. Aspose.Imaging menyederhanakan penanganan gambar, menjadikannya alat yang ampuh bagi pengembang.

Sekarang Anda siap untuk memasukkan manipulasi gambar ke dalam proyek .NET Anda menggunakan Aspose.Imaging. Mulailah bereksperimen dan ciptakan visual yang menakjubkan!

## FAQ

### Q1: Bentuk apa lagi yang bisa saya gambar dengan Aspose.Imaging untuk .NET?

A1: Anda dapat menggambar berbagai bentuk seperti elips, garis, dan kurva menggunakan pustaka Aspose.Imaging.

### Q2: Bisakah saya menggunakan Aspose.Imaging untuk .NET di aplikasi Windows dan web?

A2: Ya, Aspose.Imaging for .NET dapat digunakan di aplikasi Windows dan web, sehingga serbaguna untuk berbagai jenis proyek.

### Q3: Apakah Aspose.Imaging untuk .NET merupakan perpustakaan gratis?

 A3: Aspose.Imaging untuk .NET adalah perpustakaan komersial, tetapi Anda dapat menjelajahinya dengan uji coba gratis yang tersedia[Di Sini](https://releases.aspose.com/).

### Q4: Apakah ada fitur pemrosesan gambar tingkat lanjut di Aspose.Imaging untuk .NET?

A4: Ya, Aspose.Imaging for .NET menawarkan berbagai fitur pemrosesan gambar tingkat lanjut, termasuk pengubahan ukuran gambar, rotasi, dan banyak lagi.

### Q5: Di mana saya dapat menemukan lebih banyak sumber daya dan dukungan untuk Aspose.Imaging untuk .NET?

 A5: Anda dapat mengakses dokumentasinya[Di Sini](https://reference.aspose.com/imaging/net/) dan mencari dukungan di[Aspose.Forum pencitraan](https://forum.aspose.com/).