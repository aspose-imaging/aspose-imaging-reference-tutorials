---
date: '2026-06-28'
description: Pelajari cara mengonversi ODP ke PNG menggunakan Aspose.Imaging for Java,
  mengatur font kustom, dan menonaktifkan font sistem untuk rendering yang akurat.
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: Cara Mengonversi ODP ke PNG dengan Aspose.Imaging for Java – Panduan Font Kustom
  & Ekspor
url: /id/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Cara Mengonversi ODP ke PNG dengan Aspose.Imaging untuk Java – Font Kustom & Panduan Ekspor

Dalam aplikasi Java modern, mengonversi file OpenDocument Presentation (ODP) menjadi gambar PNG berkualitas tinggi merupakan kebutuhan umum—terutama ketika Anda perlu mempertahankan merek melalui font kustom. Tutorial ini menunjukkan **cara mengonversi ODP** ke PNG menggunakan Aspose.Imaging untuk Java, memandu Anda melalui penetapan folder font kustom, menonaktifkan font fallback sistem, dan menyetel opsi rasterisasi untuk kinerja optimal.

**What You’ll Learn**
- Cara menetapkan direktori font kustom untuk konversi ODP.  
- Cara menonaktifkan font alternatif sistem sehingga hanya tipe huruf pilihan Anda yang digunakan.  
- Cara mengekspor file ODP ke PNG dengan dimensi dan pengaturan font yang tepat.  
- Tips untuk meningkatkan kecepatan dan penggunaan memori saat memproses presentasi besar.

## Jawaban Cepat
- **Apakah saya dapat menggunakan Maven untuk menambahkan Aspose.Imaging?** Ya, tambahkan dependensi Maven dan jalankan `mvn install`.  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi Aspose.Imaging yang valid diperlukan untuk penggunaan tak terbatas.  
- **Apakah font kustom saya akan dihormati?** Tetapkan folder font dan nonaktifkan alternatif sistem untuk memaksakan penggunaannya.  
- **Format gambar apa yang didukung?** Aspose.Imaging mendukung lebih dari 120 format raster dan vektor, termasuk PNG, JPEG, TIFF, dan WebP.  
- **Apakah API thread‑safe?** Ya, sebagian besar kelas Aspose.Imaging aman untuk penggunaan bersamaan ketika Anda membuat instance terpisah per thread.

## Apa itu “cara mengonversi odp”?
*“Cara mengonversi odp”* mengacu pada proses mengubah file OpenDocument Presentation menjadi format lain—biasanya PNG—dengan mempertahankan tata letak, font, dan kesetiaan visual. Aspose.Imaging untuk Java menyediakan alur kerja satu‑metode yang menangani konversi ini tanpa memerlukan alat eksternal, memungkinkan pengembang mengintegrasikan konversi langsung ke dalam aplikasi mereka dengan kode minimal.

## Mengapa Menggunakan Aspose.Imaging untuk Java?
Aspose.Imaging mendukung **lebih dari 120 format output** dan dapat meraster file ODP multi‑halaman tanpa memuat seluruh dokumen ke memori, mengurangi penggunaan RAM puncak hingga 70 % pada presentasi besar. Perpustakaan ini juga menawarkan manajemen font bawaan, menghilangkan kebutuhan akan mesin rendering pihak ketiga.

## Prasyarat
- **Libraries**: Aspose.Imaging for Java ≥ 25.5.  
- **JDK**: Versi 8 atau lebih baru.  
- **IDE**: IntelliJ IDEA, Eclipse, atau editor kompatibel Java apa pun.  
- **Basic Knowledge**: Java I/O, pemrograman berorientasi objek, dan konsep gambar.

## Instruksi Instalasi

