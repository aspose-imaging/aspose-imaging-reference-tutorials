---
date: 2025-12-22
description: Aspose.Imaging for Java kullanarak TIFF görüntülerini nasıl kurtaracağınızı
  adım adım gösteren rehber, hasarlı görüntü verilerini hızlı ve güvenilir bir şekilde
  geri getirir.
linktitle: Recovering TIFF Image Data
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java ile TIFF Görüntülerini Nasıl Kurtarabilirsiniz
url: /tr/java/document-conversion-and-processing/recovering-tiff-image-data/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java ile TIFF Görüntülerini Nasıl Kurtarabilirsiniz

Dijital görüntüleme dünyasında **TIFF dosyalarını nasıl kurtarılır** sorunu, yüksek çözünürlüklü fotoğraflar, taranmış belgeler veya arşiv varlıklarıyla çalışan geliştiriciler için yaygın bir zorluktur. Bir TIFF bozulduğunda, tüm dosyayı atmak zorunda değilsiniz—Aspose.Imaging for Java, görüntü verilerini çıkarmanız ve yeniden oluşturmanız için gerekli araçları sağlar. Bu öğreticide, hasarlı TIFF görüntülerini kullanılabilir bir duruma geri getirebilmeniz için adım adım bir kurtarma sürecini pratik bir şekilde göstereceğiz.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.Imaging for Java  
- **Bozuk TIFF'leri kurtarabilir miyim?** Evet, `DataRecoveryMode` seçenekleriyle  
- **Üretim için lisansa ihtiyacım var mı?** Deneme dışı kullanım için ticari lisans gereklidir  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri  
- **Arka plan rengi isteğe bağlı mı?** Evet, istediğiniz herhangi bir `Color` ayarlayabilirsiniz  

## TIFF Görüntü Kurtarması Nedir?
TIFF (Tagged Image File Format), yüksek kaliteli görüntülerin depolanması için kullanılan esnek, kayıpsız bir formattır. Kurtarma, dosyayı hatalara rağmen okumak, eksik piksel verilerini yeniden oluşturmak ve isteğe bağlı olarak boşlukları bir arka plan rengiyle doldurmak anlamına gelir.

## Neden Aspose.Imaging for Java Kullanmalı?
- **Güçlü API** – Çok sayıda görüntü formatını, çok sayfalı TIFF'ler dahil, yönetir.  
- **Yerleşik kurtarma modları** – `ConsistentRecover` bozuk akışları otomatik olarak onarır.  
- **Yerel bağımlılık yok** – Saf Java, herhangi bir Maven/Gradle projesine kolayca entegre edilebilir.  

## Önkoşullar

