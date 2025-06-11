---
"description": "ODG dosyalarını Aspose.Imaging for Java ile PNG ve PDF'ye nasıl dönüştüreceğinizi öğrenin. Verimli dönüşüm için adım adım kılavuzumuzu izleyin."
"linktitle": "ODG Dosya Biçimi Desteği"
"second_title": "Aspose.Imaging Java Görüntü İşleme API'si"
"title": "ODG'yi Aspose.Imaging for Java ile PNG ve PDF'ye dönüştürün"
"url": "/tr/java/metafile-and-vector-image-handling/odg-file-format-support/"
"weight": 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# ODG'yi Aspose.Imaging for Java ile PNG ve PDF'ye dönüştürün

Belge dönüştürme dünyasında, Aspose.Imaging for Java, ODG (OpenDocument Graphics) dosyalarını PNG ve PDF formatlarına kolayca dönüştürmenize olanak tanıyan güçlü bir araç olarak öne çıkıyor. Bu eğitim, Aspose.Imaging for Java'yı kullanarak sizi adım adım süreç boyunca yönlendirecektir. İster bir geliştirici olun, ister sadece ODG dosyalarını dönüştürmek isteyen biri olun, bu makale hedefinize ulaşmanıza yardımcı olacaktır.

## Ön koşullar

Dönüştürme sürecine başlamadan önce, aşağıdaki ön koşulların mevcut olduğundan emin olmanız gerekir:

### 1. Java Geliştirme Ortamı

Sisteminizde bir Java geliştirme ortamının kurulu olduğundan emin olun. En son Java Geliştirme Kitini (JDK) şu adresten indirip yükleyebilirsiniz: [Oracle web sitesi](https://www.oracle.com/java/technologies/javase-downloads).

### 2. Java için Aspose.Görüntüleme

Java için Aspose.Imaging'i indirip yüklemeniz gerekecek. En son sürümü şu adreste bulabilirsiniz: [Aspose.Imaging for Java indirme sayfası](https://releases.aspose.com/imaging/java/).

### 3. ODG Dosyaları

Elbette, dönüştürmek istediğiniz ODG dosyalarına ihtiyacınız olacak. Bu dosyaların sisteminizdeki bir dizinde mevcut olduğundan emin olun.

## Paketleri İçe Aktar

Artık önkoşulları yerine getirdiğinize göre, Java projenize gerekli paketleri içe aktarmaya başlayalım. Bu paketler, Java için Aspose.Imaging ile etkili bir şekilde çalışmanıza olanak tanır.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.SizeF;
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
```

Şimdi dönüşüm sürecini takip etmeyi kolaylaştırmak için basit adımlara ayıracağız. Her adım için bir başlık ve açıklama sağlayacağız.

## Adım 1: Veri Dizininizi Tanımlayın

ODG dosyalarınızın bulunduğu dizini belirterek başlayın. Şunu değiştirmeniz gerekecek: `"Your Document Directory"` dizininize giden gerçek yol ile.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

## Adım 2: ODG Dosyalarını Belirleyin

Dönüştürmek istediğiniz ODG dosya adlarının bir dizisini oluşturun. Örnek dosya adlarını ODG dosyalarınızın adlarıyla değiştirin.

```java
String[] files = new String[] {"example.odg", "example1.odg"};
```

## Adım 3: Rasterleştirme Seçeneklerini Yapılandırın

ODG dosyaları için rasterleştirme seçeneklerini ayarlayın. Bu seçenekler sayfa boyutunu ve vektör rasterleştirme ayarlarını belirleyecektir.

```java
final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
```

## Adım 4: ODG Dosyalarında Döngü

Şimdi her ODG dosyasını tarayın, yükleyin ve hem PNG hem de PDF formatlarına dönüştürün.

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

Tebrikler! Aspose.Imaging for Java'yı kullanarak ODG dosyalarınızı hem PNG hem de PDF formatlarına başarıyla dönüştürdünüz.

## Çözüm

Java için Aspose.Imaging, ODG dosyalarını PNG ve PDF gibi daha yaygın olarak desteklenen görüntü biçimlerine dönüştürme sürecini basitleştirir. Bu eğitimde özetlenen adımları izleyerek, bu dönüştürmeleri Java projelerinizde verimli bir şekilde gerçekleştirebilirsiniz.

## SSS

### S1: Aspose.Imaging for Java ücretsiz bir araç mıdır?

C1: Hayır, Aspose.Imaging for Java ticari bir kütüphanedir ve fiyatlandırma bilgilerini şu adreste bulabilirsiniz: [satın alma sayfası](https://purchase.aspose.com/buy).

### S2: Satın almadan önce Aspose.Imaging for Java'yı deneyebilir miyim?

A2: Evet, ücretsiz deneme sürümünü şu adresten indirebilirsiniz: [Burada](https://releases.aspose.com/).

### S3: Java için Aspose.Imaging desteğini nasıl alabilirim?

A3: Yardım arayabilir ve soru sorabilirsiniz. [Aspose.Görüntüleme forumu](https://forum.aspose.com/).

### S4: Aspose.Imaging for Java başka hangi dosya biçimlerini işleyebilir?

A4: Aspose.Imaging for Java, BMP, JPEG, TIFF, PDF ve daha fazlası dahil olmak üzere çok çeşitli görüntü ve belge formatlarını destekler. [belgeleme](https://reference.aspose.com/imaging/java/) Kapsamlı bir liste için.

### S5: Aspose.Imaging for Java'yı ticari projelerimde kullanabilir miyim?

C5: Evet, uygun lisansı satın aldıktan sonra Aspose.Imaging for Java'yı ticari projelerinizde kullanabilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}