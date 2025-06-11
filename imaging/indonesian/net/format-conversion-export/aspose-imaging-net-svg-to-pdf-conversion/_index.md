---
"date": "2025-06-03"
"description": "Kuasai konversi SVG ke PDF dengan Aspose.Imaging .NET sambil mempertahankan kualitas font. Pelajari pengaturan direktori, penyematan font, dan banyak lagi."
"title": "Konversi SVG ke PDF yang Efisien Menggunakan Manajemen Font dan Teknik Aspose.Imaging .NET"
"url": "/id/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Konversi SVG ke PDF yang Efisien Menggunakan Aspose.Imaging .NET

## Perkenalan

Mengonversi grafik vektor ke dalam format serbaguna seperti PDF sangat penting untuk berbagi dan mencetak dokumen di era digital saat ini. Mempertahankan integritas font selama konversi ini bisa jadi sulit. Tutorial ini menunjukkan konversi SVG ke PDF yang lancar sambil mempertahankan kualitas font menggunakan Aspose.Imaging for .NET.

**Apa yang Akan Anda Pelajari:**
- Menyiapkan direktori dan mengekspor file SVG sebagai PDF.
- Teknik untuk menanamkan atau mengekspor font dalam berkas SVG.
- Menerapkan penanganan panggilan balik khusus untuk mengelola font SVG selama proses penyimpanan.

Dengan keterampilan ini, Anda dapat memastikan dokumen Anda terlihat profesional dan konsisten di berbagai platform. Mari kita mulai dengan menyiapkan lingkungan kita!

## Prasyarat

Sebelum menyelami kode, pastikan Anda memiliki hal berikut:

### Perpustakaan yang Diperlukan
- **Aspose.Imaging untuk .NET**: Penting untuk menangani konversi gambar.
- **Ruang Nama System.IO**: Untuk operasi file dan direktori.

### Pengaturan Lingkungan
Pastikan Anda memiliki lingkungan pengembangan yang kompatibel seperti Visual Studio atau IDE apa pun yang mendukung proyek .NET. Pemahaman terhadap pemrograman C# dasar akan sangat bermanfaat.

## Menyiapkan Aspose.Imaging untuk .NET

Untuk menggunakan Aspose.Imaging di proyek Anda, ikuti langkah-langkah instalasi berikut:

**Menggunakan .NET CLI:**
```bash
dotnet add package Aspose.Imaging
```

**Menggunakan Manajer Paket:**
```powershell
Install-Package Aspose.Imaging
```

**Melalui UI Pengelola Paket NuGet:**
Cari "Aspose.Imaging" dan instal versi terbaru.

### Akuisisi Lisensi
- **Uji Coba Gratis**: Mulailah dengan uji coba gratis untuk menguji fitur-fiturnya.
- **Lisensi Sementara**: Dapatkan lisensi sementara untuk evaluasi lanjutan.
- **Pembelian**: Pertimbangkan untuk membeli jika Aspose.Imaging memenuhi kebutuhan Anda.

#### Inisialisasi dan Pengaturan
Untuk menggunakan Aspose.Imaging, tambahkan sebagai dependensi dalam proyek Anda. Berikut ini adalah pengaturan dasar:

```csharp
using Aspose.Imaging;
```

Pastikan `Aspose.Imaging` namespace disertakan di bagian atas file Anda untuk mengakses kelas dan metodenya.

## Panduan Implementasi

Bagian ini menguraikan setiap fitur menjadi langkah-langkah yang dapat dikelola.

### Pengaturan Direktori dan Ekspor SVG ke PDF

#### Ringkasan
Konversi berkas SVG menjadi PDF sambil memastikan jalur direktori disiapkan dengan benar untuk keluaran.

**Langkah 1: Pastikan Direktori Output Ada**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*Penjelasan*: Cuplikan kode ini memeriksa apakah direktori keluaran ada dan membuatnya jika perlu.

**Langkah 2: Muat SVG dan Ekspor ke PDF**
```csharp
public void ReadAndExportToPdf(string inputFileName)
{
    string inputFile = Path.Combine(SourceFolder, inputFileName);
    string outFile = Path.Combine(OutFolder, inputFileName + ".pdf");
    
    using (Image image = Image.Load(inputFile))
    {
        image.Save(outFile,
            new PdfOptions { VectorRasterizationOptions = new SvgRasterizationOptions { PageSize = image.Size } });
    }
}
```
*Penjelasan*: : Itu `PdfOptions` memungkinkan konfigurasi rasterisasi konten SVG, memastikan bahwa ukuran halaman sesuai dengan dimensi gambar asli.

### Menyimpan SVG dengan Opsi Penyematan Font

