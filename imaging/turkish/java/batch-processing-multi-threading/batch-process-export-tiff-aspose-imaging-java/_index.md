---
date: '2026-02-27'
description: Aspose.Imaging for Java ile toplu olarak TIFF dosyalarını dışa aktarma
  konusunda adım adım rehber, çok sayfalı TIFF Java işleme ve görüntü döndürmeyi kapsar.
keywords:
- batch process TIFF Java
- Aspose.Imaging TIFF export
- Java TIFF image processing
- automate TIFF handling with Java
- multi-page TIFF processing
title: Java için Aspose.Imaging ile Toplu TIFF Dışa Aktarma
url: /tr/java/batch-processing-multi-threading/batch-process-export-tiff-aspose-imaging-java/
weight: 1
---

.

We must keep markdown formatting.

Let's produce final content.

Check for any inline code like `TiffImage`, `PageExportingAction`, etc; keep as is.

Translate sentences.

Proceed.

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging for Java ile Toplu TIFF Dışa Aktarma

### Giriş

**tiff dışa aktarma** dosyalarını hızlı ve güvenilir bir şekilde, özellikle çok sayfalı belgelerle çalışırken nasıl yapacağınızı öğrenmek istiyorsanız bu öğretici tam size göre. Bir TIFF dosyasını toplu olarak işleme, her sayfayı döndürme ve sonucu kaydetme sürecini Aspose.Imaging for Java ile adım adım göstereceğiz. Sonunda, bu kütüphanenin Java projelerinde yüksek performanslı görüntü işleme için neden tercih edildiğini anlayacaksınız.

**Öğrenecekleriniz**
- Java projesine Aspose.Imaging ekleme.  
- **multi page tiff java** dosyalarıyla çalışmak için **PageExportingAction** kullanma.  
- Her sayfada **tiff file rotation** uygulama.  
- İşlenen görüntüleri düşük bellek tüketimiyle dışa aktarma.

Haydi başlayalım!

## Hızlı Yanıtlar
- **TIFF işleme için birincil sınıf nedir?** Aspose.Imaging’den `TiffImage`.  
- **Her sayfayı nasıl döndürürüm?** Bir `PageExportingAction` uygulayın ve sayfada `rotate(90)` çağırın.  
- **Lisans gerekli mi?** Lisans, filigranları kaldırır ve tam işlevselliği açar.  
- **Büyük dosyaları işleyebilir miyim?** Evet—`try‑with‑resources` ve isteğe bağlı `System.gc()` kullanarak belleği serbest bırakabilirsiniz.  
- **Çoklu iş parçacığı (multi‑threading) destekleniyor mu?** Aspose.Imaging içinde doğrudan destek yok, ancak Java eşzamanlılık araçlarıyla dosya seviyesinde paralelleştirme yapabilirsiniz.

## Java’da “how to export tiff” nedir?
Bir TIFF dışa aktarmak, kaynak dosyayı yüklemek, isteğe bağlı olarak her sayfayı (ör. döndürme veya yeniden boyutlandırma) değiştirmek ve ardından sonucu yeni bir TIFF dosyasına kaydetmek anlamına gelir. Aspose.Imaging, düşük seviyeli detayları soyutlayan akıcı bir API sunar, böylece iş mantığınıza odaklanabilirsiniz.

## Toplu TIFF işleme için Aspose.Imaging neden tercih edilmeli?
- **Tam format desteği** – Çok sayfalı TIFF, JPEG, PNG, BMP ve daha fazlasını işler.  
- **Bellek verimliliği** – Akış tabanlı yükleme ve sayfa‑sayfa işleme, yığın (heap) baskısını azaltır.  
- **Zengin API** – `PageExportingAction` gibi yerleşik eylemler, tekrarlayan kod yazmadan özel mantık eklemenizi sağlar.  

## Önkoşullar
- **Aspose.Imaging for Java** (Maven, Gradle veya doğrudan indirme yoluyla temin edilebilir).  
- **JDK 8+** yüklü ve yapılandırılmış.  
- Java sözdizimi ve proje yapı araçlarına temel aşinalık.

