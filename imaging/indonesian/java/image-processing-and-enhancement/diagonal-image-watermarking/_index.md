---
title: Penandaan Air Gambar Diagonal dengan Aspose.Imaging untuk Java
linktitle: Tanda Air Gambar Diagonal
second_title: Aspose.Imaging API Pemrosesan Gambar Java
description: Sempurnakan gambar Anda dengan tanda air diagonal menggunakan Aspose.Imaging untuk Java. Ikuti panduan langkah demi langkah ini dan buat gambar bertanda air yang menakjubkan dengan mudah.
weight: 14
url: /id/java/image-processing-and-enhancement/diagonal-image-watermarking/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Penandaan Air Gambar Diagonal dengan Aspose.Imaging untuk Java


Jika Anda ingin menyempurnakan gambar Anda dengan tanda air diagonal yang bergaya, Aspose.Imaging for Java siap membantu. Dalam panduan langkah demi langkah ini, kami akan memandu Anda melalui proses menambahkan tanda air teks yang diputar 45 derajat ke gambar JPG yang sudah ada. Anda tidak perlu menjadi ahli dalam Java atau pemrosesan gambar untuk mengikutinya – kami akan membagi setiap contoh menjadi beberapa langkah untuk memastikan Anda dapat dengan mudah mencapai hasil yang profesional.

## Prasyarat

Sebelum kita terjun ke dunia watermarking gambar yang menarik, Anda memerlukan beberapa hal:

1.  Aspose.Imaging for Java: Pastikan Anda telah menginstal Aspose.Imaging for Java. Anda dapat menemukan tautan unduhan[Di Sini](https://releases.aspose.com/imaging/java/).

2. Lingkungan Pengembangan Java: Anda harus menyiapkan lingkungan pengembangan Java yang berfungsi di komputer Anda.

3. Gambar untuk diberi Tanda Air: Siapkan gambar yang ingin Anda beri tanda air dan simpan dalam direktori. Anda dapat menggunakan contoh gambar untuk tutorial ini.

## Paket Impor

Pertama, impor paket yang diperlukan agar proyek Java Anda siap untuk diberi watermark pada gambar. Di bawah ini adalah paket penting yang perlu Anda sertakan:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Langkah 1: Muat Gambar yang Ada

Muat gambar yang ingin Anda beri tanda air. Dalam contoh ini, kami berasumsi Anda memiliki gambar JPG bernama "SampleTiff1.tiff" di direktori "ModifyingImages" Anda.

```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Muat gambar JPG yang ada
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Kode lainnya ada di sini
}
```

## Langkah 2: Siapkan Teks dan Grafik Tanda Air

Sekarang, mari deklarasikan teks tanda air Anda dan atur grafik untuk tanda air tersebut.

```java
// Deklarasikan objek String dengan Teks Tanda Air
String theString = "45 Degree Rotated Text";

// Membuat dan menginisialisasi instance kelas Grafik
Graphics graphics = new Graphics(image);

// Inisialisasi objek SizeF untuk menyimpan Ukuran gambar
Size sz = graphics.getImage().getSize();
```

## Langkah 3: Tentukan Font dan Kuas

Atur font dan kuas untuk tanda air Anda. Anda dapat menyesuaikan font, ukuran, dan gaya agar sesuai dengan preferensi Anda.

```java
// Buat sebuah instance Font, inisialisasi dengan Font Face, Size, dan Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Buat sebuah instance dari SolidBrush dan atur berbagai propertinya
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Langkah 4: Format Teks Anda

Tentukan format teks tanda air Anda, termasuk perataan dan tanda format.

```java
// Inisialisasi objek kelas StringFormat dan atur berbagai propertinya
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Langkah 5: Terapkan Transformasi

Buat matriks transformasi untuk memposisikan dan memutar teks tanda air. Dalam contoh ini, kita akan memutar teks sebesar 45 derajat.

```java
// Buat objek kelas Matrix untuk transformasi
Matrix matrix = new Matrix();
//Pertama terjemahan, lalu rotasi
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Atur Transformasi melalui Matriks
graphics.setTransform(matrix);
```

## Langkah 6: Gambar dan Simpan

Sekarang, saatnya menambahkan teks ke gambar, dan menyimpan gambar yang diberi watermark ke lokasi yang Anda inginkan.

```java
// Gambarkan string pada Gambar
graphics.drawString(theString, font, brush, 0, 0, format);

// Simpan keluaran ke disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Selamat! Anda telah berhasil menambahkan tanda air diagonal ke gambar Anda menggunakan Aspose.Imaging untuk Java.

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari cara menyempurnakan gambar Anda dengan tanda air diagonal menggunakan Aspose.Imaging untuk Java. Ini adalah alat yang ampuh untuk menambahkan sentuhan profesional pada gambar Anda. Hanya dengan beberapa langkah sederhana, Anda dapat membuat gambar bertanda air menakjubkan yang menonjol dari gambar lainnya.

## FAQ

### Q1: Apakah Aspose.Imaging untuk Java cocok untuk pemula?

A1: Tentu saja! Aspose.Imaging for Java menawarkan antarmuka yang ramah pengguna dan dokumentasi yang komprehensif. Bahkan pemula pun dapat dengan cepat memulai pemrosesan gambar.

### Q2: Dapatkah saya menyesuaikan teks dan gaya tanda air?

A2: Ya, Anda dapat dengan mudah menyesuaikan teks tanda air, font, ukuran, warna, dan sudut rotasi agar sesuai dengan preferensi dan merek Anda.

### Q3: Apakah Aspose.Imaging untuk Java mendukung format gambar lain selain JPG?

A3: Ya, Aspose.Imaging for Java mendukung berbagai format gambar, termasuk BMP, PNG, GIF, dan banyak lagi.

### Q4: Apakah tersedia uji coba gratis untuk Aspose.Imaging untuk Java?

 A4: Ya, Anda dapat mencoba Aspose.Imaging untuk Java dengan uji coba gratis. Mendapatkan[Di Sini](https://releases.aspose.com/).

### Q5: Di mana saya dapat menemukan bantuan atau dukungan untuk Aspose.Imaging untuk Java?

 A5: Jika Anda memiliki pertanyaan atau memerlukan bantuan, kunjungi forum dukungan Aspose.Imaging untuk Java[Di Sini](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
