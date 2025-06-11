---
"description": "حسّن صورك بإضافة علامة مائية قطرية باستخدام Aspose.Imaging لجافا. اتبع هذا الدليل خطوة بخطوة لإنشاء صور مذهلة بعلامة مائية بكل سهولة."
"linktitle": "وضع علامة مائية قطرية على الصور"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Java Aspose.Imaging"
"title": "إضافة علامات مائية قطرية للصور باستخدام Aspose.Imaging لـ Java"
"url": "/ar/java/image-processing-and-enhancement/diagonal-image-watermarking/"
"weight": 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# إضافة علامات مائية قطرية للصور باستخدام Aspose.Imaging لـ Java


إذا كنت ترغب في تحسين صورك بإضافة علامة مائية قطرية أنيقة، فإن Aspose.Imaging for Java هنا لمساعدتك. في هذا الدليل المفصل، سنشرح لك عملية إضافة علامة مائية نصية بزاوية 45 درجة إلى صورة JPG موجودة. لستَ بحاجة إلى أن تكون خبيرًا في جافا أو معالجة الصور لمتابعة الخطوات، فسنُقسّم كل مثال إلى عدة خطوات لضمان تحقيق نتائج احترافية بسهولة.

## المتطلبات الأساسية

قبل أن نغوص في عالم العلامات المائية المثير للصور، ستحتاج إلى بعض الأشياء في مكانها:

1. Aspose.Imaging لجافا: تأكد من تثبيت Aspose.Imaging لجافا. يمكنك العثور على رابط التنزيل. [هنا](https://releases.aspose.com/imaging/java/).

2. بيئة تطوير Java: يجب أن يكون لديك بيئة تطوير Java عاملة تم إعدادها على جهاز الكمبيوتر الخاص بك.

3. إضافة علامة مائية إلى الصورة: جهّز الصورة التي تريد إضافة علامة مائية إليها، واحفظها في مجلد. يمكنك استخدام صورة نموذجية لهذا البرنامج التعليمي.

## استيراد الحزم

أولاً، استورد الحزم اللازمة لتجهيز مشروع جافا لإضافة العلامة المائية على الصور. فيما يلي الحزم الأساسية التي تحتاج إلى تضمينها:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## الخطوة 1: تحميل صورة موجودة

حمّل الصورة التي تريد إضافة علامة مائية إليها. في هذا المثال، نفترض أن لديك صورة JPG باسم "SampleTiff1.tiff" في مجلد "ModifyingImages".

```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// تحميل صورة JPG موجودة
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // بقية الكود يذهب هنا
}
```

## الخطوة 2: تحضير النصوص والرسومات الخاصة بالعلامة المائية

الآن، دعنا نعلن عن نص العلامة المائية الخاصة بك ونقوم بإعداد الرسومات الخاصة بالعلامة المائية.

```java
// إعلان كائن سلسلة مع نص العلامة المائية
String theString = "45 Degree Rotated Text";

// إنشاء وتفعيل مثيل لفئة الرسومات
Graphics graphics = new Graphics(image);

// تهيئة كائن SizeF لتخزين حجم الصورة
Size sz = graphics.getImage().getSize();
```

## الخطوة 3: تحديد الخط والفرشاة

حدّد نوع الخط والفرشاة للعلامة المائية. يمكنك تخصيص الخط والحجم والنمط بما يناسب تفضيلاتك.

```java
// إنشاء مثيل للخط، وتهيئته باستخدام وجه الخط وحجمه ونمطه
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// إنشاء مثيل لـ SolidBrush وتعيين خصائصه المختلفة
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## الخطوة 4: تنسيق النص الخاص بك

قم بتحديد تنسيق نص العلامة المائية، بما في ذلك محاذاة وأعلام التنسيق.

```java
// تهيئة كائن من فئة StringFormat وتعيين خصائصه المختلفة
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## الخطوة 5: تطبيق التحويل

أنشئ مصفوفة تحويل لتحديد موضع نص العلامة المائية وتدويره. في هذا المثال، سندوّر النص بزاوية 45 درجة.

```java
// إنشاء كائن من فئة Matrix للتحويل
Matrix matrix = new Matrix();
// أولاً الترجمة ثم التدوير
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// ضبط التحويل من خلال المصفوفة
graphics.setTransform(matrix);
```

## الخطوة 6: ارسم واحفظ

الآن، حان الوقت لإضافة النص إلى الصورة، وحفظ الصورة التي تحمل العلامة المائية في الموقع المطلوب.

```java
// ارسم الخيط على الصورة
graphics.drawString(theString, font, brush, 0, 0, format);

// حفظ الإخراج على القرص
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

تهانينا! لقد نجحت في إضافة علامة مائية قطرية إلى صورتك باستخدام Aspose.Imaging لجافا.

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية تحسين صورك بإضافة علامة مائية قطرية باستخدام Aspose.Imaging لجافا. إنها أداة فعّالة لإضافة لمسة احترافية إلى صورك. بخطوات بسيطة، يمكنك إنشاء صور مذهلة بعلامة مائية مميزة.

## الأسئلة الشائعة

### س1: هل Aspose.Imaging لـ Java مناسب للمبتدئين؟

ج١: بالتأكيد! يوفر Aspose.Imaging لجافا واجهة سهلة الاستخدام ووثائق شاملة. حتى المبتدئين يمكنهم البدء بسرعة في معالجة الصور.

### س2: هل يمكنني تخصيص نص العلامة المائية وأسلوبها؟

ج2: نعم، يمكنك بسهولة تخصيص نص العلامة المائية والخط والحجم واللون وزاوية الدوران لتتناسب مع تفضيلاتك وعلامتك التجارية.

### س3: هل يدعم Aspose.Imaging for Java تنسيقات الصور الأخرى إلى جانب JPG؟

ج3: نعم، يدعم Aspose.Imaging for Java مجموعة واسعة من تنسيقات الصور، بما في ذلك BMP وPNG وGIF والمزيد.

### س4: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Imaging لنظام Java؟

ج٤: نعم، يمكنك تجربة Aspose.Imaging لجافا بنسخة تجريبية مجانية. احصل عليه. [هنا](https://releases.aspose.com/).

### س5: أين يمكنني العثور على المساعدة أو الدعم لـ Aspose.Imaging لـ Java؟

A5: إذا كانت لديك أي أسئلة أو كنت بحاجة إلى مساعدة، تفضل بزيارة منتدى دعم Aspose.Imaging for Java [هنا](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}