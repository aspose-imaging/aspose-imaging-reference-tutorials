---
title: كيفية رسم صورة نقطية على SVG في Aspose.Imaging لـ .NET
linktitle: ارسم صورة نقطية على SVG في Aspose.Imaging لـ .NET
second_title: Aspose.Imaging .NET واجهة برمجة تطبيقات معالجة الصور
description: تعرف على كيفية رسم الصور النقطية على SVG باستخدام Aspose.Imaging for .NET. قم بتحسين تطبيقات .NET الخاصة بك باستخدام الصور الديناميكية.
type: docs
weight: 11
url: /ar/net/vector-image-processing/draw-raster-image-on-svg/
---

في عالم برمجة .NET، تعتبر Aspose.Imaging مكتبة موثوقة ومتعددة الاستخدامات للتعامل مع المهام المختلفة المتعلقة بالصور. إحدى الإمكانيات الرائعة التي تقدمها هي القدرة على رسم صورة نقطية على قماش SVG. في هذا الدليل المفصّل خطوة بخطوة، سنرشدك خلال عملية رسم صورة نقطية على ملف SVG باستخدام Aspose.Imaging for .NET.

## المتطلبات الأساسية

قبل أن نتعمق في التفاصيل، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.Imaging for .NET: يجب أن تكون المكتبة مثبتة لديك. إذا لم يكن الأمر كذلك، يمكنك تنزيله من[صفحة تنزيل Aspose.Imaging لـ .NET](https://releases.aspose.com/imaging/net/).

-  دليل المستندات الخاص بك: استبدال`"Your Document Directory"` مع المسار الفعلي إلى دليل العمل الخاص بك.

الآن، دعونا نقسم العملية إلى خطوات سهلة المتابعة:

## الخطوة 1: استيراد مساحات الأسماء الضرورية

تحتاج إلى استيراد مساحات الأسماء المطلوبة للعمل مع Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## الخطوة 2: تحميل الصور

- أولاً، قم بتحميل الصورة النقطية التي تريد رسمها على لوحة SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- بعد ذلك، قم بتحميل صورة قماش SVG حيث تريد رسم الصورة النقطية.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## الخطوة 3: الرسم على صورة SVG

 الآن، يمكنك البدء في الرسم على صورة SVG الموجودة. للقيام بذلك، تحتاج إلى إنشاء مثيل`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## الخطوة 4: ارسم الصورة النقطية

- حدد الحدود التي تريد رسم الصورة النقطية فيها وحدد المنطقة المصدر من الصورة النقطية.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## الخطوة 5: حفظ النتيجة

بعد رسم الصورة النقطية على لوحة SVG، يمكنك حفظ الصورة الناتجة:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## خاتمة

تهانينا! لقد نجحت في رسم صورة نقطية على لوحة SVG باستخدام Aspose.Imaging for .NET. يمكن أن يكون هذا مفيدًا بشكل لا يصدق لإنشاء صور غنية وديناميكية داخل تطبيقات .NET الخاصة بك.

 لمزيد من المعلومات والوثائق التفصيلية، قم بزيارة[Aspose.Imaging لوثائق .NET](https://reference.aspose.com/imaging/net/).

## أسئلة مكررة

### ما هو Aspose.Imaging لـ .NET؟
   Aspose.Imaging for .NET هي مكتبة قوية لمعالجة الصور تتيح للمطورين إنشاء الصور ومعالجتها وتحويلها بتنسيقات مختلفة داخل تطبيقات .NET.

### هل يمكنني استخدام Aspose.Imaging for .NET في المشاريع التجارية؟
    نعم، يمكنك استخدام Aspose.Imaging for .NET في كل من المشاريع التجارية وغير التجارية. يمكن العثور على تفاصيل الترخيص على[صفحة الشراء](https://purchase.aspose.com/buy).

### هل هناك نسخة تجريبية مجانية متاحة؟
    نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Imaging لـ .NET من[هنا](https://releases.aspose.com/).

### أين يمكنني الحصول على الدعم أو طرح الأسئلة؟
    إذا كان لديك أي أسئلة أو كنت بحاجة إلى الدعم، يمكنك زيارة[Aspose.منتدى التصوير](https://forum.aspose.com/).

### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Imaging لـ .NET؟
    يمكنك الحصول على ترخيص مؤقت من[هنا](https://purchase.aspose.com/temporary-license/).


