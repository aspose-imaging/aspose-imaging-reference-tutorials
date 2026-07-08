---
date: '2026-07-08'
description: Pelajari cara mengekspor TIFF dari DjVu menggunakan Aspose.Imaging untuk
  Java. Panduan langkah demi langkah yang mencakup pemuatan, pemilihan halaman, dan
  opsi ekspor.
keywords:
- how to export tiff
- java image processing
- maven aspose imaging
- how to load djvu
lastmod: '2026-07-08'
og_description: Temukan cara mengekspor TIFF dari DjVu di Java menggunakan Aspose.Imaging.
  Ikuti tutorial langkah demi langkah kami untuk konversi gambar yang cepat dan andal.
og_image_alt: Guide showing Java code to convert DjVu pages to TIFF with Aspose.Imaging
og_title: Cara Mengekspor TIFF – Panduan Java dengan Aspose.Imaging
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: Learn how to export TIFF from DjVu using Aspose.Imaging for Java. Step-by-step
    guide covering loading, page selection, and export options.
  headline: How to Export TIFF – Load and Export DjVu Pages in Java with Aspose.Imaging
  type: TechArticle
- description: Learn how to export TIFF from DjVu using Aspose.Imaging for Java. Step-by-step
    guide covering loading, page selection, and export options.
  name: How to Export TIFF – Load and Export DjVu Pages in Java with Aspose.Imaging
  steps:
  - name: '**Archival Systems** – Preserve scanned documents in a universally accepted
      format.'
    text: '**Archival Systems** – Preserve scanned documents in a universally accepted
      format.'
  - name: '**Document Review Workflows** – Pull out only the pages that need annotation.'
    text: '**Document Review Workflows** – Pull out only the pages that need annotation.'
  - name: '**Integration with DMS** – Feed TIFF images into existing document‑management
      pipelines that do not understand DjVu.'
    text: '**Integration with DMS** – Feed TIFF images into existing document‑management
      pipelines that do not understand DjVu.'
  type: HowTo
- questions:
  - answer: '`DjvuImage` represents a DjVu document in memory.'
    question: What is the main class for DjVu handling?
  - answer: Just two lines after loading the image.
    question: How many lines of code are needed to export a page to TIFF?
  - answer: '`com.aspose:aspose-imaging` (version 25.5+).'
    question: Which Maven artifact provides DjVu support?
  - answer: Yes, use `IntRange` to specify a range.
    question: Can I export multiple pages at once?
  - answer: A full license is required; a temporary trial is available.
    question: Do I need a license for production?
  type: FAQPage
tags:
- convert DjVu
- Aspose.Imaging
- Java image conversion
title: Cara Mengekspor TIFF – Memuat dan Mengekspor Halaman DjVu di Java dengan Aspose.Imaging
url: /id/java/format-conversion-export/load-export-djvu-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Cara Mengekspor TIFF – Memuat dan Mengekspor Halaman DjVu di Java dengan Aspose.Imaging

## Pendahuluan

Jika Anda perlu **how to export TIFF** dari dokumen DjVu dalam aplikasi Java, Anda berada di tempat yang tepat. DjVu adalah format kompak untuk dokumen yang dipindai, tetapi banyak sistem hilir memerlukan TIFF. Tutorial ini memandu Anda melalui proses memuat file DjVu, memilih halaman yang diperlukan, dan mengekspornya sebagai gambar TIFF berkualitas tinggi menggunakan Aspose.Imaging untuk Java. Pada akhir tutorial, Anda akan memiliki potongan kode yang dapat digunakan kembali dan cocok untuk pipeline pemrosesan gambar berbasis Java mana pun.

**Apa yang Akan Anda Pelajari**
- Cara memuat gambar DjVu menggunakan Aspose.Imaging di Java  
- Mengekspor halaman DjVu tertentu ke format TIFF  
- Mengonfigurasi opsi ekspor dan memahami parameter kunci  

Sebelum kita mulai, pastikan lingkungan pengembangan Anda memenuhi prasyarat yang tercantum di bawah ini.

## Jawaban Cepat
- **Apa kelas utama untuk penanganan DjVu?** `DjvuImage` mewakili dokumen DjVu dalam memori.  
- **Berapa baris kode yang diperlukan untuk mengekspor halaman ke TIFF?** Hanya dua baris setelah memuat gambar.  
- **Artefak Maven mana yang menyediakan dukungan DjVu?** `com.aspose:aspose-imaging` (versi 25.5+).  
- **Bisakah saya mengekspor beberapa halaman sekaligus?** Ya, gunakan `IntRange` untuk menentukan rentang.  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi penuh diperlukan; lisensi percobaan sementara tersedia.

