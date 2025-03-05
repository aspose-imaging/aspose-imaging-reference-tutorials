---
title: تحويل TIFF إلى BMP باستخدام Aspose.Imaging لـ Java
linktitle: استخراج إطارات TIFF إلى تنسيق BMP
second_title: Aspose.Imaging واجهة برمجة تطبيقات معالجة الصور لجافا
description: تعرف على كيفية استخراج إطارات TIFF إلى تنسيق BMP في Java باستخدام Aspose.Imaging for Java. اتبع دليلنا خطوة بخطوة.
type: docs
weight: 13
url: /ar/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
---
إذا كنت تعمل مع ملفات الصور في Java، وتحديدًا صور TIFF، وتحتاج إلى استخراج الإطارات منها وحفظها بتنسيق BMP، فإن Aspose.Imaging for Java هي أداة قوية ومتعددة الاستخدامات لتحقيق ذلك. في هذا الدليل التفصيلي، سنرشدك خلال عملية استخراج إطارات TIFF إلى تنسيق BMP باستخدام Aspose.Imaging for Java.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

1. بيئة تطوير Java: يجب أن يكون لديك بيئة تطوير Java عاملة معدة على نظامك.

2.  Aspose.Imaging for Java: تأكد من تثبيت مكتبة Aspose.Imaging for Java. يمكنك تنزيله من الموقع[هنا](https://releases.aspose.com/imaging/java/).

3. نموذج صورة TIFF: احصل على نموذج ملف صورة TIFF الذي تريد استخراج الإطارات منه. تأكد من توفر هذه الصورة في دليل العمل الخاص بك.

## حزم الاستيراد

لبدء العملية، تحتاج إلى استيراد الحزم اللازمة لتطبيق Java الخاص بك:

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## الخطوة 1: تحميل صورة TIFF وتهيئة عداد الإطار

```java
// المسار إلى دليل المستندات.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // قم بإنشاء مثيل int لتتبع الإطارات في TiffImage
    int frameCounter = 0;
```

## الخطوة 2: التكرار عبر إطارات TIFF

```java
    // كرر على TiffFrames في TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

## الخطوة 3: قم بتحميل بكسلات TiffFrame إلى مجموعة من الألوان

```java
        // قم بتحميل بكسلات TiffFrame إلى مجموعة من الألوان
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

## الخطوة 4: إنشاء خيارات BMP وتعيين البتات لكل بكسل

```java
        // قم بإنشاء مثيل bmpCreateOptions
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

## الخطوة 5: حفظ صورة BMP

```java
            // قم بتعيين مصدر bmpCreateOptions كـ FileCreateSource عن طريق تحديد الموقع الذي سيتم حفظ الإخراج فيه
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // قم بإنشاء صورة bmpImage جديدة
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // احفظ bmpImage بالبكسلات من TiffFrame
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## خاتمة

في هذا البرنامج التعليمي، تناولنا كيفية استخراج إطارات TIFF وحفظها كصور BMP باستخدام Aspose.Imaging for Java. باستخدام المتطلبات الأساسية الصحيحة واتباع الدليل خطوة بخطوة، يمكنك بسهولة تنفيذ مهمة تحويل الصور هذه في تطبيق Java الخاص بك.

## الأسئلة الشائعة

### س1: ما هو Aspose.Imaging لـ Java؟

ج1: Aspose.Imaging for Java عبارة عن مكتبة Java توفر إمكانات معالجة صور شاملة، مما يسمح لك بالعمل مع تنسيقات صور متنوعة وتنفيذ مهام مثل التحويل والتحرير والمعالجة.

### س2: هل يمكنني استخدام Aspose.Imaging لـ Java مع تنسيقات صور مختلفة؟

ج2: نعم، يدعم Aspose.Imaging for Java نطاقًا واسعًا من تنسيقات الصور، بما في ذلك TIFF وBMP وJPEG وPNG والعديد من التنسيقات الأخرى، مما يجعله أداة متعددة الاستخدامات للمهام المتعلقة بالصور.

### س3: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.Imaging for Java؟

 ج3: يمكنك العثور على الوثائق التفصيلية لـ Aspose.Imaging for Java[هنا](https://reference.aspose.com/imaging/java/).

### س4: هل هناك إصدار تجريبي مجاني متاح لـ Aspose.Imaging for Java؟

ج4: نعم، يمكنك استكشاف Aspose.Imaging for Java من خلال الإصدار التجريبي المجاني المتاح[هنا](https://releases.aspose.com/).

### س5: كيف يمكنني الحصول على دعم Aspose.Imaging لـ Java؟

 ج5: بالنسبة لأية أسئلة أو مشكلات أو دعم يتعلق بـ Aspose.Imaging for Java، يمكنك زيارة منتدى الدعم[هنا](https://forum.aspose.com/).