---
title: Aspose.Imaging for .NET'te SVG'de Raster Görüntü Nasıl Çizilir
linktitle: Aspose.Imaging for .NET'te SVG üzerinde Raster Görüntü Çizin
second_title: Aspose.Imaging .NET Görüntü İşleme API'si
description: Aspose.Imaging for .NET'i kullanarak SVG'de raster görüntülerin nasıl çizileceğini öğrenin. .NET uygulamalarınızı dinamik görüntülerle geliştirin.
type: docs
weight: 11
url: /tr/net/vector-image-processing/draw-raster-image-on-svg/
---

.NET programlama dünyasında Aspose.Imaging, görüntüyle ilgili çeşitli görevleri yerine getiren güvenilir ve çok yönlü bir kütüphane olarak duruyor. Sunduğu büyüleyici yeteneklerden biri, SVG tuval üzerine taramalı görüntü çizebilme yeteneğidir. Bu adım adım kılavuzda, Aspose.Imaging for .NET'i kullanarak SVG üzerinde raster görüntü çizme sürecinde size yol göstereceğiz.

## Önkoşullar

Ayrıntılara dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.Imaging for .NET: Kütüphanenin kurulu olması gerekir. Değilse, adresinden indirebilirsiniz.[Aspose.Imaging for .NET indirme sayfası](https://releases.aspose.com/imaging/net/).

-  Belge Dizininiz: Değiştirin`"Your Document Directory"` çalışma dizininizin gerçek yolu ile.

Şimdi süreci takip edilmesi kolay adımlara ayıralım:

## 1. Adım: Gerekli Ad Alanlarını İçe Aktarın

Aspose.Imaging ile çalışmak için gerekli ad alanlarını içe aktarmanız gerekir:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## 2. Adım: Görüntüleri Yükleyin

- Öncelikle çizmek istediğiniz tarama görüntüsünü SVG tuvaline yükleyin.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Daha sonra, tarama görüntüsünü çizmek istediğiniz yere SVG tuval görüntüsünü yükleyin.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## 3. Adım: SVG Görüntüsünde Çizim Yapma

Artık mevcut SVG görüntüsü üzerinde çizim yapmaya başlayabilirsiniz. Bunu yapmak için bir örneğini oluşturmanız gerekir.`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Adım 4: Raster Görüntüyü Çizin

- Raster görüntüyü çizmek istediğiniz yerin sınırlarını tanımlayın ve taramalı görüntüden kaynak bölgeyi belirtin.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Adım 5: Sonucu Kaydet

Tarama görüntüsünü SVG tuvaline çizdikten sonra ortaya çıkan görüntüyü kaydedebilirsiniz:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Çözüm

Tebrikler! Aspose.Imaging for .NET'i kullanarak SVG tuval üzerine başarılı bir şekilde taramalı görüntü çizdiniz. Bu, .NET uygulamalarınızda zengin ve dinamik görüntüler oluşturmak için inanılmaz derecede yararlı olabilir.

 Daha fazla bilgi ve ayrıntılı belgeler için şu adresi ziyaret edin:[Aspose.Imaging for .NET belgeleri](https://reference.aspose.com/imaging/net/).

## Sıkça Sorulan Sorular

### Aspose.Imaging for .NET nedir?
   Aspose.Imaging for .NET, geliştiricilerin .NET uygulamaları içinde çeşitli formatlardaki görüntüleri oluşturmasına, işlemesine ve dönüştürmesine olanak tanıyan güçlü bir görüntü işleme kitaplığıdır.

### Aspose.Imaging for .NET'i ticari projelerde kullanabilir miyim?
    Evet, Aspose.Imaging for .NET'i hem ticari hem de ticari olmayan projelerde kullanabilirsiniz. Lisans ayrıntılarına şuradan ulaşılabilir:[satın alma sayfası](https://purchase.aspose.com/buy).

### Ücretsiz deneme mevcut mu?
    Evet, Aspose.Imaging for .NET'in ücretsiz deneme sürümünü şu adresten edinebilirsiniz:[Burada](https://releases.aspose.com/).

### Nereden destek alabilirim veya soru sorabilirim?
    Sorularınız varsa veya desteğe ihtiyacınız varsa şu adresi ziyaret edebilirsiniz:[Aspose.Görüntüleme forumu](https://forum.aspose.com/).

### Aspose.Imaging for .NET için nasıl geçici lisans alabilirim?
    adresinden geçici lisans alabilirsiniz.[Burada](https://purchase.aspose.com/temporary-license/).


