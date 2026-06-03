---
date: 2026-01-09
description: تعلم كيفية تحويل الصورة إلى ثنائية باستخدام Aspose.Imaging للغة Java.
  يغطي هذا الدليل تقنيات معالجة الصور في Java لتحويل DICOM إلى BMP.
linktitle: Bradley's Adaptive Threshold Binarization
second_title: Aspose.Imaging Java Image Processing API
title: كيفية تحويل الصورة إلى ثنائية باستخدام Aspose.Imaging لجافا
url: /ar/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحويل الصورة إلى ثنائية باستخدام Aspose.Imaging للـ Java

تلعب الصور دورًا حيويًا في العالم الرقمي، سواء على المواقع الإلكترونية أو في المستندات أو كجزء من تطبيقات مختلفة. إذا كنت تتساءل **كيف تقوم بتحويل الصورة إلى ثنائية** بكفاءة، خاصةً للأنماط الطبية مثل DICOM، فأنت في المكان الصحيح. تحويل الصورة إلى ثنائية يبسط الصورة بتحويلها إلى تمثيل أبيض‑أسود، وهو مثالي للتحليل اللاحق، أو OCR، أو تحسين التخزين. في هذا الدرس سنستعرض العملية بالكامل باستخدام خوارزمية Bradley’s Adaptive Threshold Binarization في Aspose.Imaging للـ Java.

## إجابات سريعة
- **ماذا يفعل التحويل إلى ثنائية؟** يحول كل بكسل إلى إما أسود أو أبيض بناءً على عتبة محددة.
- **ما هي أفضل مكتبة لمعالجة الصور في Java؟** Aspose.Imaging للـ Java توفر ميزات تجريبية قوية وخالية من الترخيص.
- **هل يمكنني معالجة ملفات DICOM مباشرة؟** نعم، Aspose.Imaging يمكنه تحميل DICOM وتصديره كـ BMP، PNG، إلخ.
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** يتطلب الاستخدام غير التجريبي ترخيصًا تجاريًا.
- **ما نسخة Java المدعومة؟** Java 8 وما فوق متوافقة بالكامل.

## ما هو تحويل الصورة إلى ثنائية؟
تحويل الصورة إلى ثنائية هو عملية تحويل صورة رمادية أو ملونة إلى صورة ثنائية حيث يكون كل بكسل إما 0 (أسود) أو 255 (أبيض). غالبًا ما تكون هذه الخطوة هي المرحلة الأولى في خطوط معالجة الصور الطبية، ومسح المستندات، ومهام الرؤية الحاسوبية.

## لماذا نستخدم Aspose.Imaging للـ Java؟
توفر Aspose.Imaging واجهة برمجة تطبيقات Pure‑Java **تقوم بتحميل DICOM**، وتطبق خوارزميات متقدمة مثل **Bradley’s Adaptive Threshold**، وتحفظ النتيجة بصيغ شائعة دون الحاجة إلى مكتبات أصلية خارجية. إنها مثالية **لمعالجة الصور الطبية**، **تحويل DICOM إلى BMP**، وغيرها من سير عمل Java.

## المتطلبات المسبقة

قبل الغوص في الشيفرة، تأكد من توفر ما يلي:

- **بيئة تطوير Java** – JDK 8 أو أحدث مثبتة.
- **Aspose.Imaging للـ Java** – حمّلها من الموقع الرسمي: [Download Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/).
- **صورة DICOM** – أي ملف DICOM تجريبي ترغب في تحويله إلى ثنائي.

الآن بعد أن تم إعداد كل شيء، لننتقل إلى التنفيذ.

## كيفية تحويل الصورة إلى ثنائية – دليل خطوة بخطوة

### استيراد الحزم
أولاً، استورد الفئات المطلوبة من Aspose.Imaging. يحدد هذا المقتطف أيضًا مسارات ملفات الإدخال والإخراج.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// Load a DICOM image in an instance of DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Binarize image with Bradley's adaptive threshold.
    image.binarizeBradley(10);
    // Save the resultant image.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

### الخطوة 1: تعريف المسارات
حدد مواقع ملف DICOM المصدر وملف BMP الوجهة. استبدل `"Your Document Directory"` بالمجلد الفعلي على نظامك.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

