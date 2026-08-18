---
date: 2026-02-09
description: Aspose.Imaging for .NET kullanarak yay çizmeyi, BMP dosyasını kaydetmeyi,
  görüntü boyutunu ayarlamayı ve grafik arka planını belirlemeyi öğrenin. BMP görüntüleri
  oluşturmak için adım adım rehber.
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Aspose.Imaging for .NET ile Yay Nasıl Çizilir
url: /tr/net/basic-drawing/draw-arc/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET ile Yay Çizme

Görüntü işleme dünyasında, **yay nasıl çizilir** yaygın bir görevdir ve herhangi bir grafiğe görsel çekicilik katabilir. Aspose.Imaging for .NET ile sadece birkaç C# satırıyla BMP görüntüler oluşturabilir, görüntü boyutunu ayarlayabilir ve bir kalemle yay çizebilirsiniz. Bu öğreticinin sonunda yay nasıl çizilir, grafik arka planı nasıl ayarlanır ve ortaya çıkan BMP dosyasını sorunsuz bir şekilde nasıl kaydedilir, tam olarak öğreneceksiniz.

## Hızlı Yanıtlar
- **Kod ne üretir?** Sarı arka planlı ve siyah bir yay içeren 100 × 100 piksel BMP görüntüsü.  
- **Hangi kütüphane kullanılıyor?** Aspose.Imaging for .NET.  
- **Lisans gerekli mi?** Geliştirme için ücretsiz deneme çalışır; üretim için ticari lisans gerekir.  
- **Görüntü boyutunu değiştirebilir miyim?** Evet – `Image.Create` çağrısındaki genişlik ve yükseklik parametrelerini değiştirin.  
- **Çıktı formatı sabit mi?** Örnek bir BMP dosyası kaydeder, ancak Aspose.Imaging tarafından desteklenen herhangi bir format kullanılabilir.

## Aspose.Imaging’de “yay nasıl çizilir” nedir?
Yay çizmek, sınırlayıcı bir dikdörtgen, başlangıç açısı ve süpürme açısı ile tanımlanan kavisli bir çizgi segmenti oluşturmak anlamına gelir. Aspose.Imaging, **kalemle yay çizmeyi** sağlayan ve her görsel yönü kontrol etmenize imkan veren `Graphics.DrawArc` metodunu sunar.

## Bu görev için Aspose.Imaging neden kullanılmalı?
- **Tam kontrol** görüntü boyutları, renk derinliği ve dosya formatı üzerinde.  
- **Harici bağımlılık yok** – her şey saf .NET üzerinde çalışır.  
- **Yüksek performans** sunucu tarafında büyük miktarda grafik üretmek için.

## Önkoşullar

Koda geçmeden önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Aspose.Imaging for .NET** – resmi siteden [buradan](https://releases.aspose.com/imaging/net/) indirin.  
2. **Bir .NET geliştirme ortamı** (Visual Studio, VS Code veya herhangi bir C# derleyicisi).  

Gereksinimlerimiz hazır olduğuna göre, çizmeye başlayalım!

## Gerekli Ad Alanlarını İçe Aktarma

### Adım 1: Ad Alanlarını İçe Aktarın

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

Bu `using` ifadeleri, görüntü oluşturma, grafik işleme ve dosya G/Ç sınıflarına erişim sağlar.

## Aspose.Imaging for .NET ile Yay Çizme

İşlemi üç net adıma böleceğiz: görüntüyü oluşturma, grafik yüzeyini hazırlama ve sonunda yayı çizme.

### Adım 1: Görüntüyü Oluşturun (görüntü boyutunu ayarlayın ve BMP görüntüsü oluşturun)

```csharp
// Specify the directory where you want to save the image
string dataDir = "Your Document Directory";

// Create an instance of FileStream to save the image
using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
{
    // Create an instance of BmpOptions and set its properties
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;

    // Set the source for BmpOptions and create an instance of Image
    saveOptions.Source = new StreamSource(stream);
    using (Image image = Image.Create(saveOptions, 100, 100))
    {
```

Burada **görüntü boyutunu** 100 × 100 piksel olarak ayarlıyoruz ve BMP seçeneklerini yapılandırıyoruz. `FileStream`, **BMP dosyasını** istediğiniz konuma kaydetmemizi sağlar.

### Adım 2: Grafik Nesnesini Başlatın ve Grafik Arka Planını Ayarlayın

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

`Graphics` nesnesi, görüntü üzerine çizim yapmamızı sağlar. `Clear(Color.Yellow)` çağrısı ile **grafik arka planını** parlak sarı olarak ayarlıyoruz, böylece yay öne çıkıyor.

### Adım 3: Yay Parametrelerini Tanımlayın ve Kalemle Yay Çizin

```csharp
        // Define the parameters for the arc
        int width = 100;
        int height = 200;
        int startAngle = 45;
        int sweepAngle = 270;

        // Draw the arc
        graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);

        // Save the changes
        image.Save();
    }
    stream.Close();
}
```

- `width` ve `height`, sınırlayıcı dikdörtgeni tanımlar ve dolaylı olarak yay için **görüntü boyutunu** ayarlar.  
- `Pen` nesnesi, siyah renkte **kalemle yay çizmeyi** sağlar.  
- Çizimden sonra, `image.Save()` **BMP dosyasını** diske yazar.

## Yaygın Sorunlar ve İpuçları

- **Yay görünmüyor mu?** Kalem renginin arka planla kontrast oluşturduğundan emin olun (ör. sarı üzerinde siyah).  
- **Yanlış boyutlar?** Yayın sınırlayıcı dikdörtgeninin görüntüden daha büyük olabileceğini unutmayın; `width`/`height` ya da görüntü boyutunu buna göre ayarlayın.  
- **Performans ipucu:** Aynı görüntüde birden fazla şekil çizmeniz gerekiyorsa tek bir `Graphics` örneğini tekrar kullanın.

## SSS

### S1: Aspose.Imaging for .NET belgelerine nereden ulaşabilirim?

A1: Belgelere [buradan](https://reference.aspose.com/imaging/net/) ulaşabilirsiniz.

### S2: Aspose.Imaging for .NET'i nasıl indirebilirim?

A2: Aspose.Imaging for .NET'i web sitesinden [buradan](https://releases.aspose.com/imaging/net/) indirebilirsiniz.

### S3: Aspose.Imaging for .NET için ücretsiz deneme sürümü var mı?

A3: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) alabilirsiniz.

### S4: Aspose.Imaging for .NET için geçici bir lisansa ihtiyacım var mı?

A4: Geçici bir lisansa ihtiyacınız varsa, birini [buradan](https://purchase.aspose.com/temporary-license/) edinebilirsiniz.

### S5: Aspose.Imaging for .NET ile ilgili destek alabileceğim veya soru sorabileceğim yer neresi?

A5: Destek ve tartışmalar için Aspose.Imaging forumunu [buradan](https://forum.aspose.com/) ziyaret edebilirsiniz.

---

**Son Güncelleme:** 2026-02-09  
**Test Edilen Versiyon:** Aspose.Imaging 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}