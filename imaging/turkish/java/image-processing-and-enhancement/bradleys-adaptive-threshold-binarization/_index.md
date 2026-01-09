---
date: 2026-01-09
description: Aspose.Imaging for Java kullanarak görüntüyü ikili hâle getirmeyi öğrenin.
  Bu kılavuz, DICOM’dan BMP’ye dönüşüm için görüntü işleme Java tekniklerini kapsar.
linktitle: Bradley's Adaptive Threshold Binarization
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java ile Görüntüyü İkili Hale Getirme
url: /tr/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java ile Görüntüyü İkili Hale Getirme

Görseller, web sitelerinde, belgelerde ya da çeşitli uygulamaların bir parçası olarak dijital dünyada hayati bir rol oynar. **Görüntüyü nasıl ikili hale getirebileceğinizi** merak ediyorsanız, özellikle DICOM gibi tıbbi formatlar için, doğru yerdesiniz. Görüntü ikilileştirme, bir resmi siyah‑beyaz temsile dönüştürerek basitleştirir; bu, sonraki analiz, OCR veya depolama optimizasyonu için idealdir. Bu öğreticide, Aspose.Imaging for Java’nın Bradley Adaptif Eşik İkilileştirme yöntemini kullanarak tüm süreci adım adım inceleyeceğiz.

## Hızlı Yanıtlar
- **İkilileştirme ne yapar?** Her pikseli bir eşik değerine göre siyah ya da beyaz olarak dönüştürür.
- **Java görüntü işleme için en iyi kütüphane hangisidir?** Aspose.Imaging for Java, güçlü ve lisans‑sız deneme özellikleri sunar.
- **DICOM dosyalarını doğrudan işleyebilir miyim?** Evet, Aspose.Imaging DICOM’u yükleyebilir ve BMP, PNG vb. formatlarda çıktı verebilir.
- **Üretim ortamı için lisansa ihtiyacım var mı?** Deneme dışı kullanım için ticari bir lisans gereklidir.
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri tamamen uyumludur.

## Görüntü İkilileştirme Nedir?
Görüntü ikilileştirme, gri tonlamalı ya da renkli bir resmi, her pikselin 0 (siyah) ya da 255 (beyaz) olduğu ikili bir görüntüye dönüştürme işlemidir. Bu adım, tıbbi görüntü işleme hatları, belge tarama ve bilgisayarlı görü görevlerinin ilk aşaması olarak sıkça kullanılır.

## Neden Aspose.Imaging for Java?
Aspose.Imaging, **DICOM’u yükleyen**, **Bradley Adaptif Eşik** gibi gelişmiş algoritmaları uygulayan ve sonucu dış kütüphanelere ihtiyaç duymadan yaygın formatlarda kaydeden saf‑Java bir API sunar. **Tıbbi görüntü işleme**, **DICOM’u BMP’ye dönüştürme** ve diğer Java‑tabanlı iş akışları için idealdir.

## Önkoşullar

Kodlamaya başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- **Java Geliştirme Ortamı** – JDK 8 veya daha yeni bir sürüm yüklü.
- **Aspose.Imaging for Java** – Resmi siteden indirin: [Download Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/).
- **Bir DICOM Görüntüsü** – İkilileştirmek istediğiniz herhangi bir örnek DICOM dosyası.

Her şey hazır olduğuna göre, uygulamaya geçelim.

## Görüntüyü İkili Hale Getirme – Adım‑Adım Kılavuz

### Paketleri İçe Aktarma
İlk olarak gerekli Aspose.Imaging sınıflarını içe aktarın. Bu kod parçacığı ayrıca giriş ve çıkış dosya yollarını tanımlar.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// Load a DICOM image in an instance of DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Binarize image with Bradley's adaptive threshold.
    image.binarizeBradley(10);
    // Save the resultant image.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

### Adım 1: Yolları Tanımlama
Kaynak DICOM dosyanız ve hedef BMP dosyanız için konumları ayarlayın. `"Your Document Directory"` ifadesini sisteminizdeki gerçek klasörle değiştirin.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

