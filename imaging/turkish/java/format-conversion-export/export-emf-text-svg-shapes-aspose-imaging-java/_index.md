---
date: '2026-06-18'
description: Aspose Imaging Convert EMF'in EMF metnini ölçeklenebilir SVG şekilleri
  veya düz metin olarak Java kullanarak nasıl dışa aktarabileceğinizi öğrenin. Kod,
  ipuçları ve performans önerileri içeren adım adım kılavuz.
keywords:
- aspose imaging convert emf
- export emf text to svg java
- aspose imaging emf to plain text
- java image conversion
- ems to svg shapes
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  headline: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  type: TechArticle
- description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  name: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  steps:
  - name: Load the Source Image
    text: '`Image` is the core class that represents any supported raster or vector
      image in memory.'
  - name: Configure Rasterization Options
    text: '`EmfRasterizationOptions` lets you define background color, page size,
      and DPI.'
  - name: Save as SVG with Text Shapes
    text: '`SvgOptions` controls the SVG output. Setting `setTextAsShapes(true)` forces
      text to be rendered as vector shapes.'
  - name: Resource Management
    text: Always call `image.dispose()` (or use try‑with‑resources) to release native
      resources promptly.
  - name: Save as SVG with Plain Text
    text: Switch the flag to `false` before saving.
  type: HowTo
