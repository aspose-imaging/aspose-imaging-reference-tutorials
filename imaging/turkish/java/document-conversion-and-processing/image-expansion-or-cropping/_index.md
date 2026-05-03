---
date: 2026-05-03
description: Aspose.Imaging for Java ile görüntüyü nasıl kırpacağınızı, dikdörtgen
  kırpma ve tuval genişletme dahil olmak üzere öğrenin. Geliştiriciler için adım adım
  kılavuz.
keywords:
- how to crop image
- crop and expand image
- aspose imaging crop
- java image processing tutorial
- expand image canvas java
linktitle: Resim Büyütme veya Kırpma
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java ile Görüntüyü Dikdörtgene Kırpma
url: /tr/java/document-conversion-and-processing/image-expansion-or-cropping/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java ile Görüntüyü Dikdörtgene Kırpma

Bugünün hızlı hareket eden dijital dünyasında, **görseli nasıl kırpacağını** hızlı ve güvenilir bir şekilde bilmek, herhangi bir Java tabanlı görüntü iş akışı için temel bir gereksinimdir. İster bir web hizmeti için kullanıcı yüklediği fotoğrafları kırpıyor, ister bir e‑ticaret kataloğu için tutarlı küçük resimler oluşturuyor, ister bir pazarlama kampanyası için varlıkları hazırlıyor olun, Aspose.Imaging for Java işi halletmek için temiz, yüksek performanslı bir API sunar. Bu öğreticide bir görüntüden dikdörtgen kırpma ve görüntü tuvalini genişletme konularını adım adım inceleyeceğiz—Java görüntü işleme tekniklerinde uzmanlaşmak isteyen herkes için mükemmel.

## Hızlı Yanıtlar
- **Java görüntü kırpma için en iyi kütüphane nedir?** Aspose.Imaging for Java.  
- **İstediğim bir dikdörtgene kırpabilir miyim?** Evet – herhangi bir X, Y, genişlik ve yükseklik tanımlayabilirsiniz.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme sürümü test için çalışır; üretim için lisans gereklidir.  
- **Bir görüntüyü genişletmek mümkün mü?** Kesinlikle – kırpmadan önce tuval boyutunu artırabilirsiniz.  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri.

## Görüntüyü Dikdörtgene Kırpma Nedir?
Bir görüntüyü dikdörtgene kırpmak, orijinal bitmap'in bir dikdörtgen bölge (X kaydırması, Y kaydırması, genişlik, yükseklik) ile tanımlanan bir alt bölümünü çıkarmak anlamına gelir. Görüntünün geri kalanı atılır ve yalnızca ihtiyacınız olan alanı içeren yeni, daha küçük bir görüntü elde edersiniz.

## Neden Aspose.Imaging for Java Kullanmalısınız?
- **Harici bağımlılık yok** – saf Java, herhangi bir platformda çalışır.  
- **Geniş format desteği** – JPEG, PNG, BMP, TIFF ve daha fazlası.  
- **Yüksek performanslı önbellekleme** – `cacheData()` I/O yükünü azaltır.  
- **Basit API** – yükleme, dikdörtgen tanımlama ve kaydetme için tek satır çağrılar.

