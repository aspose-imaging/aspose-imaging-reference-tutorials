---
"description": "تعلم رسم القطع الناقص باستخدام Aspose.Imaging for .NET، وهي مكتبة متعددة الاستخدامات لمعالجة الصور. أنشئ رسومات مذهلة بسهولة."
"linktitle": "رسم القطع الناقص في Aspose.Imaging لـ .NET"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Aspose.Imaging .NET"
"title": "رسم القطع الناقص في Aspose.Imaging لـ .NET"
"url": "/ar/net/basic-drawing/draw-ellipse/"
"weight": 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# رسم القطع الناقص في Aspose.Imaging لـ .NET

في هذا البرنامج التعليمي، سنشرح لك عملية رسم القطع الناقص باستخدام Aspose.Imaging لـ .NET. Aspose.Imaging هي مكتبة فعّالة تتيح لك إنشاء صور بتنسيقات مختلفة ومعالجة هذه الصور ضمن تطبيقات .NET. سنبدأ بشرح المفهوم والمتطلبات الأساسية، ثم نقسم كل مثال إلى عدة خطوات لضمان فهم واضح.

## المتطلبات الأساسية

قبل أن نتعمق في رسم النقاط البيضاوية في Aspose.Imaging لـ .NET، يجب عليك التأكد من توفر المتطلبات الأساسية التالية لديك:

1. Visual Studio: تأكد من تثبيت Visual Studio على نظامك لتطوير .NET.

2. Aspose.Imaging لـ .NET: يجب أن يكون Aspose.Imaging لـ .NET مُثبّتًا لديك. إذا لم يكن مُثبّتًا، يُمكنك تنزيله من [صفحة التحميل](https://releases.aspose.com/imaging/net/).

3. دليل المستندات الخاص بك: قم بإنشاء دليل ستحفظ فيه الصور التي تم إنشاؤها أثناء هذا البرنامج التعليمي.

الآن بعد أن أصبح لدينا المتطلبات الأساسية، فلنبدأ.

## استيراد مساحات الأسماء

في هذه الخطوة، سنستورد مساحات الأسماء اللازمة للعمل مع Aspose.Imaging. اتبع الخطوات التالية:

### الخطوة 1: افتح مشروع Visual Studio الخاص بك

قم بتشغيل Visual Studio وافتح مشروع .NET الذي تخطط لاستخدام Aspose.Imaging فيه.

### الخطوة 2: إضافة باستخدام التوجيهات

في ملف التعليمات البرمجية الخاص بك، أضف التوجيهات التالية باستخدام لتضمين المساحات المطلوبة:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.Colors;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.FileFormats.Bmp.Options;
using Aspose.Imaging.Sources;
```

الآن بعد أن قمت باستيراد مساحات الأسماء الضرورية، فأنت جاهز لرسم شكل بيضاوي.

## رسم القطع الناقص

سنقدم الآن دليلاً خطوة بخطوة لكيفية رسم شكل بيضاوي باستخدام Aspose.Imaging لـ .NET. سيرشدك هذا المثال خلال العملية.

### الخطوة 1: إعداد ملف الإخراج

قبل رسم القطع الناقص، عليك إعداد ملف الإخراج. إليك كيفية القيام بذلك:

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

هنا، نقوم بإنشاء مثيل BmpOptions، وتعيين عمق البت، وتحديد مجرى المصدر.

### الخطوة 3: إنشاء صورة

إنشاء مثيل لـ `Image` الفئة مع الخيارات والأبعاد المحددة:

```csharp
using (Image image = Image.Create(saveOptions, 100, 100))
{
```

في هذه الخطوة نقوم بإنشاء صورة بحجم 100×100 بكسل.

### الخطوة 4: تهيئة الرسومات ومسح السطح

قم بتهيئة مثيل الرسومات ومسح سطح الصورة:

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
```

يقوم هذا الكود بإنشاء كائن رسومي ومسح الصورة ذات الخلفية الصفراء.

### الخطوة 5: ارسم القطع الناقص

الآن، دعونا نرسم القطع الناقص على الصورة:

```csharp
graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

هنا، نرسم قطع ناقص منقط باللون الأحمر وقطع ناقص متصل باللون الأزرق على الصورة.

### الخطوة 6: حفظ الصورة

وأخيرًا، احفظ الصورة:

```csharp
image.Save();
```

## خاتمة

رسم القطع الناقص في Aspose.Imaging لـ .NET عملية سهلة وبسيطة. باتباع الخطوات الموضحة في هذا البرنامج التعليمي، يمكنك بسهولة إنشاء الصور وتعديلها في تطبيقات .NET. يوفر Aspose.Imaging إمكانيات واسعة لتحرير الصور، مما يجعله أداة قيّمة للمطورين.

## الأسئلة الشائعة

### س1: ما هي الميزات الرئيسية لـ Aspose.Imaging لـ .NET؟

يوفر Aspose.Imaging لـ .NET مجموعة واسعة من الميزات، بما في ذلك إنشاء الصور ومعالجتها وتحويلها وعرضها. كما يدعم تنسيقات صور متنوعة ويوفر إمكانيات متقدمة لتحرير الصور.

### س2: هل يمكنني استخدام Aspose.Imaging لـ .NET في كل من تطبيقات Windows وتطبيقات الويب؟

نعم، يمكنك استخدام Aspose.Imaging لـ .NET في كل من تطبيقات سطح مكتب Windows وتطبيقات الويب، مما يجعله متعدد الاستخدامات لمختلف سيناريوهات التطوير.

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Imaging لـ .NET؟

نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Imaging لـ .NET من [صفحة التجربة](https://releases.aspose.com/).

### س4: أين يمكنني العثور على وثائق شاملة لـ Aspose.Imaging لـ .NET؟

يمكنك الوصول إلى الوثائق التفصيلية حول Aspose.Imaging لـ .NET على [صفحة التوثيق](https://reference.aspose.com/imaging/net/).

### س5: كيف يمكنني الحصول على الدعم لـ Aspose.Imaging لـ .NET إذا واجهت مشكلات؟

يمكنك طلب الدعم والتفاعل مع مجتمع Aspose على [المنتدى](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}