---
title: Aspose.Imaging for .NET ile EMF'de Raster Görüntüler Çizin
linktitle: Aspose.Imaging for .NET'te EMF'de Raster Görüntü Çizin
second_title: Aspose.Imaging .NET Görüntü İşleme API'si
description: Aspose.Imaging for .NET'i kullanarak EMF dosyalarında raster görüntülerin nasıl çizileceğini öğrenin. Çarpıcı görselleri zahmetsizce oluşturun.
weight: 10
url: /tr/net/vector-image-processing/draw-raster-image-on-emf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET ile EMF'de Raster Görüntüler Çizin


## giriiş

Aspose.Imaging for .NET kullanarak EMF (Gelişmiş Meta Dosyası) üzerinde raster görüntünün nasıl çizileceğini anlatan bu adım adım eğitime hoş geldiniz. Aspose.Imaging, .NET uygulamalarınızda çeşitli görüntü formatlarıyla çalışmanıza olanak tanıyan güçlü bir kütüphanedir. Bu eğitimde, bir EMF dosyasına raster görüntü çizme sürecinde size rehberlik edeceğiz. Gerekli ad alanlarını nasıl içe aktaracağınızı öğreneceksiniz ve öğrenme sürecini kolaylaştırmak için her örneği birden çok adıma ayıracağız.

Başlayalım!

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulları yerine getirmelisiniz:

1. Visual Studio: .NET kodunu yazıp çalıştırabilmeniz için bilgisayarınızda Visual Studio'nun kurulu olması gerekmektedir.

2.  Aspose.Imaging for .NET: Aspose.Imaging for .NET'in kurulu olduğundan emin olun. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/imaging/net/).

3. Raster Görüntü: EMF dosyasına çizmek istediğiniz bir taramalı görüntü (örneğin PNG dosyası) hazırlayın.

## Ad Alanlarını İçe Aktar

Aspose.Imaging ile çalışmak için Visual Studio projenizde gerekli ad alanlarını içe aktarmanız gerekecektir. Aşağıdaki ad alanlarını kod dosyanıza ekleyin:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Emf;
using Aspose.Imaging.FileFormats.Png;
using Aspose.Imaging.Graphics;
using System;
```

Artık önkoşulları ve ad alanlarını oluşturduğumuza göre, örneği birden çok adıma ayıralım.

## Adım 1: Çizilecek Resmi Yükleyin

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
{
    // 1. Adım kodunuz buraya gelecek
}
```

 Bu adımda çizmek istediğiniz raster görseli EMF dosyası üzerine yüklüyoruz. Yer değiştirmek`"Your Document Directory"` resminizin yolu ile.

## Adım 2: EMF Çizim Yüzeyini Yükleyin

```csharp
using (EmfImage canvasImage = (EmfImage)Image.Load(dataDir + "input.emf"))
{
    // 2. Adım kodunuz buraya gelecek
}
```

 Burada görselimiz için çizim yüzeyi görevi görecek EMF dosyasını yüklüyoruz. Değiştirdiğinizden emin olun`"input.emf"` EMF dosyanızın yolu ile birlikte.

## 3. Adım: Bir EMF Kaydedici Grafiği Oluşturun

```csharp
EmfRecorderGraphics2D graphics = EmfRecorderGraphics2D.FromEmfImage(canvasImage);
```

 Bu adımda örneğini oluşturuyoruz.`EmfRecorderGraphics2D` EMF görüntüsünden. Bu bize çizim işlemlerini kaydetmemizi sağlar.

## Adım 4: Raster Görüntüyü Çizin

```csharp
graphics.DrawImage(
    imageToDraw,
    new Rectangle(67, 67, canvasImage.Width, canvasImage.Height),
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    GraphicsUnit.Pixel);
```

 Bu adımda şunu kullanıyoruz:`DrawImage`Yüklenen taramalı görüntüyü EMF dosyasına çizme yöntemini kullanın. Çizilen görüntünün konumunu ve boyutunu kontrol etmek için kaynak ve hedef dikdörtgenleri belirtebilirsiniz.

## Adım 5: Sonuç Resmini Kaydedin

```csharp
using (EmfImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "input.DrawImage.emf");
}
```

 Son olarak, ortaya çıkan EMF görüntüsünü çizilen raster görüntüyle birlikte bir dosyaya kaydediyoruz. Dosya, belirtilen dizine "input.DrawImage.emf" adıyla kaydedilecektir.`dataDir`.

Tebrikler! Aspose.Imaging for .NET'i kullanarak EMF dosyası üzerine başarılı bir şekilde taramalı görüntü çizdiniz. İstenilen etkileri elde etmek için farklı kaynak ve hedef dikdörtgenleri keşfetmekten ve denemekten çekinmeyin.

## Çözüm

Bu eğitimde, Aspose.Imaging for .NET'i kullanarak EMF dosyasına taramalı görüntü çizmeyi öğrendik. Adım adım kılavuzu takip ederek bu işlevselliği .NET uygulamalarınıza kolayca entegre edebilirsiniz.

Aspose.Imaging ile etkileyici görüntüler oluşturmanın tadını çıkarın!

## SSS

### 1. Aynı EMF dosyasına birden fazla resim çizebilir miyim?

Evet, çizim işlemini farklı kaynak ve hedef dikdörtgenlerle tekrarlayarak aynı EMF dosyasına birden fazla görüntü çizebilirsiniz.

### 2. Aspose.Imaging .NET Core ile uyumlu mu?

Evet, Aspose.Imaging for .NET hem .NET Framework hem de .NET Core ile uyumludur.

### 3. Çizilen görüntüye döndürme veya ölçeklendirme gibi dönüşümleri nasıl uygulayabilirim?

 Kaynak ve hedef dikdörtgenleri değiştirerek dönüşümleri uygulayabilirsiniz.`DrawImage` yöntem.

### 4. EMF dosyasına vektör grafikleri de çizebilir miyim?

Evet, Aspose.Imaging for .NET'i kullanarak raster görsellerin yanı sıra vektör grafikleri ve şekiller de çizebilirsiniz.

### 5. Aspose.Imaging için nereden destek alabilirim?

 Destek ve yardım için Aspose.Imaging forumunu ziyaret edebilirsiniz.[Burada](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
