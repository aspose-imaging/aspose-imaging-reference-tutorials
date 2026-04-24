---
date: 2025-12-20
description: Java ve Aspose.Imaging kullanarak görüntüyü dikdörtgene kırpmayı ve görüntüyü
  genişletmeyi öğrenin. Geliştiriciler için adım adım rehber.
linktitle: Image Expansion or Cropping
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java ile Görüntüyü Dikdörtgene Kırp
url: /tr/java/document-conversion-and-processing/image-expansion-or-cropping/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java ile Görüntüyü Dikdörtgene Kırpma

Bugünün hızlı hareket eden dijital dünyasında, **crop image to rectangle** işlemini hızlı ve güvenilir bir şekilde yapabilmek, herhangi bir Java tabanlı görüntü iş akışı için temel bir gereksinimdir. Kullanıcıların yüklediği fotoğrafları kırpmanız, bir e‑ticaret kataloğu için küçük resimler oluşturmanız ya da sadece bir pazarlama kampanyası için varlıkları hazırlamanız gerektiğinde, Aspose.Imaging for Java işi halletmek için temiz, yüksek performanslı bir API sunar. Bu öğreticide, bir görüntüden dikdörtgen kırpma ve Java kullanarak bir görüntü tuvalini genişletme konularını adım adım inceleyeceğiz—**how to crop image java** tekniklerini ustalaşmak isteyen herkes için mükemmeldir.

## Hızlı Yanıtlar
- **What library is best for Java image cropping?** Aspose.Imaging for Java.
- **Can I crop to an arbitrary rectangle?** Evet – herhangi bir X, Y, genişlik ve yükseklik tanımlayabilirsiniz.
- **Do I need a license for development?** Ücretsiz deneme sürümü test için çalışır; üretim için bir lisans gereklidir.
- **Is expanding an image possible?** Kesinlikle – kırpmadan önce tuval boyutunu artırabilirsiniz.
- **Which Java version is supported?** Java 8 ve üzeri.

## “crop image to rectangle” nedir?
Bir görüntüyü dikdörtgene kırpmak, orijinal bitmap'in bir dikdörtgen bölge (X‑offset, Y‑offset, genişlik, yükseklik) ile tanımlanan bir alt bölümünü çıkarmak anlamına gelir. Görüntünün geri kalanı atılır ve yalnızca ihtiyacınız olan alanı içeren yeni, daha küçük bir görüntü elde edilir.

## Neden Aspose.Imaging for Java kullanmalısınız?
- **No external dependencies** – saf Java, herhangi bir platformda çalışır.
- **Broad format support** – JPEG, PNG, BMP, TIFF ve daha fazlası.
- **High‑performance caching** – `cacheData()` I/O yükünü azaltır.
- **Simple API** – yükleme, dikdörtgen tanımlama ve kaydetme için tek satır çağrılar.

## Önkoşullar

