---
date: 2026-01-17
description: Aspose.Imaging ile Java’da medyan filtresini kullanarak görüntü gürültüsünü
  nasıl kaldıracağınızı öğrenin. Bu adım adım öğretici, görüntü gürültüsünü azaltmak
  için Medyan ve Wiener filtrelerinin uygulanmasını kapsar.
linktitle: Median Filter Java – Apply Median and Wiener Filters
second_title: Aspose.Imaging Java Image Processing API
title: Median Filtre Java – Median ve Wiener Filtrelerini Uygula
url: /tr/java/image-processing-and-enhancement/median-and-wiener-filter-application/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Medyan Filtre Java – Medyan ve Wiener Filtrelerini Uygulama

Görüntü işleme dünyasında, gürültüyü ortaya çıkaran ve görüntüdeki genişlemeyi artıran kritik renklerdir. **median filter java** ile Aspose.Imaging for Java kullanarak resimleri etkili bir şekilde temizleyebilirsiniz. Bu öğretirken, bir parlaklığı gürültüsüzleştirmek için Median ve Wiener filtrelerini uygulama sürecini adım adım gösterirz, bu sayede karmaşık kod yazmadan profesyonel düzeyde sonuçlar elde edebilirsiniz.

## Hızlı Yanıtlar
- **Medyan filtre ne yapar?** Her pikseli, komşuların medyan değeriyle değiştirir, darbe gürültülerini temizlerken sizi korur.
- **Hangi kütüphanesi median filter java'yı kullanıma hazır mı?** Aspose.Imaging for Java, kullanıma hazır bir `MedianFilterOptions` sınıfı sağlar.
- **Kodu çalıştırmak için lisansa ihtiyacınız var mı?** Değerlendirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.
- **Median filtreyi diğer filtrelerle zincirleyebilir miyim?** Evet, median adımından sonra Wiener gibi ek filtreler uygulayabilirsiniz.
- **Hangi görüntü formatları destekleniyor mu?** Çoğu raster formatı (PNG, JPEG, BMP, TIFF, vb.) tam olarak desteklenir.

## Java Medyan Filtresi nedir?
Median filtre, **görüntü gürültünü çıkarmak** için yaygın olarak kullanılan doğrusal olmayan bir dijital depolama makinesidir. Java'da Aspose.Imaging, bu filtreyi `MedianFilterOptions` sınıfı aracılığıyla uygular ve kaç komşu pikselin kaydedilmediğini, hücrelerin çekirdek çekirdeklerini belirtmenize olanak tanır.

## Görüntü Gürültü Giderme için Neden Medyan Filtre Java Kullanılmalı?
- **Kenarları** ortalama basit filtrelerinden daha iyi korur.
- **Basit API** – birkaç satır kodla lekeleri ve tuz‑biber gürültülerini temizler.
- **Her raster görüntüde çalışır** Aspose.Imaging ile yüklenen, sunucu‑tarafı işleme için idealdir.

