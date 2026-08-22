---
date: 2026-05-03
description: Pelajari cara memotong gambar dengan Aspose.Imaging untuk Java, termasuk
  pemotongan persegi panjang dan perluasan kanvas. Panduan langkah demi langkah untuk
  pengembang.
keywords:
- how to crop image
- crop and expand image
- aspose imaging crop
- java image processing tutorial
- expand image canvas java
linktitle: Perluasan atau Pemotongan Gambar
second_title: Aspose.Imaging Java Image Processing API
title: Cara Memotong Gambar menjadi Persegi Panjang dengan Aspose.Imaging untuk Java
url: /id/java/document-conversion-and-processing/image-expansion-or-cropping/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Cara Memotong Gambar menjadi Persegi Panjang dengan Aspose.Imaging untuk Java

Di dunia digital yang bergerak cepat saat ini, mengetahui **how to crop image** dengan cepat dan dapat diandalkan merupakan kebutuhan utama untuk alur kerja gambar berbasis Java apa pun. Baik Anda memotong foto yang diunggah pengguna untuk layanan web, menghasilkan thumbnail yang konsisten untuk katalog e‑commerce, atau menyiapkan aset untuk kampanye pemasaran, Aspose.Imaging untuk Java menyediakan API yang bersih dan berperforma tinggi untuk menyelesaikan pekerjaan. Dalam tutorial ini kami akan membahas cara memotong persegi panjang dari gambar dan memperluas kanvas gambar—sempurna bagi siapa saja yang ingin menguasai teknik pemrosesan gambar Java.

## Jawaban Cepat
- **Library apa yang terbaik untuk pemotongan gambar Java?** Aspose.Imaging for Java.  
- **Bisakah saya memotong ke persegi panjang arbitrer?** Ya – tentukan X, Y, lebar, dan tinggi apa pun.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi diperlukan untuk produksi.  
- **Apakah memperluas gambar memungkinkan?** Tentu – Anda dapat memperbesar ukuran kanvas sebelum memotong.  
- **Versi Java apa yang didukung?** Java 8 dan yang lebih baru.

## Apa itu “crop image to rectangle”?
Memotong gambar menjadi persegi panjang berarti mengekstrak sub‑bagian dari bitmap asli yang didefinisikan oleh wilayah persegi panjang (X‑offset, Y‑offset, lebar, tinggi). Sisanya gambar dibuang, meninggalkan gambar baru yang lebih kecil yang hanya berisi area yang Anda butuhkan.

## Mengapa Menggunakan Aspose.Imaging untuk Java?
- **Tidak ada dependensi eksternal** – Java murni, bekerja di semua platform.  
- **Dukungan format luas** – JPEG, PNG, BMP, TIFF, dan lainnya.  
- **Caching berperforma tinggi** – `cacheData()` mengurangi overhead I/O.  
- **API sederhana** – pemanggilan satu baris untuk memuat, mendefinisikan persegi panjang, dan menyimpan.