### الخطوة 2: تحميل صورة DICOM
استخدم Aspose.Imaging **لتحميل صورة dicom** في كائن `DicomImage`. يتيح لك هذا الكائن الوصول الكامل إلى بيانات البكسل وطرق المعالجة.

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // The image processing steps will go here.
}
```

### الخطوة 3: تنفيذ التحويل إلى ثنائية
طبق خوارزمية Bradley’s Adaptive Threshold. المتغير (`10` في هذا المثال) يتحكم في حساسية العتبة؛ يمكنك تجربة قيم مختلفة للحصول على أفضل نتيجة.

```java
image.binarizeBradley(10);
```

### الخطوة 4: حفظ الصورة الثنائية
أخيرًا، صدّر الصورة المعالجة. هنا نستخدم صيغة BMP، لكن Aspose.Imaging يدعم PNG، JPEG، TIFF، والعديد غيرها.

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## المشكلات الشائعة & استكشاف الأخطاء وإصلاحها

- **FileNotFoundException** – تأكد من أن مسار `dataDir` ينتهي بشرطة مائلة (`/`) وأن اسم ملف DICOM مطابق تمامًا.
- **OutOfMemoryError** – قد تتطلب ملفات DICOM الكبيرة زيادة حجم الذاكرة المخصصة للـ JVM (`-Xmx2g` أو أعلى).
- **عتبة غير صحيحة** – إذا كان الناتج مظلمًا جدًا أو فاتحًا جدًا، عدّل العدد الممرّر إلى `binarizeBradley()` (مثلاً 5‑15).

## الأسئلة المتكررة

### س1: ما هو DICOM ولماذا هو مهم في التصوير الطبي؟
**ج:** DICOM هو اختصار لـ Digital Imaging and Communications in Medicine. وهو المعيار العالمي لتخزين، نقل، ومعالجة الصور الطبية، مما يتيح التوافق بين الأجهزة والأنظمة.

### س2: هل يمكنني استخدام Aspose.Imaging للـ Java في مشاريعي التجارية؟
**ج:** نعم، Aspose.Imaging للـ Java يقدم نسخ تجريبية مجانية وتراخيص تجارية. يمكنك استكشاف الخيارات والحصول على الترخيص المناسب من [موقع Aspose](https://purchase.aspose.com/buy).

### س3: هل توجد تراخيص مؤقتة متاحة لأغراض الاختبار؟
**ج:** نعم، يمكنك الحصول على ترخيص مؤقت للاختبار وتقييم Aspose.Imaging للـ Java. زر [هذا الرابط](https://purchase.aspose.com/temporary-license/) لمزيد من المعلومات.

### س4: أين يمكنني طلب المساعدة أو مناقشة القضايا المتعلقة بـ Aspose.Imaging للـ Java؟
**ج:** للحصول على دعم المجتمع والنقاشات، يمكنك زيارة [منتدى Aspose.Imaging](https://forum.aspose.com/). إنه مكان رائع للحصول على إجابات أسئلتك والتواصل مع مستخدمين آخرين.

### س5: هل Aspose.Imaging للـ Java مناسب لمعالجة الصور في تطبيقات Java أخرى؟
**ج:** بالتأكيد. تعمل المكتبة جيدًا في تطبيقات الويب، البرامج المكتبية، أدوات المعالجة الدفعية، وأكثر، مع توفير واجهة برمجة تطبيقات موحدة عبر المنصات.

## الخلاصة
لقد تعلمت الآن **كيفية تحويل الصورة إلى ثنائية** باستخدام Aspose.Imaging للـ Java مع خوارزمية Bradley’s Adaptive Threshold. هذه التقنية ذات قيمة خاصة **في معالجة الصور الطبية**، حيث تمكنك من تحويل ملفات DICOM إلى صيغ BMP خفيفة (أو صيغ أخرى) للتحليل أو التخزين. استمر في تجربة عتبات مختلفة واستكشف باقي ميزات Aspose.Imaging الغنية.

لمزيد من التفاصيل حول معالجة الصور، اطلع على الوثائق الرسمية: [Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/).

---

**آخر تحديث:** 2026-01-09  
**تم الاختبار مع:** Aspose.Imaging للـ Java 24.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}