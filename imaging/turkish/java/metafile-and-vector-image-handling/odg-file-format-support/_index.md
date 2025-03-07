---
title: Aspose.Imaging for Java ile ODG'yi PNG ve PDF'ye dönüştürün
linktitle: ODG Dosya Formatı Desteği
second_title: Aspose.Imaging Java Görüntü İşleme API'si
description: Aspose.Imaging for Java ile ODG dosyalarını PNG ve PDF'ye nasıl dönüştüreceğinizi öğrenin. Verimli dönüşüm için adım adım kılavuzumuzu izleyin.
weight: 12
url: /tr/java/metafile-and-vector-image-handling/odg-file-format-support/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java ile ODG'yi PNG ve PDF'ye dönüştürün

Belge dönüştürme dünyasında Aspose.Imaging for Java, ODG (OpenDocument Graphics) dosyalarını kolayca PNG ve PDF formatlarına dönüştürmenize olanak tanıyan güçlü bir araç olarak öne çıkıyor. Bu eğitim, Aspose.Imaging for Java'yı kullanarak süreç boyunca size adım adım rehberlik edecektir. İster bir geliştirici olun ister yalnızca ODG dosyalarını dönüştürmek isteyen biri olun, bu makale hedefinize ulaşmanıza yardımcı olacaktır.

## Önkoşullar

Dönüşüm sürecine dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olmanız gerekir:

### 1. Java Geliştirme Ortamı

 Sisteminizde bir Java geliştirme ortamının kurulu olduğundan emin olun. En son Java Geliştirme Kitini (JDK) aşağıdaki adresten indirip yükleyebilirsiniz:[Oracle web sitesi](https://www.oracle.com/java/technologies/javase-downloads).

### 2. Java için Aspose.Imaging

 Aspose.Imaging for Java'yı indirip yüklemeniz gerekecek. En son sürümü şurada bulabilirsiniz:[Aspose.Imaging for Java indirme sayfası](https://releases.aspose.com/imaging/java/).

### 3. ODG Dosyaları

Elbette dönüştürmek istediğiniz ODG dosyalarına ihtiyacınız olacak. Bu dosyaların sisteminizdeki bir dizinde bulunduğundan emin olun.

## Paketleri İçe Aktar

Artık önkoşulları yerine getirdiğinize göre, gerekli paketleri Java projenize aktarmaya başlayalım. Bu paketler Aspose.Imaging for Java ile etkili bir şekilde çalışmanıza olanak tanır.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.SizeF;
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
```

Takip etmeyi kolaylaştırmak için şimdi dönüşüm sürecini basit adımlara ayıracağız. Her adım için bir başlık ve açıklama sunacağız.

## 1. Adım: Veri Dizininizi Tanımlayın

 ODG dosyalarınızın bulunduğu dizini belirterek başlayın. Değiştirmeniz gerekecek`"Your Document Directory"` Dizininizin gerçek yolu ile.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

## Adım 2: ODG Dosyalarını Belirleyin

Dönüştürmek istediğiniz ODG dosya adlarından oluşan bir dizi oluşturun. Örnek dosya adlarını ODG dosyalarınızın adlarıyla değiştirin.

```java
String[] files = new String[] {"example.odg", "example1.odg"};
```

## 3. Adım: Rasterleştirme Seçeneklerini Yapılandırın

ODG dosyaları için rasterleştirme seçeneklerini ayarlayın. Bu seçenekler sayfa boyutunu ve vektör rasterleştirme ayarlarını belirleyecektir.

```java
final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
```

## Adım 4: ODG Dosyalarında Döngü Yapın

Şimdi her ODG dosyasını yineleyin, yükleyin ve hem PNG hem de PDF formatlarına dönüştürün.

```java
for (String file : files) {
    String fileName = dataDir + file;
    try (Image image = Image.load(fileName)) {
        rasterizationOptions.setPageSize(new SizeF(image.getWidth(), image.getHeight()));

        // PNG'ye dönüştür
        String outFileName = "Your Document Directory" + file.replace(".odg", ".png");
        image.save(outFileName, new PngOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});

        // PDF'ye dönüştür
        outFileName = "Your Document Directory" + file.replace(".odg", ".pdf");
        image.save(outFileName, new PdfOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});
    }
}
```

Tebrikler! Aspose.Imaging for Java'yı kullanarak ODG dosyalarınızı başarıyla hem PNG hem de PDF formatlarına dönüştürdünüz.

## Çözüm

Aspose.Imaging for Java, ODG dosyalarını PNG ve PDF gibi daha yaygın olarak desteklenen görüntü formatlarına dönüştürme işlemini basitleştirir. Bu eğitimde özetlenen adımları izleyerek bu dönüşümleri Java projelerinizde verimli bir şekilde gerçekleştirebilirsiniz.

## SSS'ler

### S1: Aspose.Imaging for Java ücretsiz bir araç mıdır?

 C1: Hayır, Aspose.Imaging for Java ticari bir kütüphanedir ve fiyatlandırma bilgilerini burada bulabilirsiniz.[satın alma sayfası](https://purchase.aspose.com/buy).

### S2: Satın almadan önce Aspose.Imaging for Java'yı deneyebilir miyim?

 C2: Evet, ücretsiz deneme sürümünü şuradan indirebilirsiniz:[Burada](https://releases.aspose.com/).

### S3: Aspose.Imaging for Java desteğini nasıl alabilirim?

 A3: Yardım isteyebilir ve sorular sorabilirsiniz.[Aspose.Görüntüleme forumu](https://forum.aspose.com/).

### S4: Aspose.Imaging for Java başka hangi dosya formatlarını kullanabilir?

 Cevap4: Aspose.Imaging for Java, BMP, JPEG, TIFF, PDF ve daha fazlası dahil olmak üzere çok çeşitli görüntü ve belge formatlarını destekler. Bakın[dokümantasyon](https://reference.aspose.com/imaging/java/) kapsamlı bir liste için.

### S5: Aspose.Imaging for Java'yı ticari projelerimde kullanabilir miyim?

Cevap5: Evet, uygun lisansı satın aldıktan sonra Aspose.Imaging for Java'yı ticari projelerde kullanabilirsiniz.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
