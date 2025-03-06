---
title: الثنائية مع عتبة برادلي التكيفية على صورة DICOM في Aspose.Imaging for .NET
linktitle: الثنائية مع عتبة برادلي التكيفية على صورة DICOM في Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET واجهة برمجة تطبيقات معالجة الصور
description: تعلم كيفية تطبيق عتبة التكيف الخاصة ببرادلي على صور DICOM باستخدام Aspose.Imaging for .NET. أصبحت عملية الثنائية سهلة باستخدام دليل خطوة بخطوة.
weight: 14
url: /ar/net/dicom-image-processing/binarization-with-bradleys-adaptive-threshold-on-dicom-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# الثنائية مع عتبة برادلي التكيفية على صورة DICOM في Aspose.Imaging for .NET

هل تتطلع إلى تطبيق عتبة التكيف الخاصة ببرادلي على صورة DICOM باستخدام Aspose.Imaging for .NET؟ في هذا البرنامج التعليمي الشامل، سنرشدك خلال العملية خطوة بخطوة. بحلول نهاية هذا الدليل، ستكون قادرًا على إجراء عملية التحويل الثنائي على صور DICOM بكفاءة. سنغطي كل شيء بدءًا من المتطلبات الأساسية وحتى استيراد مساحات الأسماء وتقسيم كل مثال إلى خطوات متعددة.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، دعونا نتأكد من أن لديك كل ما تحتاجه للبدء.

1. Aspose.Imaging لـ .NET

 تأكد من تثبيت Aspose.Imaging for .NET على نظامك. يمكنك تنزيله من الموقع[هنا](https://releases.aspose.com/imaging/net/).

2. صورة ديكوم

قم بإعداد صورة DICOM التي تريد تحويلها إلى صيغة ثنائية. يجب أن يكون لديك مسار الملف إلى صورة DICOM جاهزًا للمعالجة.

## استيراد مساحات الأسماء

في هذا القسم، سوف نقوم باستيراد مساحات الأسماء الضرورية للعمل مع Aspose.Imaging لـ .NET. هذه الخطوة ضرورية لإتاحة كافة الوظائف للتعليمات البرمجية الخاصة بك.


```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.FileFormats.Bmp;
```

الآن بعد أن قمنا باستيراد مساحات الأسماء الأساسية، دعنا ننتقل إلى العملية الرئيسية للتحويل الثنائي.

سنقوم الآن بتقسيم عملية التحويل الثنائي إلى خطوات متعددة، مما يضمن أنه يمكنك بسهولة متابعة وفهم كل جزء من التعليمات البرمجية.

## الخطوة 1: قم بتحميل صورة DICOM

أولاً، نحتاج إلى تحميل صورة DICOM للتحويل الثنائي. تأكد من أن لديك المسار الصحيح لصورة DICOM الخاصة بك.

```csharp
string dataDir = "Your Document Directory";
string inputFile = dataDir + "image.dcm";

using (var fileStream = new FileStream(inputFile, FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
{
    // سيتم وضع الرمز الخاص بك هنا
}
```

## الخطوة 2: ثنائية الصورة

الآن، حان الوقت لتطبيق عتبة التكيف الخاصة ببرادلي لتحويل الصورة إلى صيغة ثنائية.

```csharp
// قم بتضمين الصورة باستخدام عتبة برادلي التكيفية واحفظ الصورة الناتجة.
image.BinarizeBradley(10);
```

## الخطوة 3: احفظ الصورة الثنائية

احفظ الصورة الثنائية في الموقع المطلوب باستخدام تنسيق BMP.

```csharp
image.Save(dataDir + "BinarizationWithBradleysAdaptiveThreshold_out.bmp", new BmpOptions());
```

## خاتمة

في هذا البرنامج التعليمي، قمنا بتغطية العملية الكاملة للتحويل الثنائي باستخدام عتبة التكيف الخاصة ببرادلي على صورة DICOM باستخدام Aspose.Imaging for .NET. لقد تعلمت المتطلبات الأساسية، وكيفية استيراد مساحات الأسماء، ودليل خطوة بخطوة لتحويل الصورة إلى ثنائي. ومن خلال هذه المعرفة، يمكنك معالجة صور DICOM بكفاءة لتلبية احتياجاتك الخاصة.

الآن لديك الأدوات والمعرفة اللازمة لتعزيز قدرات معالجة الصور لديك باستخدام Aspose.Imaging for .NET.

## الأسئلة الشائعة

### س1: ما هي عتبة برادلي للتكيف؟

A1: عتبة التكيف الخاصة برادلي هي أسلوب يستخدم في معالجة الصور لفصل المقدمة والخلفية للصورة استنادًا إلى قيم العتبة التكيفية.

### س2: هل يمكنني معالجة عدة صور DICOM دفعة واحدة؟

ج2: نعم، يمكنك التكرار عبر صور DICOM المتعددة وتطبيق عملية التحويل الثنائي كما هو موضح في هذا البرنامج التعليمي.

### س3: أين يمكنني العثور على المزيد من وثائق Aspose.Imaging لـ .NET؟

 ج3: يمكنك استكشاف الوثائق[هنا](https://reference.aspose.com/imaging/net/)للحصول على معلومات تفصيلية حول استخدام Aspose.Imaging لـ .NET.

### س4: هل هناك إصدار تجريبي متاح لـ Aspose.Imaging for .NET؟

 ج4: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية[هنا](https://releases.aspose.com/) لاختبار البرنامج قبل إجراء عملية الشراء.

### س5: كيف يمكنني الحصول على دعم Aspose.Imaging لـ .NET؟

 ج5: يمكنك الانضمام إلى مجتمع Aspose والحصول على الدعم من زملائك المطورين على[منتدى أسبوز](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
