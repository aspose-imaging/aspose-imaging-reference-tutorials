---
date: '2026-09-28'
description: Pelajari cara menggunakan ccittfax3 compression java untuk membuat file
  multi-page TIFF dengan Aspose.Imaging. Secara efisien scan, archive, dan kurangi
  file size untuk document workflows.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Temukan langkah demi langkah cara menggunakan ccittfax3 compression
  java dengan Aspose.Imaging untuk membangun file multi-page TIFF yang efisien untuk
  scanning dan archiving.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: Cara membuat multi-page TIFF dengan ccittfax3 compression java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: Cara membuat multi-page TIFF dengan ccittfax3 compression java
url: /id/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menguasai pembuatan TIFF multi-halaman dengan kompresi ccittfax3 java menggunakan Aspose.Imaging

## Pendahuluan

Jika Anda perlu mengarsipkan volume besar dokumen yang dipindai sambil menjaga ukuran file tetap kecil, **ccittfax3 compression java** adalah solusi utama. Tutorial ini menunjukkan cara menghasilkan file TIFF multi‑halaman dengan kompresi CCITTFAX3 di Java menggunakan Aspose.Imaging. Anda akan belajar mengapa kompresi ini sangat efektif untuk pemindaian monokrom, cara mengkonfigurasi pustaka, dan cara menambahkan setiap halaman sebagai frame.

**Apa yang akan Anda pelajari**
- Cara menambahkan Aspose.Imaging ke proyek Java.
- Cara mengkonfigurasi `TiffOptions` untuk kompresi CCITTFAX3.
- Cara membuat `TiffImage`, mengubah ukuran gambar sumber, dan menambahkannya sebagai frame.
- Cara menyimpan TIFF multi‑halaman akhir secara efisien.

Mari kita jalani implementasi lengkap.

## Jawaban Cepat
- **Apa manfaat utama kompresi CCITTFAX3?** Pengurangan hingga 80 % ukuran file untuk pemindaian hitam‑putih.  
- **Pustaka mana yang menyediakan dukungan bawaan?** Aspose.Imaging untuk Java, versi 25.5+.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Lisensi percobaan gratis berfungsi untuk semua fitur; lisensi berbayar diperlukan untuk produksi.  
- **Bisakah saya memproses ratusan halaman?** Ya—Aspose.Imaging men-stream halaman, sehingga penggunaan memori tetap rendah.  
- **Apakah kode kompatibel dengan Java 11 dan versi lebih baru?** Tentu; API menargetkan Java 8+.

## Apa itu ccittfax3 compression java?
`CCITTFAX3` adalah algoritma kompresi monokrom lossless yang dirancang untuk faks dan gambar dokumen yang dipindai. Ia mengkodekan setiap piksel sebagai satu bit, menghasilkan output berkualitas tinggi sambil secara dramatis mengurangi ukuran file—seringkali sebesar 70‑80 % dibandingkan TIFF yang tidak terkompresi. Hal ini membuatnya ideal untuk mengarsipkan dokumen hitam‑putih dimana keakuratan harus dipertahankan.

## Mengapa menggunakan Aspose.Imaging untuk tugas ini?
Aspose.Imaging mendukung **100+** format input dan output, termasuk PDF, PNG, JPEG, dan TIFF. Arsitektur streaming-nya dapat menangani file TIFF **multi‑ratus‑halaman** tanpa memuat seluruh dokumen ke memori, menjadikannya ideal untuk proyek pengarsipan skala besar.

## Prasyarat

- **Java Development Kit (JDK)** 8 atau yang lebih baru terpasang.
- **IDE** seperti IntelliJ IDEA atau Eclipse.
- **Maven** atau **Gradle** untuk manajemen dependensi.
- Pengetahuan dasar Java (kelas, objek, koleksi).

## Menyiapkan Aspose.Imaging untuk Java

