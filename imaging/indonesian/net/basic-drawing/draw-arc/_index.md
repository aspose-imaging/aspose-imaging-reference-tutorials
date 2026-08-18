---
date: 2026-02-09
description: Pelajari cara menggambar busur menggunakan Aspose.Imaging untuk .NET,
  termasuk cara menyimpan file BMP, mengatur ukuran gambar, dan mengatur latar belakang
  grafik. Panduan langkah demi langkah untuk menghasilkan gambar BMP.
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Cara Menggambar Busur dengan Aspose.Imaging untuk .NET
url: /id/net/basic-drawing/draw-arc/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Cara Menggambar Busur dengan Aspose.Imaging for .NET

Dalam dunia pemrosesan gambar, **cara menggambar busur** adalah tugas umum yang dapat menambahkan sentuhan visual pada grafik apa pun. Dengan Aspose.Imaging for .NET Anda dapat menghasilkan gambar BMP, mengatur ukuran gambar, dan menggambar busur dengan pena dalam beberapa baris kode C#. Pada akhir tutorial ini Anda akan mengetahui cara menggambar busur, mengatur latar belakang grafik, dan menyimpan file BMP yang dihasilkan dengan mudah.

## Jawaban Cepat
- **Apa yang dihasilkan kode?** Gambar BMP 100 × 100 piksel dengan latar belakang kuning dan busur hitam.  
- **Pustaka mana yang digunakan?** Aspose.Imaging for .NET.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya mengubah ukuran gambar?** Ya – ubah parameter lebar dan tinggi pada pemanggilan `Image.Create`.  
- **Apakah format output tetap?** Contoh ini menyimpan file BMP, tetapi format apa pun yang didukung oleh Aspose.Imaging dapat digunakan.

## Apa itu “cara menggambar busur” dalam Aspose.Imaging?
Menggambar busur berarti merender segmen garis melengkung yang didefinisikan oleh persegi panjang pembatas, sudut awal, dan sudut putar. Aspose.Imaging menyediakan metode `Graphics.DrawArc`, yang memungkinkan Anda **menggambar busur dengan pena** dan mengontrol setiap aspek visual.

## Mengapa menggunakan Aspose.Imaging untuk tugas ini?
- **Kontrol penuh** atas dimensi gambar, kedalaman warna, dan format file.  
- **Tanpa dependensi eksternal** – semuanya berjalan pada .NET murni.  
- **Kinerja tinggi** untuk menghasilkan banyak grafik di sisi server.  

## Prasyarat

Sebelum kita masuk ke kode, pastikan Anda memiliki hal berikut:

1. **Aspose.Imaging for .NET** – unduh dari situs resmi [di sini](https://releases.aspose.com/imaging/net/).  
2. **Lingkungan pengembangan .NET** (Visual Studio, VS Code, atau kompiler C# apa pun).  

Setelah prasyarat kami siap, mari mulai menggambar!

## Mengimpor Namespace yang Diperlukan

Untuk bekerja dengan Aspose.Imaging Anda perlu memasukkan namespace yang relevan ke dalam ruang lingkup:

### Langkah 1: Impor Namespace

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

Pernyataan `using` ini memberi Anda akses ke kelas pembuatan gambar, penanganan grafik, dan I/O file.

## Cara Menggambar Busur dengan Aspose.Imaging for .NET

Kami akan membagi proses menjadi tiga langkah jelas: membuat gambar, menyiapkan permukaan grafik, dan akhirnya menggambar busur.

### Langkah 1: Menyiapkan Gambar (atur ukuran gambar & hasilkan gambar BMP)

```csharp
// Specify the directory where you want to save the image
string dataDir = "Your Document Directory";

// Create an instance of FileStream to save the image
using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
{
    // Create an instance of BmpOptions and set its properties
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;

    // Set the source for BmpOptions and create an instance of Image
    saveOptions.Source = new StreamSource(stream);
    using (Image image = Image.Create(saveOptions, 100, 100))
    {
```

Di sini kami **mengatur ukuran gambar** menjadi 100 × 100 piksel dan mengonfigurasi opsi BMP. `FileStream` memastikan kami **menyimpan file BMP** ke lokasi yang diinginkan.

### Langkah 2: Inisialisasi Graphics dan Mengatur Latar Belakang Grafik

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

Objek `Graphics` memungkinkan kami melukis pada gambar. Dengan memanggil `Clear(Color.Yellow)` kami **mengatur latar belakang grafik** menjadi kuning cerah, sehingga busur terlihat menonjol.

### Langkah 3: Menentukan Parameter Busur dan Menggambar Busur dengan Pena

```csharp
        // Define the parameters for the arc
        int width = 100;
        int height = 200;
        int startAngle = 45;
        int sweepAngle = 270;

        // Draw the arc
        graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);

        // Save the changes
        image.Save();
    }
    stream.Close();
}
```

- `width` dan `height` menentukan persegi panjang pembatas, secara efektif **mengatur ukuran gambar** untuk busur.  
- Objek `Pen` adalah yang memungkinkan kami **menggambar busur dengan pena** berwarna hitam.  
- Setelah menggambar, `image.Save()` menulis **file BMP** ke disk.

## Masalah Umum & Tips
- **Busur tidak terlihat?** Pastikan warna pena kontras dengan latar belakang (misalnya, hitam pada kuning).  
- **Dimensi tidak tepat?** Ingat bahwa persegi panjang pembatas busur dapat lebih besar daripada gambar; sesuaikan `width`/`height` atau ukuran gambar sesuai.  
- **Tip kinerja:** Gunakan kembali satu instance `Graphics` jika Anda perlu menggambar beberapa bentuk pada gambar yang sama.

## FAQ

### Q1: Di mana saya dapat menemukan dokumentasi untuk Aspose.Imaging for .NET?

A1: Anda dapat merujuk ke dokumentasi [di sini](https://reference.aspose.com/imaging/net/) untuk informasi lengkap tentang Aspose.Imaging for .NET.

### Q2: Bagaimana cara mengunduh Aspose.Imaging for .NET?

A2: Anda dapat mengunduh Aspose.Imaging for . .NET dari situs web [di sini](https://releases.aspose.com/imaging/net/).

### Q3: Apakah ada versi percobaan gratis untuk Aspose.Imaging for .NET?

A3: Ya, Anda dapat mendapatkan versi percobaan gratis [di sini](https://releases.aspose.com/) untuk mencoba Aspose.Imaging for .NET.

### Q4: Apakah saya memerlukan lisensi sementara untuk Aspose.Imaging for .NET?

A4: Jika Anda memerlukan lisensi sementara, Anda dapat memperoleh satu [di sini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat mencari dukungan atau mengajukan pertanyaan tentang Aspose.Imaging for .NET?

A5: Anda dapat mengunjungi forum Aspose.Imaging untuk dukungan dan diskusi [di sini](https://forum.aspose.com/).

**Terakhir Diperbarui:** 2026-02-09  
**Diuji Dengan:** Aspose.Imaging 24.11 for .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}