### Adım 2: DICOM Görüntüsünü Yükleme
Aspose.Imaging kullanarak **dicom görüntüsünü** bir `DicomImage` nesnesine **yükleyin**. Bu nesne, piksel verilerine ve işleme yöntemlerine tam erişim sağlar.

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // The image processing steps will go here.
}
```

### Adım 3: İkilileştirme İşlemini Gerçekleştirme
Bradley Adaptif Eşik algoritmasını uygulayın. Parametre (`10` bu örnekte) eşik hassasiyetini kontrol eder; en iyi sonucu elde etmek için farklı değerlerle deney yapabilirsiniz.

```java
image.binarizeBradley(10);
```

### Adım 4: İkili Görüntüyü Kaydetme
Son olarak işlenmiş görüntüyü dışa aktarın. Burada BMP formatını kullandık, ancak Aspose.Imaging PNG, JPEG, TIFF ve daha birçok formatı destekler.

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## Yaygın Sorunlar & Sorun Giderme

- **FileNotFoundException** – `dataDir` yolunun sonunda bir eğik çizgi olduğundan ve DICOM dosya adının tam olarak eşleştiğinden emin olun.
- **OutOfMemoryError** – Büyük DICOM dosyaları JVM yığın boyutunun artırılmasını gerektirebilir (`-Xmx2g` veya daha yüksek).
- **Yanlış Eşik** – Çıktı çok karanlık ya da çok aydınlık görünüyorsa, `binarizeBradley()` metoduna verilen tam sayıyı (ör. 5‑15) ayarlayın.

## Sık Sorulan Sorular

### S1: DICOM nedir ve tıbbi görüntülemede neden önemlidir?
**C:** DICOM, Digital Imaging and Communications in Medicine (Dijital Görüntüleme ve İletişim) anlamına gelir. Tıbbi görüntülerin depolanması, iletilmesi ve işlenmesi için evrensel bir standarttır; cihazlar ve sistemler arasında birlikte çalışabilirliği sağlar.

### S2: Aspose.Imaging for Java’yı ticari projelerimde kullanabilir miyim?
**C:** Evet, Aspose.Imaging for Java hem ücretsiz deneme hem de ticari lisans seçenekleri sunar. Seçeneklerinizi inceleyebilir ve gerekli lisansı [Aspose'un web sitesinden](https://purchase.aspose.com/buy) temin edebilirsiniz.

### S3: Test amaçlı geçici lisanslar mevcut mu?
**C:** Evet, Aspose.Imaging for Java’yı test ve değerlendirme amacıyla geçici bir lisans alabilirsiniz. Daha fazla bilgi için [bu bağlantıyı](https://purchase.aspose.com/temporary-license/) ziyaret edin.

### S4: Aspose.Imaging for Java ile ilgili yardım almak ya da sorunları tartışmak için nereye başvurabilirim?
**C:** Topluluk desteği ve tartışmalar için [Aspose.Imaging forumunu](https://forum.aspose.com/) ziyaret edebilirsiniz. Sorularınıza yanıt bulmak ve diğer kullanıcılarla iletişim kurmak için harika bir yerdir.

### S5: Aspose.Imaging for Java, diğer Java‑tabanlı uygulamalarda görüntü işleme için uygun mu?
**C:** Kesinlikle. Kütüphane, web uygulamaları, masaüstü yazılımları, toplu iş araçları ve daha fazlasında sorunsuz çalışır; platformlar arasında tutarlı bir API sağlar.

## Sonuç
Artık **Aspose.Imaging for Java** ve Bradley Adaptif Eşik yöntemiyle **görüntüyü nasıl ikili hale getireceğinizi** öğrendiniz. Bu teknik, **tıbbi görüntü işleme** için özellikle değerlidir; DICOM dosyalarını analiz veya depolama için hafif BMP (veya diğer) formatlarına dönüştürmenizi sağlar. Farklı eşik değerleriyle denemeler yapmaya devam edin ve Aspose.Imaging’in zengin özellik setini keşfedin.

Daha derin görüntü manipülasyonu konuları için resmi dokümantasyona göz atın: [Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/).

---

**Son Güncelleme:** 2026-01-09  
**Test Edilen Versiyon:** Aspose.Imaging for Java 24.12 (yazım anındaki en yeni sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}