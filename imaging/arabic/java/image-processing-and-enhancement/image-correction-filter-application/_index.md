---
date: 2026-01-14
description: تعلم كيفية تحسين الصور باستخدام Aspose.Imaging للغة جافا، بما في ذلك
  كيفية تطبيق الفلاتر وتوضيح الصورة باستخدام كود جافا في هذا الدليل خطوة بخطوة.
linktitle: Image Correction Filter Application
second_title: Aspose.Imaging Java Image Processing API
title: كيفية تحسين الصور باستخدام Aspose.Imaging لجافا
url: /ar/java/image-processing-and-enhancement/image-correction-filter-application/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# تطبيق مرشح تصحيح الصورة باستخدام Aspose.Imaging للـ Java

في عالم الصور الرقمية، الحاجة إلى تصحيح الصور وتعزيزها موجودة دائمًا. سواء كنت مصورًافًا، مصممًا جرافيكيًا، أو شخصًا يستمتع بتعديل صوره، فإن معرفة **how to enhance photos** أمر أساسي. Aspose.Imaging للـ Java هي مكتبة قوية يمكنها مساعدتك في تحقيق ذلك. في هذا الدليل خطوة بخطوة، سنرشدك إلى تطبيق مرشحات التصحيح، ضبط التباين، وحتى كود **sharpen image Java** للحصول على أفضل نتيجة ممكنة.

## إجابات سريعة
- **What does the filter do?** يقوم بتمليس الضوضاء وتوضيح التفاصيل في تمريرة واحدة.  
- **Do I need a license?** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **Which Java version is supported?** Java 8 وأعلى.  
- **Can I change filter strength?** نعم – تسمح لك معلمات المُنشئ بضبط التمليس والتوضيح.  
- **Is the output format flexible?** يمكنك الحفظ بصيغة JPEG أو PNG أو BMP أو TIFF بتغيير امتداد الملف.

## كيفية تحسين الصور باستخدام Aspose.Imaging للـ Java
قبل أن نغوص في الكود، دعنا نتحدث باختصار عن أهمية ذلك. تحسين الصور برمجيًا يوفر ساعات مقارنةً بالتحرير اليدوي، خاصةً عندما تحتاج إلى معالجة دفعات من الصور لكاتالوجات التجارة الإلكترونية أو وسائل التواصل الاجتماعي أو أرشيفات التصوير الطبي. المرشحات التي سنستخدمها—التمليس الثنائي الاتجاه والتوضيح—مثالية لتقليل الضوضاء مع الحفاظ على الحواف، مما يمنح صورك مظهرًا حادًا واحترافيًا.

## المتطلبات المسبقة

