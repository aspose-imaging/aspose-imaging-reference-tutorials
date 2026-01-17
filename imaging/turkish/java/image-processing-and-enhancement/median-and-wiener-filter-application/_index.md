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

# Median Filter Java – Median ve Wiener Filtrelerini Uygulama

Görüntü işleme dünyasında, gürültüyü kaldırmak ve görüntü kalitesini artırmak kritik görevlerdir. **median filter java** ile Aspose.Imaging for Java kullanarak gürültülü resimleri etkili bir şekilde temizleyebilirsiniz. Bu öğreticide, bir görüntüyü gürültüsüzleştirmek için Median ve Wiener filtrelerini uygulama sürecini adım adım göstereceğiz, böylece karmaşık kod yazmadan profesyonel düzeyde sonuçlar elde edebilirsiniz.

## Quick Answers
- **Median filtre ne yapar?** Her pikseli çevresindeki komşuların medyan değeriyle değiştirir, impuls gürültüsünü kaldırırken kenarları korur.  
- **Hangi kütüphane median filter java’yı destekler?** Aspose.Imaging for Java, kullanıma hazır bir `MedianFilterOptions` sınıfı sağlar.  
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Median filtreyi diğer filtrelerle zincirleyebilir miyim?** Evet, median adımından sonra Wiener gibi ek filtreler uygulayabilirsiniz.  
- **Hangi görüntü formatları destekleniyor?** Çoğu raster formatı (PNG, JPEG, BMP, TIFF, vb.) tam olarak desteklenir.

## What is Median Filter Java?
Median filtre, **görüntü gürültüsünü kaldırmak** için yaygın olarak kullanılan doğrusal olmayan bir dijital filtreleme tekniğidir. Java’da Aspose.Imaging, bu filtreyi `MedianFilterOptions` sınıfı aracılığıyla uygular ve kaç komşu pikselin dikkate alındığını belirleyen çekirdek boyutunu belirtmenize olanak tanır.

## Why Use Median Filter Java for Image Denoising?
- **Kenarları** basit ortalama filtrelerinden daha iyi korur.  
- **Basit API** – birkaç satır kodla lekeleri ve tuz‑biber gürültüsünü kaldırır.  
- **Her raster görüntüde çalışır** Aspose.Imaging ile yüklenen, sunucu‑tarafı işleme için idealdir.

## Prerequisites
Before diving in, ensure you have the following:

1. **Java Geliştirme Ortamı** – JDK 8 veya daha yeni bir sürüm yüklü.  
2. **Aspose.Imaging for Java** – Kütüphaneyi [buradan](https://releases.aspose.com/imaging/java/) indirip kurun.  
3. **Örnek Gürültülü Görüntü** – Temizlemek istediğiniz herhangi bir görüntü; bu kılavuzda `your‑noisy‑image.png` dosyasını kullanacağız.  

## Import Packages
In your Java project, start by importing the necessary Aspose.Imaging classes:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.imagefilters.filteroptions.MedianFilterOptions;
```

## How to Apply Median Filter Java
Below is a step‑by‑step walkthrough. Each step includes a short explanation followed by the exact code you need to copy.

### Step 1: Load the Noisy Image
First, load the image you want to denoise. This demonstrates **load image java** using Aspose.Imaging’s `Image.load` method.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (Image image = Image.load(dataDir + "your-noisy-image.png"))
{
    // Cast the image into RasterImage
    RasterImage rasterImage = (RasterImage) image;
```

### Step 2: Create and Configure the Median Filter
Create an instance of `MedianFilterOptions` and set the kernel size. A larger size removes more noise but may blur details.

```java
    // Create an instance of MedianFilterOptions class and set the size.
    MedianFilterOptions options = new MedianFilterOptions(4);
```

### Step 3: Apply the Median Filter
Apply the filter to the entire image bounds. This is the core **apply median filter** operation.

```java
    // Apply Median filter to RasterImage object.
    rasterImage.filter(image.getBounds(), options);
```

### Step 4: Save the Resultant Image
Finally, write the denoised image to disk. You can now see the effect of the median filter.

```java
    // Save the resultant image
    image.save("Your Document Directory" + "denoised-image.png");
}
```

## Common Issues and Solutions
- **Çekirdek boyutu çok büyük** – Görüntü aşırı bulanık görünebilir. Çoğu fotoğraf için 3‑5 arasında değerler deneyin.  
- **Desteklenmeyen görüntü formatı** – Dosyanın Aspose.Imaging tarafından desteklenen bir raster formatı olduğundan emin olun.  
- **OutOfMemoryError** – Büyük görüntüleri filtrelemeden önce `RasterImage` sınıfının `crop` yöntemiyle daha küçük parçalar halinde işleyin.

## Conclusion
Bu kılavuzda, Aspose.Imaging tarafından sağlanan **median filter java** yaklaşımını kullanarak **görüntüleri nasıl gürültüsüzleştireceğinizi** gösterdik. Yukarıdaki adımları izleyerek, gürültü kaldırmayı herhangi bir Java tabanlı görüntü işleme hattına hızlıca entegre edebilir ve sonuçları Wiener filtresi veya diğer gelişmiş tekniklerle zincirleyerek daha da iyileştirebilirsiniz.

## Frequently Asked Questions

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

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-01-17  
**Test Edilen:** Aspose.Imaging for Java 24.11  
**Yazar:** Aspose