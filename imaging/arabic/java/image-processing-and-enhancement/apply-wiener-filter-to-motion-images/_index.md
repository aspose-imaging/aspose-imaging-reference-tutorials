---
date: 2026-01-09
description: دليل معالجة الصور في جافا باستخدام Aspose.Imaging لجافا. تعلم كيفية تطبيق
  مرشح وينر وتحويل الصورة إلى تدرج الرمادي بأسلوب جافا لتحسين صور الحركة.
linktitle: Apply Wiener Filter to Motion Images
second_title: Aspose.Imaging Java Image Processing API
title: 'دليل معالجة الصور في جافا: مرشح وينر'
url: /ar/java/image-processing-and-enhancement/apply-wiener-filter-to-motion-images/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# دليل معالجة الصور بجافا: مرشح واينر

في هذا **دليل معالجة الصور بجافا**، سنوضح لك كيفية تحسين الصور التي تعرضت لطمس الحركة عن طريق تطبيق مرشح واينر باستخدام Aspose.Imaging for Java. ستشاهد كود خطوة بخطوة، وتتعرف على سبب فعالية المرشح، وتكتشف كيفية **تحويل الصورة إلى تدرج الرمادي java** عند الحاجة. في النهاية ستحصل على صورة نظيفة ومحدبة جاهزة للاستخدام اللاحق.

## إجابات سريعة
- **ماذا يفعل مرشح واينر؟** يقلل من طمس الحركة والضوضاء مع الحفاظ على الحواف.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للاختبار؛ الترخيص مطلوب للإنتاج.  
- **ما نسخة جافا المدعومة؟** Java 8 أو أعلى.  
- **هل يمكنني معالجة الصور الملونة؟** نعم – اضبط `setGrayscale(false)` للاحتفاظ بالألوان.  
- **كم يستغرق المعالجة؟** عادةً أقل من ثانية للصور ذات الحجم العادي.

## ما هو دليل معالجة الصور بجافا؟
**دليل معالجة الصور بجافا** يوجه المطورين عبر مهام تعديل الصور الشائعة—التحميل، والترشيح، والتحويل، والحفظ—باستخدام مكتبات جافا. هنا نركز على إزالة طمس الحركة باستخدام مرشح واينر.

## لماذا نستخدم مرشح واينر للصور المتحركة؟
غالبًا ما يظهر طمس الحركة كخطوط عندما تتحرك الكاميرا أثناء التعرض. يقوم مرشح واينر بتقدير المشهد الأصلي عن طريق نمذجة الطمس كحركة خطية ثم تطبيق ترشيح عكسي. النتيجة صورة أكثر حدة مع تقليل الضوضاء، مثالية للتصوير الفوتوغرافي، والمراقبة، أو التحضير المسبق لخوارزميات الرؤية الحاسوبية.

## المتطلبات المسبقة

