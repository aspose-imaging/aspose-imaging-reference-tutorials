---
title: ارسم صورًا نقطية على EMF باستخدام Aspose.Imaging لـ .NET
linktitle: ارسم صورة نقطية على EMF في Aspose.Imaging لـ .NET
second_title: Aspose.Imaging .NET واجهة برمجة تطبيقات معالجة الصور
description: تعرف على كيفية رسم الصور النقطية على ملفات EMF باستخدام Aspose.Imaging for .NET. قم بإنشاء صور مذهلة دون عناء.
weight: 10
url: /ar/net/vector-image-processing/draw-raster-image-on-emf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ارسم صورًا نقطية على EMF باستخدام Aspose.Imaging لـ .NET


## مقدمة

مرحبًا بك في هذا البرنامج التعليمي خطوة بخطوة حول كيفية رسم صورة نقطية على EMF (ملف تعريف محسّن) باستخدام Aspose.Imaging for .NET. Aspose.Imaging هي مكتبة قوية تسمح لك بالعمل مع تنسيقات الصور المختلفة في تطبيقات .NET الخاصة بك. سنرشدك في هذا البرنامج التعليمي خلال عملية رسم صورة نقطية على ملف EMF. ستتعلم كيفية استيراد مساحات الأسماء الضرورية، وسنقوم بتقسيم كل مثال إلى خطوات متعددة لتسهيل عملية التعلم.

هيا بنا نبدأ!

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، يجب أن تتوفر لديك المتطلبات الأساسية التالية:

1. Visual Studio: تحتاج إلى تثبيت Visual Studio على جهاز الكمبيوتر الخاص بك لكتابة وتشغيل تعليمات NET البرمجية.

2.  Aspose.Imaging for .NET: تأكد من تثبيت Aspose.Imaging for .NET. يمكنك تنزيله من[هنا](https://releases.aspose.com/imaging/net/).

3. صورة نقطية: قم بإعداد صورة نقطية (على سبيل المثال، ملف PNG) التي تريد رسمها على ملف EMF.

## استيراد مساحات الأسماء

في مشروع Visual Studio الخاص بك، ستحتاج إلى استيراد مساحات الأسماء الضرورية للعمل مع Aspose.Imaging. أضف مساحات الأسماء التالية إلى ملف التعليمات البرمجية الخاص بك:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Emf;
using Aspose.Imaging.FileFormats.Png;
using Aspose.Imaging.Graphics;
using System;
```

الآن بعد أن أصبح لدينا المتطلبات الأساسية ومساحات الأسماء، فلنقسم المثال إلى خطوات متعددة.

## الخطوة 1: قم بتحميل الصورة المراد رسمها

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
{
    // الكود الخاص بك للخطوة 1 موجود هنا
}
```

 في هذه الخطوة، نقوم بتحميل الصورة النقطية التي تريد رسمها على ملف EMF. يستبدل`"Your Document Directory"` مع المسار إلى صورتك.

## الخطوة 2: قم بتحميل سطح رسم EMF

```csharp
using (EmfImage canvasImage = (EmfImage)Image.Load(dataDir + "input.emf"))
{
    // الكود الخاص بك للخطوة 2 موجود هنا
}
```

 هنا، نقوم بتحميل ملف EMF الذي سيكون بمثابة سطح الرسم لصورتنا. تأكد من استبدال`"input.emf"` مع المسار إلى ملف EMF الخاص بك.

## الخطوة 3: إنشاء رسومات مسجل EMF

```csharp
EmfRecorderGraphics2D graphics = EmfRecorderGraphics2D.FromEmfImage(canvasImage);
```

 في هذه الخطوة، نقوم بإنشاء مثيل`EmfRecorderGraphics2D` من صورة EMF. هذا يسمح لنا بتسجيل عمليات الرسم.

## الخطوة 4: ارسم الصورة النقطية

```csharp
graphics.DrawImage(
    imageToDraw,
    new Rectangle(67, 67, canvasImage.Width, canvasImage.Height),
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    GraphicsUnit.Pixel);
```

 في هذه الخطوة نستخدم`DrawImage`طريقة لرسم الصورة النقطية المحملة على ملف EMF. يمكنك تحديد مستطيلات المصدر والوجهة للتحكم في موضع وحجم الصورة المرسومة.

## الخطوة 5: احفظ الصورة الناتجة

```csharp
using (EmfImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "input.DrawImage.emf");
}
```

 أخيرًا، نقوم بحفظ صورة EMF الناتجة مع الصورة النقطية المرسومة في ملف. سيتم حفظ الملف بالاسم "input.DrawImage.emf" في الدليل المحدد بواسطة`dataDir`.

تهانينا! لقد نجحت في رسم صورة نقطية على ملف EMF باستخدام Aspose.Imaging لـ .NET. لا تتردد في استكشاف وتجربة مستطيلات المصدر والوجهة المختلفة لتحقيق التأثيرات المطلوبة.

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية استخدام Aspose.Imaging لـ .NET لرسم صورة نقطية على ملف EMF. باتباع الدليل الموضح خطوة بخطوة، يمكنك بسهولة دمج هذه الوظيفة في تطبيقات .NET الخاصة بك.

استمتع بإنشاء صور مذهلة باستخدام Aspose.Imaging!

## الأسئلة الشائعة

### 1. هل يمكنني رسم صور متعددة على نفس ملف EMF؟

نعم، يمكنك رسم صور متعددة على نفس ملف EMF عن طريق تكرار عملية الرسم باستخدام مستطيلات مصدر ووجهة مختلفة.

### 2. هل Aspose.Imaging متوافق مع .NET Core؟

نعم، Aspose.Imaging for .NET متوافق مع كل من .NET Framework و.NET Core.

### 3. كيف يمكنني تطبيق التحويلات على الصورة المرسومة مثل التدوير أو القياس؟

 يمكنك تطبيق التحويلات عن طريق معالجة مستطيلات المصدر والوجهة في ملف`DrawImage` طريقة.

### 4. هل يمكنني رسم رسومات متجهة على ملف EMF أيضًا؟

نعم، يمكنك رسم رسومات وأشكال متجهة بالإضافة إلى الصور النقطية باستخدام Aspose.Imaging for .NET.

### 5. أين يمكنني الحصول على الدعم لـ Aspose.Imaging؟

 للحصول على الدعم والمساعدة، يمكنك زيارة منتدى Aspose.Imaging[هنا](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