## Apa itu “how to export tiff”?
**“How to export TIFF”** mengacu pada proses mengonversi gambar atau halaman dokumen menjadi Tagged Image File Format (TIFF), format lossless yang banyak digunakan untuk arsip dan pencetakan. Aspose.Imaging menangani konversi ini dalam satu panggilan API sambil mempertahankan resolusi dan pengaturan kompresi. Konversi ini mempertahankan semua detail visual, menjadikannya cocok untuk penyimpanan arsip berkualitas tinggi dan pemrosesan hilir.

## Mengapa menggunakan Aspose.Imaging untuk pemrosesan gambar Java?
Aspose.Imaging mendukung **150+** format input dan output, memproses file hingga **5.000 halaman** tanpa memuat seluruh dokumen ke memori, dan menawarkan operasi yang thread‑safe. Kemampuan terukur ini menjadikannya pilihan yang dapat diandalkan untuk beban kerja pemrosesan gambar Java dengan throughput tinggi, terutama saat menangani set dokumen besar yang memerlukan konversi batch dan overhead memori minimal.

## Prasyarat

- **Aspose.Imaging for Java Library** – versi 25.5 atau lebih baru.  
- **Java Development Kit (JDK)** – 8 atau lebih baru, dikonfigurasi dengan benar di mesin Anda.  
- **Pengetahuan dasar Java** – Anda harus nyaman dengan I/O file dan penanganan pengecualian.

## Cara mengatur Maven Aspose Imaging?
Untuk menyertakan Aspose.Imaging dalam proyek Maven, tambahkan dependensi ke `pom.xml` proyek. Maven akan mengunduh pustaka dan dependensi transitifnya, membuat API tersedia untuk kompilasi dan runtime. Setelah menambahkan potongan kode, jalankan `mvn clean install` untuk memastikan artefak terresolusi dan proyek berhasil dibangun.

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

## Cara mengatur Gradle Aspose Imaging?
Untuk build Gradle, deklarasikan dependensi Aspose.Imaging di file `build.gradle`. Gradle akan mengambil pustaka dari Maven Central, memungkinkan Anda menggunakan API dalam kode Java Anda. Setelah memperbarui skrip, segarkan proyek untuk mengunduh JAR dan menyinkronkan dependensi.

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

## Unduhan Langsung

