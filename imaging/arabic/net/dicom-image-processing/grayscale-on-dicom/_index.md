---
"description": "تعرف على كيفية إجراء التدرج الرمادي على صور DICOM باستخدام Aspose.Imaging لـ .NET، وهي مكتبة معالجة صور قوية."
"linktitle": "تدرج الرمادي على DICOM في Aspose.Imaging لـ .NET"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Aspose.Imaging .NET"
"title": "صور DICOM بدرجات الرمادي مع Aspose.Imaging لـ .NET"
"url": "/ar/net/dicom-image-processing/grayscale-on-dicom/"
"weight": 24
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# صور DICOM بدرجات الرمادي مع Aspose.Imaging لـ .NET

إذا كنت تعمل على بيانات التصوير الطبي بتنسيق DICOM وتحتاج إلى إجراء تحويلات تدرج الرمادي، فإن Aspose.Imaging for .NET يقدم حلاً فعالاً. في هذا البرنامج التعليمي المفصل، سنشرح لك عملية تحويل صورة DICOM إلى تدرج الرمادي باستخدام Aspose.Imaging. تُعد هذه المكتبة أداة متعددة الاستخدامات تتيح لك العمل مع تنسيقات صور متنوعة، بما في ذلك DICOM، في بيئة .NET. هيا بنا نبدأ!

## المتطلبات الأساسية

قبل أن تبدأ، تأكد من توفر المتطلبات الأساسية التالية:

1. Aspose.Imaging لـ .NET: يجب أن تكون هذه المكتبة مثبتة لديك. يمكنك تنزيلها من [صفحة تنزيل Aspose.Imaging لـ .NET](https://releases.aspose.com/imaging/net/).

2. صورة DICOM: يجب أن يكون لديك صورة DICOM ترغب في تدرجها الرمادي. إذا لم تكن لديك واحدة، يمكنك العثور على نماذج لصور DICOM لأغراض الاختبار.

## استيراد مساحات الأسماء

أولاً، دعنا نستورد مساحات الأسماء الضرورية للعمل مع Aspose.Imaging:

```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

الآن بعد أن قمت بوضع المتطلبات الأساسية واستيراد مساحات الأسماء، يمكننا المضي قدمًا في عملية التدرج الرمادي خطوة بخطوة.

## الخطوة 1: تهيئة صورة DICOM

نبدأ بتهيئة صورة DICOM. في هذا المثال، نفترض أن اسم ملف DICOM هو "file.dcm" وأنه موجود في مجلد محدد بواسطة `dataDir`.

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
```

## الخطوة 2: تحويل التدرج الرمادي

الخطوة التالية هي تحويل صورة DICOM المحملة إلى تمثيلها بالدرجات الرمادية باستخدام `Grayscale()` هذه الطريقة تقوم بتحويل الصورة تلقائيًا إلى تدرج الرمادي.

```csharp
{
    // تحويل الصورة إلى تمثيلها بالدرجات الرمادية
    image.Grayscale();
}
```

## الخطوة 3: حفظ الصورة ذات التدرج الرمادي

بعد تدرج اللون الرمادي في الصورة، يمكنك حفظها. في هذا المثال، نحفظها بتنسيق BMP باستخدام `BmpOptions()`.

```csharp
image.Save(dataDir + "GrayscalingOnDICOM_out.bmp", new BmpOptions());
```

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية إجراء تدرج الرمادي على صورة DICOM باستخدام Aspose.Imaging لـ .NET. تُبسّط هذه المكتبة عملية العمل مع بيانات التصوير الطبي، وتتيح لك إجراء تحويلات متنوعة بسهولة. سواء كنت تعمل على أبحاث طبية أو تطبيقات رعاية صحية، يُمكن أن تكون Aspose.Imaging أداة قيّمة في مجموعة أدوات تطوير .NET الخاصة بك.

## الأسئلة الشائعة

### س1: ما هو DICOM؟

ج١: DICOM هو اختصار لـ Digital Imaging and Communications in Medicine (التصوير الرقمي والاتصالات في الطب). وهو معيار لمعالجة الصور الطبية وتخزينها وطباعتها ونقلها.

### س2: هل برنامج Aspose.Imaging مناسب لمعالجة الصور غير الطبية؟

ج2: نعم، Aspose.Imaging هي مكتبة متعددة الاستخدامات يمكنها التعامل مع مجموعة واسعة من تنسيقات الصور لتطبيقات مختلفة تتجاوز التصوير الطبي.

### س3: أين يمكنني العثور على مزيد من الوثائق؟

أ3: يمكنك الرجوع إلى [توثيق Aspose.Imaging لـ .NET](https://reference.aspose.com/imaging/net/) لمزيد من المعلومات والأمثلة التفصيلية.

### س4: هل هناك نسخة تجريبية مجانية متاحة؟

ج4: نعم، يمكنك الوصول إلى [تجربة مجانية لبرنامج Aspose.Imaging](https://releases.aspose.com/) لتقييم قدراتها.

### س5: كيف يمكنني الحصول على الدعم لـ Aspose.Imaging؟

ج5: إذا كان لديك أي أسئلة أو تحتاج إلى مساعدة، يمكنك زيارة [منتدى Aspose.Imaging](https://forum.aspose.com/) لطلب المساعدة من المجتمع أو الاتصال بفريق الدعم الخاص بهم.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}