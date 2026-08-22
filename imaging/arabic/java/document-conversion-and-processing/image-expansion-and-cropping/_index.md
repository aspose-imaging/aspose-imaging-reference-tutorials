---
date: 2026-05-24
description: اكتشف كيفية استخدام مكتبة معالجة الصور Java، Aspose.Imaging for Java،
  لتوسيع الصور، قصها، وحفظ النتائج بكفاءة.
keywords:
- image manipulation library java
- how to crop image java
- how to expand image java
- aspose imaging expand image
linktitle: توسيع الصور وقصها
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Discover how to use the image manipulation library java, Aspose.Imaging
    for Java, to expand images, crop them, and save results efficiently.
  headline: Image Manipulation Library Java – Expand and Crop Images Using Aspose.Imaging
  type: TechArticle
- questions:
  - answer: Yes, it supports PNG, BMP, TIFF, GIF, and many more image types.
    question: Can Aspose.Imaging handle other formats besides JPEG?
  - answer: You can use `Resize` methods provided by the library; this falls under
      **resize image java** operations.
    question: Is there a way to resize the image before cropping?
  - answer: Absolutely. Loop through a collection of file paths and apply the same
      steps to each image.
    question: Does the library support batch processing of multiple images?
  - answer: '`cacheData()` loads the image into memory once, avoiding repeated disk
      reads during manipulation – this is the essence of **cache image java**.'
    question: How does caching improve performance?
  - answer: Refer to the official documentation **[documentation](https://reference.aspose.com/imaging/java/)**
      for a complete list of classes and methods.
    question: Where can I find more detailed API references?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: مكتبة معالجة الصور Java – توسيع وقص الصور باستخدام Aspose.Imaging
url: /ar/java/document-conversion-and-processing/image-expansion-and-cropping/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# مكتبة معالجة الصور Java – توسيع وقص الصور باستخدام Aspose.Imaging

معالجة الصور هي حاجة يومية لمطوري الويب والمصممين وأي شخص يعمل مع الوسائط الرقمية. في هذا الدرس ستتعلم **كيفية توسيع الصورة** ثم قصها بكفاءة باستخدام Aspose.Imaging for Java، وهي **مكتبة معالجة الصور java** رائدة. سنستعرض سير العمل الكامل — من تحميل الصورة المصدر إلى تخزين البيانات مؤقتًا، وتعريف مستطيل القص، وأخيرًا حفظ النتيجة المقصوصة.

## إجابات سريعة
- **ماذا يعني “توسيع الصورة”؟** يضيف مساحة قماشية إضافية حول الصورة الأصلية، مما يتيح لك قص مساحة أكبر.  
- **أي مكتبة يجب أن أستخدمها؟** توفر Aspose.Imaging for Java واجهة برمجة تطبيقات غنية لتوسيع الصورة، القص، والعديد من العمليات الأخرى.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تعمل للتطوير؛ يتطلب الاستخدام في الإنتاج ترخيصًا تجاريًا.  
- **هل يمكنني تخزين الصورة مؤقتًا لتحسين الأداء؟** نعم – استدعِ `cacheData()` على صورة الـ raster.  
- **هل صيغة الإخراج محدودة؟** لا، يمكنك الحفظ إلى JPEG، PNG، BMP، وغيرها من الصيغ التي تدعمها Aspose.Imaging.

## ما هو توسيع الصورة والقص في Java؟

يضيف توسيع الصورة بكسلات إضافية حول صورة موجودة، بينما يقتطع القص منطقة مستطيلة محددة. معًا يتيحان لك إعادة تأطير الصورة دون فقدان الجودة، وهو مطلب شائع لإنشاء الصور المصغرة، أصول واجهة المستخدم، أو إعداد الرسومات للطباعة.

## لماذا نستخدم Aspose.Imaging لهذه المهمة؟

توفر Aspose.Imaging حلاً عالي الأداء، **غير معتمد على الصيغة** يمكنه التعامل مع أكثر من 30 صيغة صورة ومعالجة ملفات تصل إلى 500 ميغابايت دون تحميل المستند بالكامل في الذاكرة. يقلل التخزين المؤقت المدمج من عبء الإدخال/الإخراج بنسبة تصل إلى 70 ٪، وتحتاج الواجهة البرمجية إلى عدد قليل من الأسطر فقط لتنفيذ التحويلات المعقدة، مما يجعلها مثالية لكل من السكريبتات السريعة والخدمات على نطاق واسع.

## المتطلبات المسبقة
- بيئة تطوير Java (JDK 8+)
- Aspose.Imaging for Java – قم بتنزيله **[هنا](https://releases.aspose.com/imaging/java/)**  
- بيئة تطوير متكاملة مثل Eclipse أو IntelliJ IDEA
- ملف صورة للعمل معه (مثال: `aspose-logo.jpg`)

الآن بعد أن تم إعدادك، دعنا نغوص في الكود الفعلي.

## استيراد الحزم
أولاً، استورد الفئات التي ستحتاجها. هذه الاستيرادات تمنحك الوصول إلى تحميل الصور، تعريف المستطيل، خيارات JPEG، ومعالجة صور الـ raster.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.JpegOptions;
import com.aspose.imaging.raster.RasterImage;
```

## الخطوة 1: تحميل الصورة
`RasterImage` هي فئة Aspose.Imaging التي تمثل صورة raster محملة في الذاكرة. حمّل الصورة المصدر في كائن `RasterImage`. استبدل مسار العنصر النائب بموقع ملف الصورة الخاص بك.

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
`Rectangle` يحدد إحداثيات X/Y وحجم المنطقة التي تريد الاحتفاظ بها بعد التوسيع. أنشئ `Rectangle` يحدد المنطقة التي تريد الاحتفاظ بها بعد التوسيع. تُقاس الإحداثيات من الزاوية العلوية اليسرى للوحة القماشية الموسعة.

```java
Rectangle destRect = new Rectangle(200, 200, 300, 300);
```

> **نصيحة احترافية:** اضبط قيم X و Y والعرض والارتفاع لتطابق المنطقة الدقيقة التي تحتاجها. هنا تتألق قدرة **aspose crop image**.

## الخطوة 4: حفظ الصورة المقصوصة
`JpegOptions` يتيح لك التحكم في جودة الإخراج، الضغط، وإعدادات JPEG الأخرى. أخيرًا، اكتب الجزء المقصوص إلى ملف جديد. طريقة `save` تسمح لك أيضًا بتحديد خيارات الإخراج مثل جودة JPEG.

```java
rasterImage.save("Your Document Directory" + "ExpandandCropImages_out.jpg", new JpegOptions(), destRect);
```

الملف `ExpandandCropImages_out.jpg` الآن يحتوي على اللوحة القماشية الموسعة مع المنطقة المختارة بحجم 300 × 300 بكسل المحفوظة كـ JPEG — مما يحقق متطلب **save cropped image**.

## كيف يتم توسيع الصورة في Java باستخدام Aspose.Imaging؟

حمّل صورتك الأصلية، استدعِ `rasterImage.expandCanvas(newWidth, newHeight, backgroundColor)`، ثم تابع عملية القص. **`expandCanvas` يضيف مساحة قماشية إضافية حول الصورة.** هذه الطريقة الواحدة تضيف مساحة القماش المطلوبة في عملية واحدة، مع الحفاظ على بيانات البكسل الأصلية وتمكينك من استهداف مستطيل قص أكبر دون تشويه.

## كيف يتم قص الصورة في Java باستخدام Aspose.Imaging؟

أنشئ `Rectangle` يصف المنطقة المستهدفة، ثم استدعِ `rasterImage.crop(rectangle)`. **`crop` يقتطع المنطقة المستطيلة المحددة من الصورة.** استدعاء القص يقتطع المنطقة المحددة من اللوحة القماشية الموسعة ويعيد كائن `RasterImage` جديد جاهز للحفظ. يضمن هذا النهج نتائج دقيقة على مستوى البكسل ويعمل عبر جميع الصيغ المدعومة.

## المشكلات الشائعة والحلول
| المشكلة | السبب | الحل |
|-------|--------|-----|
| `OutOfMemoryError` | صورة مصدر كبيرة بدون تخزين مؤقت | استدعِ `rasterImage.cacheData()` قبل المعالجة |
| المنطقة المقصوصة غير مركزة | إحداثيات المستطيل غير صحيحة | تحقق من إزاحات X/Y والأبعاد بالنسبة للوحة القماشية الموسعة |
| ملف الإخراج تالف | إعدادات `JpegOptions` غير صحيحة | استخدم الإعدادات الافتراضية أو اضبط `Quality = 90` |

## الأسئلة المتكررة

**س: هل يمكن لـ Aspose.Imaging التعامل مع صيغ أخرى غير JPEG؟**  
ج: نعم، يدعم PNG، BMP، TIFF، GIF، والعديد من أنواع الصور الأخرى.

**س: هل هناك طريقة لتغيير حجم الصورة قبل القص؟**  
ج: يمكنك استخدام طرق `Resize` التي توفرها المكتبة؛ وهذا يندرج تحت عمليات **resize image java**.

**س: هل تدعم المكتبة المعالجة الدفعية لعدة صور؟**  
ج: بالطبع. قم بالتكرار عبر مجموعة من مسارات الملفات وطبق نفس الخطوات على كل صورة.

**س: كيف يحسن التخزين المؤقت الأداء؟**  
ج: `cacheData()` يحمل الصورة في الذاكرة مرة واحدة، مما يجنب قراءات القرص المتكررة أثناء المعالجة – هذا هو جوهر **cache image java**.

**س: أين يمكنني العثور على مراجع API أكثر تفصيلاً؟**  
ج: ارجع إلى الوثائق الرسمية **[documentation](https://reference.aspose.com/imaging/java/)** للحصول على قائمة كاملة...

## الخلاصة
لديك الآن مثال كامل وجاهز للإنتاج حول **كيفية توسيع الصورة** وقصها باستخدام Aspose.Imaging for Java. من خلال الاستفادة من التخزين المؤقت، تعريف المستطيلات بدقة، وخيارات الحفظ المرنة، يمكنك دمج سير العمل هذا في أي خط أنابيب لمعالجة الصور مبني على Java.

استكشف المزيد بتجربة تحويلات أخرى مثل الدوران، إضافة العلامات المائية، أو إعادة الحجم الدفعي. للحصول على إرشادات إضافية، راجع **[documentation](https://reference.aspose.com/imaging/java/)** أو انضم إلى المجتمع في **[Aspose support forum](https://forum.aspose.com/)**.

---

**آخر تحديث:** 2026-05-24  
**تم الاختبار مع:** Aspose.Imaging for Java 24.11  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [معالجة الصور Java باستخدام Aspose.Imaging: التحميل، التخزين المؤقت، والقص](/imaging/java/getting-started/java-image-processing-aspose-imaging-load-cache-crop/)
- [إتقان معالجة الصور باستخدام Aspose.Imaging for Java: التحميل، الحفظ وإزالة الخلفيات](/imaging/java/image-transformations/aspose-imaging-java-master-image-processing/)
- [معالجة الصور المتوازية في Java باستخدام Aspose.Imaging: تعدد الخيوط والمعالجة الدفعية](/imaging/java/batch-processing-multi-threading/parallel-image-processing-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}