---
date: 2026-02-09
description: تعلم كيفية رسم قوس باستخدام Aspose.Imaging لـ .NET، بما في ذلك كيفية
  حفظ ملف BMP، ضبط حجم الصورة، وتعيين خلفية الرسومات. دليل خطوة بخطوة لإنشاء صور BMP.
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: كيفية رسم قوس باستخدام Aspose.Imaging لـ .NET
url: /ar/net/basic-drawing/draw-arc/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم قوس باستخدام Aspose.Imaging لـ .NET

في عالم معالجة الصور، **كيفية رسم قوس** هي مهمة شائعة يمكنها إضافة لمسة بصرية لأي رسم. باستخدام Aspose.Imaging لـ .NET يمكنك إنشاء صور BMP، ضبط حجم الصورة، ورسم قوس بالقلم في بضع أسطر فقط من C#. في نهاية هذا الدرس ستعرف بالضبط كيفية رسم قوس، ضبط خلفية الرسومات، وحفظ ملف BMP الناتج بسهولة.

## إجابات سريعة
- **ماذا ينتج الكود؟** صورة BMP بحجم 100 × 100 بكسل بخلفية صفراء وقوس أسود.  
- **ما المكتبة المستخدمة؟** Aspose.Imaging لـ .NET.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم ترخيص تجاري للإنتاج.  
- **هل يمكنني تغيير حجم الصورة؟** نعم – عدل قيم العرض والارتفاع في استدعاء `Image.Create`.  
- **هل تنسيق الإخراج ثابت؟** المثال يحفظ ملف BMP، لكن يمكن استخدام أي تنسيق تدعمه Aspose.Imaging.

## ما هو “كيفية رسم قوس” في Aspose.Imaging؟
يعني رسم قوس تمثيل مقطع خط منحني يُحدَّد بواسطة مستطيل محيط، زاوية البداية، وزاوية المسح. توفر Aspose.Imaging الطريقة `Graphics.DrawArc` التي تسمح لك **برسم قوس بالقلم** والتحكم في كل جانب بصري.

## لماذا تستخدم Aspose.Imaging لهذا الغرض؟
- **تحكم كامل** في أبعاد الصورة، عمق اللون، وتنسيق الملف.  
- **بدون تبعيات خارجية** – كل شيء يعمل على .NET النقي.  
- **أداء عالي** لتوليد أعداد كبيرة من الرسومات على جانب الخادم.  

## المتطلبات المسبقة

قبل أن نغوص في الكود، تأكد من أن لديك ما يلي:

1. **Aspose.Imaging لـ .NET** – قم بتنزيله من الموقع الرسمي [هنا](https://releases.aspose.com/imaging/net/).  
2. **بيئة تطوير .NET** (Visual Studio، VS Code، أو أي مترجم C#).  

الآن بعد أن أصبحت المتطلبات جاهزة، لنبدأ الرسم!

## استيراد المساحات الاسمية الضرورية

للعمل مع Aspose.Imaging تحتاج إلى جلب المساحات الاسمية ذات الصلة إلى النطاق:

### الخطوة 1: استيراد المساحات الاسمية

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

تُعطيك هذه عبارات `using` إمكانية الوصول إلى فئات إنشاء الصور، معالجة الرسومات، وفئات إدخال/إخراج الملفات.

## كيفية رسم قوس باستخدام Aspose.Imaging لـ .NET

سنقسم العملية إلى ثلاث خطوات واضحة: إنشاء الصورة، إعداد سطح الرسومات، وأخيرًا رسم القوس.

### الخطوة 1: إعداد الصورة (تحديد حجم الصورة وإنشاء صورة BMP)

```csharp
// Specify the directory where you want to save the image
string dataDir = "Your Document Directory";

// Create an instance of FileStream to save the image
using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
{
    // Create an instance of BmpOptions and set its properties
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;

    // Set the source for BmpOptions and create an instance of Image
    saveOptions.Source = new StreamSource(stream);
    using (Image image = Image.Create(saveOptions, 100, 100))
    {
```

هنا **نحدد حجم الصورة** إلى 100 × 100 بكسل ونُكوّن خيارات BMP. يضمن `FileStream` أننا **نحفظ ملف BMP** في الموقع المطلوب.

### الخطوة 2: تهيئة Graphics وتحديد خلفية الرسومات

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

كائن `Graphics` يسمح لنا بالرسم على الصورة. باستدعاء `Clear(Color.Yellow)` **نحدد خلفية الرسومات** إلى أصفر ساطع، مما يجعل القوس يبرز.

### الخطوة 3: تعريف معلمات القوس ورسم القوس بالقلم

```csharp
        // Define the parameters for the arc
        int width = 100;
        int height = 200;
        int startAngle = 45;
        int sweepAngle = 270;

        // Draw the arc
        graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);

        // Save the changes
        image.Save();
    }
    stream.Close();
}
```

- `width` و `height` يحددان المستطيل المحيط، وبالتالي **تحديد حجم الصورة** للقوس.  
- كائن `Pen` هو ما يسمح لنا **برسم القوس بالقلم** باللون الأسود.  
- بعد الرسم، `image.Save()` يكتب **ملف BMP** إلى القرص.

## المشكلات الشائعة والنصائح

- **القوس غير مرئي؟** تأكد من أن لون القلم يتباين مع الخلفية (مثلاً، أسود على أصفر).  
- **أبعاد غير صحيحة؟** تذكر أن المستطيل المحيط بالقوس قد يكون أكبر من الصورة؛ عدل `width`/`height` أو حجم الصورة وفقًا لذلك.  
- **نصيحة أداء:** أعد استخدام كائن `Graphics` واحد إذا كنت بحاجة لرسم أشكال متعددة على نفس الصورة.

## الأسئلة الشائعة

### س1: أين يمكنني العثور على وثائق Aspose.Imaging لـ .NET؟

ج1: يمكنك الرجوع إلى الوثائق [هنا](https://reference.aspose.com/imaging/net/) للحصول على معلومات شاملة حول Aspose.Imaging لـ .NET.

### س2: كيف يمكنني تنزيل Aspose.Imaging لـ .NET؟

ج2: يمكنك تنزيل Aspose.Imaging لـ .NET من الموقع [هنا](https://releases.aspose.com/imaging/net/).

### س3: هل تتوفر نسخة تجريبية مجانية لـ Aspose.Imaging لـ .NET؟

ج3: نعم، يمكنك الحصول على نسخة تجريبية مجانية [هنا](https://releases.aspose.com/) لتجربة Aspose.Imaging لـ .NET.

### س4: هل أحتاج إلى ترخيص مؤقت لـ Aspose.Imaging لـ .NET؟

ج4: إذا كنت بحاجة إلى ترخيص مؤقت، يمكنك الحصول عليه [هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني الحصول على الدعم أو طرح الأسئلة حول Aspose.Imaging لـ .NET؟

ج5: يمكنك زيارة منتدى Aspose.Imaging للحصول على الدعم والنقاشات [هنا](https://forum.aspose.com/).

---

**آخر تحديث:** 2026-02-09  
**تم الاختبار مع:** Aspose.Imaging 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}