## Önkoşullar
Dalışa başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Geliştirme Ortamı** – JDK 8 veya daha yeni bir sürüm yüklü.
2. **Aspose.Imaging for Java** – Kütüphaneyi [buradan](https://releases.aspose.com/imaging/java/) indirip kurun.
3. **Örnek ürünlerilü Görüntü** – Temizlemek istediğiniz herhangi bir görüntü; bu kılavuzda `your‑noisy‑image.png` dosyalarını kullanacağız.

## Paketleri İçe Aktar
Java projenizde gerekli Aspose.Imaging sınıflarını içe aktararak başlayın:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.imagefilters.filteroptions.MedianFilterOptions;
```

## Java ile Medyan Filtresi Nasıl Uygulanır
Aşağıda adım adım bir kılavuz bulunmaktadır. Her adım, kısa bir açıklama ve ardından kopyalamanız gereken tam kodu içerir.

### Adım 1: Gürültülü Görüntüyü Yükleyin
Öncelikle, gürültüsünü gidermek istediğiniz görüntüyü yükleyin. Bu, Aspose.Imaging'in `Image.load` yöntemini kullanarak **Java'da görüntü yüklemeyi** göstermektedir.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (Image image = Image.load(dataDir + "your-noisy-image.png"))
{
    // Cast the image into RasterImage
    RasterImage rasterImage = (RasterImage) image;
```

### Adım 2: Medyan Filtresini Oluşturun ve Yapılandırın
`MedianFilterOptions` sınıfından bir örnek oluşturun ve çekirdek boyutunu ayarlayın. Daha büyük bir boyut daha fazla gürültüyü giderir ancak ayrıntıları bulanıklaştırabilir.

```java
    // Create an instance of MedianFilterOptions class and set the size.
    MedianFilterOptions options = new MedianFilterOptions(4);
```

### Adım 3: Medyan Filtresini Uygulayın
Filtreyi tüm görüntü sınırlarına uygulayın. Bu, temel **medyan filtresi uygulama** işlemidir.

```java
    // Apply Median filter to RasterImage object.
    rasterImage.filter(image.getBounds(), options);
```

### Adım 4: Sonuç Görüntüsünü Kaydedin
Son olarak, gürültüsü giderilmiş görüntüyü diske yazın. Artık medyan filtresinin etkisini görebilirsiniz.

```java
    // Save the resultant image
    image.save("Your Document Directory" + "denoised-image.png");
}
```

## Yaygın Sorunlar ve Çözümler
- **Çekirdek boyutu çok büyük** – Görüntü aşırı çıktısı yansıtılmaz. Çoğu fotoğraf için 3‑5 arasında sonuçlar hatalı.
- **Desteklenmeyen görüntü formatı** – Dosyanın Aspose.Imaging tarafından bir raster formatının olduğundan emin olun.
- **OutOfMemoryError** – Büyük kayıtlardan önce `RasterImage` sınıfının `crop` yöntemiyle daha küçük parçalar halinde işleyin.

## Çözüm
Bu kılavuzda, Aspose.Imaging tarafından sağlanan **median filter java** tedavisini kullanarak **görüntüleri nasıl gürültüzleştireceğinizi** gösterdik. Yukarıdaki adımları izleyerek entegre, gürültüyü kaldırmayı herhangi bir Java tabanlı görüntü işleme hattına hızlı bir şekilde yapabilir ve sonuçları Wiener filtresi veya diğer gelişmiş tekniklerle zincirleme yaparak daha da iyileştirebilirsiniz.

## Sıkça Sorulan Sorular

**S1: Aspose.Imaging for Java nedir?**  
C1: Aspose.Imaging for Java, geliştiricilerin görüntülerle çalışmasını ve çeşitli görüntü işleme görevlerini programlı olarak gerçekleştirmesini sağlayan bir Java kütüphanesidir.

**S2: Aspose.Imaging for Java'ı ücretsiz kullanabilir miyim?**  
C2: Aspose.Imaging for Java ticari bir kütüphanedir, ancak [buradan](https://releases.aspose.com/) ücretsiz deneme sürümünü edinebilirsiniz. Ancak, uzun vadeli kullanım için [buradan](https://purchase.aspose.com/buy) bir lisans satın almanız gerekir.

**S3: Aspose.Imaging for Java için nasıl destek alabilirim?**  
C3: Aspose.Imaging topluluğu ve uzmanlarından [Aspose.Imaging Forum](https://forum.aspose.com/) üzerinden yardım ve destek alabilirsiniz.

**S4: Başka hangi görüntü iyileştirme teknikleri vardır?**  
C4: Median filtreye ek olarak, görüntü iyileştirme teknikleri arasında Wiener filtreleme, Gaussian bulanıklaştırma ve kontrast germe gibi yöntemler bulunur.

**S5: Aspose.Imaging for Java'ı web uygulamamda kullanabilir miyim?**  
C5: Evet, Aspose.Imaging for Java'ı sunucu‑tarafı görüntü işleme için web uygulamalarınıza entegre edebilirsiniz.

---

**Son Güncelleme:** 2026-01-17  
**Test Edilen:** Aspose.Imaging for Java 24.11  
**Yazar:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
