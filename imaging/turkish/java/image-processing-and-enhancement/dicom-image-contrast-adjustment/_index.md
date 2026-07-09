---
date: 2026-01-12
description: DICOM görüntülerinde kontrastı nasıl ayarlayacağınızı öğrenin – Aspose.Imaging
  for Java kullanarak kontrastı ayarlama ve DICOM'u BMP'ye dönüştürme konusunda adım
  adım bir rehber.
linktitle: DICOM Image Contrast Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java kullanarak DICOM Görüntülerinde Kontrastı Nasıl Ayarlarsınız
url: /tr/java/image-processing-and-enhancement/dicom-image-contrast-adjustment/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java ile DICOM Görüntülerinde Kontrastı Ayarlama

Modern tıbbi görüntülemede, **kontrastı nasıl ayarlayacağınız** net bir tanı ile kaçırılan bir detay arasındaki farkı yaratabilir. Bu öğretici, Aspose.Imaging for Java kullanarak DICOM dosyalarında kontrastı ayarlamak için kesin adımları size gösterir ve bu DICOM görüntülerini kolay görüntüleme veya daha fazla işleme için BMP'ye nasıl dönüştüreceğinizi gösterir. Sonunda, herhangi bir Java projesine ekleyebileceğiniz hazır‑kullanım kod parçacığına sahip olacaksınız.

## Hızlı Yanıtlar
- **Kontrast ayarlaması ne yapar?** Karanlık ve parlak pikseller arasındaki aralığı genişleterek yapıların öne çıkmasını sağlar.
- **Hangi kütüphane gereklidir?** Aspose.Imaging for Java.
- **BMP olarak çıktı alabilir miyim?** Evet – kontrastı ayarladıktan sonra DICOM'u BMP'ye dönüştürebilirsiniz.
- **Üretim için lisansa ihtiyacım var mı?** Değerlendirme dışı kullanım için ticari bir lisans gereklidir.
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri.

## Contrast Adjustment Nedir ve Neden Önemlidir?
Kontrast ayarlaması, anatomik özellikler arasındaki görsel farkı artırarak radyologların anormallikleri daha hızlı fark etmesine yardımcı olur. Bir DICOM iş akışında, dönüştürmeden önce kontrastı ayarlamak, BMP çıktısının raporlama veya arşivleme için gereken tanısal kaliteyi korumasını sağlar.

## Ön Koşullar

Before diving into the code, verify that you have:

