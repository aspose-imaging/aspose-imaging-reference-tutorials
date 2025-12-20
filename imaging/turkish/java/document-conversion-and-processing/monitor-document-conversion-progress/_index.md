---
date: 2025-12-20
description: Aspose.Imaging kullanarak Java’da görüntü dönüşümünü nasıl izleyebileceğinizi
  öğrenin. Dönüşüm ilerlemesini takip etmek ve JPG/PNG formatlarını işlemek için adım
  adım rehber.
linktitle: Monitor Image Conversion in Java
second_title: Aspose.Imaging Java Image Processing API
title: Java'da Görüntü Dönüşümünü İzle
url: /tr/java/document-conversion-and-processing/monitor-document-conversion-progress/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Java’da Görüntü Dönüştürmeyi İzleme

Bu öğreticide **Java’da görüntü dönüştürmeyi nasıl izleyebileceğinizi** Aspose.Imaging ile keşfedeceksiniz. **JPG’yi PNG’ye dönüştürmek**, görüntü formatlarını değiştirmek ya da sadece yükleme ilerlemesini takip etmek ister misiniz, her adımı sizinle paylaşacak, her parçanın neden önemli olduğunu açıklayacak ve dönüşüm sırasında gerçek‑zamanlı geri bildirim almanın yollarını göstereceğiz.

## Giriş

Aspose.Imaging for Java, Java uygulamalarınızda görüntülerle çalışmak için çok yönlü ve zengin özellikli bir kütüphanedir. **Java’da görüntü formatı dönüştürme**, resim yeniden boyutlandırma ya da gelişmiş filtreler uygulama ihtiyacınız olsun, Aspose.Imaging kapsamlı bir API sunar. Bu rehberde, özellikle büyük dosyalar veya toplu işlemler için kullanıcıya ilerleme göstermek istediğinizde faydalı olan dönüşüm sürecini izlemeye odaklanacağız.

## Hızlı Yanıtlar
- **“monitor image conversion java” ne demektir?** Java kullanarak bir görüntüyü formatlar arasında dönüştürürken yükleme ve kaydetme ilerlemesinin izlenmesi anlamına gelir.
- **Hangi kütüphane ilerleme geri aramalarını destekler?** Aspose.Imaging for Java, hem yükleme hem de dışa aktarma işlemleri için `ProgressEventHandler` sunar.
- **JPG’yi PNG’ye ilerleme izleyerek dönüştürebilir miyim?** Evet – çıktı `JpegOptions` yerine `PngOptions` olarak değiştirin ve aynı geri aramaları kullanın.
- **Geliştirme için lisansa ihtiyacım var mı?** Değerlendirme için geçici bir lisans yeterlidir; üretim için tam lisans gereklidir.
- **Hangi Java sürümü gereklidir?** Java 8 veya üzeri desteklenir.

## “monitor image conversion java” nedir?

Java’da görüntü dönüşümünü izlemek, yükleme ve kaydetme sırasında işlenen bayt sayısı hakkında gerçek‑zamanlı güncellemeler almaktır. Bu, Aspose.Imaging’in `ProgressEventHandler` aracılığıyla **LoadStarted**, **LoadCompleted**, **ExportStarted** ve **ExportCompleted** gibi olayların raporlanmasıyla sağlanır. Bu olaylara bağlanarak ilerleme çubukları gösterebilir, durumları loglayabilir ya da uygulamanızda başka eylemler tetikleyebilirsiniz.

## Neden görüntü dönüşümünü izlemelisiniz?

- **Kullanıcı Deneyimi:** Büyük görüntüler saniyelerden dakikalara kadar sürebilir; ilerleme göstermek kullanıcıları bilgilendirir.
- **Hata Yönetimi:** Duraklamalar ya da hatalar erken tespit edilerek yeniden deneme veya zarif bir şekilde iptal etme imkanı sağlar.
- **Performans İçgörüleri:** Her aşamanın ne kadar sürdüğünü bilmek toplu işlerinizde optimizasyon yapmanıza yardımcı olur.

## Ön Koşullar

