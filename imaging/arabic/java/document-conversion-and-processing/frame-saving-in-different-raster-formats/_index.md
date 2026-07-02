---
date: 2026-04-28
description: تعلم كيفية تحويل ملفات TIFF إلى PNG وكيفية تحويل ملفات TIFF إلى صيغ نقطية
  أخرى باستخدام Aspose.Imaging للغة Java. دليل خطوة بخطوة لمعالجة الصور.
keywords:
- tiff to png java
- how to convert tiff
- Aspose.Imaging Java
linktitle: حفظ الإطار في صيغ نقطية مختلفة
second_title: Aspose.Imaging Java Image Processing API
title: tiff إلى png java – تحويل TIFF إلى PNG وحفظ الإطارات بصيغ نقطية مختلفة
url: /ar/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# tiff to png java – تحويل TIFF إلى PNG وحفظ الإطارات بصيغ نقطية مختلفة

العمل مع ملفات TIFF متعددة الصفحات هو سيناريو شائع في التطبيقات التي تتعامل مع مستندات كثيرة. إذا كنت بحاجة إلى **convert tiff to png**—أو استخراج الإطارات الفردية وتخزينها بصيغ نقطية أخرى—Aspose.Imaging for Java يجعل العملية بسيطة وعالية الأداء. في هذا الدرس سنستعرض الخطوات الدقيقة لتحميل ملف TIFF، والتكرار عبر إطاراته، وحفظ كل إطار كـ PNG (يمكنك بسهولة التحويل إلى BMP أو GIF لاحقًا). في النهاية ستتعرف أيضًا على **how to convert tiff** إلى أي من الصيغ النقطية المدعومة ببضع أسطر من الشيفرة.

## إجابات سريعة
- **What does “convert tiff to png” mean?** يعني استخراج كل صفحة من ملف TIFF وكتابتها كصورة نقطية PNG.  
- **Which library handles this?** Aspose.Imaging for Java يوفر دعمًا كاملاً لاستخراج إطارات TIFF وتحويل صيغ النقطية.  
- **Do I need a license?** الإصدار التجريبي المجاني يعمل للتطوير؛ يتطلب الاستخدام في الإنتاج رخصة كاملة.  
- **Can I save to BMP or GIF instead of PNG?** نعم—فقط استبدل `PngOptions` بـ `BmpOptions` أو `GifOptions`.  
- **What Java version is required?** يوصى باستخدام Java 8 أو أعلى.

## ما هو “convert tiff to png”؟
تحويل TIFF إلى PNG يتضمن فك ترميز TIFF متعدد الصفحات، الوصول إلى كل إطار، وترميز ذلك الإطار إلى صيغة PNG، وهي صيغة غير مضغوطة، صديقة للويب، ومدعومة على نطاق واسع.

## لماذا نستخدم Aspose.Imaging for Java؟
- **Broad format support** – يدعم TIFF، PNG، JPEG، BMP، GIF، والعديد غيرها.  
- **No native dependencies** – جافا خالص، سهل الدمج في أي مشروع JVM.  
- **High performance** – مُحسّن للصور الكبيرة والمستندات متعددة الصفحات.  
- **Simple API** – يتطلب أقل قدر من الشيفرة لأداء التحويلات المعقدة.

## لماذا هذا مهم
العديد من الأنظمة القديمة تخزن المستندات الممسوحة ضوئيًا كملفات TIFF متعددة الصفحات لأن الصيغة صديقة للأرشفة. ومع ذلك، تفضّل التطبيقات الحديثة على الويب والهواتف المحمولة PNG أو BMP أو GIF لتقديم سريع وإنشاء صور مصغرة. تحويل إطارات TIFF أثناء التشغيل يقلل من تكاليف التخزين، ويحسن أوقات التحميل، ويوسّع التوافق عبر المتصفحات والأجهزة.

## المتطلبات المسبقة

