---
date: '2026-03-20'
description: تعلم كيفية استخدام Aspose.Imaging للغة Java لضغط صور TIFF باستخدام ضغط
  LZW، مما يقلل حجم الملف مع الحفاظ على الجودة.
keywords:
- compress TIFF images Java
- Aspose.Imaging LZW compression
- Java image optimization
- TIFF compression in Java with Aspose
- image compression tutorial
title: كيفية استخدام Aspose.Imaging لضغط صور TIFF في Java (دليل ضغط LZW)
url: /ar/java/compression-optimization/compress-tiff-images-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# دليل: ضغط صور TIFF باستخدام Aspose.Imaging Java

## مقدمة

في هذا الدليل، ستتعلم **كيفية استخدام Aspose.Imaging للـ Java** لضغط صور TIFF بفعالية. إدارة ملفات TIFF الكبيرة يمكن أن تستهلك التخزين وعرض النطاق الترددي بسرعة، ولكن باستخدام ضغط LZW (Lempel‑Ziv‑Welch) يمكنك **تقليل حجم ملف TIFF** دون التضحية بجودة الصورة. سنستعرض تحميل ملف TIFF، وتكوين **ضغط TIFF LZW**، وحفظ النتيجة المُحسّنة—مثالي لأي شخص مهتم بـ **تحسين صور Java**.

**ما ستتعلمه**
- كيفية إعداد Aspose.Imaging للـ Java
- تحميل ومعالجة صور TIFF بسهولة
- تكوين ضغط LZW باستخدام `TiffOptions`
- حفظ صور TIFF مُحسّنة أصغر حجمًا ولكن بدون فقدان الجودة

لنبدأ بتجهيز المتطلبات المسبقة حتى تتمكن من البدء في الضغط فورًا.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.Imaging for Java  
- **ما خوارزمية الضغط؟** LZW (بدون فقدان)  
- **إصدارات Java المدعومة؟** أحدث إصدارات JDK (مثل 11، 17)  
- **هل أحتاج إلى ترخيص؟** ترخيص تجريبي أو مؤقت يكفي للاختبار؛ يلزم ترخيص تجاري للإنتاج.  
- **نسبة تقليل الحجم المعتادة؟** حتى 30‑50 % للصور المناسبة  

## المتطلبات المسبقة

قبل تنفيذ ضغط الصور في مشروع Java الخاص بك، تأكد من توفر ما يلي:

- **مكتبة Aspose.Imaging للـ Java** – أساسية لجميع ميزات معالجة الصور.  
- **مجموعة تطوير Java (JDK)** – نسخة حديثة متوافقة مع مكتبة Aspose.  
- **معرفة أساسية بـ Java** – الإلمام بعمليات الإدخال/الإخراج والبرمجة الكائنية سيساعد.  

## إعداد Aspose.Imaging للـ Java

للبدء، أضف مكتبة Aspose.Imaging إلى نظام البناء الخاص بك. اختر الطريقة التي تناسب مشروعك.

