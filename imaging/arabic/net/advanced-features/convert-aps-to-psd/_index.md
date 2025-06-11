---
"description": "حوّل APS إلى PSD باستخدام Aspose.Imaging لـ .NET. حافظ على خصائص المتجهات أثناء التحويل."
"linktitle": "تحويل APS إلى PSD في Aspose.Imaging لـ .NET"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Aspose.Imaging .NET"
"title": "تحويل APS إلى PSD باستخدام Aspose.Imaging لـ .NET"
"url": "/ar/net/advanced-features/convert-aps-to-psd/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# تحويل APS إلى PSD باستخدام Aspose.Imaging لـ .NET

هل تبحث عن تحويل ملفات APS إلى PSD بسهولة مع الحفاظ على خصائص المتجهات؟ Aspose.Imaging for .NET هنا لتبسيط مهمتك. في هذا الدليل المفصل، سنوضح لك كيفية تحقيق هذا التحويل. 

## المتطلبات الأساسية

قبل أن نتعمق في العملية، تأكد من أن لديك المتطلبات الأساسية التالية:

1. مكتبة Aspose.Imaging لـ .NET: عليك تنزيل وتثبيت مكتبة Aspose.Imaging لـ .NET. يمكنك الحصول عليها من [صفحة التحميل](https://releases.aspose.com/imaging/net/).

2. دليل مستنداتك: تأكد من إعداد مسار دليل مستنداتك. هذا هو مكان ملف APS.

3. المعرفة الأساسية بلغة البرمجة C#: تعتبر المعرفة بلغة البرمجة C# ضرورية لتنفيذ عملية التحويل.

## استيراد مساحات الأسماء

لنبدأ باستيراد مساحات الأسماء اللازمة للعمل مع Aspose.Imaging لـ .NET. تأكد من إضافة المرجع إلى مكتبة Aspose.Imaging في مشروعك.

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Vectorization;
```

## الخطوة 1: تحميل ملف APS

ابدأ بتحميل ملف APS الذي تريد تحويله إلى PSD. حدد أيضًا مسار مجلد المستندات الذي يحتوي على ملف APS.

```csharp
string dataDir = "Your Document Directory";
string inputFileName = dataDir + "SimpleShapes.cdr";

using (Image image = Image.Load(inputFileName))
{
    // الكود الخاص بك يذهب هنا
}
```

## الخطوة 2: تكوين خيارات التحويل

في هذه الخطوة، عليك ضبط خيارات التحويل لتصدير ملف APS إلى صيغة PSD. يوفر Aspose.Imaging خيارات متنوعة لتحويل الصور المتجهة.

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

## الخطوة 3: حفظ ملف PSD

الآن، حان الوقت لحفظ ملف PSD المُحوّل في الموقع المطلوب.

```csharp
image.Save(dataDir + "result.psd", imageOptions);
```

## الخطوة 4: التنظيف

بعد اكتمال عملية التحويل، قد ترغب في حذف ملف PSD المؤقت الذي تم إنشاؤه أثناء العملية.

```csharp
File.Delete(dataDir + "result.psd");
```

## خاتمة

تحويل APS إلى PSD باستخدام Aspose.Imaging لـ .NET سهل وفعال. تتيح لك هذه المكتبة القوية الحفاظ على خصائص المتجهات أثناء التحويل، مما يجعلها أداة قيّمة لمصممي الجرافيك والمطورين على حد سواء.

## الأسئلة الشائعة

### س1: هل Aspose.Imaging لـ .NET مكتبة مجانية؟

ج١: Aspose.Imaging لـ .NET هي مكتبة تجارية. يمكنك استكشاف خيارات الترخيص على [صفحة الشراء](https://purchase.aspose.com/buy).

### س2: هل يمكنني تجربة Aspose.Imaging لـ .NET قبل شرائه؟

ج2: نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.Imaging لـ .NET من [صفحة التجربة](https://releases.aspose.com/imaging/net/).

### س3: ما هي تنسيقات الصور المتجهة المدعومة للتحويل إلى PSD؟

A3: يدعم Aspose.Imaging for .NET تحويل تنسيقات الصور المتجهة مثل CDR، وEMF، وEPS، وODG، وSVG، وWMF إلى تنسيق PSD.

### س4: هل هناك أي قيود على تعقيد الأشكال أثناء التحويل؟

ج٤: حاليًا، يدعم Aspose.Imaging تصدير الأشكال البسيطة بدون فرش نسيجية، أو الأشكال المفتوحة ذات الخطوط العريضة. مع ذلك، قد يتم تحسين هذه الميزة في الإصدارات القادمة.

### س5: أين يمكنني الحصول على الدعم أو طرح الأسئلة المتعلقة بـ Aspose.Imaging لـ .NET؟

ج5: إذا كان لديك أي أسئلة أو تحتاج إلى دعم، يمكنك زيارة [منتديات Aspose.Imaging](https://forum.aspose.com/) للحصول على المساعدة.


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}