Tambahkan pustaka ke file build Anda.

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```  

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

### Unduhan Langsung

Anda juga dapat mengunduh JAR terbaru dari [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### Akuisisi Lisensi

Lisensi percobaan gratis tersedia di [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/). Untuk penggunaan produksi, beli lisensi permanen atau minta lisensi sementara di [Aspose Purchase](https://purchase.aspose.com/temporary-license/).

Untuk penggunaan API secara detail, lihat [documentation](https://reference.aspose.com/imaging/java/) Aspose.Imaging untuk Java.

### Inisialisasi Dasar

Setelah menambahkan dependensi, inisialisasi pustaka seperti ditunjukkan di bawah.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## Cara mengkonfigurasi ccittfax3 compression java untuk TIFF multi‑halaman?

`TiffOptions` adalah kelas yang mendefinisikan format output dan pengaturan kompresi untuk file TIFF. Muat objek `TiffOptions` dengan enum `CCITTGroup3FaxCompression`, lalu atur sumber file output. Konfigurasi dua langkah ini menyiapkan penulis untuk kompresi monokrom dan memastikan setiap halaman yang ditambahkan nanti akan dienkode menggunakan algoritma CCITTFAX3, menghasilkan pengurangan ukuran yang signifikan sambil mempertahankan kualitas gambar.

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## Cara membuat instance TiffImage di Java?

`TiffImage` mewakili dokumen TIFF multi‑halaman dalam memori dan menyediakan metode untuk memanipulasi frame-nya. Pertama, tentukan lebar dan tinggi yang akan dibagikan semua halaman. Kemudian buat instance `TiffImage` menggunakan `TiffOptions` yang telah dibuat sebelumnya. Objek `TiffImage` berfungsi sebagai kontainer untuk frame individu, memungkinkan Anda menambah, menghapus, atau mengubah urutan halaman sebelum menyimpan file akhir.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## Cara memuat dan mengubah ukuran gambar sumber dari folder?

Filter direktori target untuk file JPEG, baca setiap gambar, dan ubah ukurannya agar sesuai dengan kanvas TIFF. Mengubah ukuran sebelum menambah frame mengurangi konsumsi memori dan mempercepat operasi penyimpanan. Dengan mengonversi setiap gambar sumber ke dimensi dan format piksel yang diperlukan, Anda menjamin tata letak halaman yang konsisten dan menghindari kesalahan runtime saat frame ditambahkan ke dokumen TIFF.

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## Cara menambahkan setiap gambar sebagai frame ke TIFF multi‑halaman?

`TiffFrame` adalah objek yang menyimpan gambar satu halaman dan metadata terkaitnya dalam sebuah TIFF. Iterasi gambar yang telah diubah ukurannya, buat `TiffFrame` baru, dan tambahkan ke `TiffImage`. Setiap frame menjadi halaman terpisah dalam dokumen akhir, dan pustaka secara otomatis menangani pembaruan metadata yang diperlukan, seperti jumlah halaman dan offset, memastikan struktur TIFF multi‑halaman yang valid.

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## Cara menyimpan file TIFF multi‑halaman akhir?

Panggil metode `save` pada instance `TiffImage`, dengan memberikan jalur output yang diinginkan. Pustaka secara otomatis menulis semua frame menggunakan kompresi CCITTFAX3, men-stream data ke disk secara efisien, dan menutup semua sumber daya yang mendasarinya. Setelah operasi penyimpanan selesai, file yang dihasilkan berisi semua halaman dengan kompresi yang ditentukan, siap untuk distribusi atau pengarsipan.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## Aplikasi Praktis

- **Pengarsipan dokumen:** Simpan kontrak, faktur, atau catatan hukum yang dipindai dengan beban penyimpanan minimal.
- **Pencitraan medis:** Kompres pemindaian radiologi sambil mempertahankan detail diagnostik.
- **Produksi cetak:** Hasilkan pekerjaan cetak multi‑halaman yang dapat langsung diproses oleh printer.

## Pertimbangan Kinerja

- Gunakan `ResizeOptions` yang mempertahankan rasio aspek untuk menghindari distorsi.
- Tutup setiap objek `Image` setelah menambahkan frame-nya untuk membebaskan memori native.
- Untuk batch yang sangat besar, proses file dalam aliran paralel dan tulis setiap segmen TIFF secara asynchronous.

## Kesalahan Umum dan Pemecahan Masalah

- **Format piksel tidak tepat:** CCITTFAX3 hanya bekerja dengan gambar 1‑bit (hitam‑putih). Konversi gambar berwarna ke grayscale sebelum mengubah ukuran.
- **Kebocoran memori:** Selalu panggil `dispose()` pada objek `Image` sementara; jika tidak, buffer native tetap teralokasi.
- **Ukuran file tidak berkurang:** Pastikan properti kompresi `TiffOptions` diatur; jika tidak, default (tanpa kompresi) yang digunakan.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menggunakan pendekatan ini dengan gambar berwarna?**  
A: CCITTFAX3 terbatas pada data monokrom; untuk warna gunakan kompresi JPEG atau LZW sebagai gantinya.

**Q: Apakah Aspose.Imaging mendukung streaming untuk TIFF yang sangat besar?**  
A: Ya—pustaka menulis setiap frame langsung ke aliran output, menjaga penggunaan memori tetap rendah bahkan untuk ribuan halaman.

**Q: Bagaimana cara menerapkan lisensi sementara secara programatis?**  
A: Muat file `.lic` dengan `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.

**Q: Apakah ada cara untuk meninjau TIFF sebelum menyimpan?**  
A: Anda dapat merender setiap `TiffFrame` ke `BufferedImage` dan menampilkannya dalam komponen Swing.

**Q: Versi Java mana yang secara resmi didukung?**  
A: Aspose.Imaging mendukung Java 8 hingga Java 21, termasuk rilis LTS.

## Kesimpulan

Anda kini memiliki alur kerja lengkap yang siap produksi untuk membuat file TIFF multi‑halaman dengan **ccittfax3 compression java** menggunakan Aspose.Imaging. Dengan mengikuti langkah-langkah di atas, Anda dapat mengarsipkan koleksi dokumen besar secara efisien sambil menjaga biaya penyimpanan rendah dan kualitas gambar tinggi. Jelajahi fitur tambahan Aspose.Imaging—seperti OCR, penanganan metadata, dan konversi format—untuk lebih meningkatkan pipeline pemrosesan dokumen Anda.

---

**Terakhir Diperbarui:** 2026-09-28  
**Diuji Dengan:** Aspose.Imaging 25.5 untuk Java  
**Penulis:** Aspose

## Tutorial Terkait

- [Cara Membuat TIFF Multi-Halaman dengan Aspose.Imaging untuk Java – Panduan Lengkap](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Cara Mengurangi Ukuran File Gambar dengan Kompresi LZW di Java](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Membagi Frame TIFF Multi-Halaman dengan Aspose.Imaging untuk Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}