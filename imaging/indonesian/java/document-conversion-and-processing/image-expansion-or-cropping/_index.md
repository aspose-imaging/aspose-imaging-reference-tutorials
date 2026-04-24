---
date: 2025-12-20
description: Pelajari cara memotong gambar menjadi persegi panjang dan memperluas
  gambar menggunakan Java dengan Aspose.Imaging. Panduan langkah demi langkah untuk
  pengembang.
linktitle: Image Expansion or Cropping
second_title: Aspose.Imaging Java Image Processing API
title: Potong Gambar menjadi Persegi Panjang dengan Aspose.Imaging untuk Java
url: /id/java/document-conversion-and-processing/image-expansion-or-cropping/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Memotong Gambar menjadi Persegi Panjang dengan Aspose.Imaging untuk Java

Dalam dunia digital yang bergerak cepat saat ini, kemampuan untuk **crop image to rectangle** dengan cepat dan dapat diandalkan merupakan kebutuhan utama untuk alur kerja gambar berbasis Java apa pun. Baik Anda membangun layanan web yang perlu memotong foto yang diunggah pengguna, menghasilkan thumbnail untuk katalog e‑commerce, atau sekadar menyiapkan aset untuk kampanye pemasaran, Aspose.Imaging untuk Java memberikan API yang bersih dan berperforma tinggi untuk menyelesaikan pekerjaan. Dalam tutorial ini kami akan membahas cara memotong persegi panjang dari gambar dan memperluas kanvas gambar menggunakan Java—sempurna bagi siapa saja yang ingin menguasai teknik **how to crop image java**.

## Jawaban Cepat
- **Library apa yang terbaik untuk pemotongan gambar Java?** Aspose.Imaging for Java.
- **Apakah saya dapat memotong ke persegi panjang arbitrer?** Ya – definisikan X, Y, lebar, dan tinggi apa pun.
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi diperlukan untuk produksi.
- **Apakah memperluas gambar memungkinkan?** Tentu – Anda dapat meningkatkan ukuran kanvas sebelum memotong.
- **Versi Java apa yang didukung?** Java 8 dan yang lebih baru.

## Apa itu “crop image to rectangle”?
Memotong gambar menjadi persegi panjang berarti mengekstrak sub‑bagian dari bitmap asli yang didefinisikan oleh wilayah persegi panjang (X‑offset, Y‑offset, lebar, tinggi). Sisanya dari gambar dibuang, meninggalkan gambar baru yang lebih kecil yang hanya berisi area yang Anda butuhkan.

## Mengapa menggunakan Aspose.Imaging untuk Java?
- **Tidak ada ketergantungan eksternal** – Java murni, bekerja di platform apa pun.
- **Dukungan format yang luas** – JPEG, PNG, BMP, TIFF, dan lainnya.
- **Caching berperforma tinggi** – `cacheData()` mengurangi beban I/O.
- **API sederhana** – pemanggilan satu baris untuk memuat, mendefinisikan persegi panjang, dan menyimpan.

## Prasyarat
- **Lingkungan Pengembangan Java** – JDK 8+ terpasang dan terkonfigurasi.
- **Aspose.Imaging untuk Java** – unduh dari [situs web](https://releases.aspose.com/imaging/java/).
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

> **Tips Pro:** Gunakan blok `try‑with‑resources` (seperti yang ditunjukkan) untuk memastikan gambar secara otomatis ditutup, mencegah kebocoran memori.

## Langkah 2: Menentukan Wilayah untuk Pemotongan
Di sini kami membuat `Rectangle` yang mewakili area tepat yang ingin Anda pertahankan. Persegi panjang dapat dimulai di luar batas asli – Aspose.Imaging akan secara otomatis memperluas kanvas (berguna untuk skenario **expand image using java**).

```java
// Create an instance of Rectangle class and define X, Y, Width, and Height of the rectangle
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

- **X / Y** – nilai negatif menggeser persegi panjang ke kiri/atas, menyebabkan kanvas memperluas.
- **Width / Height** – ukuran wilayah yang dipotong.

## Langkah 3: Menyimpan Gambar yang Dipotong (atau Diperluas)
Akhirnya, tulis hasilnya ke disk. Metode `save` menerima jalur tujuan, opsi format gambar, dan persegi panjang yang kami definisikan.

```java
rasterImage.save("Your Document Directory" + "Grayscaling_out.jpg", new JpegOptions(), destRect);
```

File output `Grayscaling_out.jpg` kini berisi hasil **crop image to rectangle**. Jika persegi panjang melampaui gambar asli, area tambahan diisi dengan latar belakang default (transparan untuk PNG, hitam untuk JPEG).

## Kasus Penggunaan Umum
| Scenario | Why It Matters |
|----------|----------------|
| **Pembuatan thumbnail** | Dengan cepat mengekstrak wilayah pusat untuk ukuran yang konsisten. |
| **Pemotongan gambar profil pengguna** | Menerapkan area avatar berbentuk persegi atau persegi panjang. |
| **Perluasan kanvas sebelum menambahkan watermark** | Menambah ruang di sekitar gambar tanpa merusak gambar asli. |
| **Pemrosesan batch dokumen ter-scan** | Memotong margin dalam satu kali proses. |

## Pemecahan Masalah & Tips
- **Gambar tidak dapat dimuat?** Periksa jalur file dan pastikan format gambar didukung.
- **Bingkai hitam tak terduga setelah perluasan?** Atur warna latar belakang di `JpegOptions` atau gunakan PNG untuk transparansi.
- **Kekhawatiran kinerja dengan gambar besar?** Tingkatkan ukuran heap Java (`-Xmx`) atau proses gambar dalam batch yang lebih kecil.

## Pertanyaan yang Sering Diajukan
**Q: Format gambar apa yang didukung oleh Aspose.Imaging untuk Java?**  
A: JPEG, PNG, BMP, TIFF, GIF, ICO, PSD, dan banyak lagi. Lihat dokumen resmi untuk daftar lengkap.

**Q: Bisakah saya melakukan manipulasi gambar lain dengan Aspose.Imaging untuk Java?**  
A: Tentu! Mengubah ukuran, rotasi, penyaringan, dan konversi format semuanya tersedia.

**Q: Apakah Aspose.Imaging untuk Java cocok untuk aplikasi web?**  
A: Ya. Library ini thread‑safe dan bekerja dengan baik di kontainer servlet serta layanan Spring Boot.

**Q: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.Imaging untuk Java?**  
A: Kunjungi [forum](https://forum.aspose.com/) untuk bantuan komunitas, atau buka tiket dukungan dengan lisensi yang valid.

**Q: Apakah tersedia percobaan gratis untuk Aspose.Imaging untuk Java?**  
A: Ya, Anda dapat menjelajahi library dengan percobaan gratis. Unduh dari [sini](https://releases.aspose.com/).

## Kesimpulan
Anda kini telah mempelajari cara **crop image to rectangle** dan bahkan **expand image using Java** dengan API Aspose.Imaging yang kuat. Dengan menguasai dasar‑dasar ini, Anda dapat membangun pipeline pemrosesan gambar yang handal, meningkatkan responsivitas UI, dan menyajikan konten visual yang halus di seluruh aplikasi Java apa pun.

---

**Terakhir Diperbarui:** 2025-12-20  
**Diuji Dengan:** Aspose.Imaging for Java 24.11 (terbaru pada saat penulisan)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}