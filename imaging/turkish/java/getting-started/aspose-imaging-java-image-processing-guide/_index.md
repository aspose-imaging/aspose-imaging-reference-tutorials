---
date: '2025-12-27'
description: Aspose.Imaging Java kullanarak görüntüyü nasıl döndüreceğinizi ve JPEG,
  PNG ve TIFF'i nasıl verimli bir şekilde dışa aktaracağınızı öğrenin. Görüntü işleme
  Java geliştiricileri için adım adım bir rehber.
keywords:
- Aspose.Imaging Java
- image processing Java
- exporting images Java
- rotate flip image Java
- Java image handling
title: 'Aspose.Imaging Java ile Görüntüyü Döndürme: Yükleme, İşleme ve Dışa Aktarma
  İçin Kapsamlı Rehber'
url: /tr/java/getting-started/aspose-imaging-java-image-processing-guide/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging Java'da Ustalaşmak: Görüntüyü Döndürme ve Verimli Şekilde Dışa Aktarma

## Giriş

Java uygulamasında **how to rotate image** yapmanız ve bellek kullanımını düşük tutmanız gerekiyorsa doğru yerdesiniz. Bu öğreticide, özel bir arabellekle görüntüleri yüklemeyi, döndürüp çevirme işlemlerini yapmayı ve ardından sonuçları JPEG, PNG veya TIFF olarak dışa aktarmayı adım adım inceleyeceğiz. Sonunda **image processing Java** projeleri için en iyi uygulamaları anlayacak ve bu teknikleri gerçek dünya çözümlerine entegre etmeye hazır olacaksınız.

**What You’ll Learn**
- **How to set buffer** boyutunu optimal yükleme performansı için nasıl ayarlayacağınızı.  
- **How to rotate image** ve çevirme dönüşümlerini nasıl uygulayacağınızı.  
- **How to export JPEG**, **how to export PNG** ve **png bit depth** kontrolünü nasıl yapacağınızı.  
- Bu tekniklerin parladığı pratik senaryolar.

Ön koşullarınızı doğrulayalım, ardından koda dalalım.

### Önkoşullar

Başlamadan önce şunların yüklü olduğundan emin olun:

1. **Java Development Kit (JDK)** – güncel, uyumlu bir sürüm.  
2. **Maven veya Gradle** – bağımlılık yönetimi için.  
3. **IDE** – IntelliJ IDEA, Eclipse veya herhangi bir Java‑dostu editör.  

### Aspose.Imaging for Java Kurulumu

Aspose.Imaging'i projenize aşağıdaki snippetlerden birini kullanarak ekleyin.

**Maven**

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle**

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

Ayrıca en son JAR dosyasını [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) adresinden indirebilirsiniz.