### Maven
Tambahkan dependensi berikut ke `pom.xml` Anda dan jalankan `mvn clean install`:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
Sertakan perpustakaan dalam file `build.gradle` Anda dan segarkan proyek:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Unduh Langsung
Unduh JAR terbaru dari [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

## Langkah-langkah Akuisisi Lisensi
Untuk membuka semua fungsi, terapkan lisensi sementara atau permanen:

1. **Free Trial** – Tidak memerlukan lisensi, fitur terbatas.  
2. **Temporary License** – Minta lisensi di [Aspose website](https://purchase.aspose.com/temporary-license/).  
3. **Purchase** – Beli langganan atau lisensi permanen dari [Aspose purchase page](https://purchase.aspose.com/buy).

Inisialisasi perpustakaan dengan file lisensi Anda:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## Cara menetapkan direktori font kustom untuk konversi ODP?
`FontSettings` adalah kelas yang mengelola sumber daya font untuk Aspose.Imaging. Muat font kustom Anda sebelum pemrosesan gambar dimulai. Ini memastikan setiap slide menggunakan tipe huruf yang tepat yang Anda sediakan.

Tetapkan path folder font menggunakan `FontSettings` Aspose.Imaging:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Definition anchor*: `FontSettings.setFontsFolder` memberi tahu Aspose.Imaging di mana mencari font TrueType dan OpenType di sistem file.

## Cara menonaktifkan font alternatif sistem selama konversi ODP?
Menonaktifkan alternatif sistem memaksa mesin rendering mengabaikan font yang terpasang pada sistem operasi, menjamin hanya font yang Anda sediakan yang digunakan. Ini menghilangkan substitusi font tak terduga yang dapat mengubah tampilan visual slide Anda.

Nonaktifkan alternatif sistem dengan pemanggilan berikut:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Definition anchor*: `FontSettings.setGetSystemAlternativeFont(false)` memaksa mesin menggunakan hanya font yang berada di folder yang Anda tentukan, menghilangkan substitusi tak terduga.

## Cara mengekspor file ODP ke PNG dengan font yang ditentukan?
`RasterizationOptions` menentukan bagaimana halaman vektor diraster menjadi gambar bitmap. Dengan menggabungkan konfigurasi font dengan pengaturan rasterisasi, Anda dapat mengontrol DPI, warna latar belakang, dan ukuran halaman untuk setiap PNG yang diekspor.

Implementasikan metode ekspor seperti di bawah ini:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*Definition anchor*: Kelas `RasterizationOptions` mengontrol DPI, ukuran halaman, dan warna latar belakang untuk file PNG yang dihasilkan.

### Kesalahan Umum & Solusi
- **File font hilang** – Verifikasi bahwa setiap `.ttf` atau `.otf` yang direferensikan dalam ODP ada di folder yang Anda tetapkan.  
- **Path file tidak tepat** – Gunakan path absolut atau selesaikan path relatif terhadap `System.getProperty("user.dir")`.  
- **Izin tidak cukup** – Pastikan proses Java dapat membaca direktori font dan menulis ke folder output.

## Aplikasi Praktis
1. **Slide deck konsisten merek** – Ekspor presentasi sebagai PNG untuk publikasi web sambil mempertahankan font perusahaan.  
2. **Pembuatan laporan otomatis** – Konversi setiap slide menjadi gambar untuk dimasukkan ke dalam laporan PDF atau buletin email.  
3. **Pembuatan arsip legacy** – Simpan konten ODP sebagai PNG untuk menjamin aksesibilitas di masa depan tanpa memerlukan penampil ODP.

## Pertimbangan Kinerja
- Gunakan versi Aspose.Imaging terbaru untuk memanfaatkan perbaikan rasterisasi multi‑thread (hingga 2× lebih cepat pada CPU 8‑core).  
- Bungkus pemrosesan gambar dalam blok try‑with‑resources untuk menjamin pembuangan sumber daya native tepat waktu.  
- Sesuaikan `RasterizationOptions` (mis., DPI lebih rendah) saat memproses ribuan slide untuk menyeimbangkan kualitas dan penggunaan memori.

## Pertanyaan yang Sering Diajukan

**Q: Apa versi Java minimum yang diperlukan?**  
A: Aspose.Imaging untuk Java bekerja dengan JDK 8 dan yang lebih baru; JDK 11 direkomendasikan untuk dukungan jangka panjang.

**Q: Bisakah saya mengonversi hanya slide tertentu?**  
A: Ya, tetapkan `rasterizationOptions.setPageNumber(specificSlideIndex)` sebelum memanggil `save`.

**Q: Bagaimana cara menangani file ODP yang dilindungi password?**  
A: Muat file dengan `LoadOptions` yang menyertakan password, kemudian lanjutkan dengan pengaturan font yang sama.

**Q: Apakah menonaktifkan font sistem memengaruhi kinerja?**  
A: Hal ini sedikit meningkatkan kecepatan karena mesin melewatkan pencarian font sistem, terutama terlihat pada mesin dengan koleksi font besar.

**Q: Di mana saya dapat menemukan contoh kode lebih banyak?**  
A: Jelajahi [dokumentasi resmi Aspose.Imaging](https://reference.aspose.com/imaging/java/) untuk skenario tambahan seperti konversi batch dan transformasi gambar.

## Sumber Daya Tambahan
- [Rilis Aspose.Imaging untuk Java](https://releases.aspose.com/imaging/java/)  
- [Rilis Aspose.Imaging](https://releases.aspose.com/imaging/java/)  
- [Mulai Uji Coba Gratis Anda](https://releases.aspose.com/imaging/java/)  
- [Dokumentasi Aspose.Imaging](https://reference.aspose.com/imaging/java/)  
- [Forum Aspose.Imaging](https://forum.aspose.com/c/imaging/14)  
- [Beli Lisensi Aspose](https://purchase.aspose.com/buy)  
- [Ajukan Lisensi Sementara](https://purchase.aspose.com/temporary-license/)  

---

**Last Updated:** 2026-06-28  
**Diuji Dengan:** Aspose.Imaging for Java 25.5  
**Penulis:** Aspose

## Tutorial Terkait

- [Mengonversi ODG ke PNG dengan Aspose.Imaging untuk Java: Panduan Lengkap](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Konversi Gambar Efisien di Java dengan Aspose.Imaging: Panduan Lengkap](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}