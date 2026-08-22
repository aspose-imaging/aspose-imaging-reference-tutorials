---
date: 2026-05-03
description: تعلم كيفية تحويل ملفات TIFF متعددة الصفحات إلى تنسيق BMP في Java باستخدام
  Aspose.Imaging. اتبع هذا الدليل خطوة بخطوة حول كيفية تحويل TIFF بكفاءة.
keywords:
- convert multi page tiff
- how to convert tiff
- Aspose.Imaging Java
- TIFF to BMP conversion
- image processing Java
linktitle: استخراج إطارات TIFF إلى تنسيق BMP
second_title: Aspose.Imaging Java Image Processing API
title: تحويل ملف TIFF متعدد الصفحات إلى BMP باستخدام Aspose.Imaging للـ Java
url: /ar/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# تحويل ملفات TIFF متعددة الصفحات إلى BMP باستخدام Aspose.Imaging للغة Java

إذا كنت بحاجة إلى **تحويل ملفات TIFF متعددة الصفحات** إلى صور BMP منفصلة أثناء العمل في بيئة Java، فأنت في المكان الصحيح. في هذا البرنامج التعليمي سنستعرض الخطوات الدقيقة لاستخراج كل إطار من TIFF وحفظه كملف BMP باستخدام مكتبة Aspose.Imaging للغة Java القوية. في النهاية، ستفهم ليس فقط *كيفية تحويل ملفات TIFF* برمجياً، بل أيضاً لماذا يعتبر هذا النهج موثوقاً لمهام معالجة الصور على دفعات.

## إجابات سريعة
- **ما هي المكتبة الأفضل لتحويل TIFF إلى BMP؟** Aspose.Imaging for Java  
- **كم عدد أسطر الكود المطلوبة؟** حوالي 30 سطرًا عبر خمس خطوات منطقية  
- **هل أحتاج إلى ترخيص للإنتاج؟** نعم، يلزم الحصول على ترخيص تجاري (يتوفر نسخة تجريبية مجانية)  
- **هل يمكنه معالجة ملفات TIFF متعددة الصفحات الكبيرة؟** نعم، تقوم الـ API بتدفق الإطارات بكفاءة  
- **ما نسخة Java المدعومة؟** Java 8 وما بعدها  

## ما هو “تحويل ملفات TIFF متعددة الصفحات”؟
تحويل ملف TIFF متعدد الصفحات يعني أخذ كل صفحة (أو إطار) مخزنة داخل حاوية TIFF واحدة وتصديرها كملف صورة مستقل — هنا، BMP. هذا مفيد لأرشفة المستندات، التصوير الطبي، أو أي سير عمل يتطلب صورًا نقطية للمعالجة اللاحقة.

## لماذا نستخدم Aspose.Imaging للغة Java؟
- **دعم كامل للأنساق** – يدعم TIFF، BMP، JPEG، PNG، والعديد غيرها.  
- **لا توجد تبعيات خارجية** – جافا صافية، بدون مكتبات أصلية.  
- **أداء عالي** – الوصول المتدفق إلى الإطارات يقلل من استهلاك الذاكرة.  
- **API غني** – يوفر تحكمًا دقيقًا في بيانات البكسل، عمق اللون، والبيانات الوصفية.  

## المتطلبات المسبقة

