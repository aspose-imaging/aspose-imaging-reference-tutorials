---
date: '2026-09-28'
description: تعلم كيفية استخدام ccittfax3 compression java لإنشاء ملفات TIFF متعددة
  الصفحات باستخدام Aspose.Imaging. قم بمسح المستندات بفعالية، وأرشفتها، وتقليل حجم
  الملف لتسهيل سير عمل المستندات.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: اكتشف خطوة بخطوة كيفية استخدام ccittfax3 compression java مع Aspose.Imaging
  لإنشاء ملفات TIFF متعددة الصفحات بكفاءة للمسح الضوئي والأرشفة.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: كيفية إنشاء ملف TIFF متعدد الصفحات باستخدام ccittfax3 compression java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: كيفية إنشاء ملف TIFF متعدد الصفحات باستخدام ccittfax3 compression java
url: /ar/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إتقان إنشاء ملفات TIFF متعددة الصفحات باستخدام ضغط ccittfax3 في Java مع Aspose.Imaging

## المقدمة

إذا كنت بحاجة إلى أرشفة كميات كبيرة من المستندات الممسوحة ضوئياً مع الحفاظ على حجم الملفات منخفضًا، فإن **ccittfax3 compression java** هو الحل المثالي. يوضح هذا الدرس كيفية إنشاء ملفات TIFF متعددة الصفحات باستخدام ضغط CCITTFAX3 في Java مع Aspose.Imaging. ستتعلم لماذا يعمل هذا الضغط بشكل ممتاز للصور أحادية اللون، وكيفية تكوين المكتبة، وكيفية إضافة كل صفحة كإطار.

**ما ستتعلمه**
- كيفية إضافة Aspose.Imaging إلى مشروع Java.
- كيفية تكوين `TiffOptions` لضغط CCITTFAX3.
- كيفية إنشاء `TiffImage`، تغيير حجم الصور المصدر، وإضافتها كإطارات.
- كيفية حفظ ملف TIFF متعدد الصفحات النهائي بكفاءة.

دعونا نتبع التنفيذ الكامل.

## إجابات سريعة
- **ما هو الفائدة الرئيسية لضغط CCITTFAX3؟** تقليل حجم الملف بنسبة تصل إلى 80 % للصور بالأبيض والأسود.  
- **أي مكتبة توفر دعمًا مدمجًا؟** Aspose.Imaging for Java، الإصدار 25.5+.  
- **هل أحتاج إلى ترخيص للتطوير؟** ترخيص تجريبي مجاني يعمل مع جميع الميزات؛ يلزم ترخيص مدفوع للإنتاج.  
- **هل يمكنني معالجة مئات الصفحات؟** نعم—Aspose.Imaging يبث الصفحات، لذا يبقى استهلاك الذاكرة منخفضًا.  
- **هل الكود متوافق مع Java 11 وما بعده؟** بالتأكيد؛ الـ API يستهدف Java 8+.

## ما هو ضغط ccittfax3 في Java؟
`CCITTFAX3` هو خوارزمية ضغط غير فقدانية أحادية اللون صُممت للفاكس وصور المستندات الممسوحة ضوئياً. تقوم بترميز كل بكسل كبتة واحدة، مما ينتج مخرجات عالية الجودة مع تقليل حجم الملف بشكل كبير—غالبًا بنسبة 70‑80 % مقارنةً بـ TIFF غير مضغوط. يجعل ذلك منه مثاليًا لأرشفة المستندات بالأبيض والأسود حيث يجب الحفاظ على الدقة.

## لماذا نستخدم Aspose.Imaging لهذه المهمة؟
Aspose.Imaging يدعم **100+** صيغ إدخال وإخراج، بما في ذلك PDF و PNG و JPEG و TIFF. يمكن لهندسته المعمارية القائمة على البث معالجة ملفات TIFF **متعددة المئات من الصفحات** دون تحميل المستند بالكامل في الذاكرة، مما يجعله مثاليًا لمشاريع الأرشفة على نطاق واسع.

## المتطلبات المسبقة

