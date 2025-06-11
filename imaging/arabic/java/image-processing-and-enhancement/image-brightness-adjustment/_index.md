---
"description": "تعلّم كيفية ضبط سطوع الصورة باستخدام Aspose.Imaging لجافا. حسّن صورك بسهولة مع هذا الدليل الشامل."
"linktitle": "ضبط سطوع الصورة"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Java Aspose.Imaging"
"title": "ضبط سطوع الصورة باستخدام Aspose.Imaging لـ Java"
"url": "/ar/java/image-processing-and-enhancement/image-brightness-adjustment/"
"weight": 25
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# ضبط سطوع الصورة باستخدام Aspose.Imaging لـ Java

## مقدمة

في عالم معالجة الصور الرقمية المتطور باستمرار، قد يكون تحقيق مستويات السطوع والتباين المثالية مهمةً صعبة. لحسن الحظ، بفضل قوة Aspose.Imaging for Java، يمكنك ضبط سطوع صورك بسهولة. تُعد مكتبة Java متعددة الاستخدامات هذه ميزةً قيّمةً للمطورين والشركات التي تتطلب قدرات معالجة صور فعّالة. في هذا الدليل التفصيلي، سنتعمق في تفاصيل ضبط سطوع الصور باستخدام Aspose.Imaging for Java.

## المتطلبات الأساسية

قبل أن نتعمق في عالم تعديل سطوع الصورة، هناك بعض المتطلبات الأساسية التي يجب أن تتوفر لديك:

1. بيئة تطوير جافا: تأكد من وجود بيئة تطوير جافا فعّالة على نظامك. إذا لم تكن لديك بالفعل، يمكنك تنزيل أحدث إصدار من جافا وتثبيته من [موقع إلكتروني](https://www.oracle.com/java/technologies/javase-downloads).

2. Aspose.Imaging لجافا: ستحتاج إلى تثبيت Aspose.Imaging لجافا. إذا لم تقم بذلك بعد، يمكنك العثور على تعليمات التثبيت والوثائق على موقع Aspose.Imaging الإلكتروني على [توثيق Aspose.Imaging لـ Java](https://reference.aspose.com/imaging/java/).

3. صورة نموذجية: جهّز الصورة التي ترغب في تعديل سطوعها. يمكنك استخدام صورتك الخاصة أو تنزيل صورة نموذجية للتجربة.

4. بيئة التطوير المتكاملة (IDE): يجب أن يكون لديك بيئة تطوير متكاملة مثبتة، مثل Eclipse، أو IntelliJ IDEA، أو أي بيئة تطوير Java أخرى من اختيارك.

بعد وضع هذه المتطلبات الأساسية، ستكون جاهزًا لبدء ضبط سطوع صورك باستخدام Aspose.Imaging for Java.

## استيراد الحزم

أولاً، تأكد من استيراد الحزم المطلوبة لمشروع Java الخاص بك:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import com.aspose.imaging.imageoptions.BmpOptions;
```

الآن بعد أن قمنا بتغطية المتطلبات الأساسية والواردات، دعنا نقوم بتقسيم عملية ضبط سطوع الصورة إلى دليل خطوة بخطوة:

## الخطوة 1: تحديد مسارات الملفات

للبدء، حدد مسارات ملفات الإدخال والإخراج. استبدل `"Your Document Directory"` مع المسار الفعلي إلى دليل العمل الخاص بك.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingBrightness_out.bmp";
```

## الخطوة 2: تحميل صورة DICOM

استخدم Aspose.Imaging لتحميل صورة DICOM. يمكنك القيام بذلك باستخدام الكود التالي:

```java
try (DicomImage image = (DicomImage) Image.load(inputFile)) {
    // يذهب كود معالجة الصور الخاص بك إلى هنا.
}
```

## الخطوة 3: ضبط السطوع

داخل `try` كتلة، اضبط سطوع الصورة المُحمّلة. يمكنك التحكم في درجة ضبط السطوع بتحديد القيمة داخل `adjustBrightness` على سبيل المثال، لزيادة السطوع بمقدار ٥٠، استخدم:

```java
image.adjustBrightness(50);
```

يمكنك أيضًا تقليل السطوع عن طريق تحديد قيمة سلبية.

## الخطوة 4: حفظ الصورة الناتجة

بعد ضبط السطوع، حان وقت حفظ الصورة المعدّلة. استخدم الكود التالي لحفظ الصورة بالتنسيق والخيارات المطلوبة:

```java
image.save(outputFile, new BmpOptions());
```

هذا كل شيء! لقد نجحت في ضبط سطوع صورتك باستخدام Aspose.Imaging لـ Java.

## خاتمة

في هذا البرنامج التعليمي، استكشفنا كيفية ضبط سطوع الصورة باستخدام Aspose.Imaging for Java. تُبسّط هذه المكتبة الفعّالة مهام معالجة الصور، وتوفر مجموعة واسعة من الخيارات لتخصيص تعديلات صورك. سواء كنت تُحسّن صورك، أو تُحضّر صورًا طبية، أو تُحسّن العناصر المرئية لشركتك، فإن Aspose.Imaging for Java هو أداتك المُفضّلة لمعالجة الصور باحترافية.

باتباع الخطوات الموضحة في هذا الدليل، يمكنك بسهولة ضبط سطوع صورك وتحقيق النتائج المرجوة. ابدأ الآن بالتجربة واكتشف إمكانيات صورك الكاملة مع Aspose.Imaging for Java.

## الأسئلة الشائعة

### س1: هل برنامج Aspose.Imaging for Java مناسب لمهام معالجة الصور الاحترافية؟

ج1: نعم، Aspose.Imaging for Java هي مكتبة متعددة الاستخدامات مصممة لمعالجة الصور بشكل احترافي، وتوفر مجموعة واسعة من الميزات والخيارات.

### س2: هل يمكنني استخدام Aspose.Imaging لـ Java مع مكتبات Java الأخرى؟

ج٢: بالتأكيد! يُمكن دمج Aspose.Imaging لـ Java بسلاسة مع مكتبات وأطر عمل Java الأخرى.

### س3: ما هي تنسيقات الصور التي يدعمها Aspose.Imaging لـ Java؟

A3: يدعم Aspose.Imaging for Java مجموعة واسعة من تنسيقات الصور، بما في ذلك BMP وJPEG وPNG وTIFF وGIF والمزيد.

### س4: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Imaging لنظام Java؟

ج٤: نعم، يمكنك تجربة Aspose.Imaging لـ Java مجانًا. تفضل بزيارة [هنا](https://releases.aspose.com/) للبدء.

### س5: أين يمكنني الحصول على الدعم أو المساعدة فيما يتعلق بـ Aspose.Imaging لـ Java؟

أ5: يمكنك العثور على المساعدة والانضمام إلى المجتمع في [منتدى Aspose.Imaging لـ Java](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}