- **Aspose.Imaging for Java** – En son JAR dosyasını resmi siteden [buradan](https://releases.aspose.com/imaging/java/) indirin.  
- **Java Geliştirme Ortamı** – JDK 8 veya daha yenisi, tercih ettiğiniz IDE veya yapı aracıyla.  

Temel bilgilerimizi ele aldığımıza göre, gerçek koda geçelim.

## Paketleri İçe Aktarma

İhtiyacımız olan sınıfları ilk olarak içe aktaralım. Bu ad alanları, görüntü yükleme, renk işleme ve kurtarma seçeneklerine erişim sağlar.

```java
import com.aspose.imaging.DataRecoveryMode;
import com.aspose.imaging.Image;
import com.aspose.imaging.Color;
import com.aspose.imaging.LoadOptions;
```

## TIFF Görüntülerini Kurtarma – Genel Bakış

Aşağıda dosya yolunu ayarlayacağız, kurtarma seçeneklerini yapılandıracağız ve sonunda bozuk TIFF'i yükleyeceğiz. Her adım sade bir dille açıklanmıştır, böylece kendi projelerinize uyarlayabilirsiniz.

### Adım 1: Belge Dizinini Tanımlama

TIFF dosyasının diskte bulunduğu yeri belirtin. Yer tutucuyu makinenizdeki gerçek klasörle değiştirin.

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
```

### Adım 2: LoadOptions Oluşturma

`LoadOptions`, Aspose.Imaging'e hasarlı dosyayla nasıl başa çıkacağını söyler. **Tutarlı kurtarma**yı etkinleştirir ve eksik pikseller için kırmızı bir arka plan rengi seçeriz.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setDataRecoveryMode(DataRecoveryMode.ConsistentRecover);
loadOptions.setDataBackgroundColor(Color.getRed());
```

- `DataRecoveryMode.ConsistentRecover` – Mümkün olduğunca orijinal veriyi koruyarak görüntüyü yeniden oluşturmayı dener.  
- `Color.getRed()` – Boşlukları kırmızı ile doldurur; iş akışınıza uygun herhangi bir renkle değiştirebilirsiniz.

### Adım 3: Hasarlı Görüntüyü Yükleme

Şimdi, az önce yapılandırdığımız seçeneklerle bozuk TIFF'i açıyoruz. `try‑with‑resources` bloğu, görüntünün doğru şekilde serbest bırakılmasını sağlar.

```java
try (Image image = Image.load(dataDir + "SampleTiff1.tiff", loadOptions)) {
    // Do some work on the recovered image
}
```

Bu blok içinde kurtarılan görüntüyü kaydedebilir, ek işleme uygulayabilir veya sadece özelliklerini inceleyebilirsiniz.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|--------------|------|
| **OutOfMemoryError** | Çok büyük TIFF'ler heap alanını aşar. | JVM `-Xmx` parametresini artırın veya görüntüyü parçalar halinde işleyin. |
| **Veri kurtarılmadı** | Dosya, kurtarma modunun ötesinde ciddi şekilde bozulmuş. | Farklı bir `DataRecoveryMode` (ör. `PartialRecover`) deneyin veya yedekten geri yükleyin. |
| **Yanlış arka plan rengi** | Varsayılan renk bazı görüntülerde görünmez. | `loadOptions.setDataBackgroundColor(Color.getWhite())` gibi istediğiniz özel rengi ayarlayın. |

## Sık Sorulan Sorular

**S: Veri kurtarmada arka plan renginin ayarlanmasının önemi nedir?**  
C: Arka plan rengi, yeniden oluşturulamayan pikselleri doldurarak hasarlı alanları kolayca görmenizi ve tutarlı bir görsel çıktı elde etmenizi sağlar.

**S: Aspose.Imaging for Java ile TIFF dışındaki diğer formatları da kurtarabilir miyim?**  
C: Evet, Aspose.Imaging JPEG, PNG, BMP ve daha birçok formatı destekler. Kurtarma iş akışı benzerdir; sadece dosya uzantısını değiştirmeniz yeterlidir.

**S: Kurtarılabilecek TIFF görüntüsünün boyutu için bir limit var mı?**  
C: Kurtarma, bozulmanın derecesi ve sistem belleğine bağlıdır. Aşırı büyük veya ağır hasarlı dosyalar ek kaynak veya parçalı işleme gerektirebilir.

**S: Aspose.Imaging for Java içinde ek görüntü işleme araçları var mı?**  
C: Kesinlikle. Kütüphane yeniden boyutlandırma, kırpma, filtreleme ve format dönüşümü gibi özellikler sunar; böylece hem kurtarabilir hem de görüntüleri tek bir pipeline’da iyileştirebilirsiniz.

**S: Aspose.Imaging for Java’yı ticari projelerde kullanabilir miyim?**  
C: Evet, üretim kullanımı için ticari bir lisans gereklidir. Lisansı [buradan](https://purchase.aspose.com/buy) temin edebilirsiniz.

**S: Kurtarılan görüntüyü yeni bir dosyaya nasıl kaydederim?**  
C: Yükleme sonrası `try` bloğu içinde `image.save("RecoveredImage.tiff");` çağrısını yapın.

## Sonuç

TIFF görüntü verilerini kurtarmak, yüksek çözünürlüklü veya arşiv grafiklerle çalışan herkes için hayati bir beceridir. Aspose.Imaging for Java’nın `DataRecoveryMode` ve arka plan rengi seçeneklerini kullanarak, bozuk dosyaları minimal kodla yeniden oluşturabilirsiniz. Yukarıdaki adımları bir şablon olarak alın, yolları ve renkleri ihtiyacınıza göre uyarlayın; böylece görsel varlıklarınızı güvenli ve kullanılabilir tutarsınız.

---

**Son Güncelleme:** 2025-12-22  
**Test Edilen Versiyon:** Aspose.Imaging for Java 24.11 (yazım anındaki en yeni)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}