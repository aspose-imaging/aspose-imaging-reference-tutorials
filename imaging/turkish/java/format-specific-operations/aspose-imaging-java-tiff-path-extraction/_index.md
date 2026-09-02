---
date: '2026-09-02'
description: Aspose.Imaging for Java kullanarak TIFF görüntülerinden kırpma yolu oluşturmayı
  ve çıkarmayı öğrenin. TIFF'i PSD'ye verimli bir şekilde dönüştürmek için adım adım
  talimatları izleyin.
keywords:
- create clipping path
- how to extract path
- how to convert tiff
- aspose imaging java
- convert tiff to psd
lastmod: '2026-09-02'
og_description: Aspose.Imaging for Java kullanarak TIFF görüntülerinden kırpma yolu
  oluşturmayı ve çıkarmayı öğrenin. TIFF'i PSD'ye dönüştürmek için adım adım kodu
  izleyin.
og_image_alt: Guide showing how to create clipping path in TIFF using Aspose.Imaging
  Java
og_title: Aspose.Imaging for Java ile TIFF'te kırpma yolu oluşturun
schemas:
- author: Aspose
  dateModified: '2026-09-02'
  description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  headline: Create clipping path in TIFF with Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  name: Create clipping path in TIFF with Aspose.Imaging for Java
  steps:
  - name: '**Free trial** – start with a 30‑day trial.'
    text: '**Free trial** – start with a 30‑day trial.'
  - name: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
    text: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
  - name: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
    text: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
  - name: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
    text: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
  - name: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
    text: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
  type: HowTo
- questions:
  - answer: Yes, provided you have a valid commercial license; a free trial is available
      for evaluation.
    question: Can I use Aspose.Imaging for Java in a commercial application?
  - answer: The library supports over 100 formats, including TIFF, PSD, BMP, JPEG,
      PNG, and many more.
    question: What image formats does Aspose.Imaging support?
  - answer: Verify that the source TIFF actually contains vector path resources; use
      the `hasPathResources()` check before extraction.
    question: How do I troubleshoot path extraction errors?
  - answer: Absolutely – combine the extraction code with Java’s parallel streams
      or an executor service to handle many files efficiently.
    question: Is batch processing of multiple TIFFs possible?
  - answer: Complex shapes may need manual adjustment after creation; the API handles
      standard Bezier curves and straight lines reliably.
    question: Are there limitations when creating clipping paths in TIFF?
  type: FAQPage
tags:
- create clipping path
- TIFF processing
- Aspose.Imaging
- Java image manipulation
- PSD conversion
title: Aspose.Imaging for Java ile TIFF'te kırpma yolu oluşturun
url: /tr/java/format-specific-operations/aspose-imaging-java-tiff-path-extraction/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java ile TIFF'te Kesme Yolu Oluşturma

Bu kapsamlı rehberde, TIFF dosyasında **kesme yolu nasıl oluşturulur** ve Aspose.Imaging for Java kullanarak mevcut yolların nasıl çıkarılacağını öğreneceksiniz. Sonunda, TIFF görüntülerini tamamen düzenlenebilir PSD dosyalarına dönüştürebilecek ve Photoshop ya da herhangi bir vektör‑bilgili editöre hazır hale getirebileceksiniz.

## Hızlı Yanıtlar
- **Kesme yolu nedir?** Bir görüntünün şeffaf ve opak bölgelerini tanımlayan bir vektör konturudur.  
- **Bir TIFF'ten mevcut bir yolu çıkarabilir miyim?** Evet – Aspose.Imaging gömülü yol kaynaklarını okuyabilir ve PSD olarak kaydedebilir.  
- **Yeni bir kesme yolu nasıl eklerim?** Bir `PathResource` oluşturun, vektör kayıtlarıyla doldurun ve görüntünün aktif çerçevesine atayın.  
- **Üretim kullanımında lisansa ihtiyacım var mı?** Ticari dağıtımlar için geçerli bir Aspose.Imaging lisansı gereklidir.  
- **Hangi Java sürümü gereklidir?** JDK 8 veya üzeri; kütüphane Java 11, 17 ve sonrası ile çalışır.

## Kesme Yolu Nedir?
Kesme yolu, bir görüntünün hangi bölümlerinin gösterileceğini veya gizleneceğini render motorlarına bildiren vektör‑tabanlı bir konturdur. TIFF veya PSD dosyalarının içinde bir yol kaynağı olarak depolanır ve Adobe Photoshop'ta düzenlenebilir.

## Neden TIFF'i PSD'ye Dönüştürmeliyiz?
TIFF'i PSD'ye dönüştürmek, katmanların, maskelerin ve kesme yollarının kayıpsız düzenlenmesini sağlar. Aspose.Imaging **50+ giriş ve çıkış formatı** destekler ve tüm dosyayı belleğe yüklemeden çok sayfalı TIFF'leri işleyebilir, yüksek performanslı toplu dönüşüm sunar.

