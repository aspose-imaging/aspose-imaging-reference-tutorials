---
"description": "تعلّم كيفية ضبط جاما في صور DICOM باستخدام Aspose.Imaging لـ .NET. حسّن جودة الصور الطبية بخطوات بسيطة."
"linktitle": "ضبط جاما لصورة DICOM في Aspose.Imaging لـ .NET"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Aspose.Imaging .NET"
"title": "ضبط جاما صورة DICOM باستخدام Aspose.Imaging لـ .NET"
"url": "/ar/net/dicom-image-processing/adjust-gamma-of-dicom-image/"
"weight": 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# ضبط جاما صورة DICOM باستخدام Aspose.Imaging لـ .NET

عند العمل مع الصور الطبية، غالبًا ما يتطلب الأمر تعديلات دقيقة لتحسين جودتها ووضوحها. Aspose.Imaging for .NET هي مكتبة فعّالة تتيح لك التعامل مع تنسيقات صور متنوعة، بما في ذلك DICOM (التصوير الرقمي والاتصالات في الطب). في هذا الدليل التفصيلي، سنشرح لك عملية ضبط جاما لصورة DICOM باستخدام Aspose.Imaging for .NET.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:

1. Aspose.Imaging لـ .NET: ستحتاج إلى تثبيت Aspose.Imaging لـ .NET. إذا لم يكن مثبتًا لديك بالفعل، يمكنك [قم بتحميله هنا](https://releases.aspose.com/imaging/net/).

2. الوصول إلى صورة DICOM: قم بإعداد صورة DICOM التي تريد العمل بها وتأكد من تخزينها في مكان يمكنك الوصول إليه.

3. بيئة التطوير: يجب أن يكون لديك بيئة تطوير .NET مهيأة، بما في ذلك Visual Studio أو محرر أكواد مشابه.

## استيراد مساحات الأسماء الضرورية

في مشروع .NET الخاص بك، ستحتاج إلى استيراد مساحات الأسماء اللازمة للعمل مع Aspose.Imaging. أضف مساحات الأسماء التالية إلى الكود الخاص بك:

```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
```

الآن، دعونا نقوم بتقسيم عملية ضبط جاما لصورة DICOM إلى خطوات متعددة.

## الخطوة 1: تحميل صورة DICOM

للبدء، حمّل صورة DICOM من الملف المحدد. تأكد من تحديد مسار الملف الصحيح لصورة DICOM.

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
{
    // سيتم وضع الكود الخاص بك هنا
}
```

## الخطوة 2: ضبط قيمة جاما

الآن، يمكنك ضبط جاما صورة DICOM المُحمّلة. في هذا المثال، عيّنّا قيمة جاما إلى 50، ولكن يمكنك تعديلها وفقًا لمتطلباتك الخاصة.

```csharp
image.AdjustGamma(50);
```

## الخطوة 3: إنشاء مثيل لـ BmpOptions

لحفظ صورة DICOM المعدلة كملف خريطة نقطية (BMP)، قم بإنشاء مثيل لـ `BmpOptions`.

```csharp
var bmpOptions = new BmpOptions();
```

## الخطوة 4: حفظ الصورة الناتجة

احفظ الصورة الناتجة مع جاما المعدلة كملف BMP.

```csharp
image.Save(dataDir + "AdjustGammaDICOM_out.bmp", bmpOptions);
```

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية ضبط جاما لصورة DICOM باستخدام Aspose.Imaging لـ .NET. تُسهّل هذه المكتبة معالجة الصور الطبية، مما يضمن أعلى جودة ووضوح للمتخصصين الطبيين.

من خلال اتباع هذه الخطوات البسيطة، يمكنك تحسين جودة الصورة المرئية لصور DICOM، مما يجعلها أكثر إفادة وفائدة للتشخيص الطبي.

لمزيد من المعلومات والاستخدام المتقدم لـ Aspose.Imaging لـ .NET، راجع [التوثيق](https://reference.aspose.com/imaging/net/).

## الأسئلة الشائعة

### س1: ما هو تعديل جاما في التصوير الطبي؟

ج١: تعديل جاما هو تقنية تُستخدم للتحكم في سطوع وتباين الصور الطبية، مثل الأشعة السينية أو الرنين المغناطيسي. يُحسّن هذا التعديل وضوح الصورة ودقة التشخيص.

### س2: هل يمكنني تعديل جاما صور DICOM مجانًا؟

ج٢: يُقدّم Aspose.Imaging for .NET نسخة تجريبية مجانية تُتيح لك تقييم ميزاته. مع ذلك، قد يلزم الحصول على ترخيص صالح للاستخدام في الإنتاج.

### س3: هل هناك أي مكتبات بديلة لمعالجة صور DICOM في .NET؟

ج3: نعم، هناك مكتبات أخرى مثل DicomObjects وLEADTOOLS التي يمكن استخدامها لمعالجة صور DICOM.

### س4: ما هي مهام معالجة الصور الأخرى التي يمكنني القيام بها باستخدام Aspose.Imaging لـ .NET؟

A4: يوفر Aspose.Imaging لـ .NET مجموعة واسعة من الميزات، بما في ذلك اقتصاص الصورة، وتغيير حجمها، وتدويرها، وتحويل التنسيق.

### س5: كيف يمكنني الحصول على الدعم الفني لـ Aspose.Imaging لـ .NET؟

ج5: للحصول على المساعدة الفنية ودعم المجتمع، يمكنك زيارة [منتدى Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}