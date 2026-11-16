---
date: '2026-11-16'
description: Pelajari cara membuat multi page tiff dengan Aspose.Imaging for Java.
  Konversi gambar ke tiff, gabungkan frame, dan optimalkan penyimpanan dalam satu
  panduan.
keywords:
- create multi page tiff
- convert images to tiff
- aspose imaging java
- java image processing tutorial
- multi-page tiff generation
lastmod: '2026-11-16'
og_description: Buat multi page tiff menggunakan Aspose.Imaging for Java. Panduan
  langkah demi langkah ini menunjukkan cara mengonversi gambar ke tiff, menambahkan
  frame, dan mengoptimalkan penyimpanan.
og_image_alt: 'Developer guide: create multi page tiff using Aspose.Imaging for Java'
og_title: Buat multi page tiff dengan Aspose.Imaging for Java
schemas:
- author: Aspose
  dateModified: '2026-11-16'
  description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  headline: How to create multi page tiff using Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  name: How to create multi page tiff using Aspose.Imaging for Java
  steps:
  - name: load an image
    text: '`Image.load` reads the image file into memory and returns an `Image` object
      that you can manipulate. Ensure the file path is correct to avoid `FileNotFoundException`.'
  - name: resize the image
    text: '`ResizeType.NearestNeighbourResample` preserves hard edges and pixel data,
      which is ideal when you need a faithful representation of scanned documents.'
  - name: set up TIFF options
    text: '`TiffOptions` defines the compression, bits per pixel, and other TIFF‑specific
      settings. The `source` property points to the file where the multi‑page TIFF
      will be saved.'
  - name: initialize the TIFF image
    text: '`TiffImage.create` creates an empty TIFF container with the width and height
      derived from the first resized image. This container will later hold each frame
      you add.'
  - name: load additional images
    text: The loop iterates over every file ending with `.img` (or any supported raster
      format) in the target directory, loads each image, and calls `savePixels` to
      copy pixel data into a new frame of the TIFF.
  - name: save your work
    text: '`image.save` writes the complete multi‑page TIFF to the output path you
      specified in `TiffOptions`. Verify that the directory is writable to avoid `IOException`.'
  type: HowTo
- questions:
  - answer: Absolutely. Load any supported raster format (PNG, JPEG, BMP, etc.) and
      add each as a frame using the same workflow.
    question: Can I convert PNG or JPEG files to a multi‑page TIFF with this approach?
  - answer: Yes. Call `tiffOptions.setCompression(TiffCompression.Lzw)` before creating
      the image to reduce file size while preserving quality.
    question: Is it possible to set compression (e.g., LZW) for the output TIFF?
  - answer: Use `frame.getMetadata().addProperty("Author", "Your Name")` after creating
      the frame and before saving.
    question: How do I add metadata (author, description) to each TIFF frame?
  - answer: It does. Load the file with `Image.load("existing.tiff")` and iterate
      through `((TiffImage)image).getFrames()` to access each page.
    question: Does Aspose.Imaging support reading existing multi‑page TIFFs?
  - answer: Process pages in batches, call `System.gc()` periodically, and use the
      try‑with‑resources pattern to release native memory promptly.
    question: What if I need to process thousands of pages?
  type: FAQPage
tags:
- create multi page tiff
- Aspose.Imaging
- Java image processing
- TIFF conversion
title: Cara membuat multi page tiff menggunakan Aspose.Imaging for Java
url: /id/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara membuat multi page tiff menggunakan Aspose.Imaging untuk Java

## Pendahuluan

Membuat **multi page tiff** adalah kebutuhan umum ketika Anda perlu mengarsipkan beberapa gambar terkait dalam satu file yang kompak. Baik Anda membangun sistem manajemen dokumen, pipeline pencitraan medis, atau alat pemrosesan batch, Aspose.Imaging untuk Java memberi Anda kontrol penuh atas pembuatan TIFF, kompresi, dan penanganan frame. Dalam panduan ini Anda akan belajar cara memuat, mengubah ukuran, dan menggabungkan beberapa gambar menjadi satu multi‑page TIFF, sambil menjaga penggunaan memori tetap rendah dan kinerja tetap tinggi.

