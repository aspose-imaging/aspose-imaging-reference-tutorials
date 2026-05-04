---
date: 2025-12-24
description: تعلم كيفية توسيع الصورة وإجراء قص الصورة باستخدام Aspose.Imaging للغة
  جافا. اتبع هذا الدليل خطوة بخطوة لتوسيع الصورة، قصها، وحفظها.
linktitle: Image Expansion and Cropping
second_title: Aspose.Imaging Java Image Processing API
title: كيفية توسيع الصورة وقصها باستخدام Aspose.Imaging Java
url: /ar/java/document-conversion-and-processing/image-expansion-and-cropping/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# كيفية توسيع الصورة وقصها باستخدام Aspose.Imaging Java

معالجة الصور هي حاجة يومية لمطوري الويب والمصممين وأي شخص يعمل مع الوسائط الرقمية. في هذا الدرس ستتعلم **كيفية توسيع الصورة** ثم قصها بكفاءة باستخدام Aspose.Imaging للغة Java. سنستعرض سير العمل الكامل — من تحميل الصورة المصدر إلى تخزين البيانات مؤقتًا، وتحديد مستطيل القص، وأخيرًا حفظ النتيجة المقتصة.

## إجابات سريعة
- **ماذا يعني “expand image”?** يضيف مساحة قماش إضافية حول الصورة الأصلية، مما يسمح لك بقص منطقة أكبر.
- **أي مكتبة يجب أن أستخدمها؟** توفر Aspose.Imaging للغة Java واجهة برمجة تطبيقات غنية لتوسيع الصور، والقص، والعديد من العمليات الأخرى.
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تعمل للتطوير؛ يلزم ترخيص تجاري للاستخدام في الإنتاج.
- **هل يمكنني تخزين الصورة مؤقتًا لتحسين الأداء؟** نعم – استدعِ `cacheData()` على صورة الـ raster.
- **هل صيغة الإخراج محدودة؟** لا، يمكنك الحفظ إلى JPEG، PNG، BMP، وغيرها من الصيغ التي تدعمها Aspose.Imaging.

## ما هو توسيع الصورة والقص في Java؟
يضيف توسيع الصورة بكسلات إضافية حول صورة موجودة، بينما يقتطع القص منطقة مستطيلة محددة. معًا يتيحان لك إعادة تأطير الصورة دون فقدان الجودة، وهو مطلب شائع لإنشاء الصور المصغرة، وأصول واجهة المستخدم، أو إعداد الرسومات للطباعة.

## لماذا نستخدم Aspose.Imaging لهذه المهمة؟
- **واجهة برمجة تطبيقات عالية الأداء** – التخزين المؤقت المدمج (`cacheData`) يقلل من عبء الإدخال/الإخراج.
- **غير معتمد على الصيغة** – يعمل مع JPEG، PNG، BMP، TIFF، وأكثر.
- **كود بسيط** – بضع أسطر تستبدل كود معالجة الصور الأصلي المعقد.
- **جاهز للمؤسسات** – موثوق به لكل من السكريبتات البسيطة والخدمات واسعة النطاق.

