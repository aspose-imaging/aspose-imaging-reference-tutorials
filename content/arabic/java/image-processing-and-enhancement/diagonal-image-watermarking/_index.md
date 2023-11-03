---
title: العلامة المائية للصورة القطرية باستخدام Aspose.Imaging لـ Java
linktitle: العلامة المائية للصورة القطرية
second_title: Aspose.Imaging واجهة برمجة تطبيقات معالجة الصور لجافا
description: قم بتحسين صورك باستخدام علامة مائية قطرية باستخدام Aspose.Imaging for Java. اتبع هذا الدليل التفصيلي خطوة بخطوة وقم بإنشاء صور مذهلة تحمل علامة مائية دون عناء.
type: docs
weight: 14
url: /ar/java/image-processing-and-enhancement/diagonal-image-watermarking/
---

إذا كنت تتطلع إلى تحسين صورك باستخدام علامة مائية قطرية أنيقة، فإن Aspose.Imaging for Java موجود لمساعدتك. في هذا الدليل التفصيلي، سنرشدك خلال عملية إضافة علامة مائية نصية مدورة بزاوية 45 درجة إلى صورة JPG موجودة. لا تحتاج إلى أن تكون خبيرًا في Java أو معالجة الصور لتتمكن من المتابعة - سنقوم بتقسيم كل مثال إلى خطوات متعددة للتأكد من أنه يمكنك تحقيق نتائج احترافية بسهولة.

## المتطلبات الأساسية

قبل أن نتعمق في عالم العلامات المائية للصور المثير، ستحتاج إلى بعض الأشياء:

1.  Aspose.Imaging for Java: تأكد من تثبيت Aspose.Imaging for Java. يمكنك العثور على رابط التحميل[هنا](https://releases.aspose.com/imaging/java/).

2. بيئة تطوير Java: يجب أن يكون لديك بيئة تطوير Java عاملة معدة على جهاز الكمبيوتر الخاص بك.

3. صورة إلى علامة مائية: قم بإعداد الصورة التي تريد وضع علامة مائية عليها وقم بتخزينها في الدليل. يمكنك استخدام صورة عينة لهذا البرنامج التعليمي.

## حزم الاستيراد

أولاً، قم باستيراد الحزم اللازمة لتجهيز مشروع Java الخاص بك لوضع العلامات المائية على الصور. فيما يلي الحزم الأساسية التي تحتاج إلى تضمينها:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## الخطوة 1: تحميل صورة موجودة

قم بتحميل الصورة التي تريد وضع علامة مائية عليها. في هذا المثال، نفترض أن لديك صورة JPG باسم "SampleTiff1.tiff" في دليل "ModifyingImages".

```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// قم بتحميل صورة JPG موجودة
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // بقية الكود يذهب هنا
}
```

## الخطوة 2: إعداد نص العلامة المائية والرسومات

الآن، دعنا نعلن عن نص العلامة المائية ونقوم بإعداد الرسومات الخاصة بالعلامة المائية.

```java
// قم بتعريف كائن سلسلة باستخدام نص العلامة المائية
String theString = "45 Degree Rotated Text";

// إنشاء وتهيئة مثيل لفئة الرسومات
Graphics graphics = new Graphics(image);

// قم بتهيئة كائن SizeF لتخزين حجم الصورة
Size sz = graphics.getImage().getSize();
```

## الخطوة 3: تحديد الخط والفرشاة

اضبط الخط والفرشاة للعلامة المائية الخاصة بك. يمكنك تخصيص الخط والحجم والنمط ليتناسب مع تفضيلاتك.

```java
// قم بإنشاء مثيل للخط، وقم بتهيئته باستخدام Font Face، وSize، وStyle
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// قم بإنشاء مثيل لـ SolidBrush وقم بتعيين خصائصه المختلفة
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## الخطوة 4: تنسيق النص الخاص بك

حدد تنسيق نص العلامة المائية، بما في ذلك علامات المحاذاة والتنسيق.

```java
// تهيئة كائن من فئة StringFormat وتعيين خصائصه المختلفة
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## الخطوة 5: تطبيق التحول

قم بإنشاء مصفوفة تحويل لتحديد موضع نص العلامة المائية وتدويره. في هذا المثال، سنقوم بتدوير النص بمقدار 45 درجة.

```java
// قم بإنشاء كائن من فئة Matrix للتحويل
Matrix matrix = new Matrix();
//أولا الترجمة ثم التناوب
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// اضبط التحويل من خلال المصفوفة
graphics.setTransform(matrix);
```

## الخطوة 6: الرسم والحفظ

الآن، حان الوقت لإضافة النص إلى الصورة، وحفظ الصورة ذات العلامة المائية في الموقع الذي تريده.

```java
// ارسم السلسلة على الصورة
graphics.drawString(theString, font, brush, 0, 0, format);

// حفظ الإخراج على القرص
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

تهانينا! لقد نجحت في إضافة علامة مائية قطرية إلى صورتك باستخدام Aspose.Imaging for Java.

## خاتمة

في هذا البرنامج التعليمي، تعلمنا كيفية تحسين صورك باستخدام علامة مائية قطرية باستخدام Aspose.Imaging for Java. إنها أداة قوية لإضافة لمسة احترافية إلى صورك. من خلال بضع خطوات بسيطة، يمكنك إنشاء صور مذهلة تحمل علامة مائية متميزة عن بقية الصور.

## الأسئلة الشائعة

### س1: هل Aspose.Imaging for Java مناسب للمبتدئين؟

ج1: بالتأكيد! يوفر Aspose.Imaging for Java واجهة سهلة الاستخدام ووثائق شاملة. حتى المبتدئين يمكنهم البدء بسرعة في معالجة الصور.

### س2: هل يمكنني تخصيص نص العلامة المائية ونمطها؟

ج2: نعم، يمكنك بسهولة تخصيص نص العلامة المائية والخط والحجم واللون وزاوية التدوير لتتناسب مع تفضيلاتك وعلامتك التجارية.

### س3: هل يدعم Aspose.Imaging for Java تنسيقات الصور الأخرى إلى جانب JPG؟

ج3: نعم، يدعم Aspose.Imaging for Java نطاقًا واسعًا من تنسيقات الصور، بما في ذلك BMP وPNG وGIF والمزيد.

### س4: هل هناك إصدار تجريبي مجاني متاح لـ Aspose.Imaging for Java؟

 ج4: نعم، يمكنك تجربة Aspose.Imaging for Java مع الإصدار التجريبي المجاني. احصل عليه[هنا](https://releases.aspose.com/).

### س5: أين يمكنني العثور على المساعدة أو الدعم فيما يتعلق بـ Aspose.Imaging for Java؟

 ج5: إذا كانت لديك أية أسئلة أو كنت بحاجة إلى المساعدة، قم بزيارة منتدى دعم Aspose.Imaging for Java[هنا](https://forum.aspose.com/).