**Apa yang akan Anda pelajari**
- Muat dan ubah ukuran gambar dengan Aspose.Imaging.
- Konfigurasikan `TiffOptions` untuk output multi‑page.
- Tambahkan frame dari beberapa gambar sumber.
- Simpan TIFF akhir dengan kompresi opsional.
- Skenario dunia nyata di mana multi‑page TIFF bersinar.

## Jawaban Cepat
- **Apa perpustakaan utama?** Aspose.Imaging untuk Java.  
- **Apakah saya dapat mengonversi gambar ke tiff?** Ya – tutorial ini menunjukkan cara menggabungkan PNG, JPEG, BMP, dan format lain menjadi multi‑page TIFF.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi permanen diperlukan untuk penggunaan produksi.  
- **Versi Java apa yang diperlukan?** Java 8 atau lebih tinggi (JDK 8+).  
- **Apakah kode ini thread‑safe?** Contoh dijalankan pada satu thread; untuk skenario bersamaan, kelola objek `Image` per thread.

## Cara membuat multi page tiff?

Muat gambar sumber Anda, ubah ukurannya jika diperlukan, konfigurasikan `TiffOptions`, tambahkan setiap gambar sebagai frame, dan panggil `save`. Alur singkat ini membuat multi‑page TIFF yang sesuai standar hanya dalam beberapa baris kode Java, sambil memungkinkan Anda mengontrol kompresi dan dimensi halaman.

## Apa itu multi‑page TIFF?

Multi‑page TIFF adalah file TIFF tunggal yang berisi beberapa frame gambar, masing‑masing mewakili sebuah halaman. Ini banyak digunakan untuk aplikasi arsip, faks, dan pemindaian dokumen karena menyimpan banyak halaman tanpa beban file terpisah.

## Prasyarat

- Perpustakaan **Aspose.Imaging for Java** (unduh dari tautan di bawah).  
- **JDK 8+** terpasang dan dikonfigurasi di IDE Anda (IntelliJ IDEA, Eclipse, dll.).  
- Pengetahuan dasar Java dan familiaritas dengan file I/O.

## Menyiapkan Aspose.Imaging untuk java

Untuk mulai bekerja dengan Aspose.Imaging, Anda perlu mengintegrasikannya ke dalam proyek Anda. Berikut cara melakukannya menggunakan alat build populer:

**Maven:**  
Add the following dependency to your `pom.xml`:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle:**  
Include this in your `build.gradle` file:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

Sebagai alternatif, Anda dapat **mengunduh langsung** JAR Aspose.Imaging untuk Java terbaru dari [Aspose releases](/imaging/java/).

### Akuisisi Lisensi

Anda dapat memulai dengan percobaan gratis untuk menjelajahi fitur Aspose.Imaging. Untuk penggunaan jangka panjang, pertimbangkan mengajukan lisensi sementara atau membeli lisensi penuh:
- **Percobaan gratis:** Kunjungi [Aspose Imaging Java Releases](/imaging/java/) untuk mengunduh dan mencoba perpustakaan.  
- **Lisensi sementara:** Dapatkan dari [Aspose Temporary License Page](/purchase/temporary-license/).  
- **Pembelian:** Untuk solusi permanen, kunjungi [Aspose Purchase](/purchase/buy).

## Memuat dan mengubah ukuran gambar

**Gambaran Umum:**  
Langkah pertama melibatkan memuat gambar dari sistem file dan mengubah ukurannya menggunakan metode resample nearest‑neighbor.

#### Langkah 1: muat gambar
`Image.load` membaca file gambar ke memori dan mengembalikan objek `Image` yang dapat Anda manipulasi. Pastikan jalur file benar untuk menghindari `FileNotFoundException`.  
```java
import com.aspose.imaging.Image;

String dataDir = "YOUR_DOCUMENT_DIRECTORY";
Image tempImage = Image.load(dataDir + "/Image1.png");
```

#### Langkah 2: ubah ukuran gambar
`ResizeType.NearestNeighbourResample` mempertahankan tepi keras dan data piksel, yang ideal ketika Anda memerlukan representasi yang akurat dari dokumen yang dipindai.  
```java
int width = tempImage.getWidth();
int height = tempImage.getHeight();
tempImage.resize(width, height, ResizeType.NearestNeighbourResample);
```

