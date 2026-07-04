---
date: 2026-01-24
description: تعلم كيفية تحويل OTG إلى PDF باستخدام Aspose.Imaging للغة Java. يوضح
  لك هذا الدليل خطوة بخطوة كيفية حفظ الصورة كملف PDF ومعالجة الصور بكفاءة.
linktitle: OTG File Format Support
second_title: Aspose.Imaging Java Image Processing API
title: تحويل OTG إلى PDF باستخدام Aspose.Imaging للغة Java
url: /ar/java/metafile-and-vector-image-handling/otg-file-format-support/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# تحويل OTG إلى PDF باستخدام Aspose.Imaging للـ Java

إذا كنت بحاجة إلى **تحويلكتبة معالجة سريعة
- **ماذا يعني “تحويل OTG إلى PDF”？** يحول قالب رسم مستند مفتوح إلى مستندة كصفحات مُرصَّصة.  
- **ما هي المكتبة التي تتعامل مع ذلك؟** Aspose.Imaging للـ Java، مكتبة **java image processing library** قوية.  
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تكفي للتطوير؛ يلزم ترخيص تجاري للإنتاج.  
- **هل يمكنني أيضًا إنشاء ملفات PNG؟** نعم – يمكن لنفس الكود **save image as PDF** و **save image as PNG** في تشغيل واحد.  
- **ما نسخة Java المطلوبة؟** Java 8 أو أعلى (أي JDK يدعم المكتبة).

## ما هو “تحويل OTG إلى PDF”؟
يعني تحويل ملف OTG إلى PDF تحميل مستند OTG، رَصْصَة كل صفحة، وكتابة النتيجة إلى حاوية PDF. هذا مفيد عندما تحتاج إلى مشاركة الرسومات مع مستخدمين لا يملكون سوى عارضات PDF.

## لماذا نستخدم Aspose.Imaging للـ Java في هذه المهمة؟
- **دعم كامل للصيغ** – يتعامل مع OTG و PNG و PDF والعديد من الصيغ الأخرى مباشرة.  
- **API بسيط** – لا حاجة للتعامل مع كود الرسومات منخفض المستوى؛ بضع أسطر تقوم بالعمل الشاق.  
- **متعدد المنصات** – يعمل على أي نظام تشغيل يدعم Java، مما يجعله مثاليًا للمعالجة على الخادم.  
- **الأداء** – رَصْصَة محسّنة تضمن أن يكون PDF الناتج واضحًا دون حجم ملف مفرط.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

### 1. مجموعة تطوير Java (JDK)
JDK متوافق (Java 8+). Aspose.Imaging يعمل على أي بيئة تشغيل Java قياسية.

### 2. مكتبة Aspose.Imaging للـ Java
حمّل أحدث مكتبة من الموقع الرسمي: [Download Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/).

### 3. دليل المستندات
أنشئ مجلدًا على جهازك حيث سيتواجد ملف OTG المصدر والملفات الناتجة. تذكر المسار المطلق – سنشير إليه في الكود.

## استيراد الحزم