### استخدام Maven
أضف الاعتماد التالي إلى ملف `pom.xml` الخاص بك:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### استخدام Gradle
أدرج هذا السطر في ملف `build.gradle` الخاص بك:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### تحميل مباشر
بدلاً من ذلك، قم بتحميل أحدث نسخة من [إصدارات Aspose.Imaging للـ Java](https://releases.aspose.com/imaging/java/).

#### الحصول على الترخيص
يمكنك الحصول على ترخيص تجريبي مجاني أو طلب ترخيص مؤقت لتقييم قدرات Aspose.Imaging بالكامل قبل الشراء.

## كيفية استخدام Aspose.Imaging لضغط TIFF في Java

الآن لنقسم التنفيذ خطوة بخطوة. كل كتلة شفرة تبقى كما هي من الدليل الأصلي، لكننا سنضيف سياقًا أوضح حولها.

### تحميل صورة TIFF

**لماذا هذا مهم:** تحميل الصورة بشكل صحيح ينشئ كائن `Image` صالح ستعمل عليه جميع العمليات اللاحقة.

#### الخطوة 1: استيراد فئة Image
```java
import com.aspose.imaging.Image;
```

#### الخطوة 2: تحميل الصورة من القرص
```java
String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "/sample.tiff";
Image image = Image.load(dataDir);
```

### إنشاء TiffOptions لضغط الصورة

**لماذا هذا مهم:** `TiffOptions` يتيح لك تحديد كيفية ترميز TIFF الناتج، بما في ذلك إعداد **ضغط TIFF LZW**.

#### الخطوة 1: استيراد القيم والصفوف المطلوبة
```java
import com.aspose.imaging.fileformats.tiff.enums.TiffCompressions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.imaging.imageoptions.TiffOptions;
```

#### الخطوة 2: تكوين خيارات الضغط
```java
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);
outputSettings.setBitsPerSample(new int[] { 4 });
outputSettings.setCompression(TiffCompressions.Lzw);
outputSettings.setPhotometric(TiffPhotometrics.Palette);
```

### تعيين لوحة ألوان رمادية (اختياري لكن مفيد)

تطبيق لوحة ألوان رمادية 4‑bit يمكن أن يقلل **حجم ملف TIFF** أكثر، خاصةً للمسحات الأحادية اللون.

#### الخطوة 1: استيراد مساعد اللوحة
```java
import com.aspose.imaging.ColorPaletteHelper;
```

#### الخطوة 2: تعيين لوحة الألوان الرمادية
```java
outputSettings.setPalette(ColorPaletteHelper.create4BitGrayscale(false));
```

### حفظ صورة TIFF المضغوطة

**لماذا هذا مهم:** استدعاء `save` يكتب الصورة إلى القرص باستخدام جميع الخيارات التي قمت بتكوينها، مما ينتج ملفًا أصغر ومضغوطًا بـ LZW.

#### الخطوة 1: تحديد مسار الإخراج
```java
String outputDir = "YOUR_OUTPUT_DIRECTORY" + "/SampleTiff_out.tiff";
```

#### الخطوة 2: حفظ باستخدام إعدادات الضغط
```java
image.save(outputDir, outputSettings);
```

## تطبيقات عملية

إليك بعض السيناريوهات الواقعية حيث يمكن أن يكون **ضغط صور tiff** باستخدام LZW نقطة تحول:

1. **أرشفة المستندات** – تخزين ملفات PDF أو TIFF الممسوحة ضوئيًا بشكل أكثر كفاءة.  
2. **التصوير الطبي** – الحفاظ على تفاصيل التشخيص مع الحفاظ على حجم الملفات ضمن نطاق معقول.  
3. **أرشفة التصوير الفوتوغرافي** – الاحتفاظ بالنسخ الأصلية عالية الدقة دون إغراق التخزين.  
4. **تطبيقات الويب** – تقديم صور أصغر لتحميل الصفحات بسرعة وتقليل تكاليف النطاق الترددي.  

## اعتبارات الأداء

عند العمل مع صور كبيرة، احرص على مراعاة هذه النصائح للحفاظ على الأداء الأمثل:

- **إدارة الذاكرة:** حرّر كائنات `Image` الكبيرة فورًا (`image.dispose()`) إذا كنت تعالج العديد من الملفات في حلقة.  
- **تحسين عمق البت:** اضبط `BitsPerSample` إلى أقل قيمة مقبولة لحالتك.  
- **معالجة دفعات:** للعمليات الضخمة، فكر في تعدد الخيوط لكن راقب استهلاك الذاكرة في JVM.  

## مشكلات شائعة وحلولها

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| خطأ OutOfMemoryError أثناء تحميل ملفات TIFF الضخمة | تم تحميل الصورة بالكامل في الذاكرة | استخدم `Image.load(dataDir, new LoadOptions { BufferSize = … })` أو عالج الصورة على شكل بلاطات. |
| الملف المحفوظ أكبر من الأصلي | `BitsPerSample` غير صحيح أو عدم تطابق اللوحة | تحقق من أن `setBitsPerSample` يطابق عمق ألوان الصورة المصدر. |
| لوحة الألوان الرمادية تظهر بشكل غير صحيح | لم يتم تطبيق اللوحة قبل الحفظ | تأكد من استدعاء `outputSettings.setPalette(...)` **قبل** `image.save`. |

## الأسئلة المتكررة

**س: ما هو ضغط LZW؟**  
**ج:** ضغط Lempel‑Ziv‑Welch (LZW) هو خوارزمية بدون فقدان تقلل حجم الملف دون فقدان أي بيانات صورة.

**س: هل يمكنني استخدام Aspose.Imaging للـ Java في المشاريع التجارية؟**  
**ج:** نعم، يمكنك شراء ترخيص لاستخدامه تجاريًا. زر [Aspose Purchase](https://purchase.aspose.com/buy) للمزيد من التفاصيل.

**س: هل المكتبة متوافقة مع جميع إصدارات JDK؟**  
**ج:** تدعم معظم إصدارات JDK الحديثة. تحقق من الوثائق الرسمية لمعرفة التوافق الدقيق للإصدارات.

**س: كيف أتعامل مع الصور الكبيرة دون نفاد الذاكرة؟**  
**ج:** نفّذ ممارسات إدارة الذاكرة الفعّالة، مثل تحرير كائنات `Image` فورًا ومعالجة الصور على أجزاء أصغر عندما يكون ذلك ممكنًا.

**س: ما هي صيغ الملفات الأخرى التي يدعمها Aspose.Imaging؟**  
**ج:** المكتبة تدعم BMP، JPEG، PNG، GIF، والعديد غيرها. استكشف القائمة الكاملة على موقع [documentation site](https://reference.aspose.com/imaging/java/).

## الموارد

- **الوثائق:** [Aspose.Imaging Java Reference](https://reference.aspose.com/imaging/java/)  
- **التحميل:** [Latest Releases](https://releases.aspose.com/imaging/java/)  
- **الشراء:** [Buy Now](https://purchase.aspose.com/buy)  
- **تجربة مجانية:** [Start Here](https://releases.aspose.com/imaging/java/)  
- **ترخيص مؤقت:** [Request Here](https://purchase.aspose.com/temporary-license/)  
- **الدعم:** لمزيد من المساعدة، زر [Aspose Forum](https://forum.aspose.com/c/imaging/14)

---  

**آخر تحديث:** 2026-03-20  
**تم الاختبار مع:** Aspose.Imaging 25.5 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}