1. **Aspose.Imaging for Java** – resmi siteden [buradan](https://releases.aspose.com/imaging/java/) indirin.  
2. **Java Development Environment** – JDK 8+ ve favori IDE'niz (IntelliJ, Eclipse, VS Code, vb.).  
3. **A DICOM Image** – geliştirmek istediğiniz herhangi bir .dcm dosyası; örnek dosyalar çevrimiçi olarak mevcuttur veya kendi klinik verilerinizi kullanabilirsiniz.

## Paketleri İçe Aktarma

Bu içe aktarmalar, DICOM işleme ve BMP kaydetme özelliklerine erişmenizi sağlar.

```java
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
```

## DICOM Görüntülerinde Kontrastı Nasıl Ayarlarsınız

Aşağıda tam, adım‑adım iş akışı yer almaktadır. Her adım, Aspose.Imaging'e yeni olsanız bile kolay anlaşılır bir dilde açıklanmıştır.

### Adım 1: Dosya Yollarını Belirleyin

Giriş DICOM konumunu ve istenen çıktı BMP yolunu ayarlayın. Yer tutucuyu makinenizdeki gerçek dizinle değiştirin.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingContrast_out.bmp";
```

### Adım 2: DICOM Görüntüyü Yükleyin

`FileInputStream` kullanarak DICOM dosyasını açıyoruz. `try‑with‑resources` bloğu, akışın otomatik olarak kapanmasını sağlar.

```java
File file = new File(inputFile);

try (FileInputStream fis = new FileInputStream(file)) {
    try (DicomImage image = (DicomImage) Image.load(fis)) {
        // All further processing happens inside this block
    }
} catch (IOException ex) {
    Logger.println(ex.getMessage());
    ex.printStackTrace();
}
```

### Adım 3: Kontrastı Ayarlayın

İç `try` bloğu içinde `adjustContrast` metodunu çağırın. Değer **‑100** (azaltma) ile **+100** (arttırma) arasında olabilir. Bu örnekte kontrastı 50 birim artırıyoruz.

```java
image.adjustContrast(50);
```

### Adım 4: DICOM'u BMP'ye Dönüştürün ve Görüntüyü Kaydedin

Kontrastı ayarladıktan sonra bir `BmpOptions` örneği oluşturup sonucu BMP dosyası olarak kaydediyoruz. Bu adım **DICOM'u BMP'ye dönüştürür**, size yaygın olarak desteklenen bir raster formatı sağlar.

```java
image.save(outputFile, new BmpOptions());
```

## Yaygın Sorunlar ve İpuçları
- **Geçersiz DICOM dosyası** – .dcm dosyasının desteklenmeyen bir transfer sözdizimiyle sıkıştırılmadığından emin olun. Aspose.Imaging çoğu standart DICOM kodlamasını destekler.
- **Kontrast değeri aralık dışında** – ±100'ün üzerindeki değerler kırpılır; görüntünün histogramına uygun bir sayı seçin.
- **Bellek kullanımı** – Büyük DICOM serileri önemli miktarda RAM tüketebilir. `OutOfMemoryError` ile karşılaşırsanız bir seferde bir dilim işleyin.

## Sonuç

Artık Aspose.Imaging for Java kullanarak DICOM görüntülerinde **kontrastı nasıl ayarlayacağınızı** ve **DICOM'u BMP'ye nasıl dönüştüreceğinizi** öğrendiniz. Bu iş akışı hızlı, güvenilir ve daha büyük tıbbi‑görüntü hatlarına entegre edilebilir; ister bir PACS görüntüleyici, bir araştırma aracı ya da otomatik raporlama sistemi oluşturuyor olun.

Aspose.Imaging for Java, düşük seviyeli DICOM işlemesini soyutlayarak, görüntülerinizin klinik değerine odaklanmanızı sağlar.

## Sıkça Sorulan Sorular

**Q: DICOM nedir ve neden tıbbi görüntülemede standarttır?**  
**A:** DICOM (Digital Imaging and Communications in Medicine), tıbbi görüntüleri depolamak, iletmek ve paylaşmak için evrensel bir formattır; cihazlar ve kurumlar arasında birlikte çalışabilirliği sağlar.

**Q: Parlaklığı da kontrastla birlikte ayarlayabilir miyim?**  
**A:** Evet, `adjustBrightness(int value)` metodu benzer şekilde çalışır ve kaydetmeden önce zincirlenebilir.

**Q: Aspose.Imaging BMP dışındaki diğer çıktı formatlarını destekliyor mu?**  
**A:** Kesinlikle – ilgili `*Options` sınıfını kullanarak PNG, JPEG, TIFF ve daha birçok formata dışa aktarabilirsiniz.

**Q: Üretim kullanımında ticari bir lisans gerekli mi?**  
**A:** Evet. Bir lisans satın alabilirsiniz [buradan](https://purchase.aspose.com/buy) veya geçici bir değerlendirme lisansı edinebilirsiniz [buradan](https://purchase.aspose.com/temporary-license/).

**Q: Daha fazla yardım ve örnek nereden bulunabilir?**  
**A:** Aspose.Imaging for Java topluluk forumu, kapsamlı dokümantasyon ve örnek kod sağlar: [Aspose.Imaging for Java forum](https://forum.aspose.com/).

---

**Son Güncelleme:** 2026-01-12  
**Test Edilen Versiyon:** Aspose.Imaging for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}