1. **Java Development Environment** – قم بتثبيت JDK من [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads).  
2. **Aspose.Imaging for Java** – حمّل المكتبة من [website](https://releases.aspose.com/imaging/java/).  
3. **Image Files** – احرص على أن تكون الصور التي تريد تحسينها جاهزة في مجلد يمكنك الإشارة إليه من الكود الخاص بك.

الآن بعد أن تم إعداد كل شيء، لنبدأ بالبرمجة.

## استيراد الحزم

للعمل مع Aspose.Imaging تحتاج إلى استيراد عدد من الفئات. أدناه قائمة الاستيراد الدقيقة التي ستضعها في أعلى ملف Java الخاص بك.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.imagefilters.filteroptions.BilateralSmoothingFilterOptions;
import com.aspose.imaging.imagefilters.filteroptions.SharpenFilterOptions;
import com.aspose.imaging.Rectangle;
```

## دليل خطوة‑بخطوة

### الخطوة 1: تحميل الصورة

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "aspose-logo.jpg"))
{
    // Your code for image loading goes here
}
```

استبدل `"Your Document Directory"` بالمسار الفعلي للمجلد الذي يحتوي على الصورة المصدر.

### الخطوة 2: الحصول على حدود الصورة

```java
com.aspose.imaging.Rectangle rect = rasterImage.getBounds();
```

معرفة حدود الصورة يتيح لنا تطبيق المرشحات على الصورة بالكامل.

### الخطوة 3: تعريف مرشحات التصحيح

```java
com.aspose.imaging.imagefilters.filteroptions.BilateralSmoothingFilterOptions bilateralOptions =
        new com.aspose.imaging.imagefilters.filteroptions.BilateralSmoothingFilterOptions(3);

com.aspose.imaging.imagefilters.filteroptions.SharpenFilterOptions sharpenOptions =
        new com.aspose.imaging.imagefilters.filteroptions.SharpenFilterOptions();
```

هنا نقوم بإنشاء مرشح **bilateral smoothing** (ممتاز لتقليل الضوضاء) ومرشح **sharpen** – مثال **sharpen image java** الكلاسيكي.

### الخطوة 4: تطبيق المرشحات

```java
rasterImage.filter(rect, bilateralOptions);
rasterImage.filter(rect, sharpenOptions);
```

يتم تطبيق كلا المرشحين على المستطيل الذي حصلنا عليه مسبقًا.

### الخطوة 5: ضبط التباين

```java
rasterImage.adjustContrast(-10);
```

لا تتردد في تجربة قيمة التباين؛ الأرقام السالبة تُظلم الظلال، بينما الأرقام الموجبة تعزز الإضاءات.

### الخطوة 6: ضبط السطوع باستخدام Binarize Bradley

```java
rasterImage.binarizeBradley(80);
```

يعمل بائناري برادلي جيدًا لضبط السطوع بشكل موحد.

### الخطوة 7: حفظ الصورة المصححة

```java
rasterImage.save("Your Document Directory" + "a1_out.jpg");
```

تم الآن تخزين صورتك المحسنة في المجلد المحدد للإخراج.

## كيفية تطبيق المرشح في Java – نصائح وحيل
- **Filter Order Matters:** قم بتطبيق التمليس قبل التوضيح لتجنب تضخيم الضوضاء.  
- **Parameter Tuning:** معلمة المُنشئ لـ `BilateralSmoothingFilterOptions` تتحكم في نصف قطر التمليس؛ القيم الأعلى تعطي نتائج أكثر سلاسة ولكن قد تمحو التفاصيل الدقيقة.  
- **Batch Processing:** ضع الخطوات السابقة داخل حلقة لمعالجة دليل كامل من الصور تلقائيًا.

## المشكلات الشائعة والحلول
- **OutOfMemoryError:** استخدم `try‑with‑resources` (كما هو موضح) وعالج الصور الكبيرة على شكل مربعات إذا كانت الذاكرة محدودة.  
- **Unsupported Format:** تأكد من أن تنسيق الملف المدخل مدعوم من Aspose.Imaging (مثل JPEG، PNG، BMP، TIFF).  
- **License Not Found:** إذا ظهرت لك رسالة تحذير عن وضع التقييم، ضع ملف الترخيص في جذر المشروع وحمّله باستخدام `License license = new License(); license.setLicense("Aspose.Imaging.lic");`.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.Imaging للـ Java في المشاريع التجارية؟

**ج1:** نعم، Aspose.Imaging للـ Java متاح للاستخدام التجاري. يمكنك الحصول على ترخيص من [website](https://purchase.aspose.com/buy).

### س2: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Imaging للـ Java؟

**ج2:** نعم، يمكنك تنزيل نسخة تجريبية مجانية من [here](https://releases.aspose.com/).

### س3: أين يمكنني العثور على وثائق إضافية ودعم لـ Aspose.Imaging للـ Java؟

**ج3:** يمكنك الرجوع إلى الوثائق على [Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/) والحصول على الدعم عبر [Aspose.Imaging forum](https://forum.aspose.com/).

### س4: ما هي بعض حالات الاستخدام الشائعة لتصحيح الصور في Aspose.Imaging للـ Java؟

**ج4:** يُستخدم تصحيح الصور غالبًا في التصوير الفوتوغرافي، التصميم الجرافيكي، والتصوير الطبي لتحسين جودة الصور لأغراض مختلفة.

### س5: هل يمكنني دمج Aspose.Imaging للـ Java مع مكتبات أو أطر عمل Java أخرى؟

**ج5:** نعم، يمكن دمج Aspose.Imaging للـ Java مع مكتبات وأطر عمل Java أخرى لتوسيع وظائفه وإمكاناته.

### أسئلة وإجابات إضافية

**س:** كيف يختلف مرشح التمليس الثنائي الاتجاه عن التمليس البسيط؟  
**ج:** يقلل التمليس الثنائي الاتجاه من الضوضاء مع الحفاظ على الحواف، على عكس تمليس Gaussian الذي يمسح كل شيء بشكل موحد.

**س:** هل يمكنني ضبط شدة التوضيح؟  
**ج:** مُنشئ `SharpenFilterOptions` يقبل معلمات نصف القطر والكمية؛ تعديل هذه القيم يتيح لك التحكم في قوة تأثير التوضيح.

---

**Last Updated:** 2026-01-14  
**Tested With:** Aspose.Imaging for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}