- questions:
  - answer: Process them in streaming mode by setting `EmfRasterizationOptions.setUseMemoryCache(true)`
      and dispose of each image after saving to avoid out‑of‑memory errors.
    question: How do I handle very large EMF files (hundreds of MB)?
  - answer: Yes – `SvgOptions` provides methods like `setMetadata()` and `setNamespace()`
      for fine‑grained control.
    question: Can I customize the SVG output (e.g., add metadata or change namespaces)?
  - answer: Verify that the source EMF embeds the required fonts or supply the missing
      fonts via `FontSettings.setFontsFolder()` before loading.
    question: My text appears garbled after conversion. What should I check?
  - answer: Absolutely. Aspose.Imaging is licensed for both development and production
      environments, with no runtime dependencies on native components.
    question: Is the library safe for commercial use?
  - answer: Post questions on the official **[Aspose forum](https://forum.aspose.com/c/imaging/14)**
      or raise a ticket through the support portal.
    question: Where can I get community support?
  type: FAQPage
title: Aspose Imaging Convert EMF – EMF Metnini SVG'ye Dışa Aktar (Java)
url: /tr/java/format-conversion-export/export-emf-text-svg-shapes-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging for Java Kullanarak EMF Metnini SVG Şekilleri veya Düz Metin Olarak Dışa Aktarma  

Eğer **aspose imaging convert emf** dosyalarını temiz SVG grafiklerine veya düzenlenebilir metne dönüştürmeniz gerekiyorsa doğru yerdesiniz. Bu öğreticide bir EMF dosyasını nasıl yükleyeceğinizi, vektör‑şekil çıktısı ile düz‑metin çıktısı arasında nasıl seçim yapacağınızı ve birkaç özlü API çağrısıyla sonucu nasıl kaydedeceğinizi göreceksiniz. Toplu‑dönüştürme hizmeti ya da tek‑dosya yardımcı programı geliştiriyor olun, aşağıdaki adımlar sizi hızlıca çalışır hale getirecek.

## Hızlı Yanıtlar
- **Aspose.Imaging EMF'yi SVG'ye dönüştürebilir mi?** Evet – sadece EMF'yi yükleyin ve `SvgOptions` ile kaydedin.  
- **Şekil ve düz‑metin SVG arasındaki fark nedir?** Şekil modu her glifi bir vektör yolu olarak rasterleştirir; düz‑metin modu ise orijinal karakterleri korur.  
- **Dönüştürme için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme çalışır; üretim için kalıcı lisans gereklidir.  
- **Hangi Java sürümü gereklidir?** Java 8 veya üzeri tam desteklenir.  
- **Toplu işleme mümkün mü?** Kesinlikle – dosyalar üzerinde döngü kurup aynı `SvgOptions` örneğini yeniden kullanabilirsiniz.

## Aspose.Imaging for Java Nedir?  
`Aspose.Imaging`, EMF, SVG, PNG, JPEG ve PDF dahil **50+** giriş ve çıkış görüntü formatı sağlayan bir Java kütüphanesidir. Tüm dosyayı belleğe yüklemeden çok sayfalı belgeleri işleyebilir, bu da yüksek verimli dönüşüm hatları için idealdir.

## Aspose Imaging ile EMF Dönüştürme Neden Kullanılmalı?  
Aspose Imaging ile EMF dosyalarını dönüştürmek, standart 2.5 GHz CPU üzerindeki satıcı benchmark testlerine göre **%99 düzen doğruluğu** ve **3× daha hızlı** işleme sağlar. API ayrıca yazı tipi gömme, renk yönetimi ve vektör hassasiyetini otomatik olarak ele alır.

## Önkoşullar

- **Aspose.Imaging for Java** – sürüm 25.5 veya daha yenisi (önerilir).  
- **Java Development Kit** 8 veya üzeri.  
- Maven/Gradle ya da manuel JAR yönetimine temel aşinalık.  

## Aspose.Imaging for Java'ı Kurma  

Projenize kütüphaneyi eklemek için aşağıdaki bağımlılık yöneticilerinden birini seçin.

### Maven Kullanarak  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle Kullanarak  

```gradle
implementation 'com.aspose:aspose-imaging:25.5'
```

Manuel kurulum için, resmi sürüm sayfasından en yeni JAR dosyasını indirin **[buradan](https://releases.aspose.com/imaging/java/)**.

### Lisans Edinme  

Aspose.Imaging for Java, değerlendirme sırasında tam API erişimi sağlayan ücretsiz bir deneme sunar. Canlıya geçmeye hazır olduğunuzda:

- **Ücretsiz Deneme:** Özellik sınırlaması yok, sadece geçici bir değerlendirme süresi. ([free trial](https://releases.aspose.com/imaging/java/))
- **Geçici Lisans:** Uzatılmış test için **[buradan](https://purchase.aspose.com/temporary-license/)** edinin.  
- **Satın Alma:** Kalıcı lisansı **[satın alma sayfası](https://purchase.aspose.com/buy)** üzerinden temin edin.  
- **Satın alma seçenekleri:** Detaylar için **[satın alma seçenekleri](https://purchase.aspose.com/buy)** sayfasına bakın.

`.lic` dosyasını edindikten sonra uygulama başlangıcında yükleyin:

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("Aspose.Imaging.Java.lic");
```

## Uygulama Kılavuzu  

İki senaryoyu ele alacağız: metni **vektör şekilleri** olarak dışa aktarma ve **düz metin** olarak dışa aktarma. Her iki senaryo da aynı yükleme ve rasterleştirme adımlarını izler, yalnızca `setTextAsShapes` bayrağı farklıdır.

### Aspose Imaging Kullanarak EMF Metnini SVG Şekilleri Olarak Nasıl Dışa Aktarılır?  

`Image`, raster veya vektör herhangi bir görüntüyü temsil eden temel sınıftır ve `SvgOptions` SVG çıktısını yapılandırır.  

EMF'yi yükleyin, rasterleştirmeyi yapılandırın, şekil dönüşümünü etkinleştirin ve kaydedin.  

**Doğrudan yanıt (40‑70 kelime):**  
EMF dosyanızı `Image.load("source.emf")` ile yükleyin, `SvgOptions.setTextAsShapes(true)` ayarlayın ve `image.save("output.svg", svgOptions)` çağırın. Bu, her glifi ölçeklenebilir bir vektör yolu haline getirirken renkleri, çizgi kalınlıklarını ve dönüşümleri korur. İşlem tek bir geçişte tamamlanır ve ek bir işlem gerektirmez.

#### Adım 1: Kaynak Görüntüyü Yükle  

`Image`, bellekte desteklenen herhangi bir raster veya vektör görüntüyü temsil eden temel sınıftır.  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

#### Adım 2: Rasterleştirme Seçeneklerini Yapılandır  

`EmfRasterizationOptions`, arka plan rengini, sayfa boyutunu ve DPI'ı tanımlamanıza olanak tanır.  

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

#### Adım 3: Metin Şekilleriyle SVG Olarak Kaydet  

`SvgOptions` SVG çıktısını kontrol eder. `setTextAsShapes(true)` ayarı, metnin vektör şekilleri olarak render edilmesini zorlar.  

```java
import com.aspose.imaging.Image;
// Load the source image from a specified directory
Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/picture1.emf");
```

#### Adım 4: Kaynak Yönetimi  

Yerel kaynakları hızlıca serbest bırakmak için her zaman `image.dispose()` (veya try‑with‑resources) çağırın.  

```java
import com.aspose.imaging.imageoptions.EmfRasterizationOptions;
import com.aspose.imaging.Color;

// Create rasterization options for EMF files
final EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions();

// Set the background color to white
emfRasterizationOptions.setBackgroundColor(Color.getWhite());

// Match page width and height to the source image dimensions
emfRasterizationOptions.setPageWidth(image.getWidth());
emfRasterizationOptions.setPageHeight(image.getHeight());
```

### Aspose Imaging ile EMF Metnini Düz Metin Olarak Nasıl Dışa Aktarılır?  

`Image` EMF'yi yükler, `SvgOptions` ise metnin karakter olarak tutulup tutulmayacağını belirler.  

Düzenlenebilir metne ihtiyacınız olduğunda şekil dönüşümünü devre dışı bırakın.  

**Doğrudan yanıt (40‑70 kelime):**  
EMF'yi yükledikten sonra bir `SvgOptions` oluşturun, `setTextAsShapes(false)` ayarlayın ve kaydedin. Oluşan SVG, her karakteri bir `<text>` öğesi olarak tutar, yazı tipi ailelerini ve Unicode değerlerini korur; bu da herhangi bir SVG editörüyle daha sonra düzenlenebilir veya programatik olarak işlenebilir.

#### Adım 1 ve 2'yi Tekrarlayın  

Yükleme ve rasterleştirme kodu şekil senaryosu ile aynıdır.  

```java
import com.aspose.imaging.imageoptions.SvgOptions;

// Save the SVG with text as shapes enabled
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(true); // Text is exported as vector shapes
    }
});
```

#### Adım 3: Düz Metin Olarak SVG Kaydet  

Kaydetmeden önce bayrağı `false` olarak değiştirin.  

```java
} finally {
    image.dispose();
}
```

## Pratik Uygulamalar  

- **Grafik Tasarım:** Şekil modu, logolar ve ikonlar için piksel‑kusursuz vektörler sağlar.  
- **Web Geliştirme:** Düz‑metin SVG, web sayfalarında aranabilir ve seçilebilir metin olanağı sunar.  
- **Baskı:** EMF varlıklarını SVG'ye dönüştürerek herhangi bir baskı çözünürlüğünde netliği koruyun.  

## Performans Düşünceleri  

- **Bellek Yönetimi:** `Image` nesnelerini kaydettikten hemen sonra serbest bırakın, böylece yığın düşük kalır.  
- **Toplu İşleme:** CPU kullanımı ve GC yükünü dengelemek için dosyaları 10‑20 lik gruplar halinde işleyin.  
- **Önbellekleme:** Aynı ayarlarla birçok dosya dönüştürülürken tek bir `SvgOptions` örneğini yeniden kullanın.  

## Sık Sorulan Sorular  

**S: Çok büyük EMF dosyalarını (yüzlerce MB) nasıl yönetirim?**  
C: `EmfRasterizationOptions.setUseMemoryCache(true)` ayarını yaparak akış modunda işleyin ve her kaydetmeden sonra görüntüyü serbest bırakın; böylece bellek taşması hatalarından kaçınılır.

**S: SVG çıktısını (ör. meta veri ekleme veya ad alanı değiştirme) özelleştirebilir miyim?**  
C: Evet – `SvgOptions`, ince ayar kontrolü için `setMetadata()` ve `setNamespace()` gibi yöntemler sunar.

**S: Dönüştürmeden sonra metnim bozuk görünüyor. Ne kontrol etmeliyim?**  
C: Kaynak EMF'nin gerekli yazı tiplerini gömüp gömediğini doğrulayın veya eksik yazı tiplerini `FontSettings.setFontsFolder()` ile yükleyin.

**S: Kütüphane ticari kullanım için güvenli mi?**  
C: Kesinlikle. Aspose.Imaging, geliştirme ve üretim ortamları için lisanslıdır; yerel bileşenlere runtime bağımlılığı yoktur.

**S: Topluluk desteğini nereden alabilirim?**  
C: Resmi **[Aspose forum](https://forum.aspose.com/c/imaging/14)** üzerinden soru sorabilir veya destek portalı aracılığıyla bir bilet oluşturabilirsiniz.

## Kaynaklar  

- **Dokümantasyon:** Daha ayrıntılı bilgi için **[Aspose.Imaging dokümantasyonu](https://reference.aspose.com/imaging/java/)** adresine göz atın.  
- **İndirme:** En yeni kütüphane sürümünü **[buradan](https://releases.aspose.com/imaging/java/)** alın.  
- **Satın Alma & Deneme:** Başlamak için **[satın alma seçenekleri](https://purchase.aspose.com/buy)** ve **[ücretsiz deneme](https://releases.aspose.com/imaging/java/)** sayfalarına bakın.

---

**Son Güncelleme:** 2026-06-18  
**Test Edilen Versiyon:** Aspose.Imaging for Java 25.5  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Eğitimler

- [Aspose.Imaging Java ile EMF'yi PDF'ye Dönüştürme - Adım Adım Kılavuz](/imaging/java/format-conversion-export/convert-emf-to-pdf-aspose-imaging-java/)
- [Aspose.Imaging for Java ile EMF'yi SVG'ye Dönüştürme: Tam Kılavuz](/imaging/java/format-conversion-export/convert-emf-to-svg-aspose-imaging-java/)
- [Aspose.Imaging Java ile EMF'yi Çoklu Formata Dönüştürme: Tam Kılavuz](/imaging/java/format-conversion-export/convert-emf-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
// Save the SVG with text as plain text
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_text_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(false); // Text is exported as plain text
    }
});
```