---
"description": "تعرّف على كيفية التعامل مع بيانات تعريف XMP في الصور باستخدام Aspose.Imaging لـ Java. أدرج بيانات تعريفية واسترجعها لتحسين ملفات صورك."
"linktitle": "معالجة بيانات XMP في الصور"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Java Aspose.Imaging"
"title": "معالجة بيانات XMP في الصور باستخدام Aspose.Imaging لـ Java"
"url": "/ar/java/document-conversion-and-processing/xmp-data-handling-in-images/"
"weight": 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# معالجة بيانات XMP في الصور باستخدام Aspose.Imaging لـ Java

Aspose.Imaging for Java هي مكتبة متعددة الاستخدامات وفعّالة للتعامل مع الصور بتنسيقات متنوعة. سيرشدك هذا البرنامج التعليمي خلال عملية معالجة بيانات XMP (منصة البيانات الوصفية القابلة للتوسيع) في الصور باستخدام Aspose.Imaging for Java. XMP هو معيار لتضمين البيانات الوصفية في ملفات الصور، مما يسمح لك بتخزين معلومات قيّمة مثل اسم المؤلف والوصف وغيرها.

## المتطلبات الأساسية

قبل أن تبدأ، تأكد من توفر المتطلبات الأساسية التالية:

- بيئة تطوير Java تم إعدادها على جهاز الكمبيوتر الخاص بك.
- تم تثبيت مكتبة Aspose.Imaging لجافا. يمكنك تنزيلها من [موقع Aspose.Imaging لـ Java](https://releases.aspose.com/imaging/java/).
- فهم أساسي لبرمجة جافا.

## استيراد الحزم

ابدأ باستيراد الحزم اللازمة لمشروع جافا. يمكنك إضافة عبارات الاستيراد التالية في بداية الكود:

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

## الخطوة 1: تحديد حجم الصورة وخيارات TIFF

أولاً، حدد المجلد الذي ستُخزَّن فيه صورتك، وأنشئ مستطيلاً لتحديد حجم الصورة. في هذا المثال، نستخدم صورة Tiff مع خيارات مُحدَّدة.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## الخطوة 2: إنشاء صورة جديدة

الآن، أنشئ صورة جديدة بالخيارات المحددة. ستُستخدم هذه الصورة لتخزين بيانات XMP الوصفية.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## الخطوة 3: إنشاء رأس ومقطع XMP

أنشئ مثيلات من XMP-Header وXMP-Trailer لبيانات XMP الوصفية. تساعد هذه الرؤوس والمقتطفات في تحديد بنية البيانات الوصفية.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## الخطوة 4: إنشاء معلومات XMP Meta

الآن، أنشئ مثيلًا لبيانات XMP الوصفية لتعيين سمات مختلفة. يمكنك إضافة معلومات مثل المؤلف والوصف.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## الخطوة 5: إنشاء غلاف حزمة XMP

قم بإنشاء مثيل لـ XmpPacketWrapper يحتوي على رأس XMP والمقطع الدعائي ومعلومات التعريف.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## الخطوة 6: إضافة حزمة الفوتوشوب

لتخزين معلومات خاصة بفوتوشوب، أنشئ حزمة فوتوشوب وحدد سماتها، مثل المدينة والبلد ووضع اللون. ثم أضف هذه الحزمة إلى بيانات تعريف XMP.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## الخطوة 7: إضافة حزمة Dublin Core

للحصول على معلومات عامة، مثل المؤلف والعنوان والقيم الإضافية، أنشئ حزمة DublinCore وحدد سماتها. أضف هذه الحزمة إلى بيانات تعريف XMP أيضًا.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## الخطوة 8: تحديث بيانات XMP التعريفية في الصورة

قم بتحديث بيانات XMP في الصورة باستخدام `setXmpData` طريقة.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## الخطوة 9: حفظ الصورة

يمكنك الآن حفظ الصورة باستخدام بيانات XMP المضمنة على القرص أو في مجرى الذاكرة.

```java
    image.save(ms);
```

## الخطوة 10: تحميل الصورة واسترداد بيانات XMP التعريفية

لاسترداد بيانات XMP من الصورة، قم بتحميل الصورة من مجرى الذاكرة أو القرص والوصول إلى بيانات XMP.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // استخدم بيانات الحزمة ...
        }
    }
}
```

تهانينا! لقد نجحت في تعلم كيفية التعامل مع بيانات XMP في الصور باستخدام Aspose.Imaging لـ Java. يتيح لك هذا تخزين واسترجاع بيانات وصفية قيّمة داخل ملفات صورك.

## خاتمة

في هذا البرنامج التعليمي، استكشفنا كيفية التعامل مع بيانات تعريف XMP في الصور باستخدام Aspose.Imaging لـ Java. باتباع هذا الدليل التفصيلي، يمكنك بسهولة تضمين واسترجاع بيانات التعريف في ملفات صورك، مما يُحسّن معلوماتها وسهولة استخدامها.

## الأسئلة الشائعة

### س1: ما هي بيانات XMP التعريفية؟

ج١: XMP (منصة البيانات الوصفية القابلة للتوسيع) هو معيار لتضمين البيانات الوصفية في أنواع مختلفة من الملفات، بما في ذلك الصور. يسمح لك بتخزين معلومات مثل المؤلف والعنوان والوصف وغيرها داخل الملف نفسه.

### س2: لماذا تعتبر بيانات XMP مهمة؟

ج٢: بيانات تعريف XMP ضرورية لتنظيم الأصول الرقمية وتصنيفها. فهي تساعد في تحديد الملكية، ووصف المحتوى، وإضافة سياق للملفات، مثل الصور، مما يجعلها أكثر سهولة في الوصول إليها وأكثر فائدة.

### س3: هل يمكنني تعديل بيانات XMP التعريفية بعد تضمينها في صورة؟

ج٣: نعم، يمكنك تعديل بيانات تعريف XMP بعد تضمينها في صورة. يوفر Aspose.Imaging for Java أدوات لتعديل سمات البيانات التعريفية وتحديثها حسب الحاجة.

### س4: هل Aspose.Imaging for Java أداة مجانية؟

ج٤: يُقدّم Aspose.Imaging for Java نسخة تجريبية مجانية، ولكن للحصول على كامل الوظائف والاستخدام المُوسّع، يلزم الحصول على ترخيص مدفوع. يمكنك استكشاف الخيارات المتاحة على [موقع Aspose.Imaging لـ Java](https://purchase.aspose.com/buy).

### س5: أين يمكنني الحصول على المساعدة والدعم لـ Aspose.Imaging لـ Java؟

A5: إذا واجهت أي مشكلات أو كانت لديك أسئلة تتعلق بـ Aspose.Imaging for Java، فيمكنك زيارة [منتديات Aspose.Imaging](https://forum.aspose.com/) للحصول على الدعم والتوجيه المجتمعي.



## الكود المصدر الكامل
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// حدد حجم الصورة عن طريق تعريف المستطيل
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// إنشاء صورة جديدة فقط لأغراض العينة
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// إنشاء مثيل لـ XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// إنشاء مثيل لـ Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// إنشاء مثيل لفئة XMP meta لتعيين سمات مختلفة
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// إنشاء مثيل لـ XmpPacketWrapper يحتوي على جميع البيانات الوصفية
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// إنشاء مثيل لحزمة Photoshop وتعيين سمات Photoshop
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// إضافة حزمة فوتوشوب إلى بيانات تعريف XMP
	xmpData.addPackage(photoshopPackage);
	// إنشاء مثيل لحزمة DublinCore وتعيين سمات dublinCore
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// إضافة حزمة dublinCore إلى بيانات تعريف XMP
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// تحديث بيانات XMP الوصفية في الصورة
	image.setXmpData(xmpData);
	// حفظ الصورة على القرص أو في مجرى الذاكرة
	image.save(ms);
	// قم بتحميل الصورة من مجرى الذاكرة أو من القرص لقراءة/الحصول على البيانات الوصفية
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// الحصول على بيانات تعريف XMP
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// استخدم بيانات الحزمة ...
		}
	}
}
        
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}