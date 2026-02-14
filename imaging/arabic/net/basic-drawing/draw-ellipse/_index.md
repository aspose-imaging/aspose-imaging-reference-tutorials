---
date: 2026-02-14
description: تعلم كيفية رسم إهليلج في Aspose.Imaging لـ .NET، وهي مكتبة متعددة الاستخدامات
  لمعالجة الصور. أنشئ رسومات مذهلة بسهولة.
linktitle: How to Draw Ellipse in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: كيفية رسم إهليلج في Aspose.Imaging لـ .NET
url: /ar/net/basic-drawing/draw-ellipse/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم القطع الناقص باستخدام Aspose.Imaging لـ .NET

في هذا البرنامج التعليمي، سنوضح لك **كيفية رسم القطع الناقص** باستخدام Aspose.Imaging لـ .NET. Aspose.Imaging هي مكتبة قوية تتيح لك تعديل وإنشاء الصور بمختلف الصيغ داخل تطبيقات .NET الخاصة بك. سنبدأ بتقديم المفهوم والمتطلبات المسبقة، ثم نقسم كل مثال إلى عدة خطوات لضمان فهم واضح.

## إجابات سريعة
- **ما المكتبة المستخدمة؟** Aspose.Imaging for .NET  
- **كم من الوقت تستغرق العملية؟** حوالي 10 دقائق لرسم قطع ناقص أساسي  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ الترخيص مطلوب للإنتاج  
- **هل يمكنني تعيين خلفية الصورة؟** نعم – استخدم `Graphics.Clear` لتعيين أي لون خلفية  
- **هل هذا متوافق مع .NET 6+؟** بالتأكيد، الـ API يعمل مع جميع إصدارات .NET الحديثة  

## المتطلبات المسبقة

قبل أن نبدأ في رسم القطع الناقص باستخدام Aspose.Imaging لـ .NET، يجب التأكد من توفر المتطلبات التالية:

