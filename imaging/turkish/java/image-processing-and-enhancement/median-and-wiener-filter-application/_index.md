---
title: Medyan ve Wiener Filtre Uygulaması
linktitle: Medyan ve Wiener Filtre Uygulaması
second_title: Aspose.Imaging Java Görüntü İşleme API'si
description: Aspose.Imaging for Java ile görüntü kalitesini nasıl artıracağınızı öğrenin. Bu adım adım eğitim, görüntü kirliliğini gidermeye yönelik Medyan ve Wiener filtre uygulamalarını kapsar.
weight: 19
url: /tr/java/image-processing-and-enhancement/median-and-wiener-filter-application/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Medyan ve Wiener Filtre Uygulaması

Görüntü işleme dünyasında gürültüyü gidermek ve görüntü kalitesini artırmak çok önemli görevlerdir. Aspose.Imaging for Java, görüntülerle çalışmak için çeşitli araçlar ve filtreler sağlayan güçlü bir kütüphanedir. Bu eğitimde, bir görüntüyü temizlemek ve gürültüyü gidermek amacıyla Medyan ve Wiener filtrelerini uygulamak için kitaplığı kullanma sürecinde size yol göstereceğiz. Bu adım adım kılavuz, profesyonel düzeyde görüntü iyileştirme elde etmenize yardımcı olacaktır.

## Önkoşullar

Bu eğitime dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

1. Java Geliştirme Ortamı: Bilgisayarınızda çalışan bir Java geliştirme ortamının olduğundan emin olun.

2. Aspose.Imaging for Java: Aspose.Imaging for Java kütüphanesini şu adresten indirip yükleyin:[Burada](https://releases.aspose.com/imaging/java/).

3. Örnek Gürültülü Görüntü: Gürültüyü gidermek istediğiniz gürültülü bir görüntü hazırlayın. Bu eğitim için istediğiniz herhangi bir resmi kullanabilirsiniz.

## Paketleri İçe Aktar

Java projenizde Aspose.Imaging for Java ile çalışmak için gerekli paketleri içe aktararak başlayın:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.imagefilters.filteroptions.MedianFilterOptions;
```

## 1. Adım: Gürültülü Görüntüyü Yükleyin

İlk adım gürültülü görüntüyü Aspose.Imaging kullanarak yüklemektir. Gürültülü görüntü dosyanızın yolunu belirttiğinizden emin olun.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (Image image = Image.load(dataDir + "your-noisy-image.png"))
{
    // Görüntüyü RasterImage'a yayınlayın
    RasterImage rasterImage = (RasterImage) image;
```

## Adım 2: Medyan Filtresini Oluşturun ve Yapılandırın

 Şimdi bunun bir örneğini oluşturun`MedianFilterOptions` sınıfını seçin ve filtrenin boyutunu yapılandırın. Filtre boyutu, medyan filtre uygulanırken dikkate alınacak her pikselin etrafındaki alanı belirler. Daha büyük bir boyut gürültüyü azaltabilir ancak görüntüyü bulanıklaştırabilir.

```java
    // MedianFilterOptions sınıfının bir örneğini oluşturun ve boyutu ayarlayın.
    MedianFilterOptions options = new MedianFilterOptions(4);
```

## 3. Adım: Medyan Filtresini Uygulayın

Daha sonra, önceki adımda yapılandırdığınız seçenekleri kullanarak Medyan filtresini RasterImage nesnesine uygulayın. Bu, görüntüdeki gürültünün giderilmesine yardımcı olacaktır.

```java
    // RasterImage nesnesine Medyan filtresini uygulayın.
    rasterImage.filter(image.getBounds(), options);
```

## Adım 4: Ortaya Çıkan Görüntüyü Kaydedin

Medyan filtresini uyguladıktan sonra gürültüsü giderilen görüntüyü istediğiniz konuma kaydedin.

```java
    // Ortaya çıkan görüntüyü kaydedin
    image.save("Your Document Directory" + "denoised-image.png");
}
```

Tebrikler! Aspose.Imaging for Java ile Medyan filtresini kullanarak bir görüntünün gürültüsünü başarıyla giderdiniz.

## Çözüm

Bu eğitimde, Aspose.Imaging for Java'nın bir görüntünün gürültüsünü gidermek için Medyan filtresini nasıl uygulayacağımızı araştırdık. Bu kitaplık, çok çeşitli filtreler ve araçlar sunarak onu görüntü işleme görevleri için değerli bir kaynak haline getirir. Bu kılavuzda özetlenen adımları izleyerek görüntü kalitesini artırabilir ve gürültüyü etkili bir şekilde giderebilirsiniz.

## SSS'ler

### S1: Aspose.Imaging for Java nedir?

Cevap1: Aspose.Imaging for Java, geliştiricilerin görüntülerle çalışmasına ve çeşitli görüntü işleme görevlerini programlı olarak gerçekleştirmesine olanak tanıyan bir Java kitaplığıdır.

### S2: Aspose.Imaging for Java'yı ücretsiz kullanabilir miyim?

 Cevap2: Aspose.Imaging for Java ticari bir kütüphanedir, ancak ücretsiz deneme sürümünü şu adresten edinebilirsiniz:[Burada](https://releases.aspose.com/) Ancak uzun süreli kullanım için adresinden bir lisans satın almanız gerekecektir.[Burada](https://purchase.aspose.com/buy).

### S3: Aspose.Imaging for Java desteğini nasıl alabilirim?

 Cevap3: Aspose.Imaging topluluğundan ve uzmanlardan yardım ve yardım isteyebilirsiniz.[Aspose.Görüntüleme Forumu](https://forum.aspose.com/).

### S4: Diğer görüntü iyileştirme teknikleri nelerdir?

Cevap4: Medyan filtresine ek olarak, görüntü iyileştirme teknikleri Wiener filtrelemeyi, Gauss bulanıklaştırmayı ve kontrast genişletmeyi ve diğerlerini içerir.

### S5: Aspose.Imaging for Java'yı web uygulamamda kullanabilir miyim?

Cevap5: Evet, Aspose.Imaging for Java'yı sunucu tarafı görüntü işleme için web uygulamalarınıza entegre edebilirsiniz.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
