---
title: Opsi Pengubahan Ukuran Gambar DICOM Lainnya di Aspose.Imaging untuk .NET
linktitle: Opsi Pengubahan Ukuran Gambar DICOM Lainnya di Aspose.Imaging untuk .NET
second_title: Aspose.Imaging .NET API Pemrosesan Gambar
description: Pelajari cara mengubah ukuran gambar DICOM menggunakan Aspose.Imaging untuk .NET. Panduan langkah demi langkah untuk manipulasi gambar medis yang efisien.
type: docs
weight: 20
url: /id/net/dicom-image-processing/dicoms-other-image-resizing-options/
---
Apakah Anda ingin bekerja dengan gambar DICOM (Digital Imaging and Communications in Medicine) di aplikasi .NET Anda? Aspose.Imaging for .NET menyediakan seperangkat alat canggih untuk memanipulasi gambar DICOM secara efisien. Dalam tutorial ini, kita akan mempelajari "Opsi Pengubahan Ukuran Gambar Lainnya DICOM" menggunakan Aspose.Imaging untuk .NET. Kami akan membahas prasyarat, mengimpor namespace, dan memberikan panduan langkah demi langkah untuk membantu Anda memahami dan menerapkan pengubahan ukuran gambar DICOM secara efektif.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1. Instal Aspose.Imaging untuk .NET
Untuk bekerja dengan gambar DICOM menggunakan Aspose.Imaging untuk .NET, Anda perlu menginstal perpustakaan. Anda dapat mengunduhnya dari situs web.

[Unduh Aspose.Imaging untuk .NET](https://releases.aspose.com/imaging/net/)

2. Siapkan Lingkungan Pengembangan
Pastikan Anda telah menyiapkan lingkungan pengembangan .NET, termasuk Visual Studio atau IDE lain yang kompatibel.

3. Gambar DICOM
Anda harus memiliki file gambar DICOM (misalnya, "file.dcm") yang ingin Anda ubah ukurannya menggunakan Aspose.Imaging untuk .NET.

## Impor Namespace

Dalam kode C# Anda, Anda perlu mengimpor namespace yang diperlukan untuk menggunakan Aspose.Imaging. Berikut cara melakukannya:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
```

Sekarang, mari kita uraikan proses pengubahan ukuran gambar menjadi beberapa langkah.

## Langkah 1: Muat Gambar DICOM
Untuk memulai, Anda perlu memuat image DICOM dari sistem file Anda.

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
{
    // Kode Anda di sini
}
```

## Langkah 2: Ubah Ukuran Berdasarkan Tinggi Secara Proporsional
Anda dapat mengubah ukuran gambar DICOM secara proporsional dengan menentukan tinggi dalam piksel dan jenis pengubahan ukuran. Dalam contoh ini, kami menggunakan "AdaptiveResample" sebagai tipe pengubahan ukuran.

```csharp
image.ResizeHeightProportionally(100, ResizeType.AdaptiveResample);
```

## Langkah 3: Simpan Gambar yang Diubah Ukurannya
Setelah mengubah ukuran gambar, Anda dapat menyimpannya dalam format yang diinginkan. Di sini, kami menyimpannya sebagai gambar BMP.

```csharp
image.Save(dataDir + "DICOMSOtherImageResizingOptions_out.bmp", new BmpOptions());
```

## Langkah 4: Ubah Ukuran Berdasarkan Lebar Secara Proporsional
Anda juga dapat mengubah ukuran gambar DICOM secara proporsional dengan menentukan lebar dalam piksel dan jenis pengubahan ukuran.

```csharp
image1.ResizeWidthProportionally(150, ResizeType.AdaptiveResample);
```

## Langkah 5: Simpan Gambar yang Diubah Ukurannya
Simpan gambar yang telah diubah ukurannya sebagai gambar BMP, seperti pada langkah sebelumnya.

```csharp
image1.Save(dataDir + "DICOMSOtherImageResizingOptions1_out.bmp", new BmpOptions());
```

Selamat! Anda telah berhasil mengubah ukuran gambar DICOM menggunakan Aspose.Imaging untuk .NET. Perpustakaan ini menawarkan berbagai opsi untuk memanipulasi gambar DICOM, menjadikannya alat yang berharga untuk aplikasi perawatan kesehatan dan pencitraan medis.

## Kesimpulan

Dalam tutorial ini, kita menjelajahi "Opsi Pengubahan Ukuran Gambar Lainnya DICOM" menggunakan Aspose.Imaging untuk .NET. Kami membahas prasyarat, mengimpor namespace, dan memberikan panduan langkah demi langkah untuk mengubah ukuran gambar DICOM. Aspose.Imaging untuk .NET menyederhanakan proses bekerja dengan gambar medis, menawarkan berbagai fitur untuk aplikasi perawatan kesehatan.

Ada pertanyaan lebih lanjut atau butuh bantuan dengan Aspose.Imaging untuk .NET? Lihat dokumentasi atau kunjungi forum komunitas Aspose untuk mendapatkan dukungan:

- [Aspose.Imaging untuk Dokumentasi .NET](https://reference.aspose.com/imaging/net/)
- [Aspose.Imaging untuk Dukungan .NET](https://forum.aspose.com/)

## FAQ

### Q1: Apa itu DICOM?

A1: DICOM adalah singkatan dari Pencitraan Digital dan Komunikasi dalam Kedokteran. Ini adalah standar untuk mengirimkan, menyimpan, dan berbagi gambar medis, seperti sinar-X, MRI, dan CT scan, dalam format digital.

### Q2: Bisakah saya menggunakan Aspose.Imaging untuk .NET secara gratis?

A2: Aspose.Imaging untuk .NET adalah perpustakaan komersial. Anda dapat mengunduh versi uji coba gratis untuk mengevaluasi fitur-fiturnya, tetapi lisensi diperlukan untuk penggunaan penuh.

### Q3: Opsi manipulasi gambar apa lagi yang ditawarkan Aspose.Imaging for .NET?

A3: Aspose.Imaging untuk .NET menyediakan berbagai pilihan pemrosesan gambar, termasuk konversi format, penyempurnaan gambar, dan menggambar pada gambar. Anda dapat menjelajahi serangkaian fitur lengkap di dokumentasi.

### Q4: Apakah Aspose.Imaging untuk .NET cocok untuk aplikasi perawatan kesehatan?

A4: Ya, Aspose.Imaging untuk .NET biasanya digunakan dalam aplikasi perawatan kesehatan untuk menangani gambar DICOM, menjadikannya alat yang berharga untuk pengembangan perangkat lunak pencitraan medis.

### Q5: Bisakah saya mendapatkan lisensi sementara untuk Aspose.Imaging untuk .NET?
w
 A5: Ya, Anda bisa mendapatkan lisensi sementara untuk tujuan pengujian dan evaluasi. Mengunjungi[Halaman Lisensi Sementara Aspose](https://purchase.aspose.com/temporary-license/) untuk informasi lebih lanjut.