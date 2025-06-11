---
"description": "تعلّم كيفية رسم صور نقطية بتنسيق SVG باستخدام Aspose.Imaging لـ .NET. حسّن تطبيقات .NET لديك بصور ديناميكية."
"linktitle": "رسم صورة نقطية على SVG في Aspose.Imaging لـ .NET"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Aspose.Imaging .NET"
"title": "كيفية رسم صورة نقطية بتنسيق SVG في Aspose.Imaging لـ .NET"
"url": "/ar/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم صورة نقطية بتنسيق SVG في Aspose.Imaging لـ .NET


في عالم برمجة .NET، تُعدّ Aspose.Imaging مكتبةً موثوقةً ومتعددة الاستخدامات للتعامل مع مختلف المهام المتعلقة بالصور. ومن بين إمكانياتها الرائعة إمكانية رسم صورة نقطية على لوحة SVG. في هذا الدليل المُفصّل، سنشرح لك عملية رسم صورة نقطية على SVG باستخدام Aspose.Imaging لـ .NET.

## المتطلبات الأساسية

قبل أن نتعمق في التفاصيل، تأكد من أن لديك المتطلبات الأساسية التالية:

- Aspose.Imaging لـ .NET: يجب تثبيت المكتبة. إذا لم تكن كذلك، يمكنك تنزيلها من [صفحة تنزيل Aspose.Imaging لـ .NET](https://releases.aspose.com/imaging/net/).

- دليل المستندات الخاص بك: استبدال `"Your Document Directory"` مع المسار الفعلي إلى دليل العمل الخاص بك.

الآن، دعونا نقسم العملية إلى خطوات سهلة المتابعة:

## الخطوة 1: استيراد مساحات الأسماء الضرورية

يجب عليك استيراد مساحات الأسماء المطلوبة للعمل مع Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## الخطوة 2: تحميل الصور

- أولاً، قم بتحميل الصورة النقطية التي تريد رسمها على قماش SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- بعد ذلك، قم بتحميل صورة قماش SVG حيث تريد رسم الصورة النقطية.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## الخطوة 3: الرسم على صورة SVG

الآن، يمكنك البدء بالرسم على صورة SVG الحالية. للقيام بذلك، عليك إنشاء مثيل من `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## الخطوة 4: ارسم الصورة النقطية

- قم بتحديد الحدود التي تريد رسم الصورة النقطية عندها وحدد منطقة المصدر من الصورة النقطية.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## الخطوة 5: حفظ النتيجة

بعد رسم الصورة النقطية على قماش SVG، يمكنك حفظ الصورة الناتجة:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## خاتمة

تهانينا! لقد نجحت في رسم صورة نقطية على لوحة SVG باستخدام Aspose.Imaging لـ .NET. يُعد هذا مفيدًا للغاية لإنشاء صور غنية وديناميكية ضمن تطبيقات .NET.

لمزيد من المعلومات والوثائق التفصيلية، قم بزيارة [توثيق Aspose.Imaging لـ .NET](https://reference.aspose.com/imaging/net/).

## الأسئلة الشائعة

### ما هو Aspose.Imaging لـ .NET؟
   Aspose.Imaging for .NET هي مكتبة معالجة صور قوية تسمح للمطورين بإنشاء الصور ومعالجتها وتحويلها بتنسيقات مختلفة داخل تطبيقات .NET.

### هل يمكنني استخدام Aspose.Imaging لـ .NET في المشاريع التجارية؟
   نعم، يمكنك استخدام Aspose.Imaging لـ .NET في المشاريع التجارية وغير التجارية. يمكنك الاطلاع على تفاصيل الترخيص على [صفحة الشراء](https://purchase.aspose.com/buy).

### هل هناك نسخة تجريبية مجانية متاحة؟
   نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Imaging لـ .NET من [هنا](https://releases.aspose.com/).

### أين يمكنني الحصول على الدعم أو طرح الأسئلة؟
   إذا كان لديك أي أسئلة أو تحتاج إلى دعم، يمكنك زيارة [منتدى Aspose.Imaging](https://forum.aspose.com/).

### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Imaging لـ .NET؟
   يمكنك الحصول على ترخيص مؤقت من [هنا](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}