---
date: '2026-06-28'
description: Aspose.Imaging for Java kullanarak ODP'yi PNG'ye nasıl dönüştüreceğinizi
  öğrenin, özel yazı tiplerini ayarlayın ve doğru renderleme için sistem yazı tiplerini
  devre dışı bırakın.
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: Aspose.Imaging for Java ile ODP'yi PNG'ye Dönüştürme – Özel Yazı Tipleri ve
  Dışa Aktarma Kılavuzu
url: /tr/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging for Java ile ODP'yi PNG'ye Dönüştürme – Özel Yazı Tipleri ve Dışa Aktarma Kılavuzu

Modern Java uygulamalarında, OpenDocument Presentation (ODP) dosyalarını yüksek kaliteli PNG görüntülerine dönüştürmek yaygın bir gereksinimdir—özellikle özel yazı tipleriyle markalaşmayı korumanız gerektiğinde. Bu öğreticide **ODP'yi PNG'ye nasıl dönüştüreceğinizi** Aspose.Imaging for Java kullanarak gösteriyor, özel bir yazı tipi klasörü ayarlamayı, sistem yedekleme yazı tiplerini devre dışı bırakmayı ve optimal performans için rasterleştirme seçeneklerini ince ayarlamayı adım adım anlatıyor.

**Öğrenecekleriniz**
- ODP dönüşümü için özel bir yazı tipi dizini nasıl ayarlanır.  
- Sistem alternatif yazı tipleri nasıl devre dışı bırakılır, böylece yalnızca seçtiğiniz tipografiler kullanılır.  
- ODP dosyasını kesin boyutlar ve yazı tipi ayarlarıyla PNG olarak nasıl dışa aktarılır.  
- Büyük sunumları işlerken hız ve bellek kullanımını artırmak için ipuçları.

## Hızlı Yanıtlar
- **Maven kullanarak Aspose.Imaging ekleyebilir miyim?** Evet, Maven bağımlılığını ekleyin ve `mvn install` komutunu çalıştırın.  
- **Üretim ortamında lisansa ihtiyacım var mı?** Sınırsız kullanım için geçerli bir Aspose.Imaging lisansı gereklidir.  
- **Özel yazı tiplerim dikkate alınacak mı?** Yazı tipleri klasörünü ayarlayın ve sistem alternatiflerini devre dışı bırakarak bunları zorunlu kılın.  
- **Hangi görüntü formatları destekleniyor?** Aspose.Imaging, PNG, JPEG, TIFF ve WebP dahil olmak üzere 120'den fazla raster ve vektör formatını destekler.  
- **API çok iş parçacıklı (thread‑safe) mı?** Evet, çoğu Aspose.Imaging sınıfı, her iş parçacığı için ayrı örnekler oluşturduğunuzda eşzamanlı kullanım için güvenlidir.

## “how to convert odp” nedir?
*“How to convert odp”* ifadesi, bir OpenDocument Presentation dosyasını başka bir formata—genellikle PNG—dönüştürme sürecini, düzeni, yazı tiplerini ve görsel sadakati koruyarak tanımlar. Aspose.Imaging for Java, bu dönüşümü dış araçlara ihtiyaç duymadan tek‑metot bir iş akışıyla gerçekleştirir ve geliştiricilerin dönüşümü doğrudan uygulamalarına minimum kodla entegre etmelerini sağlar.

## Neden Aspose.Imaging for Java Kullanmalısınız?
Aspose.Imaging, **120+ çıktı formatı** destekler ve çok sayfalı ODP dosyalarını bellek içinde tüm belgeyi yüklemeden rasterleştirerek büyük sunumlarda en yüksek RAM kullanımını %70’e kadar azaltır. Kütüphane ayrıca yerleşik yazı tipi yönetimi sunar, üçüncü‑taraf render motorlarına olan ihtiyacı ortadan kaldırır.

## Önkoşullar
- **Kütüphaneler**: Aspose.Imaging for Java ≥ 25.5.  
- **JDK**: Versiyon 8 veya daha yenisi.  
- **IDE**: IntelliJ IDEA, Eclipse veya herhangi bir Java uyumlu editör.  
- **Temel Bilgi**: Java I/O, nesne‑yönelimli programlama ve görüntü kavramları.

## Kurulum Talimatları

### Maven
Aşağıdaki bağımlılığı `pom.xml` dosyanıza ekleyin ve `mvn clean install` komutunu çalıştırın:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
`build.gradle` dosyanıza kütüphaneyi ekleyin ve projeyi yenileyin:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Doğrudan İndirme
En son JAR dosyasını [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) adresinden indirin.

