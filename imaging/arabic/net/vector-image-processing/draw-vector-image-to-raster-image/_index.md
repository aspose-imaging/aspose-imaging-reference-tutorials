---
title: ارسم صورة متجهة إلى صورة نقطية في Aspose.Imaging لـ .NET
linktitle: ارسم صورة متجهة إلى صورة نقطية في Aspose.Imaging لـ .NET
second_title: Aspose.Imaging .NET واجهة برمجة تطبيقات معالجة الصور
description: تعرف على كيفية تحويل الصور المتجهة إلى صور نقطية في .NET باستخدام Aspose.Imaging. دليل خطوة بخطوة لمعالجة الصور بكفاءة.
weight: 13
url: /ar/net/vector-image-processing/draw-vector-image-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ارسم صورة متجهة إلى صورة نقطية في Aspose.Imaging لـ .NET


هل تتطلع إلى تحويل الصور المتجهة إلى صور نقطية بسهولة في تطبيقات .NET الخاصة بك؟ يوفر Aspose.Imaging for .NET حلاً فعالاً لهذه المهمة. في هذا الدليل التفصيلي خطوة بخطوة، سنرشدك خلال عملية رسم الصور المتجهة إلى الصور النقطية باستخدام Aspose.Imaging for .NET. 

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

### 1. Aspose.Imaging لـ .NET

 يجب أن يكون Aspose.Imaging for .NET مثبتًا لديك. إذا لم يكن لديك، يمكنك تنزيله من الموقع على[قم بتنزيل Aspose.Imaging لـ .NET](https://releases.aspose.com/imaging/net/).

### 2. بيئة تطوير .NET

تأكد من إعداد بيئة تطوير .NET على جهاز الكمبيوتر الخاص بك. يمكنك استخدام Visual Studio أو أي أداة تطوير .NET أخرى.

الآن، دعونا نقسم عملية رسم الصور المتجهة إلى صور نقطية إلى خطوات بسيطة وسهلة المتابعة:

## الخطوة 1: تهيئة مشروعك

ابدأ بإنشاء مشروع .NET جديد في بيئة التطوير الخاصة بك. تأكد من دمج Aspose.Imaging for .NET في مشروعك.

## الخطوة 2: تحميل الصورة المتجهة

في هذه الخطوة، نقوم بتحميل الصورة المتجهة (بتنسيق SVG) التي تريد تحويلها إلى صورة نقطية.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## الخطوة 3: تنقيط الصورة المتجهة

الآن، نحن بحاجة إلى تنقيط صورة SVG إلى تنسيق PNG. هذا هو المكان الذي يحدث فيه التحويل من المتجه إلى البيانات النقطية.

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## الخطوة 4: تحميل الصورة النقطية

بعد التنقيط، قم بتحميل صورة PNG من الدفق لمزيد من الرسم.

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## الخطوة 5: ارسم الصورة النقطية

الآن، يمكننا رسم الصورة النقطية على صورة SVG الموجودة.

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## الخطوة 6: حفظ النتيجة

وأخيراً، احفظ الصورة الناتجة. لديك الآن صورة نقطية تتضمن الصورة المتجهة الخاصة بك.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## خاتمة

في هذا البرنامج التعليمي، أوضحنا كيفية تحويل الصور المتجهة إلى صور نقطية باستخدام Aspose.Imaging for .NET. من خلال هذه الخطوات البسيطة، يمكنك دمج هذه الوظيفة بسهولة في تطبيقات .NET الخاصة بك.

### أسئلة مكررة

### ما هو Aspose.Imaging لـ .NET؟
Aspose.Imaging for .NET هي مكتبة .NET توفر ميزات قوية لمعالجة الصور، بما في ذلك القدرة على العمل مع تنسيقات الصور المختلفة، وتحويل الصور، وتنفيذ مهام معالجة الصور المتقدمة.

### أين يمكنني العثور على الوثائق الخاصة بـ Aspose.Imaging for .NET؟
 يمكنك العثور على وثائق Aspose.Imaging لـ .NET[هنا](https://reference.aspose.com/imaging/net/).

### هل هناك نسخة تجريبية مجانية متاحة؟
 نعم، يمكنك الوصول إلى النسخة التجريبية المجانية من Aspose.Imaging for .NET[هنا](https://releases.aspose.com/).

### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Imaging لـ .NET؟
 إذا كنت بحاجة إلى ترخيص مؤقت، يمكنك الحصول عليه[هنا](https://purchase.aspose.com/temporary-license/).

### أين يمكنني الحصول على الدعم لـ Aspose.Imaging لـ .NET؟
 للحصول على أي دعم أو استفسارات، يمكنك زيارة[Aspose.منتدى التصوير](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
