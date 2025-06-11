---
"description": "تعلّم كيفية استخراج إطارات TIFF إلى صيغة BMP في جافا باستخدام Aspose.Imaging for Java. اتبع دليلنا خطوة بخطوة."
"linktitle": "استخراج إطارات TIFF إلى تنسيق BMP"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Java Aspose.Imaging"
"title": "تحويل TIFF إلى BMP باستخدام Aspose.Imaging لـ Java"
"url": "/ar/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/"
"weight": 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# تحويل TIFF إلى BMP باستخدام Aspose.Imaging لـ Java

إذا كنت تعمل على ملفات صور بلغة جافا، وتحديدًا صور TIFF، وتحتاج إلى استخراج إطارات منها وحفظها بصيغة BMP، فإن Aspose.Imaging for Java أداة فعّالة ومتعددة الاستخدامات لتحقيق ذلك. في هذا الدليل التفصيلي، سنشرح لك عملية استخراج إطارات TIFF إلى صيغة BMP باستخدام Aspose.Imaging for Java.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

1. بيئة تطوير Java: يجب أن يكون لديك بيئة تطوير Java عاملة تم إعدادها على نظامك.

2. Aspose.Imaging لجافا: تأكد من تثبيت مكتبة Aspose.Imaging لجافا. يمكنك تنزيلها من الموقع الإلكتروني. [هنا](https://releases.aspose.com/imaging/java/).

3. صورة TIFF نموذجية: لديك ملف صورة TIFF نموذجي ترغب في استخراج الإطارات منه. تأكد من توفر هذه الصورة في مجلد العمل.

## استيراد الحزم

لبدء العملية، تحتاج إلى استيراد الحزم اللازمة لتطبيق Java الخاص بك:

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## الخطوة 1: تحميل صورة TIFF وتهيئة عداد الإطارات

```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // إنشاء مثيل لـ int لتتبع الإطارات في TiffImage
    int frameCounter = 0;
```

## الخطوة 2: التكرار عبر إطارات TIFF

```java
    // التكرار على TiffFrames في TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

## الخطوة 3: تحميل وحدات البكسل من TiffFrame إلى مجموعة من الألوان

```java
        // تحميل وحدات بكسل TiffFrame في مجموعة من الألوان
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

## الخطوة 4: إنشاء خيارات BMP وتعيين البتات لكل بكسل

```java
        // إنشاء مثيل لـ bmpCreateOptions
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

## الخطوة 5: حفظ صورة BMP

```java
            // قم بتعيين مصدر bmpCreateOptions كـ FileCreateSource من خلال تحديد الموقع الذي سيتم حفظ الإخراج فيه
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // إنشاء صورة bmpImage جديدة
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // حفظ صورة bmpImage بالبكسل من TiffFrame
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## خاتمة

في هذا البرنامج التعليمي، تناولنا كيفية استخراج إطارات TIFF وحفظها كصور BMP باستخدام Aspose.Imaging لجافا. مع توفر المتطلبات الأساسية الصحيحة واتباع الدليل خطوة بخطوة، يمكنك بسهولة تحويل الصور في تطبيق جافا الخاص بك.

## الأسئلة الشائعة

### س1: ما هو Aspose.Imaging لـ Java؟

A1: Aspose.Imaging for Java هي مكتبة Java توفر إمكانيات معالجة الصور الشاملة، مما يسمح لك بالعمل مع تنسيقات الصور المختلفة وأداء مهام مثل التحويل والتحرير والتلاعب.

### س2: هل يمكنني استخدام Aspose.Imaging لـ Java مع تنسيقات صور مختلفة؟

ج2: نعم، يدعم Aspose.Imaging for Java مجموعة واسعة من تنسيقات الصور، بما في ذلك TIFF وBMP وJPEG وPNG والعديد من التنسيقات الأخرى، مما يجعله أداة متعددة الاستخدامات للمهام المتعلقة بالصور.

### س3: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.Imaging لـ Java؟

A3: يمكنك العثور على وثائق مفصلة لـ Aspose.Imaging لـ Java [هنا](https://reference.aspose.com/imaging/java/).

### س4: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Imaging لنظام Java؟

ج4: نعم، يمكنك استكشاف Aspose.Imaging لـ Java من خلال إصدار تجريبي مجاني متاح [هنا](https://releases.aspose.com/).

### س5: كيف أحصل على الدعم لـ Aspose.Imaging لـ Java؟

ج5: لأي أسئلة أو مشكلات أو دعم يتعلق بـ Aspose.Imaging for Java، يمكنك زيارة منتدى الدعم [هنا](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}