## Prasyarat
- **Lingkungan Pengembangan Java** – JDK 8+ terpasang dan terkonfigurasi.  
- **Aspose.Imaging untuk Java** – unduh dari [website](https://releases.aspose.com/imaging/java/).  
- **Pengetahuan Dasar Java** – familiar dengan kelas, try‑with‑resources, dan jalur file.  
- **Gambar untuk Dikerjakan** – JPEG/PNG apa pun yang ingin Anda potong atau perbesar.

## Mengimpor Paket
Pertama, arahkan kode ke folder yang berisi gambar sumber Anda. Potongan kode ini tetap tidak berubah dari tutorial asli.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

Ganti `"Your Document Directory"` dengan jalur absolut di mesin Anda.

## Langkah 1: Memuat Gambar
Memuat gambar adalah dasar untuk setiap manipulasi. Kami juga memanggil `cacheData()` untuk menyimpan bitmap di memori agar operasi selanjutnya lebih cepat.

```java
try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
{
    rasterImage.cacheData();
}
```

> **Pro tip:** Gunakan blok `try‑with‑resources` (seperti yang ditunjukkan) untuk memastikan gambar secara otomatis ditutup, mencegah kebocoran memori.

## Langkah 2: Menentukan Wilayah untuk Pemotongan
Di sini kami membuat `Rectangle` yang mewakili area tepat yang ingin Anda pertahankan. Persegi panjang dapat dimulai di luar batas asli – Aspose.Imaging akan secara otomatis memperluas kanvas (berguna untuk skenario **expand image canvas java**).

```java
// Create an instance of Rectangle class and define X, Y, Width, and Height of the rectangle
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

- **X / Y** – nilai negatif menggeser persegi panjang ke kiri/atas, menyebabkan kanvas diperluas.  
- **Width / Height** – ukuran wilayah yang dipotong.

## Langkah 3: Menyimpan Gambar yang Dipotong (atau Diperluas)
Akhirnya, tulis hasilnya ke disk. Metode `save` menerima jalur tujuan, opsi format gambar, dan persegi panjang yang kami definisikan.

```java
rasterImage.save("Your Document Directory" + "Grayscaling_out.jpg", new JpegOptions(), destRect);
```

File output `Grayscaling_out.jpg` sekarang berisi hasil **crop image to rectangle**. Jika persegi panjang melampaui gambar asli, area tambahan akan diisi dengan latar belakang default (transparan untuk PNG, hitam untuk JPEG).

## Cara Memotong Gambar dengan Aspose.Imaging untuk Java
Bagian ini mengulang langkah inti dalam daftar periksa singkat sehingga Anda dapat dengan cepat merujuknya saat menulis kode:

1. **Setel direktori data** – arahkan ke folder yang berisi gambar sumber.  
2. **Muat gambar** dengan `Image.load()` dan panggil `cacheData()`.  
3. **Buat `Rectangle`** yang mendefinisikan wilayah pemotongan (atau perluasan kanvas).  
4. **Simpan** gambar baru menggunakan `rasterImage.save()` dan berikan persegi panjang.

## Memotong dan Memperluas Gambar – Kasus Penggunaan Dunia Nyata
| Skenario | Mengapa Penting |
|----------|-----------------|
| **Pembuatan thumbnail** | Dengan cepat mengekstrak wilayah tengah untuk ukuran yang konsisten. |
| **Pemotongan gambar profil pengguna** | Menegakkan area avatar berbentuk persegi atau persegi panjang. |
| **Perluasan kanvas sebelum menambahkan watermark** | Menambahkan ruang di sekitar gambar tanpa merusak gambar asli. |
| **Pemrosesan batch dokumen ter-scan** | Memotong margin dalam satu proses. |

## Pemecahan Masalah & Tips
- **Gambar tidak dapat dimuat?** Verifikasi jalur file dan pastikan format gambar didukung.  
- **Bingkai hitam tak terduga setelah perluasan?** Atur warna latar belakang di `JpegOptions` atau gunakan PNG untuk transparansi.  
- **Kekhawatiran kinerja dengan gambar besar?** Tingkatkan ukuran heap Java (`-Xmx`) atau proses gambar dalam batch yang lebih kecil.  
- **Jebakan umum:** Lupa memanggil `cacheData()` dapat menyebabkan I/O lebih lambat pada operasi selanjutnya.

## Pertanyaan yang Sering Diajukan

**Q: Format gambar apa yang didukung oleh Aspose.Imaging untuk Java?**  
A: JPEG, PNG, BMP, TIFF, GIF, ICO, PSD, dan banyak lagi. Lihat dokumentasi resmi untuk daftar lengkap.

**Q: Bisakah saya melakukan manipulasi gambar lain dengan Aspose.Imaging untuk Java?**  
A: Tentu! Mengubah ukuran, rotasi, penyaringan, dan konversi format semuanya tersedia.

**Q: Apakah Aspose.Imaging untuk Java cocok untuk aplikasi web?**  
A: Ya. Perpustakaan ini thread‑safe dan bekerja dengan baik di kontainer servlet serta layanan Spring Boot.

**Q: Bagaimana cara mendapatkan dukungan untuk Aspose.Imaging untuk Java?**  
A: Kunjungi [forum](https://forum.aspose.com/) untuk bantuan komunitas, atau buka tiket dukungan dengan lisensi yang valid.

**Q: Apakah tersedia versi percobaan gratis untuk Aspose.Imaging untuk Java?**  
A: Ya, Anda dapat menjelajahi perpustakaan dengan versi percobaan gratis. Unduh dari [sini](https://releases.aspose.com/).

## Kesimpulan
Anda kini telah mempelajari **how to crop image** menjadi persegi panjang dan bahkan **expand image canvas** menggunakan API Aspose.Imaging yang kuat. Dengan menguasai dasar-dasar ini, Anda dapat membangun pipeline pemrosesan gambar yang handal, meningkatkan responsivitas UI, dan menyajikan konten visual yang halus di semua aplikasi Java.

---

**Terakhir Diperbarui:** 2026-05-03  
**Diuji Dengan:** Aspose.Imaging untuk Java 24.11 (terbaru pada saat penulisan)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}