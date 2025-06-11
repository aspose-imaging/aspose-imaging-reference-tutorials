---
"description": "تعرّف على كيفية تحويل الصور المتجهة إلى صور نقطية في .NET باستخدام Aspose.Imaging. دليل خطوة بخطوة لمعالجة الصور بكفاءة."
"linktitle": "رسم صورة متجهة إلى صورة نقطية في Aspose.Imaging لـ .NET"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Aspose.Imaging .NET"
"title": "رسم صورة متجهة إلى صورة نقطية في Aspose.Imaging لـ .NET"
"url": "/ar/net/vector-image-processing/draw-vector-image-to-raster-image/"
"weight": 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# رسم صورة متجهة إلى صورة نقطية في Aspose.Imaging لـ .NET


هل ترغب في تحويل الصور المتجهة إلى صور نقطية بسهولة في تطبيقات .NET؟ يوفر Aspose.Imaging for .NET حلاً فعالاً لهذه المهمة. في هذا الدليل المفصل، سنشرح لك عملية تحويل الصور المتجهة إلى صور نقطية باستخدام Aspose.Imaging for .NET. 

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:

### 1. Aspose.Imaging لـ .NET

يجب أن يكون لديك Aspose.Imaging for .NET مُثبّتًا. إذا لم يكن مُثبّتًا لديك، يُمكنك تنزيله من الموقع الإلكتروني على [تنزيل Aspose.Imaging لـ .NET](https://releases.aspose.com/imaging/net/).

### 2. بيئة تطوير .NET

تأكد من تثبيت بيئة تطوير .NET على جهاز الكمبيوتر الخاص بك. يمكنك استخدام Visual Studio أو أي أداة تطوير .NET أخرى.

الآن، دعنا نقسم عملية تحويل الصور المتجهة إلى صور نقطية إلى خطوات بسيطة وسهلة المتابعة:

## الخطوة 1: تهيئة مشروعك

ابدأ بإنشاء مشروع .NET جديد في بيئة التطوير الخاصة بك. تأكد من دمج Aspose.Imaging for .NET في مشروعك.

## الخطوة 2: تحميل صورة المتجه

في هذه الخطوة، نقوم بتحميل الصورة المتجهة (بتنسيق SVG) التي نريد تحويلها إلى صورة نقطية.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## الخطوة 3: تحويل الصورة المتجهة إلى صورة نقطية

الآن، نحتاج إلى تحويل صورة SVG إلى صيغة PNG. هنا يتم التحويل من متجه إلى نقطي.

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## الخطوة 4: تحميل الصورة النقطية

بعد التحويل إلى صورة نقطية، قم بتحميل صورة PNG من التدفق لمزيد من الرسم.

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

أخيرًا، احفظ الصورة الناتجة. لديك الآن صورة نقطية تتضمن صورتك المتجهة.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## خاتمة

في هذا البرنامج التعليمي، شرحنا كيفية تحويل الصور المتجهة إلى صور نقطية باستخدام Aspose.Imaging لـ .NET. بهذه الخطوات البسيطة، يمكنك دمج هذه الوظيفة بسهولة في تطبيقات .NET الخاصة بك.

### الأسئلة الشائعة

### ما هو Aspose.Imaging لـ .NET؟
Aspose.Imaging for .NET هي مكتبة .NET توفر ميزات معالجة الصور القوية، بما في ذلك القدرة على العمل مع تنسيقات الصور المختلفة، وتحويل الصور، وإجراء مهام معالجة الصور المتقدمة.

### أين يمكنني العثور على الوثائق الخاصة بـ Aspose.Imaging لـ .NET؟
يمكنك العثور على الوثائق الخاصة بـ Aspose.Imaging لـ .NET [هنا](https://reference.aspose.com/imaging/net/).

### هل هناك نسخة تجريبية مجانية متاحة؟
نعم، يمكنك الوصول إلى نسخة تجريبية مجانية من Aspose.Imaging لـ .NET [هنا](https://releases.aspose.com/).

### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Imaging لـ .NET؟
إذا كنت بحاجة إلى ترخيص مؤقت، يمكنك الحصول على واحد [هنا](https://purchase.aspose.com/temporary-license/).

### أين يمكنني الحصول على الدعم لـ Aspose.Imaging لـ .NET؟
لأي دعم أو استفسارات يمكنك زيارة [منتدى Aspose.Imaging](https://forum.aspose.com/).


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}