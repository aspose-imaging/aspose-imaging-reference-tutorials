---
date: 2026-01-17
description: تعلم كيفية استخدام مرشح المتوسط في جافا مع Aspose.Imaging لإزالة ضوضاء
  الصورة. يغطي هذا الدليل خطوة بخطوة تطبيق مرشحات المتوسط وواينر لإزالة الضوضاء من
  الصور.
linktitle: Median Filter Java – Apply Median and Wiener Filters
second_title: Aspose.Imaging Java Image Processing API
title: مرشح المتوسط جافا – تطبيق مرشحات المتوسط وواينر
url: /ar/java/image-processing-and-enhancement/median-and-wiener-filter-application/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Median Filter Java – تطبيق مرشحات Median و Wiener

في عالم معالجة الصور، إزالة الضوضاء وتحسين جودة الصورة من المهام الحيوية. باستخدام **median filter java**، يمكنك تنظيف الصور المشوشة بفعالية باستخدام Aspose.Imaging for Java. في هذا الدرس، سنرشدك خلال عملية تطبيق مرشحات Median و Wiener لإزالة الضوضاء من الصورة، حتى تتمكن من الحصول على نتائج بمستوى احترافي دون كتابة كود معقد.

## إجابات سريعة
- **ما الذي يفعله مرشح المتوسط؟** يستبدل كل بكسل بقيمة المتوسط للجوار المحيط به، مما يزيل ضوضاء النبضات مع الحفاظ على الحواف.  
- **أي مكتبة تدعم median filter java؟** Aspose.Imaging for Java توفر فئة `MedianFilterOptions` جاهزة للاستخدام.  
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** النسخة التجريبية المجانية تعمل للتقييم؛ يلزم ترخيص تجاري للإنتاج.  
- **هل يمكنني ربط مرشح المتوسط بمرشحات أخرى؟** نعم، يمكنك تطبيق مرشحات إضافية مثل Wiener بعد خطوة المتوسط.  
- **ما صيغ الصور المدعومة؟** معظم صيغ الصور النقطية (PNG، JPEG، BMP، TIFF، إلخ) مدعومة بالكامل.

## ما هو Median Filter Java؟
مرشح المتوسط هو تقنية ترشيح رقمية غير خطية تُستخدم عادةً **لإزالة ضوضاء الصورة**. في Java، تقوم Aspose.Imaging بتنفيذ هذا المرشح عبر فئة `MedianFilterOptions`، مما يتيح لك تحديد حجم النواة الذي يحدد عدد البكسلات المجاورة التي يتم أخذها في الاعتبار.

## لماذا نستخدم Median Filter Java لإزالة الضوضاء من الصور؟
- **يحافظ على الحواف** بشكل أفضل من مرشحات المتوسط البسيطة.  
- **واجهة برمجة تطبيقات بسيطة** – بضع أسطر من الكود تزيل الضوضاء النقطية وملح‑وفلفل.  
- **يعمل على أي صورة نقطية** تم تحميلها باستخدام Aspose.Imaging، مما يجعله مثالياً للمعالجة على الخادم.

## المتطلبات المسبقة
قبل البدء، تأكد من وجود ما يلي:

