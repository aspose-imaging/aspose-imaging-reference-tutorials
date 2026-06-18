---
date: '2026-06-18'
description: تعلم كيفية استخدام اعتماد Maven من Aspose Imaging لتحويل ملفات DJVU إلى
  صور BMP في Java. دليل خطوة بخطوة مع الإعداد، الخيارات، وتصدير نطاق الصفحات.
keywords:
- aspose imaging maven dependency
- how to convert djvu
- convert djvu to bmp java
- aspose imaging java setup
- djvu page export bmp
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how to use the Aspose Imaging Maven dependency to convert DJVU
    files to BMP images in Java. Step‑by‑step guide with setup, options, and page‑range
    export.
  headline: Aspose Imaging Maven Dependency – Convert DJVU to BMP in Java
  type: TechArticle
- description: Learn how to use the Aspose Imaging Maven dependency to convert DJVU
    files to BMP images in Java. Step‑by‑step guide with setup, options, and page‑range
    export.
  name: Aspose Imaging Maven Dependency – Convert DJVU to BMP in Java
  steps:
  - name: '**Archiving:** Convert DJVU files to BMP for easier archival and retrieval.'
    text: '**Archiving:** Convert DJVU files to BMP for easier archival and retrieval.'
  - name: '**Document Sharing:** Share individual images from DJVU documents without
      requiring specialized viewers.'
    text: '**Document Sharing:** Share individual images from DJVU documents without
      requiring specialized viewers.'
  - name: '**Web Development:** Use BMP images for web projects that need lossless
      graphics.'
    text: '**Web Development:** Use BMP images for web projects that need lossless
      graphics.'
  - name: '**Education:** Provide students with accessible image formats for study
      materials.'
    text: '**Education:** Provide students with accessible image formats for study
      materials.'
  - name: '**Integration:** Embed this conversion process into larger Java applications
      for automated workflows.'
    text: '**Integration:** Embed this conversion process into larger Java applications
      for automated workflows.'
  type: HowTo
