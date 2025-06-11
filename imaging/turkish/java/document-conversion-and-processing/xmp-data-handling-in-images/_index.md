---
"description": "Aspose.Imaging for Java kullanarak resimlerdeki XMP meta verilerinin nasıl işleneceğini öğrenin. Resim dosyalarınızı geliştirmek için meta verileri gömün ve alın."
"linktitle": "Görüntülerde XMP Veri İşleme"
"second_title": "Aspose.Imaging Java Görüntü İşleme API'si"
"title": "Aspose.Imaging for Java ile Görüntülerde XMP Veri İşleme"
"url": "/tr/java/document-conversion-and-processing/xmp-data-handling-in-images/"
"weight": 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java ile Görüntülerde XMP Veri İşleme

Aspose.Imaging for Java, çeşitli formatlardaki resimlerle çalışmak için çok yönlü ve güçlü bir kütüphanedir. Bu eğitim, Aspose.Imaging for Java kullanarak resimlerdeki XMP (Genişletilebilir Meta Veri Platformu) verilerini işleme sürecinde size rehberlik edecektir. XMP, resim dosyalarına meta veri yerleştirmek için bir standarttır ve yazar, açıklama ve daha fazlası gibi değerli bilgileri depolamanıza olanak tanır.

## Ön koşullar

Başlamadan önce aşağıdaki ön koşulların mevcut olduğundan emin olun:

