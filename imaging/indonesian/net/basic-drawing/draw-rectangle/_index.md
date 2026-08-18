---
date: 2026-02-12
description: Pelajari cara membuat gambar kosong dengan Aspose dan cara menggambar
  persegi panjang di .NET menggunakan Aspose.Imaging – panduan cepat untuk manipulasi
  gambar dalam aplikasi .NET Anda.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Buat Gambar Kosong Aspose – Menggambar Persegi Panjang di .NET
url: /id/net/basic-drawing/draw-rectangle/
weight: 14
---

Translate FAQ.

Make sure to keep links unchanged.

Let's craft final output.{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Buat Gambar Kosong Aspose – Gambar Persegi Panjang di .NET

Membuat dan memanipulasi gambar dalam aplikasi .NET dapat terasa menakutkan, tetapi dengan Aspose.Imaging Anda dapat **membuat gambar kosong Aspose** hanya dengan beberapa baris kode dan kemudian menggambar bentuk di atasnya. Pada tutorial ini kami akan membahas seluruh proses — dari menyiapkan kanvas kosong hingga menggambar persegi panjang—sehingga Anda dapat langsung menambahkan grafik ke proyek .NET Anda.

## Jawaban Cepat
- **Apa arti “create blank image Aspose”?** Itu berarti menghasilkan bitmap kosong menggunakan API Aspose.Imaging.  
- **Bagaimana cara menggambar persegi panjang .net dengan Aspose?** Gunakan metode `Graphics.DrawRectangle` setelah menginisialisasi objek `Graphics`.  
- **Paket NuGet mana yang diperlukan?** `Aspose.Imaging` (versi terbaru).  
- **Apakah saya dapat menyimpan gambar sebagai PNG, JPEG, atau BMP?** Ya – cukup ubah opsi gambar (misalnya, `BmpOptions`, `JpegOptions`).  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi komersial diperlukan untuk produksi.

## Apa itu “create blank image Aspose”?
Membuat gambar kosong berarti mengalokasikan buffer piksel dengan lebar, tinggi, dan format piksel yang ditentukan. Aspose.Imaging menangani detail tingkat rendah, memberikan Anda kanvas siap gambar tanpa harus berurusan dengan GDI+ atau System.Drawing.

## Mengapa menggunakan Aspose.Imaging untuk menggambar persegi panjang di .NET?
- **Cross‑platform** – berfungsi di Windows, Linux, dan macOS.  
- **Tanpa dependensi native** – kode murni yang dikelola, sempurna untuk lingkungan server.  
- **API menggambar yang kaya** – mendukung pens, brushes, anti‑aliasing, dan banyak tipe bentuk.  
- **Kinerja tinggi** – dioptimalkan untuk gambar besar dan pemrosesan batch.

## Prasyarat

1. **Aspose.Imaging untuk .NET** – unduh dari [halaman unduhan](https://releases.aspose.com/imaging/net/).  
2. **Lingkungan Pengembangan** – Visual Studio, VS Code, atau IDE kompatibel .NET lainnya.  
3. **Runtime .NET** – .NET 6+ atau .NET Framework 4.7.2+.  

Setelah semua siap, mari kita selami kode.

## Cara membuat gambar kosong Aspose di .NET?

### Langkah 1: Impor namespace yang diperlukan

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Namespace ini memberi Anda akses ke kelas inti imaging, tipe brush, dan opsi penyimpanan gambar.

### Langkah 2: Buat gambar kosong (kanvas)

```csharp
string dataDir = "Your Document Directory";  // Set the path to your document directory
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Your drawing code will go here
        image.Save();
    }
}
```

Pada blok ini kami:

* Menentukan lokasi output (`dataDir`).  
* Mengonfigurasi `BmpOptions` untuk menggunakan format piksel 32‑bit.  
* Membuat **gambar kosong** berukuran 100 × 100 piksel.  

### Langkah 3: Cara menggambar persegi panjang .net dengan Aspose.Imaging

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` mengisi kanvas dengan warna latar belakang (kuning dalam contoh ini).  
* `DrawRectangle` menggambar dua persegi panjang—satu dengan pena merah sederhana, lainnya dengan brush biru padat—untuk kontras visual.

### Langkah 4: Simpan gambar

```csharp
image.Save();
```

Memanggil `Save` menulis bitmap ke sistem file menggunakan opsi yang telah didefinisikan sebelumnya.

## Masalah Umum & Tips

| Masalah | Alasan | Perbaikan |
|-------|--------|-----|
| **Gambar kosong muncul hitam** | Latar belakang tidak dibersihkan | Panggil `graphic.Clear(Color.WarnaAnda)` sebelum menggambar. |
| **Exception file tidak ditemukan** | `dataDir` mengarah ke folder yang tidak ada | Pastikan direktori ada atau gunakan `Path.Combine` dengan `Environment.CurrentDirectory`. |
| **Warna tidak tepat** | Menggunakan `System.Drawing.Color` alih-alih `Aspose.Imaging.Color` | Selalu impor `Aspose.Imaging.Color`. |
| **Lag kinerja pada gambar besar** | Menggunakan `BmpOptions` default dengan bit‑per‑pixel tinggi | Beralih ke `JpegOptions` atau `PngOptions` untuk kompresi. |

## Pertanyaan yang Sering Diajukan (Diperluas)

**T: Apakah saya dapat menggambar bentuk lain selain persegi panjang?**  
J: Tentu saja. Aspose.Imaging menyediakan metode seperti `DrawEllipse`, `DrawLine`, dan `DrawPolygon`.

**T: Apakah perpustakaan ini gratis untuk penggunaan komersial?**  
J: Tidak, Aspose.Imaging adalah produk komersial, tetapi Anda dapat mengevaluasinya dengan percobaan gratis yang tersedia [di sini](https://releases.aspose.com/).

**T: Apakah ini bekerja pada aplikasi Windows maupun web?**  
J: Ya, kode yang sama berjalan di ASP.NET, Blazor, dan aplikasi konsol.

**T: Bagaimana cara mengubah format output menjadi PNG?**  
J: Ganti `BmpOptions` dengan `PngOptions` dan sesuaikan ekstensi file yang bersangkutan.

**T: Di mana saya dapat menemukan dokumentasi lebih detail?**  
J: Akses referensi API lengkap [di sini](https://reference.aspose.com/imaging/net/) dan bergabung dengan komunitas di [forum Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2026-02-12  
**Diuji Dengan:** Aspose.Imaging 24.12 untuk .NET  
**Penulis:** Aspose