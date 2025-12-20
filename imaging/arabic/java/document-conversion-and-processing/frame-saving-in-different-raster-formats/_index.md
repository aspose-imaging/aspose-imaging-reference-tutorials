---
date: 2025-12-20
description: تعلم كيفية تحويل ملفات TIFF إلى PNG وحفظ الصورة بصيغة PNG أو BMP أو GIF
  باستخدام Aspose.Imaging للغة Java. دليل خطوة بخطوة لتعديل الصور.
linktitle: Frame Saving in Different Raster Formats
second_title: Aspose.Imaging Java Image Processing API
title: كيفية تحويل TIFF إلى PNG وحفظ الإطارات بصيغ نقطية مختلفة
url: /ar/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# تحويل TIFF إلى PNG وحفظ الإطارات بتنسيقات نقطية مختلفة

العمل مع ملفات TIFF متعددة الصفحات هو سيناريو شائع في التطبيقات التي تتعامل مع المستندات بكثرة. إذا كنت بحاجة إلى **تحويل tiff إلى png** — أو استخراج الإطارات الفردية وتخزينها بتنسيقات نقطية أخرى — فإن Aspose.Imaging for Java يجعل العملية مباشرة وعالية الأداء. في هذا البرنامج التعليمي سنستعرض الخطوات الدقيقة لتحميل ملف TIFF، التكرار عبر إطاراته، وحفظ كل إطار كـ PNG (يمكنك بسهولة التحويل إلى BMP أو GIF لاحقًا).

## إجابات سريعة
- **ماذا يعني “convert tiff to png”؟** يعني استخراج كل صفحة من ملف TIFF وكتابتها كصورة نقطية PNG.  
- **أي مكتبة تتعامل مع هذا؟** Aspose.Imaging for Java توفر دعمًا كاملاً لاستخراج إطارات TIFF وتحويل تنسيقات النقطية.  
- **هل أحتاج إلى ترخيص؟** الإصدار التجريبي المجاني يكفي للتطوير؛ الترخيص الكامل مطلوب للاستخدام في الإنتاج.  
- **هل يمكنني الحفظ إلى BMP أو GIF بدلاً من PNG؟** نعم — فقط استبدل `PngOptions` بـ `BmpOptions` أو `GifOptions`.  
- **ما نسخة Java المطلوبة؟** يوصى بـ Java 8 أو أعلى.

## ما هو “convert tiff to png”؟
تحويل TIFF إلى PNG يتضمن فك ترميز TIFF متعدد الصفحات، الوصول إلى كل إطار، وترميز ذلك الإطار إلى تنسيق PNG، وهو تنسيق غير مضغوط، صديق للويب، ومدعوم على نطاق واسع.

## لماذا نستخدم Aspose.Imaging for Java؟
- **دعم واسع للتنسيقات** – يدعم TIFF، PNG، JPEG، BMP، GIF، والعديد غيرها.  
- **بدون تبعيات أصلية** – جافا صافية، سهل التكامل مع أي مشروع JVM.  
- **أداء عالي** – مُحسّن للصور الكبيرة والوثائق متعددة الصفحات.  
- **واجهة برمجة تطبيقات بسيطة** – القليل من الشيفرة المطلوبة لأداء التحويلات المعقدة.

## المتطلبات المسبقة