## Önkoşullar
- **Java Development Kit (JDK)** 8 veya daha yeni bir sürüm yüklü.
- **Aspose.Imaging for Java** kütüphanesi (Maven, Gradle veya doğrudan indirme yoluyla ekleyin).  
- Java programlama kavramlarına temel aşinalık.

## Aspose.Imaging for Java Nasıl Kurulur
Herhangi bir kod eklemeden önce, kütüphanenin derleme sisteminizde doğru şekilde referans edildiğinden ve geçerli bir lisans dosyanız olduğundan emin olun. Bu, API'nin değerlendirme kısıtlamaları olmadan çalışmasını ve yol manipülasyonu dahil tüm özelliklerin kullanılabilir olmasını sağlar.

### Maven
Aşağıdaki bağımlılığı `pom.xml` dosyanıza ekleyin:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle
Bu satırı `build.gradle` dosyanıza ekleyin:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Doğrudan indirme
En son sürümü [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) adresinden indirin.

#### Lisans edinme
1. **Free trial** – 30‑günlük deneme sürümüyle başlayın.  
2. **Temporary license** – [temporary license page](https://purchase.aspose.com/temporary-license/) adresinden bir tane edinin.  
3. **Purchase** – [Aspose's website](https://purchase.aspose.com/buy) üzerinden tam lisans satın alın.

Kurulum ve lisanslama tamamlandıktan sonra, projenizde Aspose.Imaging'i başlatın:
```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path_to_license_file");
```

## TIFF'ten Kesme Yolu Nasıl Çıkarılır?
Kesme yolu çıkarmak, TIFF'i yüklemeyi, gömülü yol kaynaklarını bulmayı ve bu kaynakları yeni bir PSD dosyasına yazmayı içerir. İşlem, kaynak görüntüden vektör verilerini doğrudan okur, doğruluğu korur ve raster dönüşümünden kaçınır.

TIFF'i yükleyin, yol kaynakları üzerinde döngü yapın ve sonucu PSD olarak kaydedin. Bu işlem gömülü vektör verilerini okur ve tek bir geçişte yeni bir dosyaya yazar.
```java
String filePath = "YOUR_DOCUMENT_DIRECTORY/SupportExtractingPathsFromTiff/Sample.tif";
try (TiffImage image = (TiffImage) com.aspose.imaging.Image.load(filePath)) {
    // Proceed with extraction steps...
}
```

Aktif çerçevedeki yol kaynakları üzerinde döngü yapın ve toplayın:
```java
for (PathResource path : image.getActiveFrame().getPathResources()) {
    System.out.println(path.getName());  // Output the name of each path resource found.
}
```

Çıkarılan yollarla görüntüyü yeni bir PSD dosyasına kaydedin:
```java
String outFilePath = "YOUR_OUTPUT_DIRECTORY/SampleWithPaths.psd";
image.save(outFilePath);
```

## TIFF'te Kesme Yolu Nasıl Oluşturulur?
Kesme yolu oluşturmak, istenen vektör konturu tanımlayan bir `PathResource` oluşturmayı, bunu TIFF'in aktif çerçevesine eklemeyi ve ardından yolu korumak için görüntüyü (veya bir kopyasını) PSD olarak kaydetmeyi gerektirir. Bu yaklaşım, raster dosyalara programlı olarak vektör maskeleri eklemenizi sağlar.

PathResource, bir görüntü dosyası içinde depolanan bir vektör yolunu temsil eder.  
Gerekli özelliklerle yeni bir `PathResource` başlatın:
```java
final PathResource pathResource = new PathResource();
pathResource.setBlockId((short) 2000); // Set Block ID per Photoshop specs
pathResource.setName("My Clipping Path"); // Name your clipping path for easy identification

// Create and add vector path records using the provided coordinates.
pathResource.setRecords(createRecords(0.2f, 0.2f, 0.8f, 0.2f, 0.8f, 0.8f, 0.2f, 0.8f));
```

Oluşturulan yol kaynağını görüntünün aktif çerçevesine atayın:
```java
List<PathResource> list = new LinkedList<>();
list.add(pathResource);
image.getActiveFrame().setPathResources(list);
```

Değiştirilen TIFF'i artık kesme yolu içeren bir PSD olarak kaydedin:
```java
String outFilePath2 = "YOUR_OUTPUT_DIRECTORY/ImageWithPath.psd";
image.save(outFilePath2);
```

## Yardımcı Metodlar

### Kayıtları Oluştur
Bezier düğümleri ve uzunluk kayıtları kullanarak vektör yol kayıtları oluşturun:
```java
private static List<VectorPathRecord> createRecords(float ... coordinates) {
    List<VectorPathRecord> records = createBezierRecords(coordinates); 
    LengthRecord lr = new LengthRecord();
    lr.setOpen(false);
    lr.setRecordCount(records.size());
    
    records.add(0, lr);
    return records;
}
```

### Bezier Kayıtlarını Oluştur
Koordinat dizilerini Bezier vektör yol kayıtlarına dönüştürün:
```java
private static List<VectorPathRecord> createBezierRecords(float[] coordinates) {
    final List<VectorPathRecord> list = new LinkedList<>();
    
    for (int index = 0; index < coordinates.length - 1; index += 2) {
        PointF point = new PointF(coordinates[index], coordinates[index + 1]);
        list.add(createBezierRecord(point));
    }
    
    return list;
}
```

### Tek Bezier Kayıt Oluştur
Tek bir Bezier düğüm vektör yol kaydı tanımlayın:
```java
private static VectorPathRecord createBezierRecord(PointF point) {
    BezierKnotRecord it = new BezierKnotRecord();
    it.setPathPoints(new PointF[] { point, point, point });
    return it;
}
```

## Pratik Uygulamalar
1. **Graphic design workflows** – Photoshop'ta katmanları ve maskeleri düzenlemek için TIFF'i PSD'ye dönüştürün.  
2. **Automated image pipelines** – Binlerce TIFF'i toplu işleyin, yolları anında çıkarın veya ekleyin.  
3. **Data‑driven visualizations** – Raster kaynaklardan kesin grafikler veya şemalar üretmek için vektör yolları kullanın.

## Performans Düşünceleri
- **Memory management** – Görüntü nesnelerinin hızlı bir şekilde serbest bırakılmasını sağlamak için try‑with‑resources kullanın.  
- **Batch processing** – Büyük görüntü setleri için dönüşümleri Java’nın `ForkJoinPool` ile paralelleştirin.  
- **Resolution handling** – İşlem süresini düşük tutup kaliteyi korumak için DPI'yi yalnızca gerektiğinde ayarlayın.

## Sonuç
Artık TIFF dosyalarında **kesme yolu oluşturma** ve Aspose.Imaging for Java kullanarak mevcut yolları çıkarma konusunda bilgi sahibisiniz. Bu teknikler, masaüstü araçlarından kurumsal düzeyde işleme hatlarına kadar herhangi bir Java‑tabanlı iş akışına gelişmiş görüntü işleme entegrasyonu yapmanızı sağlar.

### Sonraki Adımlar
- Farklı vektör şekilleri ve yol özellikleriyle deneyler yapın.  
- Filigran ekleme, format dönüştürme ve meta veri işleme gibi ek Aspose.Imaging özelliklerini keşfedin.

## Sıkça Sorulan Sorular

**Q: Aspose.Imaging for Java'yi ticari bir uygulamada kullanabilir miyim?**  
A: Evet, geçerli bir ticari lisansınız olduğu sürece; değerlendirme için ücretsiz deneme sürümü mevcuttur.

**Q: Aspose.Imaging hangi görüntü formatlarını destekliyor?**  
A: Kütüphane, TIFF, PSD, BMP, JPEG, PNG ve daha fazlası dahil olmak üzere 100'den fazla formatı destekler.

**Q: Yol çıkarma hatalarını nasıl gideririm?**  
A: Kaynak TIFF'in gerçekten vektör yol kaynakları içerdiğini doğrulayın; çıkarma işleminden önce `hasPathResources()` kontrolünü kullanın.

**Q: Birden fazla TIFF'in toplu işlenmesi mümkün mü?**  
A: Kesinlikle – çıkarma kodunu Java’nın paralel akışları veya bir yürütücü servisi ile birleştirerek birçok dosyayı verimli bir şekilde işleyin.

**Q: TIFF'te kesme yolu oluştururken sınırlamalar var mı?**  
A: Karmaşık şekiller oluşturulduktan sonra manuel ayarlama gerektirebilir; API standart Bezier eğrileri ve düz çizgileri güvenilir bir şekilde işler.

---

**Son Güncelleme:** 2026-09-02  
**Test Edilen Versiyon:** Aspose.Imaging for Java 24.12  
**Yazar:** Aspose  

## Kaynaklar

- [Aspose.Imaging Dokümantasyonu](https://reference.aspose.com/imaging/java/)
- [Aspose.Imaging for Java'ı İndir](https://releases.aspose.com/imaging/java/)
- [Lisans Satın Al](https://purchase.aspose.com/buy)
- [Ücretsiz Deneme](https://releases.aspose.com/imaging/java/)
- [Geçici Lisans](https://purchase.aspose.com/temporary-license/)
- [Aspose Destek Forumları](https://forum.aspose.com/c/imaging/14)

## İlgili Eğitimler

- [Aspose.Imaging for Java ile Görüntüyü PSD'ye Dönüştür – Adım‑Adım Kılavuz](/imaging/java/format-conversion-export/convert-images-to-psd-using-aspose-imaging-java-guide/)
- [Aspose.Imaging Java ile TIFF'i GraphicsPath'e Dönüştürme](/imaging/java/advanced-drawing-graphics/aspose-imaging-java-tiff-graphicspath-conversion/)
- [Aspose.Imaging ile Java'da TIFF Görüntülerini Verimli Şekilde Yükleme ve Kaydetme](/imaging/java/image-loading-saving/aspose-imaging-java-tiff-image-saving/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}