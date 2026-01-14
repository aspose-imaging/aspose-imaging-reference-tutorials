---
date: 2026-01-14
description: تعلم كيفية تحويل ملفات DICOM إلى BMP وضبط قيمتها غاما في Java باستخدام
  Aspose.Imaging. يوضح هذا الدليل كيفية معالجة صور DICOM بسهولة.
linktitle: DICOM Image Gamma Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: تحويل DICOM إلى BMP – تعديل غاما باستخدام Aspose.Imaging للغة Java
url: /ar/java/image-processing-and-enhancement/dicom-image-gamma-adjustment/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DICOM إلى BMP – تعديل جاما باستخدام Aspose.Imaging للـ Java

إذا كنت بحاجة إلى **تحويل DICOM إلى BMP** مع ضبط تباين الصورة بدقة، فأنت في المكان الصحيح. في هذا البرنامج التعليمي سنستعرض الخطوات الدقيقة لتحميل ملف DICOM، وتطبيق تصحيح جاما، وحفظ النتيجة كصورة BMP باستخدام Aspose.Imaging للـ Java. في النهاية ستفهم **كيفية معالجة DICOM** برمجياً وإنتاج مخرجات bitmap عالية الجودة لتدفقات عمل التصوير الطبي اللاحقة.

## إجابات سريعة
- **ما معنى “تحويل DICOM إلى BMP”؟** يحول صورة طبية بصيغة DICOM إلى ملف BMP قياسي مع الحفاظ على بيانات البكسل.  
- **أي مكتبة تتعامل مع التحويل؟** Aspose.Imaging للـ Java توفر واجهة برمجة تطبيقات بسيطة لتحميل DICOM وحفظه كـ BMP.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **كم من الوقت يستغرق تشغيل الكود؟** أقل من ثانية لملفات DICOM النموذجية بحجم 512 × 512 على معالج حديث.  
- **هل يمكنني تغيير قيمة الجاما؟** نعم—مرّر أي عدد صحيح (مثال: 30‑70) إلى `adjustGamma()` لتناسب احتياجات التباين الخاصة بك.

## ما هو “تحويل DICOM إلى BMP”؟
يعني تحويل DICOM إلى BMP فك تشفير صيغة الصورة الطبية DICOM وإعادة ترميز بيانات البكسل إلى ملف BMP. يُدعم BMP على نطاق واسع من أدوات التصوير، مما يجعله مثالياً للفحص البصري، وإعداد التقارير، أو المعالجة الإضافية.

## لماذا تعديل الجاما عند التحويل؟
تعديل الجاما يغيّر منحنى الإضاءة في الصورة، مما يعزز وضوح التفاصيل الدقيقة دون تعديل البيانات الأساسية. هذا مهم بشكل خاص في مجال الأشعة حيث يمكن أن يؤثر التباين على التشخيص.

## المتطلبات المسبقة

### 1. بيئة تطوير Java
- JDK 8 أو أحدث مثبت ومُعد في بيئة التطوير المتكاملة (IDE) أو سطر الأوامر.

