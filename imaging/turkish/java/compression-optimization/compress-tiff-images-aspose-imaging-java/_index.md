---
date: '2026-03-20'
description: Aspose.Imaging for Java'yı kullanarak TIFF görüntülerini LZW sıkıştırmasıyla
  nasıl sıkıştıracağınızı öğrenin; dosya boyutunu küçültürken kaliteyi koruyun.
keywords:
- compress TIFF images Java
- Aspose.Imaging LZW compression
- Java image optimization
- TIFF compression in Java with Aspose
- image compression tutorial
title: Aspose.Imaging'i Kullanarak Java'da TIFF Görüntülerini Sıkıştırma (LZW Sıkıştırma
  Rehberi)
url: /tr/java/compression-optimization/compress-tiff-images-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Tutorial: Compressing TIFF Images Using Aspose.Imaging Java

## Introduction

Bu öğreticide **Aspose.Imaging for Java** kullanarak TIFF görüntülerini verimli bir şekilde sıkıştırmayı öğreneceksiniz. Büyük TIFF dosyalarını yönetmek depolama ve bant genişliğini hızla tüketebilir, ancak LZW (Lempel‑Ziv‑Welch) sıkıştırmasıyla **TIFF dosya boyutunu** görüntü kalitesinden ödün vermeden **azaltabilirsiniz**. Bir TIFF dosyasını yükleme, **tiff compression LZW** ayarlama ve optimize edilmiş sonucu kaydetme adımlarını göstereceğiz—**java image optimization** ile ilgilenen herkes için ideal.

**Öğrenecekleriniz**
- Aspose.Imaging for Java nasıl kurulur
- TIFF görüntülerinin kolayca yüklenmesi ve işlenmesi
- `TiffOptions` ile LZW sıkıştırmasının yapılandırılması
- Daha küçük ama kayıpsız TIFF görüntülerinin kaydedilmesi

Hemen sıkıştırmaya başlayabilmeniz için ön koşulları gözden geçirelim.

## Quick Answers
- **Gerekli kütüphane nedir?** Aspose.Imaging for Java  
- **Hangi sıkıştırma algoritması?** LZW (kayıpsız)  
- **Desteklenen Java sürümleri?** En yeni JDK'lar (ör. 11, 17)  
- **Lisans gerekli mi?** Test için bir deneme veya geçici lisans yeterlidir; üretim için ticari lisans gerekir.  
- **Tipik boyut azaltma oranı?** Uygun görüntülerde %30‑50 ’ye kadar  

## Prerequisites

Java projenizde görüntü sıkıştırmasını uygulamadan önce aşağıdakilerin mevcut olduğundan emin olun:

- **Aspose.Imaging for Java library** – tüm görüntü işleme özellikleri için zorunludur.  
- **Java Development Kit (JDK)** – Aspose kütüphanesiyle uyumlu güncel bir sürüm.  
- **Temel Java bilgisi** – dosya I/O ve nesne‑yönelimli kavramlara aşina olmak işinizi kolaylaştırır.

## Setting Up Aspose.Imaging for Java

Başlamak için Aspose.Imaging kütüphanesini derleme sisteminize ekleyin. Projenize uygun yöntemi seçin.

### Using Maven
`pom.xml` dosyanıza aşağıdaki bağımlılığı ekleyin:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Using Gradle
`build.gradle` dosyanıza şu satırı ekleyin:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Direct Download
Alternatif olarak, en son sürümü [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) adresinden indirebilirsiniz.

#### License Acquisition
Satın almadan önce Aspose.Imaging'in yeteneklerini tam olarak değerlendirmek için ücretsiz deneme lisansı ya da geçici lisans alabilirsiniz.

## How to Use Aspose.Imaging for TIFF Compression in Java

Şimdi uygulamayı adım adım inceleyelim. Her kod bloğu orijinal öğreticiden değiştirilmemiştir; ancak etrafına daha net açıklamalar ekleyeceğiz.

### Loading a TIFF Image

**Neden önemli:** Görüntüyü doğru şekilde yüklemek, sonraki tüm işlemlerin uygulanacağı geçerli bir `Image` nesnesi oluşturur.

#### Step 1: Import the Image class
```java
import com.aspose.imaging.Image;
```

#### Step 2: Load the image from disk
```java
String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "/sample.tiff";
Image image = Image.load(dataDir);
```

### Creating TiffOptions for Image Compression

**Neden önemli:** `TiffOptions`, çıktı TIFF'inin nasıl kodlanacağını tanımlamanızı sağlar; burada **tiff compression LZW** ayarı da bulunur.

#### Step 1: Import the required enums and options class
```java
import com.aspose.imaging.fileformats.tiff.enums.TiffCompressions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.imaging.imageoptions.TiffOptions;
```

#### Step 2: Configure compression options
```java
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);
outputSettings.setBitsPerSample(new int[] { 4 });
outputSettings.setCompression(TiffCompressions.Lzw);
outputSettings.setPhotometric(TiffPhotometrics.Palette);
```

