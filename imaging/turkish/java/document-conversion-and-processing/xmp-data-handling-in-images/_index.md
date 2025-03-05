---
title: Aspose.Imaging for Java ile Görüntülerde XMP Verilerinin Kullanımı
linktitle: Görüntülerde XMP Veri İşleme
second_title: Aspose.Imaging Java Görüntü İşleme API'si
description: Aspose.Imaging for Java kullanarak görüntülerdeki XMP meta verilerini nasıl işleyeceğinizi öğrenin. Görüntü dosyalarınızı geliştirmek için meta verileri gömün ve alın.
type: docs
weight: 16
url: /tr/java/document-conversion-and-processing/xmp-data-handling-in-images/
---
Aspose.Imaging for Java, çeşitli formatlardaki görüntülerle çalışmak için çok yönlü ve güçlü bir kütüphanedir. Bu eğitim, Aspose.Imaging for Java kullanarak görüntülerdeki XMP (Genişletilebilir Meta Veri Platformu) verilerini işleme sürecinde size rehberlik edecektir. XMP, meta verileri görüntü dosyalarına gömmeye yönelik bir standarttır; yazar, açıklama ve daha fazlası gibi değerli bilgileri saklamanıza olanak tanır.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Bilgisayarınızda kurulmuş bir Java geliştirme ortamı.
-  Aspose.Imaging for Java kütüphanesi kuruldu. adresinden indirebilirsiniz.[Aspose.Imaging for Java web sitesi](https://releases.aspose.com/imaging/java/).
- Java programlamanın temel anlayışı.

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

Şimdi örneği adım adım kılavuza ayıralım:

## Adım 1: Görüntü Boyutunu ve Tiff Seçeneklerini Belirleyin

Öncelikle görselinizin saklanacağı dizini tanımlayın ve görselin boyutunu belirtmek için bir Dikdörtgen oluşturun. Bu örnekte belirli seçeneklere sahip bir Tiff görüntüsü kullanıyoruz.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## 2. Adım: Yeni Bir Görüntü Oluşturun

Şimdi belirtilen seçeneklerle yeni bir resim oluşturun. Bu görüntü XMP meta verilerini depolamak için kullanılacaktır.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## 3. Adım: XMP Başlığı ve Fragmanı Oluşturun

XMP meta verileriniz için XMP-Header ve XMP-Trailer örneklerini oluşturun. Bu başlıklar ve fragmanlar meta veri yapısını tanımlamaya yardımcı olur.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## 4. Adım: XMP Meta Bilgilerini Oluşturun

Şimdi farklı nitelikleri ayarlamak için bir XMP meta örneği oluşturun. Yazar ve açıklama gibi bilgileri ekleyebilirsiniz.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Adım 5: XMP Paket Sarmalayıcı Oluşturun

XMP üstbilgisini, fragmanını ve meta bilgilerini içeren bir XmpPacketWrapper örneği oluşturun.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Adım 6: Photoshop Paketini Ekleyin

Photoshop'a özgü bilgileri depolamak için bir Photoshop paketi oluşturun ve şehir, ülke ve renk modu gibi özelliklerini ayarlayın. Daha sonra bu paketi XMP meta verilerine ekleyin.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## Adım 7: Dublin Çekirdek Paketini Ekleyin

Yazar, başlık ve ek değerler gibi daha genel bilgiler için bir DublinCore paketi oluşturun ve niteliklerini ayarlayın. Bu paketi XMP meta verilerine de ekleyin.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## 8. Adım: Görüntüdeki XMP Meta Verilerini Güncelleyin

 kullanarak XMP meta verilerini görüntüye güncelleyin.`setXmpData` yöntem.

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

Görüntüden XMP meta verilerini almak için görüntüyü bellek akışından veya diskten yükleyin ve XMP verilerine erişin.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Paket verilerini kullan...
        }
    }
}
```

Tebrikler! Aspose.Imaging for Java'yı kullanarak görüntülerdeki XMP verilerinin nasıl işleneceğini başarıyla öğrendiniz. Bu, görüntü dosyalarınızdaki değerli meta verileri saklamanıza ve almanıza olanak tanır.

## Çözüm

Bu eğitimde Aspose.Imaging for Java kullanarak görüntülerde XMP meta verileriyle nasıl çalışılacağını araştırdık. Adım adım kılavuzu takip ederek meta verileri görüntü dosyalarınıza kolayca gömebilir ve alabilirsiniz, böylece bilgilerini ve kullanılabilirliğini artırabilirsiniz.

## SSS'ler

### S1: XMP meta verileri nedir?

Cevap1: XMP (Genişletilebilir Meta Veri Platformu), meta verileri görüntüler de dahil olmak üzere çeşitli dosya türlerine yerleştirmeye yönelik bir standarttır. Yazar, başlık, açıklama ve daha fazlası gibi bilgileri dosyanın kendisinde saklamanıza olanak tanır.

### S2: XMP meta verileri neden önemlidir?

Cevap2: XMP meta verileri, dijital varlıkları düzenlemek ve kategorize etmek için gereklidir. Sahipliğin atfedilmesine, içeriğin açıklanmasına ve görseller gibi dosyalara bağlam eklenmesine yardımcı olarak onları daha erişilebilir ve anlamlı hale getirir.

### S3: XMP meta verilerini bir görüntüye yerleştirdikten sonra düzenleyebilir miyim?

C3: Evet, XMP meta verilerini bir görüntüye yerleştirdikten sonra düzenleyebilirsiniz. Aspose.Imaging for Java, meta veri niteliklerini gerektiği gibi değiştirmek ve güncellemek için araçlar sağlar.

### S4: Aspose.Imaging for Java ücretsiz bir araç mıdır?

 Cevap4: Aspose.Imaging for Java ücretsiz bir deneme sürümü sunuyor ancak tam işlevsellik ve genişletilmiş kullanım için ücretli bir lisans gereklidir. Üzerindeki seçenekleri inceleyebilirsiniz.[Aspose.Imaging for Java web sitesi](https://purchase.aspose.com/buy).

### S5: Aspose.Imaging for Java için nereden yardım ve destek alabilirim?

 Cevap5: Aspose.Imaging for Java ile ilgili herhangi bir sorunla karşılaşırsanız veya sorularınız varsa, şu adresi ziyaret edebilirsiniz:[Aspose.Görüntüleme forumları](https://forum.aspose.com/) topluluk desteği ve rehberlik için.



## Kaynak Kodunu Tamamlayın
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Bir Dikdörtgen tanımlayarak görüntünün boyutunu belirtin
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// yalnızca örnek amaçlı olarak yepyeni bir görüntü oluşturun
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// XMP-Header'ın bir örneğini oluşturun
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// Xmp-TrailerPi'nin bir örneğini oluşturun
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// farklı nitelikleri ayarlamak için XMP meta sınıfının bir örneğini oluşturun
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	//tüm meta verileri içeren bir XmpPacketWrapper örneği oluşturun
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// Photoshop paketinin bir örneğini oluşturun ve photoshop niteliklerini ayarlayın
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// photoshop paketini XMP meta verilerine ekleyin
	xmpData.addPackage(photoshopPackage);
	// DublinCore paketinin bir örneğini oluşturun ve dublinCore niteliklerini ayarlayın
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// dublinCore Paketini XMP meta verilerine ekleyin
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// XMP meta verilerini görüntüye güncelleme
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
			// Paket verilerini kullan...
		}
	}
}
        
```