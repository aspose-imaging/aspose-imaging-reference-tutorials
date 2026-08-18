---
date: 2026-02-12
description: تعلم كيفية إنشاء صورة فارغة باستخدام Aspose وكيفية رسم مستطيل في .NET
  باستخدام Aspose.Imaging – دليل سريع لتعديل الصور في تطبيقات .NET الخاصة بك.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: إنشاء صورة فارغة Aspose – رسم مستطيلات في .NET
url: /ar/net/basic-drawing/draw-rectangle/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء صورة فارغة Aspose – رسم مستطيلات في .NET

إنشاء ومعالجة الصور في تطبيقات .NET قد يبدو صعبًا، ولكن باستخدام Aspose.Imaging يمكنك **إنشاء صورة فارغة Aspose** ببضع أسطر من الشيفرة ثم رسم الأشكال عليها. في هذا الدرس سنستعرض العملية بالكامل — من إعداد لوحة رسم فارغة إلى رسم المستطيلات—حتى تتمكن من إضافة الرسومات إلى مشاريع .NET الخاصة بك على الفور.

## إجابات سريعة
- **ماذا يعني “create blank image Aspose”?** يعني إنشاء صورة bitmap فارغة باستخدام Aspose.Imaging API.  
- **كيف ترسم مستطيل .net باستخدام Aspose؟** استخدم طريقة `Graphics.DrawRectangle` بعد تهيئة كائن `Graphics`.  
- **ما حزمة NuGet المطلوبة؟** `Aspose.Imaging` (أحدث إصدار).  
- **هل يمكنني حفظ الصورة بصيغة PNG أو JPEG أو BMP؟** نعم – فقط غير خيارات الصورة (مثل `BmpOptions`، `JpegOptions`).  
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تكفي للتقييم؛ يتطلب الترخيص التجاري للإنتاج.

## ما هو “create blank image Aspose”؟
إنشاء صورة فارغة يعني تخصيص مخزن بكسلات بعرض وارتفاع وتنسيق بكسل محددين. تتولى Aspose.Imaging التفاصيل منخفضة المستوى، وتوفر لك لوحة رسم جاهزة للرسم دون الحاجة للتعامل مع GDI+ أو System.Drawing.

## لماذا تستخدم Aspose.Imaging لرسم المستطيلات في .NET؟
- **متعدد المنصات** – يعمل على Windows وLinux وmacOS.  
- **بدون تبعيات أصلية** – كود مُدار بالكامل، مثالي لبيئات الخوادم.  
- **واجهة برمجة رسومات غنية** – تدعم الأقلام، الفرش، مكافحة التعرجات، والعديد من أنواع الأشكال.  
- **أداء عالي** – مُحسّن للصور الكبيرة والمعالجة الدفعية.

## المتطلبات المسبقة

1. **Aspose.Imaging for .NET** – قم بتنزيله من [صفحة التحميل](https://releases.aspose.com/imaging/net/).  
2. **بيئة التطوير** – Visual Studio أو VS Code أو أي IDE متوافق مع .NET.  
3. **بيئة تشغيل .NET** – .NET 6+ أو .NET Framework 4.7.2+.  

الآن بعد أن تم إعداد كل شيء، دعنا نغوص في الشيفرة.

## كيف تنشئ صورة فارغة Aspose في .NET؟

### الخطوة 1: استيراد المساحات الاسمية المطلوبة

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

هذه المساحات الاسمية تمنحك الوصول إلى الفئات الأساسية للصور، وأنواع الفرش، وخيارات حفظ الصورة.

### الخطوة 2: إنشاء صورة فارغة (اللوحة)

```csharp
string dataDir = "Your Document Directory";  // Set the path to your document directory
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Your drawing code will go here
        image.Save();
    }
}
```

في هذا الجزء نقوم بـ:
* تحديد موقع الإخراج (`dataDir`).  
* إعداد `BmpOptions` لاستخدام تنسيق بكسل 32‑بت.  
* إنشاء **صورة فارغة** بحجم 100 × 100 بكسل.  

### الخطوة 3: كيف ترسم مستطيل .net باستخدام Aspose.Imaging

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` يملأ اللوحة بلون خلفية (أصفر في هذا المثال).  
* `DrawRectangle` يرسم مستطيلين—أحدهما بقلم أحمر بسيط، والآخر بفرشاة صلبة زرقاء—للتباين البصري.

### الخطوة 4: حفظ الصورة

```csharp
image.Save();
```

استدعاء `Save` يكتب ملف الـ bitmap إلى نظام الملفات باستخدام الخيارات التي تم تعريفها مسبقًا.

## المشكلات الشائعة والنصائح

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **الصورة الفارغة تظهر باللون الأسود** | الخلفية لم تُمسح | استدعِ `graphic.Clear(Color.YourColor)` قبل الرسم. |
| **استثناء ملف غير موجود** | `dataDir` يشير إلى مجلد غير موجود | تأكد من وجود المجلد أو استخدم `Path.Combine` مع `Environment.CurrentDirectory`. |
| **ألوان غير صحيحة** | استخدام `System.Drawing.Color` بدلاً من `Aspose.Imaging.Color` | دائمًا استورد `Aspose.Imaging.Color`. |
| **بطء الأداء على الصور الكبيرة** | استخدام `BmpOptions` الافتراضية مع عدد بتات عالي لكل بكسل | تحول إلى `JpegOptions` أو `PngOptions` للضغط. |

## الأسئلة المتكررة (موسعة)

**س: هل يمكنني رسم أشكال أخرى غير المستطيلات؟**  
**ج:** بالتأكيد. توفر Aspose.Imaging طرقًا مثل `DrawEllipse` و `DrawLine` و `DrawPolygon`.

**س: هل المكتبة مجانية للاستخدام التجاري؟**  
**ج:** لا، Aspose.Imaging منتج تجاري، لكن يمكنك تقييمه من خلال نسخة تجريبية مجانية متوفرة [هنا](https://releases.aspose.com/).

**س: هل يعمل هذا على كل من Windows وتطبيقات الويب؟**  
**ج:** نعم، نفس الشيفرة تعمل في ASP.NET وBlazor وتطبيقات الكونسول.

**س: كيف أغير صيغة الإخراج إلى PNG؟**  
**ج:** استبدل `BmpOptions` بـ `PngOptions` وعدّل امتداد الملف وفقًا لذلك.

**س: أين يمكنني العثور على وثائق أكثر تفصيلاً؟**  
**ج:** احصل على مرجع API الكامل [هنا](https://reference.aspose.com/imaging/net/) وانضم إلى المجتمع في [منتدى Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-02-12  
**تم الاختبار مع:** Aspose.Imaging 24.12 for .NET  
**المؤلف:** Aspose