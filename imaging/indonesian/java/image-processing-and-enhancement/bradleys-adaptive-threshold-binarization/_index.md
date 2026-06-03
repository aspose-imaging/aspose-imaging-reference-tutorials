---
date: 2026-01-09
description: Pelajari cara membinarisasi gambar menggunakan Aspose.Imaging untuk Java.
  Panduan ini mencakup teknik pemrosesan gambar Java untuk konversi DICOM ke BMP.
linktitle: Bradley's Adaptive Threshold Binarization
second_title: Aspose.Imaging Java Image Processing API
title: Cara Membinarisasi Gambar dengan Aspose.Imaging untuk Java
url: /id/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Cara Membinarisasi Gambar dengan Aspose.Imaging untuk Java

Gambar memainkan peran penting dalam dunia digital, baik di situs web, dokumen, maupun sebagai bagian dari berbagai aplikasi. Jika Anda bertanya-tanya **cara membinarisasi gambar** secara efisien, terutama untuk format medis seperti DICOM, Anda berada di tempat yang tepat. Binarisasi gambar menyederhanakan sebuah foto dengan mengubahnya menjadi representasi hitam‑putih, yang ideal untuk analisis lanjutan, OCR, atau optimalisasi penyimpanan. Dalam tutorial ini kami akan memandu Anda melalui seluruh proses menggunakan Bradley’s Adaptive Threshold Binarization dari Aspose.Imaging untuk Java.

## Jawaban Cepat
- **Apa yang dilakukan binarisasi?** Mengubah setiap piksel menjadi hitam atau putih berdasarkan ambang batas.
- **Perpustakaan mana yang terbaik untuk pemrosesan gambar Java?** Aspose.Imaging untuk Java menyediakan fitur percobaan bebas lisensi yang kuat.
- **Bisakah saya memproses file DICOM secara langsung?** Ya, Aspose.Imaging dapat memuat DICOM dan menghasilkan BMP, PNG, dll.
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi komersial diperlukan untuk penggunaan di luar percobaan.
- **Versi Java apa yang didukung?** Java 8 dan yang lebih baru sepenuhnya kompatibel.

## Apa Itu Binarisasi Gambar?
Binarisasi gambar adalah proses mengubah gambar skala abu‑abu atau berwarna menjadi gambar biner di mana setiap piksel bernilai 0 (hitam) atau 255 (putih). Langkah ini sering menjadi tahap pertama dalam pipeline pemrosesan gambar medis, pemindaian dokumen, dan tugas computer‑vision.

## Mengapa Menggunakan Aspose.Imaging untuk Java?
Aspose.Imaging menawarkan API murni‑Java yang **memuat DICOM**, menerapkan algoritma canggih seperti **Bradley’s Adaptive Threshold**, dan menyimpan hasil dalam format umum tanpa memerlukan perpustakaan native eksternal. Ini ideal untuk **pemrosesan gambar medis**, **mengonversi DICOM ke BMP**, dan alur kerja berbasis Java lainnya.

## Prasyarat

Sebelum menyelam ke kode, pastikan Anda memiliki hal‑hal berikut:

- **Lingkungan Pengembangan Java** – JDK 8 atau yang lebih baru terpasang.
- **Aspose.Imaging untuk Java** – Unduh dari situs resmi: [Download Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/).
- **Gambar DICOM** – File DICOM contoh apa pun yang ingin Anda binarisasi.

Setelah semuanya siap, mari lanjut ke implementasinya.

## Cara Membinarisasi Gambar – Panduan Langkah‑per‑Langkah

### Mengimpor Paket
Pertama, impor kelas Aspose.Imaging yang diperlukan. Potongan kode ini juga mendefinisikan jalur file input dan output.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// Load a DICOM image in an instance of DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Binarize image with Bradley's adaptive threshold.
    image.binarizeBradley(10);
    // Save the resultant image.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

### Langkah 1: Menentukan Jalur
Atur lokasi untuk file DICOM sumber Anda dan file BMP tujuan. Ganti `"Your Document Directory"` dengan folder aktual di sistem Anda.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

