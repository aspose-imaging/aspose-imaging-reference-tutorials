---
date: 2026-01-17
description: Aspose.Imaging for Java kullanarak görüntülerin parlaklığını nasıl ayarlayacağınızı
  öğrenin. Bu Java görüntü işleme öğreticisi, zahmetsiz Java görüntü iyileştirmesini
  gösterir.
linktitle: Image Brightness Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java ile Görüntülerin Parlaklığını Nasıl Ayarlarsınız
url: /tr/java/image-processing-and-enhancement/image-brightness-adjustment/
weight: 25
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Görüntülerin Parlaklığını Aspose.Imaging for Java ile Nasıl Ayarlarsınız

## Giriş

Parlaklık ayarlama, **java image processing** içinde en yaygın görevlerden biridir. Tıbbi taramaları hazırlıyor, ürün fotoğraflarını cilalıyor ya da kişisel resimleri iyileştiriyor olun, **parlaklığı nasıl ayarlayacağınızı** hızlı ve güvenilir bir şekilde bilmek saatler süren manuel çalışmayı tasarruf ettirebilir. Bu öğreticide, Aspose.Imaging for Java kullanarak **parlaklığı nasıl ayarlayacağınızı** gösteren tam, üretim‑hazır bir örnek üzerinden adım adım ilerleyeceğiz; bu güçlü kütüphane kutudan çıkar çıkmaz onlarca formatı destekler.

## Hızlı Yanıtlar
- **“parlaklık ayarlama” ne anlama gelir?** Görüntünün her pikselinin genel ışıklılığını değiştirir.  
- **Hangi kütüphane kullanılıyor?** Aspose.Imaging for Java.  
- **Lisans gerekli mi?** Geliştirme için ücretsiz deneme sürümü yeterlidir; üretim için ticari lisans gerekir.  
- **Desteklenen formatlar?** BMP, JPEG, PNG, DICOM, TIFF ve daha fazlası.  
- **Tipik uygulama süresi?** Temel bir betik için yaklaşık 10 dakika.

## Java görüntü işleme içinde “parlaklığı nasıl ayarlayacağınız” nedir?

Parlaklık ayarlama, piksel yoğunluk değerlerine uniform bir offset uygulamaktır. Aspose.Imaging’de bu, `adjustBrightness(int value)` metodu ile sunulur; pozitif değerler görüntüyü aydınlatır, negatif değerler karartır.

## Neden Aspose.Imaging for Java görüntü iyileştirme için tercih edilmeli?

- **Geniş format desteği** – DICOM, BMP, JPEG, PNG, TIFF vb. ekstra codec gerektirmeden işler.  
- **Basit API** – Parlaklık, kontrast ve gama gibi yaygın ayarlamalar tek satırda yapılır.  
- **Performans‑optimizasyonu** – Büyük tıbbi görüntüler ve yüksek çözünürlüklü fotoğraflarda verimli çalışır.  
- **Çapraz platform** – Herhangi bir JVM üzerinde çalışır, sunucu‑tarafı iş akışları için idealdir.

## Önkoşullar