#### Ringkasan
Simpan berkas SVG sambil mengendalikan pengaturan penyematan font untuk mempertahankan kesetiaan font.

**Langkah 1: Tentukan Direktori Output dan Font**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*Penjelasan*Pastikan direktori telah disiapkan sebelum menyimpan file.

**Langkah 2: Simpan SVG dengan Opsi Font Kustom**
```csharp
public void Save(bool useEmbedded, string fileName, int expectedCountFonts)
{
    string fontStoreType = useEmbedded ? "Embedded" : "Stream";
    string inputFile = Path.Combine(SourceFolder, fileName);
    string outFileName = $"{Path.GetFileNameWithoutExtension(fileName)}_{fontStoreType}.svg";
    string outputFile = Path.Combine(OutFolder, outFileName);

    using (Image image = Image.Load(inputFile))
    {
        EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions
        {
            BackgroundColor = Color.White,
            PageWidth = image.Width,
            PageHeight = image.Height
        };

        string testingFileName = Path.GetFileNameWithoutExtension(inputFile);
        string fontFolder = Path.Combine(FontFolder, testingFileName);

        image.Save(outputFile,
            new SvgOptions
            {
                VectorRasterizationOptions = emfRasterizationOptions,
                Callback = new SvgCallbackFontTest(useEmbedded, fontFolder)
                {
                    Link = FontFolderName + "/" + testingFileName
                }
            });
    }

    if (!useEmbedded)
    {
        string[] files = Directory.GetFiles(fontFolder);
        if (files.Length != expectedCountFonts)
        {
            throw new Exception($"Expected count font files = {expectedCountFonts}, Current count font files = {files.Length}");
        }
    }
}
```
*Penjelasan*: Metode ini memungkinkan Anda menentukan apakah font akan disematkan atau dialirkan, yang memengaruhi cara penyimpanan dan aksesnya.

### Penanganan Panggilan Balik Font SVG Kustom

#### Ringkasan
Terapkan penanganan khusus untuk mengelola sumber daya font selama penyimpanan SVG.

**Langkah 1: Terapkan Kelas SvgCallbackFontTest**
```csharp
public class SvgCallbackFontTest : SvgResourceKeeperCallback
{
    private readonly string outFolder;
    private readonly bool useEmbeddedFont;
    private int fontCounter = 0;

    public string Link { get; set; }

    public SvgCallbackFontTest(bool useEmbeddedFont, string outFolder)
    {
        this.useEmbeddedFont = useEmbeddedFont;
        this.outFolder = outFolder;
        
        if (Directory.Exists(outFolder))
        {
            Directory.Delete(this.outFolder, true);
        }
    }

    public override void OnFontResourceReady(FontStoringArgs args)
    {
        if (this.useEmbeddedFont)
        {
            args.FontStoreType = FontStoreType.Embedded;
        }
        else
        {
            args.FontStoreType = FontStoreType.Stream;
            string fontFolder = this.outFolder;

            if (!Directory.Exists(fontFolder))
            {
                Directory.CreateDirectory(fontFolder);
            }

            string fName = args.SourceFontFileName;
            if (!File.Exists(fName))
            {
                fName = $"font_{this.fontCounter++}.ttf";
            }

            string fileName = Path.Combine(fontFolder, Path.GetFileName(fName));
            
            args.DestFontStream = new FileStream(fileName, FileMode.OpenOrCreate);
            args.DisposeStream = true;
            args.FontFileUri = $".{this.Link}/{Path.GetFileName(fName)}";
        }
    }
}
```
*Penjelasan*: Kelas ini menangani sumber daya font dengan memutuskan apakah akan menanamkannya secara langsung atau menyimpannya secara terpisah. Kelas ini memastikan bahwa font direferensikan dan disimpan dengan benar selama proses ekspor SVG.

## Aplikasi Praktis

1. **Pembuatan Laporan Otomatis**: Gunakan Aspose.Imaging untuk mengubah draf desain menjadi PDF agar terdistribusi secara konsisten.
2. **Penerbitan Digital**Pastikan rendering font berkualitas tinggi saat mengonversi artikel dengan grafik tertanam dari SVG ke PDF.
3. **Berbagi Dokumen Lintas Platform**: Menjaga integritas visual dokumen yang dibagikan antara sistem operasi yang berbeda.

## Pertimbangan Kinerja

### Tips untuk Mengoptimalkan Kinerja
- Gunakan praktik penanganan berkas yang efisien, seperti membuang aliran berkas segera setelah digunakan.
- Minimalkan penggunaan memori dengan menghapus objek dan direktori yang tidak digunakan setelah pemrosesan selesai.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}