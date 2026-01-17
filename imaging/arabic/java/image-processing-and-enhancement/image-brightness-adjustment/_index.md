---
date: 2026-01-17
description: تعلم كيفية ضبط سطوع الصور باستخدام Aspose.Imaging للـ Java. يوضح هذا
  الدرس لمعالجة الصور بلغة Java تحسين الصور بسهولة.
linktitle: Image Brightness Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: كيفية تعديل سطوع الصور باستخدام Aspose.Imaging للغة جافا
url: /ar/java/image-processing-and-enhancement/image-brightness-adjustment/
weight: 25
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تعديل سطوع الصور باستخدام Aspose.Imaging for Java

## المقدمة

تعديل السطوع هو أحد أكثر المهام شيوعًا في **معالجة الصور بجافا**. سواء كنت تُعدّ مسحات طبية، أو تُحسّن صور المنتجات، أو ببساطة تُحسّن الصور الشخصية، فإن معرفة **كيفية تعديل السطوع** بسرعة وبشكل موثوق يمكن أن توفر ساعات من العمل اليدوي. في هذا الدرس سنستعرض مثالًا كاملاً جاهزًا للإنتاج يُظهر **كيفية تعديل السطوع** باستخدام Aspose.Imaging for Java، مكتبة قوية تدعم العشرات من الصيغ مباشرةً.

## إجابات سريعة
- **ماذا يعني “تعديل السطوع”؟** يغيّر الإضاءة العامة لكل بكسل في الصورة.  
- **ما المكتبة المستخدمة؟** Aspose.Imaging for Java.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم ترخيص تجاري للإنتاج.  
- **الصيغ المدعومة؟** BMP، JPEG، PNG، DICOM، TIFF، والعديد غيرها.  
- **الوقت التقريبي للتنفيذ؟** حوالي 10 دقائق لكتابة سكريبت أساسي.

## ما هو “كيفية تعديل السطوع” في معالجة الصور بجافا؟

تعديل السطوع يعني تطبيق إزاحة موحدة على قيم شدة البكسل. في Aspose.Imaging يتم ذلك عبر الطريقة `adjustBrightness(int value)`، حيث القيم الموجبة تُضيء الصورة والقيم السالبة تُظلمها.

## لماذا نستخدم Aspose.Imaging لتحسين الصور بجافا؟

- **دعم واسع للصيغ** – يتعامل مع DICOM، BMP، JPEG، PNG، TIFF، وغيرها دون الحاجة إلى ترميزات إضافية.  
- **واجهة برمجة تطبيقات بسيطة** – استدعاءات سطر واحد للتعديلات الشائعة مثل السطوع، التباين، والجاما.  
- **محسّن للأداء** – يعمل بكفاءة على الصور الطبية الكبيرة والصور عالية الدقة.  
- **متعدد المنصات** – يعمل على أي JVM، مما يجعله مثاليًا لأنابيب المعالجة على الخادم.

## المتطلبات المسبقة

قبل الغوص في الكود، تأكد من توفر ما يلي:

1. **بيئة تطوير جافا** – ثبّت أحدث JDK من [الموقع](https://www.oracle.com/java/technologies/javase-downloads).  
2. **Aspose.Imaging for Java** – اتبع دليل التثبيت على موقع Aspose.Imaging عبر [Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/).  
3. **صورة تجريبية** – ملف DICOM (`image.dcm`) أو أي صيغة مدعومة أخرى تريد إضاءةها.  
4. **بيئة تطوير متكاملة** – Eclipse، IntelliJ IDEA، أو أي IDE جافا تفضله.

مع توافر هذه المتطلبات، لنبدأ كتابة الكود.

## استيراد الحزم

أولاً، استورد الفئات المطلوبة من Aspose.Imaging:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import com.aspose.imaging.imageoptions.BmpOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تعريف مسارات الملفات

حدد مواقع الإدخال والإخراج. استبدل `"Your Document Directory"` بالمجلد الفعلي على جهازك.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingBrightness_out.bmp";
```

### الخطوة 2: تحميل صورة DICOM

استخدم طريقة `Image.load` لقراءة ملف DICOM إلى الذاكرة.

```java
try (DicomImage image = (DicomImage) Image.load(inputFile)) {
    // Image is now ready for processing.
}
```

### الخطوة 3: تعديل السطوع

داخل كتلة `try`، استدعِ `adjustBrightness`. القيمة `50` تُضيء الصورة بشكل ملحوظ؛ استخدم أرقامًا سالبة لتظليلها.

```java
image.adjustBrightness(50);
```

> **نصيحة احترافية:** للحصول على تعديلات دقيقة، ابدأ بالقيم بين `-20` و`20`. جرّب مستويات مختلفة لتجنب فقدان التفاصيل في الإضاءات أو الظلال.

### الخطوة 4: حفظ الصورة الناتجة

أخيرًا، اكتب الصورة المعدلة إلى القرص باستخدام خيارات BMP (يمكنك اختيار صيغ أخرى حسب الحاجة).

```java
image.save(outputFile, new BmpOptions());
```

عند انتهاء البرنامج، سيحتوي الملف `AdjustingBrightness_out.bmp` على النسخة المُضيئة من صورة DICOM الأصلية.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **لم يتم إنشاء ملف الإخراج** | مسار غير صحيح أو نقص في صلاحيات الكتابة | تحقق من مسار `outputFile` وتأكد من وجود المجلد وصلاحية الكتابة. |
| **الصورة تبدو باهتة** | قيمة السطوع مرتفعة جدًا | قلل قيمة التعديل أو طبّق تصحيح التباين بعد الإضاءة. |
| **خطأ صيغة غير مدعومة** | محاولة تحميل صيغة لا يدعمها محمل DICOM | استخدم الفئة المناسبة (مثل `BmpImage`) للملفات غير DICOM. |

## الأسئلة المتكررة

### س1: هل Aspose.Imaging for Java مناسب لمهام معالجة الصور الاحترافية؟

ج1: نعم، Aspose.Imaging for Java مكتبة متعددة الاستخدامات صُممت للمعالجة الاحترافية للصور، وتوفر مجموعة واسعة من الميزات والخيارات.

### س2: هل يمكنني استخدام Aspose.Imaging for Java مع مكتبات جافا أخرى؟

ج2: بالتأكيد! يمكن دمج Aspose.Imaging for Java بسلاسة مع مكتبات وإطارات عمل جافا الأخرى.

### س3: ما هي صيغ الصور التي يدعمها Aspose.Imaging for Java؟

ج3: يدعم Aspose.Imaging for Java مجموعة واسعة من الصيغ، بما فيها BMP، JPEG، PNG، TIFF، GIF، وغيرها.

### س4: هل هناك نسخة تجريبية مجانية من Aspose.Imaging for Java؟

ج4: نعم، يمكنك تجربة Aspose.Imaging for Java بنسخة تجريبية مجانية. زر [هنا](https://releases.aspose.com/) للبدء.

### س5: أين يمكنني الحصول على الدعم أو المساعدة بخصوص Aspose.Imaging for Java؟

ج5: يمكنك العثور على المساعدة والانضمام إلى المجتمع عبر [منتدى Aspose.Imaging for Java](https://forum.aspose.com/).

## الخلاصة

في هذا **الدرس المتعلق بمعالجة الصور بجافا** عرضنا **كيفية تعديل السطوع** باستخدام Aspose.Imaging for Java. باتباع الخطوات الأربع المختصرة—استيراد الحزم، تعريف المسارات، تحميل الصورة، تعديل السطوع، وحفظ النتيجة—يمكنك دمج تحسين الصور بجافا بشكل قوي في أي تطبيق، سواء في أنابيب التصوير الطبي أو سير عمل صور التجارة الإلكترونية. جرّب قيم سطوع مختلفة، وادمجها مع تعديلات التباين أو الجاما، واكتشف الإمكانات الكاملة لبياناتك البصرية.

---

**آخر تحديث:** 2026-01-17  
**تم الاختبار مع:** Aspose.Imaging for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}