---
date: '2026-11-17'
description: تعرف على كيفية إنشاء ملفات TIFF باستخدام Aspose.Imaging for Java. يغطي
  هذا الدليل تحويل الصور إلى TIFF، وإنشاء ملفات TIFF متعددة الصفحات، ونصائح الأداء.
keywords:
- how to create tiff
- convert images to tiff
- java image conversion
- load and resize image
- aspose imaging java
lastmod: '2026-11-17'
og_description: تعرف على كيفية إنشاء صور TIFF باستخدام Aspose.Imaging for Java. يشرح
  هذا الدليل خطوات تحميل الصور، وتغيير حجمها، وتجميع إطارات متعددة في ملف TIFF متعدد
  الصفحات، بالإضافة إلى نصائح الأداء وتفاصيل الترخيص.
og_image_alt: 'Tutorial illustration: creating a multi-page TIFF with Aspose.Imaging
  for Java'
og_title: كيفية إنشاء TIFF متعددة الصفحات باستخدام Aspose.Imaging for Java
schemas:
- author: Aspose
  dateModified: '2026-11-17'
  description: Learn how to create tiff with Aspose.Imaging for Java. This guide covers
    converting images to tiff, building multi-page TIFFs, and performance tips.
  headline: How to create multi-page tiff image using Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create tiff with Aspose.Imaging for Java. This guide covers
    converting images to tiff, building multi-page TIFFs, and performance tips.
  name: How to create multi-page tiff image using Aspose.Imaging for Java
  steps:
  - name: load an image
    text: '- **Explanation:** The `load` method reads the image from the specified
      directory. Ensure your path is correct to avoid file‑not‑found errors.'
  - name: resize the image
    text: '- **Explanation:** Resizing with `ResizeType.NearestNeighbourResample`
      maintains pixel data without interpolation, preserving image quality in certain
      scenarios.'
  - name: set up TIFF options
    text: '- **Explanation:** `TiffOptions` configure how the TIFF file is created.
      The source parameter points to where your multi‑page TIFF will be saved.'
  - name: initialize the TIFF image
    text: '- **Explanation:** The `create` method initializes a new multi‑page TIFF
      with dimensions derived from our resized image.'
  - name: load additional images
    text: '- **Explanation:** This block iterates over files in the directory ending
      with `.img`, adding each as a new frame to the TIFF image. The `savePixels`
      method ensures that pixel data from each loaded image is accurately transferred.'
  - name: save your work
    text: '- **Explanation:** The `save` method writes the complete multi‑page TIFF
      image to your specified output directory. Ensure that this path is accessible
      and writable.'
  type: HowTo
- questions:
  - answer: Absolutely. Load any supported raster format (PNG, JPEG, BMP, etc.) and
      add each as a frame using the same workflow.
    question: Can I convert PNG or JPEG files to a multi‑page TIFF with this approach?
  - answer: Yes. You can configure `tiffOptions.setCompression(TiffCompression.Lzw)`
      before creating the image.
    question: Is it possible to set compression (e.g., LZW) for the output TIFF?
  - answer: Use `frame.getMetadata().addProperty("Author", "Your Name")` after creating
      the frame and before saving.
    question: How do I add metadata (e.g., author, description) to each TIFF frame?
  - answer: It does. Use `Image.load("existing.tiff")` and iterate through `((TiffImage)image).getFrames()`.
    question: Does Aspose.Imaging support reading existing multi‑page TIFFs?
  - answer: Process pages in batches and periodically call `System.gc()` or use Java's
      `try-with-resources` pattern (as shown) to release memory promptly.
    question: What if I need to process thousands of pages?
  type: FAQPage
tags:
- tiff conversion
- Aspose.Imaging
- java image processing
- multi-page tiff
- image manipulation
title: كيفية إنشاء صورة TIFF متعددة الصفحات باستخدام Aspose.Imaging for Java
url: /ar/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء صورة TIFF متعددة الصفحات باستخدام Aspose.Imaging للغة Java