## Membuat opsi TIFF dan sumber

**Gambaran Umum:**  
Selanjutnya, kami menyiapkan opsi yang diperlukan untuk membuat file TIFF multi‑page baru. Ini melibatkan penentuan format yang diharapkan dan konfigurasi sumber.

#### Langkah 1: siapkan opsi TIFF
`TiffOptions` mendefinisikan kompresi, bit per piksel, dan pengaturan khusus TIFF lainnya. Properti `source` menunjuk ke file tempat multi‑page TIFF akan disimpan.  
```java
import com.aspose.imaging.fileformats.tiff.TiffOptions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.sources.FileCreateSource;

TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setSource(new FileCreateSource("YOUR_DOCUMENT_DIRECTORY/MultiPage.tiff", false));
```

## Membuat dan menginisialisasi gambar TIFF multi‑page

**Gambaran Umum:**  
Sekarang, kami membuat instance gambar TIFF multi‑page dengan dimensi yang ditentukan.

#### Langkah 1: inisialisasi gambar TIFF
`TiffImage.create` membuat kontainer TIFF kosong dengan lebar dan tinggi yang diambil dari gambar pertama yang diubah ukurannya. Kontainer ini nantinya akan menampung setiap frame yang Anda tambahkan.  
```java
import com.aspose.imaging.fileformats.tiff.TiffImage;

TiffImage tiffImage = (TiffImage) Image.create(tiffOptions, width, height);
```

## Memproses beberapa gambar dan menambahkan frame ke TIFF

**Gambaran Umum:**  
Bagian ini melibatkan penambahan beberapa gambar sebagai frame ke dalam file TIFF multi‑page Anda.

#### Langkah 1: muat gambar tambahan
Loop iterasi setiap file yang berakhiran `.img` (atau format raster yang didukung) di direktori target, memuat setiap gambar, dan memanggil `savePixels` untuk menyalin data piksel ke frame baru TIFF.  
```java
import java.io.File;
import java.io.FilenameFilter;
import com.aspose.imaging.fileformats.tiff.TiffFrame;

File di = new File(dataDir);
String[] files = di.list(new FilenameFilter() {
    @Override
    public boolean accept(File dir, String name) {
        return name.endsWith(".img");
    }
});

if (files != null) {
    int index = 0;
    for (String file : files) {
        try (Image inputImage = Image.load(dataDir + "/" + file)) {
            if (index > 0) {
                TiffFrame newframe = new TiffFrame(tiffOptions, width, height);
                tiffImage.addFrame(newframe);
            }
            TiffFrame frame = tiffImage.getFrames()[index];
            frame.savePixels(frame.getBounds(), ((RasterImage) inputImage).loadPixels(inputImage.getBounds()));
            index += 1;
        }
    }
}
```

## Menyimpan gambar TIFF multi‑page

**Gambaran Umum:**  
Akhirnya, simpan file TIFF multi‑page Anda untuk mempertahankan semua perubahan yang dibuat selama pemrosesan.

#### Langkah 1: simpan pekerjaan Anda
`image.save` menulis TIFF multi‑page lengkap ke jalur output yang Anda tentukan dalam `TiffOptions`. Pastikan direktori dapat ditulisi untuk menghindari `IOException`.  
```java
import com.aspose.imaging.examples.Utils;

tiffImage.save("YOUR_OUTPUT_DIRECTORY/output.tiff");
```

## Aplikasi Praktis

Memahami cara **mengonversi gambar ke tiff** menggunakan Aspose.Imaging untuk Java dapat bermanfaat dalam beberapa skenario dunia nyata:

1. **Proyek arsip:** Simpan ratusan halaman yang dipindai dalam satu file, mengurangi kekacauan sistem file dan menyederhanakan strategi cadangan.  
2. **Pencitraan medis:** Gabungkan irisan CT, MRI, atau X‑ray menjadi satu multi‑page TIFF untuk transfer mudah antar sistem.  
3. **Manajemen dokumen:** Simpan PDF berversi, kontrak yang dipindai, atau faktur bersama, memungkinkan pengambilan dan pencetakan yang lebih cepat.