- **بيئة تطوير جافا** – JDK 8 أو أحدث مثبتة.  
- **مكتبة Aspose.Imaging for Java** – حمّلها من [رابط التحميل](https://releases.aspose.com/imaging/java/).  
- **معرفة أساسية بمعالجة الصور** – الإلمام بمفاهيم مثل الصور النقطية والفلاتر يساعد.

## استيراد الحزم

في مشروع جافا الخاص بك، استورد الفئات المطلوبة من Aspose.Imaging:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.png.PngImage;
import com.aspose.imaging.imagefilters.filtertype.MotionWienerFilterOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل الصورة

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";
try (Image image = Image.load(dataDir + "your-motion-image.png"))
{
```

استبدل `"your-motion-image.png"` باسم ملف الصورة التي تحتوي على طمس الحركة والتي تريد تنظيفها.

### الخطوة 2: تحويل نوع الصورة

```java
    // Cast the image into RasterImage
    RasterImage rasterImage = (RasterImage) image;
```

تحويل الصورة إلى `RasterImage` يمنحك إمكانية الوصول إلى عمليات على مستوى البكسل المطلوبة للمرشح.

### الخطوة 3: إنشاء خيارات مرشح واينر  

هنا نوضح أيضًا **تحويل الصورة إلى تدرج الرمادي java** عبر تفعيل علم التدرج الرمادي.

```java
    // Create an instance of MotionWienerFilterOptions class and set the
    // length, smooth value, and angle.
    MotionWienerFilterOptions options = new MotionWienerFilterOptions(50, 9, 90);
    options.setGrayscale(true);
```

- **Length (50)** – الطول التقريبي لطمس الحركة بالبكسل.  
- **Smooth (9)** – يتحكم في مقدار التنعيم؛ القيم الأعلى تقلل الضوضاء بشكل أكثر حدة.  
- **Angle (90)** – اتجاه طمس الحركة بالدرجة.  
- **Grayscale** – اضبطه `true` لتحويل الصورة إلى تدرج رمادي قبل الترشيح (مفيد للعديد من خطوط التحليل).

### الخطوة 4: تطبيق مرشح واينر

```java
    // Apply the Wiener filter to the RasterImage object.
    rasterImage.filter(image.getBounds(), options);
```

يقوم المرشح بمعالجة كل بكسل داخل حدود الصورة باستخدام الخيارات المحددة أعلاه.

### الخطوة 5: حفظ الصورة الناتجة

```java
    // Save the resultant image
    image.save("Your Document Directory" + "FilteredMotionImage.png");
}
```

اختر اسم ملف إخراج يعكس سير عملك. الملف المحفوظ سيحتوي على الصورة التي تم إزالة طمسها، وربما تحويلها إلى تدرج رمادي إذا اخترت ذلك.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **الصورة لا تزال ضبابية** | قيم معلمات المرشح (الطول، النعومة، الزاوية) لا تتطابق مع الطمس الفعلي. | جرّب قيمًا مختلفة؛ استخدم الفحص البصري أو مقاييس آلية. |
| **Memory OutOfMemoryError** | الصور الكبيرة جدًا تستهلك ذاكرة RAM كثيرة. | عالج الصورة على أجزاء (tiles) أو زد حجم heap في JVM (`-Xmx`). |
| **تحول الصور الملونة إلى تدرج رمادي** | تم تفعيل `setGrayscale(true)`. | اضبط `options.setGrayscale(false)` للاحتفاظ بالألوان. |

## الأسئلة المتكررة

### س1: ما هو مرشح واينر وكيف يعمل؟
**ج:** مرشح واينر تقنية إحصائية تقدّر الصورة الأصلية عن طريق تقليل متوسط الخطأ التربيعي بين الصورة المفلترة والصورة الحقيقية، مما يقلل الضوضاء وطمس الحركة.

### س2: هل يمكنني تطبيق مرشح واينر على الصور الملونة أيضًا؟
**ج:** نعم. اضبط `options.setGrayscale(false)` للاحتفاظ بالقنوات اللونية الأصلية أثناء الترشيح.

### س3: هل Aspose.Imaging for Java مناسب للمعالجة في الوقت الحقيقي؟
**ج:** هو ممتاز للمعالجة الدفعة وغير المتصلة. للمتطلبات الفورية، قد تحتاج إلى مكتبة موجهة للبث أو تسريع GPU أصلي.

### س4: أين يمكنني تحميل مكتبة Aspose.Imaging for Java؟
**ج:** من صفحة التحميل الرسمية: [رابط التحميل](https://releases.aspose.com/imaging/java/).

### س5: كيف أحصل على مساعدة إذا واجهت مشاكل؟
**ج:** زر منتدى المجتمع على [منتدى دعم Aspose.Imaging for Java](https://forum.aspose.com/) للحصول على مساعدة من خبراء Aspose ومطوريين آخرين.

## الخلاصة

لقد أكملت الآن **دليل معالجة الصور بجافا** الكامل الذي يحمل صورة طمس الحركة، يضبط مرشح واينر (مع خيار تحويل إلى تدرج رمادي اختياري)، يطبق المرشح، ويحفظ النتيجة المنقاة. لا تتردد في تعديل معلمات المرشح لتتناسب مع أنماط طمس مختلفة، أو ربط فلاتر إضافية لمزيد من التحسين.

لمزيد من التفاصيل، استكشف الوثائق الرسمية: [توثيق Aspose.Imaging for Java](https://reference.aspose.com/imaging/java/).

---

**آخر تحديث:** 2026-01-09  
**تم الاختبار مع:** Aspose.Imaging for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}