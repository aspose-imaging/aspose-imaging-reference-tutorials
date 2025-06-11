---
"description": "تعلّم كيفية رسم صور نقطية على ملفات EMF باستخدام Aspose.Imaging لـ .NET. أنشئ صورًا مذهلة بكل سهولة."
"linktitle": "رسم صورة نقطية على EMF في Aspose.Imaging لـ .NET"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Aspose.Imaging .NET"
"title": "رسم صور نقطية على EMF باستخدام Aspose.Imaging لـ .NET"
"url": "/ar/net/vector-image-processing/draw-raster-image-on-emf/"
"weight": 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# رسم صور نقطية على EMF باستخدام Aspose.Imaging لـ .NET


## مقدمة

مرحبًا بكم في هذا البرنامج التعليمي خطوة بخطوة حول كيفية رسم صورة نقطية على ملف EMF (ملف تعريفي مُحسَّن) باستخدام Aspose.Imaging لـ .NET. Aspose.Imaging هي مكتبة فعّالة تتيح لك العمل مع تنسيقات صور متنوعة في تطبيقات .NET. في هذا البرنامج التعليمي، سنرشدك خلال عملية رسم صورة نقطية على ملف EMF. ستتعلم كيفية استيراد مساحات الأسماء اللازمة، وسنُقسّم كل مثال إلى عدة خطوات لتسهيل عملية التعلم.

دعونا نبدأ!

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، يجب أن يكون لديك المتطلبات الأساسية التالية:

1. Visual Studio: يجب أن يكون لديك Visual Studio مثبتًا على جهاز الكمبيوتر الخاص بك لتتمكن من كتابة وتشغيل كود .NET.

2. Aspose.Imaging لـ .NET: تأكد من تثبيت Aspose.Imaging لـ .NET. يمكنك تنزيله من [هنا](https://releases.aspose.com/imaging/net/).

3. صورة نقطية: قم بإعداد صورة نقطية (على سبيل المثال، ملف PNG) التي تريد رسمها على ملف EMF.

## استيراد مساحات الأسماء

في مشروع Visual Studio، ستحتاج إلى استيراد مساحات الأسماء اللازمة للعمل مع Aspose.Imaging. أضف مساحات الأسماء التالية إلى ملف الكود الخاص بك:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Emf;
using Aspose.Imaging.FileFormats.Png;
using Aspose.Imaging.Graphics;
using System;
```

الآن بعد أن أصبح لدينا المتطلبات الأساسية ومساحات الأسماء في مكانها، دعنا نقسم المثال إلى خطوات متعددة.

## الخطوة 1: تحميل الصورة المراد رسمها

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
{
    // الكود الخاص بالخطوة 1 يذهب هنا
}
```

في هذه الخطوة، نقوم بتحميل الصورة النقطية التي نريد رسمها على ملف EMF. استبدل `"Your Document Directory"` مع المسار إلى صورتك.

## الخطوة 2: تحميل سطح رسم EMF

```csharp
using (EmfImage canvasImage = (EmfImage)Image.Load(dataDir + "input.emf"))
{
    // الكود الخاص بالخطوة 2 يذهب هنا
}
```

هنا، نقوم بتحميل ملف EMF الذي سيُستخدم كسطح رسم لصورتنا. تأكد من استبدال `"input.emf"` مع المسار إلى ملف EMF الخاص بك.

## الخطوة 3: إنشاء رسومات مسجل EMF

```csharp
EmfRecorderGraphics2D graphics = EmfRecorderGraphics2D.FromEmfImage(canvasImage);
```

في هذه الخطوة، نقوم بإنشاء مثيل لـ `EmfRecorderGraphics2D` من صورة EMF. هذا يسمح لنا بتسجيل عمليات الرسم.

## الخطوة 4: ارسم الصورة النقطية

```csharp
graphics.DrawImage(
    imageToDraw,
    new Rectangle(67, 67, canvasImage.Width, canvasImage.Height),
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    GraphicsUnit.Pixel);
```

في هذه الخطوة نستخدم `DrawImage` طريقة لرسم الصورة النقطية المُحمَّلة على ملف EMF. يمكنك تحديد مستطيلي المصدر والوجهة للتحكم في موضع وحجم الصورة المرسومة.

## الخطوة 5: حفظ صورة النتيجة

```csharp
using (EmfImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "input.DrawImage.emf");
}
```

أخيرًا، نحفظ صورة EMF الناتجة مع الصورة النقطية المرسومة في ملف. سيتم حفظ الملف باسم "input.DrawImage.emf" في المجلد المحدد بواسطة `dataDir`.

تهانينا! لقد نجحت في رسم صورة نقطية على ملف EMF باستخدام Aspose.Imaging لـ .NET. لا تتردد في استكشاف وتجربة مستطيلات المصدر والوجهة المختلفة لتحقيق التأثيرات المطلوبة.

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية استخدام Aspose.Imaging لـ .NET لرسم صورة نقطية على ملف EMF. باتباع هذا الدليل خطوة بخطوة، يمكنك بسهولة دمج هذه الوظيفة في تطبيقات .NET.

استمتع بإنشاء صور مذهلة مع Aspose.Imaging!

## الأسئلة الشائعة

### 1. هل يمكنني رسم صور متعددة على نفس ملف EMF؟

نعم، يمكنك رسم صور متعددة على نفس ملف EMF عن طريق تكرار عملية الرسم باستخدام مستطيلات مصدر ووجهة مختلفة.

### 2. هل Aspose.Imaging متوافق مع .NET Core؟

نعم، Aspose.Imaging for .NET متوافق مع كل من .NET Framework و.NET Core.

### 3. كيف يمكنني تطبيق التحولات على الصورة المرسومة، مثل التدوير أو التدرج؟

يمكنك تطبيق التحويلات عن طريق معالجة مستطيلات المصدر والوجهة في `DrawImage` طريقة.

### 4. هل يمكنني رسم الرسومات المتجهة على ملف EMF أيضًا؟

نعم، يمكنك رسم الرسومات والأشكال المتجهة بالإضافة إلى الصور النقطية باستخدام Aspose.Imaging لـ .NET.

### 5. أين يمكنني الحصول على الدعم لـ Aspose.Imaging؟

للحصول على الدعم والمساعدة، يمكنك زيارة منتدى Aspose.Imaging [هنا](https://forum.aspose.com/).


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}