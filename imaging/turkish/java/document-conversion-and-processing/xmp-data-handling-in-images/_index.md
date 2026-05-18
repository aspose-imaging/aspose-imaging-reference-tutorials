---
date: 2026-05-18
description: Java görüntü işleme kütüphanesi Aspose.Imaging'i kullanarak görüntülere
  XMP meta verilerini eklemeyi ve almaya yönelik adım adım kodlarla nasıl yapılacağını
  öğrenin.
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: Görüntülerde XMP Veri İşleme
schemas:
- author: Aspose
  dateModified: '2026-05-18'
  description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  headline: 'Java Image Processing Library: XMP with Aspose.Imaging'
  type: TechArticle
- description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  name: 'Java Image Processing Library: XMP with Aspose.Imaging'
  steps:
  - name: Specify Image Size and Tiff Options
    text: First, define the directory where your image will be stored and create a
      `Rectangle` to specify the size of the image. In this example, we use a TIFF
      image with certain options. `TiffOptions` configures format‑specific settings
      for the TIFF image.
  - name: Create a New Image
    text: Now, create a new image with the specified options. This image will be used
      to store the XMP metadata. `TiffImage` represents a TIFF image object, and `TiffFrame`
      defines an individual frame within it.
  - name: Create XMP Header and Trailer
    text: Create instances of XMP‑Header and XMP‑Trailer for your XMP metadata. These
      headers and trailers help define the metadata structure. `XmpHeaderPi` and `XmpTrailerPi`
      represent the XMP packet’s opening and closing sections.
  - name: Create XMP Meta Information
    text: Now, create an instance of XMP meta to set different attributes. You can
      add information like the author and description. `XmpMeta` holds the core metadata
      fields such as author and description.
  - name: Create XMP Packet Wrapper
    text: '`XmpPacketWrapper` is the container that holds the XMP header, trailer,
      and meta information in a single packet. It ensures the packet conforms to the
      XMP specification. `XmpPacketWrapper` packages the header, meta, and trailer
      into a single XMP packet.'
  - name: Add Photoshop Package
    text: To store Photoshop‑specific information, create a Photoshop package and
      set its attributes, such as city, country, and color mode. Then, add this package
      to the XMP metadata. `PhotoshopPackage` stores Photoshop‑specific metadata like
      city, country, and color mode.
  - name: Add Dublin Core Package
    text: For more general information, like author, title, and additional values,
      create a DublinCore package and set its attributes. Add this package to the
      XMP metadata as well. `DublinCorePackage` contains standard Dublin Core fields
      such as title, creator, and keywords.
  - name: Update XMP Metadata in the Image
    text: Update the XMP metadata into the image using the `setXmpData` method. This
      call writes the XMP packet into the image’s metadata section. `setXmpData` writes
      the XMP packet into the image’s metadata section.
  - name: Save the Image
    text: You can now save the image with the embedded XMP metadata on the disk or
      in a memory stream.
  - name: Load the Image and Retrieve XMP Metadata
    text: To retrieve the XMP metadata from the image, load the image from the memory
      stream or disk and access the XMP data via the `getXmpData` method. `getXmpData`
      reads the embedded XMP packet from the image. Congratulations! You've successfully
      learned how to handle XMP data in images using Aspose.Imagin
  type: HowTo
