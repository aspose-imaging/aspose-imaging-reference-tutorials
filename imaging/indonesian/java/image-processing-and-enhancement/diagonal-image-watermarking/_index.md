---
date: 2026-01-09
description: Pelajari cara menambahkan watermark ke gambar dengan Aspose.Imaging untuk
  Java. Tutorial pemrosesan gambar Java ini menunjukkan langkah demi langkah cara
  membuat watermark diagonal dengan cepat.
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: Cara Menambahkan Watermark – Watermark Gambar Diagonal (Java)
url: /id/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Cara Menambahkan Watermark – Watermark Gambar Diagonal (Java)

Jika Anda ingin **how to add watermark** ke gambar Anda dengan orientasi diagonal yang bergaya, Aspose.Imaging for Java mempermudahnya. Dalam tutorial langkah‑demi‑langkah ini kami akan menunjukkan cara menambahkan watermark teks berputar 45‑derajat ke gambar JPG (atau format lain yang didukung). Anda tidak perlu menjadi ahli Java – setiap blok dijelaskan dengan bahasa sederhana sehingga Anda dapat mereplikasi hasilnya dalam hitungan menit.

## Jawaban Cepat
- **Perpustakaan apa yang digunakan?** Aspose.Imaging for Java  
- **Kata kunci utama yang dibahas?** how to add watermark  
- **Format gambar yang didukung?** JPEG, PNG, BMP, TIFF, GIF dan lainnya  
- **Berapa banyak kode yang diperlukan?** Hanya tujuh blok kode singkat  
- **Apakah saya memerlukan lisensi untuk pengujian?** Versi percobaan gratis tersedia; lisensi diperlukan untuk produksi  

## Apa itu “how to add watermark” dalam pemrosesan gambar?
Menambahkan watermark berarti menempatkan teks atau grafik semi‑transparan di atas gambar untuk melindungi kepemilikan atau menyampaikan merek. Watermark diagonal terutama efektif karena melintasi seluruh gambar dan lebih sulit dipotong.

## Mengapa menggunakan Aspose.Imaging for Java?
Aspose.Imaging menyediakan API tingkat tinggi yang menyembunyikan manipulasi piksel tingkat rendah, mendukung puluhan format, dan bekerja pada runtime Java apa pun. Ini memungkinkan Anda fokus pada *apa* yang ingin dicapai—seperti menambahkan watermark diagonal—tanpa harus khawatir tentang keanehan format gambar.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal‑hal berikut:

1. **Aspose.Imaging for Java** – unduh versi terbaru dari situs resmi **[here](https://releases.aspose.com/imaging/java/)**.  
2. **Java Development Environment** – JDK 8+ dan IDE favorit Anda (IntelliJ, Eclipse, VS Code, dll.).  
3. **Sebuah gambar untuk watermark** – letakkan contoh JPG/TIFF/PNG di folder yang akan Anda referensikan dalam kode.

## Impor Paket

Pertama, impor kelas‑kelas yang Anda perlukan. Menjaga impor bersama membuat kode lebih mudah dibaca dan dipelihara.

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Langkah 1: Memuat Gambar yang Ada

Kami mulai dengan memuat gambar sumber. Metode `Image.load` secara otomatis mendeteksi formatnya.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **Tip pro:** Bungkus objek `Image` dalam blok try‑with‑resources (seperti yang ditunjukkan) sehingga secara otomatis dibuang, mencegah kebocoran memori.

## Langkah 2: Menyiapkan Teks dan Grafik Watermark

Buat objek `Graphics` yang terhubung ke gambar yang dimuat dan simpan ukuran gambar untuk perhitungan selanjutnya.

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## Langkah 3: Menentukan Font dan Brush

Pilih font yang menonjol dan brush yang menentukan warna serta opasitas watermark. Sesuaikan opasitas agar watermark menjadi semi‑transparan.

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Langkah 4: Memformat Teks Anda

Atur perataan dan flag format sehingga teks berada di tengah ketika digambar.

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Langkah 5: Menerapkan Transformasi

Matriks transformasi memungkinkan kita memindahkan asal ke tengah gambar dan kemudian memutar teks sebesar ‑45° (searah jarum jam).

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## Langkah 6: Menggambar dan Menyimpan

Akhirnya, render string ke gambar dan tulis hasilnya ke disk.

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Saat Anda membuka `AddDiagonalWatermarkToImage_out.jpg` Anda akan melihat teks merah semi‑transparan miring melintasi tengah gambar.

## Masalah Umum & Solusi

| Masalah | Penyebab | Solusi |
|---------|----------|--------|
| Watermark muncul terlalu pudar | Opacity diatur ke 0 (sepenuhnya transparan) | Tingkatkan opacity, misalnya `brush.setOpacity(0.5f);` |
| Teks terpotong di tepi | Translasi tidak terpusat untuk gambar bukan persegi | Gunakan `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` seperti ditunjukkan, lalu sesuaikan sudut rotasi jika diperlukan |
| Kesalahan format gambar tidak didukung | Menggunakan versi Aspose.Imaging yang lebih lama | Perbarui ke rilis Aspose.Imaging terbaru |

## Pertanyaan yang Sering Diajukan

### Q1: Apakah Aspose.Imaging for Java cocok untuk pemula?

**A:** Tentu saja! API-nya intuitif, dan dokumentasinya menyediakan contoh yang jelas. Bahkan pengembang yang baru dalam pemrosesan gambar dapat mengikuti tutorial ini dan menghasilkan hasil profesional dengan cepat.

### Q2: Bisakah saya menyesuaikan teks dan gaya watermark?

**A:** Ya. Ubah variabel `theString`, pilih `Font` yang berbeda, modifikasi `brush.setColor(...)`, atau sesuaikan sudut rotasi pada matriks agar sesuai dengan merek Anda.

### Q3: Apakah Aspose.Imaging for Java mendukung format gambar lain selain JPG?

**A:** Ya. Perpustakaan ini bekerja dengan BMP, PNG, GIF, TIFF, PSD, dan banyak lagi. Cukup arahkan metode `Image.load` ke file yang sesuai.

### Q4: Apakah tersedia versi percobaan gratis untuk Aspose.Imaging for Java?

**A:** Ya, Anda dapat mencoba Aspose.Imaging for Java dengan versi percobaan gratis. Dapatkan **[here](https://releases.aspose.com/)**.

### Q5: Di mana saya dapat menemukan bantuan atau dukungan untuk Aspose.Imaging for Java?

**A:** Untuk pertanyaan, laporan bug, atau saran praktik terbaik, kunjungi forum dukungan Aspose.Imaging for Java **[here](https://forum.aspose.com/)**.

---

**Terakhir Diperbarui:** 2026-01-09  
**Diuji Dengan:** Aspose.Imaging for Java 24.11 (terbaru pada saat penulisan)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}