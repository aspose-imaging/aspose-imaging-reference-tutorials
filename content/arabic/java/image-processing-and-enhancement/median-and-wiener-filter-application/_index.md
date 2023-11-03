---
title: تطبيق مرشح الوسيط و وينر
linktitle: تطبيق مرشح الوسيط و وينر
second_title: Aspose.Imaging واجهة برمجة تطبيقات معالجة الصور لجافا
description: تعرف على كيفية تحسين جودة الصورة باستخدام Aspose.Imaging for Java. يغطي هذا البرنامج التعليمي خطوة بخطوة تطبيقات مرشح Median وWiener لتقليل ضوضاء الصورة.
type: docs
weight: 19
url: /ar/java/image-processing-and-enhancement/median-and-wiener-filter-application/
---
في عالم معالجة الصور، تعد إزالة الضوضاء وتحسين جودة الصورة من المهام الحاسمة. Aspose.Imaging for Java هي مكتبة قوية توفر أدوات ومرشحات متنوعة للعمل مع الصور. في هذا البرنامج التعليمي، سنرشدك خلال عملية استخدام المكتبة لتطبيق مرشحات Median وWiener لتنظيف الصورة وتقليل التشويش. سيساعدك هذا الدليل المفصّل خطوة بخطوة على تحقيق تحسين احترافي للصورة.

## المتطلبات الأساسية

قبل الغوص في هذا البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

1. بيئة تطوير Java: تأكد من أن لديك بيئة تطوير Java عاملة على جهاز الكمبيوتر الخاص بك.

2. Aspose.Imaging for Java: قم بتنزيل وتثبيت مكتبة Aspose.Imaging for Java من[هنا](https://releases.aspose.com/imaging/java/).

3. نموذج صورة مزعجة: قم بإعداد صورة مزعجة تريد تقليل الضوضاء فيها. يمكنك استخدام أي صورة من اختيارك لهذا البرنامج التعليمي.

## حزم الاستيراد

في مشروع Java الخاص بك، ابدأ باستيراد الحزم اللازمة للعمل مع Aspose.Imaging for Java:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.imagefilters.filteroptions.MedianFilterOptions;
```

## الخطوة 1: قم بتحميل الصورة المزعجة

الخطوة الأولى هي تحميل الصورة المزعجة باستخدام Aspose.Imaging. تأكد من تحديد المسار إلى ملف الصورة المزعج.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (Image image = Image.load(dataDir + "your-noisy-image.png"))
{
    // إرسال الصورة إلى RasterImage
    RasterImage rasterImage = (RasterImage) image;
```

## الخطوة 2: إنشاء وتكوين عامل التصفية المتوسط

 الآن، قم بإنشاء مثيل لـ`MedianFilterOptions` فئة وتكوين حجم عامل التصفية. يحدد حجم المرشح المنطقة المحيطة بكل بكسل والتي سيتم أخذها في الاعتبار عند تطبيق المرشح المتوسط. يمكن أن يؤدي الحجم الأكبر إلى تقليل الضوضاء ولكنه قد يؤدي إلى تشويش الصورة.

```java
    // قم بإنشاء مثيل لفئة MedianFilterOptions وقم بتعيين الحجم.
    MedianFilterOptions options = new MedianFilterOptions(4);
```

## الخطوة 3: تطبيق مرشح المتوسط

بعد ذلك، قم بتطبيق مرشح Median على كائن RasterImage باستخدام الخيارات التي قمت بتكوينها في الخطوة السابقة. سيساعد هذا في إزالة الضوضاء من الصورة.

```java
    // تطبيق عامل التصفية المتوسط على كائن RasterImage.
    rasterImage.filter(image.getBounds(), options);
```

## الخطوة 4: احفظ الصورة الناتجة

بعد تطبيق مرشح الوسيط، احفظ الصورة المخففة للضوضاء في الموقع الذي تريده.

```java
    // احفظ الصورة الناتجة
    image.save("Your Document Directory" + "denoised-image.png");
}
```

تهانينا! لقد نجحت في إزالة الضوضاء من الصورة باستخدام مرشح Median مع Aspose.Imaging for Java.

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا كيفية استخدام Aspose.Imaging لـ Java لتطبيق مرشح متوسط لتقليل الضوضاء في الصورة. توفر هذه المكتبة مجموعة واسعة من المرشحات والأدوات، مما يجعلها مصدرًا قيمًا لمهام معالجة الصور. باتباع الخطوات الموضحة في هذا الدليل، يمكنك تحسين جودة الصورة وإزالة التشويش بفعالية.

## الأسئلة الشائعة

### س1: ما هو Aspose.Imaging لـ Java؟

A1: Aspose.Imaging for Java هي مكتبة Java تسمح للمطورين بالعمل مع الصور وتنفيذ مهام معالجة الصور المتنوعة برمجيًا.

### س2: هل يمكنني استخدام Aspose.Imaging لـ Java مجانًا؟

 ج2: Aspose.Imaging for Java هي مكتبة تجارية، ولكن يمكنك الحصول على نسخة تجريبية مجانية منها[هنا](https://releases.aspose.com/) ومع ذلك، للاستخدام الممتد، سوف تحتاج إلى شراء ترخيص من[هنا](https://purchase.aspose.com/buy).

### س3: كيف يمكنني الحصول على دعم Aspose.Imaging لـ Java؟

 ج3: يمكنك طلب المساعدة والمساعدة من مجتمع Aspose.Imaging والخبراء في[Aspose.منتدى التصوير](https://forum.aspose.com/).

### س4: ما هي بعض تقنيات تحسين الصورة الأخرى؟

ج4: بالإضافة إلى عامل التصفية المتوسط، تشتمل تقنيات تحسين الصورة على تصفية Wiener، وتمويه Gaussian، وتمديد التباين، من بين أمور أخرى.

### س5: هل يمكنني استخدام Aspose.Imaging for Java في تطبيق الويب الخاص بي؟

ج5: نعم، يمكنك دمج Aspose.Imaging for Java في تطبيقات الويب الخاصة بك لمعالجة الصور من جانب الخادم.