## مقدمة

في عالمنا الرقمي اليوم، **كيفية إنشاء tiff** بكفاءة مهمة للأرشفة، التصوير الطبي، ومشاريع إدارة المستندات. يوفر Aspose.Imaging للغة Java طريقة برمجية لدمج عدة صور نقطية—PNG، JPEG، BMP—في ملف TIFF متعدد الصفحات مع الحفاظ على استهلاك الذاكرة منخفضًا. يوضح هذا الدرس خطوة بخطوة كيفية التحميل، إعادة التحجيم، تكوين خيارات TIFF، إضافة الإطارات، وأخيرًا حفظ النتيجة. في النهاية، ستفهم لماذا يُعد Aspose.Imaging خيارًا موثوقًا لأنابيب الصور ذات الحجم الكبير.

**ما ستتعلمه**
- تحميل وإعادة تحجيم ملفات الصور باستخدام Aspose.Imaging.
- إنشاء خيارات TIFF وتكوين المصدر لإخراج متعدد الصفحات.
- إضافة إطارات من صور متعددة لبناء TIFF متعدد الصفحات.
- حفظ TIFF النهائي بكفاءة للاستخدام اللاحق.
- سيناريوهات واقعية حيث يكون تحويل الصور إلى tiff ذا قيمة.

## إجابات سريعة
- **ما هي المكتبة الأساسية؟** Aspose.Imaging للغة Java.
- **هل يمكنني تحويل الصور إلى tiff؟** نعم – يوضح الدرس كيفية دمج PNG و JPEG وغيرها في TIFF متعدد الصفحات.
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تكفي للتقييم؛ الترخيص الدائم مطلوب للإنتاج.
- **ما نسخة Java المطلوبة؟** Java 8 أو أعلى (JDK 8+).
- **هل الشيفرة آمنة للخطوط المتعددة؟** المثال يعمل على خيط واحد؛ للسيناريوهات المتزامنة، أدِر كائنات Image لكل خيط.

## ما هو Aspose.Imaging للغة Java؟

Aspose.Imaging للغة Java هو API شامل يدعم **أكثر من 100** تنسيق صورة ويوفر ميزات متقدمة مثل الضغط غير الفاقد، معالجة الإطارات المتعددة، والبث. يتيح للمطورين التعامل مع الصور دون الاعتماد على مكتبات أصلية، مما يجعله مثاليًا لبيئات الخوادم متعددة المنصات.

## لماذا تستخدم Aspose.Imaging لإنشاء TIFF متعدد الصفحات؟

يوفر Aspose.Imaging أداءً عاليًا، عمق ميزات واسع، وموثوقية مثبتة لإنشاء ملفات TIFF متعددة الصفحات. يمكنه معالجة ملفات تصل إلى 2 GB مع الحفاظ على استهلاك الذاكرة منخفضًا، يقدم أكثر من 50 خوارزمية ضغط، ويعمل باستمرار عبر Windows و macOS و Linux مع Java 8‑21.

- **الأداء:** يعالج ملفات تصل إلى 2 GB دون تحميل الصورة بالكامل إلى الذاكرة، مما يقلل ضغط الكومة بنسبة تصل إلى 70 % مقارنةً بالطرق البسيطة.
- **عمق المميزات:** يقدم أكثر من 50 خوارزمية ضغط (بما في ذلك LZW، Deflate، و JPEG) ويسمح بحقن بيانات تعريفية لكل إطار.
- **الموثوقية:** تم اختباره على Windows و macOS و Linux مع Java 8‑21، مما يضمن نتائج متسقة عبر المنصات.

## المتطلبات المسبقة