Kemungkinan integrasi termasuk menghubungkan fungsi ini dengan solusi penyimpanan cloud seperti AWS S3 atau Azure Blob Storage, memungkinkan pipeline arsip otomatis.

## Pertimbangan Kinerja

Saat bekerja dengan perpustakaan pemrosesan gambar di Java:
- **Ubah ukuran sebelum menambahkan frame** – mengurangi jejak memori hingga 60 % untuk pemindaian resolusi tinggi.  
- **Gunakan API streaming** – Aspose.Imaging dapat memproses gambar dalam potongan, yang membantu saat menangani TIFF dengan lebih dari 500 halaman.  
- **Buang objek Image dengan cepat** – bungkus penggunaan dalam `try (Image img = Image.load(...)) { … }` untuk membebaskan sumber daya native secara otomatis.

## Mengapa menggunakan Aspose.Imaging untuk Java?

Aspose.Imaging mendukung **50+** format input dan output, termasuk PNG, JPEG, BMP, GIF, dan TIFF, serta dapat memproses file TIFF ratusan halaman tanpa memuat seluruh dokumen ke memori. Benchmark menunjukkan pengurangan penggunaan CPU sebesar 30 % dibandingkan dengan Java ImageIO native saat menangani batch besar.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya mengonversi file PNG atau JPEG ke multi‑page TIFF dengan pendekatan ini?**  
A: Tentu saja. Muat format raster yang didukung (PNG, JPEG, BMP, dll.) dan tambahkan masing‑masing sebagai frame menggunakan alur kerja yang sama.

**Q: Apakah memungkinkan mengatur kompresi (misalnya, LZW) untuk TIFF output?**  
A: Ya. Panggil `tiffOptions.setCompression(TiffCompression.Lzw)` sebelum membuat gambar untuk mengurangi ukuran file sambil mempertahankan kualitas.

**Q: Bagaimana cara menambahkan metadata (penulis, deskripsi) ke setiap frame TIFF?**  
A: Gunakan `frame.getMetadata().addProperty("Author", "Your Name")` setelah membuat frame dan sebelum menyimpan.

**Q: Apakah Aspose.Imaging mendukung pembacaan multi‑page TIFF yang sudah ada?**  
A: Ya. Muat file dengan `Image.load("existing.tiff")` dan iterasi melalui `((TiffImage)image).getFrames()` untuk mengakses setiap halaman.

**Q: Bagaimana jika saya perlu memproses ribuan halaman?**  
A: Proses halaman dalam batch, panggil `System.gc()` secara berkala, dan gunakan pola try‑with‑resources untuk melepaskan memori native dengan cepat.

## Sumber Daya

- [Dokumentasi Aspose.Imaging untuk Java](/reference/imaging/java/)
- [Unduh Versi Terbaru](/imaging/java/)
- [Opsi Lisensi Pembelian](/purchase/buy)
- [Pembelian Aspose](/purchase/buy)
- [Mulai dengan Percobaan Gratis](/imaging/java/)
- [Informasi Lisensi Sementara](/purchase/temporary-license/)
- [Dukungan Komunitas dan Forum](/forum/imaging/14)

Dengan memanfaatkan sumber daya ini, Anda dapat memperdalam pemahaman tentang Aspose.Imaging untuk Java dan menerapkannya secara efektif dalam proyek Anda. Selamat coding!

---

**Last Updated:** 2026-11-16  
**Tested With:** Aspose.Imaging for Java 25.5  
**Author:** Aspose

```java
// Example: load and save a TIFF
Image img = Image.load("input.png");
img.save("output.tiff");
```

## Tutorial Terkait

- [Convert Multi-Frame TIFF to JPEG with Aspose.Imaging for Java - A Complete Guide](/imaging/java/image-loading-saving/convert-multi-frame-tiff-to-jpeg-aspose-imaging-java/)
- [Split Multi Page TIFF Frames with Aspose.Imaging for Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)
- [aspose imaging java – Convert TIFF to BMP Frames](/imaging/java/animation-multi-frame-images/extract-tiff-frames-to-bmp-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}