---
"date": "2025-06-03"
"description": "Aspose.Imaging .NET ile yazı tipi kalitesini korurken SVG'yi PDF'ye dönüştürmede ustalaşın. Dizin kurulumunu, yazı tiplerini yerleştirmeyi ve daha fazlasını öğrenin."
"title": "Aspose.Imaging .NET&#58; Yazı Tipi Yönetimi ve Teknikleri Kullanılarak Verimli SVG'den PDF'ye Dönüştürme"
"url": "/tr/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging .NET Kullanarak Verimli SVG'den PDF'ye Dönüştürme

## giriiş

Vektör grafiklerini PDF gibi çok yönlü formatlara dönüştürmek, günümüzün dijital çağında belge paylaşımı ve yazdırma için çok önemlidir. Bu dönüştürme sırasında yazı tipi bütünlüğünü korumak zor olabilir. Bu eğitim, Aspose.Imaging for .NET kullanarak yazı tipi kalitesini korurken sorunsuz SVG'den PDF'ye dönüştürmeyi gösterir.

**Ne Öğreneceksiniz:**
- Dizinlerin ayarlanması ve SVG dosyalarının PDF olarak dışa aktarılması.
- SVG dosyalarına yazı tiplerini yerleştirme veya dışa aktarma teknikleri.
- Kaydetme işlemi sırasında SVG yazı tiplerini yönetmek için özel bir geri çağırma işleyicisi uygulanıyor.

Bu becerilerle, belgelerinizin farklı platformlarda profesyonel ve tutarlı görünmesini sağlayabilirsiniz. Ortamımızı ayarlayarak başlayalım!

## Ön koşullar

Koda dalmadan önce aşağıdakilerin mevcut olduğundan emin olun:

### Gerekli Kütüphaneler
- **.NET için Aspose.Görüntüleme**: Görüntü dönüştürmelerini yönetmek için gereklidir.
- **System.IO Ad Alanı**: Dosya ve dizin işlemleri için.

### Çevre Kurulumu
Visual Studio veya .NET projelerini destekleyen herhangi bir IDE gibi uyumlu bir geliştirme ortamınız olduğundan emin olun. Temel C# programlamaya aşinalık faydalıdır.

## .NET için Aspose.Imaging Kurulumu

Projenizde Aspose.Imaging'i kullanmak için şu kurulum adımlarını izleyin:

**.NET CLI kullanımı:**
```bash
dotnet add package Aspose.Imaging
```

**Paket Yöneticisini Kullanma:**
```powershell
Install-Package Aspose.Imaging
```

**NuGet Paket Yöneticisi Kullanıcı Arayüzü aracılığıyla:**
"Aspose.Imaging"i arayın ve en son sürümü yükleyin.

### Lisans Edinimi
- **Ücretsiz Deneme**: Özellikleri test etmek için ücretsiz denemeyle başlayın.
- **Geçici Lisans**:Uzun süreli değerlendirme için geçici lisans alın.
- **Satın almak**: Eğer Aspose.Imaging ihtiyaçlarınızı karşılıyorsa satın almayı düşünebilirsiniz.

#### Başlatma ve Kurulum
Aspose.Imaging'i kullanmak için, bunu projenize bir bağımlılık olarak ekleyin. İşte temel bir kurulum:

```csharp
using Aspose.Imaging;
```

Sağlamak `Aspose.Imaging` namespace, sınıflarına ve metotlarına erişmek için dosyanızın en üstüne eklenir.

## Uygulama Kılavuzu

Bu bölüm her özelliği yönetilebilir adımlara ayırır.

### Dizin Kurulumu ve SVG'yi PDF'ye Aktarma

#### Genel bakış
Çıktı için dizin yollarının doğru şekilde ayarlandığından emin olarak bir SVG dosyasını PDF'ye dönüştürün.

**Adım 1: Çıktı Dizininin Var Olduğundan Emin Olun**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*Açıklama*: Bu kod parçacığı çıktı dizininin var olup olmadığını kontrol eder ve gerekirse oluşturur.

**Adım 2: SVG'yi yükleyin ve PDF'e aktarın**
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
*Açıklama*: : `PdfOptions` SVG içeriğinin rasterleştirilmesinin yapılandırılmasına izin verir ve sayfa boyutunun orijinal görüntü boyutlarıyla eşleşmesini sağlar.

### Font Gömme Seçenekleriyle SVG Kaydetme

#### Genel bakış
Yazı tipi doğruluğunu korumak için yazı tipi yerleştirme ayarlarını kontrol ederken bir SVG dosyası kaydedin.

**Adım 1: Çıktı ve Yazı Tipi Dizinlerini Tanımlayın**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*Açıklama*: Dosyaları kaydetmeden önce dizinlerin ayarlandığından emin olun.

**Adım 2: SVG'yi Özel Yazı Tipi Seçenekleriyle Kaydedin**
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
*Açıklama*: Bu yöntem, yazı tiplerinin gömülmesi mi yoksa yayınlanması mı gerektiğini belirtmenize olanak tanır ve bunların nasıl depolanacağını ve erişileceğini etkiler.

### Özel SVG Yazı Tipi Geri Arama İşleyicisi

#### Genel bakış
SVG kaydetme sırasında yazı tipi kaynaklarını yönetmek için özel bir işleyici uygulayın.

**Adım 1: SvgCallbackFontTest Sınıfını Uygulayın**
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
*Açıklama*: Bu sınıf, font kaynaklarını doğrudan gömmek mi yoksa ayrı olarak mı depolamak gerektiğine karar vererek yönetir. SVG dışa aktarma işlemi sırasında fontların doğru şekilde referans alınmasını ve kaydedilmesini sağlar.

## Pratik Uygulamalar

1. **Otomatik Rapor Oluşturma**: Tasarım taslaklarını tutarlı dağıtım için PDF'lere dönüştürmek amacıyla Aspose.Imaging'i kullanın.
2. **Dijital Yayıncılık**Gömülü grafikler içeren makaleleri SVG'den PDF'e dönüştürürken yüksek kaliteli yazı tipi oluşturulmasını sağlayın.
3. **Platformlar Arası Belge Paylaşımı**: Farklı işletim sistemleri arasında paylaşılan belgelerin görsel bütünlüğünü koruyun.

## Performans Hususları

### Performansı Optimize Etmeye Yönelik İpuçları
- Akışları kullandıktan hemen sonra atmak gibi etkili dosya işleme uygulamalarını kullanın.
- İşlem tamamlandıktan sonra kullanılmayan nesneleri ve dizinleri temizleyerek bellek kullanımını en aza indirin.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}