1. **Java Development Environment** – تأكد من تثبيت JDK. قم بتحميله من [Oracle website](https://www.oracle.com/java/technologies/javase-downloads) إذا لم تقم بذلك بعد.  
2. **Aspose.Imaging for Java Library** – الوصول إلى مرجع API عبر [documentation](https://reference.aspose.com/imaging/java/). احصل على المكتبة من [download page](https://releases.aspose.com/imaging/java/). نسخة تجريبية مجانية متاحة [here](https://releases.aspose.com/)، ويمكن شراء رخصة كاملة [here](https://purchase.aspose.com/buy).  
3. **Sample TIFF Image** – احرص على وجود ملف TIFF متعدد الصفحات جاهز للمعالجة.

الآن بعد تغطية المتطلبات المسبقة، دعونا نغوص في الشيفرة.

## كيفية تحويل TIFF إلى PNG باستخدام Aspose.Imaging for Java

### استيراد الحزم
أولاً، استورد الفئات المطلوبة من Aspose.Imaging.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

### الخطوة 1: تحميل صورة TIFF
قم بتهيئة دليل البيانات وحمل ملف TIFF المصدر.

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

### الخطوة 2: حفظ الإطارات بصيغ نقطية مختلفة
تكرار عبر كل إطار و**save image as png**. لتحويل **convert tiff to bmp** أو إجراء **tiff to gif conversion**، استبدل ببساطة `PngOptions` بـ `BmpOptions` أو `GifOptions`.

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **نصيحة احترافية:** احتفظ بكتلة `try‑with‑resources` كما هو موضح لضمان التخلص الصحيح من ملف TIFF بعد المعالجة.

## حالات الاستخدام الشائعة
- **Document archiving:** تحويل مستندات TIFF الممسوحة إلى PNG للمعاينة على الويب.  
- **Thumbnail generation:** استخراج الإطار الأول من TIFF وحفظه كصورة مصغرة PNG صغيرة.  
- **Format migration:** نقل أصول TIFF القديمة إلى صيغ حديثة مثل BMP أو GIF للتوافق مع الأنظمة القديمة.

## استكشاف الأخطاء وإصلاحها & نصائح
- **Missing frames:** تحقق من أن ملف TIFF المصدر يحتوي فعليًا على صفحات متعددة؛ استخدم `multiImage.getFrames().size()` للتصحيح.  
- **Out‑of‑memory errors:** عالج ملفات TIFF الكبيرة صفحة بصفحة كما هو موضح بدلاً من تحميل الملف بالكامل في الذاكرة.  
- **Quality control:** PNG غير مضغوط؛ إذا كنت بحاجة إلى ملفات أصغر، فكر في استخدام خيارات JPEG مع إعدادات الجودة.

## الأسئلة المتكررة

**Q1: ما هي صيغ النقطية المدعومة لحفظ الإطارات في Aspose.Imaging for Java؟**  
A1: Aspose.Imaging for Java يدعم مجموعة واسعة من صيغ النقطية، بما في ذلك PNG، JPEG، BMP، GIF، وأكثر. يمكنك اختيار الصيغة التي تناسب احتياجات تطبيقك.

**Q2: هل يمكنني إجراء عمليات صور أخرى باستخدام Aspose.Imaging for Java؟**  
A2: نعم، Aspose.Imaging for Java يقدم مجموعة شاملة من الميزات لمعالجة الصور، بما في ذلك تغيير الحجم، القص، وتطبيق فلاتر وتأثيرات مختلفة. إنه أداة متعددة الاستخدامات لجميع متطلبات معالجة الصور.

**Q3: كيف يمكنني الحصول على رخصة كاملة لـ Aspose.Imaging for Java؟**  
A: لشراء رخصة كاملة لـ Aspose.Imaging for Java، زر [purchase page](https://purchase.aspose.com/buy). ستجد خيارات ترخيص مختلفة تناسب مشروعك.

**Q4: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Imaging for Java؟**  
A: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية من Aspose.Imaging for Java عبر [releases page](https://releases.aspose.com/). تتيح لك هذه التجربة استكشاف قدرات المكتبة قبل الشراء.

**Q5: أين يمكنني طلب الدعم أو المساعدة بخصوص Aspose.Imaging for Java؟**  
A: لأي أسئلة أو مشكلات أو مساعدة بخصوص Aspose.Imaging for Java، يمكنك زيارة [Aspose Imaging forum](https://forum.aspose.com/). المجتمع وفريق الدعم موجودان لمساعدتك.

---

**آخر تحديث:** 2026-04-28  
**تم الاختبار مع:** Aspose.Imaging for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}