---
date: '2026-09-02'
description: تعلم كيفية إنشاء مسار قص واستخراجه من صور TIFF باستخدام Aspose.Imaging
  for Java. اتبع التعليمات خطوة بخطوة لتحويل TIFF إلى PSD بكفاءة.
keywords:
- create clipping path
- how to extract path
- how to convert tiff
- aspose imaging java
- convert tiff to psd
lastmod: '2026-09-02'
og_description: تعلم كيفية إنشاء مسار قص واستخراجه من صور TIFF باستخدام Aspose.Imaging
  for Java. اتبع الكود خطوة بخطوة لتحويل TIFF إلى PSD.
og_image_alt: Guide showing how to create clipping path in TIFF using Aspose.Imaging
  Java
og_title: إنشاء مسار قص في ملفات TIFF باستخدام Aspose.Imaging for Java
schemas:
- author: Aspose
  dateModified: '2026-09-02'
  description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  headline: Create clipping path in TIFF with Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  name: Create clipping path in TIFF with Aspose.Imaging for Java
  steps:
  - name: '**Free trial** – start with a 30‑day trial.'
    text: '**Free trial** – start with a 30‑day trial.'
  - name: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
    text: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
  - name: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
    text: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
  - name: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
    text: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
  - name: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
    text: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
  type: HowTo
- questions:
  - answer: Yes, provided you have a valid commercial license; a free trial is available
      for evaluation.
    question: Can I use Aspose.Imaging for Java in a commercial application?
  - answer: The library supports over 100 formats, including TIFF, PSD, BMP, JPEG,
      PNG, and many more.
    question: What image formats does Aspose.Imaging support?
  - answer: Verify that the source TIFF actually contains vector path resources; use
      the `hasPathResources()` check before extraction.
    question: How do I troubleshoot path extraction errors?
  - answer: Absolutely – combine the extraction code with Java’s parallel streams
      or an executor service to handle many files efficiently.
    question: Is batch processing of multiple TIFFs possible?
  - answer: Complex shapes may need manual adjustment after creation; the API handles
      standard Bezier curves and straight lines reliably.
    question: Are there limitations when creating clipping paths in TIFF?
  type: FAQPage
tags:
- create clipping path
- TIFF processing
- Aspose.Imaging
- Java image manipulation
- PSD conversion
title: إنشاء مسار قص في ملفات TIFF باستخدام Aspose.Imaging for Java
url: /ar/java/format-specific-operations/aspose-imaging-java-tiff-path-extraction/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء مسار قص في TIFF باستخدام Aspose.Imaging للـ Java

في هذا الدليل الشامل ستتعلم **كيفية إنشاء مسار قص** في ملف TIFF وكيفية استخراج المسارات الموجودة باستخدام Aspose.Imaging للـ Java. في النهاية، ستكون قادرًا على تحويل صور TIFF إلى ملفات PSD قابلة للتحرير بالكامل، مما يجعلها جاهزة لبرنامج Photoshop أو أي محرر يدعم المتجهات.

## إجابات سريعة
- **ما هو مسار القص؟** مخطط متجه يحدد المناطق الشفافة والمعتمة في الصورة.  
- **هل يمكنني استخراج مسار موجود من TIFF؟** نعم – يمكن لـ Aspose.Imaging قراءة موارد المسار المدمجة وحفظها كملف PSD.  
- **كيف يمكنني إضافة مسار قص جديد؟** أنشئ `PathResource`، واملأه بسجلات المتجه، ثم عينه إلى الإطار النشط للصورة.  
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟** يلزم وجود ترخيص صالح لـ Aspose.Imaging للنشر التجاري.  
- **ما نسخة Java المطلوبة؟** JDK 8 أو أعلى؛ المكتبة تعمل مع Java 11، 17، وما بعده.

## ما هو مسار القص؟
مسار القص هو مخطط يعتمد على المتجه يحدد لمحركات العرض أي أجزاء من الصورة يجب إظهارها أو إخفاؤها. يتم تخزينه كموارد مسار داخل ملفات TIFF أو PSD ويمكن تحريره في Adobe Photoshop.

## لماذا تحويل TIFF إلى PSD؟
تحويل TIFF إلى PSD يتيح تحريرًا بدون فقدان للطبقات والماسكات ومسارات القص. يدعم Aspose.Imaging **أكثر من 50 تنسيقًا للإدخال والإخراج** ويمكنه معالجة ملفات TIFF متعددة الصفحات مئات الصفحات دون تحميل الملف بالكامل في الذاكرة، مما يمنحك تحويل دفعي عالي الأداء.

## المتطلبات المسبقة
- **Java Development Kit (JDK)** 8 أو أحدث مثبت.
- **Aspose.Imaging for Java** مكتبة (أضفها عبر Maven أو Gradle أو التحميل المباشر).
- إلمام أساسي بمفاهيم برمجة Java.