- questions:
  - answer: DJVU is a highly compressed file format designed for storing scanned documents,
      images, and multi‑page publications while maintaining visual fidelity.
    question: What is a DJVU file?
  - answer: Yes, modify the `IntRange` parameters to target any start and end indices
      you require.
    question: Can I convert other page ranges besides the first two pages?
  - answer: Increase the bits‑per‑pixel setting in `BmpOptions` to 32 and ensure the
      source DJVU pages are not downscaled during loading.
    question: My BMP files look blurry—how can I improve quality?
  - answer: Process the file in chunks, dispose of each `DjvuImage` after saving,
      and consider streaming pages rather than loading the entire document at once.
    question: How do I handle very large DJVU files efficiently?
  - answer: Visit the [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      or the [Aspose.Imaging Java Documentation](https://reference.aspose.com/imaging/java/)
      for comprehensive guides, API references, and sample projects. For community
      help, see [Aspose.Imaging Support](https://forum.aspose.com/c/imaging/14).
    question: Where can I find more Aspose.Imaging resources?
  type: FAQPage
title: اعتماد Maven من Aspose Imaging – تحويل DJVU إلى BMP في Java
url: /ar/java/format-conversion-export/export-djvu-pages-bmp-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# دليل شامل: استخدام Aspose.Imaging Java لتصدير صفحات DJVU كملفات BMP

## مقدمة

في العصر الرقمي، إدارة وتحويل صيغ المستندات بكفاءة أمر حاسم لتبادل المحتوى بسلاسة وأرشفة فعّالة. **The Aspose Imaging Maven dependency** يجعل من السهل تحويل ملفات DJVU إلى صور BMP أكثر قابلية للوصول دون الحاجة لكتابة شفرة تحليل منخفضة المستوى. يوضح هذا الدرس كيفية تحميل مستند DJVU، ضبط خيارات تصدير BMP، اختيار صفحات محددة، وحفظ كل صفحة كملف BMP منفصل—كل ذلك ببضع أسطر من Java.

**ما ستتعلمه**

- كيفية إضافة Aspose Imaging Maven dependency إلى مشروعك.  
- كيفية تحميل ومعالجة ملفات DJVU باستخدام Aspose.Imaging لـ Java.  
- كيفية ضبط خيارات تصدير BMP مثل عمق اللون.  
- كيفية تعريف نطاق صفحات مخصص وتصدير تلك الصفحات كملفات BMP منفصلة.  

بنهاية هذا الدليل، ستكون قادرًا على دمج تحويل DJVU إلى BMP في أي تطبيق Java، مما يحسّن سير عمل المستندات ويقلل الاعتماد على عارضات الطرف الثالث.

## إجابات سريعة
- **Which Maven artifact adds Aspose.Imaging?** `com.aspose:aspose-imaging`
- **Can I export only selected pages?** Yes, use `IntRange` to specify page indices.
- **What BMP color depth is recommended?** 32 bits per pixel for lossless quality.
- **Is a license required for production?** Yes, a purchased license removes evaluation limits.
- **Which Java version is supported?** Java 8 and later.

## ما هو Aspose Imaging Maven Dependency؟
**Aspose Imaging Maven dependency** هو حزمة متوافقة مع Maven توفر API شاملة لقراءة، معالجة، وتحويل أكثر من 100 صيغة صورة ومستند مباشرة من شفرة Java. إضافة هذه الاعتمادية إلى ملف `pom.xml` يمنحك وصولًا فوريًا إلى فئات مثل `Image`، `DjvuImage`، و `IntRange` دون الحاجة لإدارة JAR يدويًا.

## لماذا تستخدم Aspose.Imaging لتحويل DJVU إلى BMP؟
Aspose.Imaging يدعم **أكثر من 100 صيغة إدخال وإخراج** ويمكنه معالجة ملفات DJVU متعددة الصفحات دون تحميل المستند بالكامل إلى الذاكرة، مما يقلل استهلاك RAM بنسبة تصل إلى 70 % مقارنةً بالطرق البسيطة. مشفر BMP الأصلي يحافظ على دقة الألوان بالكامل، مما يجعله مثاليًا لاستخراج صور بأعلى جودة للأرشفة.

## المتطلبات المسبقة
- **Aspose.Imaging for Java** الإصدار 25.5 (أو أحدث).  
- **Java Development Kit** 8 أو أحدث مثبت.  
- إلمام بأدوات البناء Maven أو Gradle.  
- ترخيص Aspose.Imaging صالح (التجربة تعمل للتقييم).

## إعداد Aspose.Imaging لـ Java

### معلومات التثبيت

**Maven:**  
أضف الاعتمادية التالية إلى ملف `pom.xml` الخاص بك:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

**Gradle:**  
لمستخدمي Gradle، أدرج المكتبة بهذا السطر في `build.gradle`:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

**Direct Download:**  
بدلاً من ذلك، يمكنك تنزيل أحدث إصدار من [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/). يمكنك أيضًا الرجوع إلى صفحة [Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/) لسجل الإصدارات.

### الحصول على الترخيص

لاستخدام Aspose.Imaging بالكامل:

- **Free Trial:** ابدأ بتجربة مجانية لاستكشاف إمكانياته. ([Start Your Free Trial](https://releases.aspose.com/imaging/java/))  
- **Temporary License:** احصل على ترخيص مؤقت إذا كنت بحاجة إلى مزيد من الوقت لتقييم المكتبة. ([Get a Temporary License](https://purchase.aspose.com/temporary-license/))  
- **Purchase:** للاستخدام طويل الأمد، فكر في شراء ترخيص. ([Buy Aspose.Imaging](https://purchase.aspose.com/buy))

**Basic Initialization:**  
بعد إعداد بيئتك والحصول على الترخيص (إن لزم)، قم بتهيئة Aspose.Imaging كما يلي:

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path/to/your/license/file.lic");
```

## كيفية تحويل DJVU إلى BMP في Java؟

حمّل ملف DJVU باستخدام `Image.load("source.djvu")`، اضبط خيارات تصدير BMP، حدد نطاق الصفحات المطلوب، واستدعِ `save` لكل صفحة – يمكن إنجاز التحويل بالكامل بأقل من عشر أسطر من الشفرة. هذه الطريقة تتعامل مع عمق اللون، فهرسة الصفحات، وإدخال/إخراج الملفات تلقائيًا، مما يتيح لك التركيز على منطق الأعمال بدلاً من تحليل الصور.

### تحميل ومعالجة ملف DJVU

**نظرة عامة:**  
تحميل ملف DJVU هو الخطوة الأولى في سير العمل. Aspose.Imaging لـ Java يبسط هذه العملية، مما يتيح لك التعامل مع مستندات DJVU بسهولة.

طريقة `Image.load` تقرأ ملف DJVU إلى كائن `DjvuImage`، الذي يمثل المستند متعدد الصفحات في الذاكرة.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.djvu.DjvuImage;

String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "Sample.djvu";
try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
    // The DjVuImage object now holds the loaded DJVU file and can be processed further.
}
```

**شرح:**  
- **`Image.load`:** يحمل ملف DJVU الخاص بك ويعيد كائن `DjvuImage` لمزيد من المعالجة.  

### ضبط خيارات التصدير لتنسيق BMP

**نظرة عامة:**  
ضبط خيارات التصدير يضمن أن ملفات BMP الناتجة تلبي متطلبات الجودة الخاصة بك.

`BmpOptions` يسمح لك بتحديد خصائص مثل عدد البتات لكل بكسل، الضغط، والدقة قبل الحفظ.

```java
import com.aspose.imaging.imageoptions.BmpOptions;

BmpOptions exportOptions = new BmpOptions();
exportOptions.setBitsPerPixel(32);
```

**شرح:**  
- **`setBitsPerPixel`:** يحدد عمق اللون للصور المصدرة. استخدام 32 بت لكل بكسل ينتج ملفات BMP غير مضغوطة وعالية الجودة مناسبة للأرشفة.

### تحديد نطاق الصفحات للتصدير

**نظرة عامة:**  
تحديد الصفحات التي تريد تصديرها يتيح لك التركيز على المحتوى ذي الصلة.

`IntRange` ينشئ نطاقًا من مؤشرات الصفحات التي تبدأ من الصفر؛ في هذا المثال نختار الصفحتين الأوليين.

```java
import com.aspose.imaging.IntRange;

IntRange range = new IntRange(0, 2);
```

**شرح:**  
- **`IntRange`:** يمثل نطاقًا متواصلًا من أرقام الصفحات. عدّل قيم البداية والنهاية لتصدير أي مجموعة فرعية تحتاجها.

### تصدير الصفحات المحددة كملفات BMP منفصلة

**نظرة عامة:**  
الخطوة النهائية تتضمن تصدير الصفحات المختارة كملفات BMP فردية.

`DjvuMultiPageOptions` يضبط التصدير لكل صفحة، و `image.save` يكتب ملفات BMP إلى الدليل المستهدف.

```java
import com.aspose.imaging.imageoptions.DjvuMultiPageOptions;

int counter = 0;
for (int i : range.getRange()) {
    exportOptions.setMultiPageOptions(new DjvuMultiPageOptions(range.getArrayOneItemFromIndex(counter)));
    image.save("YOUR_OUTPUT_DIRECTORY" + (counter++) + ".bmp", exportOptions);
}
```

**شرح:**  
- **`DjvuMultiPageOptions`:** يحمل معلومات نطاق الصفحات وخيارات BMP للتصدير متعدد الصفحات.  
- **`image.save`:** يحفظ كل صفحة مختارة كملف BMP منفصل على القرص.

## تطبيقات عملية

1. **الأرشفة:** تحويل ملفات DJVU إلى BMP لتسهيل الأرشفة والاسترجاع.  
2. **مشاركة المستندات:** مشاركة صور فردية من مستندات DJVU دون الحاجة إلى عارضين متخصصين.  
3. **تطوير الويب:** استخدام صور BMP في مشاريع الويب التي تحتاج إلى رسومات غير مضغوطة.  
4. **التعليم:** توفير صيغ صور قابلة للوصول للطلاب لاستخدامها في المواد الدراسية.  
5. **التكامل:** دمج عملية التحويل هذه في تطبيقات Java أكبر لأتمتة سير العمل.

## اعتبارات الأداء

- **تحسين استخدام الذاكرة:** حرّر كائنات `DjvuImage` فورًا باستخدام `close()` لتحرير الموارد الأصلية.  
- **المعالجة الدفعية:** عالج عدة ملفات DJVU في حلقة لتقليل عبء الإدخال/الإخراج.  
- **المعالجة المتوازية:** استفد من `ExecutorService` في Java لتحويل الصفحات بشكل متزامن على خوادم متعددة النوى.

## المشكلات الشائعة والحلول

- **OutOfMemoryError في ملفات DJVU الكبيرة:** استخدم `image.dispose()` بعد حفظ كل صفحة وفكر في زيادة حجم heap للـ JVM فقط عند الحاجة.  
- **إخراج BMP منخفض الجودة:** تأكد من ضبط `BmpOptions.setBitsPerPixel(32)`؛ القيم الأقل تقلل من دقة الألوان.  
- **غياب صفحات في الناتج:** تحقق من أن مؤشرات `IntRange` تتطابق مع عدد الصفحات الفعلي (`djvuImage.getPages().size()`).

## الأسئلة المتكررة

**س: ما هو ملف DJVU؟**  
ج: DJVU هو صيغة مضغوطة عاليًا مصممة لتخزين المستندات الممسوحة ضوئيًا، الصور، والمنشورات متعددة الصفحات مع الحفاظ على جودة بصرية جيدة.

**س: هل يمكنني تحويل نطاق صفحات آخر غير الصفحتين الأوليين؟**  
ج: نعم، عدّل معلمات `IntRange` لاستهداف أي بداية ونهاية تحتاجها.

**س: ملفات BMP الخاصة بي تبدو غير واضحة—كيف يمكن تحسين الجودة؟**  
ج: زد إعداد `bits‑per‑pixel` في `BmpOptions` إلى 32 وتأكد من أن صفحات DJVU الأصلية لم تُقلص أثناء التحميل.

**س: كيف أتعامل مع ملفات DJVU الكبيرة جدًا بكفاءة؟**  
ج: عالج الملف على دفعات، حرّر كل `DjvuImage` بعد الحفظ، وفكّر في بث الصفحات بدلاً من تحميل المستند بالكامل مرة واحدة.

**س: أين يمكنني العثور على المزيد من موارد Aspose.Imaging؟**  
ج: زر [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/) أو [Aspose.Imaging Java Documentation](https://reference.aspose.com/imaging/java/) للحصول على أدلة شاملة، مراجع API، ومشاريع نموذجية. للمساعدة المجتمعية، راجع [Aspose.Imaging Support](https://forum.aspose.com/c/imaging/14).

---

**آخر تحديث:** 2026-06-18  
**تم الاختبار مع:** Aspose.Imaging 25.5 for Java  
**المؤلف:** Aspose

## دروس ذات صلة

- [Convert DjVu to Grayscale PNG with Aspose.Imaging for Java | Format Conversion Tutorial](/imaging/java/format-conversion-export/export-djvu-grayscale-png-aspose-java/)
- [Convert DjVu to TIFF in Java with Aspose.Imaging: Step-by-Step Guide](/imaging/java/format-conversion-export/load-export-djvu-tiff-aspose-imaging-java/)
- [Convert DjVu to PDF using Aspose.Imaging for Java - Step-by-Step Guide](/imaging/java/image-loading-saving/convert-djvu-to-pdf-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}