1. **بيئة تطوير Java** – تأكد من تثبيت JDK. حمّله من [موقع Oracle](https://www.oracle.com/java/technologies/javase-downloads) إذا لم تكن قد فعلت ذلك بالفعل.  
2. **مكتبة Aspose.Imaging for Java** – اطلع على مرجع API في [التوثيق](https://reference.aspose.com/imaging/java/). احصل على المكتبة من [صفحة التحميل](https://releases.aspose.com/imaging/java/). نسخة تجريبية مجانية متاحة [هنا](https://releases.aspose.com/)، ويمكن شراء ترخيص كامل [هنا](https://purchase.aspose.com/buy).  
3. **صورة TIFF تجريبية** – احرص على وجود ملف TIFF متعدد الصفحات جاهز للمعالجة.

الآن بعد تغطية المتطلبات المسبقة، دعنا ننتقل إلى الشيفرة.

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
حدد مسار دليل البيانات وحمّل ملف TIFF المصدر.

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

### الخطوة 2: حفظ الإطارات بتنسيقات نقطية مختلفة
قم بالتكرار على كل إطار و**احفظ الصورة كـ png**. لتحويل **tiff إلى bmp** أو إجراء **تحويل tiff إلى gif**، استبدل ببساطة `PngOptions` بـ `BmpOptions` أو `GifOptions`.

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **نصيحة محترف:** احتفظ بكتلة `try‑with‑resources` كما هو موضح لضمان التخلص الصحيح من ملف TIFF بعد المعالجة.

## حالات الاستخدام الشائعة
- **أرشفة المستندات:** تحويل مستندات TIFF الممسوحة ضوئيًا إلى PNG للمعاينة على الويب.  
- **إنشاء الصور المصغرة:** استخراج الإطار الأول من TIFF وحفظه كصورة PNG صغيرة.  
- **ترحيل التنسيقات:** نقل أصول TIFF القديمة إلى تنسيقات حديثة مثل BMP أو GIF لتوافق أفضل مع الأنظمة القديمة.

## استكشاف الأخطاء وإصلاحها & نصائح
- **الإطارات المفقودة:** تأكد من أن ملف TIFF المصدر يحتوي فعلاً على صفحات متعددة؛ استخدم `multiImage.getFrames().size()` للتصحيح.  
- **أخطاء الذاكرة:** عالج ملفات TIFF الكبيرة صفحةً بصفحة كما هو موضح بدلاً من تحميل الملف بالكامل في الذاكرة.  
- **مراقبة الجودة:** PNG غير مضغوط؛ إذا كنت تحتاج إلى ملفات أصغر، ففكّر في استخدام خيارات JPEG مع إعدادات الجودة.

## الأسئلة المتكررة

**س1: ما هي تنسيقات النقطية المدعومة لحفظ الإطارات في Aspose.Imaging for Java؟**  
ج1: تدعم Aspose.Imaging for Java مجموعة واسعة من التنسيقات النقطية، بما في ذلك PNG، JPEG، BMP، GIF، وأكثر. يمكنك اختيار التنسيق الأنسب لاحتياجات تطبيقك.

**س2: هل يمكنني إجراء عمليات صور أخرى باستخدام Aspose.Imaging for Java؟**  
ج2: نعم، تقدم Aspose.Imaging for Java مجموعة شاملة من الميزات لمعالجة الصور، بما في ذلك تغيير الحجم، القص، وتطبيق فلاتر وتأثيرات مختلفة. إنها أداة متعددة الاستخدامات لجميع متطلبات معالجة الصور الخاصة بك.

**س3: كيف يمكنني الحصول على ترخيص كامل لـ Aspose.Imaging for Java؟**  
ج: لشراء ترخيص كامل لـ Aspose.Imaging for Java، زر [صفحة الشراء](https://purchase.aspose.com/buy). ستجد خيارات ترخيص متعددة تناسب مشروعك.

**س4: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Imaging for Java؟**  
ج: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية من Aspose.Imaging for Java عبر [صفحة الإصدارات](https://releases.aspose.com/). تتيح لك هذه النسخة استكشاف قدرات المكتبة قبل اتخاذ قرار الشراء.

**س5: أين يمكنني طلب الدعم أو المساعدة بخصوص Aspose.Imaging for Java؟**  
ج: لأي أسئلة أو مشكلات أو للحصول على مساعدة بخصوص Aspose.Imaging for Java، يمكنك زيارة [منتدى Aspose Imaging](https://forum.aspose.com/). المجتمع وفريق الدعم موجودان لمساعدتك.

---

**آخر تحديث:** 2025-12-20  
**تم الاختبار مع:** Aspose.Imaging for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}