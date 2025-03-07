---
title: Aspose.Imaging for Java ile Görüntü Düzeltme Filtresi Uygulaması
linktitle: Görüntü Düzeltme Filtresi Uygulaması
second_title: Aspose.Imaging Java Görüntü İşleme API'si
description: Aspose.Imaging for Java ile görsellerinizi geliştirin. Düzeltme filtreleri uygulamak ve görüntü kalitesini optimize etmek için adım adım kılavuz.
weight: 16
url: /tr/java/image-processing-and-enhancement/image-correction-filter-application/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java ile Görüntü Düzeltme Filtresi Uygulaması

Dijital görüntü alanında, görüntü düzeltme ve iyileştirme ihtiyacı her zaman mevcuttur. İster profesyonel bir fotoğrafçı, ister grafik tasarımcı, ister fotoğraflarında ince ayar yapmaktan hoşlanan biri olun, doğru araçların elinizin altında olması çok önemlidir. Aspose.Imaging for Java, tam da bunu başarmanıza yardımcı olabilecek güçlü bir kütüphanedir. Bu adım adım kılavuzda, resimlerinize görüntü düzeltme filtreleri uygulamak için Aspose.Imaging for Java'yı kullanma sürecinde size yol göstereceğiz.

## Önkoşullar

Aspose.Imaging for Java'yı kullanarak görüntü düzeltme dünyasına dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olmanız gerekir:

1.  Java Geliştirme Ortamı: Sisteminizde Java'nın kurulu olduğundan emin olun. Şuradan indirebilirsiniz[Oracle'ın web sitesi](https://www.oracle.com/java/technologies/javase-downloads).

2.  Aspose.Imaging for Java: Aspose.Imaging for Java kütüphanesini edinmeniz gerekecektir. adresinden indirebilirsiniz.[İnternet sitesi](https://releases.aspose.com/imaging/java/).

3. İmaj Dosyalarınız: Düzeltme filtreleri uygulamak istediğiniz imaj dosyalarını hazırlayın ve bir dizine yerleştirin.

Artık gerekli araç ve kaynaklara sahip olduğunuza göre adım adım kılavuza başlayalım.

## Paketleri İçe Aktar

Bu bölümde Aspose.Imaging for Java'yı etkili bir şekilde kullanmak için gerekli paketleri içe aktararak başlayacağız.

### Adım 1: Aspose.Imaging Kütüphanesini İçe Aktarın

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.imagefilters.filteroptions.BilateralSmoothingFilterOptions;
import com.aspose.imaging.imagefilters.filteroptions.SharpenFilterOptions;
import com.aspose.imaging.Rectangle;
```

Görüntü düzeltme amacıyla Aspose.Imaging'i kullanmak için bu paketleri Java sınıfınızın başına eklediğinizden emin olun.

Şimdi görüntü düzeltme filtrelerini uygulama sürecini bir dizi yönetilebilir adıma ayıralım.

## 1. Adım: Görüntüyü Yükleyin

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "aspose-logo.jpg"))
{
    // Resim yükleme kodunuz buraya gelecek
}
```

 İlk adım, düzeltmek istediğiniz görüntüyü yüklemektir. Yer değiştirmek`"Your Document Directory"` resim dizininizin gerçek yolunu belirtin ve üzerinde çalışmak istediğiniz resim dosyasını belirtin.

## 2. Adım: Resim Sınırlarını Alın

```java
com.aspose.imaging.Rectangle rect = rasterImage.getBounds();
```

Bu adım, yüklenen görüntünün sınırlarının (dikdörtgen) alınmasını içerir. Bu bilgiler daha sonraki işlemler için kullanılacaktır.

## 3. Adım: Düzeltme Filtrelerini Tanımlayın

```java
com.aspose.imaging.imagefilters.filteroptions.BilateralSmoothingFilterOptions bilateralOptions =
        new com.aspose.imaging.imagefilters.filteroptions.BilateralSmoothingFilterOptions(3);

com.aspose.imaging.imagefilters.filteroptions.SharpenFilterOptions sharpenOptions =
        new com.aspose.imaging.imagefilters.filteroptions.SharpenFilterOptions();
```

Burada ikili yumuşatma ve keskinleştirme için filtre seçeneklerinin örneklerini oluşturuyoruz. Bu filtreler görüntüye uygulanacaktır.

## 4. Adım: Filtreleri Uygulayın

```java
rasterImage.filter(rect, bilateralOptions);
rasterImage.filter(rect, sharpenOptions);
```

Tanımlanan filtreleri belirtilen dikdörtgen içindeki görüntüye uygulayın.

## Adım 5: Kontrastı Ayarlayın

```java
rasterImage.adjustContrast(-10);
```

Bu adımda görüntünün kontrastını ayarlıyoruz. İstenilen etkiyi elde etmek için farklı değerlerle denemeler yapabilirsiniz.

## Adım 6: Binarize Bradley'i Kullanarak Parlaklığı Ayarlayın

```java
rasterImage.binarizeBradley(80);
```

Burada Binarize Bradley filtresini kullanarak görüntünün parlaklığını ayarlıyoruz.

## Adım 7: Düzeltilen Görüntüyü Kaydedin

```java
rasterImage.save("Your Document Directory" + "a1_out.jpg");
```

Son olarak, düzeltilmiş görüntüyü belirttiğiniz çıktı dizinine kaydedin.

## Çözüm

Aspose.Imaging for Java, görüntü düzeltme ve geliştirme için güçlü bir araç seti sağlar. Bu adım adım kılavuzda, bir görüntüyü yüklemek, düzeltme filtreleri uygulamak, kontrastı ayarlamak ve nihai sonucu kaydetmek için temel adımları ele aldık. Bu adımları izleyerek ve farklı parametrelerle denemeler yaparak görsellerinizi geliştirmede etkileyici sonuçlar elde edebilirsiniz.

## Sıkça Sorulan Sorular

### S1: Aspose.Imaging for Java'yı ticari projelerde kullanabilir miyim?

 Cevap1: Evet, Aspose.Imaging for Java ticari kullanıma açıktır. adresinden lisans alabilirsiniz.[İnternet sitesi](https://purchase.aspose.com/buy).

### S2: Aspose.Imaging for Java'nın ücretsiz deneme sürümü mevcut mu?

 C2: Evet, ücretsiz deneme sürümünü şuradan indirebilirsiniz:[Burada](https://releases.aspose.com/).

### S3: Aspose.Imaging for Java için ek belgeleri ve desteği nerede bulabilirim?

 A3: Şu adresteki belgelere başvurabilirsiniz:[Aspose.Imaging for Java Dokümantasyonu](https://reference.aspose.com/imaging/java/) ve bu konuda destek isteyin[Aspose.Görüntüleme forumu](https://forum.aspose.com/).

### S4: Aspose.Imaging for Java'da görüntü düzeltmenin yaygın kullanım durumları nelerdir?

Cevap4: Görüntü düzeltme, fotoğrafçılıkta, grafik tasarımda ve tıbbi görüntülemede çeşitli amaçlarla görüntülerin kalitesini artırmak ve iyileştirmek için sıklıkla kullanılır.

### S5: Aspose.Imaging for Java'yı diğer Java kütüphaneleri veya çerçeveleriyle kullanabilir miyim?

Cevap5: Evet, Aspose.Imaging for Java, işlevselliğini ve yeteneklerini genişletmek için diğer Java kitaplıkları ve çerçeveleriyle entegre edilebilir.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