### Setting a Grayscale Palette (Optional but Helpful)

4‑bit gri tonlamalı bir palet uygulamak, özellikle tek renkli taramalarda **TIFF dosya boyutunu daha da azaltabilir**.

#### Step 1: Import the palette helper
```java
import com.aspose.imaging.ColorPaletteHelper;
```

#### Step 2: Assign the grayscale palette
```java
outputSettings.setPalette(ColorPaletteHelper.create4BitGrayscale(false));
```

### Saving the Compressed TIFF Image

**Neden önemli:** `save` çağrısı, yapılandırdığınız tüm seçenekleri kullanarak görüntüyü diske yazar ve daha küçük, LZW‑sıkıştırmalı bir dosya üretir.

#### Step 1: Define the output path
```java
String outputDir = "YOUR_OUTPUT_DIRECTORY" + "/SampleTiff_out.tiff";
```

#### Step 2: Save with the compression settings
```java
image.save(outputDir, outputSettings);
```

## Practical Applications

**how to compress tiff** görüntüleri LZW ile sıkıştırmanın gerçek dünyadaki bazı senaryoları:

1. **Arşivleme Belgeleri** – Taranan PDF'leri veya TIFF'leri daha verimli saklayın.  
2. **Tıbbi Görüntüleme** – Tanısal detayı korurken dosya boyutlarını yönetilebilir tutun.  
3. **Fotoğraf Arşivleri** – Yüksek çözünürlüklü ana dosyaları depolama alanını şişirmeden saklayın.  
4. **Web Uygulamaları** – Daha küçük görüntülerle sayfa yükleme süresini ve bant genişliği maliyetlerini azaltın.

## Performance Considerations

Büyük görüntülerle çalışırken optimum performansı korumak için şu ipuçlarını aklınızda bulundurun:

- **Bellek Yönetimi:** Bir döngü içinde birden çok dosya işliyorsanız büyük `Image` nesnelerini hemen (`image.dispose()`) serbest bırakın.  
- **Bit Derinliği Optimizasyonu:** Kullanım durumunuza uygun en düşük `BitsPerSample` değerini ayarlayın.  
- **Toplu İşleme:** Çoklu dosya işlemleri için çok iş parçacıklı (multithreading) yaklaşımını düşünebilirsiniz, ancak JVM yığın kullanımını izleyin.

## Common Issues and Solutions

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| OutOfMemoryError while loading huge TIFFs | Image loaded fully into memory | Use `Image.load(dataDir, new LoadOptions { BufferSize = … })` or process in tiles. |
| Saved file is larger than original | Incorrect `BitsPerSample` or palette mismatch | Verify that `setBitsPerSample` matches the source image's color depth. |
| Grayscale palette appears wrong | Palette not applied before saving | Ensure `outputSettings.setPalette(...)` is called **before** `image.save`. |

## Frequently Asked Questions

**Q: LZW sıkıştırması nedir?**  
A: Lempel‑Ziv‑Welch (LZW) sıkıştırması, görüntü verisini kaybetmeden dosya boyutunu azaltan kayıpsız bir algoritmadır.

**Q: Aspose.Imaging for Java’yı ticari projelerde kullanabilir miyim?**  
A: Evet, ticari kullanım için lisans satın alabilirsiniz. Detaylar için [Aspose Purchase](https://purchase.aspose.com/buy) sayfasını ziyaret edin.

**Q: Kütüphane tüm JDK sürümleriyle uyumlu mu?**  
A: Çoğu yeni JDK sürümünü destekler. Tam sürüm uyumluluğu için resmi dokümantasyona bakın.

**Q: Büyük görüntülerde bellek tükenmesini nasıl önleyebilirim?**  
A: `Image` nesnelerini zamanında dispose ederek ve mümkün olduğunda görüntüleri daha küçük parçalar halinde işleyerek bellek yönetimini etkinleştirin.

**Q: Aspose.Imaging başka hangi dosya formatlarını destekliyor?**  
A: BMP, JPEG, PNG, GIF ve daha birçok formatı işler. Tam listeyi [documentation site](https://reference.aspose.com/imaging/java/) üzerinden inceleyin.

## Resources

- **Documentation:** [Aspose.Imaging Java Reference](https://reference.aspose.com/imaging/java/)  
- **Download:** [Latest Releases](https://releases.aspose.com/imaging/java/)  
- **Purchase:** [Buy Now](https://purchase.aspose.com/buy)  
- **Free Trial:** [Start Here](https://releases.aspose.com/imaging/java/)  
- **Temporary License:** [Request Here](https://purchase.aspose.com/temporary-license/)  
- **Support:** Daha fazla yardım için [Aspose Forum](https://forum.aspose.com/c/imaging/14) adresini ziyaret edin.

---  

**Last Updated:** 2026-03-20  
**Tested With:** Aspose.Imaging 25.5 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}