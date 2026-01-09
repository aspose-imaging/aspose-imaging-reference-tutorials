---
date: 2026-01-09
description: Aspose.Imaging for Java ile görüntülere filigran eklemeyi öğrenin. Bu
  Java görüntü işleme öğreticisi, adım adım hızlı bir şekilde diyagonal bir filigran
  oluşturmayı gösterir.
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: Filigran Nasıl Eklenir – Çapraz Görüntü Filigranı (Java)
url: /tr/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Su İşareti Ekleme – Çapraz Görüntü Su İşareti (Java)

Eğer resimlerinize şık bir çapraz yönlendirme ile **how to add watermark** eklemek istiyorsanız, Aspose.Imaging for Java bunu zahmetsiz hale getirir. Bu adım‑adım öğreticide, bir JPG (veya desteklenen herhangi bir) görüntüye 45‑derece döndürülmüş metin su işareti eklemeyi göstereceğiz. Java sihirbazı olmanıza gerek yok – her blok sade bir dille açıklanmıştır, böylece sonucu dakikalar içinde yeniden oluşturabilirsiniz.

## Hızlı Cevaplar
- **Hangi kütüphane kullanılıyor?** Aspose.Imaging for Java  
- **Hangi birincil anahtar kelime kapsanıyor?** how to add watermark  
- **Desteklenen görüntü formatları?** JPEG, PNG, BMP, TIFF, GIF and more  
- **Ne kadar kod gerekiyor?** Only seven concise code blocks  
- **Test için lisansa ihtiyacım var mı?** A free trial is available; a license is required for production  

## “how to add watermark” görüntü işleme'de nedir?

Su işareti eklemek, bir görüntünün üzerine yarı‑saydam metin veya grafik yerleştirerek mülkiyeti korumak veya marka mesajı iletmek anlamına gelir. Çapraz bir su işareti özellikle etkilidir çünkü tüm resmi kaplar ve kırpılması daha zordur.

## Neden Aspose.Imaging for Java kullanmalı?

Aspose.Imaging, düşük seviyeli piksel manipülasyonunu soyutlayan yüksek seviyeli bir API sağlar, onlarca formatı destekler ve herhangi bir Java çalışma zamanında çalışır. Size, çapraz bir su işareti eklemek gibi *ne* yapmak istediğinize odaklanmanızı sağlar, görüntü formatı incelikleriyle uğraşmadan.

## Önkoşullar

İlerlemeye başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Aspose.Imaging for Java** – resmi siteden en son sürümü **[here](https://releases.aspose.com/imaging/java/)** adresinden indirin.  
2. **Java Development Environment** – JDK 8+ ve favori IDE'niz (IntelliJ, Eclipse, VS Code, vb.).  
3. **An image to watermark** – kodda referans göstereceğiniz bir klasöre örnek bir JPG/TIFF/PNG yerleştirin.

## Paketleri İçe Aktarma

İlk olarak, ihtiyacınız olan sınıfları içe aktarın. İçe aktarmaları bir arada tutmak kodun okunmasını ve bakımını kolaylaştırır.

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Adım 1: Mevcut Bir Görüntüyü Yükleme

Kaynak resmi yükleyerek başlıyoruz. `Image.load` yöntemi formatı otomatik olarak algılar.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **Pro tip:** `Image` nesnesini (gösterildiği gibi) bir try‑with‑resources bloğuna sarın, böylece otomatik olarak serbest bırakılır ve bellek sızıntıları önlenir.

## Adım 2: Su İşareti Metni ve Grafiklerini Hazırlama

Yüklenen görüntüye bağlı bir `Graphics` nesnesi oluşturun ve daha sonraki hesaplamalar için görüntü boyutunu saklayın.

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## Adım 3: Yazı Tipi ve Fırçayı Tanımlama

Öne çıkan bir yazı tipi ve su işaretinin rengini ve opaklığını belirleyen bir fırça seçin. Opaklığı ayarlayarak su işaretini yarı‑saydam hâle getirin.

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Adım 4: Metninizi Biçimlendirme

Metin çizildiğinde ortalanması için hizalama ve biçimlendirme bayraklarını ayarlayın.

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Adım 5: Dönüşümü Uygulama

Bir dönüşüm matrisi, orijini görüntünün merkezine taşımamıza ve ardından metni ‑45° (saat yönünde) döndürmemize olanak tanır.

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## Adım 6: Çiz ve Kaydet

Son olarak, dizeyi görüntü üzerine işleyin ve sonucu diske yazın.

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

`AddDiagonalWatermarkToImage_out.jpg` dosyasını açtığınızda, kırmızı, yarı‑saydam metnin resmin ortasından çapraz olarak geçtiğini göreceksiniz.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|-------|
| Watermark appears too faint | Opacity set to 0 (fully transparent) | Increase opacity, e.g., `brush.setOpacity(0.5f);` |
| Text is clipped at edges | Translation not centered for non‑square images | Use `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` as shown, then adjust rotation angle if needed |
| Unsupported image format error | Using an older Aspose.Imaging version | Update to the latest Aspose.Imaging release |

## Sıkça Sorulan Sorular

### Q1: Aspose.Imaging for Java yeni başlayanlar için uygun mu?

**A:** Kesinlikle! API sezgiseldir ve dokümantasyon net örnekler sunar. Görüntü işleme konusunda yeni olan geliştiriciler bile bu öğreticiyi izleyerek hızlıca profesyonel sonuçlar elde edebilir.

### Q2: Su işareti metnini ve stilini özelleştirebilir miyim?

**A:** Evet. `theString` değişkenini değiştirin, farklı bir `Font` seçin, `brush.setColor(...)` değerini değiştirin veya matris içindeki dönüş açıını markanıza uygun şekilde ayarlayın.

### Q3: Aspose.Imaging for Java JPG dışındaki diğer görüntü formatlarını destekliyor mu?

**A:** Evet. Kütüphane BMP, PNG, GIF, TIFF, PSD ve daha birçok formatı destekler. Tek yapmanız gereken `Image.load` yöntemine uygun dosyayı göstermek.

### Q4: Aspose.Imaging for Java için ücretsiz deneme mevcut mu?

**A:** Evet, Aspose.Imaging for Java'ı ücretsiz deneme ile deneyebilirsiniz. **[buradan](https://releases.aspose.com/)** edinin.

### Q5: Aspose.Imaging for Java için yardım veya destek nereden bulabilirim?

**A:** Sorular, hata raporları veya en iyi uygulama tavsiyeleri için Aspose.Imaging for Java destek forumunu **[burada](https://forum.aspose.com/)** ziyaret edin.

---

**Son Güncelleme:** 2026-01-09  
**Test Edilen:** Aspose.Imaging for Java 24.11 (latest at time of writing)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}