---
date: 2026-01-24
description: تعلم كيفية إنشاء صور WMF باستخدام Aspose.Imaging للغة Java – دليل خطوة
  بخطوة حول كيفية إنشاء ملفات WMF الميتافايل.
linktitle: Generate WMF Metafile Images
second_title: Aspose.Imaging Java Image Processing API
title: كيفية إنشاء صور WMF باستخدام Aspose.Imaging للـ Java
url: /ar/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء صور WMF باستخدام Aspose.Imaging للـ Java

هل ترغب في **تعلم كيفية إنشاء صور WMF (Windows Metafile)** باستخدام تطبيقات أداة قوية تتيح لك توليد صور WMF بسرعة وبشكل موثوق. في هذا الدليل خطوة‑بخطوة، سنرشدك إلى كل ما تحتاج معرفته **لإنشاء ملفات WMF**، من إعداد السطحـ Java. WMF (Windows Metafile) قياسي.  
- **كم يستغرق تشغيل المثال الأساسي؟** عادةً أقل من ثانية على جهاز كمبيوتر حديث.

## كيفية إنشاء صور WMF – نظرة عامة
يقدم هذا القسم صورة مختصرة لسير العمل: إنشاء سطح رسم، تنسيق الرسومات، إضافة أشكال أو صور، وأخيرًا حفظ ملف WMF. فهم العملية العامة يساعدك على تعديل المثال ليتناسب مع حالات الاستخدام الخاصة بك، مثل توليد المخططات، الأيقونات، أو عناصر واجهة المستخدم المخصصة.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

