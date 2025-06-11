---
"description": "تعلّم كيفية إنشاء صور ملفات تعريفية بصيغة WMF في جافا باستخدام Aspose.Imaging. اتبع هذا الدليل خطوة بخطوة للحصول على إمكانيات فعّالة لإنشاء الصور."
"linktitle": "إنشاء صور ملفات تعريف WMF"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Java Aspose.Imaging"
"title": "إنشاء صور WMF باستخدام Aspose.Imaging لـ Java"
"url": "/ar/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/"
"weight": 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء صور WMF باستخدام Aspose.Imaging لـ Java

هل ترغب في إنشاء صور WMF (ملفات تعريف Windows) باستخدام تطبيقات Java؟ Aspose.Imaging for Java أداة فعّالة تُمكّنك من إنشاء صور WMF بسهولة. في هذا الدليل المُفصّل، سنشرح لك عملية استخدام Aspose.Imaging for Java لإنشاء صور ملفات تعريف WMF. 

## المتطلبات الأساسية

قبل أن تبدأ، تأكد من توفر المتطلبات الأساسية التالية:

- بيئة تطوير Java تم إعدادها على جهاز الكمبيوتر الخاص بك.
- تم تثبيت مكتبة Aspose.Imaging لجافا. يمكنك تنزيلها من [موقع إلكتروني](https://releases.aspose.com/imaging/java/).
- المعرفة الأساسية ببرمجة جافا.

## استيراد الحزم

أولاً، قم باستيراد الحزم اللازمة لتطبيق Java الخاص بك لاستخدام Aspose.Imaging لـ Java:

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

## الخطوة 1: إنشاء لوحة قماشية

لبدء إنشاء صورة WMF الخاصة بك، ستحتاج إلى إنشاء لوحة قماشية يمكنك رسم الأشكال عليها. `WmfRecorderGraphics2D` توفر لك هذه الفئة هذه اللوحة. إليك كيفية إنشاء مثيل لها:

```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

في الكود أعلاه، قمنا بتحديد أبعاد القماش (100 × 100) والدقة (96 نقطة في البوصة).

## الخطوة 2: تعيين لون الخلفية

بعد ذلك، حدد لون خلفية لوحتك. يمكنك استخدام `setBackgroundColor` طريقة تعيين لون الخلفية:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

في هذا المثال، قمنا بتعيين لون الخلفية إلى الدخان الأبيض.

## الخطوة 3: تحديد القلم والفرشاة

لرسم الأشكال على القماش، عليك تحديد قلم وفرشاة. يُستخدم القلم لرسم الخطوط العريضة، بينما تُستخدم الفرشاة لملء الأشكال. إليك كيفية إنشاء قلم وفرشاة صلبة:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

في هذا الكود، قمنا بإنشاء قلم أزرق وفرشاة صلبة باللون الأصفر والأخضر.

## الخطوة 4: ملء ورسم الأشكال

الآن، لنملأ ونرسم بعض الأشكال الأساسية على اللوحة. سنبدأ بمضلع:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

هنا، نملأ ونرسم مضلعًا باستخدام القلم والفرشاة المحددين. يمكنك تعديل الإحداثيات والأشكال حسب الحاجة.

## الخطوة 5: استخدم HatchBrush

لإضافة نسيج إلى الأشكال الخاصة بك، يمكنك استخدام `HatchBrush`. على سبيل المثال:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

في هذا الكود، نقوم بإنشاء فرشاة متقاطعة بألوان الأبيض والفضي.

## الخطوة 6: املأ الشكل البيضاوي وارسمه

دعونا نملأ ونرسم شكلًا بيضاويًا على القماش:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

يمكنك تعديل موضع وحجم القطع الناقص حسب الحاجة.

## الخطوة 7: ارسم قوسًا ومكعبًا من بيزير

يُمكن أيضًا رسم أشكال أكثر تعقيدًا. إليك كيفية رسم قوس ومنحنى بيزير مكعب:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

في الكود أعلاه، نرسم أولاً قوسًا بنمط خط منقط، ثم نرسم منحنى بيزير مكعبًا بقلم أحمر متصل.

## الخطوة 8: إضافة الصور

يمكنك أيضًا إضافة صور إلى ملف WMF التعريفي. إليك الطريقة:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

في هذه الخطوة، نقوم بتحميل صورة ووضعها على القماش عند الإحداثيات المحددة (50، 50).

## الخطوة 9: ارسم الخطوط والفطيرة

لإضافة خطوط وأشكال دائرية، يمكنك اتباع الأمثلة التالية:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

هنا، نرسم خطًا ونملأ/نرسم شكل دائري باستخدام القلم والفرشاة المحددين.

## الخطوة 10: ارسم خطًا متعددًا ونصًا

إن إضافة النص والخطوط المتعددة أمر بسيط:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

يمكنك تخصيص الخط والنص ونقاط الخطوط المتعددة حسب الحاجة.

## الخطوة 11: حفظ صورة WMF

بمجرد إنشاء صورة WMF الخاصة بك، حان الوقت لحفظها:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

سيقوم هذا الكود بحفظ صورة WMF في الدليل المحدد.

هذا كل شيء! لقد نجحت في إنشاء صورة ملف تعريف WMF باستخدام Aspose.Imaging لـ Java.

## خاتمة

في هذا البرنامج التعليمي، استكشفنا كيفية إنشاء صور ملفات تعريفية بصيغة WMF باستخدام Aspose.Imaging لجافا. غطينا المتطلبات الأساسية اللازمة، والحزم المستوردة، وقدمنا تعليمات خطوة بخطوة لرسم أشكال مختلفة، وإضافة القوام، وإدراج الصور، وحفظ الصورة النهائية. يوفر Aspose.Imaging لجافا مجموعة قوية من الأدوات لمعالجة الصور وإنشائها، مما يجعله موردًا قيّمًا لتطبيقات جافا.

## الأسئلة الشائعة

### س1: ما هو تنسيق صورة WMF؟

ج١: WMF هو اختصار لـ Windows Metafile، وهو تنسيق رسومي متجهي يُستخدم لتخزين الصور والرسومات وغيرها من البيانات الرسومية. يُستخدم هذا التنسيق عادةً في تطبيقات Windows، ويمكن تعديل حجمه بسهولة دون فقدان الجودة.

### س2: أين يمكنني تنزيل Aspose.Imaging لـ Java؟

A2: يمكنك تنزيل Aspose.Imaging for Java من [موقع إلكتروني](https://releases.aspose.com/imaging/java/).

### س3: هل أحتاج إلى مهارات برمجة متقدمة لاستخدام Aspose.Imaging لـ Java؟

A3: على الرغم من أن معرفة برمجة Java الأساسية مطلوبة، فإن Aspose.Imaging for Java يوفر واجهة برمجة تطبيقات سهلة الاستخدام تعمل على تبسيط مهام معالجة الصور وإنشائها.

### س4: هل يمكنني استخدام Aspose.Imaging لـ Java لأغراض تجارية؟

ج٤: نعم، يُقدّم Aspose.Imaging for Java تراخيص تجارية للشركات والمطوّرين. يُمكنك شراء الترخيص من [هنا](https://purchase.aspose.com/buy).

### س5: أين يمكنني الحصول على الدعم أو طرح الأسئلة حول Aspose.Imaging لـ Java؟

A5: يمكنك العثور على الدعم والتفاعل مع مجتمع Aspose على [منتديات Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}