## Lisans Edinme Adımları
1. **Ücretsiz Deneme** – Lisans gerektirmez, sınırlı özellikler.  
2. **Geçici Lisans** – [Aspose web sitesinden](https://purchase.aspose.com/temporary-license/) bir lisans isteyin.  
3. **Satın Alma** – [Aspose satın alma sayfasından](https://purchase.aspose.com/buy) abonelik ya da kalıcı lisans satın alın.

Kütüphaneyi lisans dosyanızla başlatın:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## ODP Dönüşümü İçin Özel Bir Yazı Tipi Dizini Nasıl Ayarlanır?
`FontSettings` Aspose.Imaging için yazı tipi kaynaklarını yöneten bir sınıftır. Görüntü işleme başlamadan önce özel yazı tiplerinizi yükleyin. Bu, her slaytın sağladığınız tam tipografiyi kullanmasını sağlar.

Aspose.Imaging’in `FontSettings` sınıfını kullanarak yazı tipleri klasör yolunu ayarlayın:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Definition anchor*: `FontSettings.setFontsFolder` Aspose.Imaging’e dosya sisteminde TrueType ve OpenType yazı tiplerini nerede arayacağını söyler.

## ODP Dönüşümü Sırasında Sistem Alternatif Yazı Tiplerini Nasıl Devre Dışı Bırakırsınız?
Sistem alternatiflerini devre dışı bırakmak, render motorunun işletim sistemine kurulu yazı tiplerini görmezden gelmesini sağlar; böylece yalnızca siz sağladığınız yazı tipleri kullanılır. Bu, slaytlarınızın görsel görünümünü değiştirebilecek beklenmedik yazı tipi ikamelerini ortadan kaldırır.

Aşağıdaki çağrıyı kullanarak sistem alternatiflerini devre dışı bırakın:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Definition anchor*: `FontSettings.setGetSystemAlternativeFont(false)` motoru yalnızca tanımladığınız klasördeki yazı tiplerini kullanmaya zorlar, beklenmedik ikameleri ortadan kaldırır.

## Belirli Bir Yazı Tipiyle ODP Dosyasını PNG'ye Nasıl Dışa Aktarırsınız?
`RasterizationOptions` vektör sayfalarının bitmap görüntülere nasıl rasterleştirileceğini tanımlar. Yazı tipi yapılandırmasını rasterleştirme ayarlarıyla birleştirerek DPI, arka plan rengi ve sayfa boyutunu her dışa aktarılan PNG için kontrol edebilirsiniz.

Aşağıda gösterildiği gibi dışa aktarma metodunu uygulayın:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*Definition anchor*: `RasterizationOptions` sınıfı, oluşturulan PNG dosyaları için DPI, sayfa boyutu ve arka plan rengini kontrol eder.

### Yaygın Tuzaklar ve Çözümler
- **Eksik yazı tipi dosyaları** – ODP içinde referans verilen her `.ttf` veya `.otf` dosyasının ayarladığınız klasörde bulunduğunu doğrulayın.  
- **Yanlış dosya yolları** – Mutlak yollar kullanın veya göreli yolları `System.getProperty("user.dir")` üzerinden çözün.  
- **Yetersiz izinler** – Java sürecinin yazı tipi klasörünü okuyabildiğinden ve çıktı klasörüne yazabildiğinden emin olun.

## Pratik Uygulamalar
1. **Marka tutarlı slayt paketleri** – Sunumları web yayıncılığı için PNG olarak dışa aktarın ve kurumsal yazı tiplerini koruyun.  
2. **Otomatik rapor oluşturma** – Her slaytı PDF raporları veya e‑posta bültenlerine eklemek için bir görüntüye dönüştürün.  
3. **Eski arşiv oluşturma** – ODP içeriğini PNG olarak saklayın, böylece gelecekte ODP görüntüleyicilerine ihtiyaç duymadan erişilebilir olur.

## Performans Düşünceleri
- En son Aspose.Imaging sürümünü kullanarak çok iş parçacıklı rasterleştirme iyileştirmelerinden (8 çekirdekli CPU'larda 2× daha hızlı) faydalanın.  
- Görüntü işleme kodunu bir try‑with‑resources bloğuna sararak yerel kaynakların zamanında serbest bırakılmasını garantileyin.  
- Binlerce slaytı işlerken kalite ve bellek kullanımını dengelemek için `RasterizationOptions` ayarlarını (ör. DPI'yi düşürmek) ayarlayın.

## Sıkça Sorulan Sorular

**S: Minimum Java sürümü nedir?**  
**C:** Aspose.Imaging for Java JDK 8 ve üzeri sürümlerle çalışır; uzun vadeli destek için JDK 11 önerilir.

**S: Yalnızca seçili slaytları dönüştürebilir miyim?**  
**C:** Evet, `save` metodunu çağırmadan önce `rasterizationOptions.setPageNumber(specificSlideIndex)` ayarlayın.

**S: Şifre korumalı ODP dosyalarını nasıl yönetirim?**  
**C:** Şifreyi içeren `LoadOptions` ile dosyayı yükleyin, ardından aynı yazı tipi ayarlarıyla devam edin.

**S: Sistem yazı tiplerini devre dışı bırakmak performansı etkiler mi?**  
**C:** Motorun sistem yazı tiplerini aramamasını sağladığı için hızda hafif bir artış olur; özellikle çok sayıda yazı tipine sahip makinelerde belirgindir.

**S: Daha fazla kod örneği nerede bulunabilir?**  
**C:** Toplu dönüşüm ve görüntü dönüşümleri gibi ek senaryolar için resmi [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/) sayfasını inceleyin.

## Ek Kaynaklar
- [Aspose.Imaging for Java sürümleri](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Sürümleri](https://releases.aspose.com/imaging/java/)  
- [Ücretsiz Denemenizi Başlatın](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Dokümantasyonu](https://reference.aspose.com/imaging/java/)  
- [Aspose.Imaging Forum](https://forum.aspose.com/c/imaging/14)  
- [Aspose Lisansını Satın Al](https://purchase.aspose.com/buy)  
- [Geçici Lisans Başvurusu](https://purchase.aspose.com/temporary-license/)  

---

**Son Güncelleme:** 2026-06-28  
**Test Edilen:** Aspose.Imaging for Java 25.5  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.Imaging for Java ile ODG'yi PNG'ye Dönüştürme: Tam Kılavuz](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Java'da Aspose.Imaging ile Verimli Görüntü Dönüşümü: Tam Kılavuz](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}