- **المكتبات المطلوبة:** Aspose.Imaging للغة Java (قم بالتنزيل من الموقع الرسمي).
- **بيئة التطوير:** JDK 8+ مثبت؛ يُنصح باستخدام IDE مثل IntelliJ IDEA أو Eclipse.
- **المعرفة الأساسية:** الإلمام بصياغة Java وعمليات إدخال/إخراج الملفات.

## إعداد Aspose.Imaging للغة Java

لبدء العمل مع Aspose.Imaging، دمجه في مشروعك باستخدام أداة البناء المفضلة.

**Maven:**  
أضف الاعتماد التالي إلى ملف `pom.xml` الخاص بك:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle:**  
أدرج هذا في ملف `build.gradle` الخاص بك:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

بدلاً من ذلك، يمكنك **تنزيل مباشرة** أحدث ملف JAR لـ Aspose.Imaging للغة Java من [Aspose releases](/imaging/java/).

### الحصول على الترخيص

يمكنك البدء بنسخة تجريبية مجانية لاستكشاف ميزات Aspose.Imaging. للاستخدام الممتد، فكر في الحصول على ترخيص مؤقت أو شراء ترخيص كامل:
- **نسخة تجريبية مجانية:** زر [Aspose Imaging Java Releases](/imaging/java/) لتنزيل وتجربة المكتبة.
- **ترخيص مؤقت:** احصل عليه من [Aspose Temporary License Page](/purchase/temporary-license/).
- **شراء:** للحصول على حل دائم، انتقل إلى [Aspose Purchase](/purchase/buy).

بعد دمج Aspose.Imaging في مشروعك وإعداد التراخيص اللازمة، أنت جاهز لبدء تنفيذ دليل إنشاء TIFF متعدد الصفحات.

## كيف تنشئ صورة TIFF متعددة الصفحات باستخدام Aspose.Imaging للغة Java؟

حمّل صور المصدر، قم بتكوين `TiffOptions`، أنشئ ملف TIFF فارغ متعدد الصفحات، أضف كل صورة معاد تحجيمها كإطار، وأخيرًا استدعِ `save`. يتطلب هذا التدفق من البداية إلى النهاية عددًا قليلًا من استدعاءات API ويعمل في أقل من ثانية للوثائق النموذجية ذات 5 صفحات على معالج حديث.

### تحميل وإعادة تحجيم صورة

**تعريف:** `Image.load` يقرأ ملف الصورة إلى الذاكرة، بينما `Resize` يغير أبعادها دون فقدان تنسيق البكسل الأصلي.

#### الخطوة 1: تحميل صورة
```java
import com.aspose.imaging.Image;

String dataDir = "YOUR_DOCUMENT_DIRECTORY";
Image tempImage = Image.load(dataDir + "/Image1.png");
```
- **شرح:** طريقة `load` تقرأ الصورة من الدليل المحدد. تأكد من صحة المسار لتجنب أخطاء عدم العثور على الملف.

#### الخطوة 2: إعادة تحجيم الصورة
```java
int width = tempImage.getWidth();
int height = tempImage.getHeight();
tempImage.resize(width, height, ResizeType.NearestNeighbourResample);
```
- **شرح:** إعادة التحجيم باستخدام `ResizeType.NearestNeighbourResample` تحافظ على بيانات البكسل دون استيفاء، مما يحافظ على جودة الصورة في بعض السيناريوهات.

### إنشاء خيارات TIFF والمصدر

**تعريف:** `TiffOptions` يحدد المعلمات لإنشاء ملف TIFF، مثل الضغط، تدفق المصدر، وأبعاد الصفحات.

#### الخطوة 1: إعداد خيارات TIFF
```java
import com.aspose.imaging.fileformats.tiff.TiffOptions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.sources.FileCreateSource;

TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setSource(new FileCreateSource("YOUR_DOCUMENT_DIRECTORY/MultiPage.tiff", false));
```
- **شرح:** `TiffOptions` يضبط طريقة إنشاء ملف TIFF. معلمة المصدر تشير إلى المكان الذي سيُحفظ فيه TIFF متعدد الصفحات.