1. **بيئة تطوير Java** – JDK 8+ وIDE المفضلة لديك.  
2. **Aspose.Imaging للغة Java** – قم بتحميل أحدث ملف JAR من الموقع الرسمي **[هنا](https://releases.aspose.com/imaging/java/)**.  
3. **ملف TIFF متعدد الصفحات تجريبي** – ضع ملف TIFF (مثال: `sample.tiff`) في دليل معروف يمكن لرمزك قراءته.  

## استيراد الحزم

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## كيفية تحويل ملفات TIFF متعددة الصفحات إلى BMP باستخدام Aspose.Imaging

### الخطوة 1: تحميل صورة TIFF وتهيئة عداد الإطارات

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // Create an instance of int to keep track of frames in TiffImage
    int frameCounter = 0;
```

### الخطوة 2: التكرار عبر إطارات TIFF

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

### الخطوة 4: إنشاء خيارات BMP وتحديد عدد البتات لكل بكسل

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

## المشكلات الشائعة والنصائح

- **استخدام الذاكرة:** عند التعامل مع ملفات TIFF الكبيرة جدًا، فكر في معالجة الإطارات واحدةً تلو الأخرى (كما هو موضح) بدلاً من تحميل الصورة بالكامل في الذاكرة.  
- **تسمية الملفات:** تُنشئ الدالة `String.format` اسم ملف فريد لكل إطار (`...out0.bmp`, `...out1.bmp`, إلخ). عدّل النمط إذا كنت بحاجة إلى صيغة تسمية مختلفة.  
- **عمق البت:** يدعم BMP عدة أعماق للبت؛ 24‑بت (لون حقيقي) يعمل في معظم السيناريوهات. غيّر `setBitsPerPixel` إذا كنت تحتاج إلى إخراج بت 8‑بت رمادي.  

## الأسئلة المتكررة

### س1: ما هو Aspose.Imaging للغة Java؟

ج1: Aspose.Imaging للغة Java هي مكتبة جافا توفر قدرات معالجة صور واسعة، تتيح لك العمل مع صيغ صور مختلفة وأداء مهام مثل التحويل، التحرير، والتلاعب.

### س2: هل يمكنني استخدام Aspose.Imaging للغة Java مع صيغ صور مختلفة؟

ج2: نعم، يدعم Aspose.Imaging للغة Java مجموعة واسعة من صيغ الصور، بما في ذلك TIFF، BMP، JPEG، PNG، والعديد غيرها، مما يجعله أداة متعددة الاستخدامات لمهام الصور.

### س3: أين يمكنني العثور على وثائق Aspose.Imaging للغة Java؟

ج3: يمكنك العثور على وثائق مفصلة لـ Aspose.Imaging للغة Java **[هنا](https://reference.aspose.com/imaging/java/)**.

### س4: هل تتوفر نسخة تجريبية مجانية لـ Aspose.Imaging للغة Java؟

ج4: نعم، يمكنك تجربة Aspose.Imaging للغة Java من خلال نسخة تجريبية مجانية متوفرة **[هنا](https://releases.aspose.com/)**.

### س5: كيف يمكنني الحصول على الدعم لـ Aspose.Imaging للغة Java؟

ج5: لأي أسئلة أو مشكلات أو دعم يتعلق بـ Aspose.Imaging للغة Java، يمكنك زيارة منتدى الدعم **[هنا](https://forum.aspose.com/)**.

## الأسئلة المتكررة

**س: هل يمكنني تحويل ملف TIFF متعدد الصفحات إلى صيغ أخرى (مثل PNG) باستخدام نفس النهج؟**  
ج: بالتأكيد. استبدل `BmpOptions` بالفئة المناسبة للخيارات (مثل `PngOptions`) وقم بتعديل امتداد الملف في مسار `FileCreateSource`.

**س: هل يتعامل Aspose.Imaging مع ملفات TIFF المضغوطة (LZW، CCITT)؟**  
ج: نعم، تقوم المكتبة بفك ضغط صيغ ضغط TIFF المدعومة بشكل شفاف أثناء استخراج الإطارات.

**س: هل يمكن الحفاظ على بيانات EXIF الوصفية عند التحويل إلى BMP؟**  
ج: لا يدعم BMP بيانات EXIF الوصفية. إذا كنت بحاجة إلى الاحتفاظ بالبيانات الوصفية، فكر في التحويل إلى صيغة تدعمها (مثل PNG) أو انسخ البيانات الوصفية يدوياً بعد التحويل.

**س: كيف يمكنني معالجة عدة ملفات TIFF دفعةً في مجلد؟**  
ج: ضع الشيفرة أعلاه داخل حلقة تت iterates over كائنات `File` في دليل، مع تحديث `dataDir` واسم الملف المصدر لكل ملف.

**س: ما الترخيص المطلوب للنشر التجاري؟**  
ج: يلزم الحصول على ترخيص Aspose.Imaging للغة Java مدفوع للاستخدام في الإنتاج. يمكن استخدام ترخيص تجريبي مؤقت أثناء التطوير.

---

**آخر تحديث:** 2026-05-03  
**تم الاختبار مع:** Aspose.Imaging for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}