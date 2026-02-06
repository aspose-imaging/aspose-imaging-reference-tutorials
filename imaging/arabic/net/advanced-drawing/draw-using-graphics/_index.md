---
date: 2026-02-06
description: تعلم كيفية رسم الرسومات باستخدام Aspose.Imaging لـ .NET، بما في ذلك كيفية
  ضبط خيارات الصورة، مسح سطح الصورة، تطبيق التدرج الخطي، ورسم الأشكال بلغة C#.
linktitle: Draw Using Graphics in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: كيفية رسم الرسومات باستخدام Aspose.Imaging لـ .NET – إتقان رسم الصور
url: /ar/net/advanced-drawing/draw-using-graphics/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم الرسومات باستخدام Aspose.Imaging لـ .NET

في عالم معالجة الصور وتعديلها، **كيفية رسم الرسومات** باستخدام Aspose.Imaging لـ .NET هو سؤال شائع بين مطوري .NET. يوضح هذا الدرس كيفية إنشاء صورة bitmap، ضبط خيارات الصورة، مسح سطح الصورة، تطبيق تدرج لوني خطي، ورسم الأشكال في C#. في النهاية ستحصل على مثال عملي يمكنك تكييفه مع مشاريعك الخاصة.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.Imaging لـ .NET (قم بتنزيلها من **رابط التحميل** الرسمي).  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6+.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **هل يمكنني تطبيق تدرج لوني خطي؟** نعم – `LinearGradientBrush` يتيح لك ملء الأشكال بتدرج سلس بين الألوان.  
- **كيف أقوم بمسح سطح الصورة؟** استخدم `graphics.Clear(Color.White)` (أو أي لون خلفية آخر).

## ما معنى “كيفية رسم الرسومات” في Aspose.Imaging؟
رسم الرسومات يعني استخدام فئة `Graphics` لتصوير الأشكال المتجهة، النصوص، والمناطق المملوءة على لوحة صورة. يشبه ذلك GDI+ لكنه يعمل عبر المنصات ويدعم مجموعة واسعة من صيغ الصور.

## لماذا نستخدم Aspose.Imaging لرسم الرسومات؟
- **API غني للرسم** – أقلام، فرش، تدرجات، وتنعيم الحواف مدمجة.  
- **بدون تبعيات خارجية** – كل الوظائف موجودة داخل المكتبة.  
- **يدعم أكثر من 100 صيغة صورة** – من BMP و PNG إلى RAW و PSD.  
- **جاهز للمؤسسات** – أداء عالي، آمن للمتعدد الخيوط، ومُوثّق بالكامل.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

