---
"description": "تعرّف على كيفية تحويل ملفات ODG إلى PNG وPDF باستخدام Aspose.Imaging لجافا. اتبع دليلنا خطوة بخطوة لتحويل فعّال."
"linktitle": "دعم تنسيق ملف ODG"
"second_title": "واجهة برمجة تطبيقات معالجة الصور Java Aspose.Imaging"
"title": "تحويل ODG إلى PNG وPDF باستخدام Aspose.Imaging لـ Java"
"url": "/ar/java/metafile-and-vector-image-handling/odg-file-format-support/"
"weight": 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# تحويل ODG إلى PNG وPDF باستخدام Aspose.Imaging لـ Java

في عالم تحويل المستندات، يبرز Aspose.Imaging for Java كأداة فعّالة تُمكّنك من تحويل ملفات ODG (رسومات OpenDocument) بسهولة إلى صيغتي PNG وPDF. سيرشدك هذا البرنامج التعليمي خلال العملية خطوة بخطوة باستخدام Aspose.Imaging for Java. سواء كنت مطورًا أو شخصًا يبحث عن تحويل ملفات ODG، ستساعدك هذه المقالة على تحقيق هدفك.

## المتطلبات الأساسية

قبل أن نتعمق في عملية التحويل، ستحتاج إلى التأكد من توفر المتطلبات الأساسية التالية:

### 1. بيئة تطوير جافا

تأكد من تثبيت بيئة تطوير جافا على نظامك. يمكنك تنزيل وتثبيت أحدث إصدار من مجموعة تطوير جافا (JDK) من [موقع أوراكل](https://www.oracle.com/java/technologies/javase-downloads).

### 2. Aspose.Imaging لـ Java

ستحتاج إلى تنزيل وتثبيت Aspose.Imaging لجافا. يمكنك العثور على أحدث إصدار على [صفحة تنزيل Aspose.Imaging لـ Java](https://releases.aspose.com/imaging/java/).

### 3. ملفات ODG

بالطبع، ستحتاج إلى ملفات ODG التي تريد تحويلها. تأكد من توفر هذه الملفات في مجلد على نظامك.

## استيراد الحزم

بعد أن أصبحت لديك المتطلبات الأساسية، لنبدأ باستيراد الحزم اللازمة لمشروع جافا. ستتيح لك هذه الحزم العمل مع Aspose.Imaging for Java بفعالية.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.SizeF;
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
```

سنُقسّم الآن عملية التحويل إلى خطوات بسيطة ليسهل متابعتها. سنُقدّم لكل خطوة عنوانًا وشرحًا.

## الخطوة 1: تحديد دليل البيانات الخاص بك

ابدأ بتحديد الدليل الذي توجد فيه ملفات ODG. ستحتاج إلى استبدال `"Your Document Directory"` مع المسار الفعلي إلى الدليل الخاص بك.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

## الخطوة 2: تحديد ملفات ODG

أنشئ مصفوفة من أسماء ملفات ODG التي ترغب في تحويلها. استبدل أسماء الملفات النموذجية بأسماء ملفات ODG الخاصة بك.

```java
String[] files = new String[] {"example.odg", "example1.odg"};
```

## الخطوة 3: تكوين خيارات التنقيح

اضبط خيارات التبخير لملفات ODG. ستحدد هذه الخيارات حجم الصفحة وإعدادات التبخير للمتجهات.

```java
final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
```

## الخطوة 4: تكرار ملفات ODG

الآن، قم بتكرار كل ملف ODG، وقم بتحميله، وتحويله إلى تنسيقي PNG وPDF.

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

        // تحويل إلى PDF
        outFileName = "Your Document Directory" + file.replace(".odg", ".pdf");
        image.save(outFileName, new PdfOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});
    }
}
```

تهانينا! لقد نجحت في تحويل ملفات ODG إلى صيغتي PNG وPDF باستخدام Aspose.Imaging لـ Java.

## خاتمة

يُبسّط Aspose.Imaging for Java عملية تحويل ملفات ODG إلى صيغ صور مدعومة على نطاق أوسع، مثل PNG وPDF. باتباع الخطوات الموضحة في هذا البرنامج التعليمي، يمكنك إجراء هذه التحويلات بكفاءة في مشاريع Java الخاصة بك.

## الأسئلة الشائعة

### س1: هل Aspose.Imaging for Java أداة مجانية؟

ج1: لا، Aspose.Imaging for Java عبارة عن مكتبة تجارية، ويمكنك العثور على معلومات التسعير على [صفحة الشراء](https://purchase.aspose.com/buy).

### س2: هل يمكنني تجربة Aspose.Imaging لـJava قبل الشراء؟

ج2: نعم، يمكنك تنزيل نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على الدعم لـ Aspose.Imaging لـ Java؟

ج3: يمكنك طلب المساعدة وطرح الأسئلة على [منتدى Aspose.Imaging](https://forum.aspose.com/).

### س4: ما هي تنسيقات الملفات الأخرى التي يمكن لـ Aspose.Imaging for Java التعامل معها؟

A4: يدعم Aspose.Imaging for Java مجموعة واسعة من تنسيقات الصور والمستندات، بما في ذلك BMP وJPEG وTIFF وPDF وغيرها. راجع [التوثيق](https://reference.aspose.com/imaging/java/) للحصول على قائمة شاملة.

### س5: هل يمكنني استخدام Aspose.Imaging لـ Java في مشاريعي التجارية؟

ج5: نعم، يمكنك استخدام Aspose.Imaging for Java في المشاريع التجارية بعد شراء الترخيص المناسب.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}