Koda geçmeden önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Geliştirme Ortamı** – En yeni JDK’yı [web sitesinden](https://www.oracle.com/java/technologies/javase-downloads) indirin.  
2. **Aspose.Imaging for Java** – Kurulum kılavuzunu Aspose.Imaging web sitesindeki [Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/) adresinden izleyin.  
3. **Örnek Görüntü** – Parlaklaştırmak istediğiniz bir DICOM dosyası (`image.dcm`) veya başka bir desteklenen format.  
4. **IDE** – Eclipse, IntelliJ IDEA veya tercih ettiğiniz herhangi bir Java IDE.

Bu önkoşullar hazır olduğunda, kodlamaya başlayalım.

## Paketleri İçe Aktar

İlk olarak, gerekli Aspose.Imaging sınıflarını içe aktarın:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import com.aspose.imaging.imageoptions.BmpOptions;
```

## Adım‑Adım Kılavuz

### Adım 1: Dosya Yollarını Tanımla

Girdi ve çıktı konumlarını ayarlayın. `"Your Document Directory"` ifadesini makinenizdeki gerçek klasörle değiştirin.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingBrightness_out.bmp";
```

### Adım 2: DICOM Görüntüyü Yükle

`Image.load` metodunu kullanarak DICOM dosyasını belleğe okuyun.

```java
try (DicomImage image = (DicomImage) Image.load(inputFile)) {
    // Image is now ready for processing.
}
```

### Adım 3: Parlaklığı Ayarla

`try` bloğu içinde `adjustBrightness` metodunu çağırın. `50` değeri resmi belirgin şekilde aydınlatır; karartmak için negatif sayılar kullanın.

```java
image.adjustBrightness(50);
```

> **İpucu:** İnce ayarlamalar için `-20` ile `20` arasında değerlerle başlayın. Farklı seviyeleri test ederek vurguların ya da gölgelerin kırpılmasını önleyin.

### Adım 4: Sonuç Görüntüyü Kaydet

Değiştirilen görüntüyü BMP seçenekleriyle diske yazın (gerektiğinde başka formatları da seçebilirsiniz).

```java
image.save(outputFile, new BmpOptions());
```

Program tamamlandığında, `AdjustingBrightness_out.bmp` orijinal DICOM görüntünüzün parlaklaştırılmış sürümünü içerecektir.

## Yaygın Sorunlar & Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|------|
| **Çıktı dosyası oluşturulmadı** | Yanlış yol veya yazma izni eksikliği | `outputFile` yolunu doğrulayın ve klasörün var olduğundan ve yazılabilir olduğundan emin olun. |
| **Görüntü soluk görünüyor** | Parlaklık değeri çok yüksek | Ayarlama değerini azaltın veya parlaklaştırdıktan sonra kontrast düzeltmesi uygulayın. |
| **Desteklenmeyen format hatası** | DICOM yükleyicisi tarafından işlenemeyen bir format yüklenmeye çalışıldı | DICOM dışı dosyalar için uygun görüntü sınıfını (ör. `BmpImage`) kullanın. |

## Sık Sorulan Sorular

### S1: Aspose.Imaging for Java profesyonel görüntü işleme görevleri için uygun mu?

A1: Evet, Aspose.Imaging for Java, geniş özellik ve seçenek yelpazesi sunan profesyonel görüntü işleme için çok yönlü bir kütüphanedir.

### S2: Aspose.Imaging for Java’yı diğer Java kütüphaneleriyle birlikte kullanabilir miyim?

A2: Kesinlikle! Aspose.Imaging for Java, diğer Java kütüphaneleri ve çerçeveleriyle sorunsuz bir şekilde entegre edilebilir.

### S3: Aspose.Imaging for Java hangi görüntü formatlarını destekyor?

A3: Aspose.Imaging for Java, BMP, JPEG, PNG, TIFF, GIF ve daha fazlası dahil olmak üzere geniş bir görüntü formatı yelpazesini destekler.

### S4: Aspose.Imaging for Java için ücretsiz bir deneme sürümü var mı?

A4: Evet, Aspose.Imaging for Java’yı ücretsiz deneme sürümüyle deneyebilirsiniz. Başlamak için [buraya](https://releases.aspose.com/) tıklayın.

### S5: Aspose.Imaging for Java ile ilgili destek veya yardım nereden alabilirim?

A5: Yardım alabilir ve topluluğa katılabilirsiniz: [Aspose.Imaging for Java forumu](https://forum.aspose.com/).

## Sonuç

Bu **java image processing tutorial**’da Aspose.Imaging for Java kullanarak **parlaklığı nasıl ayarlayacağınızı** gösterdik. Paketi içe aktarma, yolları tanımlama, görüntüyü yükleme, parlaklığı ayarlama ve kaydetme adımlarını izleyerek, tıbbi görüntüleme hatlarından e‑ticaret fotoğraf akışlarına kadar herhangi bir uygulamaya sağlam **java image enhancement** entegrasyonu sağlayabilirsiniz. Farklı parlaklık değerleriyle deney yapın, kontrast ya da gama ayarlarıyla birleştirin ve görsel verinizin tam potansiyelini ortaya çıkarın.

---

**Son Güncelleme:** 2026-01-17  
**Test Edilen Versiyon:** Aspose.Imaging for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}