1. **Aspose.Imaging لـ .NET** – حمّله من **[رابط التحميل](https://releases.aspose.com/imaging/net/)**.  
2. **بيئة تطوير .NET** – Visual Studio أو VS Code أو Rider.  
3. **معرفة أساسية بـ C#** – يجب أن تكون مرتاحًا مع الفئات، الطرق، وتعليمة `using`.

## استيراد المساحات الاسمية

أولاً، استدعِ المساحة الاسمية المطلوبة:

```csharp
using Aspose.Imaging;
```

هذه السطر يمنحك الوصول إلى جميع فئات Aspose.Imaging، بما في ذلك `Image`، `Graphics`، `BmpOptions`، وأنواع الفرش والأقلام المختلفة.

## كيفية رسم الرسومات باستخدام Aspose.Imaging

فيما يلي شرح خطوة بخطوة. كل خطوة تتضمن شرحًا مختصرًا يليه كتلة الكود الأصلية (بدون تعديل).

### الخطوة 1: ضبط خيارات الصورة وإنشاء لوحة رسم  

نبدأ بتكوين خيارات الـ bitmap – هذا هو جزء **ضبط خيارات الصورة** في العملية. الخاصية `BitsPerPixel` تحدد عمق اللون، بينما `FileCreateSource` يشير إلى مجلد الإخراج.

```csharp
public static void Run()
{
    Console.WriteLine("Running example DrawingUsingGraphics");
    string dataDir = "Your Document Directory";
    BmpOptions imageOptions = new BmpOptions();
    imageOptions.BitsPerPixel = 24;
    imageOptions.Source = new FileCreateSource(dataDir, false);
    
    // Create an image with the specified options
    using (var image = Image.Create(imageOptions, 500, 500))
    {
        var graphics = new Graphics(image);
        // Continue with drawing operations
    }
    Console.WriteLine("Finished example DrawingUsingGraphics");
}
```

### الخطوة 2: مسح سطح الصورة  

قبل رسم أي شيء، من الممارسات الجيدة **مسح سطح الصورة** لتبدأ بخلفية نظيفة.

```csharp
graphics.Clear(Color.White);
```

يمكنك استبدال `Color.White` بأي قيمة `Color` أخرى لتعيين خلفية مختلفة.

### الخطوة 3: تعريف قلم ورسم الأشكال  

الآن نقوم **برسم الأشكال** بأسلوب C#. القلم `Pen` يحدد لون الحد وعرضه، بينما كائن `Graphics` يرسم الهندسة.

```csharp
var pen = new Pen(Color.Blue);
graphics.DrawEllipse(pen, new Rectangle(10, 10, 150, 100));

using (var linearGradientBrush = new LinearGradientBrush(image.Bounds, Color.Red, Color.White, 45f))
{
    graphics.FillPolygon(
        linearGradientBrush,
        new[] { new Point(200, 200), new Point(400, 200), new Point(250, 350) });
}
```

في المقتطف أعلاه نطبق أيضًا **تدرجًا خطيًا** على مضلع، مما يخلق انتقالًا سلسًا من الأحمر إلى الأبيض بزاوية 45 درجة.

### الخطوة 4: حفظ الصورة  

أخيرًا، احفظ الـ bitmap على القرص. طريقة `Image.Save()` تكتب الملف باستخدام الصيغة المحددة في الخيارات (BMP في هذه الحالة).

```csharp
image.Save();
```

## المشكلات الشائعة والحلول

| المشكلة | سبب حدوثها | الحل |
|---------|------------|------|
| **عدم حفظ الصورة** | `dataDir` يشير إلى مجلد غير موجود. | تأكد من وجود المجلد أو استخدم `Path.Combine` مع `Environment.CurrentDirectory`. |
| **التدرج يظهر صلبًا** | زاوية `LinearGradientBrush` خارج النطاق. | استخدم زاوية بين 0‑360 درجة؛ 45f تعمل جيدًا للتدرجات القطرية. |
| **عرض القلم رفيع جدًا** | عرض القلم الافتراضي 1 بكسل. | أنشئ القلم بعرض محدد: `new Pen(Color.Blue, 3)`. |
| **استثناء نفاد الذاكرة** | أبعاد الصورة كبيرة جدًا. | قلل العرض/الارتفاع أو عالج الصورة على شكل قطع (tiles). |

## الأسئلة المتكررة

### س: ما هو Aspose.Imaging لـ .NET؟  
ج: Aspose.Imaging لـ .NET هي مكتبة قوية لمعالجة الصور تتيح للمطورين إنشاء، تعديل، وتحويل الصور بصيغ متعددة باستخدام .NET.

### س: أين يمكنني تنزيل Aspose.Imaging لـ .NET؟  
ج: يمكنك تنزيل Aspose.Imaging لـ .NET من **[رابط التحميل](https://releases.aspose.com/imaging/net/)**.

### س: هل يمكن تجربة Aspose.Imaging لـ .NET قبل الشراء؟  
ج: نعم، يمكنك تجربة نسخة تجريبية مجانية من Aspose.Imaging لـ .NET عبر زيارة **[هذا الرابط](https://releases.aspose.com/)**.

### س: كيف أحصل على ترخيص مؤقت لـ Aspose.Imaging لـ .NET؟  
ج: للحصول على ترخيص مؤقت، زر **[هذا الرابط](https://purchase.aspose.com/temporary-license/)**.

### س: ما هي الميزات الرئيسية لـ Aspose.Imaging لـ .NET؟  
ج: تقدم Aspose.Imaging لـ .NET ميزات مثل إنشاء الصور، تعديلها، تحويلها، دعم مجموعة واسعة من صيغ الصور، وقدرات رسم متقدمة.

## الخاتمة

أصبح لديك الآن مثال كامل وجاهز للإنتاج يوضح **كيفية رسم الرسومات** باستخدام Aspose.Imaging لـ .NET. من خلال ضبط خيارات الصورة، مسح السطح، تطبيق تدرج لوني خطي، ورسم الأشكال، يمكنك بناء أي شيء من المخططات البسيطة إلى أعمال فنية معقدة تُنشأ برمجيًا. إذا واجهت أي صعوبات، فإن مجتمع Aspose مكان رائع لطرح الأسئلة.

إذا صادفت أي مشاكل أو كان لديك أسئلة، لا تتردد بزيارة **[منتدى دعم Aspose.Imaging](https://forum.aspose.com/)** للحصول على المساعدة.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-02-06  
**تم الاختبار مع:** Aspose.Imaging لـ .NET (أحدث إصدار)  
**المؤلف:** Aspose  

---