---
title: قم بتحويل APS إلى PSD باستخدام Aspose.Imaging لـ .NET
linktitle: تحويل APS إلى PSD في Aspose.Imaging لـ .NET
second_title: Aspose.Imaging .NET واجهة برمجة تطبيقات معالجة الصور
description: قم بتحويل APS إلى PSD باستخدام Aspose.Imaging لـ .NET. الحفاظ على خصائص المتجهات أثناء التحويل.
type: docs
weight: 11
url: /ar/net/advanced-features/convert-aps-to-psd/
---
هل تتطلع إلى تحويل ملفات APS إلى تنسيق PSD بسهولة مع الحفاظ على خصائص المتجهات؟ Aspose.Imaging for .NET موجود هنا لتبسيط مهمتك. وفي هذا الدليل التفصيلي، سنوضح لك كيفية تحقيق هذا التحويل. 

## المتطلبات الأساسية

قبل أن نتعمق في هذه العملية، تأكد من توفر المتطلبات الأساسية التالية:

1.  Aspose.Imaging لـ .NET Library: أنت بحاجة إلى تنزيل وتثبيت مكتبة Aspose.Imaging لـ .NET. يمكنك الحصول عليه من[صفحة التحميل](https://releases.aspose.com/imaging/net/).

2. دليل المستندات الخاص بك: تأكد من أن المسار إلى دليل المستندات الخاص بك جاهز. هذا هو المكان الذي يوجد فيه ملف APS.

3. المعرفة الأساسية بـ C#: يعد الإلمام بلغة البرمجة C# أمرًا ضروريًا لتنفيذ عملية التحويل.

## استيراد مساحات الأسماء

لنبدأ باستيراد مساحات الأسماء الضرورية للعمل مع Aspose.Imaging لـ .NET. تأكد من إضافة المرجع إلى مكتبة Aspose.Imaging في مشروعك.

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Vectorization;
```

## الخطوة 1: قم بتحميل ملف APS

ابدأ بتحميل ملف APS الذي تريد تحويله إلى PSD. ستحدد أيضًا المسار إلى دليل المستند حيث يوجد ملف APS.

```csharp
string dataDir = "Your Document Directory";
string inputFileName = dataDir + "SimpleShapes.cdr";

using (Image image = Image.Load(inputFileName))
{
    // الكود الخاص بك يذهب هنا
}
```

## الخطوة 2: تكوين خيارات التحويل

في هذه الخطوة، تحتاج إلى إعداد خيارات التحويل لتصدير ملف APS إلى تنسيق PSD. يوفر Aspose.Imaging خيارات متنوعة لتحويل الصور المتجهة.

```csharp
PsdOptions imageOptions = new PsdOptions()
{
    VectorRasterizationOptions = new VectorRasterizationOptions(),
    VectorizationOptions = new PsdVectorizationOptions()
    {
        VectorDataCompositionMode = VectorDataCompositionMode.SeparateLayers
    }
};

imageOptions.VectorRasterizationOptions.PageWidth = image.Width;
imageOptions.VectorRasterizationOptions.PageHeight = image.Height;
```

## الخطوة 3: احفظ ملف PSD

حان الوقت الآن لحفظ ملف PSD المحول إلى الموقع الذي تريده.

```csharp
image.Save(dataDir + "result.psd", imageOptions);
```

## الخطوة 4: التنظيف

بعد اكتمال التحويل، قد ترغب في حذف ملف PSD المؤقت الذي تم إنشاؤه أثناء العملية.

```csharp
File.Delete(dataDir + "result.psd");
```

## خاتمة

يعد تحويل تنسيق APS إلى تنسيق PSD باستخدام Aspose.Imaging لـ .NET أمرًا مباشرًا وفعالاً. تسمح لك هذه المكتبة القوية بالحفاظ على خصائص المتجهات أثناء التحويل، مما يجعلها أداة قيمة لمصممي الجرافيك والمطورين على حدٍ سواء.

## الأسئلة الشائعة

### س1: هل يعتبر Aspose.Imaging for .NET مكتبة مجانية؟

 A1: Aspose.Imaging for .NET هي مكتبة تجارية. يمكنك استكشاف خيارات الترخيص على[صفحة الشراء](https://purchase.aspose.com/buy).

### س2: هل يمكنني تجربة Aspose.Imaging لـ .NET قبل شرائه؟

 ج2: نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Imaging لـ .NET من[صفحة تجريبية](https://releases.aspose.com/imaging/net/).

### س3: ما هي تنسيقات الصور المتجهة المدعومة للتحويل إلى PSD؟

ج3: يدعم Aspose.Imaging for .NET تحويل تنسيقات الصور المتجهة مثل CDR وEMF وEPS وODG وSVG وWMF إلى تنسيق PSD.

### س 4: هل هناك أي قيود على مدى تعقيد الأشكال أثناء التحويل؟

ج4: حاليًا، يدعم Aspose.Imaging تصدير الأشكال غير المعقدة جدًا بدون فرش الملمس أو الأشكال المفتوحة ذات الحد. ومع ذلك، قد يتم تحسين هذا في الإصدارات القادمة.

### س5: أين يمكنني الحصول على الدعم أو طرح الأسئلة المتعلقة بـ Aspose.Imaging for .NET؟

 ج5: إذا كانت لديك أية أسئلة أو كنت بحاجة إلى الدعم، فيمكنك زيارة[Aspose.منتديات التصوير](https://forum.aspose.com/) للمساعدة.