- Bilgisayarınızda kurulu bir Java geliştirme ortamı.
- Java kütüphanesi için Aspose.Imaging yüklendi. Bunu şuradan indirebilirsiniz: [Java web sitesi için Aspose.Imaging](https://releases.aspose.com/imaging/java/).
- Java programlamanın temellerini anlamak.

## Paketleri İçe Aktarma

Gerekli paketleri Java projenize aktararak başlayın. Kodunuzun başına aşağıdaki içe aktarma ifadelerini ekleyebilirsiniz:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.xmp.XmpPackage;
import com.aspose.imaging.xmp.XmpPacketWrapper;
import com.aspose.imaging.xmp.XmpMeta;
import com.aspose.imaging.xmp.photoshop.ColorMode;
import com.aspose.imaging.xmp.photoshop.PhotoshopPackage;
import com.aspose.imaging.xmp.dc.DublinCorePackage;
import com.aspose.imaging.xmp.header.XmpHeaderPi;
import com.aspose.imaging.xmp.trailer.XmpTrailerPi;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Şimdi örneği adım adım açıklayalım:

## Adım 1: Görüntü Boyutunu ve Tiff Seçeneklerini Belirleyin

Öncelikle, görüntünüzün depolanacağı dizini tanımlayın ve görüntünün boyutunu belirtmek için bir Dikdörtgen oluşturun. Bu örnekte, belirli seçeneklere sahip bir Tiff görüntüsü kullanıyoruz.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## Adım 2: Yeni Bir Görüntü Oluşturun

Şimdi belirtilen seçeneklerle yeni bir görüntü oluşturun. Bu görüntü XMP meta verilerini depolamak için kullanılacaktır.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## Adım 3: XMP Başlığı ve Fragmanı Oluşturun

XMP meta verileriniz için XMP-Header ve XMP-Trailer örnekleri oluşturun. Bu başlıklar ve fragmanlar meta veri yapısını tanımlamaya yardımcı olur.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Adım 4: XMP Meta Bilgilerini Oluşturun

Şimdi, farklı öznitelikler ayarlamak için bir XMP meta örneği oluşturun. Yazar ve açıklama gibi bilgiler ekleyebilirsiniz.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Adım 5: XMP Paket Sarmalayıcısını Oluşturun

XMP başlığını, fragmanını ve meta bilgilerini içeren bir XmpPacketWrapper örneği oluşturun.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Adım 6: Photoshop Paketini Ekleyin

Photoshop'a özgü bilgileri depolamak için bir Photoshop paketi oluşturun ve şehir, ülke ve renk modu gibi niteliklerini ayarlayın. Ardından, bu paketi XMP meta verilerine ekleyin.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## Adım 7: Dublin Core Paketini Ekleyin

Yazar, başlık ve ek değerler gibi daha genel bilgiler için bir DublinCore paketi oluşturun ve özniteliklerini ayarlayın. Bu paketi XMP meta verilerine de ekleyin.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## Adım 8: Görüntüdeki XMP Meta Verilerini Güncelleyin

XMP meta verilerini görüntüye güncelleyin `setXmpData` yöntem.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## Adım 9: Görüntüyü Kaydedin

Artık görüntüyü gömülü XMP meta verileriyle birlikte diske veya bir bellek akışına kaydedebilirsiniz.

```java
    image.save(ms);
```

## Adım 10: Görüntüyü Yükleyin ve XMP Meta Verilerini Alın

Görüntüden XMP meta verilerini almak için, görüntüyü bellek akışından veya diskten yükleyin ve XMP verilerine erişin.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Paket verilerini kullan ...
        }
    }
}
```

Tebrikler! Aspose.Imaging for Java kullanarak resimlerdeki XMP verilerini nasıl işleyeceğiniz konusunda başarılı bir şekilde bilgi edindiniz. Bu, resim dosyalarınızda değerli meta verileri depolamanıza ve geri almanıza olanak tanır.

## Çözüm

Bu eğitimde, Aspose.Imaging for Java kullanarak resimlerdeki XMP meta verileriyle nasıl çalışılacağını inceledik. Adım adım kılavuzu izleyerek, resim dosyalarınıza meta verileri kolayca yerleştirebilir ve alabilir, bilgilerini ve kullanılabilirliklerini artırabilirsiniz.

## SSS

### S1: XMP meta verisi nedir?

A1: XMP (Genişletilebilir Meta Veri Platformu), resimler de dahil olmak üzere çeşitli dosya türlerine meta veri yerleştirmek için bir standarttır. Yazar, başlık, açıklama ve daha fazlası gibi bilgileri dosyanın kendisinde depolamanıza olanak tanır.

### S2: XMP meta verileri neden önemlidir?

A2: XMP meta verileri, dijital varlıkları düzenlemek ve kategorilere ayırmak için önemlidir. Sahipliği atfetmeye, içeriği tanımlamaya ve resimler gibi dosyalara bağlam eklemeye yardımcı olur, bunları daha erişilebilir ve anlamlı hale getirir.

### S3: XMP meta verilerini bir görüntüye yerleştirdikten sonra düzenleyebilir miyim?

C3: Evet, XMP meta verilerini bir görüntüye yerleştirdikten sonra düzenleyebilirsiniz. Java için Aspose.Imaging, meta veri özniteliklerini gerektiği gibi değiştirmek ve güncellemek için araçlar sağlar.

### S4: Aspose.Imaging for Java ücretsiz bir araç mıdır?

A4: Aspose.Imaging for Java ücretsiz deneme sürümü sunar, ancak tam işlevsellik ve genişletilmiş kullanım için ücretli bir lisans gerekir. Seçenekleri şu adreste inceleyebilirsiniz: [Java web sitesi için Aspose.Imaging](https://purchase.aspose.com/buy).

### S5: Aspose.Imaging for Java için yardım ve desteği nereden alabilirim?

C5: Aspose.Imaging for Java ile ilgili herhangi bir sorunla karşılaşırsanız veya sorularınız varsa, şu adresi ziyaret edebilirsiniz: [Aspose.Görüntüleme forumları](https://forum.aspose.com/) Topluluk desteği ve rehberliği için.



## Tam Kaynak Kodu
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Bir Dikdörtgen tanımlayarak görüntünün boyutunu belirtin
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// sadece örnek amaçlı yepyeni bir görüntü oluşturun
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// XMP-Header'ın bir örneğini oluştur
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// Xmp-TrailerPi'nin bir örneğini oluşturun
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// farklı öznitelikler ayarlamak için XMP meta sınıfının bir örneğini oluşturun
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// tüm meta verileri içeren bir XmpPacketWrapper örneği oluşturun
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// Photoshop paketinin bir örneğini oluşturun ve photoshop niteliklerini ayarlayın
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// photoshop paketini XMP meta verilerine ekle
	xmpData.addPackage(photoshopPackage);
	// DublinCore paketinin bir örneğini oluşturun ve dublinCore özniteliklerini ayarlayın
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// dublinCore Paketini XMP meta verilerine ekleyin
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// XMP meta verilerini görüntüye güncelle
	image.setXmpData(xmpData);
	// Görüntüyü diske veya bellek akışına kaydedin
	image.save(ms);
	// Meta verileri okumak/almak için görüntüyü bellek akışından veya diskten yükleyin
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// XMP meta verilerini alma
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Paket verilerini kullan ...
		}
	}
}
        
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}