- بيئة تطوير Java (يفضل JDK 8 أو أعلى).  
- مكتبة Aspose.Imaging للـ Java مثبتة. يمكنك تحميلها من [الموقع الإلكتروني](https://releases.aspose.com/imaging/java/).  
- معرفة أساسية ببرمجة Java.

## استيراد الحزم

أولاً، استورد الحزم الضرورية لتطبيق Java الخاص بك لاستخدام Aspose.Imaging للـ Java:

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

## الخطوة 1: إنشاء سطح رسم

لبدء إنشاء صورة WMF الخاصة بك، تحتاج إلى سطح رسم يمكنك رسم الأشكال عليه. توفر لك فئة `WmfRecorderGraphics2D` هذا السطح. إليك كيفية إنشاء كائن منها:

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

في الشيفرة أعلاه، نحدد أبعاد السطح (100 × 100) والدقة (96 DPI).

## الخطوة 2: تعيين لون الخلفية

بعد ذلك، حدد لون الخلفية لسطح الرسم. يمكنك استخدام طريقة `setBackgroundColor` لتعيين لون الخلفية:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

في هذا المثال نضبط لون الخلفية إلى **white smoke**.

## الخطوة 3: تعريف القلم والفرشاة

لرسم الأشكال على السطح، تحتاج إلى تعريف قلم وفرشاة. القلم يُستخدم لرسم الحدود، والفرشاة تُستخدم لتعبئة الأشكال. إليك كيفية إنشاء قلم وفرشاة صلبة:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

في هذه الشيفرة، ننشئ قلمًا أزرق وفرشاة صلبة بلون أصفر‑أخضر.

## الخطوة 4: تعبئة ورسم الأشكال

الآن، لنقم بتعبئة ورسم بعض الأشكال الأساسية على السطح. سنبدأ بمضلع:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

هنا نقوم بتعبئة ورسم مضلع باستخدام القلم والفرشاة المحددين. عدّل الإحداثيات لإنشاء أي شكل تحتاجه.

## الخطوة 5: استخدام HatchBrush

لإضافة أنماط نسيجية إلى الأشكال، يمكنك استخدام `HatchBrush`. مثال:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

في هذه الشيفرة، ننشئ فرشاة **cross‑hatch** بألوان أبيض وفضي.

## الخطوة 6: تعبئة ورسم إهليلج

لنقم بتعبئة ورسم إهليلج على السطح:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

يمكنك تعديل موضع وحجم الإهليلج حسب الحاجة.

## الخطوة 7: رسم قوس ومنحنى بيزيه مكعب

يمكنك أيضًا رسم أشكال أكثر تعقيدًا. إليك كيفية رسم قوس ومنحنى بيزيه مكعب:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

في الشيفرة أعلاه، نرسم أولاً قوسًا بنمط خط منقط، ثم نرسم منحنى بيزيه مكعب بقلم أحمر صلب.

## الخطوة 8: إضافة صور

يمكنك أيضًا إضافة صور إلى ملف WMF. إليك الطريقة:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

في هذه الخطوة، نقوم بتحميل صورة ووضعها على السطح عند الإحداثيات المحددة (50, 50).

## الخطوة 9: رسم خطوط وفطيرة

لإضافة خطوط وأشكال فطيرة، يمكنك اتباع الأمثلة التالية:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

هنا نرسم خطًا ونعبئ/نرسم شكل فطيرة باستخدام القلم والفرشاة المحددين.

## الخطوة 10: رسم خط متعدد النقاط ونص

إضافة نص وخط متعدد النقاط أمر بسيط:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

يمكنك تخصيص الخط، النص، ونقاط الخط المتعدد حسب الحاجة.

## الخطوة 11: حفظ صورة WMF

بعد إنشاء صورة WMF، حان وقت حفظها:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

هذه الشيفرة ستحفظ صورة WMF في الدليل المحدد.

هذا كل شيء—لقد نجحت في توليد ملف WMF باستخدام Aspose.Imaging للـ Java.

## الخاتمة

في هذا الدرس استكشفنا كيفية **إنشاء ملفات WMF** باستخدام Aspose.Imaging للـ Java. غطينا المتطلبات المسبقة، استوردنا الحزم الضرورية، وتابعنا كل خطوة رسم—من الأشكال الأساسية إلى النصوص والصور المضمنة—قبل أن نحفظ ملف WMF في النهاية. توفر لك Aspose.Imaging للـ Java مجموعة غنية من البدائل الرسومية، مما يجعلها مثالية لتوليد الرسومات المتجهية برمجيًا.

## الأسئلة المتكررة

### س1: ما هو تنسيق صورة WMF؟

ج1: WMF هو اختصار لـ **Windows Metafile**، وهو تنسيق رسومات متجهية يُستخدم لتخزين الصور، الرسومات، وغيرها من البيانات الرسومية. يُستَخدم بشكل شائع في تطبيقات Windows ويمكن تكبيره دون فقدان الجودة.

### س2: أين يمكنني تنزيل Aspose.Imaging للـ Java؟

ج2: يمكنك تنزيل Aspose.Imaging للـ Java من [الموقع الإلكتروني](https://releases.aspose.com/imaging/java/).

### س3: هل أحتاج إلى مهارات برمجة متقدمة لاستخدام Aspose.Imaging للـ Java؟

ج3: بينما يلزمك معرفة أساسية ببرمجة Java، توفر Aspose.Imaging للـ Java API سهل الاستخدام يبسط مهام معالجة وإنشاء الصور.

### س4: هل يمكنني استخدام Aspose.Imaging للـ Java لأغراض تجارية؟

ج4: نعم، تقدم Aspose.Imaging للـ Java تراخيص تجارية للشركات والمطورين. يمكنك شراء ترخيص [من هنا](https://purchase.aspose.com/buy).

### س5: أين يمكنني الحصول على الدعم أو طرح الأسئلة حول Aspose.Imaging للـ Java؟

ج5: يمكنك العثور على الدعم والتفاعل مع المجتمع عبر [منتديات Aspose.Imaging](https://forum.aspose.com/).

---

**آخر تحديث:** 2026-01-24  
**تم الاختبار مع:** Aspose.Imaging للـ Java 24.12 (الأحدث)  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}