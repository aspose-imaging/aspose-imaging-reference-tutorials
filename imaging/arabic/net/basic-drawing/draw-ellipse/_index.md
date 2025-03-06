---
title: رسم علامات الحذف في Aspose.Imaging لـ .NET
linktitle: رسم القطع الناقص في Aspose.Imaging لـ .NET
second_title: Aspose.Imaging .NET واجهة برمجة تطبيقات معالجة الصور
description: تعلم كيفية رسم الأشكال البيضاوية في Aspose.Imaging for .NET، وهي مكتبة متعددة الاستخدامات لمعالجة الصور. قم بإنشاء رسومات مذهلة بسهولة.
weight: 12
url: /ar/net/basic-drawing/draw-ellipse/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# رسم علامات الحذف في Aspose.Imaging لـ .NET

في هذا البرنامج التعليمي، سنرشدك خلال عملية رسم القطع الناقص باستخدام Aspose.Imaging for .NET. Aspose.Imaging هي مكتبة قوية تسمح لك بمعالجة وإنشاء الصور بتنسيقات مختلفة داخل تطبيقات .NET الخاصة بك. سنبدأ بتقديم المفهوم والمتطلبات الأساسية، ثم نقسم كل مثال إلى خطوات متعددة لضمان الفهم الواضح.

## المتطلبات الأساسية

قبل أن نتعمق في رسم الأشكال البيضاوية في Aspose.Imaging for .NET، يجب عليك التأكد من توفر المتطلبات الأساسية التالية:

1. Visual Studio: تأكد من تثبيت Visual Studio على نظامك لتطوير .NET.

2.  Aspose.Imaging for .NET: يجب أن يكون Aspose.Imaging for .NET مثبتًا لديك. إذا لم يكن الأمر كذلك، يمكنك تنزيله من[صفحة التحميل](https://releases.aspose.com/imaging/net/).

3. دليل المستندات الخاص بك: قم بإنشاء دليل حيث ستحفظ الصور التي تم إنشاؤها أثناء هذا البرنامج التعليمي.

والآن بعد أن توفرت لدينا المتطلبات الأساسية، فلنبدأ.

## استيراد مساحات الأسماء

في هذه الخطوة، سنقوم باستيراد مساحات الأسماء اللازمة للعمل مع Aspose.Imaging. اتبع الخطوات التالية:

### الخطوة 1: افتح مشروع Visual Studio الخاص بك

قم بتشغيل Visual Studio وافتح مشروع .NET الخاص بك حيث تخطط لاستخدام Aspose.Imaging.

### الخطوة 2: إضافة باستخدام التوجيهات

في ملف التعليمات البرمجية الخاص بك، قم بإضافة ما يلي باستخدام التوجيهات لتضمين مساحات الأسماء المطلوبة:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.Colors;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.FileFormats.Bmp.Options;
using Aspose.Imaging.Sources;
```

الآن بعد أن قمت باستيراد مساحات الأسماء الضرورية، أصبحت جاهزًا لرسم شكل بيضاوي.

## رسم القطع الناقص

سنقدم الآن دليلاً خطوة بخطوة حول كيفية رسم شكل بيضاوي باستخدام Aspose.Imaging for .NET. هذا المثال سوف يرشدك خلال هذه العملية.

### الخطوة 1: إعداد ملف الإخراج

قبل رسم شكل بيضاوي، تحتاج إلى إعداد ملف الإخراج. وإليك كيف يمكنك القيام بذلك:

```csharp
string dataDir = "Your Document Directory";
using (FileStream stream = new FileStream(dataDir + "DrawingEllipse_out.bmp", FileMode.Create))
{
```

في مقتطف التعليمات البرمجية هذا، نقوم بإنشاء FileStream لتحديد مسار ملف الإخراج.

### الخطوة 2: تكوين BmpOptions

لتكوين تنسيق BMP والخصائص الأخرى، استخدم الكود التالي:

```csharp
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
saveOptions.Source = new StreamSource(stream);
```

هنا، نقوم بإنشاء مثيل BmpOptions، وتعيين عمق البت، وتحديد التدفق المصدر.

### الخطوة 3: إنشاء صورة

 إنشاء مثيل لـ`Image` فئة مع الخيارات والأبعاد المحددة:

```csharp
using (Image image = Image.Create(saveOptions, 100, 100))
{
```

في هذه الخطوة، نقوم بإنشاء صورة بحجم 100x100 بكسل.

### الخطوة 4: تهيئة الرسومات ومسح السطح

تهيئة مثيل الرسومات ومسح سطح الصورة:

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
```

يقوم هذا الرمز بإنشاء كائن رسومي ومسح الصورة بخلفية صفراء.

### الخطوة 5: رسم علامات الحذف

الآن لنرسم أشكالًا بيضاوية على الصورة:

```csharp
graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

هنا، نرسم قطعًا ناقصًا باللون الأحمر وقطعًا ناقصًا باللون الأزرق على الصورة.

### الخطوة 6: احفظ الصورة

وأخيراً احفظ الصورة:

```csharp
image.Save();
```

## خاتمة

يعد رسم علامات الحذف في Aspose.Imaging لـ .NET عملية مباشرة. باستخدام الخطوات الموضحة في هذا البرنامج التعليمي، يمكنك بسهولة إنشاء الصور ومعالجتها في تطبيقات .NET الخاصة بك. يوفر Aspose.Imaging نطاقًا واسعًا من إمكانيات تحرير الصور، مما يجعله أداة قيمة للمطورين.

## الأسئلة الشائعة

### س1: ما هي الميزات الرئيسية لبرنامج Aspose.Imaging لـ .NET؟

يوفر Aspose.Imaging for .NET نطاقًا واسعًا من الميزات، بما في ذلك إنشاء الصور ومعالجتها وتحويلها وعرضها. وهو يدعم تنسيقات الصور المختلفة ويوفر إمكانات متقدمة لتحرير الصور.

### س2: هل يمكنني استخدام Aspose.Imaging for .NET في كل من تطبيقات Windows والويب؟

نعم، يمكنك استخدام Aspose.Imaging for .NET في كل من تطبيقات سطح مكتب Windows وتطبيقات الويب، مما يجعله متعدد الاستخدامات لسيناريوهات التطوير المختلفة.

### س3: هل هناك إصدار تجريبي مجاني متاح لـ Aspose.Imaging for .NET؟

 نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Imaging لـ .NET من[صفحة تجريبية](https://releases.aspose.com/).

### س4: أين يمكنني العثور على وثائق شاملة لـ Aspose.Imaging for .NET؟

 يمكنك الوصول إلى الوثائق التفصيلية حول Aspose.Imaging for .NET على الموقع[صفحة التوثيق](https://reference.aspose.com/imaging/net/).

### س5: كيف يمكنني الحصول على دعم Aspose.Imaging لـ .NET إذا واجهت مشكلات؟

 يمكنك طلب الدعم والتفاعل مع مجتمع Aspose على[المنتدى](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