- **Java Development Kit (JDK)** 8 أو أحدث مثبت.
- **IDE** مثل IntelliJ IDEA أو Eclipse.
- **Maven** أو **Gradle** لإدارة التبعيات.
- معرفة أساسية بـ Java (الفئات، الكائنات، المجموعات).

## إعداد Aspose.Imaging للـ Java

Add the library to your build file.

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```  

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

### التحميل المباشر

يمكنك أيضًا تنزيل أحدث JAR من [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### الحصول على الترخيص

ترخيص تجريبي مجاني متاح من [صفحة التجربة المجانية لـ Aspose](https://releases.aspose.com/imaging/java/). للاستخدام الإنتاجي، اشترِ ترخيصًا دائمًا أو اطلب ترخيصًا مؤقتًا عبر [Aspose Purchase](https://purchase.aspose.com/temporary-license/).

للاطلاع على تفاصيل استخدام الـ API، راجع [توثيق Aspose.Imaging للـ Java](https://reference.aspose.com/imaging/java/).

### التهيئة الأساسية

After adding the dependency, initialise the library as shown below.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## كيفية تكوين ضغط ccittfax3 للـ Java لإنشاء TIFF متعدد الصفحات؟

`TiffOptions` هي فئة تحدد تنسيق الإخراج وإعدادات الضغط لملف TIFF. قم بتحميل كائن `TiffOptions` باستخدام تعداد `CCITTGroup3FaxCompression`، ثم حدد مصدر ملف الإخراج. هذه الإعدادات ذات الخطوتين تُعد الكاتب للضغط أحادي اللون وتضمن أن كل صفحة تُضاف لاحقًا سيتم ترميزها باستخدام خوارزمية CCITTFAX3، مما يؤدي إلى تقليل حجم كبير مع الحفاظ على جودة الصورة.

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## كيفية إنشاء كائن TiffImage في Java؟

`TiffImage` تمثل مستند TIFF متعدد الصفحات في الذاكرة وتوفر طرقًا للتعامل مع إطاراته. أولاً، حدد العرض والارتفاع المشتركين لجميع الصفحات. ثم أنشئ كائن `TiffImage` باستخدام `TiffOptions` التي تم إنشاؤها مسبقًا. يعمل كائن `TiffImage` كحاوية للإطارات الفردية، مما يتيح لك إضافة أو إزالة أو إعادة ترتيب الصفحات قبل حفظ الملف النهائي.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## كيفية تحميل وتغيير حجم الصور المصدر من مجلد؟

قم بتصفية الدليل المستهدف للعثور على ملفات JPEG، اقرأ كل صورة، وقم بتغيير حجمها لتتناسب مع لوحة TIFF. تغيير الحجم قبل إضافة الإطارات يقلل من استهلاك الذاكرة ويسرّع عملية الحفظ. من خلال تحويل كل صورة مصدر إلى الأبعاد وتنسيق البكسل المطلوبين، تضمن تخطيط صفحات متسق وتتفادى أخطاء وقت التشغيل عند إلحاق الإطارات بمستند TIFF.

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## كيفية إضافة كل صورة كإطار إلى TIFF متعدد الصفحات؟

`TiffFrame` هو كائن يحمل صورة صفحة واحدة والبيانات الوصفية المرتبطة بها داخل TIFF. قم بالتكرار على الصور التي تم تغيير حجمها، أنشئ `TiffFrame` جديدًا، وألحقه بـ `TiffImage`. يصبح كل إطار صفحة منفصلة في المستند النهائي، وتتعامل المكتبة تلقائيًا مع تحديثات البيانات الوصفية اللازمة، مثل عدد الصفحات والإزاحات، لضمان بنية TIFF متعددة الصفحات صالحة.

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## كيفية حفظ ملف TIFF متعدد الصفحات النهائي؟

استدعِ طريقة `save` على كائن `TiffImage`، مع تمرير مسار الإخراج المطلوب. تقوم المكتبة تلقائيًا بكتابة جميع الإطارات باستخدام ضغط CCITTFAX3، وتبث البيانات إلى القرص بكفاءة، وتغلق أي موارد أساسية. بعد اكتمال عملية الحفظ، يحتوي الملف الناتج على جميع الصفحات بالضغط المحدد، جاهز للتوزيع أو الأرشفة.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## التطبيقات العملية

- **أرشفة المستندات:** تخزين العقود الممسوحة، الفواتير، أو السجلات القانونية بأقل مساحة تخزين.
- **التصوير الطبي:** ضغط فحوصات الأشعة مع الحفاظ على التفاصيل التشخيصية.
- **إنتاج الطباعة:** إنشاء مهام طباعة متعددة الصفحات يمكن للطابعات استهلاكها مباشرة.

## اعتبارات الأداء

- استخدم `ResizeOptions` التي تحافظ على نسبة الأبعاد لتجنب التشويه.
- أغلق كل كائن `Image` بعد إضافة إطاره لتحرير الذاكرة الأصلية.
- للمجموعات الكبيرة جدًا، عالج الملفات في تدفقات متوازية واكتب كل جزء من TIFF بشكل غير متزامن.

## المشكلات الشائعة واستكشاف الأخطاء

- **تنسيق بكسل غير صحيح:** يعمل CCITTFAX3 فقط مع صور 1‑bit (أبيض وأسود). حوّل الصور الملونة إلى تدرج الرمادي قبل تغيير الحجم.
- **تسرب الذاكرة:** دائمًا استدعِ `dispose()` على كائنات `Image` المؤقتة؛ وإلا ستظل المخازن الأصلية محجوزة.
- **حجم الملف لم ينخفض:** تأكد من ضبط خاصية الضغط في `TiffOptions`؛ وإلا سيُستخدم الافتراضي (بدون ضغط).

## الأسئلة المتكررة

**س: هل يمكنني استخدام هذه الطريقة مع الصور الملونة؟**  
ج: يقتصر CCITTFAX3 على البيانات أحادية اللون؛ للون استخدم ضغط JPEG أو LZW بدلاً من ذلك.

**س: هل يدعم Aspose.Imaging البث لملفات TIFF الضخمة؟**  
ج: نعم—المكتبة تكتب كل إطار مباشرة إلى تدفق الإخراج، مما يحافظ على انخفاض استهلاك الذاكرة حتى لآلاف الصفحات.

**س: كيف يمكنني تطبيق ترخيص مؤقت برمجيًا؟**  
ج: حمّل ملف `.lic` باستخدام `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.