## Aspose.Imaging for Java Kurulumu

Aşağıda kütüphaneyi projenize eklemenin üç desteklenen yolu yer alıyor.

### Maven
`pom.xml` dosyanıza aşağıdaki bağımlılığı ekleyin:

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle
`build.gradle` dosyanıza şu satırı ekleyin:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Doğrudan İndirme
En yeni JAR dosyasını [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) adresinden indirebilirsiniz.

#### Lisans Edinme
Tüm özellikleri açmak için bir lisans alın:
- **Ücretsiz Deneme** – Kısa bir süre sınırsız keşif.  
- **Geçici Lisans** – Kısa vadeli projeler için ideal.  
- **Tam Lisans** – Üretim ortamları için önerilir.

#### Temel Başlatma
Uygulama başlangıcında lisansınızı yükleyin:

```java
// Load the license if available
License license = new License();
license.setLicense("path_to_your_license_file.lic");
```

## Uygulama Kılavuzu

### Aspose.Imaging for Java ile Toplu TIFF Görüntüsü Dışa Aktarma

Çözümü net adımlara böleceğiz, böylece kolayca takip edebileceksiniz.

### Adım 1: Kaynak TIFF dosyasını yükleyin
Girdi ve çıktı dizinlerini tanımlayın, ardından Aspose.Imaging’i işlemek istediğiniz dosyaya yönlendirin.

```java
String dataDir = "YOUR_DOCUMENT_DIRECTORY";
String fileName = "10MB_Tif.tif";
String inputFileName = Path.combine(dataDir, fileName);
```

### Adım 2: Sayfa‑dışa‑aktarma eylemi ayarlayın (tiff file rotation)
Her sayfayı 90 derece döndüren bir `PageExportingAction` oluşturun. Bu eylem, çok sayfalı TIFF’teki her sayfa için çalışır.

```java
try (TiffImage tiffImage = (TiffImage) Image.load(inputFileName)) {
    tiffImage.setPageExportingAction(new PageExportingAction() {
        @Override
        public void invoke(int pageIndex, Image page) {
            System.gc(); // Manage memory usage efficiently.
            ((RasterImage) page).rotate(90); // Rotate each page by 90 degrees.
        }
    });

    String outputFileNameTif = Path.combine("YOUR_OUTPUT_DIRECTORY", "ExportTiffBatchMode_output.tif");
    tiffImage.save(outputFileNameTif); // Save the processed image.
}
```

#### Neden Önemli
- **PageExportingAction**, çok sayfalı TIFF senaryoları için her sayfa üzerinde ince ayar yapmanızı sağlar.  
- Açık `System.gc()` çağrısı, çok büyük dosyalar işlendiğinde bellek kullanımını düşük tutmaya yardımcı olur.

### Adım 3: Çalıştırın ve doğrulayın
Programı çalıştırın. İşlem tamamlandığında, çıktı klasörünüzde `ExportTiffBatchMode_output.tif` dosyasını bulacaksınız; her sayfa belirtilen şekilde döndürülmüş olacaktır.

## Özel Sayfa Dışa Aktarma Eylemleri
Daha karmaşık işlemler (ör. filtre uygulama, çözünürlük değiştirme) gerekiyorsa, `PageExportingAction` sınıfını kendi mantığınızla genişletebilirsiniz. Bu esneklik, çözümü karmaşık veri akışları için ölçeklenebilir kılar.

## Pratik Uygulama Alanları

| Senaryo | Toplu dışa aktarma nasıl yardımcı olur |
|----------|----------------------------------------|
| **Tıbbi Görüntüleme** | Çok sayfalı DICOM‑türevi TIFF’leri döndürüp dışa aktararak sonraki analizlere hazır hale getirir. |
| **Arşivleme** | Büyük taranmış belge koleksiyonlarını tutarlı yönlendirilmiş TIFF’lere dönüştürür. |
| **Baskı Hizmetleri** | Yüksek çözünürlüklü TIFF’leri büyük formatlı yazıcılar için doğru sayfa yönlendirmesiyle hazırlar. |

