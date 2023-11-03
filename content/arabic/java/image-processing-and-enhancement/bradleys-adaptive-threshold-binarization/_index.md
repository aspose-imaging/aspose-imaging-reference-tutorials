---
title: الصورة الثنائية مع Aspose.Imaging لجافا
linktitle: برادلي عتبة التكيف الثنائية
second_title: Aspose.Imaging واجهة برمجة تطبيقات معالجة الصور لجافا
description: تعلم ثنائية الصورة باستخدام Aspose.Imaging لـ Java. تحويل صور DICOM بسهولة. استكشف دليلاً خطوة بخطوة مع أمثلة التعليمات البرمجية.
type: docs
weight: 27
url: /ar/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
---
تلعب الصور دورًا حاسمًا في العالم الرقمي، سواء على مواقع الويب أو في المستندات أو كجزء من التطبيقات المختلفة. تعد معالجة الصور مهمة أساسية في هذه المجالات، وإحدى العمليات الأساسية هي ثنائية الصورة. تعمل عملية Binarization على تبسيط الصورة عن طريق تحويلها إلى نموذج ثنائي، مما يسهل على أجهزة الكمبيوتر معالجتها. تعد Aspose.Imaging for Java أداة قوية توفر نطاقًا واسعًا من ميزات معالجة الصور، وفي هذا البرنامج التعليمي، سنستكشف كيفية إجراء عملية ثنائية الصورة باستخدام Aspose.Imaging's Bradley's Adaptive Threshold Binarization. 

## المتطلبات الأساسية

قبل الغوص في عالم ثنائية الصور باستخدام Aspose.Imaging for Java، دعنا نتأكد من أن لديك كل ما تحتاجه:

### بيئة تطوير جافا

يجب أن يكون لديك بيئة تطوير Java معدة على نظامك. إذا لم تكن قد قمت بذلك بالفعل، فيمكنك تنزيل وتثبيت Java Development Kit (JDK) من موقع Oracle على الويب.

### Aspose.Imaging لجافا

لمتابعة هذا البرنامج التعليمي، ستحتاج إلى تثبيت Aspose.Imaging for Java. ويمكنك تحميله من موقع Aspose باستخدام الرابط التالي:[تحميل Aspose.Imaging لجافا](https://releases.aspose.com/imaging/java/).

### صورة ديكوم

ستحتاج إلى صورة DICOM التي تريد تحويلها إلى صيغة ثنائية. إذا لم يكن لديك واحدة، يمكنك العثور على نماذج صور DICOM عبر الإنترنت، أو يمكنك استخدام صور DICOM الخاصة بك.

الآن بعد أن اكتملت متطلباتك الأساسية، دعنا ننتقل إلى الخطوة التالية.

## حزم الاستيراد

في هذا القسم، سنقوم باستيراد الحزم الضرورية من Aspose.Imaging for Java. تحتوي هذه الحزم على الفئات والأساليب اللازمة لتنفيذ عملية Bradley's Adaptive Threshold Binarization على صورة DICOM.

```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// قم بتحميل صورة DICOM في مثيل DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // ثنائية الصورة مع عتبة برادلي التكيفية.
    image.binarizeBradley(10);
    // احفظ الصورة الناتجة.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

## الخطوة 1: تحديد المسارات

 أولاً، حدد المسارات لصورة DICOM المدخلة وصورة الإخراج الثنائية. يستبدل`"Your Document Directory"` مع المسار الفعلي إلى الدليل الخاص بك.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

## الخطوة 2: قم بتحميل صورة DICOM

استخدم Aspose.Imaging لتحميل صورة DICOM المحددة بواسطة`inputFile` . تقوم هذه العملية بإنشاء مثيل لـ`DicomImage` فصل.

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // سيتم الانتقال إلى خطوات معالجة الصور هنا.
}
```

## الخطوة 3: تنفيذ الثنائية

 قم بتنفيذ عملية Bradley's Adaptive Threshold Binarization على صورة DICOM المحملة. في هذا المثال، عتبة`10` يتم تطبيقه.

```java
image.binarizeBradley(10);
```

## الخطوة 4: احفظ الصورة الثنائية

احفظ الصورة الثنائية الناتجة في ملف الإخراج المحدد باستخدام تنسيق BMP.

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية إجراء ثنائية الصورة باستخدام Aspose.Imaging لـ Java باستخدام Adaptive Threshold Binarization من Bradley. تتيح لك هذه الأداة القوية تحسين قدرات معالجة الصور لديك، مما يجعلها أحد الأصول القيمة في التطبيقات المختلفة.

 تذكر أن تستكشف وثائق Aspose.Imaging الشاملة لمزيد من إمكانيات معالجة الصور:[Aspose.Imaging لتوثيق جافا](https://reference.aspose.com/imaging/java/).

## الأسئلة الشائعة

### س1: ما هو DICOM وما أهميته في التصوير الطبي؟

ج1: يرمز DICOM إلى التصوير الرقمي والاتصالات في الطب، وهو تنسيق قياسي للصور الطبية والمعلومات ذات الصلة. فهو يلعب دورًا حاسمًا في تخزين الصور الطبية وتبادلها وتفسيرها، مما يجعله أمرًا حيويًا لمتخصصي الرعاية الصحية وأنظمة التصوير الطبي.

### س2: هل يمكنني استخدام Aspose.Imaging for Java في مشاريعي التجارية؟

 ج2: نعم، يقدم Aspose.Imaging for Java كلا من التجارب المجانية والتراخيص التجارية. يمكنك استكشاف خياراتك والحصول على الترخيص اللازم من[موقع Aspose](https://purchase.aspose.com/buy).

### س3: هل هناك أي تراخيص مؤقتة متاحة لأغراض الاختبار؟

 ج3: نعم، يمكنك الحصول على ترخيص مؤقت لاختبار وتقييم Aspose.Imaging for Java. يزور[هذا الرابط](https://purchase.aspose.com/temporary-license/) للمزيد من المعلومات.

### س4: أين يمكنني طلب المساعدة أو مناقشة المشكلات المتعلقة بـ Aspose.Imaging for Java؟

 ج4: للحصول على دعم المجتمع والمناقشات، يمكنك زيارة[Aspose.منتدى التصوير](https://forum.aspose.com/). إنه مكان رائع للعثور على إجابات لأسئلتك والتواصل مع المستخدمين الآخرين.

### س 5: هل Aspose.Imaging for Java مناسب لمعالجة الصور في التطبيقات الأخرى المستندة إلى Java؟

ج5: نعم، يعد Aspose.Imaging for Java متعدد الاستخدامات ويمكن استخدامه في العديد من التطبيقات المستندة إلى Java، بما في ذلك تطبيقات الويب وبرامج سطح المكتب والمزيد.