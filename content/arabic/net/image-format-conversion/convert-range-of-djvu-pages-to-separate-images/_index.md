---
title: تحويل نطاق صفحات DJVU إلى صور منفصلة في Aspose.Imaging لـ .NET
linktitle: تحويل نطاق صفحات DJVU إلى صور منفصلة في Aspose.Imaging لـ .NET
second_title: Aspose.Imaging .NET واجهة برمجة تطبيقات معالجة الصور
description: اكتشف كيفية تحويل صفحات DJVU إلى صور منفصلة باستخدام Aspose.Imaging for .NET. يتم توفير دليل خطوة بخطوة وأمثلة التعليمات البرمجية والأسئلة الشائعة.
type: docs
weight: 19
url: /ar/net/image-format-conversion/convert-range-of-djvu-pages-to-separate-images/
---
إذا كنت تبحث عن مكتبة .NET قوية للتعامل مع مهام تحويل الصور ومعالجتها، فإن Aspose.Imaging for .NET هو الخيار الأمثل. في هذا البرنامج التعليمي، سنرشدك خلال عملية تحويل مجموعة من صفحات DJVU إلى صور منفصلة باستخدام Aspose.Imaging. ستجد تعليمات خطوة بخطوة ومقتطفات التعليمات البرمجية لمساعدتك في تحقيق هذه المهمة.

## المتطلبات الأساسية

قبل أن نتعمق في عملية التحويل، تأكد من توفر المتطلبات الأساسية التالية:

1. Aspose.Imaging لمكتبة .NET

 ستحتاج إلى تثبيت Aspose.Imaging for .NET. إذا لم تكن قد قمت بذلك بالفعل، يمكنك تنزيله من[Aspose.Imaging لصفحة .NET](https://releases.aspose.com/imaging/net/).

2. بيئة التطوير

للمتابعة، يجب أن يكون لديك بيئة تطوير تم إعدادها باستخدام Visual Studio أو أي برنامج .NET IDE آخر.

## استيراد مساحات الأسماء الضرورية

أولاً، تحتاج إلى تضمين مساحات الأسماء المطلوبة في التعليمات البرمجية الخاصة بك للعمل مع Aspose.Imaging. وإليك كيف يمكنك القيام بذلك:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Djvu;
using Aspose.Imaging.FileFormats.Djvu.Options;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.RasterImage;
```

## تحويل صفحات DJVU

الآن، دعنا نقسم عملية تحويل مجموعة من صفحات DJVU إلى صور منفصلة باستخدام Aspose.Imaging for .NET إلى سلسلة من الخطوات سهلة المتابعة.

### الخطوة 1: قم بتحميل صورة DJVU

 للبدء، يجب عليك تحميل صورة DJVU التي تريد تحويلها. يستبدل`"Your Document Directory"` بالمسار الفعلي لملف DJVU الخاص بك.

```csharp
string dataDir = "Your Document Directory";

// قم بتحميل صورة ديجيفو
using (DjvuImage image = (DjvuImage)Image.Load(dataDir + "Sample.djvu"))
{
    // سيتم وضع الرمز الخاص بك لمزيد من المعالجة هنا.
}
```

### الخطوة 2: ضبط خيارات التصدير

 الآن، قم بإنشاء مثيل لـ`BmpOptions` وتكوين الخيارات المطلوبة للصور الناتجة. في هذا المثال، قمنا بتعيين`BitsPerPixel` إلى 32.

```csharp
BmpOptions exportOptions = new BmpOptions();
exportOptions.BitsPerPixel = 32;
```

### الخطوة 3: تحديد نطاق الصفحات

 لتحديد نطاق الصفحات التي تريد تصديرها، قم بإنشاء مثيل لها`IntRange` وتهيئته مع نطاق الصفحات. في هذه الحالة، نقوم بتصدير الصفحات من 0 إلى 2.

```csharp
IntRange range = new IntRange(0, 2);
```

### الخطوة 4: حلقة من خلال الصفحات

الآن، قم بالمرور عبر الصفحات الموجودة ضمن النطاق المحدد واحفظ كل صفحة كصورة BMP منفصلة. لا تدعم ملفات DJVU الطبقات، لذلك نقوم بحفظ كل صفحة على حدة.

```csharp
int counter = 0;
foreach (var i in range.Range)
{
    exportOptions.MultiPageOptions = new DjvuMultiPageOptions(range.GetArrayOneItemFromIndex(counter));
    image.Save(dataDir + string.Format("{0}_out.bmp", counter++), exportOptions);
}
```

وهذا كل شيء! لقد نجحت في تحويل مجموعة من صفحات DJVU إلى صور منفصلة باستخدام Aspose.Imaging for .NET.

## خاتمة

يعمل Aspose.Imaging for .NET على تبسيط مهام تحويل الصور، مما يجعله خيارًا ممتازًا للمطورين. في هذا البرنامج التعليمي، أرشدناك خلال عملية تحويل صفحات DJVU إلى صور منفصلة خطوة بخطوة. مع وجود الكود الصحيح والمكتبة تحت تصرفك، يصبح تحويل الصور أمرًا سهلاً.

## الأسئلة الشائعة

### س1: هل يعتبر Aspose.Imaging for .NET مكتبة مجانية؟

 ج1: لا، إنها مكتبة تجارية، ولكن يمكنك تنزيل ملف[تجربة مجانية](https://releases.aspose.com/) لاختبار قدراته.

### س2: هل يمكنني شراء ترخيص مؤقت لـ Aspose.Imaging لـ .NET؟

 ج2: نعم، يمكنك الحصول على ترخيص مؤقت من[صفحة الشراء](https://purchase.aspose.com/temporary-license/).

### س3: أين يمكنني العثور على وثائق Aspose.Imaging لـ .NET؟

 ج3: يمكنك استكشاف الوثائق الشاملة[هنا](https://reference.aspose.com/imaging/net/).

### س 4: ما هي تنسيقات الصور التي يدعمها Aspose.Imaging لـ .NET؟

ج4: يدعم Aspose.Imaging for .NET نطاقًا واسعًا من تنسيقات الصور، بما في ذلك BMP وJPEG وPNG وTIFF والمزيد.

### س5: هل يمكنني الحصول على الدعم والمساعدة إذا واجهت مشاكل؟

 ج5: نعم، يمكنك طلب المساعدة والتواصل مع المجتمع على[Aspose.منتدى التصوير](https://forum.aspose.com/).