1. **بيئة تطوير Java** – JDK 8 أو أحدث مثبت.  
2. **Aspose.Imaging for Java** – قم بتنزيل وتثبيت المكتبة من [here](https://releases.aspose.com/imaging/java/).  
3. **صورة مشوشة تجريبية** – أي صورة تريد تنظيفها؛ في هذا الدليل سنستخدم `your‑noisy‑image.png`.  

## استيراد الحزم
في مشروع Java الخاص بك، ابدأ باستيراد الفئات الضرورية من Aspose.Imaging:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.imagefilters.filteroptions.MedianFilterOptions;
```

## كيفية تطبيق Median Filter Java
فيما يلي دليل خطوة بخطوة. كل خطوة تتضمن شرحًا مختصرًا يليه الكود الدقيق الذي تحتاج إلى نسخه.

### الخطوة 1: تحميل الصورة المشوشة
أولاً، قم بتحميل الصورة التي تريد إزالة الضوضاء منها. هذا يوضح **load image java** باستخدام طريقة `Image.load` من Aspose.Imaging.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (Image image = Image.load(dataDir + "your-noisy-image.png"))
{
    // Cast the image into RasterImage
    RasterImage rasterImage = (RasterImage) image;
```

### الخطوة 2: إنشاء وتكوين مرشح المتوسط
أنشئ مثيلاً من `MedianFilterOptions` وحدد حجم النواة. الحجم الأكبر يزيل المزيد من الضوضاء لكنه قد يطمس التفاصيل.

```java
    // Create an instance of MedianFilterOptions class and set the size.
    MedianFilterOptions options = new MedianFilterOptions(4);
```

### الخطوة 3: تطبيق مرشح المتوسط
طبق المرشح على كامل حدود الصورة. هذه هي العملية الأساسية لـ **apply median filter**.

```java
    // Apply Median filter to RasterImage object.
    rasterImage.filter(image.getBounds(), options);
```

### الخطوة 4: حفظ الصورة الناتجة
أخيرًا، احفظ الصورة التي تمت إزالة الضوضاء منها إلى القرص. يمكنك الآن رؤية تأثير مرشح المتوسط.

```java
    // Save the resultant image
    image.save("Your Document Directory" + "denoised-image.png");
}
```

## المشكلات الشائعة والحلول
- **حجم النواة كبير جدًا** – قد تظهر الصورة مموهة بشكل مفرط. جرّب قيمًا بين 3‑5 لمعظم الصور الفوتوغرافية.  
- **صيغة صورة غير مدعومة** – تأكد من أن الملف بصيغة نقطية مدعومة من قبل Aspose.Imaging.  
- **OutOfMemoryError** – عالج الصور الكبيرة على قطع أصغر باستخدام طريقة `crop` في `RasterImage` قبل الترشيح.

## الخلاصة
في هذا الدليل، عرضنا **كيفية إزالة الضوضاء من الصور** باستخدام نهج **median filter java** المقدم من Aspose.Imaging. باتباع الخطوات أعلاه، يمكنك دمج إزالة الضوضاء بسرعة في أي خط معالجة صور مبني على Java، ويمكنك تحسين النتائج أكثر بربط مرشح Wiener أو تقنيات متقدمة أخرى.

## الأسئلة المتكررة

**س1: ما هو Aspose.Imaging for Java؟**  
ج1: Aspose.Imaging for Java هي مكتبة Java تتيح للمطورين العمل مع الصور وأداء مهام معالجة الصور المختلفة برمجيًا.

**س2: هل يمكنني استخدام Aspose.Imaging for Java مجانًا؟**  
ج2: Aspose.Imaging for Java هي مكتبة تجارية، ولكن يمكنك الحصول على نسخة تجريبية مجانية من [here](https://releases.aspose.com/). ومع ذلك، للاستخدام الموسع، ستحتاج إلى شراء ترخيص من [here](https://purchase.aspose.com/buy).

**س3: كيف يمكنني الحصول على دعم Aspose.Imaging for Java؟**  
ج3: يمكنك طلب المساعدة من مجتمع Aspose.Imaging والخبراء على [Aspose.Imaging Forum](https://forum.aspose.com/).

**س4: ما هي بعض تقنيات تحسين الصور الأخرى؟**  
ج4: بالإضافة إلى مرشح Median، تشمل تقنيات تحسين الصور الترشيح Wiener، التمويه Gaussian، وتمديد التباين، وغيرها.

**س5: هل يمكنني استخدام Aspose.Imaging for Java في تطبيق الويب الخاص بي؟**  
ج5: نعم، يمكنك دمج Aspose.Imaging for Java في تطبيقات الويب الخاصة بك لمعالجة الصور على الخادم.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-01-17  
**تم الاختبار مع:** Aspose.Imaging for Java 24.11  
**المؤلف:** Aspose