## المتطلبات المسبقة
- بيئة تطوير Java (JDK 8+)
- Aspose.Imaging للغة Java – قم بتنزيله **[هنا](https://releases.aspose.com/imaging/java/)**  
- بيئة تطوير متكاملة مثل Eclipse أو IntelliJ IDEA
- ملف صورة للعمل معه (مثال: `aspose-logo.jpg`)

الآن بعد أن تم إعدادك، دعنا نغوص في الكود الفعلي.

## استيراد الحزم
أولاً، استورد الفئات التي ستحتاجها. هذه الاستيرادات تمنحك الوصول إلى تحميل الصور، تعريف المستطيل، خيارات JPEG، ومعالجة صور raster.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.JpegOptions;
import com.aspose.imaging.raster.RasterImage;
```

## الخطوة 1: تحميل الصورة
حمّل الصورة المصدر في كائن `RasterImage`. استبدل مسار العنصر النائب بموقع ملف الصورة الخاص بك.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
{
    // Your code here
}
```

## الخطوة 2: تخزين بيانات الصورة مؤقتًا
التخزين المؤقت يسرّع العمليات اللاحقة، خاصةً عندما تقرأ بيانات البكسل عدة مرات.

```java
rasterImage.cacheData();
```

## الخطوة 3: تعريف مستطيل القص
أنشئ كائن `Rectangle` يحدد المنطقة التي تريد الاحتفاظ بها بعد التوسيع. تُقاس الإحداثيات من الزاوية العلوية اليسرى للقماش الموسع.

```java
Rectangle destRect = new Rectangle(200, 200, 300, 300);
```

> **نصيحة احترافية:** اضبط قيم X وY والعرض والارتفاع لتطابق المنطقة الدقيقة التي تحتاجها. هنا تتألق قدرة **aspose crop image**.

## الخطوة 4: حفظ الصورة المقتصة
أخيرًا، احفظ الجزء المقتص إلى ملف جديد. تتيح لك طريقة `save` أيضًا تحديد خيارات الإخراج مثل جودة JPEG.

```java
rasterImage.save("Your Document Directory" + "ExpandandCropImages_out.jpg", new JpegOptions(), destRect);
```

الملف `ExpandandCropImages_out.jpg` الآن يحتوي على القماش الموسع مع المنطقة المختارة 300 × 300 بكسل المحفوظة كـ JPEG — مما يحقق متطلب **save cropped image**.

## المشكلات الشائعة والحلول
| Issue | Reason | Fix |
|-------|--------|-----|
| `OutOfMemoryError` | صورة مصدر كبيرة بدون تخزين مؤقت | استدعِ `rasterImage.cacheData()` قبل المعالجة |
| Cropped area is off‑center | إحداثيات المستطيل خاطئة | تحقق من إزاحات X/Y والأبعاد بالنسبة للقماش الموسع |
| Output file is corrupted | إعدادات `JpegOptions` غير صحيحة | استخدم الخيارات الافتراضية أو عيّن `Quality = 90` |

## الأسئلة المتكررة

**س: هل يمكن لـ Aspose.Imaging التعامل مع صيغ أخرى غير JPEG؟**  
ج: نعم، يدعم PNG، BMP، TIFF، GIF، والعديد من أنواع الصور الأخرى.

**س: هل هناك طريقة لتغيير حجم الصورة قبل القص؟**  
ج: يمكنك استخدام طرق `Resize` التي توفرها المكتبة؛ وهذا يندرج تحت عمليات **resize image java**.

**س: هل تدعم المكتبة المعالجة الدفعية لعدة صور؟**  
ج: بالتأكيد. قم بالتكرار عبر مجموعة من مسارات الملفات وطبق نفس الخطوات على كل صورة.

**س: كيف يحسن التخزين المؤقت الأداء؟**  
ج: تقوم `cacheData()` بتحميل الصورة إلى الذاكرة مرة واحدة، مما يجنب قراءات القرص المتكررة أثناء المعالجة – وهذا هو جوهر **cache image java**.

**س: أين يمكنني العثور على مراجع API أكثر تفصيلًا؟**  
ج: راجع الوثائق الرسمية **[documentation](https://reference.aspose.com/imaging/java/)** للحصول على قائمة كاملة بالفئات والطرق.

## الخلاصة
أصبحت الآن تملك مثالًا كاملاً وجاهزًا للإنتاج حول **كيفية توسيع الصورة** وقصها باستخدام Aspose.Imaging للغة Java. من خلال الاستفادة من التخزين المؤقت، وتعريف المستطيلات بدقة، وخيارات الحفظ المرنة، يمكنك دمج سير العمل هذا في أي خط أنابيب لمعالجة الصور مبني على Java.

استكشف المزيد بتجربة تحويلات أخرى مثل الدوران، إضافة العلامات المائية، أو تغيير الحجم الدفعي. للحصول على إرشادات إضافية، راجع **[documentation](https://reference.aspose.com/imaging/java/)** أو انضم إلى المجتمع في **[Aspose support forum](https://forum.aspose.com/)**.

---

**آخر تحديث:** 2025-12-24  
**تم الاختبار مع:** Aspose.Imaging for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}