- questions:
  - answer: XMP is an XML‑based standard for embedding descriptive information directly
      inside files, enabling consistent metadata across applications.
    question: What is XMP metadata?
  - answer: It lets you tag images with author, copyright, keywords, and custom data,
      improving searchability and asset management without external databases.
    question: Why is XMP metadata important?
  - answer: Yes, Aspose.Imaging for Java provides methods to modify existing XMP packets
      and write them back to the file.
    question: Can I edit XMP metadata after embedding it in an image?
  - answer: A free trial is available for evaluation, but a paid license is required
      for production use. You can explore options on the [Aspose.Imaging for Java
      website](https://purchase.aspose.com/buy).
    question: Is Aspose.Imaging for Java a free tool?
  - answer: Visit the [Aspose.Imaging forums](https://forum.aspose.com/) for community
      assistance, or contact Aspose support directly for paid‑license customers.
    question: Where can I get help and support for Aspose.Imaging for Java?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: 'Java Görüntü İşleme Kütüphanesi: XMP with Aspose.Imaging'
url: /tr/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Java için Aspose.Imaging ile Görsellerde XMP Veri İşleme

Aspose.Imaging bir **java image processing library**'dir ve onlarca raster ve vektör formatı ile çalışmanıza olanak tanır. Bu öğreticide, Aspose.Imaging for Java kullanarak görsellere XMP (Extensible Metadata Platform) verisini nasıl gömeceğinizi ve geri alacağınızı öğreneceksiniz. Sonunda, yazar, açıklama ve özel meta verileri doğrudan görüntü dosyalarınıza depolayabilecek, böylece dosyalar aranabilir ve kendini tanımlayan hâle gelecektir.

## Hızlı Yanıtlar
- **XMP nedir?** XMP, görüntüler, PDF'ler ve videolar gibi dosyalar içinde meta veriyi gömmek için standartlaştırılmış bir XML‑tabanlı formattır.  
- **Java'da XMP'yi hangi kütüphane yönetir?** Aspose.Imaging for Java, XMP paketlerini okuma ve yazma için eksiksiz bir API sağlar.  
- **Lisans gerekir mi?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari bir lisans gereklidir.  
- **Kaç tane görüntü formatı destekleniyor?** TIFF, JPEG, PNG, PSD ve RAW dahil olmak üzere 150'den fazla format.  
- **Büyük görüntüleri işleyebilir miyim?** Evet – kütüphane, tüm görüntüyü belleğe yüklemeden 2 GB'a kadar dosyaları işleyebilir.

## XMP meta verisi nedir?
XMP meta verisi, tanımlayıcı bilgileri doğrudan dijital dosyalara gömen bir XML‑tabanlı standarttır. Yazar, telif hakkı, anahtar kelimeler ve özel verilerin uygulamalar arasında tutarlı bir şekilde depolanmasını sağlar. XML olduğu için, XMP özel ad alanlarıyla genişletilebilir; bu sayede geliştiriciler, temel şemayı anlayan araçlarla uyumlu kalırken, kendi alanlarını ekleyebilir. Bu, XMP'yi uzun vadeli varlık yönetimi ve uygulamalar arası birlikte çalışabilirlik için ideal kılar.

## XMP için neden bir Java görüntü işleme kütüphanesi kullanmalı?
Aspose.Imaging for Java, **150+ image formats** destekler ve çok gigabaytlık dosyaları akış (streaming) şeklinde işleyebilir, bu da bellek tüketimini naif yüklemeye göre %80'e kadar azaltır. API ayrıca XMP paketlerinin standartlara uygun kalmasını garanti eder, böylece Adobe Photoshop, Lightroom ve diğer araçlarla uyumluluk sağlanır.

## Önkoşullar

Başlamadan önce, aşağıdaki önkoşulların karşılandığından emin olun:

- Bilgisayarınızda bir Java geliştirme ortamı kurulu.  
- Aspose.Imaging for Java kütüphanesi yüklü. Bunu [Aspose.Imaging for Java website](https://releases.aspose.com/imaging/java/) adresinden indirebilirsiniz.  
- Java programlamaya temel bir anlayış.

## Paketleri İçe Aktarma

Java projenize gerekli paketleri içe aktararak başlayın. Aşağıdaki import ifadelerini kodunuzun başına ekleyebilirsiniz:

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

Şimdi, örneği adım adım bir kılavuza ayıralım:

## Java görüntü işleme kütüphanesi kullanarak XMP meta verisini nasıl gömebilirsiniz?

Görselinizi yükleyin, bir XMP paketi oluşturun, paketi görsele ekleyin ve kaydedin – hepsi birkaç kısa satırda. Aspose.Imaging'in `setXmpData` yöntemi, paketi ayrı bir meta veri dosyasına ihtiyaç duymadan doğrudan dosyaya yazar. İşlem, dosya tabanlı ve akış tabanlı görsellerde çalışır, bu da web hizmetleri ve toplu işler için uygundur.

### Adım 1: Görüntü Boyutunu ve Tiff Seçeneklerini Belirleme

İlk olarak, görselinizin saklanacağı dizini tanımlayın ve görüntünün boyutunu belirtmek için bir `Rectangle` oluşturun. Bu örnekte belirli seçeneklerle bir TIFF görseli kullanıyoruz. `TiffOptions`, TIFF görseli için format‑özel ayarları yapılandırır.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### Adım 2: Yeni Bir Görüntü Oluşturma

Şimdi, belirtilen seçeneklerle yeni bir görsel oluşturun. Bu görsel, XMP meta verisini depolamak için kullanılacak. `TiffImage` bir TIFF görsel nesnesini temsil eder ve `TiffFrame` içinde tek bir çerçeveyi tanımlar.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### Adım 3: XMP Başlığı ve Sonlandırıcısını Oluşturma

XMP meta veriniz için XMP‑Header ve XMP‑Trailer örnekleri oluşturun. Bu başlıklar ve sonlandırıcılar meta veri yapısını tanımlamaya yardımcı olur. `XmpHeaderPi` ve `XmpTrailerPi`, XMP paketinin açılış ve kapanış bölümlerini temsil eder.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### Adım 4: XMP Meta Bilgisi Oluşturma

Şimdi, farklı özellikleri ayarlamak için bir XMP meta örneği oluşturun. Yazar ve açıklama gibi bilgileri ekleyebilirsiniz. `XmpMeta`, yazar ve açıklama gibi temel meta veri alanlarını tutar.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### Adım 5: XMP Paket Sarmalayıcısını Oluşturma

`XmpPacketWrapper`, XMP başlığını, sonlandırıcısını ve meta bilgisini tek bir paket içinde tutan kapsayıcıdır. Paketin XMP spesifikasyonuna uygun olmasını sağlar. `XmpPacketWrapper`, başlık, meta ve sonlandırıcıyı tek bir XMP paketinde birleştirir.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### Adım 6: Photoshop Paketi Ekleme

Photoshop‑özel bilgileri depolamak için bir Photoshop paketi oluşturun ve şehir, ülke ve renk modu gibi özelliklerini ayarlayın. Ardından bu paketi XMP meta verisine ekleyin. `PhotoshopPackage`, şehir, ülke ve renk modu gibi Photoshop‑özel meta verileri saklar.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### Adım 7: Dublin Core Paketi Ekleme

Yazar, başlık ve ek değerler gibi daha genel bilgiler için bir DublinCore paketi oluşturun ve özelliklerini ayarlayın. Bu paketi de XMP meta verisine ekleyin. `DublinCorePackage`, başlık, yaratıcı ve anahtar kelimeler gibi standart Dublin Core alanlarını içerir.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### Adım 8: Görüntüde XMP Meta Verisini Güncelleme

`setXmpData` yöntemiyle XMP meta verisini görüntüye güncelleyin. Bu çağrı, XMP paketini görüntünün meta veri bölümüne yazar. `setXmpData`, XMP paketini görüntünün meta veri bölümüne yazar.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### Adım 9: Görüntüyü Kaydetme

Artık XMP meta verisi gömülü görüntüyü diske ya da bir bellek akışına kaydedebilirsiniz.

```java
    image.save(ms);
```

### Adım 10: Görüntüyü Yükleyip XMP Meta Verisini Almak

Görselden XMP meta verisini almak için, görüntüyü bellek akışından ya da diskten yükleyin ve `getXmpData` yöntemiyle XMP verisine erişin. `getXmpData`, gömülü XMP paketini görüntüden okur.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

Tebrikler! Aspose.Imaging for Java kullanarak görsellerde XMP verisini nasıl yöneteceğinizi başarıyla öğrendiniz. Bu, görüntü dosyalarınız içinde değerli meta verileri depolamanıza ve almanıza olanak tanır.

## Yaygın Sorunlar ve Çözümler

- **Meta veri Photoshop'ta görünmüyor:** XMP paketinin doğru XML şemasını izlediğinden emin olun; Aspose.Imaging bunu otomatik olarak doğrular, ancak özel ad alanlarının kaydedilmesi gerekebilir.  
- **Büyük TIFF dosyaları OutOfMemoryError hatasına neden oluyor:** `Compression`'ı `LZW` olarak ayarlı `TiffOptions` kullanın ve akışı etkinleştirin (`loadOptions.setBufferSize`) böylece bellek kullanımı düşük tutulur.  
- **Beklenmeyen karakter kodlaması:** XMP UTF‑8 bekler; bozuk veri oluşmasını önlemek için her zaman `StandardCharsets.UTF_8` kullanarak string'leri geçin.

## Sık Sorulan Sorular

**S: XMP meta verisi nedir?**  
**C:** XMP, tanımlayıcı bilgileri doğrudan dosyalar içine gömen bir XML‑tabanlı standarttır ve uygulamalar arasında tutarlı meta veri sağlar.

**S: XMP meta verisi neden önemlidir?**  
**C:** Görsellere yazar, telif hakkı, anahtar kelimeler ve özel veri etiketlemenizi sağlar, böylece dış veri tabanları olmadan aranabilirlik ve varlık yönetimi iyileşir.

**S: Görsele XMP meta verisi gömdükten sonra düzenleyebilir miyim?**  
**C:** Evet, Aspose.Imaging for Java mevcut XMP paketlerini değiştirmek ve dosyaya geri yazmak için yöntemler sunar.

**S: Aspose.Imaging for Java ücretsiz bir araç mı?**  
**C:** Değerlendirme için ücretsiz bir deneme sürümü mevcuttur, ancak üretim kullanımı için ücretli lisans gerekir. Seçenekleri [Aspose.Imaging for Java website](https://purchase.aspose.com/buy) adresinde inceleyebilirsiniz.

**S: Aspose.Imaging for Java için yardım ve destek nereden alabilirim?**  
**C:** Topluluk desteği için [Aspose.Imaging forums](https://forum.aspose.com/) adresini ziyaret edin veya ücretli lisans müşterileri için doğrudan Aspose desteğiyle iletişime geçin.

## Sonuç

Bu öğreticide, önde gelen **java image processing library** Aspose.Imaging for Java kullanarak görsellerde XMP meta verisiyle nasıl çalışılacağını inceledik. Adım adım kılavuzu izleyerek XMP verisini kolayca gömebilir, güncelleyebilir ve alabilirsiniz; böylece dijital varlıklarınızı aranabilir, standartlara uygun meta verilerle zenginleştirirsiniz.

---

**Son Güncelleme:** 2026-05-18  
**Test Edilen Versiyon:** Aspose.Imaging for Java 24.12  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [Java Görüntü İşlemede Ustalaşın: Aspose.Imaging ile EXIF Verisini Değiştirin](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [Aspose.Imaging ile Java Görüntü İşleme: Görselleri Yükleme, İyileştirme ve Kaydetme](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [Aspose.Imaging Kütüphanesi ile İleri Düzey Java Görüntü İşleme](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Specify the size of image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// create the brand new image just for sample purposes
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// create an instance of XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// create an instance of Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// create an instance of XMP meta class to set different attributes
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// create an instance of XmpPacketWrapper that contains all metadata
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// create an instance of Photoshop package and set photoshop attributes
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// add photoshop package into XMP metadata
	xmpData.addPackage(photoshopPackage);
	// create an instance of DublinCore package and set dublinCore attributes
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// add dublinCore Package into XMP metadata
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// update XMP metadata into image
	image.setXmpData(xmpData);
	// Save image on the disk or in memory stream
	image.save(ms);
	// Load the image from memory stream or from disk to read/get the metadata
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Getting the XMP metadata
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Use package data ...
		}
	}
}
        
```