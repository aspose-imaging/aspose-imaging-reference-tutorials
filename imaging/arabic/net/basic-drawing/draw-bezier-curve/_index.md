---
"description": "تعلّم كيفية رسم منحنيات بيزير في Aspose.Imaging لـ .NET. حسّن رسومات .NET لديك بهذا الدليل المفصل."
"linktitle": "ارسم منحنى بيزير في Aspose.Imaging لـ .NET"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Aspose.Imaging .NET"
"title": "رسم منحنيات بيزير في Aspose.Imaging لـ .NET"
"url": "/ar/net/basic-drawing/draw-bezier-curve/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# رسم منحنيات بيزير في Aspose.Imaging لـ .NET

Aspose.Imaging for .NET هي مكتبة فعّالة توفر دعمًا شاملاً لمعالجة الصور. في هذا البرنامج التعليمي، سنرشدك خلال عملية رسم منحنيات بيزير باستخدام Aspose.Imaging for .NET. تُعد منحنيات بيزير أساسية لإنشاء رسومات سلسة وجذابة بصريًا في تطبيقات .NET.

## المتطلبات الأساسية

قبل أن نتعمق في رسم منحنيات بيزير، عليك التأكد من أن لديك المتطلبات الأساسية التالية:

1. Visual Studio: تأكد من تثبيت Visual Studio، حيث سنعمل على تطوير .NET.

2. Aspose.Imaging for .NET: نزّل وثبّت مكتبة Aspose.Imaging for .NET. يمكنك الحصول عليها من [رابط التحميل](https://releases.aspose.com/imaging/net/).

3. المعرفة الأساسية بلغة C#: تعرف على برمجة C# حيث سنقوم بكتابة كود C#.

4. دليل مستنداتك: خصص دليلاً لحفظ صورة الإخراج. استبدل `"Your Document Directory"` في الكود مع مسار الدليل الفعلي الخاص بك.

الآن، دعونا نقسم العملية إلى خطوات بسيطة.

## الخطوة 1: تهيئة البيئة

للبدء، افتح Visual Studio وأنشئ مشروع C# جديدًا. تأكد من إضافة مرجع إلى مكتبة Aspose.Imaging في مشروعك.

## الخطوة 2: رسم منحنى بيزير

الآن، لنكتب الكود لرسم منحنى بيزير. إليك شرحًا خطوة بخطوة:

### الخطوة 2.1: إنشاء تدفق الملفات

```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
using (FileStream stream = new FileStream(dataDir + "DrawingBezier_out.bmp", FileMode.Create))
{
    // الكود الخاص بك يذهب هنا.
}
```

يستبدل `"Your Document Directory"` مع المسار الفعلي إلى دليل المستند الذي تريد حفظ الصورة الناتجة فيه.

### الخطوة 2.2: تعيين BmpOptions

```csharp
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
saveOptions.Source = new StreamSource(stream);
```

في هذه الخطوة، نقوم بإنشاء مثيل لـ `BmpOptions` وتعيين خصائصه، مثل عدد البتات لكل بكسل ومصدر الصورة.

### الخطوة 2.3: إنشاء صورة

```csharp
using (Image image = Image.Create(saveOptions, 100, 100))
{
    // الكود الخاص بك يذهب هنا.
}
```

هنا، نقوم بإنشاء `Image` باستخدام الخيارات المحددة، يمكنك ضبط عرض وارتفاع الصورة.

### الخطوة 2.4: تهيئة الرسومات

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
```

نحن ننشئ `Graphics` الكائن وتعيين لون خلفية الصورة إلى اللون الأصفر.

### الخطوة 2.5: تحديد معلمات بيزير

```csharp
Pen BlackPen = new Pen(Color.Black, 3);
float startX = 10;
float startY = 25;
float controlX1 = 20;
float controlY1 = 5;
float controlX2 = 55;
float controlY2 = 10;
float endX = 90;
float endY = 25;
```

في هذه الخطوة، نقوم بتحديد معلمات منحنى بيزير، بما في ذلك نقاط التحكم ونقاط النهاية.

### الخطوة 2.6: ارسم منحنى بيزير

```csharp
graphic.DrawBezier(BlackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
image.Save();
```

وأخيرا، نستخدم `DrawBezier` طريقة لرسم منحنى بيزير بالمعلمات المحددة. `image.Save()` يتم استخدام الطريقة لحفظ الصورة ذات المنحنى.

## خاتمة

يُعد رسم منحنيات بيزير في Aspose.Imaging لـ .NET طريقة فعّالة لتحسين المظهر المرئي لتطبيقات .NET. باتباع هذه الخطوات البسيطة، يمكنك إنشاء رسومات سلسة وجذابة بصريًا.

الآن بعد أن تعلمت كيفية رسم منحنيات بيزير باستخدام Aspose.Imaging لـ .NET، يمكنك استكشاف المزيد من الميزات والقدرات التي توفرها هذه المكتبة متعددة الاستخدامات في مشاريع .NET الخاصة بك.

## الأسئلة الشائعة

### س1: ما هو منحنى بيزير؟

ج١: منحنى بيزير هو منحنى مُعرَّف رياضيًا ويُستخدم في الرسومات والتصميم الحاسوبي. يُحدَّد بنقاط تحكم تُؤثِّر على شكل المنحنى ومساره.

### س2: هل يمكنني تخصيص مظهر منحنى بيزير المرسوم باستخدام Aspose.Imaging؟

ج2: نعم، يمكنك تخصيص مظهر منحنى بيزير عن طريق ضبط المعلمات مثل اللون والسمك ونقاط التحكم.

### س3: هل هناك أنواع أخرى من المنحنيات التي يدعمها Aspose.Imaging؟

ج3: نعم، يدعم Aspose.Imaging لـ .NET أنواعًا مختلفة من المنحنيات، بما في ذلك منحنيات بيزير التربيعية ومنحنيات بيزير المكعبة.

### س4: هل Aspose.Imaging for .NET متوافق مع تنسيقات الصور المختلفة؟

ج4: نعم، يدعم Aspose.Imaging for .NET مجموعة واسعة من تنسيقات الصور، بما في ذلك BMP وPNG وJPEG والمزيد.

### س5: أين يمكنني العثور على موارد ودعم إضافي لـ Aspose.Imaging لـ .NET؟

أ5: يمكنك استكشاف [التوثيق](https://reference.aspose.com/imaging/net/) لـ Aspose.Imaging لـ .NET واطلب المساعدة في [منتدى Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}