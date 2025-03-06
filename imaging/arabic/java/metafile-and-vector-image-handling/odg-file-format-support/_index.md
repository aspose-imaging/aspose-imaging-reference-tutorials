---
title: قم بتحويل ODG إلى PNG وPDF باستخدام Aspose.Imaging لـ Java
linktitle: دعم تنسيق ملف ODG
second_title: Aspose.Imaging واجهة برمجة تطبيقات معالجة الصور لجافا
description: تعرف على كيفية تحويل ملفات ODG إلى PNG وPDF باستخدام Aspose.Imaging لـ Java. اتبع دليلنا خطوة بخطوة للتحويل الفعال.
weight: 12
url: /ar/java/metafile-and-vector-image-handling/odg-file-format-support/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# قم بتحويل ODG إلى PNG وPDF باستخدام Aspose.Imaging لـ Java

في عالم تحويل المستندات، يبرز Aspose.Imaging for Java كأداة قوية تتيح لك تحويل ملفات ODG (OpenDocument Graphics) بسهولة إلى تنسيقات PNG وPDF. سيرشدك هذا البرنامج التعليمي خلال العملية خطوة بخطوة، باستخدام Aspose.Imaging for Java. سواء كنت مطورًا أو مجرد شخص يتطلع إلى تحويل ملفات ODG، ستساعدك هذه المقالة على تحقيق هدفك.

## المتطلبات الأساسية

قبل أن نتعمق في عملية التحويل، ستحتاج إلى التأكد من توفر المتطلبات الأساسية التالية:

### 1. بيئة تطوير جافا

 تأكد من إعداد بيئة تطوير Java على نظامك. يمكنك تنزيل وتثبيت أحدث إصدار من Java Development Kit (JDK) من[موقع أوراكل](https://www.oracle.com/java/technologies/javase-downloads).

### 2. Aspose.Imaging لجافا

 ستحتاج إلى تنزيل Aspose.Imaging لـ Java وتثبيته. يمكنك العثور على أحدث إصدار على[صفحة تنزيل Aspose.Imaging لـ Java](https://releases.aspose.com/imaging/java/).

### 3. ملفات ODG

وبطبيعة الحال، سوف تحتاج إلى ملفات ODG التي تريد تحويلها. تأكد من توفر هذه الملفات في دليل على نظامك.

## حزم الاستيراد

الآن بعد أن حصلت على المتطلبات الأساسية، فلنبدأ باستيراد الحزم الضرورية في مشروع Java الخاص بك. ستسمح لك هذه الحزم بالعمل مع Aspose.Imaging for Java بفعالية.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.SizeF;
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
```

سنقوم الآن بتقسيم عملية التحويل إلى خطوات بسيطة لتسهيل متابعتها. لكل خطوة، سنقدم عنوانًا وشرحًا.

## الخطوة 1: تحديد دليل البيانات الخاص بك

 ابدأ بتحديد الدليل الذي توجد به ملفات ODG الخاصة بك. سوف تحتاج إلى استبدال`"Your Document Directory"` مع المسار الفعلي إلى الدليل الخاص بك.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

## الخطوة 2: تحديد ملفات ODG

قم بإنشاء مصفوفة من أسماء ملفات ODG التي تريد تحويلها. استبدل أسماء ملفات الأمثلة بأسماء ملفات ODG الخاصة بك.

```java
String[] files = new String[] {"example.odg", "example1.odg"};
```

## الخطوة 3: تكوين خيارات التنقيط

قم بإعداد خيارات التنقيط لملفات ODG. ستحدد هذه الخيارات حجم الصفحة وإعدادات تنقيط المتجهات.

```java
final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
```

## الخطوة 4: حلقة من خلال ملفات ODG

الآن، قم بالتكرار خلال كل ملف ODG، وقم بتحميله، وقم بتحويله إلى تنسيقات PNG وPDF.

```java
for (String file : files) {
    String fileName = dataDir + file;
    try (Image image = Image.load(fileName)) {
        rasterizationOptions.setPageSize(new SizeF(image.getWidth(), image.getHeight()));

        // تحويل إلى PNG
        String outFileName = "Your Document Directory" + file.replace(".odg", ".png");
        image.save(outFileName, new PngOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});

        // تحويل إلى قوات الدفاع الشعبي
        outFileName = "Your Document Directory" + file.replace(".odg", ".pdf");
        image.save(outFileName, new PdfOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});
    }
}
```

تهانينا! لقد نجحت في تحويل ملفات ODG إلى تنسيقات PNG وPDF باستخدام Aspose.Imaging for Java.

## خاتمة

يعمل Aspose.Imaging for Java على تبسيط عملية تحويل ملفات ODG إلى تنسيقات صور مدعومة على نطاق أوسع مثل PNG وPDF. باتباع الخطوات الموضحة في هذا البرنامج التعليمي، يمكنك إجراء هذه التحويلات بكفاءة في مشاريع Java الخاصة بك.

## الأسئلة الشائعة

### س1: هل Aspose.Imaging for Java أداة مجانية؟

 ج1: لا، Aspose.Imaging for Java هي مكتبة تجارية، ويمكنك العثور على معلومات التسعير على الموقع[صفحة الشراء](https://purchase.aspose.com/buy).

### س2: هل يمكنني تجربة Aspose.Imaging لـ Java قبل الشراء؟

 ج2: نعم، يمكنك تنزيل نسخة تجريبية مجانية من[هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على دعم Aspose.Imaging لـ Java؟

 ج3: يمكنك طلب المساعدة وطرح الأسئلة على الموقع[Aspose.منتدى التصوير](https://forum.aspose.com/).

### س 4: ما هي تنسيقات الملفات الأخرى التي يمكن لـ Aspose.Imaging for Java التعامل معها؟

 ج4: يدعم Aspose.Imaging for Java نطاقًا واسعًا من تنسيقات الصور والمستندات، بما في ذلك BMP وJPEG وTIFF وPDF والمزيد. الرجوع إلى[توثيق](https://reference.aspose.com/imaging/java/) للحصول على قائمة شاملة.

### س5: هل يمكنني استخدام Aspose.Imaging for Java في مشاريعي التجارية؟

ج5: نعم، يمكنك استخدام Aspose.Imaging for Java في المشاريع التجارية بعد شراء الترخيص المناسب.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
