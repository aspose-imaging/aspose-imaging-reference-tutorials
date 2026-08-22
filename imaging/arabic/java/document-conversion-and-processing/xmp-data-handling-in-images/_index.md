---
date: 2026-05-18
description: تعلم كيفية استخدام مكتبة معالجة الصور لجافا Aspose.Imaging لتضمين واسترجاع
  بيانات XMP الوصفية في الصور، مع كود خطوة بخطوة.
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: معالجة بيانات XMP في الصور
schemas:
- author: Aspose
  dateModified: '2026-05-18'
  description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  headline: 'Java Image Processing Library: XMP with Aspose.Imaging'
  type: TechArticle
- description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  name: 'Java Image Processing Library: XMP with Aspose.Imaging'
  steps:
  - name: Specify Image Size and Tiff Options
    text: First, define the directory where your image will be stored and create a
      `Rectangle` to specify the size of the image. In this example, we use a TIFF
      image with certain options. `TiffOptions` configures format‑specific settings
      for the TIFF image.
  - name: Create a New Image
    text: Now, create a new image with the specified options. This image will be used
      to store the XMP metadata. `TiffImage` represents a TIFF image object, and `TiffFrame`
      defines an individual frame within it.
  - name: Create XMP Header and Trailer
    text: Create instances of XMP‑Header and XMP‑Trailer for your XMP metadata. These
      headers and trailers help define the metadata structure. `XmpHeaderPi` and `XmpTrailerPi`
      represent the XMP packet’s opening and closing sections.
  - name: Create XMP Meta Information
    text: Now, create an instance of XMP meta to set different attributes. You can
      add information like the author and description. `XmpMeta` holds the core metadata
      fields such as author and description.
  - name: Create XMP Packet Wrapper
    text: '`XmpPacketWrapper` is the container that holds the XMP header, trailer,
      and meta information in a single packet. It ensures the packet conforms to the
      XMP specification. `XmpPacketWrapper` packages the header, meta, and trailer
      into a single XMP packet.'
  - name: Add Photoshop Package
    text: To store Photoshop‑specific information, create a Photoshop package and
      set its attributes, such as city, country, and color mode. Then, add this package
      to the XMP metadata. `PhotoshopPackage` stores Photoshop‑specific metadata like
      city, country, and color mode.
  - name: Add Dublin Core Package
    text: For more general information, like author, title, and additional values,
      create a DublinCore package and set its attributes. Add this package to the
      XMP metadata as well. `DublinCorePackage` contains standard Dublin Core fields
      such as title, creator, and keywords.
  - name: Update XMP Metadata in the Image
    text: Update the XMP metadata into the image using the `setXmpData` method. This
      call writes the XMP packet into the image’s metadata section. `setXmpData` writes
      the XMP packet into the image’s metadata section.
  - name: Save the Image
    text: You can now save the image with the embedded XMP metadata on the disk or
      in a memory stream.
  - name: Load the Image and Retrieve XMP Metadata
    text: To retrieve the XMP metadata from the image, load the image from the memory
      stream or disk and access the XMP data via the `getXmpData` method. `getXmpData`
      reads the embedded XMP packet from the image. Congratulations! You've successfully
      learned how to handle XMP data in images using Aspose.Imagin
  type: HowTo
