---
date: 2025-12-19
description: تعلم كيفية تحويل ملفات TIFF إلى BMP في Java باستخدام Aspose.Imaging.
  يوضح هذا الدليل خطوة بخطوة لمعالجة الصور في Java تحويل الصور لملفات TIFF متعددة
  الصفحات.
linktitle: Extract TIFF Frames to BMP Format
second_title: Aspose.Imaging Java Image Processing API
title: كيفية تحويل TIFF إلى BMP باستخدام Aspose.Imaging للـ Java
url: /ar/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# تحويل tiff إلى bmp باستخدام Aspose.Imaging for Java

إذا كنت بحاجة إلى **تحويل tiff إلى bmp** داخل تطبيق Java، فأنت في المكان الصحيح. سواء كنت تتعامل مع ملف TIFF صفحة واحدة أو مستند متعدد الصفحات، فإن Aspose.Imaging for Java يجعل العملية بسيطة وموثوقة. في هذا الدليل سنستعرض استخراج كل إطار من ملف TIFF وحفظه كصورة BMP منفردة — مثالي لسيناريوهات تحويل الصور في Java.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع التحويل؟** Aspose.Imaging for Java  
- **هل يمكنه معالجة ملفات TIFF متعددة الصفحات؟** نعم – يتم حفظ كل إطار كملف BMP منفصل  
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟** يلزم وجود ترخيص Aspose صالح للاستخدام التجاري  
- **ما نسخة Java المدعومة؟** Java 8 أو أعلى  
- **كم من الوقت يستغرق تشغيل الكود؟** عادةً بضع ثوانٍ للصور ذات الحجم القياسي  

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من توفر المتطلبات التالية:

1. **بيئة تطوير Java** – JDK يعمل (8 أو أحدث) وIDE أو أداة بناء من اختيارك.  
2. **Aspose.Imaging for Java** – حمّل أحدث ملف JAR من الموقع [هنا](https://releases.aspose.com/imaging/java/).  
3. **صورة TIFF نموذجية** – ملف TIFF (صفحة واحدة أو متعددة) وضعه في دليل العمل الخاص بالمشروع.

## استيراد الحزم

لبدء العملية، تحتاج إلى استيراد الحزم الضرورية لتطبيق Java الخاص بك:

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## دليل خطوة بخطوة لتحويل tiff إلى bmp

### الخطوة 1: تحميل صورة TIFF وتهيئة عداد الإطارات

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // Create an instance of int to keep track of frames in TiffImage
    int frameCounter = 0;
```

### الخطوة 2: تكرار عبر إطارات TIFF

```java
    // Iterate over the TiffFrames in TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

### الخطوة 3: تحميل بكسلات TiffFrame إلى مصفوفة من الألوان

```java
        // Load Pixels of TiffFrame into an array of Colors
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

### الخطوة 4: إنشاء خيارات BMP وتعيين عدد البتات لكل بكسل

```java
        // Create an instance of bmpCreateOptions
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

### الخطوة 5: حفظ صورة BMP

```java
            // Set the Source of bmpCreateOptions as FileCreateSource by specifying the location where output will be saved
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // Create a new bmpImage
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // Save the bmpImage with pixels from TiffFrame
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## لماذا تستخدم Aspose.Imaging for Java؟

- **دعم متعدد الصفحات قوي** – يتعامل مع أي عدد من إطارات TIFF دون الحاجة إلى كود إضافي.  
- **تنفيذ Java نقي** – لا يعتمد على مكتبات أصلية، مما يجعله مثالياً للنشر عبر الأنظمة.  
- **إخراج BMP عالي الجودة** – يمكنك التحكم في عدد البتات لكل بكسل، الضغط، وعمق اللون.  
- **مجموعة أدوات شاملة لتحويل الصور في Java** – يعمل مع JPEG، PNG، GIF، والعديد من الصيغ الأخرى.

## المشكلات الشائعة & استكشاف الأخطاء

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| `OutOfMemoryError` أثناء تحميل ملفات TIFF الكبيرة | تم تحميل الصورة بالكامل في الذاكرة | عالج الإطارات واحدةً تلو الأخرى كما هو موضح، أو زد حجم الذاكرة المخصصة للـ JVM (`-Xmx`) |
| ملف BMP تالف | قيمة `BitsPerPixel` غير صحيحة | استخدم 24 أو 32 للحصول على BMP بألوان حقيقية |
| لا يتم إنشاء ملفات إخراج | مسار دليل الإخراج غير صحيح | تحقق من أن `Your Document Directory` يشير إلى مجلد موجود |

## الأسئلة المتكررة

### س1: ما هو Aspose.Imaging for Java؟

ج1: Aspose.Imaging for Java هي مكتبة Java توفر إمكانيات معالجة صور واسعة، تتيح لك العمل مع صيغ صور متعددة وإجراء مهام مثل التحويل، التحرير، والتلاعب.

### س2: هل يمكنني استخدام Aspose.Imaging for Java مع صيغ صور مختلفة؟

ج2: نعم، يدعم Aspose.Imaging for Java مجموعة واسعة من صيغ الصور، بما في ذلك TIFF، BMP، JPEG، PNG، والعديد غيرها، مما يجعله أداة متعددة الاستخدامات لمهام الصور.

### س3: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.Imaging for Java؟

ج3: يمكنك العثور على وثائق مفصلة لـ Aspose.Imaging for Java [هنا](https://reference.aspose.com/imaging/java/).

### س4: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Imaging for Java؟

ج4: نعم، يمكنك تجربة Aspose.Imaging for Java عبر نسخة تجريبية مجانية متاحة [هنا](https://releases.aspose.com/).

### س5: كيف يمكنني الحصول على الدعم لـ Aspose.Imaging for Java؟

ج5: لأي أسئلة أو مشكلات أو دعم يتعلق بـ Aspose.Imaging for Java، يمكنك زيارة منتدى الدعم [هنا](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2025-12-19  
**تم الاختبار باستخدام:** Aspose.Imaging for Java 24.12 (latest)  
**المؤلف:** Aspose  

---