## Performans Dikkat Edilecek Noktalar
- **Garbage Collection** – `System.gc()` yalnızca gerektiğinde çağrılmalı; aşırı kullanım performansı düşürebilir.  
- **Kaynak Yönetimi** – `try‑with‑resources` bloğu, dosya tutamaçlarının (handle) hızlıca serbest bırakılmasını garantiler.  
- **JVM Yığını** – Çok büyük dosyalar için yığın boyutunu (`-Xmx2G` veya daha yüksek) artırarak `OutOfMemoryError` oluşumunu önleyin.

## Sonuç
Artık **how to export tiff** dosyalarını toplu olarak işleyebilen, her sayfayı döndürebilen ve sonucu Aspose.Imaging for Java ile kaydedebilen eksiksiz, üretim‑hazır bir yönteme sahipsiniz. Bu yaklaşım bellek‑verimli, genişletmesi kolay ve çeşitli sektörlerde kullanılabilir.

### Sonraki Adımlar
- Diğer sayfa işlemlerini (ör. ölçekleme, renk dönüşümü) deneyin.  
- Bu rutini Java’nın `ExecutorService`iyle birleştirerek birden fazla TIFF dosyasını paralel işleyin.  
- Metaveri düzenleme veya format dönüşümü gibi ek Aspose.Imaging yeteneklerini keşfedin.

## SSS Bölümü

**S1: Çok büyük TIFF dosyalarını nasıl yönetirim?**  
C: JVM yığın boyutunu artırın (`-Xmx2G` veya daha fazla) ve `PageExportingAction`ı sayfa sayfa işlemek için kullanın; bu sayede bellek tüketimi düşük kalır.

**S2: Aspose.Imaging diğer görüntü formatlarını işleyebilir mi?**  
C: Evet, JPEG, PNG, BMP, GIF ve daha birçok formatı destekler. Tam liste için [belgelere](https://reference.aspose.com/imaging/java/) bakın.

**S3: Toplu işleme için dahili çoklu iş parçacığı var mı?**  
C: Aspose.Imaging içinde dahili bir threading mekanizması yoktur, ancak Java’nın `ExecutorService`i veya paralel akışlarıyla paralel işlem yapabilirsiniz.

**S4: Ücretsiz denemenin sınırlamaları nelerdir?**  
C: Deneme sürümü filigran ekler ve zaman sınırlıdır. Sınırsız kullanım için geçici ya da tam lisans alın.

**S5: Sorun yaşarsam nereden yardım alabilirim?**  
C: Topluluk desteği ve resmi Aspose desteği için [destek forumuna](https://forum.aspose.com/c/imaging/14) göz atın.

## Kaynaklar

- **Belgelendirme**: Ayrıntılı kılavuzlar ve API referansları için [Aspose.Imaging for Java documentation](https://reference.aspose.com/imaging/java/) adresini ziyaret edin.  
- **İndirme**: En yeni sürümler [Aspose.Imaging for Java downloads](https://releases.aspose.com/imaging/java/) adresinde bulunabilir.  
- **Satın Alma**: Lisans almak için [Aspose purchase page](https://purchase.aspose.com/buy) sayfasını kullanın.  
- **Ücretsiz Deneme**: Özellikleri keşfetmek için [free trial version](https://releases.aspose.com/imaging/java/) sayfasından başlayın.  
- **Geçici Lisans**: Geçici lisans talep etmek için [Aspose temporary license page](https://purchase.aspose.com/temporary-license/) adresine gidin.  
- **Destek**: Her türlü soru için [support forum](https://forum.aspose.com/c/imaging/14) adresine bakabilirsiniz.

---

**Son Güncelleme:** 2026-02-27  
**Test Edilen Sürüm:** Aspose.Imaging 25.5 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}