- **Java Development Environment** – JDK 8+ yüklü ve yapılandırılmış.
- **Aspose.Imaging for Java** – [website](https://releases.aspose.com/imaging/java/) adresinden indirin.
- **Basic Java Knowledge** – sınıflar, try‑with‑resources ve dosya yollarına aşina olmak.
- **Image to Work With** – kırpmak veya genişletmek istediğiniz herhangi bir JPEG/PNG.

## Paketleri İçe Aktarma

İlk olarak, kodu kaynak görüntülerin bulunduğu klasöre yönlendirin. Bu kod parçacığı orijinal öğreticideki gibi değişmeden kalır.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

`"Your Document Directory"` ifadesini makinenizdeki mutlak yol ile değiştirin.

## Adım 1: Görüntüyü Yükle

Görüntüyü yüklemek, herhangi bir manipülasyonun temelidir. Ayrıca `cacheData()` çağrısı yaparak bitmap'i bellekte tutar ve sonraki işlemleri hızlandırır.

```java
try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
{
    rasterImage.cacheData();
}
```

> **Pro tip:** Görüntünün otomatik olarak kapanmasını sağlamak ve bellek sızıntılarını önlemek için (gösterildiği gibi) bir `try‑with‑resources` bloğu kullanın.

## Adım 2: Kırpma Bölgesini Tanımla

Burada, tutmak istediğiniz kesin alanı temsil eden bir `Rectangle` oluşturuyoruz. Dikdörtgen, orijinal sınırların dışından başlayabilir – Aspose.Imaging tuvali otomatik olarak genişletecektir (**expand image using java** senaryosu için faydalıdır).

```java
// Create an instance of Rectangle class and define X, Y, Width, and Height of the rectangle
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

- **X / Y** – negatif değerler dikdörtgeni sola/yuvara kaydırır ve tuvalin genişlemesine neden olur.
- **Width / Height** – kırpılan bölgenin boyutu.

## Adım 3: Kırpılmış (veya Genişletilmiş) Görüntüyü Kaydet

Son olarak, sonucu diske yazın. `save` yöntemi hedef yolu, görüntü formatı seçeneklerini ve tanımladığımız dikdörtgeni alır.

```java
rasterImage.save("Your Document Directory" + "Grayscaling_out.jpg", new JpegOptions(), destRect);
```

Çıktı dosyası `Grayscaling_out.jpg` artık **crop image to rectangle** sonucunu içeriyor. Dikdörtgen orijinal görüntünün dışına uzanıyorsa, ekstra alan varsayılan bir arka planla doldurulur (PNG için şeffaf, JPEG için siyah).

## Yaygın Kullanım Durumları

| Senaryo | Neden Önemli |
|----------|----------------|
| **Thumbnail generation** | Tutarlı boyutlandırma için merkezi bölgeyi hızlıca çıkarır. |
| **User‑profile picture cropping** | Kare veya dikdörtgen avatar alanını zorunlu kılar. |
| **Canvas expansion before adding watermarks** | Orijinali bozmadan görüntünün etrafına boşluk ekler. |
| **Batch processing of scanned documents** | Tek seferde kenar boşluklarını kırpar. |

## Sorun Giderme ve İpuçları

- **Image not loading?** Dosya yolunu doğrulayın ve görüntü formatının desteklendiğinden emin olun.
- **Unexpected black borders after expansion?** `JpegOptions` içinde bir arka plan rengi ayarlayın veya şeffaflık için PNG kullanın.
- **Performance concerns with large images?** Java yığın boyutunu (`-Xmx`) artırın veya görüntüleri daha küçük partiler halinde işleyin.

## Sıkça Sorulan Sorular

**Q: What image formats does Aspose.Imaging for Java support?**  
A: JPEG, PNG, BMP, TIFF, GIF, ICO, PSD ve daha fazlası. Tam liste için resmi dokümantasyona bakın.

**Q: Can I perform other image manipulations with Aspose.Imaging for Java?**  
A: Kesinlikle! Yeniden boyutlandırma, döndürme, filtreleme ve format dönüştürme gibi işlemler de mevcuttur.

**Q: Is Aspose.Imaging for Java suitable for web applications?**  
A: Evet. Kütüphane thread‑safe'dir ve servlet konteynerleri ile Spring Boot servislerinde sorunsuz çalışır.

**Q: How can I get support for Aspose.Imaging for Java?**  
A: Topluluk yardımı için [forum](https://forum.aspose.com/) adresini ziyaret edin veya geçerli bir lisansla destek bileti açın.

**Q: Is there a free trial available for Aspose.Imaging for Java?**  
A: Evet, kütüphaneyi ücretsiz deneme sürümüyle keşfedebilirsiniz. [buradan](https://releases.aspose.com/) indirin.

## Sonuç

Artık **crop image to rectangle** ve hatta **expand image using Java** işlemlerini güçlü Aspose.Imaging API'si ile nasıl yapacağınızı öğrendiniz. Bu temelleri ustalaştırarak sağlam görüntü‑işleme hatları oluşturabilir, UI yanıt süresini iyileştirebilir ve herhangi bir Java uygulamasında şık görsel içerikler sunabilirsiniz.

---

**Son Güncelleme:** 2025-12-20  
**Test Edilen Versiyon:** Aspose.Imaging for Java 24.11 (yazım zamanı en güncel)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}