## Önkoşullar
- **Java Development Environment** – JDK 8+ yüklü ve yapılandırılmış.  
- **Aspose.Imaging for Java** – [website](https://releases.aspose.com/imaging/java/) adresinden indirin.  
- **Basic Java Knowledge** – sınıflar, try‑with‑resources ve dosya yolları konularına aşina olmak.  
- **Image to Work With** – kırpmak veya genişletmek istediğiniz herhangi bir JPEG/PNG.

## Paketleri İçe Aktarma
İlk olarak, kodu kaynak görüntülerinizi içeren klasöre yönlendirin. Bu snippet orijinal öğreticide olduğu gibi değişmeden kalır.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

`"Your Document Directory"` ifadesini makinenizdeki mutlak yol ile değiştirin.

## Adım 1: Görüntüyü Yükle
Görüntüyü yüklemek, herhangi bir manipülasyonun temelidir. Ayrıca `cacheData()` çağrısıyla bitmap'i bellekte tutarak sonraki işlemlerin hızlı olmasını sağlarız.

```java
try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
{
    rasterImage.cacheData();
}
```

> **Pro ipucu:** Görüntünün otomatik olarak kapanmasını sağlamak ve bellek sızıntılarını önlemek için (gösterildiği gibi) bir `try‑with‑resources` bloğu kullanın.

## Adım 2: Kırpma Bölgesini Tanımla
Burada, tutmak istediğiniz kesin alanı temsil eden bir `Rectangle` oluşturuyoruz. Dikdörtgen, orijinal sınırların dışından başlayabilir – Aspose.Imaging tuvali otomatik olarak genişletecektir (**expand image canvas java** senaryosu için faydalıdır).

```java
// Create an instance of Rectangle class and define X, Y, Width, and Height of the rectangle
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

- **X / Y** – negatif değerler dikdörtgeni sola/yukarı kaydırır ve tuvalin genişlemesine neden olur.  
- **Width / Height** – kırpılan bölgenin boyutu.

## Adım 3: Kırpılmış (veya Genişletilmiş) Görüntüyü Kaydet
Son olarak, sonucu diske yazın. `save` metodu hedef yolu, görüntü formatı seçeneklerini ve tanımladığımız dikdörtgeni alır.

```java
rasterImage.save("Your Document Directory" + "Grayscaling_out.jpg", new JpegOptions(), destRect);
```

`Grayscaling_out.jpg` çıktı dosyası artık **crop image to rectangle** sonucunu içeriyor. Eğer dikdörtgen orijinal görüntünün dışına uzanıyorsa, ekstra alan varsayılan bir arka planla doldurulur (PNG için şeffaf, JPEG için siyah).

## Aspose.Imaging for Java ile Görüntüyü Nasıl Kırparız
Bu bölüm, kod yazarken hızlıca başvurabileceğiniz öz bir kontrol listesi şeklinde temel adımları tekrar eder:

1. **Veri dizinini ayarla** – kaynak görüntüleri içeren klasöre işaret edin.  
2. **Görüntüyü yükle** `Image.load()` ile ve `cacheData()` çağırın.  
3. **Bir `Rectangle` oluştur** kırpma bölgesini (veya tuval genişletmeyi) tanımlamak için.  
4. **Kaydet** yeni görüntüyü `rasterImage.save()` kullanarak ve dikdörtgeni geçerek.

## Görüntüyü Kırp ve Genişlet – Gerçek Dünya Kullanım Senaryoları
| Senaryo | Neden Önemli |
|----------|----------------|
| **Küçük resim oluşturma** | Tutarlı boyutlandırma için merkezi bir bölgeyi hızlıca çıkarın. |
| **Kullanıcı profili resmi kırpma** | Kare veya dikdörtgen bir avatar alanı zorunlu kılın. |
| **Filigran eklemeden önce tuval genişletme** | Orijinali bozmadan görüntünün etrafına boşluk ekleyin. |
| **Taranmış belgelerin toplu işlenmesi** | Kenarlıkları tek seferde kırpın. |

## Sorun Giderme ve İpuçları
- **Görüntü yüklenmiyor mu?** Dosya yolunu doğrulayın ve görüntü formatının desteklendiğinden emin olun.  
- **Genişletmeden sonra beklenmeyen siyah kenarlar?** `JpegOptions` içinde bir arka plan rengi ayarlayın veya şeffaflık için PNG kullanın.  
- **Büyük görüntülerde performans endişeleri?** Java yığın boyutunu (`-Xmx`) artırın veya görüntüleri daha küçük partilerde işleyin.  
- **Yaygın tuzak:** `cacheData()` çağırmayı unutmak, sonraki işlemlerde daha yavaş I/O'ya yol açabilir.

## Sıkça Sorulan Sorular

**S: Aspose.Imaging for Java hangi görüntü formatlarını destekliyor?**  
C: JPEG, PNG, BMP, TIFF, GIF, ICO, PSD ve daha fazlası. Tam liste için resmi dokümantasyona bakın.

**S: Aspose.Imaging for Java ile başka görüntü manipülasyonları yapabilir miyim?**  
C: Kesinlikle! Yeniden boyutlandırma, döndürme, filtreleme ve format dönüşümü gibi işlemler mevcuttur.

**S: Aspose.Imaging for Java web uygulamaları için uygun mu?**  
C: Evet. Kütüphane çoklu iş parçacığı güvenlidir ve servlet konteynerlerinde ve Spring Boot servislerinde iyi çalışır.

**S: Aspose.Imaging for Java için destek nasıl alabilirim?**  
C: Topluluk yardımı için [forum](https://forum.aspose.com/) adresini ziyaret edin veya geçerli bir lisansla destek talebi açın.

**S: Aspose.Imaging for Java için ücretsiz deneme mevcut mu?**  
C: Evet, kütüphaneyi ücretsiz deneme sürümüyle keşfedebilirsiniz. [buradan](https://releases.aspose.com/) indirin.

## Sonuç
Artık güçlü Aspose.Imaging API'sini kullanarak bir görüntüyü dikdörtgene **kırpmayı** ve hatta **görüntü tuvalini genişletmeyi** öğrendiniz. Bu temelleri ustalaşarak sağlam görüntü işleme boru hatları oluşturabilir, UI yanıt süresini iyileştirebilir ve herhangi bir Java uygulamasında şık görsel içerikler sunabilirsiniz.

---

**Son Güncelleme:** 2026-05-03  
**Test Edilen Versiyon:** Aspose.Imaging for Java 24.11 (yazım zamanındaki en son)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}