---
"description": "Aspose.Imaging for .NET kullanarak SVG üzerine raster resimlerin nasıl çizileceğini öğrenin. .NET uygulamalarınızı dinamik resimlerle geliştirin."
"linktitle": "Aspose.Imaging for .NET'te SVG'ye Raster Görüntüsü Çizme"
"second_title": "Aspose.Imaging .NET Görüntü İşleme API'si"
"title": "Aspose.Imaging for .NET'te SVG Üzerine Raster Görüntü Nasıl Çizilir"
"url": "/tr/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET'te SVG Üzerine Raster Görüntü Nasıl Çizilir


.NET programlama dünyasında, Aspose.Imaging çeşitli görüntüyle ilgili görevleri ele almak için güvenilir ve çok yönlü bir kütüphane olarak öne çıkıyor. Sunduğu büyüleyici yeteneklerden biri de bir SVG tuvali üzerine raster görüntü çizme yeteneğidir. Bu adım adım kılavuzda, .NET için Aspose.Imaging kullanarak bir SVG üzerine raster görüntü çizme sürecini adım adım anlatacağız.

## Ön koşullar

Ayrıntılara girmeden önce, aşağıdaki ön koşulların mevcut olduğundan emin olun:

- Aspose.Imaging for .NET: Kütüphaneyi yüklemiş olmanız gerekir. Değilse, şuradan indirebilirsiniz: [Aspose.Imaging for .NET indirme sayfası](https://releases.aspose.com/imaging/net/).

- Belge Dizininiz: Değiştir `"Your Document Directory"` çalışma dizininize giden gerçek yol ile.

Şimdi süreci kolay takip edilebilir adımlara bölelim:

## Adım 1: Gerekli Ad Alanlarını İçe Aktarın

Aspose.Imaging ile çalışmak için gerekli ad alanlarını içe aktarmanız gerekir:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Adım 2: Görüntüleri Yükleyin

- Öncelikle SVG tuvaline çizmek istediğiniz raster görüntüyü yükleyin.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Daha sonra raster resmi çizmek istediğiniz SVG tuval resmini yükleyin.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Adım 3: SVG Görüntüsüne Çizim

Şimdi, mevcut SVG resminin üzerine çizim yapmaya başlayabilirsiniz. Bunu yapmak için, bir örnek oluşturmanız gerekir `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Adım 4: Raster Görüntüyü Çizin

- Raster görüntüyü çizmek istediğiniz sınırları tanımlayın ve raster görüntüden kaynak bölgeyi belirtin.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Adım 5: Sonucu Kaydedin

Raster görüntüyü SVG tuvaline çizdikten sonra ortaya çıkan görüntüyü kaydedebilirsiniz:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Çözüm

Tebrikler! Aspose.Imaging for .NET kullanarak bir SVG tuvaline başarılı bir şekilde raster resim çizdiniz. Bu, .NET uygulamalarınızda zengin ve dinamik resimler oluşturmak için inanılmaz derecede faydalı olabilir.

Daha fazla bilgi ve ayrıntılı belgeler için şu adresi ziyaret edin: [Aspose.Imaging for .NET belgeleri](https://reference.aspose.com/imaging/net/).

## Sıkça Sorulan Sorular

### Aspose.Imaging for .NET nedir?
   Aspose.Imaging for .NET, geliştiricilerin .NET uygulamaları içerisinde çeşitli formatlardaki görüntüleri oluşturmalarına, düzenlemelerine ve dönüştürmelerine olanak tanıyan güçlü bir görüntü işleme kütüphanesidir.

### Aspose.Imaging for .NET'i ticari projelerde kullanabilir miyim?
   Evet, Aspose.Imaging for .NET'i hem ticari hem de ticari olmayan projelerde kullanabilirsiniz. Lisanslama ayrıntıları şu adreste bulunabilir: [satın alma sayfası](https://purchase.aspose.com/buy).

### Ücretsiz deneme imkanı var mı?
   Evet, Aspose.Imaging for .NET'in ücretsiz deneme sürümünü şu adresten edinebilirsiniz: [Burada](https://releases.aspose.com/).

### Nereden destek alabilirim veya soru sorabilirim?
   Herhangi bir sorunuz varsa veya desteğe ihtiyacınız varsa, şu adresi ziyaret edebilirsiniz: [Aspose.Görüntüleme forumu](https://forum.aspose.com/).

### Aspose.Imaging for .NET için geçici lisansı nasıl alabilirim?
   Geçici lisansı şuradan alabilirsiniz: [Burada](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}