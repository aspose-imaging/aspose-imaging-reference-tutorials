---
date: 2026-01-09
description: تعلم كيفية إضافة علامة مائية إلى الصور باستخدام Aspose.Imaging للغة Java.
  يوضح هذا الدرس في معالجة الصور بلغة Java خطوة بخطوة كيفية إنشاء علامة مائية مائلة
  بسرعة.
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: كيفية إضافة علامة مائية – وضع علامة مائية مائلة على الصورة (جافا)
url: /ar/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة علامة مائية – وضع علامة مائية مائلة على الصورة (Java)

إذا كنت تبحث عن **كيفية إضافة علامة مائية** إلى صورك بزاوية مائلة أنيقة، فإن Aspose.Imaging for Java يجعل العملية سهلة. في هذا الدليل خطوة‑بخطوة سنستعرض إضافة علامة مائية نصية مائلة بزاوية 45 درجة إلى صورة JPG (أو أي صيغة مدعومة). لا تحتاج إلى أن تكون خبيرًا في Java – كل جزء مشروح بلغة بسيطة حتى تتمكن من تكرار النتيجة في دقائق.

## إجابات سريعة
- **ما المكتبة المستخدمة؟** Aspose.Imaging for Java  
- **ما الكلمة المفتاحية الأساسية التي يتم تغطيتها؟** كيفية إضافة علامة مائية  
- **الصيغ المدعومة للصور؟** JPEG, PNG, BMP, TIFF, GIF وأكثر  
- **كم عدد أسطر الكود المطلوبة؟** سبعة كتل كود مختصرة فقط  
- **هل أحتاج إلى رخصة للاختبار؟** نسخة تجريبية مجانية متاحة؛ الرخصة مطلوبة للإنتاج  

## ما معنى “كيفية إضافة علامة مائية” في معالجة الصور؟
إضافة علامة مائية تعني وضع نص أو رسومات شبه شفافة فوق الصورة لحماية الملكية أو لترويج العلامة التجارية. تكون العلامة المائية المائلة فعّالة بشكل خاص لأنها تغطي كامل الصورة وتكون أصعب في إزالتها.

## لماذا نستخدم Aspose.Imaging for Java؟
توفر Aspose.Imaging واجهة برمجة تطبيقات عالية المستوى تُجردك من التعامل مع بكسلات الصورة منخفضة المستوى، وتدعم عشرات الصيغ، وتعمل على أي بيئة تشغيل Java. تتيح لك التركيز على *ما* تريد تحقيقه—مثل إضافة علامة مائية مائلة—دون القلق بشأن تفاصيل صيغ الصور.

## المتطلبات المسبقة

قبل البدء، تأكد من توفر ما يلي:

1. **Aspose.Imaging for Java** – حمّل أحدث نسخة من الموقع الرسمي **[هنا](https://releases.aspose.com/imaging/java/)**.  
2. **بيئة تطوير Java** – JDK 8+ وأي IDE تفضله (IntelliJ, Eclipse, VS Code، إلخ).  
3. **صورة لتطبيق العلامة المائية** – ضع ملف JPG/TIFF/PNG تجريبي في مجلد ستشير إليه في الكود.

## استيراد الحزم

أولاً، استورد الفئات التي ستحتاجها. إبقاء الاستيرادات معًا يجعل الكود أسهل للقراءة والصيانة.

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## الخطوة 1: تحميل صورة موجودة

نبدأ بتحميل الصورة المصدر. طريقة `Image.load` تكتشف الصيغة تلقائيًا.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **نصيحة احترافية:** ضع كائن `Image` داخل عبارة `try‑with‑resources` (كما هو موضح) لتتم إزالته تلقائيًا، مما يمنع تسرب الذاكرة.

## الخطوة 2: إعداد نص العلامة المائية والرسومات

أنشئ كائن `Graphics` مرتبط بالصورة المحملة واحفظ حجم الصورة لحسابات لاحقة.

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## الخطوة 3: تعريف الخط والفرشاة

اختر خطًا بارزًا وفرشاة تحدد لون العلامة المائية وشفافيتها. عدّل الشفافية لجعل العلامة شبه شفافة.

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## الخطوة 4: تنسيق النص

حدد محاذاة وعلامات تنسيق بحيث يكون النص مركّزًا عند رسمه.

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## الخطوة 5: تطبيق التحويل

مصفوفة التحويل تسمح لنا بنقل الأصل إلى مركز الصورة ثم تدوير النص بزاوية ‑45° (عقارب الساعة).

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## الخطوة 6: الرسم والحفظ

أخيرًا، ارسم السلسلة على الصورة واكتب النتيجة إلى القرص.

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

عند فتح `AddDiagonalWatermarkToImage_out.jpg` ستظهر النص الأحمر شبه الشفاف مائلًا عبر مركز الصورة.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|---------|--------|-----|
| العلامة المائية باهتة جدًا | تم ضبط الشفافية على 0 (شفافة بالكامل) | زيادة الشفافية، مثال: `brush.setOpacity(0.5f);` |
| النص مقطوع عند الحواف | لم يتم توسيط الترجمة للصور غير المربعة | استخدم `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` كما هو موضح، ثم عدّل زاوية الدوران إذا لزم الأمر |
| خطأ في صيغة الصورة غير المدعومة | استخدام نسخة قديمة من Aspose.Imaging | حدّث إلى أحدث إصدار من Aspose.Imaging |

## الأسئلة المتكررة

### س1: هل Aspose.Imaging for Java مناسب للمبتدئين؟

**ج:** بالتأكيد! الواجهة سهلة الفهم، والوثائق تقدم أمثلة واضحة. حتى المطورين الجدد في معالجة الصور يمكنهم اتباع هذا الدليل وإنتاج نتائج احترافية بسرعة.

### س2: هل يمكنني تخصيص نص العلامة المائية والأسلوب؟

**ج:** نعم. غيّر المتغير `theString`، اختر `Font` مختلف، عدّل `brush.setColor(...)`، أو عدّل زاوية الدوران في المصفوفة لتتناسب مع هوية علامتك التجارية.

### س3: هل يدعم Aspose.Imaging for Java صيغ صور أخرى غير JPG؟

**ج:** نعم. المكتبة تعمل مع BMP, PNG, GIF, TIFF, PSD، والعديد غيرها. فقط وجه طريقة `Image.load` إلى الملف المناسب.

### س4: هل هناك نسخة تجريبية مجانية من Aspose.Imaging for Java؟

**ج:** نعم، يمكنك تجربة Aspose.Imaging for Java بنسخة تجريبية مجانية. احصل عليها **[هنا](https://releases.aspose.com/)**.

### س5: أين يمكنني الحصول على المساعدة أو الدعم لـ Aspose.Imaging for Java؟

**ج:** للأسئلة، تقارير الأخطاء، أو نصائح أفضل الممارسات، زر منتدى دعم Aspose.Imaging for Java **[هنا](https://forum.aspose.com/)**.

---

**آخر تحديث:** 2026-01-09  
**تم الاختبار مع:** Aspose.Imaging for Java 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}