---
"description": "Pelajari binerisasi gambar dengan Aspose.Imaging untuk Java. Ubah gambar DICOM dengan mudah. Jelajahi panduan langkah demi langkah dengan contoh kode."
"linktitle": "Binarisasi Ambang Adaptif Bradley"
"second_title": "API Pemrosesan Gambar Java Aspose.Imaging"
"title": "Binarisasi Gambar dengan Aspose.Imaging untuk Java"
"url": "/id/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/"
"weight": 27
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Binarisasi Gambar dengan Aspose.Imaging untuk Java

Gambar memainkan peran penting dalam dunia digital, baik di situs web, dokumen, atau sebagai bagian dari berbagai aplikasi. Pemrosesan gambar merupakan tugas penting dalam domain ini, dan salah satu operasi mendasarnya adalah binerisasi gambar. Binarisasi menyederhanakan gambar dengan mengubahnya menjadi bentuk biner, sehingga memudahkan komputer untuk memprosesnya. Aspose.Imaging untuk Java adalah alat canggih yang menyediakan berbagai fitur manipulasi gambar, dan dalam tutorial ini, kita akan menjelajahi cara melakukan binerisasi gambar menggunakan Bradley's Adaptive Threshold Binarization milik Aspose.Imaging. 

## Prasyarat

Sebelum menyelami dunia binarisasi gambar dengan Aspose.Imaging untuk Java, mari pastikan Anda memiliki semua yang Anda butuhkan:

### Lingkungan Pengembangan Java

Anda harus memiliki lingkungan pengembangan Java yang sudah disiapkan di sistem Anda. Jika belum, Anda dapat mengunduh dan menginstal Java Development Kit (JDK) dari situs web Oracle.

### Aspose.Imaging untuk Java

Untuk mengikuti tutorial ini, Anda harus menginstal Aspose.Imaging for Java. Anda dapat mengunduhnya dari situs web Aspose menggunakan tautan berikut: [Unduh Aspose.Imaging untuk Java](https://releases.aspose.com/imaging/java/).

### Gambar DICOM

Anda memerlukan citra DICOM yang ingin dibinerisasi. Jika tidak memilikinya, Anda dapat mencari contoh citra DICOM secara daring, atau Anda dapat menggunakan citra DICOM Anda sendiri.

Sekarang setelah prasyarat Anda terpenuhi, mari kita lanjut ke langkah berikutnya.

## Paket Impor

Di bagian ini, kita akan mengimpor paket-paket yang diperlukan dari Aspose.Imaging untuk Java. Paket-paket ini berisi kelas-kelas dan metode-metode yang diperlukan untuk melakukan Bradley's Adaptive Threshold Binarization pada citra DICOM.

```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// Memuat citra DICOM dalam contoh DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Binerisasikan gambar dengan ambang adaptif Bradley.
    image.binarizeBradley(10);
    // Simpan gambar yang dihasilkan.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

## Langkah 1: Tentukan Jalurnya

Pertama, tentukan jalur untuk citra DICOM masukan dan citra biner keluaran. Ganti `"Your Document Directory"` dengan jalur sebenarnya ke direktori Anda.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

## Langkah 2: Muat Gambar DICOM

Gunakan Aspose.Imaging untuk memuat gambar DICOM yang ditentukan oleh `inputFile`Operasi ini menciptakan sebuah contoh `DicomImage` kelas.

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Langkah-langkah pemrosesan gambar akan ada di sini.
}
```

## Langkah 3: Lakukan Binarisasi

Lakukan Binarisasi Ambang Adaptif Bradley pada gambar DICOM yang dimuat. Dalam contoh ini, ambang batas `10` diterapkan.

```java
image.binarizeBradley(10);
```

## Langkah 4: Simpan Gambar Biner

Simpan gambar biner yang dihasilkan ke file keluaran yang ditentukan menggunakan format BMP.

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara melakukan binerisasi gambar dengan Aspose.Imaging untuk Java menggunakan Adaptive Threshold Binarization milik Bradley. Alat canggih ini memungkinkan Anda untuk meningkatkan kemampuan pemrosesan gambar, menjadikannya aset berharga dalam berbagai aplikasi.

Ingatlah untuk menjelajahi dokumentasi Aspose.Imaging yang luas untuk kemungkinan pemrosesan gambar yang lebih banyak: [Dokumentasi Aspose.Imaging untuk Java](https://reference.aspose.com/imaging/java/).

## Pertanyaan yang Sering Diajukan

### Q1: Apa itu DICOM, dan mengapa penting dalam pencitraan medis?

A1: DICOM adalah singkatan dari Digital Imaging and Communications in Medicine, dan merupakan format standar untuk gambar medis dan informasi terkait. DICOM berperan penting dalam penyimpanan, pertukaran, dan interpretasi gambar medis, sehingga sangat penting bagi para profesional perawatan kesehatan dan sistem pencitraan medis.

### Q2: Dapatkah saya menggunakan Aspose.Imaging untuk Java dalam proyek komersial saya?

A2: Ya, Aspose.Imaging untuk Java menawarkan uji coba gratis dan lisensi komersial. Anda dapat menjelajahi pilihan Anda dan memperoleh lisensi yang diperlukan dari [Situs web Aspose](https://purchase.aspose.com/buy).

### Q3: Apakah ada lisensi sementara yang tersedia untuk tujuan pengujian?

A3: Ya, Anda dapat memperoleh lisensi sementara untuk menguji dan mengevaluasi Aspose.Imaging untuk Java. Kunjungi [tautan ini](https://purchase.aspose.com/temporary-license/) untuk informasi lebih lanjut.

### Q4: Di mana saya dapat mencari bantuan atau mendiskusikan masalah yang terkait dengan Aspose.Imaging untuk Java?

A4: Untuk dukungan dan diskusi komunitas, Anda dapat mengunjungi [Forum Aspose.Imaging](https://forum.aspose.com/)Ini adalah tempat yang bagus untuk menemukan jawaban atas pertanyaan Anda dan terhubung dengan pengguna lain.

### Q5: Apakah Aspose.Imaging untuk Java cocok untuk pemrosesan gambar di aplikasi berbasis Java lainnya?

A5: Ya, Aspose.Imaging untuk Java bersifat serbaguna dan dapat digunakan dalam berbagai aplikasi berbasis Java, termasuk aplikasi web, perangkat lunak desktop, dan banyak lagi.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}