### إنشاء وتهيئة صورة TIFF متعددة الصفحات

**تعريف:** `Image.create` يهيئ TIFF متعدد الصفحات جديد بالأبعاد والخيارات المحددة.

#### الخطوة 1: تهيئة صورة TIFF
```java
import com.aspose.imaging.fileformats.tiff.TiffImage;

TiffImage tiffImage = (TiffImage) Image.create(tiffOptions, width, height);
```
- **شرح:** طريقة `create` تهيئ TIFF متعدد الصفحات جديد بأبعاد مستمدة من صورتنا المعاد تحجيمها.

### معالجة صور متعددة وإضافة إطارات إلى TIFF

#### الخطوة 1: تحميل صور إضافية
```java
import java.io.File;
import java.io.FilenameFilter;
import com.aspose.imaging.fileformats.tiff.TiffFrame;

File di = new File(dataDir);
String[] files = di.list(new FilenameFilter() {
    @Override
    public boolean accept(File dir, String name) {
        return name.endsWith(".img");
    }
});

if (files != null) {
    int index = 0;
    for (String file : files) {
        try (Image inputImage = Image.load(dataDir + "/" + file)) {
            if (index > 0) {
                TiffFrame newframe = new TiffFrame(tiffOptions, width, height);
                tiffImage.addFrame(newframe);
            }
            TiffFrame frame = tiffImage.getFrames()[index];
            frame.savePixels(frame.getBounds(), ((RasterImage) inputImage).loadPixels(inputImage.getBounds()));
            index += 1;
        }
    }
}
```
- **شرح:** هذه الكتلة تتكرر عبر الملفات في الدليل التي تنتهي بـ `.img`، وتضيف كل منها كإطار جديد إلى صورة TIFF. طريقة `savePixels` تضمن نقل بيانات البكسل من كل صورة محملة بدقة.

### حفظ صورة TIFF متعددة الصفحات

**تعريف:** `Image.save` يكتب TIFF متعدد الصفحات المُجمّع إلى المسار المحدد.

#### الخطوة 1: حفظ عملك
```java
import com.aspose.imaging.examples.Utils;

tiffImage.save("YOUR_OUTPUT_DIRECTORY/output.tiff");
```
- **شرح:** طريقة `save` تكتب صورة TIFF متعددة الصفحات الكاملة إلى الدليل المحدد كإخراج. تأكد من أن هذا المسار قابل للوصول والكتابة.

## تطبيقات عملية

فهم كيفية **تحويل الصور إلى tiff** باستخدام Aspose.Imaging للغة Java يمكن أن يكون مفيدًا في عدة سيناريوهات واقعية:

1. **مشاريع الأرشفة:** تخزين متعدد للصور في ملف واحد بكفاءة للاحتفاظ بالبيانات التاريخية.
2. **التصوير الطبي:** دمج فحوصات مختلفة في مستند شامل لتسهيل التحليل والمشاركة.
3. **أنظمة إدارة المستندات:** استخدام TIFF متعددة الصفحات للحفاظ على إصدارات المستندات داخل أنظمة المؤسسة الداخلية.

يمكن دمج هذه الوظيفة مع حلول التخزين السحابي مثل AWS S3 أو Azure Blob Storage، مما يتيح عمليات أرشفة تلقائية.

## اعتبارات الأداء

عند العمل مع مكتبات معالجة الصور في Java:

- إعادة تحجيم الصور قبل إضافة الإطارات لتقليل استهلاك الذاكرة حتى 60 %.
- استخدام البث (`Image.load(stream)`) للملفات الكبيرة جدًا لتجنب تحميل الصورة بالكامل إلى ذاكرة JVM.
- إطلاق الموارد بسرعة باستخدام try‑with‑resources أو استدعاءات `dispose()` الصريحة.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|----------|
| **OutOfMemoryError** عند معالجة صور عالية الدقة | الاحتفاظ بالصورة بالكامل في الذاكرة | تمكين `TiffOptions.setSource(new FileCreateSource(..., false))` لاستخدام مصدر قائم على ملف ومعالجة الصفحات بشكل متسلسل. |
| **ظهور صفحات فارغة** بعد إضافة الإطارات | عدم توافق حجم الإطار | تأكد من أن أبعاد كل إطار تتطابق مع لوحة TIFF أو استدعِ `frame.resize()` قبل `savePixels`. |
| **ألوان غير صحيحة** بعد التحويل | لم يتم الحفاظ على مساحة اللون | قم بتعيين `tiffOptions.setColorType(ColorType.Rgb)` قبل إنشاء TIFF. |

## الأسئلة المتكررة

**س: هل يمكنني تحويل ملفات PNG أو JPEG إلى TIFF متعدد الصفحات باستخدام هذه الطريقة؟**  
ج: بالتأكيد. قم بتحميل أي تنسيق نقطي مدعوم (PNG، JPEG، BMP، إلخ) وأضف كل منها كإطار باستخدام نفس سير العمل.

**س: هل يمكن ضبط الضغط (مثل LZW) لملف TIFF الناتج؟**  
ج: نعم. يمكنك تكوين `tiffOptions.setCompression(TiffCompression.Lzw)` قبل إنشاء الصورة.

**س: كيف يمكنني إضافة بيانات تعريفية (مثل المؤلف، الوصف) لكل إطار في TIFF؟**  
ج: استخدم `frame.getMetadata().addProperty("Author", "Your Name")` بعد إنشاء الإطار وقبل الحفظ.

**س: هل يدعم Aspose.Imaging قراءة ملفات TIFF متعددة الصفحات الموجودة؟**  
ج: نعم. استخدم `Image.load("existing.tiff")` وتصفح `((TiffImage)image).getFrames()`.

**س: ماذا لو احتجت لمعالجة آلاف الصفحات؟**  
ج: عالج الصفحات على دفعات واستدعِ `System.gc()` دوريًا أو استخدم نمط `try-with-resources` (كما هو موضح) لإطلاق الذاكرة بسرعة.

## الموارد

- [توثيق Aspose.Imaging للغة Java](/reference/imaging/java/)
- [تنزيل أحدث نسخة](/imaging/java/)
- [خيارات ترخيص الشراء](/purchase/buy)
- [ابدأ بنسخة تجريبية مجانية](/imaging/java/)
- [معلومات الترخيص المؤقت](/purchase/temporary-license/)
- [دعم المجتمع والمنتديات](/forum/imaging/14)
- [شراء Aspose](/purchase/buy)

من خلال الاستفادة من هذه الموارد، يمكنك تعميق فهمك لـ Aspose.Imaging للغة Java وتطبيقه بفعالية في مشاريعك. برمجة سعيدة!

---

**آخر تحديث:** 2026-11-17  
**تم الاختبار مع:** Aspose.Imaging للغة Java 25.5  
**المؤلف:** Aspose

```java
// Example: load and save a TIFF
Image img = Image.load("input.png");
img.save("output.tiff");
```

## دروس ذات صلة

- [تحميل صور TIFF في Java باستخدام Aspose.Imaging: دليل كامل](/imaging/java/image-loading-saving/load-tiff-image-aspose-imaging-java-guide/)
- [معالجة TIFF متعدد الإطارات في Java باستخدام Aspose.Imaging](/imaging/java/animation-multi-frame-images/java-aspose-imaging-multi-frame-tiff-processing/)
- [تحويل TIFF متعدد الإطارات إلى JPEG باستخدام Aspose.Imaging للغة Java - دليل كامل](/imaging/java/image-loading-saving/convert-multi-frame-tiff-to-jpeg-aspose-imaging-java/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}