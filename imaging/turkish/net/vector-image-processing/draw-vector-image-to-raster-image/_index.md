---
title: Aspose.Imaging for .NET'te Vektör Görüntüsünü Raster Görüntüye Çizin
linktitle: Aspose.Imaging for .NET'te Vektör Görüntüsünü Raster Görüntüye Çizin
second_title: Aspose.Imaging .NET Görüntü İşleme API'si
description: Aspose.Imaging'i kullanarak vektör görüntülerini .NET'te raster görüntülere nasıl dönüştüreceğinizi öğrenin. Verimli görüntü işleme için adım adım kılavuz.
weight: 13
url: /tr/net/vector-image-processing/draw-vector-image-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET'te Vektör Görüntüsünü Raster Görüntüye Çizin


.NET uygulamalarınızda vektör görüntülerini zahmetsizce raster görüntülere dönüştürmek mi istiyorsunuz? Aspose.Imaging for .NET bu görev için etkili bir çözüm sunar. Bu adım adım kılavuzda, Aspose.Imaging for .NET kullanarak vektör görüntülerini raster görüntülere dönüştürme sürecinde size yol göstereceğiz. 

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

### 1. Aspose.Imaging for .NET

 Aspose.Imaging for .NET'in kurulu olması gerekir. Eğer elinizde yoksa, adresindeki web sitesinden indirebilirsiniz.[Aspose.Imaging for .NET'i indirin](https://releases.aspose.com/imaging/net/).

### 2. .NET Geliştirme Ortamı

Bilgisayarınızda bir .NET geliştirme ortamının kurulu olduğundan emin olun. Visual Studio'yu veya başka herhangi bir .NET geliştirme aracını kullanabilirsiniz.

Şimdi vektör görüntülerini raster görüntülere dönüştürme işlemini basit, takip edilmesi kolay adımlara ayıralım:

## 1. Adım: Projenizi Başlatın

Geliştirme ortamınızda yeni bir .NET projesi oluşturarak başlayın. Aspose.Imaging for .NET'in projenize entegre olduğundan emin olun.

## Adım 2: Vektör Görüntüsünü Yükleyin

Bu adımda raster görsele dönüştürmek istediğiniz vektör görseli (SVG formatında) yüklüyoruz.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## Adım 3: Vektör Görüntüsünü Rasterleştirin

Şimdi SVG görüntüsünü PNG formatına rasterleştirmemiz gerekiyor. Vektörden raster'a dönüşümün gerçekleştiği yer burasıdır.

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## Adım 4: Raster Görüntüyü Yükleyin

Rasterleştirmeden sonra, daha fazla çizim için PNG görüntüsünü akıştan yükleyin.

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## Adım 5: Raster Görüntüyü Çizin

Artık taramalı görüntüyü mevcut SVG görüntüsünün üzerine çizebiliriz.

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## Adım 6: Sonucu Kaydet

Son olarak sonuç resmini kaydedin. Artık vektör görüntünüzü içeren bir raster görüntünüz var.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## Çözüm

Bu derste Aspose.Imaging for .NET kullanarak vektör görüntülerin raster görüntülere nasıl dönüştürüleceğini gösterdik. Bu basit adımlarla bu işlevselliği .NET uygulamalarınıza zahmetsizce entegre edebilirsiniz.

### Sıkça Sorulan Sorular

### Aspose.Imaging for .NET nedir?
Aspose.Imaging for .NET, çeşitli görüntü formatlarıyla çalışma, görüntüleri dönüştürme ve gelişmiş görüntü işleme görevlerini gerçekleştirme gibi güçlü görüntü işleme özellikleri sağlayan bir .NET kitaplığıdır.

### Aspose.Imaging for .NET belgelerini nerede bulabilirim?
 Aspose.Imaging for .NET belgelerini bulabilirsiniz[Burada](https://reference.aspose.com/imaging/net/).

### Ücretsiz deneme sürümü mevcut mu?
 Evet, Aspose.Imaging for .NET'in ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### Aspose.Imaging for .NET için nasıl geçici lisans alabilirim?
 Geçici bir lisansa ihtiyacınız varsa bir tane alabilirsiniz.[Burada](https://purchase.aspose.com/temporary-license/).

### Aspose.Imaging for .NET için nereden destek alabilirim?
 Her türlü destek veya sorularınız için şu adresi ziyaret edebilirsiniz:[Aspose.Görüntüleme forumu](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