**س: هل هناك طريقة لمعاينة TIFF قبل الحفظ؟**  
ج: يمكنك عرض كل `TiffFrame` كـ `BufferedImage` وعرضه في مكوّن Swing.

**س: ما إصدارات Java المدعومة رسميًا؟**  
ج: يدعم Aspose.Imaging Java 8 حتى Java 21، بما في ذلك إصدارات LTS.

## الخلاصة

أنت الآن تمتلك سير عمل كامل وجاهز للإنتاج لإنشاء ملفات TIFF متعددة الصفحات باستخدام **ccittfax3 compression java** مع Aspose.Imaging. باتباع الخطوات أعلاه، يمكنك أرشفة مجموعات مستندات ضخمة بكفاءة مع الحفاظ على انخفاض تكاليف التخزين وجودة الصورة العالية. استكشف ميزات إضافية في Aspose.Imaging—مثل OCR، ومعالجة البيانات الوصفية، وتحويل الصيغ—لتعزيز خط أنابيب معالجة المستندات الخاص بك.

---

**آخر تحديث:** 2026-09-28  
**تم الاختبار مع:** Aspose.Imaging 25.5 للـ Java  
**المؤلف:** Aspose

## دروس ذات صلة

- [كيفية إنشاء TIFF متعدد الصفحات باستخدام Aspose.Imaging للـ Java – دليل كامل](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [كيفية تقليل حجم ملف الصورة باستخدام ضغط LZW في Java](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [تقسيم إطارات TIFF متعددة الصفحات باستخدام Aspose.Imaging للـ Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}