- questions:
  - answer: XMP is an XML‑based standard for embedding descriptive information directly
      inside files, enabling consistent metadata across applications.
    question: What is XMP metadata?
  - answer: It lets you tag images with author, copyright, keywords, and custom data,
      improving searchability and asset management without external databases.
    question: Why is XMP metadata important?
  - answer: Yes, Aspose.Imaging for Java provides methods to modify existing XMP packets
      and write them back to the file.
    question: Can I edit XMP metadata after embedding it in an image?
  - answer: A free trial is available for evaluation, but a paid license is required
      for production use. You can explore options on the [Aspose.Imaging for Java
      website](https://purchase.aspose.com/buy).
    question: Is Aspose.Imaging for Java a free tool?
  - answer: Visit the [Aspose.Imaging forums](https://forum.aspose.com/) for community
      assistance, or contact Aspose support directly for paid‑license customers.
    question: Where can I get help and support for Aspose.Imaging for Java?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: 'مكتبة معالجة الصور لجافا: XMP مع Aspose.Imaging'
url: /ar/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# معالجة بيانات XMP في الصور باستخدام Aspose.Imaging للـ Java

Aspose.Imaging هي **java image processing library** التي تتيح لك العمل مع العشرات من صيغ الرسوم النقطية والمتجهة. في هذا الدرس ستتعلم كيفية تضمين واسترجاع بيانات XMP (منصة البيانات الوصفية القابلة للتوسيع) في الصور باستخدام Aspose.Imaging للـ Java. في النهاية، ستتمكن من تخزين المؤلف، الوصف، والبيانات الوصفية المخصصة مباشرة داخل ملفات الصور، مما يجعلها قابلة للبحث وتصف نفسها.

## إجابات سريعة
- **What is XMP?** XMP هو تنسيق موحد قائم على XML لتضمين البيانات الوصفية داخل ملفات مثل الصور، PDF، والفيديوهات.  
- **Which library handles XMP in Java?** Aspose.Imaging للـ Java توفر API كامل لقراءة وكتابة حزم XMP.  
- **Do I need a license?** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **How many image formats are supported?** أكثر من 150 صيغة، بما في ذلك TIFF، JPEG، PNG، PSD، و RAW.  
- **Can I process large images?** نعم – يمكن للمكتبة معالجة ملفات تصل إلى 2 GB دون تحميل الصورة بالكامل في الذاكرة.

## ما هو XMP metadata؟
XMP metadata هو معيار قائم على XML يدمج معلومات وصفية مباشرة داخل الملفات الرقمية. يتيح تخزينًا متسقًا للمؤلف، حقوق النشر، الكلمات المفتاحية، والبيانات المخصصة عبر التطبيقات. وبما أنه XML، يمكن توسيع XMP باستخدام مساحات أسماء مخصصة، مما يسمح للمطورين بإضافة حقول مملوكة مع الحفاظ على التوافق مع الأدوات التي تدعم المخطط الأساسي. وهذا يجعل XMP مثاليًا لإدارة الأصول على المدى الطويل والتوافق بين التطبيقات.

## لماذا نستخدم مكتبة معالجة صور جافا لـ XMP؟
Aspose.Imaging للـ Java يدعم **150+ image formats** ويمكنه معالجة ملفات متعددة الجيجابايت بطريقة تدفقية، مما يقلل استهلاك الذاكرة حتى 80 % مقارنة بالتحميل الكامل. تضمن API أيضًا أن حزم XMP تظل متوافقة مع المعايير، مما يضمن التوافق مع Adobe Photoshop و Lightroom وغيرها من الأدوات.

## المتطلبات المسبقة

- بيئة تطوير Java مُعدة على جهازك.  
- مكتبة Aspose.Imaging للـ Java مُثبتة. يمكنك تنزيلها من [موقع Aspose.Imaging للـ Java](https://releases.aspose.com/imaging/java/).  
- فهم أساسي لبرمجة Java.

## استيراد الحزم

ابدأ باستيراد الحزم اللازمة إلى مشروع Java الخاص بك. يمكنك إضافة عبارات الاستيراد التالية في بداية الكود:

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

الآن، دعنا نقسم المثال إلى دليل خطوة بخطوة:

## كيفية تضمين بيانات XMP الوصفية باستخدام مكتبة معالجة صور جافا؟

حمّل صورتك، أنشئ حزمة XMP، أرفق الحزمة بالصورة، واحفظ — كل ذلك في بضع أسطر مختصرة. طريقة `setXmpData` في Aspose.Imaging تكتب الحزمة مباشرةً في الملف دون الحاجة إلى ملف بيانات وصفية منفصل. العملية تعمل مع الصور القائمة على الملفات وكذلك على التدفقات، مما يجعلها مناسبة لخدمات الويب والمهام الدفعية.

### الخطوة 1: تحديد حجم الصورة وخيارات TIFF

أولاً، حدد الدليل الذي سيتم تخزين الصورة فيه وأنشئ كائن `Rectangle` لتحديد حجم الصورة. في هذا المثال، نستخدم صورة TIFF مع بعض الخيارات. `TiffOptions` يضبط إعدادات خاصة بصيغة TIFF.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### الخطوة 2: إنشاء صورة جديدة

الآن، أنشئ صورة جديدة باستخدام الخيارات المحددة. ستُستخدم هذه الصورة لتخزين بيانات XMP الوصفية. `TiffImage` يمثل كائن صورة TIFF، و `TiffFrame` يحدد إطارًا فرديًا داخلها.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### الخطوة 3: إنشاء رأس وتذييل XMP

أنشئ مثيلات لـ XMP‑Header و XMP‑Trailer لبيانات XMP الوصفية. تساعد هذه الرؤوس والتذييلات في تعريف بنية البيانات الوصفية. `XmpHeaderPi` و `XmpTrailerPi` يمثلان القسمين الافتتاحي والإغلاق لحزمة XMP.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### الخطوة 4: إنشاء معلومات XMP الوصفية

الآن، أنشئ مثيلًا لـ XMP meta لتعيين سمات مختلفة. يمكنك إضافة معلومات مثل المؤلف والوصف. `XmpMeta` يحتوي على الحقول الأساسية للبيانات الوصفية مثل المؤلف والوصف.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### الخطوة 5: إنشاء غلاف حزمة XMP

`XmpPacketWrapper` هو الحاوية التي تحتفظ برأس XMP، التذييل، ومعلومات meta في حزمة واحدة. يضمن أن الحزمة تتوافق مع مواصفات XMP. `XmpPacketWrapper` يجمع الرأس، meta، والتذييل في حزمة XMP واحدة.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### الخطوة 6: إضافة حزمة Photoshop

لتخزين معلومات خاصة بـ Photoshop، أنشئ حزمة Photoshop وحدد سماتها مثل المدينة، الدولة، ووضع اللون. ثم أضف هذه الحزمة إلى بيانات XMP الوصفية. `PhotoshopPackage` يخزن بيانات وصفية خاصة بـ Photoshop مثل المدينة، الدولة، ووضع اللون.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### الخطوة 7: إضافة حزمة Dublin Core

للحصول على معلومات أكثر عمومية، مثل المؤلف، العنوان، وقيم إضافية، أنشئ حزمة DublinCore وحدد سماتها. أضف هذه الحزمة إلى بيانات XMP الوصفية أيضًا. `DublinCorePackage` يحتوي على حقول Dublin Core القياسية مثل العنوان، المنشئ، والكلمات المفتاحية.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### الخطوة 8: تحديث بيانات XMP الوصفية في الصورة

قم بتحديث بيانات XMP الوصفية في الصورة باستخدام طريقة `setXmpData`. هذه العملية تكتب حزمة XMP في قسم البيانات الوصفية للصورة. `setXmpData` يكتب حزمة XMP في قسم البيانات الوصفية للصورة.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### الخطوة 9: حفظ الصورة

يمكنك الآن حفظ الصورة مع بيانات XMP المضمنة على القرص أو في تدفق الذاكرة.

```java
    image.save(ms);
```

### الخطوة 10: تحميل الصورة واسترجاع بيانات XMP الوصفية

لاسترجاع بيانات XMP الوصفية من الصورة، حمّل الصورة من تدفق الذاكرة أو القرص واطّلع على بيانات XMP عبر طريقة `getXmpData`. `getXmpData` يقرأ حزمة XMP المضمنة من الصورة.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

تهانينا! لقد تعلمت بنجاح كيفية معالجة بيانات XMP في الصور باستخدام Aspose.Imaging للـ Java. يتيح لك ذلك تخزين واسترجاع بيانات وصفية قيمة داخل ملفات الصور الخاصة بك.

## المشكلات الشائعة والحلول

- **Metadata not appearing in Photoshop:** تأكد من أن حزمة XMP تتبع مخطط XML الصحيح؛ Aspose.Imaging يتحقق منها تلقائيًا، لكن قد تحتاج مساحات الأسماء المخصصة إلى تسجيل.  
- **Large TIFF files cause OutOfMemoryError:** استخدم `TiffOptions` مع تعيين `Compression` إلى `LZW` وفعل التدفق (`loadOptions.setBufferSize`) للحفاظ على انخفاض استهلاك الذاكرة.  
- **Unexpected character encoding:** XMP يتوقع UTF‑8؛ احرص دائمًا على تمرير السلاسل باستخدام `StandardCharsets.UTF_8` لتجنب البيانات المشوشة.

## الأسئلة المتكررة

**س: ما هو XMP metadata؟**  
ج: XMP هو معيار قائم على XML لتضمين معلومات وصفية مباشرة داخل الملفات، مما يتيح بيانات وصفية متسقة عبر التطبيقات.

**س: لماذا بيانات XMP الوصفية مهمة؟**  
ج: تتيح لك وسم الصور بالمؤلف، حقوق النشر، الكلمات المفتاحية، والبيانات المخصصة، مما يحسن قابلية البحث وإدارة الأصول دون الحاجة إلى قواعد بيانات خارجية.

**س: هل يمكن تعديل بيانات XMP الوصفية بعد تضمينها في صورة؟**  
ج: نعم، Aspose.Imaging للـ Java يوفر طرقًا لتعديل حزم XMP الموجودة وإعادة كتابتها إلى الملف.

**س: هل Aspose.Imaging للـ Java أداة مجانية؟**  
ج: تتوفر نسخة تجريبية مجانية للتقييم، لكن يلزم الحصول على ترخيص مدفوع للاستخدام في الإنتاج. يمكنك استكشاف الخيارات على [موقع Aspose.Imaging للـ Java](https://purchase.aspose.com/buy).

**س: أين يمكنني الحصول على المساعدة والدعم لـ Aspose.Imaging للـ Java؟**  
ج: زر [منتديات Aspose.Imaging](https://forum.aspose.com/) للحصول على مساعدة المجتمع، أو تواصل مباشرةً مع دعم Aspose لعملاء الترخيص المدفوع.

## الخلاصة

في هذا الدرس، استكشفنا كيفية العمل مع بيانات XMP الوصفية في الصور باستخدام Aspose.Imaging للـ Java، وهي **java image processing library** رائدة. باتباع دليل الخطوة بخطوة، يمكنك بسهولة تضمين، تحديث، واسترجاع بيانات XMP، مما يثري أصولك الرقمية ببيانات وصفية قابلة للبحث ومتوافقة مع المعايير.

---

**آخر تحديث:** 2026-05-18  
**تم الاختبار مع:** Aspose.Imaging for Java 24.12  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [إتقان معالجة صور Java: تعديل بيانات EXIF باستخدام Aspose.Imaging](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [معالجة صور Java باستخدام Aspose.Imaging: تحميل، تحسين وحفظ الصور](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [معالجة صور Java المتقدمة باستخدام مكتبة Aspose.Imaging](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Specify the size of image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// create the brand new image just for sample purposes
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// create an instance of XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// create an instance of Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// create an instance of XMP meta class to set different attributes
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// create an instance of XmpPacketWrapper that contains all metadata
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// create an instance of Photoshop package and set photoshop attributes
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// add photoshop package into XMP metadata
	xmpData.addPackage(photoshopPackage);
	// create an instance of DublinCore package and set dublinCore attributes
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// add dublinCore Package into XMP metadata
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// update XMP metadata into image
	image.setXmpData(xmpData);
	// Save image on the disk or in memory stream
	image.save(ms);
	// Load the image from memory stream or from disk to read/get the metadata
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Getting the XMP metadata
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Use package data ...
		}
	}
}
        
```