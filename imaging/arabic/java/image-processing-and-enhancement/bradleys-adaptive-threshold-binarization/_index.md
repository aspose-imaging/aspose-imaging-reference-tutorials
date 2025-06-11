---
"description": "تعلم تحويل الصور إلى صور ثنائية باستخدام Aspose.Imaging لجافا. حوّل صور DICOM بسهولة. استكشف دليلاً خطوة بخطوة مع أمثلة برمجية."
"linktitle": "ثنائيات عتبة برادلي التكيفية"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Java Aspose.Imaging"
"title": "تحويل الصور إلى صور ثنائية باستخدام Aspose.Imaging لـ Java"
"url": "/ar/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/"
"weight": 27
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# تحويل الصور إلى صور ثنائية باستخدام Aspose.Imaging لـ Java

تلعب الصور دورًا محوريًا في العالم الرقمي، سواءً على مواقع الويب أو في المستندات أو كجزء من تطبيقات متنوعة. تُعد معالجة الصور مهمة أساسية في هذه المجالات، ومن العمليات الأساسية فيها تحويل الصور إلى صيغة ثنائية. تُبسط هذه العملية الصورة بتحويلها إلى صيغة ثنائية، مما يُسهّل على أجهزة الكمبيوتر معالجتها. يُعد Aspose.Imaging for Java أداة فعّالة توفر مجموعة واسعة من ميزات معالجة الصور، وفي هذا البرنامج التعليمي، سنستكشف كيفية إجراء تحويل الصور إلى صيغة ثنائية باستخدام خاصية Bradley's Adaptive Threshold Binarization من Aspose.Imaging. 

## المتطلبات الأساسية

قبل الغوص في عالم تحويل الصور إلى صور ثنائية باستخدام Aspose.Imaging لـ Java، دعنا نتأكد من أن لديك كل ما تحتاجه:

### بيئة تطوير جافا

يجب أن يكون لديك بيئة تطوير جافا مُثبّتة على نظامك. إذا لم تكن مُثبّتة بالفعل، يمكنك تنزيل وتثبيت Java Development Kit (JDK) من موقع Oracle الإلكتروني.

### Aspose.Imaging لـ Java

لمتابعة هذا البرنامج التعليمي، ستحتاج إلى تثبيت Aspose.Imaging for Java. يمكنك تنزيله من موقع Aspose الإلكتروني باستخدام الرابط التالي: [تنزيل Aspose.Imaging لـ Java](https://releases.aspose.com/imaging/java/).

### صورة DICOM

ستحتاج إلى صورة DICOM ترغب في تحويلها إلى صورة ثنائية. إذا لم تكن لديك واحدة، يمكنك العثور على نماذج صور DICOM على الإنترنت، أو استخدام صور DICOM الخاصة بك.

الآن بعد أن أصبحت المتطلبات الأساسية جاهزة، دعنا ننتقل إلى الخطوة التالية.

## استيراد الحزم

في هذا القسم، سنستورد الحزم اللازمة من Aspose.Imaging لجافا. تحتوي هذه الحزم على الفئات والطرق اللازمة لتنفيذ عملية برادلي للتحويل الثنائي التكيفي للعتبة على صورة DICOM.

```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// تحميل صورة DICOM في مثيل DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // قم بتحويل الصورة إلى صورة ثنائية باستخدام عتبة برادلي التكيفية.
    image.binarizeBradley(10);
    // احفظ الصورة الناتجة.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

## الخطوة 1: تحديد المسارات

أولاً، حدد مسارات صورة DICOM المدخلة والصورة الثنائية الناتجة. استبدل `"Your Document Directory"` مع المسار الفعلي إلى الدليل الخاص بك.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

## الخطوة 2: تحميل صورة DICOM

استخدم Aspose.Imaging لتحميل صورة DICOM المحددة بواسطة `inputFile`. هذه العملية تنشئ مثيلًا لـ `DicomImage` فصل.

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // خطوات معالجة الصورة سوف تذهب هنا.
}
```

## الخطوة 3: تنفيذ عملية الثنائية

نفّذ عملية تحويل العتبة التكيفية لبرادلي إلى صورة DICOM المحملة. في هذا المثال، عتبة `10` يتم تطبيقه.

```java
image.binarizeBradley(10);
```

## الخطوة 4: حفظ الصورة الثنائية

احفظ الصورة الثنائية الناتجة في ملف الإخراج المحدد باستخدام تنسيق BMP.

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## خاتمة

تهانينا! لقد تعلمتَ بنجاح كيفية إجراء عملية تحويل الصور إلى صور ثنائية باستخدام Aspose.Imaging لجافا باستخدام تقنية Bradley's Adaptive Threshold Binarization. تتيح لك هذه الأداة الفعّالة تحسين قدراتك في معالجة الصور، مما يجعلها أداة قيّمة في تطبيقات متنوعة.

تذكر أن تستكشف وثائق Aspose.Imaging الشاملة لمزيد من إمكانيات معالجة الصور: [توثيق Aspose.Imaging لـ Java](https://reference.aspose.com/imaging/java/).

## الأسئلة الشائعة

### س1: ما هو DICOM، ولماذا هو مهم في التصوير الطبي؟

ج١: DICOM هو اختصار لـ Digital Imaging and Communications in Medicine (التصوير الرقمي والاتصالات في الطب)، وهو تنسيق قياسي للصور الطبية والمعلومات ذات الصلة. يلعب دورًا محوريًا في تخزين الصور الطبية وتبادلها وتفسيرها، مما يجعله حيويًا لمقدمي الرعاية الصحية وأنظمة التصوير الطبي.

### س2: هل يمكنني استخدام Aspose.Imaging لـ Java في مشاريعي التجارية؟

ج٢: نعم، يُقدّم Aspose.Imaging for Java نسخًا تجريبية مجانية وتراخيص تجارية. يمكنك استكشاف خياراتك والحصول على التراخيص اللازمة من [موقع Aspose](https://purchase.aspose.com/buy).

### س3: هل هناك أي تراخيص مؤقتة متاحة لأغراض الاختبار؟

ج٣: نعم، يمكنك الحصول على ترخيص مؤقت لاختبار وتقييم Aspose.Imaging لجافا. تفضل بزيارة [هذا الرابط](https://purchase.aspose.com/temporary-license/) لمزيد من المعلومات.

### س4: أين يمكنني طلب المساعدة أو مناقشة المشكلات المتعلقة بـ Aspose.Imaging for Java؟

أ4: للحصول على دعم المجتمع والمناقشات، يمكنك زيارة [منتدى Aspose.Imaging](https://forum.aspose.com/)إنه مكان رائع للعثور على إجابات لأسئلتك والتواصل مع مستخدمين آخرين.

### س5: هل Aspose.Imaging for Java مناسب لمعالجة الصور في التطبيقات الأخرى المستندة إلى Java؟

ج5: نعم، يعد Aspose.Imaging for Java متعدد الاستخدامات ويمكن استخدامه في العديد من التطبيقات المستندة إلى Java، بما في ذلك تطبيقات الويب وبرامج سطح المكتب والمزيد.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}