### 2. مكتبة Aspose.Imaging للـ Java
- قم بتنزيل المكتبة من [رابط التحميل](https://releases.aspose.com/imaging/java/).

### 3. صورة DICOM الإدخال
- احرص على وجود ملف DICOM جاهز. تتوفر ملفات عينة مجانية على الإنترنت للاختبار.

## استيراد الحزم
أولاً، استورد الفئات التي ستحتاجها. يجب أن يبقى المكوّن أدناه كما هو تمامًا:

```java
import com.aspose.imaging.fileformats.dicom.DicomImage;
import com.aspose.imaging.image.Image;
import com.aspose.imaging.imageoptions.BmpOptions;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
```

## تحويل DICOM إلى BMP – دليل خطوة بخطوة

### الخطوة 1: تعيين مسارات الملفات
حدد مكان وجود ملف DICOM المصدر ومكان كتابة ملف BMP الناتج.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = dataDir + "AdjustingGamma.bmp";
```

### الخطوة 2: تحميل صورة DICOM
افتح تدفق الملف وأنشئ مثيلًا من `DicomImage`.

```java
File file = new File(inputFile);

try (FileInputStream fis = new FileInputStream(file)) {
    // Load a DICOM image in an instance of DicomImage
    try (DicomImage image = (DicomImage) Image.load(fis)) {
```

### الخطوة 3: تعديل الجاما
طبق تصحيح الجاما المطلوب (مثال: 50) قبل الحفظ.

```java
        // Adjust the gamma
        image.adjustGamma(50);
```

### الخطوة 4: حفظ BMP الناتج
أنشئ خيارات BMP واكتب الصورة المعالجة إلى القرص. يتعامل كتلة `catch` مع أي مشكلات إدخال/إخراج.

```java
        // Create an instance of BmpOptions for the resultant image and save the resultant image
        image.save(outputFile, new BmpOptions());
    }
} catch (IOException ex) {
    // Handle any potential exceptions
    com.aspose.imaging.examples.Logger.println(ex.getMessage());
    ex.printStackTrace();
}
```

هذا هو سير العمل الكامل لـ **تحويل DICOM إلى BMP** مع تعديل الجاما.

## المشكلات الشائعة والحلول
- **علامات DICOM غير المدعومة** – تأكد من أن ملف DICOM يحتوي على بيانات البكسل؛ قد تحتاج التدفقات المشفرة أو المضغوطة إلى فك ترميز إضافي.  
- **أخطاء نفاد الذاكرة** – للصور الكبيرة جدًا، زد حجم ذاكرة JVM (`-Xmx2g`) أو عالج الصورة على شكل قطع.  
- **قيمة جاما غير صحيحة** – القيم الأقل من 0 أو الأعلى من 100 قد تنتج نتائج غير متوقعة؛ التزم بالنطاق 0‑100.

## الأسئلة المتكررة

**س: ما هي صورة DICOM؟**  
ج: DICOM (Digital Imaging and Communications in Medicine) هي الصيغة العالمية لتخزين ونقل الصور الطبية مثل الأشعة السينية، والمسح الضوئي الطبقي (CT)، والرنين المغناطيسي (MRI).

**س: لماذا تعديل الجاما مهم لصور DICOM؟**  
ج: تعديل الجاما يحسن التباين البصري، مما يجعل الهياكل التشريحية أسهل في الرؤية أثناء التحليل.

**س: هل يمكنني معالجة صور DICOM بلغات أخرى؟**  
ج: نعم—توفر Aspose.Imaging مكتبات لـ .NET، Java، ومنصات أخرى، مما يتيح التطوير عبر اللغات.

**س: هل هناك قيود عند العمل مع ملفات DICOM؟**  
ج: بعض ملفات DICOM تحتوي على بيانات وصفية واسعة أو ضغط مملوك؛ فهم معيار DICOM يساعد على تجنب المشكلات.

**س: أين يمكنني العثور على المزيد من دروس Aspose.Imaging؟**  
ج: استكشف [توثيق Aspose.Imaging](https://reference.aspose.com/imaging/java/) للحصول على أدلة إضافية، مراجع API، ومشاريع نموذجية.

## الخاتمة
باتباعك لهذا الدليل، أصبحت الآن تعرف **كيفية معالجة DICOM**، وتطبيق تصحيح الجاما، و**تحويل DICOM إلى BMP** باستخدام Aspose.Imaging للـ Java. هذه القدرة تُسهل سير عمل الصور الطبية، وتتيح لك إنشاء تمثيلات bitmap للتقارير، وتحليل الذكاء الاصطناعي، أو الأرشفة.

إذا واجهت أي تحديات، فإن المجتمع في [منتدى Aspose.Imaging](https://forum.aspose.com/) مكان رائع لطرح الأسئلة ومشاركة الأفكار.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-01-14  
**تم الاختبار مع:** Aspose.Imaging للـ Java 24.11 (الأحدث وقت الكتابة)  
**المؤلف:** Aspose