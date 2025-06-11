---
"description": "Aspose.Imaging for Java kullanarak resimlerinizi çapraz filigranla geliştirin. Bu adım adım kılavuzu izleyin ve zahmetsizce çarpıcı filigranlı resimler oluşturun."
"linktitle": "Diyagonal Görüntü Filigranlama"
"second_title": "Aspose.Imaging Java Görüntü İşleme API'si"
"title": "Java için Aspose.Imaging ile Diyagonal Görüntü Filigranlama"
"url": "/tr/java/image-processing-and-enhancement/diagonal-image-watermarking/"
"weight": 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Java için Aspose.Imaging ile Diyagonal Görüntü Filigranlama


Resimlerinizi şık bir diyagonal filigranla geliştirmek istiyorsanız, Java için Aspose.Imaging size yardımcı olmak için burada. Bu adım adım kılavuzda, mevcut bir JPG resmine 45 derece döndürülmüş metin filigranı ekleme sürecini adım adım anlatacağız. Takip etmek için Java veya görüntü işleme konusunda uzman olmanıza gerek yok; her örneği profesyonel sonuçlara kolayca ulaşmanızı sağlamak için birden fazla adıma ayıracağız.

## Ön koşullar

Resim filigranlamanın heyecan verici dünyasına dalmadan önce, birkaç şeyin yerli yerinde olması gerekir:

1. Java için Aspose.Imaging: Java için Aspose.Imaging'in yüklü olduğundan emin olun. İndirme bağlantısını bulabilirsiniz [Burada](https://releases.aspose.com/imaging/java/).

2. Java Geliştirme Ortamı: Bilgisayarınızda çalışan bir Java geliştirme ortamının kurulu olması gerekir.

3. Filigran Eklemek İçin Bir Resim: Filigran eklemek istediğiniz resmi hazırlayın ve bir dizinde saklayın. Bu eğitim için bir örnek resim kullanabilirsiniz.

## Paketleri İçe Aktar

Öncelikle, Java projenizi resim filigranı için hazır hale getirmek için gerekli paketleri içe aktarın. Aşağıda dahil etmeniz gereken temel paketler bulunmaktadır:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Adım 1: Mevcut Bir Görüntüyü Yükleyin

Filigran eklemek istediğiniz resmi yükleyin. Bu örnekte, "ModifyingImages" dizininizde "SampleTiff1.tiff" adlı bir JPG resminiz olduğunu varsayıyoruz.

```java
// Belgeler dizinine giden yol.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Mevcut bir JPG resmini yükleyin
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Kodun geri kalanı buraya gelecek
}
```

## Adım 2: Filigran Metni ve Grafiklerini Hazırlayın

Şimdi filigran metninizi tanımlayalım ve filigran için grafikleri ayarlayalım.

```java
// Filigran Metni ile bir Dize nesnesi bildirin
String theString = "45 Degree Rotated Text";

// Graphics sınıfının bir örneğini oluşturun ve başlatın
Graphics graphics = new Graphics(image);

// Görüntü Boyutunu depolamak için SizeF nesnesini başlatın
Size sz = graphics.getImage().getSize();
```

## Adım 3: Yazı Tipini ve Fırçayı Tanımlayın

Filigranınız için yazı tipini ve fırçayı ayarlayın. Yazı tipini, boyutunu ve stilini tercihlerinize uyacak şekilde özelleştirebilirsiniz.

```java
// Bir Font örneği oluşturun, bunu Font Yüzü, Boyutu ve Stili ile başlatın
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// SolidBrush'ın bir örneğini oluşturun ve çeşitli özelliklerini ayarlayın
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Adım 4: Metninizi Biçimlendirin

Filigran metniniz için hizalama ve biçim işaretleri dahil olmak üzere biçimi tanımlayın.

```java
// StringFormat sınıfının bir nesnesini başlatın ve çeşitli özelliklerini ayarlayın
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Adım 5: Dönüşümü Uygula

Filigran metnini konumlandırmak ve döndürmek için bir dönüşüm matrisi oluşturun. Bu örnekte metni 45 derece döndüreceğiz.

```java
// Dönüşüm için Matrix sınıfından bir nesne oluşturun
Matrix matrix = new Matrix();
// Önce bir çeviri sonra bir rotasyon
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Dönüşümü Matris Üzerinden Ayarlayın
graphics.setTransform(matrix);
```

## Adım 6: Çiz ve Kaydet

Şimdi, metni görsele eklemenin ve filigranlı görseli istediğiniz yere kaydetmenin zamanı geldi.

```java
// Resimdeki ipi çizin
graphics.drawString(theString, font, brush, 0, 0, format);

// Çıktıyı diske kaydet
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Tebrikler! Aspose.Imaging for Java'yı kullanarak resminize çapraz filigran eklemeyi başardınız.

## Çözüm

Bu eğitimde, Aspose.Imaging for Java kullanarak resimlerinizi diyagonal filigranla nasıl geliştireceğinizi öğrendik. Resimlerinize profesyonel bir dokunuş katmak için güçlü bir araçtır. Sadece birkaç basit adımla, diğerlerinden sıyrılan çarpıcı filigranlı resimler oluşturabilirsiniz.

## SSS

### S1: Aspose.Imaging for Java yeni başlayanlar için uygun mu?

A1: Kesinlikle! Aspose.Imaging for Java, kullanıcı dostu bir arayüz ve kapsamlı belgeler sunar. Yeni başlayanlar bile görüntü işlemeye hızla başlayabilir.

### S2: Filigran metnini ve stilini özelleştirebilir miyim?

C2: Evet, filigran metnini, yazı tipini, boyutunu, rengini ve dönüş açısını tercihlerinize ve markanıza uyacak şekilde kolayca özelleştirebilirsiniz.

### S3: Aspose.Imaging for Java, JPG dışında başka resim formatlarını da destekliyor mu?

C3: Evet, Aspose.Imaging for Java, BMP, PNG, GIF ve daha fazlası dahil olmak üzere çok çeşitli görüntü formatlarını destekler.

### S4: Aspose.Imaging for Java için ücretsiz deneme sürümü var mı?

A4: Evet, Aspose.Imaging for Java'yı ücretsiz deneme sürümüyle deneyebilirsiniz. Edinin [Burada](https://releases.aspose.com/).

### S5: Aspose.Imaging for Java için yardım veya desteği nerede bulabilirim?

A5: Herhangi bir sorunuz varsa veya yardıma ihtiyacınız varsa Aspose.Imaging for Java destek forumunu ziyaret edin [Burada](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}