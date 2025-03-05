---
title: Binarisasi Gambar dengan Aspose.Imaging untuk Java
linktitle: Binarisasi Ambang Adaptif Bradley
second_title: Aspose.Imaging API Pemrosesan Gambar Java
description: Pelajari binerisasi gambar dengan Aspose.Imaging untuk Java. Ubah gambar DICOM dengan mudah. Jelajahi panduan langkah demi langkah dengan contoh kode.
type: docs
weight: 27
url: /id/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
---
Gambar memainkan peran penting dalam dunia digital, baik di situs web, dokumen, atau sebagai bagian dari berbagai aplikasi. Pemrosesan gambar adalah tugas penting dalam domain ini, dan salah satu operasi mendasarnya adalah binarisasi gambar. Binarisasi menyederhanakan gambar dengan mengubahnya menjadi bentuk biner, sehingga memudahkan komputer untuk memprosesnya. Aspose.Imaging untuk Java adalah alat canggih yang menyediakan berbagai fitur manipulasi gambar, dan dalam tutorial ini, kita akan mempelajari cara melakukan binarisasi gambar menggunakan Binarisasi Ambang Adaptif Bradley dari Aspose.Imaging. 

## Prasyarat

Sebelum terjun ke dunia binarisasi gambar dengan Aspose.Imaging untuk Java, pastikan Anda memiliki semua yang Anda butuhkan:

### Lingkungan Pengembangan Jawa

Anda harus menyiapkan lingkungan pengembangan Java di sistem Anda. Jika Anda belum melakukannya, Anda dapat mengunduh dan menginstal Java Development Kit (JDK) dari situs web Oracle.

### Aspose. Pencitraan untuk Java

Untuk mengikuti tutorial ini, Anda harus menginstal Aspose.Imaging for Java. Anda dapat mendownloadnya dari website Aspose menggunakan link berikut:[Unduh Aspose.Imaging untuk Java](https://releases.aspose.com/imaging/java/).

### Gambar DICOM

Anda memerlukan gambar DICOM yang ingin Anda binarisasi. Jika Anda tidak memilikinya, Anda dapat menemukan contoh gambar DICOM secara online, atau Anda dapat menggunakan gambar DICOM Anda sendiri.

Sekarang setelah prasyarat Anda siap, mari lanjutkan ke langkah berikutnya.

## Paket Impor

Di bagian ini, kita akan mengimpor paket yang diperlukan dari Aspose.Imaging untuk Java. Paket-paket ini berisi kelas dan metode yang diperlukan untuk melakukan Binarisasi Ambang Adaptif Bradley pada gambar DICOM.

```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// Muat gambar DICOM dalam contoh DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Binarkan gambar dengan ambang batas adaptif Bradley.
    image.binarizeBradley(10);
    // Simpan gambar yang dihasilkan.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

## Langkah 1: Tentukan Jalurnya

 Pertama, tentukan jalur untuk gambar DICOM masukan dan gambar biner keluaran. Mengganti`"Your Document Directory"` dengan jalur sebenarnya ke direktori Anda.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

## Langkah 2: Muat Gambar DICOM

Gunakan Aspose.Imaging untuk memuat gambar DICOM yang ditentukan oleh`inputFile` . Operasi ini menciptakan sebuah instance dari`DicomImage` kelas.

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Langkah-langkah pemrosesan gambar akan dijelaskan di sini.
}
```

## Langkah 3: Lakukan Binarisasi

 Lakukan Binarisasi Ambang Adaptif Bradley pada gambar DICOM yang dimuat. Dalam contoh ini, ambang batas sebesar`10` diterapkan.

```java
image.binarizeBradley(10);
```

## Langkah 4: Simpan Gambar Binarisasi

Simpan gambar biner yang dihasilkan ke file keluaran yang ditentukan menggunakan format BMP.

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara melakukan binarisasi gambar dengan Aspose.Imaging untuk Java menggunakan Binarisasi Ambang Adaptif Bradley. Alat canggih ini memungkinkan Anda meningkatkan kemampuan pemrosesan gambar, menjadikannya aset berharga dalam berbagai aplikasi.

 Ingatlah untuk menjelajahi dokumentasi ekstensif Aspose.Imaging untuk kemungkinan pemrosesan gambar yang lebih banyak:[Aspose.Imaging untuk Dokumentasi Java](https://reference.aspose.com/imaging/java/).

## FAQ

### Q1: Apa itu DICOM dan mengapa penting dalam pencitraan medis?

A1: DICOM adalah singkatan dari Digital Imaging and Communications in Medicine, dan merupakan format standar untuk gambar medis dan informasi terkait. Ini memainkan peran penting dalam penyimpanan, pertukaran, dan interpretasi gambar medis, sehingga penting bagi profesional kesehatan dan sistem pencitraan medis.

### Q2: Bisakah saya menggunakan Aspose.Imaging for Java dalam proyek komersial saya?

 A2: Ya, Aspose.Imaging untuk Java menawarkan uji coba gratis dan lisensi komersial. Anda dapat menjelajahi pilihan Anda dan memperoleh lisensi yang diperlukan dari[Situs web Aspose](https://purchase.aspose.com/buy).

### Q3: Apakah ada lisensi sementara yang tersedia untuk tujuan pengujian?

 A3: Ya, Anda bisa mendapatkan lisensi sementara untuk menguji dan mengevaluasi Aspose.Imaging untuk Java. Mengunjungi[Link ini](https://purchase.aspose.com/temporary-license/) untuk informasi lebih lanjut.

### Q4: Di mana saya dapat mencari bantuan atau mendiskusikan masalah terkait Aspose.Imaging untuk Java?

 A4: Untuk dukungan dan diskusi komunitas, Anda dapat mengunjungi[Aspose.Forum pencitraan](https://forum.aspose.com/). Ini adalah tempat yang bagus untuk menemukan jawaban atas pertanyaan Anda dan terhubung dengan pengguna lain.

### Q5: Apakah Aspose.Imaging for Java cocok untuk pemrosesan gambar di aplikasi berbasis Java lainnya?

A5: Ya, Aspose.Imaging for Java serbaguna dan dapat digunakan dalam berbagai aplikasi berbasis Java, termasuk aplikasi web, perangkat lunak desktop, dan banyak lagi.