## كيفية إعداد Aspose.Imaging للـ Java
قبل إضافة أي كود، تأكد من أن المكتبة مُشار إليها بشكل صحيح في نظام البناء الخاص بك وأن لديك ملف ترخيص صالح. هذا يضمن أن API يعمل بدون قيود التقييم وأن جميع الميزات، بما في ذلك معالجة المسارات، متاحة.

### Maven
أضف الاعتماد التالي إلى ملف `pom.xml` الخاص بك:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle
أدرج هذا السطر في ملف `build.gradle` الخاص بك:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### التحميل المباشر
حمّل أحدث نسخة من [إصدارات Aspose.Imaging للـ Java](https://releases.aspose.com/imaging/java/).

#### الحصول على الترخيص
1. **تجربة مجانية** – ابدأ بتجربة لمدة 30 يومًا.  
2. **ترخيص مؤقت** – احصل على واحد من [صفحة الترخيص المؤقت](https://purchase.aspose.com/temporary-license/).  
3. **شراء** – اشترِ ترخيصًا كاملاً من [موقع Aspose](https://purchase.aspose.com/buy).

بعد التثبيت والترخيص، قم بتهيئة Aspose.Imaging في مشروعك:
```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path_to_license_file");
```

## كيفية استخراج مسار القص من TIFF؟
يتضمن استخراج مسار القص تحميل ملف TIFF، وتحديد أي موارد مسار مدمجة، وكتابة تلك الموارد إلى ملف PSD جديد. تقرأ العملية بيانات المتجه مباشرةً من صورة المصدر، مع الحفاظ على الدقة وتجنب تحويلها إلى نقطية.

حمّل ملف TIFF، وتكرّر عبر موارد المسار الخاصة به، واحفظ النتيجة كملف PSD. تقوم هذه العملية بقراءة بيانات المتجه المدمجة وكتابتها إلى ملف جديد في خطوة واحدة.
```java
String filePath = "YOUR_DOCUMENT_DIRECTORY/SupportExtractingPathsFromTiff/Sample.tif";
try (TiffImage image = (TiffImage) com.aspose.imaging.Image.load(filePath)) {
    // Proceed with extraction steps...
}
```

تكرّر عبر موارد المسار في الإطار النشط وجمعها:
```java
for (PathResource path : image.getActiveFrame().getPathResources()) {
    System.out.println(path.getName());  // Output the name of each path resource found.
}
```

احفظ الصورة مع المسارات المستخرجة إلى ملف PSD جديد:
```java
String outFilePath = "YOUR_OUTPUT_DIRECTORY/SampleWithPaths.psd";
image.save(outFilePath);
```

## كيفية إنشاء مسار قص في TIFF؟
يتطلب إنشاء مسار قص بناء `PathResource` يصف المخطط المتجه المطلوب، وإرفاقه بالإطار النشط لملف TIFF، ثم حفظ الصورة (أو نسخة) كملف PSD بحيث يُحفظ المسار. يتيح لك هذا النهج إضافة أقنعة متجهية إلى ملفات نقطية برمجيًا.

يمثل PathResource مسارًا متجهيًا مخزنًا داخل ملف صورة.  
قم بتهيئة `PathResource` جديد بالسمات المطلوبة:
```java
final PathResource pathResource = new PathResource();
pathResource.setBlockId((short) 2000); // Set Block ID per Photoshop specs
pathResource.setName("My Clipping Path"); // Name your clipping path for easy identification

// Create and add vector path records using the provided coordinates.
pathResource.setRecords(createRecords(0.2f, 0.2f, 0.8f, 0.2f, 0.8f, 0.8f, 0.2f, 0.8f));
```

عيّن مورد المسار الذي تم إنشاؤه إلى الإطار النشط للصورة:
```java
List<PathResource> list = new LinkedList<>();
list.add(pathResource);
image.getActiveFrame().setPathResources(list);
```

احفظ ملف TIFF المعدل كملف PSD يحتوي الآن على مسار القص:
```java
String outFilePath2 = "YOUR_OUTPUT_DIRECTORY/ImageWithPath.psd";
image.save(outFilePath2);
```

## طرق المساعدة

### إنشاء السجلات
أنشئ سجلات مسار المتجه باستخدام عقد Bezier وسجلات الطول:
```java
private static List<VectorPathRecord> createRecords(float ... coordinates) {
    List<VectorPathRecord> records = createBezierRecords(coordinates); 
    LengthRecord lr = new LengthRecord();
    lr.setOpen(false);
    lr.setRecordCount(records.size());
    
    records.add(0, lr);
    return records;
}
```

### إنشاء سجلات Bezier
حوّل مصفوفات الإحداثيات إلى سجلات مسار متجه Bezier:
```java
private static List<VectorPathRecord> createBezierRecords(float[] coordinates) {
    final List<VectorPathRecord> list = new LinkedList<>();
    
    for (int index = 0; index < coordinates.length - 1; index += 2) {
        PointF point = new PointF(coordinates[index], coordinates[index + 1]);
        list.add(createBezierRecord(point));
    }
    
    return list;
}
```

### إنشاء سجل Bezier
عرّف سجل مسار متجه عقدة Bezier واحدة:
```java
private static VectorPathRecord createBezierRecord(PointF point) {
    BezierKnotRecord it = new BezierKnotRecord();
    it.setPathPoints(new PointF[] { point, point, point });
    return it;
}
```

## التطبيقات العملية
1. **سير عمل التصميم الجرافيكي** – تحويل TIFF إلى PSD لتحرير الطبقات والماسكات في Photoshop.  
2. **خطوط معالجة الصور الآلية** – معالجة دفعة من آلاف ملفات TIFF، استخراج أو إضافة مسارات في الوقت الفعلي.  
3. **التصوير البصري القائم على البيانات** – استخدم مسارات المتجه لإنشاء مخططات أو مخططات دقيقة من مصادر نقطية.

## اعتبارات الأداء
- **إدارة الذاكرة** – استخدم try‑with‑resources لضمان التخلص السريع من كائنات الصورة.  
- **المعالجة الدفعية** – قم بتوازي التحويلات باستخدام `ForkJoinPool` في Java لمجموعات الصور الكبيرة.  
- **معالجة الدقة** – عدّل DPI فقط عند الضرورة للحفاظ على وقت المعالجة منخفضًا مع الحفاظ على الجودة.

## الخلاصة
أنت الآن تعرف كيف **تنشئ مسار قص** في ملفات TIFF وتستخرج المسارات الموجودة باستخدام Aspose.Imaging للـ Java. تتيح لك هذه التقنيات دمج معالجة صور متقدمة في أي سير عمل مبني على Java، من الأدوات المكتبية إلى خطوط المعالجة على مستوى المؤسسات.

### الخطوات التالية
- جرّب أشكالًا متجهية مختلفة وسمات المسار.  
- استكشف ميزات إضافية في Aspose.Imaging مثل إضافة العلامات المائية، تحويل الصيغ، ومعالجة البيانات الوصفية.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Imaging للـ Java في تطبيق تجاري؟**  
ج: نعم، بشرط أن يكون لديك ترخيص تجاري صالح؛ تتوفر نسخة تجريبية مجانية للتقييم.

**س: ما هي صيغ الصور التي يدعمها Aspose.Imaging؟**  
ج: تدعم المكتبة أكثر من 100 صيغة، بما في ذلك TIFF، PSD، BMP، JPEG، PNG، والعديد غيرها.

**س: كيف يمكنني استكشاف أخطاء استخراج المسار؟**  
ج: تأكد من أن ملف TIFF المصدر يحتوي فعليًا على موارد مسار متجه؛ استخدم الفحص `hasPathResources()` قبل الاستخراج.

**س: هل المعالجة الدفعية لعدة ملفات TIFF ممكنة؟**  
ج: بالتأكيد – اجمع كود الاستخراج مع تدفقات Java المتوازية أو خدمة تنفيذ لمعالجة العديد من الملفات بكفاءة.

**س: هل هناك قيود عند إنشاء مسارات قص في TIFF؟**  
ج: قد تحتاج الأشكال المعقدة إلى تعديل يدوي بعد الإنشاء؛ تتعامل API بشكل موثوق مع منحنيات Bezier القياسية والخطوط المستقيمة.

---

**آخر تحديث:** 2026-09-02  
**تم الاختبار مع:** Aspose.Imaging for Java 24.12  
**المؤلف:** Aspose  

## الموارد

- [توثيق Aspose.Imaging](https://reference.aspose.com/imaging/java/)
- [تحميل Aspose.Imaging للـ Java](https://releases.aspose.com/imaging/java/)
- [شراء ترخيص](https://purchase.aspose.com/buy)
- [تجربة مجانية](https://releases.aspose.com/imaging/java/)
- [ترخيص مؤقت](https://purchase.aspose.com/temporary-license/)
- [منتدى دعم Aspose](https://forum.aspose.com/c/imaging/14)

## دروس ذات صلة

- [تحويل الصورة إلى PSD باستخدام Aspose.Imaging للـ Java – دليل خطوة بخطوة](/imaging/java/format-conversion-export/convert-images-to-psd-using-aspose-imaging-java-guide/)
- [كيفية تحويل TIFF إلى GraphicsPath باستخدام Aspose.Imaging Java](/imaging/java/advanced-drawing-graphics/aspose-imaging-java-tiff-graphicspath-conversion/)
- [تحميل وحفظ صور TIFF بفعالية في Java باستخدام Aspose.Imaging](/imaging/java/image-loading-saving/aspose-imaging-java-tiff-image-saving/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}