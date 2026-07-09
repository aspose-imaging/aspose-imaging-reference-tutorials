---
date: 2026-01-12
description: تعلم كيفية تعديل التباين في صور DICOM – دليل خطوة بخطوة حول كيفية تعديل
  التباين باستخدام Aspose.Imaging للغة Java وتحويل DICOM إلى BMP.
linktitle: DICOM Image Contrast Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: كيفية تعديل التباين في صور DICOM باستخدام Aspose.Imaging للغة Java
url: /ar/java/image-processing-and-enhancement/dicom-image-contrast-adjustment/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تعديل التباين في صور DICOM باستخدام Aspose.Imaging for Java

في التصوير الطبي الحديث، **كيفية تعديل التباين** يمكن أن تكون الفارق بين تشخيص واضح وتفصيل مفقود. يشرح هذا الدليل الخطوات الدقيقة لتعديل التباين في ملفات DICOM باستخدام Aspose.Imaging for Java، ويظهر لك كيفية تحويل تلك الصور إلى BMP لسهولة العرض أو المعالجة الإضافية. في النهاية، ستحصل على مقتطف شفرة جاهز للاستخدام يمكنك إدراجه في أي مشروع Java.

## إجابات سريعة
- **ماذا يفعل تعديل التباين؟** يوسع النطاق بين البكسلات الداكنة والفاتحة، مما يجعل الهياكل تبرز.
- **ما المكتبة المطلوبة؟** Aspose.Imaging for Java.
- **هل يمكنني الإخراج إلى BMP؟** نعم – يمكنك تحويل DICOM إلى BMP بعد تعديل التباين.
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم ترخيص تجاري للاستخدام غير التجريبي.
- **ما نسخة Java المدعومة؟** Java 8 وأحدث.

## ما هو تعديل التباين ولماذا هو مهم؟
يعزز تعديل التباين الفارق البصري بين الميزات التشريحية، مما يساعد أطباء الأشعة على اكتشاف الشذوذ بسرعة أكبر. في سير عمل DICOM، يضمن تعديل التباين قبل التحويل أن يحتفظ ملف BMP بجودة تشخيصية تحتاجها للتقارير أو الأرشفة.

## المتطلبات المسبقة

قبل الغوص في الشفرة، تأكد من أن لديك:

1. **Aspose.Imaging for Java** – قم بتنزيله من الموقع الرسمي [هنا](https://releases.aspose.com/imaging/java/).  
2. **بيئة تطوير Java** – JDK 8+ وIDE المفضلة لديك (IntelliJ, Eclipse, VS Code, إلخ).  
3. **صورة DICOM** – أي ملف .dcm ترغب في تحسينه؛ تتوفر ملفات نموذجية على الإنترنت أو يمكنك استخدام بياناتك السريرية الخاصة.

## استيراد الحزم

هذه الاستيرادات تمنحك الوصول إلى معالجة DICOM وحفظ BMP.

```java
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
```

## كيفية تعديل التباين في صور DICOM

فيما يلي سير العمل الكامل خطوة بخطوة. يتم شرح كل خطوة بلغة بسيطة لتتمكن من المتابعة حتى وإن كنت جديدًا على Aspose.Imaging.

### الخطوة 1: تحديد مسارات الملفات

حدد موقع ملف DICOM المدخل ومسار BMP المطلوب إخراجه. استبدل العنصر النائب بالمسار الفعلي على جهازك.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingContrast_out.bmp";
```

### الخطوة 2: تحميل صورة DICOM

نفتح ملف DICOM باستخدام `FileInputStream`. يضمن كتلة `try‑with‑resources` إغلاق الدفق تلقائيًا.

```java
File file = new File(inputFile);

try (FileInputStream fis = new FileInputStream(file)) {
    try (DicomImage image = (DicomImage) Image.load(fis)) {
        // All further processing happens inside this block
    }
} catch (IOException ex) {
    Logger.println(ex.getMessage());
    ex.printStackTrace();
}
```

### الخطوة 3: تعديل التباين

داخل كتلة `try` الداخلية، استدعِ `adjustContrast`. يمكن أن تتراوح القيمة من **‑100** (تقليل) إلى **+100** (زيادة). في هذا المثال نزيد التباين بمقدار 50 وحدة.

```java
image.adjustContrast(50);
```

### الخطوة 4: تحويل DICOM إلى BMP وحفظ الصورة

بعد تعديل التباين، ننشئ كائن `BmpOptions` ونحفظ النتيجة كملف BMP. هذه الخطوة **تحول DICOM إلى BMP**، مما يمنحك تنسيق نقطي مدعوم على نطاق واسع.

```java
image.save(outputFile, new BmpOptions());
```

## المشكلات الشائعة والنصائح

- **ملف DICOM غير صالح** – تأكد من أن ملف .dcm غير مضغوط بصيغة نقل غير مدعومة. يدعم Aspose.Imaging معظم ترميزات DICOM القياسية.  
- **قيمة التباين خارج النطاق** – القيم التي تتجاوز ±100 تُقيد تلقائيًا؛ اختر رقمًا يناسب هيستوجرام الصورة.  
- **استهلاك الذاكرة** – قد تستهلك سلاسل DICOM الكبيرة كمية كبيرة من RAM. عالج شريحة واحدة في كل مرة إذا واجهت `OutOfMemoryError`.

## الخلاصة

لقد تعلمت الآن **كيفية تعديل التباين** في صور DICOM باستخدام Aspose.Imaging for Java وكيفية **تحويل DICOM إلى BMP** للمهام اللاحقة. هذا سير العمل سريع، موثوق، ويمكن دمجه في خطوط أنابيب الصور الطبية الأكبر، سواء كنت تبني عارض PACS، أداة بحث، أو نظام تقارير آلي.

يُبسط Aspose.Imaging for Java التعامل منخفض المستوى مع DICOM، مما يتيح لك التركيز على القيمة السريرية لصورك.

## الأسئلة المتكررة

**س: ما هو DICOM ولماذا هو المعيار في التصوير الطبي؟**  
ج: DICOM (Digital Imaging and Communications in Medicine) هو الصيغة العالمية لتخزين، نقل، ومشاركة الصور الطبية، مما يضمن التوافق بين الأجهزة والمؤسسات.

**س: هل يمكنني تعديل السطوع مع التباين؟**  
ج: نعم، طريقة `adjustBrightness(int value)` تعمل بطريقة مشابهة ويمكن ربطها قبل الحفظ.

**س: هل يدعم Aspose.Imaging صيغ إخراج أخرى غير BMP؟**  
ج: بالتأكيد – يمكنك التصدير إلى PNG، JPEG، TIFF، والعديد غيرها باستخدام فئة `*Options` المناسبة.

**س: هل يلزم ترخيص تجاري للاستخدام في الإنتاج؟**  
ج: نعم. يمكنك شراء ترخيص [هنا](https://purchase.aspose.com/buy) أو الحصول على ترخيص تجريبي مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني العثور على مزيد من المساعدة والأمثلة؟**  
ج: يوفر منتدى مجتمع Aspose.Imaging for Java وثائق واسعة وأمثلة شفرة: [منتدى Aspose.Imaging for Java](https://forum.aspose.com/).

---

**آخر تحديث:** 2026-01-12  
**تم الاختبار مع:** Aspose.Imaging for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}