أضف الاستيرادات المطلوبة في أعلى ملف Java الخاص بك حتى يعرف المترجم أين يجد الفئات:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Size;
import com.aspose.imaging.imageoptions.ImageOptionsBase;
import com.aspose.imaging.imageoptions.otg.OtgRasterizationOptions;
import com.aspose.imaging.imageoptions.pdf.PdfOptions;
import com.aspose.imaging.imageoptions.png.PngOptions;
```

## دليل خطوة بخطوة لتحويل OTG إلى PDF

### الخطوة 1: تعريف دليل البيانات
وجّه المكتبة إلى المجلد الذي يحتوي على ملف OTG الخاص بك.

```java
String dataDir = "Your Document Directory" + "OTG/";
```

استبدل `"Your Document Directory"` بالمسار الفعلي على جهازك.

### الخطوة 2: تحديد اسم ملف OTG
أخبر البرنامج أي ملف OTG يجب معالجته.

```java
String fileName = "VariousObjectsMultiPage.otg";
```

لا تتردد في استخدام أي ملف OTG لديك.

### الخطوة 3: إعداد خيارات الإخراج
أنشئ مصفوفة تخبر Aspose.Imaging بإنشاء ملفات PNG و PDF معًا.

```java
ImageOptionsBase[] options = { new PngOptions(), new PdfOptions() };
```

هذا يتيح لك **create PDF from image** وإنتاج صور مصغرة PNG في تشغيل واحد.

### الخطوة 4: تحميل صورة OTG
افتح ملف OTG باستخدام الطريقة `Image.load`.

```java
try (Image image = Image.load(inputFileName))
```

يجب أن يكون `inputFileName` هو المسار الكامل إلى ملف OTG (مثال: `dataDir + fileName`).

### الخطوة 5: تكوين خيارات الترصيص
حدد حجم الرَصْصَة بحيث يتطابق الناتج مع الأبعاد الأصلية.

```java
OtgRasterizationOptions otgRasterizationOptions = new OtgRasterizationOptions();
otgRasterizationOptions.setPageSize(Size.to_SizeF(image.getSize()));
```

هذه الخيارات حاسمة للحصول على عرض دقيق عندما تقوم **convert OTG to PDF**.

### الخطوة 6: حفظ الصورة المحوَّلة
قم بالتكرار عبر مصفوفة الخيارات واكتب كل ملف ناتج.

```java
image.save("Your Document Directory" + "output" + fileExt, item);
```

- يمكن أن يكون `"output"` أي اسم تفضله.  
- يتم تعيين `fileExt` تلقائيًا إلى `.png` أو `.pdf` بناءً على العنصر الحالي `item` في الحلقة.

عند انتهاء الحلقة، ستحصل على نسخة PDF ونسخة PNG من الرسم الأصلي بصيغة OTG.

## المشكلات الشائعة & استكشاف الأخطاء

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| **NullPointerException on `image.getSize()`** | لم يتم تحميل ملف OTG بشكل صحيح (مسار خاطئ). | تحقق من أن `inputFileName` يشير إلى ملف OTG الفعلي. |
| **Generated PDF is blank** | لم تُضبط خيارات الرَصْصَة أو كان هناك عدم توافق في حجم الصفحة. | تأكد من أن `otgRasterizationOptions.setPageSize(...)` يستخدم حجم الصورة. |
| **Output file not created** | عدم وجود أذونات كتابة على المجلد المستهدف. | شغّل البرنامج بأذونات نظام ملفات كافية أو اختر دليلًا قابلًا للكتابة. |

## الأسئلة المتكررة

**س: ما هو Aspose.Imaging للـ Java؟**  
ج: Aspose.Imaging للـ Java هي **java image processing library** تمكّن المطورين من العمل مع أكثر من 100 صيغة صورة، إجراء التحويلات، وتطبيق الرَصْصَة المتقدمة.

**س: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.Imaging للـ Java؟**  
ج: يمكنك الوصول إلى الوثائق هنا: [Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/).

**س: هل تتوفر نسخة تجريبية مجانية من Aspose.Imaging للـ Java؟**  
ج: نعم، يمكنك تنزيل نسخة تجريبية مجانية من Aspose.Imaging للـ Java من [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Imaging للـ Java؟**  
ج: يمكنك الحصول على ترخيص مؤقت بزيارة [this link](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني طلب الدعم والمساعدة لـ Aspose.Imaging للـ Java؟**  
ج: إذا كان لديك أي أسئلة أو واجهت مشاكل، يمكنك زيارة منتدى الدعم الخاص بـ Aspose.Imaging للـ Java على [Aspose Forum](https://forum.aspose.com/).

### أسئلة سريعة إضافية

**س: هل يمكنني استخدام هذا الكود **save image as PDF** لصيغ أخرى مثل JPEG؟**  
ج: بالتأكيد. استبدل ملف المصدر بملف JPEG واحتفظ بـ `PdfOptions` في مصفوفة `options`؛ ستتعامل المكتبة مع التحويل.

**س: هل يدعم Aspose.Imaging معالجة دفعة من ملفات OTG متعددة؟**  
ج: نعم. ضع منطق التحميل والحفظ داخل حلقة تتكرر على قائمة بأسماء الملفات.

## الخلاصة

الآن لديك وصفة كاملة وجاهزة للإنتاج **convert OTG to PDF** (وبشكل اختياري PNG) باستخدام Aspose.Imaging للـ Java. يتيح لك هذا النهج الاستفادة من محرك **java convert image formats** القوي، مما يسمح لك بـ **save image as PDF** ببضع أسطر من الشيفرة. لا تتردد في توسيع العينة لمعالجة ملفات متعددة، دمجها في خدمة ويب، أو الجمع بينها وبين منتجات Aspose الأخرى لإنشاء تدفقات عمل وثائق أكثر غنى.

---

**آخر تحديث:** 2026-01-24  
**تم الاختبار مع:** Aspose.Imaging للـ Java 24.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}