---
title: Membuat Gambar WMF dengan Aspose.Imaging untuk Java
linktitle: Hasilkan Gambar Metafile WMF
second_title: Aspose.Imaging API Pemrosesan Gambar Java
description: Pelajari cara membuat gambar metafile WMF di Java menggunakan Aspose.Imaging. Ikuti panduan langkah demi langkah ini untuk kemampuan menghasilkan gambar yang hebat.
weight: 10
url: /id/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Membuat Gambar WMF dengan Aspose.Imaging untuk Java

Apakah Anda ingin membuat gambar WMF (Windows Metafile) dengan aplikasi Java Anda? Aspose.Imaging for Java adalah alat canggih yang memungkinkan Anda menghasilkan gambar WMF dengan mudah. Dalam panduan langkah demi langkah ini, kami akan memandu Anda melalui proses penggunaan Aspose.Imaging untuk Java untuk membuat gambar metafile WMF. 

## Prasyarat

Sebelum memulai, pastikan Anda memiliki prasyarat berikut:

- Lingkungan pengembangan Java diatur di komputer Anda.
-  Aspose.Imaging untuk perpustakaan Java diinstal. Anda dapat mengunduhnya dari[situs web](https://releases.aspose.com/imaging/java/).
- Pengetahuan dasar tentang pemrograman Java.

## Paket Impor

Pertama, impor paket yang diperlukan untuk aplikasi Java Anda agar dapat menggunakan Aspose.Imaging untuk Java:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.color.*;
import com.aspose.imaging.coreexceptions.ImageLoadException;
import com.aspose.imaging.imageoptions.WmfOptions;
import com.aspose.imaging.internal.system.drawing.*;
import com.aspose.imaging.internal.system.drawing.imaging.*;
import com.aspose.imaging.pen.*;
import com.aspose.imaging.system.drawing.*;
```

## Langkah 1: Buat Kanvas

 Untuk mulai membuat gambar WMF, Anda perlu membuat kanvas tempat Anda bisa menggambar bentuk. Itu`WmfRecorderGraphics2D` class memberi Anda kanvas ini. Inilah cara Anda membuat instance-nya:

```java
// Jalur ke direktori dokumen.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

Pada kode di atas, kita menentukan dimensi kanvas (100x100) dan resolusi (96 DPI).

## Langkah 2: Atur Warna Latar Belakang

 Selanjutnya, tentukan warna latar belakang kanvas Anda. Anda dapat menggunakan`setBackgroundColor` metode untuk mengatur warna latar belakang:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

Dalam contoh ini, kita mengatur warna latar belakang menjadi asap putih.

## Langkah 3: Tentukan Pena dan Kuas

Untuk menggambar bentuk di kanvas, Anda perlu menentukan pena dan kuas. Pena digunakan untuk menggambar garis, dan kuas digunakan untuk mengisi bentuk. Inilah cara Anda membuat pena dan kuas padat:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

Dalam kode ini, kita membuat pena biru dan kuas padat berwarna kuning-hijau.

## Langkah 4: Isi dan Gambar Bentuk

Sekarang, mari mengisi dan menggambar beberapa bentuk dasar di kanvas. Kita akan mulai dengan poligon:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Di sini, kita mengisi dan menggambar poligon menggunakan pena dan kuas yang ditentukan. Anda dapat mengatur koordinat dan bentuk sesuai kebutuhan.

## Langkah 5: Gunakan HatchBrush

 Untuk menambahkan tekstur pada bentuk Anda, Anda dapat menggunakan a`HatchBrush`. Misalnya:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

Dalam kode ini, kita membuat brush cross-hatch dengan warna putih dan perak.

## Langkah 6: Isi dan Gambar Ellipse

Mari mengisi dan menggambar elips di kanvas:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

Anda dapat mengatur posisi dan ukuran elips sesuai kebutuhan.

## Langkah 7: Gambar Arc dan Cubic Bezier

Menggambar bentuk yang lebih kompleks juga dimungkinkan. Berikut cara menggambar busur dan kurva Bezier kubik:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

Pada kode di atas, pertama-tama kita menggambar busur dengan gaya garis putus-putus, lalu kita menggambar kurva Bezier kubik dengan pena merah solid.

## Langkah 8: Tambahkan Gambar

Anda juga dapat menambahkan gambar ke metafile WMF Anda. Berikut cara melakukannya:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

Pada langkah ini, kita memuat gambar dan menempatkannya di kanvas pada koordinat yang ditentukan (50, 50).

## Langkah 9: Gambar Garis dan Pai

Untuk menambahkan garis dan bentuk pai, Anda dapat mengikuti contoh berikut:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Di sini, kita menggambar garis dan mengisi/menggambar bentuk pai menggunakan pena dan kuas yang ditentukan.

## Langkah 10: Gambar Polyline dan Teks

Menambahkan teks dan polyline sangatlah mudah:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

Anda dapat menyesuaikan font, teks, dan titik polyline sesuai kebutuhan.

## Langkah 11: Simpan Gambar WMF

Setelah Anda membuat gambar WMF, saatnya menyimpannya:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Kode ini akan menyimpan gambar WMF ke direktori yang ditentukan.

Itu dia! Anda telah berhasil membuat gambar metafile WMF menggunakan Aspose.Imaging untuk Java.

## Kesimpulan

Dalam tutorial ini, kita telah menjelajahi cara membuat gambar metafile WMF menggunakan Aspose.Imaging untuk Java. Kami membahas prasyarat yang diperlukan, paket yang diimpor, dan memberikan petunjuk langkah demi langkah untuk menggambar berbagai bentuk, menambahkan tekstur, menyisipkan gambar, dan menyimpan gambar akhir. Aspose.Imaging for Java menawarkan seperangkat alat canggih untuk manipulasi dan pembuatan gambar, menjadikannya sumber daya berharga untuk aplikasi Java Anda.

## FAQ

### Q1: Apa yang dimaksud dengan format gambar WMF?

A1: WMF adalah singkatan dari Windows Metafile, yang merupakan format grafik vektor yang digunakan untuk menyimpan gambar, gambar, dan data grafis lainnya. Ini biasanya digunakan dalam aplikasi Windows dan dapat dengan mudah diskalakan tanpa kehilangan kualitas.

### Q2: Di mana saya dapat mengunduh Aspose.Imaging untuk Java?

 A2: Anda dapat mengunduh Aspose.Imaging untuk Java dari[situs web](https://releases.aspose.com/imaging/java/).

### Q3: Apakah saya memerlukan keterampilan pemrograman tingkat lanjut untuk menggunakan Aspose.Imaging untuk Java?

A3: Meskipun pengetahuan dasar pemrograman Java diperlukan, Aspose.Imaging for Java menyediakan API ramah pengguna yang menyederhanakan tugas manipulasi dan pembuatan gambar.

### Q4: Dapatkah saya menggunakan Aspose.Imaging untuk Java untuk tujuan komersial?

 A4: Ya, Aspose.Imaging for Java menawarkan lisensi komersial untuk bisnis dan pengembang. Anda dapat membeli lisensi dari[Di Sini](https://purchase.aspose.com/buy).

### Q5: Di mana saya bisa mendapatkan dukungan atau mengajukan pertanyaan tentang Aspose.Imaging untuk Java?

 A5: Anda dapat mendapatkan dukungan dan terlibat dengan komunitas Aspose di[Aspose.Forum pencitraan](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