Anda juga dapat mengunduh JAR terbaru dari [Aspose.Imaging releases](https://releases.aspose.com/imaging/java/).

### Akuisisi Lisensi

- **Free Trial** – dapatkan lisensi sementara untuk evaluasi.  
- **Purchase** – pertimbangkan membeli lisensi penuh untuk penggunaan produksi.

## Inisialisasi dan Penyiapan

Sebelum menggunakan API apa pun, Anda harus menginisialisasi pustaka. `License` adalah kelas yang digunakan untuk menerapkan file lisensi Aspose.Imaging Anda ke pustaka, memastikan fungsionalitas penuh tanpa batasan evaluasi.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path/to/your/license.lic");
```

## Cara memuat DjVu?

`DjvuImage` adalah objek tingkat‑atas yang mewakili file DjVu dalam memori. Untuk membaca dokumen DjVu, panggil metode statis `Image.load()` dengan jalur file; metode ini mengembalikan instance `Image` yang Anda cast ke `DjvuImage`. `Image.load()` adalah metode statis yang membaca file gambar dan mengembalikan objek `Image` yang mewakili konten yang dimuat.

```java
   String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "/Sample.djvu";
   ```

```java
   try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
       // The image is now loaded and ready for further processing.
   }
   ```

### Pemecahan Masalah

- Verifikasi bahwa jalur file benar dan dapat diakses.  
- Bungkus pemanggilan load dalam blok try‑catch untuk menangani `IOException` atau `ImageLoadException`.

## Cara mengekspor TIFF?

Mengekspor halaman DjVu ke TIFF melibatkan pembuatan objek `TiffOptions` yang menentukan kompresi, resolusi, dan pengaturan lainnya, kemudian memanggil metode `save()` pada halaman yang diinginkan. `TiffOptions` adalah kelas yang menyimpan konfigurasi untuk output TIFF, seperti jenis kompresi dan kedalaman warna. Gunakan `IntRange` untuk memilih halaman yang akan dikonversi, kemudian iterasi dan simpan setiap halaman sebagai file TIFF terpisah.

Buat direktori output, atur `TiffOptions`, pilih halaman dengan `IntRange`, dan akhirnya simpan setiap halaman sebagai file TIFF.

```java
   String outputDir = "YOUR_OUTPUT_DIRECTORY" + "/ConvertDjvuPagesToTiff_out.tiff";
   ```

```java
   TiffOptions exportOptions = new TiffOptions(TiffExpectedFormat.TiffDeflateBw);
   ```

```java
   IntRange range = new IntRange(0, 2); // Export the first three pages.
   exportOptions.setMultiPageOptions(new DjvuMultiPageOptions(range));
   ```

```java
   try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
       image.save(outputDir, exportOptions);
   }
   ```

### Kesalahan Umum

- Pastikan `outputDir` ada; jika tidak, `save()` akan melempar pengecualian.  
- Ingat bahwa indeks halaman **berbasis nol**; halaman 1 memiliki indeks 0.  

## Aplikasi Praktis

Mengekspor halaman DjVu ke TIFF berguna dalam banyak skenario:

1. **Sistem Arsip** – Menjaga dokumen yang dipindai dalam format yang diterima secara universal.  
2. **Alur Kerja Review Dokumen** – Mengambil hanya halaman yang memerlukan anotasi.  
3. **Integrasi dengan DMS** – Menyalurkan gambar TIFF ke pipeline manajemen dokumen yang ada yang tidak memahami DjVu.  

## Pertimbangan Kinerja

Saat menangani file DjVu besar:

- Gunakan **try‑with‑resources** untuk secara otomatis menutup stream dan membebaskan memori.  
- Proses file dalam potongan (mis., 10 halaman sekaligus) untuk menjaga jejak heap tetap rendah.  
- Lebih pilih `TiffCompression.CCITT4` untuk pemindaian hitam‑putih guna mengurangi ukuran file tanpa kehilangan kualitas.  

## Pertanyaan yang Sering Diajukan

**Q:** Bagaimana cara menginstal Aspose.Imaging untuk Java dalam proyek saya?  
**A:** Gunakan Maven atau Gradle seperti yang ditunjukkan di atas, atau unduh langsung dari [Aspose's releases page](https://releases.aspose.com/imaging/java/).

**Q:** Bisakah saya mengekspor gambar DjVu ke format selain TIFF?  
**A:** Ya, Aspose.Imaging juga mendukung PNG, JPEG, BMP, dan banyak format lainnya.

**Q:** Apa yang harus saya lakukan jika file lisensi saya tidak dikenali?  
**A:** Verifikasi bahwa jalur lisensi benar dan Anda memanggil `License.setLicense()` sebelum penggunaan API lainnya.

**Q:** Bagaimana saya dapat menangani file DjVu yang sangat besar secara efisien?  
**A:** Proses dokumen dalam rentang halaman yang lebih kecil dan lepaskan setiap instance `DjvuImage` dengan cepat untuk menghindari tekanan memori.

**Q:** Apakah Aspose.Imaging gratis untuk penggunaan komersial?  
**A:** Lisensi percobaan sementara gratis, tetapi lisensi yang dibeli diperlukan untuk penerapan produksi.

## Sumber Daya

- **Documentation**: [Aspose.Imaging Java API Reference](https://reference.aspose.com/imaging/java/)  
- **Download**: [Aspose.Imaging for Java Releases](https://releases.aspose.com/imaging/java/)  
- **Purchase**: [Buy Aspose.Imaging](https://purchase.aspose.com/buy)  
- **Free License**: [Get a Free License](https://releases.aspose.com/imaging/java/)  
- **Temporary License**: [Request a Temporary License](https://purchase.aspose.com/temporary-license/)  
- **Support**: [Aspose Community Forum](https://forum.aspose.com/c/imaging/14)

Dengan menguasai langkah-langkah di atas, Anda dapat dengan andal **how to export TIFF** dari file DjVu dalam solusi berbasis Java apa pun. Selamat coding!

---

**Last Updated:** 2026-07-08  
**Tested With:** Aspose.Imaging 25.5 for Java  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Create Multi-Page TIFF with Aspose.Imaging for Java: A Complete Guide](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Convert DjVu to PDF using Aspose.Imaging for Java - Step-by-Step Guide](/imaging/java/image-loading-saving/convert-djvu-to-pdf-aspose-imaging-java/)
- [Convert DJVU to BMP in Java with Aspose.Imaging: Step-by-Step Guide](/imaging/java/format-conversion-export/export-djvu-pages-bmp-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}