1. **Java Geliştirme Ortamı** – En yeni JDK’yı [Oracle web sitesinden](https://www.oracle.com/java/technologies/javase-downloads) indirin.
2. **Aspose.Imaging for Java** – Kütüphaneyi [Aspose.Imaging for Java sayfasından](https://releases.aspose.com/imaging/java/) indirin. JAR dosyasını projenizin sınıf yoluna ekleyin.
3. **IDE** – Eclipse, IntelliJ IDEA veya NetBeans kullanılabilir.

## Paketleri İçe Aktarma

Ön koşullar hazır olduğunda gerekli sınıfları içe aktarın. İçe aktarmalar temel `Image` sınıfını, yükleme seçeneklerini, JPEG seçeneklerini ve ilerleme‑olay arayüzlerini içerir.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.LoadOptions;
import com.aspose.imaging.imageoptions.JpegOptions;
import com.aspose.imaging.imageloadoptions.ProgressEventHandler;
import com.aspose.imaging.imageloadoptions.ProgressEventHandlerInfo;
import java.nio.file.Path;
import java.util.logging.Logger;
```

## Adım 1: Dizin ve Giriş Görüntüsünü Ayarlama

Kaynak görüntünüzün nerede bulunduğunu ve adını tanımlayın. JPG, PNG, BMP vb. desteklenen herhangi bir formatı gösterebilirsiniz.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
String fileName = "aspose-logo.jpg";
String inputFileName = dataDir + fileName;
```

> **İpucu:** Gerçek projelerde platform‑bağımsız yollar için `Paths.get(...)` kullanın.

## Adım 2: Giriş Görüntüsünü Yükleme

Görüntüyü yüklemek, ilerleme olaylarını almaya başladığınız yerdir. `ProgressEventHandler`, her bir parça işlendiğinde `progressCallback`i tetikler.

```java
try (Image image = Image.load(inputFileName, new LoadOptions() {
    {
        setIProgressEventHandler(new ProgressEventHandler() {
            @Override
            public void invoke(ProgressEventHandlerInfo info) {
                progressCallback(info);
            }
        });
    }
})) {
    // Image loaded successfully
    // You can perform further operations on the loaded image here
}
```

`try‑with‑resources` bloğu, görüntünün otomatik olarak serbest bırakılmasını sağlar; bu büyük dosyalar için önemlidir.

## Adım 3: Çıktı Görüntüsünü Kaydetme

Şimdi görüntüyü dışa aktarın. Bu örnekte JPEG olarak baseline sıkıştırma ve %100 kalite ile kaydediyoruz, ancak `PngOptions`a geçerek **convert JPG PNG java** tarzı dönüşümler yapabilirsiniz.

```java
image.save(
    Path.combine("Your Document Directory", "outputFile_Baseline.jpg"),
    new JpegOptions() {
        {
            setCompressionType(JpegCompressionMode.Baseline);
            setQuality(100);
            setProgressEventHandler(new ProgressEventHandler() {
                @Override
                public void invoke(ProgressEventHandlerInfo info) {
                    exportProgressCallback(info);
                }
            });
        }
    });
```

Çıktı yolunu ve dosya adını ihtiyacınıza göre değiştirin. Aynı geri arama mekanizması, dışa aktarma ilerlemesini canlı olarak verir.

## Adım 4: İlerleme Geri Aramaları

Hem yükleme hem de kaydetme, durumu raporlamak için geri aramalar kullanır. Aşağıda yalnızca ilerlemeyi konsola kaydeden yardımcı metodlar bulunur.

```java
static void progressCallback(ProgressEventHandlerInfo info) {
    Logger.printf("Progress %s : %d/%d", info.getEventType(), info.getValue(), info.getMaxValue());
}

static void exportProgressCallback(ProgressEventHandlerInfo info) {
    Logger.printf("Export event %s : %d/%d", info.getEventType(), info.getValue(), info.getMaxValue());
}
```

`Logger.printf`i, bir Swing ilerleme çubuğunu güncellemek ya da WebSocket mesajı göndermek gibi herhangi bir UI güncelleme mantığıyla değiştirebilirsiniz.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|--------------|-------|
| **İlerleme çıktısı yok** | Geri arama eklenmemiş veya logger yapılandırılmamış | `setIProgressEventHandler` (yükleme) ve `setProgressEventHandler` (kaydetme) ayarlandığından ve logger’ın konsola veya UI’ya yazdığından emin olun. |
| **Büyük dosyalarda OutOfMemoryError** | Görüntü tamamen belleğe yükleniyor | `ImageLoadOptions` ile `setBufferSize` kullanın veya mümkün olduğunda görüntüyü parçalar halinde işleyin. |
| **Yanlış çıktı formatı** | PNG dönüşümü için `JpegOptions` kullanılıyor | `PngOptions`a geçin ve format‑özel ayarları düzenleyin. |
| **LicenseException** | Değerlendirme süresi dolmuş deneme sürümü kullanılıyor | `License license = new License(); license.setLicense("Aspose.Imaging.Java.lic");` ile geçici ya da tam lisans uygulayın. |

## Sık Sorulan Sorular

**S: Aspose.Imaging for Java hangi görüntü formatlarını destekler?**  
C: Aspose.Imaging for Java JPEG, PNG, BMP, TIFF, GIF, WebP ve daha birçok formatı destekler. Tam listeyi [dökümantasyonda](https://reference.aspose.com/imaging/java/) bulabilirsiniz.

**S: İlerleme izlerken gelişmiş görüntü düzenleme yapabilir miyim?**  
C: Evet. Görüntü yüklendikten sonra yeniden boyutlandırma, kırpma, filtre uygulama gibi işlemler yapabilir ve ardından ilerleme geri aramalarıyla kaydedebilirsiniz.

**S: Kütüphane büyük ölçekli toplu işleme için uygun mu?**  
C: Kesinlikle. API yüksek performanslı senaryolar için optimize edilmiştir ve ilerleme olayları her dosyayı ayrı ayrı izlemenizi sağlar.

**S: Test için geçici bir lisans nasıl alınır?**  
C: 30 gün geçerli bir deneme lisansı talep etmek için [geçici lisans sayfasını](https://purchase.aspose.com/temporary-license/) ziyaret edin.

**S: Topluluk desteği nereden alınabilir?**  
C: Aspose [destek forumu](https://forum.aspose.com/) sorularınızı sormak ve çözümler paylaşmak için harika bir yerdir.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2025-12-20  
**Test Edilen Versiyon:** Aspose.Imaging for Java 24.12 (latest)  
**Yazar:** Aspose  

---