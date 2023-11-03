---
title: معالجة بيانات XMP في الصور باستخدام Aspose.Imaging لـ Java
linktitle: معالجة بيانات XMP في الصور
second_title: Aspose.Imaging واجهة برمجة تطبيقات معالجة الصور لجافا
description: تعرف على كيفية التعامل مع بيانات تعريف XMP في الصور باستخدام Aspose.Imaging for Java. قم بتضمين واسترجاع البيانات الوصفية لتحسين ملفات الصور الخاصة بك.
type: docs
weight: 16
url: /ar/java/document-conversion-and-processing/xmp-data-handling-in-images/
---
Aspose.Imaging for Java هي مكتبة قوية ومتعددة الاستخدامات للتعامل مع الصور بتنسيقات مختلفة. سيرشدك هذا البرنامج التعليمي خلال عملية التعامل مع بيانات XMP (منصة البيانات الوصفية القابلة للتوسيع) في الصور باستخدام Aspose.Imaging for Java. يعد XMP معيارًا لدمج بيانات التعريف في ملفات الصور، مما يسمح لك بتخزين معلومات قيمة مثل المؤلف والوصف والمزيد.

## المتطلبات الأساسية

قبل البدء، تأكد من توفر المتطلبات الأساسية التالية:

- تم إعداد بيئة تطوير Java على جهاز الكمبيوتر الخاص بك.
-  تم تثبيت Aspose.Imaging لمكتبة Java. يمكنك تنزيله من[Aspose.Imaging لموقع جافا](https://releases.aspose.com/imaging/java/).
- الفهم الأساسي لبرمجة جافا.

## استيراد الحزم

ابدأ باستيراد الحزم الضرورية لمشروع Java الخاص بك. يمكنك إضافة عبارات الاستيراد التالية في بداية التعليمات البرمجية الخاصة بك:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.xmp.XmpPackage;
import com.aspose.imaging.xmp.XmpPacketWrapper;
import com.aspose.imaging.xmp.XmpMeta;
import com.aspose.imaging.xmp.photoshop.ColorMode;
import com.aspose.imaging.xmp.photoshop.PhotoshopPackage;
import com.aspose.imaging.xmp.dc.DublinCorePackage;
import com.aspose.imaging.xmp.header.XmpHeaderPi;
import com.aspose.imaging.xmp.trailer.XmpTrailerPi;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

الآن، دعونا نقسم المثال إلى دليل خطوة بخطوة:

## الخطوة 1: تحديد حجم الصورة وخيارات Tiff

أولاً، حدد الدليل الذي سيتم تخزين صورتك فيه وقم بإنشاء مستطيل لتحديد حجم الصورة. في هذا المثال، نستخدم صورة Tiff مع خيارات معينة.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## الخطوة 2: إنشاء صورة جديدة

الآن، قم بإنشاء صورة جديدة بالخيارات المحددة. سيتم استخدام هذه الصورة لتخزين بيانات تعريف XMP.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## الخطوة 3: إنشاء رأس XMP ومقطورة

قم بإنشاء مثيلات XMP-Header وXMP-Trailer لبيانات تعريف XMP الخاصة بك. تساعد هذه الرؤوس والمقطورات في تحديد بنية البيانات التعريفية.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## الخطوة 4: إنشاء معلومات تعريف XMP

الآن، قم بإنشاء مثيل لـ XMP meta لتعيين سمات مختلفة. يمكنك إضافة معلومات مثل المؤلف والوصف.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## الخطوة 5: إنشاء غلاف حزمة XMP

قم بإنشاء مثيل XmpPacketWrapper الذي يحتوي على معلومات رأس XMP والمقطورة ومعلومات التعريف.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## الخطوة 6: إضافة حزمة فوتوشوب

لتخزين معلومات خاصة بـ Photoshop، قم بإنشاء حزمة Photoshop وقم بتعيين سماتها، مثل المدينة والبلد ووضع الألوان. ثم قم بإضافة هذه الحزمة إلى بيانات تعريف XMP.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## الخطوة 7: إضافة حزمة دبلن الأساسية

لمزيد من المعلومات العامة، مثل المؤلف والعنوان والقيم الإضافية، قم بإنشاء حزمة DublinCore وقم بتعيين سماتها. أضف هذه الحزمة إلى بيانات تعريف XMP أيضًا.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## الخطوة 8: تحديث بيانات تعريف XMP في الصورة

 قم بتحديث بيانات تعريف XMP في الصورة باستخدام ملف`setXmpData` طريقة.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## الخطوة 9: احفظ الصورة

يمكنك الآن حفظ الصورة باستخدام بيانات تعريف XMP المضمنة على القرص أو في تدفق الذاكرة.

```java
    image.save(ms);
```

## الخطوة 10: قم بتحميل الصورة واسترجاع بيانات تعريف XMP

لاسترداد بيانات تعريف XMP من الصورة، قم بتحميل الصورة من دفق الذاكرة أو القرص وقم بالوصول إلى بيانات XMP.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // استخدام بيانات الحزمة...
        }
    }
}
```

تهانينا! لقد تعلمت بنجاح كيفية التعامل مع بيانات XMP في الصور باستخدام Aspose.Imaging for Java. يتيح لك ذلك تخزين واسترجاع البيانات التعريفية القيمة داخل ملفات الصور الخاصة بك.

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا كيفية العمل مع بيانات تعريف XMP في الصور باستخدام Aspose.Imaging for Java. باتباع الدليل الموضح خطوة بخطوة، يمكنك بسهولة تضمين البيانات التعريفية واسترجاعها داخل ملفات الصور الخاصة بك، مما يعزز معلوماتها وسهولة استخدامها.

## الأسئلة الشائعة

### س١: ما هي بيانات تعريف XMP؟

A1: يعد XMP (منصة بيانات التعريف القابلة للتوسيع) معيارًا لتضمين بيانات التعريف في أنواع مختلفة من الملفات، بما في ذلك الصور. يسمح لك بتخزين معلومات مثل المؤلف والعنوان والوصف والمزيد داخل الملف نفسه.

### س2: ما سبب أهمية بيانات تعريف XMP؟

ج2: تعد بيانات تعريف XMP ضرورية لتنظيم الأصول الرقمية وتصنيفها. فهو يساعد في إسناد الملكية، ووصف المحتوى، وإضافة سياق إلى الملفات مثل الصور، مما يجعلها أكثر سهولة في الوصول إليها وذات معنى.

### س3: هل يمكنني تحرير بيانات تعريف XMP بعد تضمينها في صورة؟

ج3: نعم، يمكنك تحرير بيانات تعريف XMP بعد تضمينها في الصورة. يوفر Aspose.Imaging for Java أدوات لتعديل وتحديث سمات بيانات التعريف حسب الحاجة.

### س 4: هل يعتبر Aspose.Imaging for Java أداة مجانية؟

 ج4: يقدم Aspose.Imaging for Java إصدارًا تجريبيًا مجانيًا، ولكن للحصول على الوظائف الكاملة والاستخدام الموسع، يلزم الحصول على ترخيص مدفوع. يمكنك استكشاف الخيارات الموجودة على[Aspose.Imaging لموقع جافا](https://purchase.aspose.com/buy).

### س5: أين يمكنني الحصول على المساعدة والدعم فيما يتعلق بـ Aspose.Imaging for Java؟

 ج5: إذا واجهت أية مشكلات أو كانت لديك أسئلة تتعلق بـ Aspose.Imaging for Java، فيمكنك زيارة[Aspose.منتديات التصوير](https://forum.aspose.com/) لدعم وتوجيه المجتمع.



## استكمال كود المصدر
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// حدد حجم الصورة عن طريق تحديد مستطيل
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// قم بإنشاء الصورة الجديدة تمامًا لأغراض العينة فقط
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// إنشاء مثيل لـ XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// قم بإنشاء مثيل لـ Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// قم بإنشاء مثيل لفئة التعريف XMP لتعيين سمات مختلفة
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	//إنشاء مثيل XmpPacketWrapper الذي يحتوي على كافة بيانات التعريف
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// إنشاء مثيل لحزمة Photoshop وتعيين سمات Photoshop
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// إضافة حزمة Photoshop إلى بيانات تعريف XMP
	xmpData.addPackage(photoshopPackage);
	// قم بإنشاء مثيل لحزمة DublinCore وقم بتعيين سمات dublinCore
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// قم بإضافة حزمة dublinCore إلى بيانات تعريف XMP
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// تحديث بيانات تعريف XMP في الصورة
	image.setXmpData(xmpData);
	// حفظ الصورة على القرص أو في دفق الذاكرة
	image.save(ms);
	// قم بتحميل الصورة من دفق الذاكرة أو من القرص لقراءة/الحصول على البيانات التعريفية
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// الحصول على بيانات تعريف XMP
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// استخدام بيانات الحزمة...
		}
	}
}
        
```