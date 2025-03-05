---
title: إنشاء صور WMF باستخدام Aspose.Imaging لـ Java
linktitle: إنشاء صور ملف تعريف WMF
second_title: Aspose.Imaging واجهة برمجة تطبيقات معالجة الصور لجافا
description: تعرف على كيفية إنشاء صور ملف تعريف WMF في Java باستخدام Aspose.Imaging. اتبع هذا الدليل المفصّل خطوة بخطوة للحصول على إمكانات قوية لإنشاء الصور.
type: docs
weight: 10
url: /ar/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/
---
هل تتطلع إلى إنشاء صور WMF (ملف تعريف Windows) باستخدام تطبيقات Java الخاصة بك؟ Aspose.Imaging for Java هي أداة قوية تسمح لك بإنشاء صور WMF بسهولة. في هذا الدليل المفصّل خطوة بخطوة، سنرشدك خلال عملية استخدام Aspose.Imaging for Java لإنشاء صور ملف تعريف WMF. 

## المتطلبات الأساسية

قبل البدء، تأكد من توفر المتطلبات الأساسية التالية:

- تم إعداد بيئة تطوير Java على جهاز الكمبيوتر الخاص بك.
-  تم تثبيت Aspose.Imaging لمكتبة Java. يمكنك تنزيله من[موقع إلكتروني](https://releases.aspose.com/imaging/java/).
- المعرفة الأساسية ببرمجة جافا.

## حزم الاستيراد

أولاً، قم باستيراد الحزم اللازمة لتطبيق Java الخاص بك لاستخدام Aspose.Imaging for Java:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.color.*;
import com.aspose.imaging.coreexceptions.ImageLoadException;
import com.aspose.imaging.imageoptions.WmfOptions;
import com.aspose.imaging.internal.system.drawing.*;
import com.aspose.imaging.internal.system.drawing.imaging.*;
import com.aspose.imaging.pen.*;
import com.aspose.imaging.system.drawing.*;
```

## الخطوة 1: إنشاء قماش

 للبدء في إنشاء صورة WMF الخاصة بك، تحتاج إلى إنشاء لوحة قماشية يمكنك من خلالها رسم الأشكال. ال`WmfRecorderGraphics2D` يوفر لك الفصل هذه اللوحة القماشية. إليك كيفية إنشاء مثيل له:

```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

في الكود أعلاه، نحدد أبعاد اللوحة القماشية (100 × 100) والدقة (96 نقطة في البوصة).

## الخطوة 2: تعيين لون الخلفية

 بعد ذلك، حدد لون الخلفية لقماشك. يمكنك استخدام ال`setBackgroundColor` طريقة ضبط لون الخلفية:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

في هذا المثال، قمنا بتعيين لون الخلفية إلى الدخان الأبيض.

## الخطوة 3: تحديد القلم والفرشاة

لرسم الأشكال على القماش، تحتاج إلى تحديد قلم وفرشاة. يستخدم القلم لرسم الخطوط العريضة، وتستخدم الفرشاة لملء الأشكال. إليك كيفية إنشاء قلم وفرشاة صلبة:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

في هذا الكود، نقوم بإنشاء قلم أزرق وفرشاة صلبة باللون الأصفر والأخضر.

## الخطوة 4: ملء ورسم الأشكال

الآن، دعونا نملأ ونرسم بعض الأشكال الأساسية على القماش. سنبدأ بالمضلع:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

هنا، نقوم بملء ورسم مضلع باستخدام القلم والفرشاة المحددين. يمكنك ضبط الإحداثيات والأشكال حسب الحاجة.

## الخطوة 5: استخدم HatchBrush

 لإضافة مواد إلى الأشكال الخاصة بك، يمكنك استخدام`HatchBrush`. على سبيل المثال:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

في هذا الكود، نقوم بإنشاء فرشاة متقاطعة باللونين الأبيض والفضي.

## الخطوة 6: ملء ورسم القطع الناقص

دعونا نملأ ونرسم شكلًا ناقصًا على القماش:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

يمكنك ضبط موضع وحجم القطع الناقص حسب الحاجة.

## الخطوة 7: ارسم القوس والبيزير المكعب

من الممكن أيضًا رسم أشكال أكثر تعقيدًا. إليك كيفية رسم قوس ومنحنى بيزيير المكعب:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

في الكود أعلاه، نرسم أولاً قوسًا بنمط الخط المنقط، ثم نرسم منحنى بيزييه المكعب بقلم أحمر خالص.

## الخطوة 8: إضافة الصور

يمكنك أيضًا إضافة صور إلى ملف تعريف WMF الخاص بك. هيريس كيفية القيام بذلك:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

في هذه الخطوة، نقوم بتحميل صورة ووضعها على اللوحة القماشية عند الإحداثيات المحددة (50، 50).

## الخطوة 9: رسم الخطوط والفطيرة

لإضافة خطوط وأشكال دائرية، يمكنك اتباع الأمثلة التالية:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

هنا، نرسم خطًا ونملأ/نرسم شكل دائري باستخدام القلم والفرشاة المحددين.

## الخطوة 10: رسم الخطوط المتعددة والنص

تعد إضافة النص والخطوط المتعددة أمرًا بسيطًا:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

يمكنك تخصيص الخط والنص ونقاط الخطوط المتعددة حسب الحاجة.

## الخطوة 11: احفظ صورة WMF

بمجرد إنشاء صورة WMF الخاصة بك، فقد حان الوقت لحفظها:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

سيحفظ هذا الرمز صورة WMF في الدليل المحدد.

هذا كل شيء! لقد نجحت في إنشاء صورة ملف تعريف WMF باستخدام Aspose.Imaging for Java.

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا كيفية إنشاء صور ملف تعريف WMF باستخدام Aspose.Imaging for Java. لقد قمنا بتغطية المتطلبات الأساسية اللازمة، والحزم المستوردة، وقدمنا تعليمات خطوة بخطوة لرسم الأشكال المختلفة، وإضافة الأنسجة، وإدراج الصور، وحفظ الصورة النهائية. يقدم Aspose.Imaging for Java مجموعة قوية من الأدوات لمعالجة الصور وإنشائها، مما يجعلها مصدرًا قيمًا لتطبيقات Java الخاصة بك.

## الأسئلة الشائعة

### س1: ما هو تنسيق صورة WMF؟

A1: WMF يرمز إلى Windows Metafile، وهو تنسيق رسومات متجهة يستخدم لتخزين الصور والرسومات والبيانات الرسومية الأخرى. يتم استخدامه بشكل شائع في تطبيقات Windows ويمكن توسيع نطاقه بسهولة دون فقدان الجودة.

### س2: أين يمكنني تنزيل Aspose.Imaging لـ Java؟

 ج٢: يمكنك تنزيل Aspose.Imaging for Java من ملف[موقع إلكتروني](https://releases.aspose.com/imaging/java/).

### س3: هل أحتاج إلى مهارات برمجة متقدمة لاستخدام Aspose.Imaging لـ Java؟

ج3: على الرغم من أن المعرفة الأساسية ببرمجة Java مطلوبة، فإن Aspose.Imaging for Java يوفر واجهة برمجة تطبيقات سهلة الاستخدام تعمل على تبسيط مهام معالجة الصور وإنشائها.

### س4: هل يمكنني استخدام Aspose.Imaging for Java لأغراض تجارية؟

 ج4: نعم، يوفر Aspose.Imaging for Java تراخيص تجارية للشركات والمطورين. يمكنك شراء ترخيص من[هنا](https://purchase.aspose.com/buy).

### س5: أين يمكنني الحصول على الدعم أو طرح الأسئلة حول Aspose.Imaging for Java؟

 ج5: يمكنك العثور على الدعم والتفاعل مع مجتمع Aspose على[Aspose.منتديات التصوير](https://forum.aspose.com/).