### Langkah 2: Memuat Gambar DICOM
Gunakan Aspose.Imaging untuk **memuat gambar dicom** ke dalam objek `DicomImage`. Objek ini memberi Anda akses penuh ke data piksel dan metode pemrosesan.

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // The image processing steps will go here.
}
```

### Langkah 3: Melakukan Binarisasi
Terapkan algoritma Bradley’s Adaptive Threshold. Parameter (`10` dalam contoh ini) mengontrol sensitivitas ambang; Anda dapat bereksperimen dengan nilai berbeda untuk hasil optimal.

```java
image.binarizeBradley(10);
```

### Langkah 4: Menyimpan Gambar Binarisasi
Akhirnya, ekspor gambar yang telah diproses. Di sini kami menggunakan format BMP, tetapi Aspose.Imaging mendukung PNG, JPEG, TIFF, dan banyak lagi.

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## Masalah Umum & Pemecahan Masalah

- **FileNotFoundException** – Pastikan jalur `dataDir` diakhiri dengan garis miring dan nama file DICOM cocok persis.
- **OutOfMemoryError** – File DICOM berukuran besar mungkin memerlukan peningkatan ukuran heap JVM (`-Xmx2g` atau lebih tinggi).
- **Ambang Tidak Tepat** – Jika output terlalu gelap atau terlalu terang, sesuaikan nilai integer yang diberikan ke `binarizeBradley()` (misalnya, 5‑15).

## Pertanyaan yang Sering Diajukan

### Q1: Apa itu DICOM, dan mengapa penting dalam pencitraan medis?
**A:** DICOM adalah singkatan dari Digital Imaging and Communications in Medicine. Ini merupakan standar universal untuk menyimpan, mentransmisikan, dan menangani gambar medis, memungkinkan interoperabilitas antar perangkat dan sistem.

### Q2: Bisakah saya menggunakan Aspose.Imaging untuk Java dalam proyek komersial saya?
**A:** Ya, Aspose.Imaging untuk Java menawarkan percobaan gratis serta lisensi komersial. Anda dapat menjelajahi opsi dan memperoleh lisensi yang diperlukan dari [situs Aspose](https://purchase.aspose.com/buy).

### Q3: Apakah ada lisensi sementara yang tersedia untuk tujuan pengujian?
**A:** Ya, Anda dapat memperoleh lisensi sementara untuk menguji dan mengevaluasi Aspose.Imaging untuk Java. Kunjungi [tautan ini](https://purchase.aspose.com/temporary-license/) untuk informasi lebih lanjut.

### Q4: Di mana saya dapat mencari bantuan atau berdiskusi tentang masalah terkait Aspose.Imaging untuk Java?
**A:** Untuk dukungan komunitas dan diskusi, Anda dapat mengunjungi [forum Aspose.Imaging](https://forum.aspose.com/). Tempat yang bagus untuk menemukan jawaban atas pertanyaan Anda dan terhubung dengan pengguna lain.

### Q5: Apakah Aspose.Imaging untuk Java cocok untuk pemrosesan gambar di aplikasi Java‑lainnya?
**A:** Tentu saja. Perpustakaan ini bekerja dengan baik di aplikasi web, perangkat lunak desktop, alat pemrosesan batch, dan lainnya, menyediakan API konsisten di semua platform.

## Kesimpulan
Anda kini telah mempelajari **cara membinarisasi gambar** menggunakan Aspose.Imaging untuk Java dengan Bradley’s Adaptive Threshold. Teknik ini sangat berharga untuk **pemrosesan gambar medis**, memungkinkan Anda mengonversi file DICOM ke format BMP ringan (atau format lain) untuk analisis atau penyimpanan. Terus bereksperimen dengan ambang yang berbeda dan jelajahi fitur lengkap Aspose.Imaging yang kaya.

Untuk pendalaman lebih lanjut tentang manipulasi gambar, lihat dokumentasi resmi: [Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/).

---

**Terakhir Diperbarui:** 2026-01-09  
**Diuji Dengan:** Aspose.Imaging untuk Java 24.12 (terbaru pada saat penulisan)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}