> **Pro tip:** Değerlendirme filigranlarından kaçınmak için ücretsiz deneme lisansını erken kaydedin. Kalıcı bir lisans, [purchase portal](https://purchase.aspose.com/buy) üzerinden temin edilebilir.

## Hızlı Yanıtlar
- **Görüntüyü nasıl döndürürüm?** `RasterImage.rotate(angle)` veya `rotateFlip(type)` kullanın.  
- **Arabellek nasıl ayarlanır?** `LoadOptions.setBufferSizeHint(int)` yapılandırın.  
- **JPEG nasıl dışa aktarılır?** Gri tonlu bir palet ile `JpegOptions` oluşturun.  
- **PNG nasıl dışa aktarılır?** `PngOptions` kullanın ve `PngColorType.Grayscale` ayarlayın.  
- **PNG dosya boyutunu ne etkiler?** **png bit depth** ayarı (8‑bit yaygındır).  

## Yükleme İçin Arabellek Boyutunu Nasıl Ayarlarsınız

Büyük dosyaların yüklenmesi belleği zorlayabilir. Aspose.Imaging, kaynak tüketimini daha ince kontrol etmenizi sağlayan bir arabellek boyutu ipucu sunar.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.LoadOptions;
import com.aspose.imaging.RasterImage;

String sourceImagePath = "YOUR_DOCUMENT_DIRECTORY/Png/00020.png";
LoadOptions loadOptions = new LoadOptions();
loadOptions.setBufferSizeHint(450); // how to set buffer size (in KB)

try (RasterImage image = (RasterImage) Image.load(sourceImagePath, loadOptions)) {
    if (!image.isCached()) {
        image.cacheData(); // cache for faster subsequent operations
    }
}
```

**Neden önemli:** İyi seçilmiş bir arabellek GC baskısını azaltır ve sonraki dönüşümleri hızlandırır.

## Görüntüyü Döndürme ve Çevirme Nasıl Yapılır

Şimdi görüntü yüklendiğine göre, yönünü değiştirebilirsiniz.

```java
import com.aspose.imaging.RasterImage;

float rotateAngle = 90; // how to rotate image: 90 degrees
Integer rotateFlipType = null; // set to a RotateFlipType enum if flipping is needed

try (RasterImage image = Image.load(sourceImagePath) as RasterImage) {
    if (!image.isCached()) {
        image.cacheData();
    }
    if (rotateAngle != 0) {
        image.rotate(rotateAngle); // rotate image
    }
    if (rotateFlipType != null) {
        image.rotateFlip(rotateFlipType); // optional flip
    }
}
```

**İpucu:** Tek bir çağrıda hem döndürme hem de çevirme gerekiyorsa `rotateFlip` kullanın—daha verimlidir.

## Gri Tonlu Optimizasyonla JPEG Nasıl Dışa Aktarılır

Web teslimatı için dosya boyutunu hafif tutarken JPEG dışa aktarmak sıkça gerekir.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.imaging.imageoptions.JpegOptions;
import com.aspose.imaging.sources.ColorPaletteHelper;

String outputJpegPath = "YOUR_OUTPUT_DIRECTORY/00020_jpeg.jpg";

try (RasterImage image = Image.load(sourceImagePath) as RasterImage) {
    if (!image.isCached()) {
        image.cacheData();
    }
    JpegOptions jpegOptions = new JpegOptions();
    int bitDepth = 8; // typical for JPEG
    if (bitDepth <= 8) {
        jpegOptions.setPalette(ColorPaletteHelper.create8BitGrayscale(true));
        jpegOptions.setColorType(JpegCompressionColorMode.Grayscale);
    }
    image.save(outputJpegPath, jpegOptions); // how to export jpeg
}
```

**Sonuç:** Dosya boyutu azaltılmış ancak görsel netliği korunan bir gri tonlu JPEG.

## Gri Tonlu ve Bit Derinliği Yapılandırmasıyla PNG Nasıl Dışa Aktarılır

Kayıpsız kalite gerektiğinde PNG tercih edilir. **png bit depth** kontrolü, boyut ve doğruluk dengesini ayarlamanızı sağlar.

```java
import com.aspose.imaging.fileformats.png.PngColorType;
import com.aspose.imaging.imageoptions.PngOptions;

String outputPngPath = "YOUR_OUTPUT_DIRECTORY/00020_png.png";

try (RasterImage image = Image.load(sourceImagePath) as RasterImage) {
    if (!image.isCached()) {
        image.cacheData();
    }
    PngOptions pngOptions = new PngOptions();
    int bitDepth = 8; // how to export png with 8‑bit grayscale
    if (bitDepth <= 8) {
        pngOptions.setColorType(PngColorType.Grayscale);
        pngOptions.setBitDepth((byte) bitDepth); // png bit depth
    }
    image.save(outputPngPath, pngOptions); // how to export png
}
```

**Not:** Bit derinliğini 8’in altına düşürmek boyutu daha da azaltır, ancak görsel kaliteye dikkat edin.

## Özel Sıkıştırma ve Fotometri ile TIFF Nasıl Dışa Aktarılır

TIFF, esnekliğin önemli olduğu arşivleme veya baskı iş akışları için idealdir.

```java
import com.aspose.imaging.fileformats.tiff.enums.TiffCompressions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.imaging.imageoptions.TiffOptions;

String outputTiffPath = "YOUR_OUTPUT_DIRECTORY/00020_tiff.tiff";

try (RasterImage image = Image.load(sourceImagePath) as RasterImage) {
    if (!image.isCached()) {
        image.cacheData();
    }
    TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
    int bitDepth = 1; // example: 1‑bit monochrome
    switch (bitDepth) {
        case 1:
            tiffOptions.setPhotometric(TiffPhotometrics.MinIsWhite);
            tiffOptions.setPalette(ColorPaletteHelper.createMonochrome());
            tiffOptions.setCompression(TiffCompressions.CcittFax4);
            tiffOptions.setBitsPerSample(new int[]{1});
            break;
        case 8:
            tiffOptions.setPhotometric(TiffPhotometrics.MinIsWhite);
            tiffOptions.setPalette(ColorPaletteHelper.create8BitGrayscale(true));
            tiffOptions.setCompression(TiffCompressions.Deflate);
            tiffOptions.setBitsPerSample(new int[]{8});
            break;
        default:
            int bitsPerSample = bitDepth / 3;
            tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
            tiffOptions.setCompression(TiffCompressions.Jpeg);
            tiffOptions.setBitsPerSample(new int[]{bitsPerSample, bitsPerSample, bitsPerSample});
            break;
    }
    image.save(outputTiffPath, tiffOptions); // export TIFF with custom settings
}
```

**Neden TIFF?** Çoklu sıkıştırma ve fotometrik yorumlamaları desteklemesi, yüksek kalite arşivleme için mükemmeldir.

## Pratik Uygulamalar

- **Web platformları:** Görüntüleri döndürerek ve optimize JPEG/PNG olarak dışa aktararak sayfa yükleme sürelerini azaltın.  
- **Dijital arşivler:** Orijinalleri kayıpsız sıkıştırmalı TIFF olarak koruyun.  
- **CMS boru hatları:** Toplu işleme otomasyonu—döndürme, çevirme ve dışa aktarma—tek bir iş akışında.  
- **Fotoğraf düzenleme araçları:** Kullanıcılara harici editörlere ihtiyaç duymadan hızlı yönlendirme düzeltmeleri sunun.  

## Performans Düşünceleri

- **Akıllıca önbellekle:** Aynı görüntü üzerinde birden fazla işlem yapacaksanız `image.cacheData()` çağırın.  
- **Doğru bit derinliğini seçin:** 8‑bit gri ton çoğu web görüntüsü için ideal; 1‑bit siyah‑beyaz taramalar için uygundur.  
- **Belleği izleyin:** Büyük toplular `LoadOptions` aracılığıyla uygun bir arabellek boyutu ayarlamaktan fayda sağlar.  

## Sonuç

**how to rotate image**, özel bir arabellek ayarlama ve JPEG, PNG, TIFF'yi optimal ayarlarla dışa aktarma konularını ele aldık. Bu desenleri uygulayarak performansı artırabilir ve herhangi bir Java tabanlı çözümde yüksek kalite görseller sunabilirsiniz.

Daha derin keşif için resmi kılavuza bakın: [Aspose.Imaging documentation](https://docs.aspose.com/imaging/java/).

## Sıkça Sorulan Sorular

**S: Aspose.Imaging for Java nasıl kurulur?**  
C: Yukarıda gösterilen Maven veya Gradle bağımlılığını ekleyin, ya da sürüm sayfasından JAR dosyasını indirin.

**S: Hangi görüntü formatları destekleniyor?**  
C: JPEG, PNG, TIFF, BMP, GIF ve daha birçok format—tam liste için ürün dokümantasyonuna bakın.

**S: Bu kütüphaneyi ticari bir projede kullanabilir miyim?**  
C: Evet, satın alma portalı üzerinden alınan geçerli bir lisansla kullanabilirsiniz.

**S: Çok büyük görüntülerle başa çıkmanın en iyi yolu nedir?**  
C: Bellek tüketimini kontrol etmek için `LoadOptions.setBufferSizeHint` kullanın ve birden fazla işlem yapmadan önce her zaman görüntüyü önbelleğe alın.

**S: PNG dosyalarının boyutunu daha da nasıl küçültebilirim?**  
C: Renk doğruluğu kritik olmadığında **png bit depth** değerini 4‑bit veya 2‑bit'e düşürün ve mümkün olduğunda gri ton kullanın.

**Last Updated:** 2025-12-27  
**Tested With:** Aspose.Imaging 25.5 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}