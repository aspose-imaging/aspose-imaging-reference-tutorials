---
date: 2026-02-12
description: Aspose ile boş bir resim oluşturmayı ve Aspose.Imaging kullanarak .NET'te
  dikdörtgen çizmeyi öğrenin – .NET uygulamalarınızda görüntü işleme için hızlı bir
  rehber.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Aspose ile Boş Görüntü Oluştur – .NET'te Dikdörtgen Çiz
url: /tr/net/basic-drawing/draw-rectangle/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Boş Görüntü Aspose Oluşturma – .NET'te Dikdörtgen Çizme

.NET uygulamalarında görüntü oluşturmak ve manipüle etmek zorlayıcı görünebilir, ancak Aspose.Imaging ile sadece birkaç satır kodla **create blank image Aspose** oluşturabilir ve üzerine şekiller çizebilirsiniz. Bu öğreticide, boş bir tuval oluşturulmasından dikdörtgen çizimine kadar tüm süreci adım adım göstereceğiz—böylece .NET projelerinize hemen grafik eklemeye başlayabilirsiniz.

## Hızlı Yanıtlar
- **“create blank image Aspose” ne anlama geliyor?** Aspose.Imaging API'sini kullanarak boş bir bitmap oluşturmak anlamına gelir.  
- **Aspose ile .net'te dikdörtgen nasıl çizilir?** Bir `Graphics` nesnesi başlattıktan sonra `Graphics.DrawRectangle` metodunu kullanın.  
- **Hangi NuGet paketi gerekiyor?** `Aspose.Imaging` (en son sürüm).  
- **Görüntüyü PNG, JPEG veya BMP olarak kaydedebilir miyim?** Evet – sadece görüntü seçeneklerini değiştirin (ör. `BmpOptions`, `JpegOptions`).  
- **Geliştirme için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.

## “create blank image Aspose” nedir?
Boş bir görüntü oluşturmak, tanımlı genişlik, yükseklik ve piksel formatına sahip bir piksel tamponu ayırmak anlamına gelir. Aspose.Imaging düşük seviyeli ayrıntıları yönetir ve GDI+ ya da System.Drawing ile uğraşmadan çizime hazır bir tuval sağlar.

## .NET'te dikdörtgen çizmek için Aspose.Imaging neden kullanılmalı?
- **Cross‑platform** – Windows, Linux ve macOS'ta çalışır.  
- **Yerel bağımlılık yok** – saf yönetilen kod, sunucu ortamları için mükemmel.  
- **Zengin çizim API'si** – kalemler, fırçalar, anti‑aliasing ve birçok şekil türünü destekler.  
- **Yüksek performans** – büyük görüntüler ve toplu işlem için optimize edilmiştir.

## Önkoşullar

1. **Aspose.Imaging for .NET** – [download page](https://releases.aspose.com/imaging/net/) adresinden indirin.  
2. **Geliştirme Ortamı** – Visual Studio, VS Code veya herhangi bir .NET uyumlu IDE.  
3. **.NET çalışma zamanı** – .NET 6+ veya .NET Framework 4.7.2+.

Şimdi her şey hazır olduğuna göre, koda dalalım.

## .NET'te boş görüntü Aspose nasıl oluşturulur?

### Adım 1: Gerekli ad alanlarını içe aktarın

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Bu ad alanları, temel görüntüleme sınıflarına, fırça türlerine ve görüntü kaydetme seçeneklerine erişim sağlar.

### Adım 2: Boş bir görüntü oluşturun (tuval)

```csharp
string dataDir = "Your Document Directory";  // Set the path to your document directory
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Your drawing code will go here
        image.Save();
    }
}
```

Bu blokta:
* Çıktı konumunu (`dataDir`) tanımlarız.  
* `BmpOptions`'ı 32‑bit piksel formatı kullanacak şekilde yapılandırırız.  
* 100 × 100 piksel **blank image** oluştururuz.

### Adım 3: Aspose.Imaging ile .net'te dikdörtgen nasıl çizilir

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` tuvali bir arka plan rengiyle doldurur (bu örnekte sarı).  
* `DrawRectangle` iki dikdörtgen çizer—biri basit kırmızı bir kalemle, diğeri mavi katı bir fırça ile—görsel kontrast sağlamak için.

### Adım 4: Görüntüyü kaydedin

```csharp
image.Save();
```

`Save` çağrısı, bitmap'i daha önce tanımlanan seçenekleri kullanarak dosya sistemine yazar.

## Yaygın Sorunlar ve İpuçları

| Issue | Reason | Fix |
|-------|--------|-----|
| **Boş görüntü siyah görünüyor** | Arka plan temizlenmedi | `graphic.Clear(Color.YourColor)` metodunu çizmeden önce çağırın. |
| **Dosya bulunamadı istisnası** | `dataDir` mevcut olmayan bir klasöre işaret ediyor | Klasörün var olduğundan emin olun veya `Environment.CurrentDirectory` ile `Path.Combine` kullanın. |
| **Yanlış renkler** | `System.Drawing.Color` yerine `Aspose.Imaging.Color` kullanılması | Her zaman `Aspose.Imaging.Color` içe aktarın. |
| **Büyük görüntülerde performans gecikmesi** | Yüksek bit‑per‑pixel değerine sahip varsayılan `BmpOptions` kullanılması | Sıkıştırma için `JpegOptions` veya `PngOptions`'a geçin. |

## Sıkça Sorulan Sorular (Genişletilmiş)

**S: Dikdörtgen dışında başka şekiller çizebilir miyim?**  
C: Kesinlikle. Aspose.Imaging `DrawEllipse`, `DrawLine` ve `DrawPolygon` gibi metodlar sunar.

**S: Kütüphane ticari kullanım için ücretsiz mi?**  
C: Hayır, Aspose.Imaging ticari bir üründür, ancak [buradan](https://releases.aspose.com/) ücretsiz deneme sürümüyle değerlendirebilirsiniz.

**S: Bu hem Windows hem de web uygulamalarında çalışır mı?**  
C: Evet, aynı kod ASP.NET, Blazor ve konsol uygulamalarında çalışır.

**S: Çıktı formatını PNG'ye nasıl değiştiririm?**  
C: `BmpOptions` yerine `PngOptions` kullanın ve dosya uzantısını buna göre ayarlayın.

**S: Daha ayrıntılı belgeleri nereden bulabilirim?**  
C: Tam API referansına [buradan](https://reference.aspose.com/imaging/net/) ulaşabilir ve topluluğa [Aspose.Imaging forumunda](https://forum.aspose.com/) katılabilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-02-12  
**Test Edilen:** Aspose.Imaging 24.12 for .NET  
**Yazar:** Aspose