---
title: Aspose.Imaging for .NET'te XMP Etiketlerinin Saklanması Desteği
linktitle: Aspose.Imaging for .NET'te XMP Etiketlerinin Saklanması Desteği
second_title: Aspose.Imaging .NET Görüntü İşleme API'si
description: Aspose.Imaging for .NET kullanarak DICOM görüntülerine XMP meta verilerini nasıl ekleyeceğinizi öğrenin. Bu adım adım kılavuzla görüntü yönetimini ve organizasyonunu optimize edin.
type: docs
weight: 25
url: /tr/net/dicom-image-processing/support-storing-xmp-tags/
---
Aspose.Imaging for .NET, .NET ortamında çeşitli görüntü formatlarıyla çalışmanıza olanak tanıyan güçlü bir kütüphanedir. Bu eğitimde, Aspose.Imaging for .NET'te XMP (Genişletilebilir Meta Veri Platformu) etiketlerinin saklanmasının nasıl destekleneceğini keşfedeceğiz. XMP etiketleri, görüntülere meta veri bilgileri eklemek ve dijital varlıklarınızı organize etmeyi ve yönetmeyi kolaylaştırmak için gereklidir. Bunu nasıl başaracağınızı anlamanıza yardımcı olmak için süreci birden fazla adıma ayıracağız.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

- Aspose.Imaging for .NET: Aspose.Imaging for .NET'in kurulu olması gerekir. adresinden indirebilirsiniz.[Aspose.Imaging for .NET web sitesi](https://releases.aspose.com/imaging/net/).

## Ad Alanlarını İçe Aktar

.NET projenize Aspose.Imaging ile çalışmak için gerekli ad alanlarını içe aktarın:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Exif;
using Aspose.Imaging.FileFormats.Dicom;
```

Şimdi Aspose.Imaging for .NET kullanarak XMP etiketlerinin saklanmasını desteklemek için adım adım kılavuza bakalım.

## 1. Adım: DICOM Görüntüsünü Yükleyin

 Çalışmak istediğiniz DICOM görüntüsünü yükleyerek başlayın. Yer değiştirmek`"Your Document Directory"` DICOM görüntünüzün bulunduğu gerçek dizin yolu ile.

```csharp
string dataDir = "Your Document Directory";
using (DicomImage image = (DicomImage)Image.Load(dataDir + "file.dcm"))
{
    // Kodunuz buraya gelecek
}
```

## 2. Adım: Bir XMP Paketi ve Dicom Paketi Oluşturun

Meta verilerinizi depolamak için bir XmpPacketWrapper ve DicomPackage oluşturun. Kurum, üretici, hasta ayrıntıları, seri bilgileri ve çalışma ayrıntıları gibi çeşitli meta veri alanlarını ayarlayabilirsiniz.

```csharp
XmpPacketWrapper xmpPacketWrapper = new XmpPacketWrapper();
DicomPackage dicomPackage = new DicomPackage();

dicomPackage.SetEquipmentInstitution("Test Institution");
dicomPackage.SetEquipmentManufacturer("Test Manufacturer");
dicomPackage.SetPatientBirthDate("19010101");
dicomPackage.SetPatientId("010101");
dicomPackage.SetPatientName("Test Name");
dicomPackage.SetPatientSex("M");
dicomPackage.SetSeriesDateTime("19020202");
dicomPackage.SetSeriesDescription("Test Series Description");
dicomPackage.SetSeriesModality("Test Modality");
dicomPackage.SetSeriesNumber("01");
dicomPackage.SetStudyDateTime("19030303");
dicomPackage.SetStudyDescription("Test Study Description");
dicomPackage.SetStudyId("02");
dicomPackage.SetStudyPhysician("Test Physician");

xmpPacketWrapper.AddPackage(dicomPackage);
```

## 3. Adım: Görüntüyü XMP Meta Verileriyle Kaydedin

 Şimdi görüntüyü eklenen XMP meta verileriyle birlikte kaydedin.`DicomOptions` sınıf.

```csharp
string outputFile = dataDir + "output.dcm";
image.Save(outputFile, new DicomOptions() { XmpData = xmpPacketWrapper });
```

## 4. Adım: XMP Etiketlerini Doğrulayın

Kaydedilen görüntüyü yükleyin ve XMP etiketlerini eklemeden önce ve sonra DICOM bilgilerini karşılaştırın.

```csharp
using (DicomImage imageSaved = (DicomImage)Image.Load(outputFile))
{
    List<string> originalDicomInfo = image.FileInfo.DicomInfo;
    List<string> imageSavedDicomInfo = imageSaved.FileInfo.DicomInfo;
    int tagsCountDiff = Math.Abs(imageSavedDicomInfo.Count - originalDicomInfo.Count);
}
```

## Çözüm

Bu eğitimde, Aspose.Imaging for .NET kullanarak XMP etiketlerinin DICOM görüntülerine kaydedilmesini nasıl destekleyeceğimizi öğrendik. Resimlerinize meta veri eklemek organizasyon ve yönetim açısından çok önemlidir. Aspose.Imaging bu süreci basitleştirir ve görüntü meta verileriyle verimli bir şekilde çalışmanıza olanak tanır.

 Daha fazla ayrıntı ve gelişmiş kullanım için bkz.[Aspose.Imaging for .NET belgeleri](https://reference.aspose.com/imaging/net/).

## SSS'ler

### S1: XMP meta verileri nedir?

Cevap1: XMP (Genişletilebilir Meta Veri Platformu), görüntüler de dahil olmak üzere dijital varlıklara meta veriler eklemeye yönelik bir standarttır. Dosyanın çeşitli niteliklerinin düzenlenmesine ve tanımlanmasına yardımcı olur.

### S2: Mevcut XMP meta verilerini Aspose.Imaging for .NET kullanarak düzenleyebilir miyim?

Cevap2: Evet, Aspose.Imaging'i kullanarak mevcut XMP meta verilerini düzenleyebilir ve görüntülere yeni meta veriler ekleyebilirsiniz.

### S3: Aspose.Imaging for .NET profesyonel görüntü işleme görevlerine uygun mu?

A3: Kesinlikle. Aspose.Imaging for .NET, görüntü işleme, düzenleme ve dönüştürme için çok çeşitli özellikler sunarak profesyonel kullanıma uygun hale getirir.

### S4: Aspose.Imaging for .NET hakkında nereden destek alabilirim veya soru sorabilirim?

 A4: ziyaret edebilirsiniz[Aspose.Imaging for .NET forumu](https://forum.aspose.com/) Destek almak ve aklınıza takılan soruları sormak için.

### S5: Aspose.Imaging for .NET için nasıl geçici lisans alabilirim?

 Cevap5: adresini ziyaret ederek Aspose.Imaging for .NET için geçici bir lisans alabilirsiniz.[bu bağlantı](https://purchase.aspose.com/temporary-license/).
