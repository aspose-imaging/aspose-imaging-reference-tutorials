---
"description": "تعرّف على كيفية تحسين جودة الصور باستخدام Aspose.Imaging لجافا. يتناول هذا البرنامج التعليمي خطوة بخطوة تطبيقات مرشحي Median وWiener لإزالة الضوضاء من الصور."
"linktitle": "تطبيق مرشح الوسيط ومرشح وينر"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Java Aspose.Imaging"
"title": "تطبيق مرشح الوسيط ومرشح وينر"
"url": "/ar/java/image-processing-and-enhancement/median-and-wiener-filter-application/"
"weight": 19
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# تطبيق مرشح الوسيط ومرشح وينر

في عالم معالجة الصور، يُعدّ إزالة التشويش وتحسين جودة الصورة مهمتين أساسيتين. Aspose.Imaging لجافا مكتبة فعّالة تُوفّر أدوات وفلاتر مُتنوّعة للعمل مع الصور. في هذا البرنامج التعليمي، سنشرح لك عملية استخدام المكتبة لتطبيق فلاتر Median وWiener لتنظيف الصورة وإزالة التشويش منها. سيساعدك هذا الدليل المُفصّل على تحسين صورك باحترافية.

## المتطلبات الأساسية

قبل الغوص في هذا البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:

1. بيئة تطوير Java: تأكد من أن لديك بيئة تطوير Java عاملة على جهاز الكمبيوتر الخاص بك.

2. Aspose.Imaging for Java: قم بتنزيل مكتبة Aspose.Imaging for Java وتثبيتها من [هنا](https://releases.aspose.com/imaging/java/).

3. صورة نموذجية ذات تشويش: جهّز صورة ذات تشويش ترغب في إزالة التشويش منها. يمكنك استخدام أي صورة من اختيارك لهذا البرنامج التعليمي.

## استيراد الحزم

في مشروع Java الخاص بك، ابدأ باستيراد الحزم اللازمة للعمل مع Aspose.Imaging لـ Java:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.imagefilters.filteroptions.MedianFilterOptions;
```

## الخطوة 1: تحميل الصورة المشوشة

الخطوة الأولى هي تحميل الصورة المشوشة باستخدام Aspose.Imaging. تأكد من تحديد مسار ملف الصورة المشوشة.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (Image image = Image.load(dataDir + "your-noisy-image.png"))
{
    // تحويل الصورة إلى RasterImage
    RasterImage rasterImage = (RasterImage) image;
```

## الخطوة 2: إنشاء وتكوين مرشح الوسيط

الآن، قم بإنشاء مثيل لـ `MedianFilterOptions` حدّد فئة وحجم الفلتر. يُحدد حجم الفلتر المساحة المحيطة بكل بكسل والتي سيتم أخذها في الاعتبار عند تطبيق الفلتر الوسيط. قد يُقلل الحجم الأكبر التشويش، ولكنه قد يُشوّش الصورة.

```java
    // قم بإنشاء مثيل لفئة MedianFilterOptions وقم بتعيين الحجم.
    MedianFilterOptions options = new MedianFilterOptions(4);
```

## الخطوة 3: تطبيق مرشح الوسيط

بعد ذلك، طبّق مرشح الوسيط على كائن الصورة النقطية باستخدام الخيارات التي حدّدتها في الخطوة السابقة. سيساعد هذا على إزالة التشويش من الصورة.

```java
    // قم بتطبيق مرشح الوسيط على كائن RasterImage.
    rasterImage.filter(image.getBounds(), options);
```

## الخطوة 4: حفظ الصورة الناتجة

بعد تطبيق مرشح الوسيط، احفظ الصورة الخالية من الضوضاء في الموقع المطلوب.

```java
    // احفظ الصورة الناتجة
    image.save("Your Document Directory" + "denoised-image.png");
}
```

تهانينا! لقد نجحت في إزالة الضوضاء من الصورة باستخدام مرشح الوسيط مع Aspose.Imaging لـ Java.

## خاتمة

في هذا البرنامج التعليمي، استكشفنا كيفية استخدام Aspose.Imaging في جافا لتطبيق مرشح متوسط لإزالة الضوضاء من الصورة. توفر هذه المكتبة مجموعة واسعة من المرشحات والأدوات، مما يجعلها موردًا قيّمًا لمهام معالجة الصور. باتباع الخطوات الموضحة في هذا الدليل، يمكنك تحسين جودة الصورة وإزالة الضوضاء بفعالية.

## الأسئلة الشائعة

### س1: ما هو Aspose.Imaging لـ Java؟

A1: Aspose.Imaging for Java هي مكتبة Java تسمح للمطورين بالعمل مع الصور وأداء مهام معالجة الصور المختلفة برمجيًا.

### س2: هل يمكنني استخدام Aspose.Imaging لـ Java مجانًا؟

A2: Aspose.Imaging for Java هي مكتبة تجارية، ولكن يمكنك الحصول على نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/)ومع ذلك، للاستخدام الموسع، ستحتاج إلى شراء ترخيص من [هنا](https://purchase.aspose.com/buy).

### س3: كيف يمكنني الحصول على الدعم لـ Aspose.Imaging لـ Java؟

ج3: يمكنك طلب المساعدة والمساعدة من مجتمع Aspose.Imaging والخبراء في [منتدى Aspose.Imaging](https://forum.aspose.com/).

### س4: ما هي بعض تقنيات تحسين الصورة الأخرى؟

A4: بالإضافة إلى مرشح الوسيط، تتضمن تقنيات تحسين الصورة ترشيح Wiener، والتمويه الغاوسي، وتمديد التباين، وغيرها.

### س5: هل يمكنني استخدام Aspose.Imaging لـ Java في تطبيق الويب الخاص بي؟

ج5: نعم، يمكنك دمج Aspose.Imaging for Java في تطبيقات الويب الخاصة بك لمعالجة الصور على جانب الخادم.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}