---
title: Aspose.Imaging for Java ile Çapraz Görüntü Filigranı
linktitle: Çapraz Görüntü Filigranı
second_title: Aspose.Imaging Java Görüntü İşleme API'si
description: Aspose.Imaging for Java'yı kullanarak görsellerinizi çapraz filigranla geliştirin. Bu adım adım kılavuzu izleyin ve zahmetsizce çarpıcı filigranlı görüntüler oluşturun.
weight: 14
url: /tr/java/image-processing-and-enhancement/diagonal-image-watermarking/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java ile Çapraz Görüntü Filigranı


Resimlerinizi şık bir diyagonal filigranla geliştirmek istiyorsanız Aspose.Imaging for Java size yardımcı olmak için burada. Bu adım adım kılavuzda, mevcut bir JPG görüntüsüne 45 derece döndürülmüş metin filigranı ekleme sürecinde size yol göstereceğiz. Bunu takip etmek için Java veya görüntü işleme konusunda uzman olmanıza gerek yok; profesyonel sonuçlara kolayca ulaşabilmenizi sağlamak için her örneği birden fazla adıma ayıracağız.

## Önkoşullar

Görüntü filigranlamanın heyecan verici dünyasına dalmadan önce birkaç şeye ihtiyacınız olacak:

1.  Aspose.Imaging for Java: Aspose.Imaging for Java'nın kurulu olduğundan emin olun. İndirme linkini bulabilirsiniz[Burada](https://releases.aspose.com/imaging/java/).

2. Java Geliştirme Ortamı: Bilgisayarınızda çalışan bir Java geliştirme ortamının kurulu olması gerekir.

3. Filigranlanacak Görüntü: Filigranlamak istediğiniz görüntüyü hazırlayın ve bir dizinde saklayın. Bu eğitim için örnek bir resim kullanabilirsiniz.

## Paketleri İçe Aktar

Öncelikle Java projenizi görüntü filigranı için hazır hale getirmek için gerekli paketleri içe aktarın. Eklemeniz gereken temel paketler aşağıdadır:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## 1. Adım: Mevcut Bir Görüntüyü Yükleyin

Filigran eklemek istediğiniz görüntüyü yükleyin. Bu örnekte, "ModifyingImages" dizininizde "SampleTiff1.tiff" adında bir JPG resminizin olduğunu varsayıyoruz.

```java
// Belgeler dizininin yolu.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Mevcut bir JPG resmini yükleyin
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Kodun geri kalanı buraya gelecek
}
```

## Adım 2: Filigran Metnini ve Grafiklerini Hazırlayın

Şimdi filigran metninizi bildirelim ve filigran için grafikleri ayarlayalım.

```java
// Filigran Metni ile bir String nesnesi bildirin
String theString = "45 Degree Rotated Text";

// Graphics sınıfının bir örneğini oluşturun ve başlatın
Graphics graphics = new Graphics(image);

// Görüntü Boyutunu depolamak için SizeF nesnesini başlatın
Size sz = graphics.getImage().getSize();
```

## 3. Adım: Yazı Tipini ve Fırçayı Tanımlayın

Filigranınızın yazı tipini ve fırçasını ayarlayın. Yazı tipini, boyutunu ve stilini tercihlerinize uyacak şekilde özelleştirebilirsiniz.

```java
// Bir Font örneği oluşturun, Font Yüzü, Boyutu ve Stili ile başlatın
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// SolidBrush'un bir örneğini oluşturun ve çeşitli özelliklerini ayarlayın
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Adım 4: Metninizi Biçimlendirin

Hizalama ve biçim bayrakları da dahil olmak üzere filigran metninizin biçimini tanımlayın.

```java
// StringFormat sınıfının bir nesnesini başlatın ve çeşitli özelliklerini ayarlayın
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Adım 5: Dönüşümü Uygulayın

Filigran metnini konumlandırmak ve döndürmek için bir dönüştürme matrisi oluşturun. Bu örnekte metni 45 derece döndüreceğiz.

```java
// Dönüşüm için Matrix sınıfının bir nesnesini oluşturun
Matrix matrix = new Matrix();
//Önce bir çeviri, sonra bir döndürme
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Matris Yoluyla Dönüşümü Ayarlayın
graphics.setTransform(matrix);
```

## Adım 6: Çizin ve Kaydedin

Şimdi görsele metin ekleme ve filigranlı görseli istediğiniz konuma kaydetme zamanı geldi.

```java
// Dizeyi görüntünün üzerine çizin
graphics.drawString(theString, font, brush, 0, 0, format);

// Çıktıyı diske kaydet
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Tebrikler! Aspose.Imaging for Java'yı kullanarak görüntünüze başarıyla çapraz filigran eklediniz.

## Çözüm

Bu eğitimde Aspose.Imaging for Java'yı kullanarak görsellerinizi çapraz filigranla nasıl geliştireceğinizi öğrendik. Resimlerinize profesyonel bir dokunuş katmak için güçlü bir araçtır. Yalnızca birkaç basit adımla, diğerlerinden öne çıkan çarpıcı filigranlı görüntüler oluşturabilirsiniz.

## SSS'ler

### S1: Aspose.Imaging for Java yeni başlayanlar için uygun mu?

A1: Kesinlikle! Aspose.Imaging for Java, kullanıcı dostu bir arayüz ve kapsamlı belgeler sunar. Yeni başlayanlar bile görüntü işlemeye hızla başlayabilir.

### S2: Filigran metnini ve stilini özelleştirebilir miyim?

C2: Evet, filigran metnini, yazı tipini, boyutunu, rengini ve dönüş açısını tercihlerinize ve markanıza uyacak şekilde kolayca özelleştirebilirsiniz.

### S3: Aspose.Imaging for Java, JPG'nin yanı sıra diğer görüntü formatlarını da destekliyor mu?

Cevap3: Evet, Aspose.Imaging for Java, BMP, PNG, GIF ve daha fazlası dahil çok çeşitli görüntü formatlarını destekler.

### S4: Aspose.Imaging for Java'nın ücretsiz deneme sürümü mevcut mu?

 Cevap4: Evet, Aspose.Imaging for Java'yı ücretsiz deneme sürümüyle deneyebilirsiniz. Anla[Burada](https://releases.aspose.com/).

### S5: Aspose.Imaging for Java için nereden yardım veya destek bulabilirim?

 Cevap5: Herhangi bir sorunuz varsa veya yardıma ihtiyacınız varsa Aspose.Imaging for Java destek forumunu ziyaret edin.[Burada](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