1. Visual Studio: تأكد من تثبيت Visual Studio على نظامك لتطوير .NET.  
2. Aspose.Imaging لـ .NET: يجب أن تكون قد ثبتت Aspose.Imaging لـ .NET. إذا لم يكن كذلك، يمكنك تنزيله من [صفحة التحميل](https://releases.aspose.com/imaging/net/).  
3. دليل المستندات الخاص بك: أنشئ دليلًا لحفظ الصور التي سيتم إنشاؤها خلال هذا البرنامج التعليمي.  

الآن بعد أن تم توفير المتطلبات المسبقة، لنبدأ.

## استيراد مساحات الأسماء

في هذه الخطوة، سنستورد مساحات الأسماء الضرورية للعمل مع Aspose.Imaging. اتبع الخطوات أدناه:

### الخطوة 1: فتح مشروع Visual Studio الخاص بك

شغّل Visual Studio وافتح مشروع .NET الذي تخطط لاستخدام Aspose.Imaging فيه.

### الخطوة 2: إضافة توجيهات using

في ملف الكود الخاص بك، أضف توجيهات using التالية لتضمين مساحات الأسماء المطلوبة:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.Colors;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.FileFormats.Bmp.Options;
using Aspose.Imaging.Sources;
```

الآن بعد أن استوردت مساحات الأسماء الضرورية، أنت جاهز لرسم القطع الناقص.

## كيفية رسم القطع الناقص باستخدام Aspose.Imaging

سنقدم الآن دليلًا خطوة بخطوة حول **كيفية رسم القطع الناقص** باستخدام Aspose.Imaging لـ .NET. سيوجهك هذا المثال خلال العملية.

### الخطوة 1: إعداد ملف الإخراج

قبل رسم القطع الناقص، تحتاج إلى إعداد ملف الإخراج. إليك كيفية القيام بذلك:

```csharp
string dataDir = "Your Document Directory";
using (FileStream stream = new FileStream(dataDir + "DrawingEllipse_out.bmp", FileMode.Create))
{
```

في هذا المقتطف البرمجي، نقوم بإنشاء `FileStream` لتحديد مسار ملف الإخراج.

### الخطوة 2: تكوين BmpOptions

لتكوين صيغة BMP والخصائص الأخرى، استخدم الكود التالي:

```csharp
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
saveOptions.Source = new StreamSource(stream);
```

هنا، ننشئ كائن `BmpOptions`، نحدد عمق البت، ونحدد تدفق المصدر.

### الخطوة 3: إنشاء صورة

أنشئ مثيلًا من فئة `Image` باستخدام الخيارات والأبعاد المحددة:

```csharp
using (Image image = Image.Create(saveOptions, 100, 100))
{
```

في هذه الخطوة، ننشئ صورة بحجم 100 × 100 بكسل.

## كيفية تعيين خلفية الصورة

خلفية نظيفة تجعل القطع الناقص يبرز. يمكنك تعيين أي لون خلفية قبل رسم الأشكال.

### الخطوة 4: تهيئة Graphics ومسح السطح

تهيئة كائن `Graphics` ومسح سطح الصورة:

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
```

هذا الكود ينشئ كائن `Graphics` و**يضبط خلفية الصورة** إلى اللون الأصفر، مُعدًا لوحة رسم.

## إنشاء رسومات مخصصة باستخدام Aspose.Imaging

بمجرد أن تصبح اللوحة جاهزة، يمكنك البدء في إنشاء رسومات مخصصة مثل القطع الناقص، الخطوط، أو المضلعات.

### الخطوة 5: رسم القطع الناقص

الآن، دعنا نرسم القطع الناقص على الصورة:

```csharp
graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

هنا، نرسم قطعًا ناقصًا أحمر وقطعًا ناقصًا أزرق صلب على الصورة.

### الخطوة 6: حفظ الصورة

أخيرًا، احفظ الصورة:

```csharp
image.Save();
```

## الخلاصة

رسم القطع الناقص في Aspose.Imaging لـ .NET عملية بسيطة. مع الخطوات الموضحة في هذا البرنامج التعليمي، يمكنك بسهولة إنشاء وتعديل الصور في تطبيقات .NET الخاصة بك. توفر Aspose.Imaging مجموعة واسعة من إمكانيات تحرير الصور، مما يجعلها أداة قيمة للمطورين. الآن تعرف **كيفية رسم القطع الناقص** ويمكنك توسيع هذه المعرفة لإنشاء رسومات أكثر غنى.

## الأسئلة المتكررة

### س1: ما هي الميزات الرئيسية لـ Aspose.Imaging لـ .NET؟

توفر Aspose.Imaging لـ .NET مجموعة واسعة من الميزات، بما في ذلك إنشاء الصور، تعديلها، تحويلها، وعرضها. تدعم صيغ صور متعددة وتوفر إمكانيات تحرير صور متقدمة.

### س2: هل يمكنني استخدام Aspose.Imaging لـ .NET في كل من تطبيقات Windows وتطبيقات الويب؟

نعم، يمكنك استخدام Aspose.Imaging لـ .NET في كل من تطبيقات سطح المكتب على Windows وتطبيقات الويب، مما يجعلها متعددة الاستخدامات لمختلف سيناريوهات التطوير.

### س3: هل تتوفر نسخة تجريبية مجانية لـ Aspose.Imaging لـ .NET؟

نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Imaging لـ .NET من [صفحة التجربة](https://releases.aspose.com/).

### س4: أين يمكنني العثور على وثائق شاملة لـ Aspose.Imaging لـ .NET؟

يمكنك الوصول إلى وثائق مفصلة حول Aspose.Imaging لـ .NET على [صفحة الوثائق](https://reference.aspose.com/imaging/net/).

### س5: كيف يمكنني الحصول على الدعم لـ Aspose.Imaging لـ .NET إذا واجهت مشاكل؟

يمكنك طلب الدعم والتفاعل مع مجتمع Aspose على [المنتدى](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-02-14  
**تم الاختبار مع:** Aspose.Imaging لـ .NET (أحدث إصدار)  
**المؤلف:** Aspose