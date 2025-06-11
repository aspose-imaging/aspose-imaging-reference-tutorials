---
"description": "اكتشف كيفية تحويل صفحات DJVU إلى صور منفصلة باستخدام Aspose.Imaging لـ .NET. دليل خطوة بخطوة، وأمثلة برمجية، وأسئلة شائعة."
"linktitle": "تحويل نطاق صفحات DJVU إلى صور منفصلة في Aspose.Imaging لـ .NET"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Aspose.Imaging .NET"
"title": "تحويل نطاق صفحات DJVU إلى صور منفصلة في Aspose.Imaging لـ .NET"
"url": "/ar/net/image-format-conversion/convert-range-of-djvu-pages-to-separate-images/"
"weight": 19
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# تحويل نطاق صفحات DJVU إلى صور منفصلة في Aspose.Imaging لـ .NET

إذا كنت تبحث عن مكتبة .NET فعّالة لتحويل الصور ومعالجتها، فإن Aspose.Imaging for .NET هو الخيار الأمثل. في هذا البرنامج التعليمي، سنرشدك خلال عملية تحويل مجموعة من صفحات DJVU إلى صور منفصلة باستخدام Aspose.Imaging. ستجد تعليمات خطوة بخطوة ومقاطع برمجية لمساعدتك في إنجاز هذه المهمة.

## المتطلبات الأساسية

قبل أن نتعمق في عملية التحويل، تأكد من توفر المتطلبات الأساسية التالية:

1. مكتبة Aspose.Imaging لـ .NET

ستحتاج إلى تثبيت Aspose.Imaging لـ .NET. إذا لم يكن مثبتًا لديك، يمكنك تنزيله من [صفحة Aspose.Imaging لـ .NET](https://releases.aspose.com/imaging/net/).

2. بيئة التطوير

للمتابعة، يجب أن يكون لديك بيئة تطوير تم إعدادها باستخدام Visual Studio أو أي .NET IDE آخر.

## استيراد مساحات الأسماء الضرورية

أولاً، عليك تضمين مساحات الأسماء المطلوبة في الكود الخاص بك للعمل مع Aspose.Imaging. إليك كيفية القيام بذلك:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Djvu;
using Aspose.Imaging.FileFormats.Djvu.Options;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.RasterImage;
```

## تحويل صفحات DJVU

الآن، دعنا نقوم بتقسيم عملية تحويل مجموعة من صفحات DJVU إلى صور منفصلة باستخدام Aspose.Imaging لـ .NET إلى سلسلة من الخطوات السهلة المتابعة.

### الخطوة 1: تحميل صورة DJVU

للبدء، يجب عليك تحميل صورة DJVU التي تريد تحويلها. استبدل `"Your Document Directory"` مع المسار الفعلي لملف DJVU الخاص بك.

```csharp
string dataDir = "Your Document Directory";

// تحميل صورة DjVu
using (DjvuImage image = (DjvuImage)Image.Load(dataDir + "Sample.djvu"))
{
    // سيتم وضع الكود الخاص بك للمعالجة الإضافية هنا.
}
```

### الخطوة 2: تعيين خيارات التصدير

الآن، قم بإنشاء مثيل لـ `BmpOptions` وقم بتكوين الخيارات المطلوبة للصور الناتجة. في هذا المثال، قمنا بضبط `BitsPerPixel` إلى 32.

```csharp
BmpOptions exportOptions = new BmpOptions();
exportOptions.BitsPerPixel = 32;
```

### الخطوة 3: تحديد نطاق الصفحات

لتحديد نطاق الصفحات التي تريد تصديرها، قم بإنشاء مثيل لـ `IntRange` وتهيئته بنطاق الصفحات. في هذه الحالة، نُصدّر الصفحات من ٠ إلى ٢.

```csharp
IntRange range = new IntRange(0, 2);
```

### الخطوة 4: التنقل عبر الصفحات

الآن، تجوّل بين الصفحات ضمن النطاق المحدد، واحفظ كل صفحة كصورة BMP منفصلة. ملفات DJVU لا تدعم الطبقات، لذا نحفظ كل صفحة على حدة.

```csharp
int counter = 0;
foreach (var i in range.Range)
{
    exportOptions.MultiPageOptions = new DjvuMultiPageOptions(range.GetArrayOneItemFromIndex(counter));
    image.Save(dataDir + string.Format("{0}_out.bmp", counter++), exportOptions);
}
```

وهذا كل شيء! لقد نجحت في تحويل مجموعة من صفحات DJVU إلى صور منفصلة باستخدام Aspose.Imaging لـ .NET.

## خاتمة

يُبسّط Aspose.Imaging لـ .NET مهام تحويل الصور، مما يجعله خيارًا ممتازًا للمطورين. في هذا البرنامج التعليمي، شرحنا لك عملية تحويل صفحات DJVU إلى صور منفصلة خطوة بخطوة. مع توفر الكود والمكتبة المناسبين، سيصبح تحويل الصور سهلًا للغاية.

## الأسئلة الشائعة

### س1: هل Aspose.Imaging لـ .NET مكتبة مجانية؟

ج1: لا، إنها مكتبة تجارية، ولكن يمكنك تنزيلها [نسخة تجريبية مجانية](https://releases.aspose.com/) لاختبار قدراتها.

### س2: هل يمكنني شراء ترخيص مؤقت لـ Aspose.Imaging لـ .NET؟

ج2: نعم، يمكنك الحصول على ترخيص مؤقت من [صفحة الشراء](https://purchase.aspose.com/temporary-license/).

### س3: أين يمكنني العثور على وثائق Aspose.Imaging لـ .NET؟

أ3: يمكنك استكشاف الوثائق الشاملة [هنا](https://reference.aspose.com/imaging/net/).

### س4: ما هي تنسيقات الصور التي يدعمها Aspose.Imaging لـ .NET؟

A4: يدعم Aspose.Imaging for .NET مجموعة واسعة من تنسيقات الصور، بما في ذلك BMP وJPEG وPNG وTIFF والمزيد.

### س5: هل يمكنني الحصول على الدعم والمساعدة إذا واجهت مشاكل؟

ج5: نعم، يمكنك طلب المساعدة والتواصل مع المجتمع على [منتدى Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}