---
date: '2026-02-22'
description: تعلم كيفية إنشاء PNG متحرك في Java بإضافة تبعية Aspose Imaging Maven،
  وتحويل TIFF إلى APNG وحفظ الصورة كـ APNG.
keywords:
- animated PNG Java
- Aspose.Imaging tutorial
- Java APNG creation
- load save APNG in Java
- animation & multi-frame images
title: إنشاء PNG متحرك في Java – إضافة تبعية Aspose Imaging لـ Maven
url: /ar/java/animation-multi-frame-images/aspose-imaging-java-animated-png-guide/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# إنشاء PNG متحرك Java – إضافة تبعية Aspose Imaging لـ Maven

## المقدمة

هل تتطلع إلى **إنشاء PNG متحرك Java** لتطبيقات تُبهِر المستخدمين برسومات سلسة ومتعددة الإطارات؟ إضافة **aspose imaging maven dependency** تمنحك واجهة برمجة تطبيقات قوية وعالية الأداء لتحميل وتعديل وحفظ ملفات APNG دون الحاجة إلى التعامل مع تعديل البكسلات على مستوى منخفض. سواءً كنت تبني بوابة ويب، أو واجهة سطح مكتب، أو أداة تصور بيانات، يمكن للـ PNG المتحرك أن يجعل واجهتك تبدو عصرية وجذابة.

في هذا الدليل سنستعرض كل ما تحتاجه — من إعداد تبعية Maven إلى تحويل ملف TIFF متعدد الصفحات إلى PNG متحرك والتحكم في توقيت الإطارات. في النهاية، ستكون قادرًا على **إنشاء PNG متحرك Java** بثقة.

## إجابات سريعة
- **ما المكتبة التي تمكّن إنشاء APNG في Java؟** Aspose.Imaging مع تبعية aspose imaging maven dependency.  
- **أي صيغة يمكن تحويلها إلى APNG؟** يمكن تحويل صور TIFF إلى PNG متحركة.  
- **كيف يمكن التحكم في سرعة الرسوم المتحركة؟** استخدم `ApngOptions.setDefaultFrameTime(milliseconds)`.  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** نعم، يلزم وجود ترخيص صالح لـ Aspose.Imaging.  
- **هل يمكنني استخدام Maven أو Gradle؟** كلاهما مدعومان؛ فقط أضف التبعية المناسبة.

## كيف تُنشئ PNG متحرك Java باستخدام Aspose.Imaging؟
توفر Aspose.Imaging واجهة برمجة تطبيقات نظيفة وموجهة كائنيًا تُجردك من تعقيدات صيغة APNG. ببساطة تقوم بتحميل صورة المصدر (غالبًا TIFF متعدد الصفحات)، تُكوّن `ApngOptions`، ثم تستدعي `save`. تتولى المكتبة استخراج الإطارات، وضبط التوقيت، وترميز PNG لك.

## لماذا نستخدم Aspose.Imaging لإنشاء APNG؟
- **معالجة عالية الأداء** – مُحسّنة للصور الكبيرة والرسوم المتحركة متعددة الإطارات.  
- **متعددة المنصات** – تعمل على أي بيئة متوافقة مع JVM.  
- **مجموعة ميزات غنية** – تدعم التحويل، وتوقيت الإطارات، والعديد من صيغ الصور الأخرى.  
- **واجهة برمجة تطبيقات بسيطة** – كود مختصر للمهام المعقدة مثل تحويل TIFF إلى APNG.

## المتطلبات المسبقة
- معرفة أساسية ببرمجة Java.  
- بيئة تطوير متكاملة مثل IntelliJ IDEA أو Eclipse.  
- Maven أو Gradle لإدارة التبعيات (أو ملف JAR).

## إضافة تبعية Maven لـ Aspose Imaging
### Maven
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

لمن يفضّلون التحميل المباشر، يمكنكم الحصول على أحدث نسخة من [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### الحصول على الترخيص
لفتح مجموعة الميزات الكاملة دون حدود التقييم:

- **تجربة مجانية:** ابدأ بتجربة مجانية لاختبار الوظائف.  
- **ترخيص مؤقت:** احصل على ترخيص مؤقت للوصول الموسع أثناء التطوير.  
- **شراء:** للاستخدام طويل الأمد، فكر في شراء المكتبة.

قم بتهيئة الترخيص في الكود الخاص بك:

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path/to/your/license/file.lic");
```

## كيفية تحويل TIFF إلى APNG باستخدام Aspose.Imaging
### تحميل صورة
أولاً، استورد الفئة الأساسية `Image` وحمّل ملف TIFF المصدر:

```java
import com.aspose.imaging.Image;
```

```java
String inputFilePath = "YOUR_DOCUMENT_DIRECTORY/img4.tif";

try (Image image = Image.load(inputFilePath)) {
    // The image is now loaded and ready for manipulation.
}
```

### ضبط مدة الإطار الافتراضية لـ APNG
تحكم في سرعة الرسوم المتحركة عبر تكوين `ApngOptions`:

```java
import com.aspose.imaging.imageoptions.ApngOptions;
```

```java
ApngOptions op = new ApngOptions();
op.setDefaultFrameTime(500); // Default frame time set to 500 milliseconds
```

### حفظ الصورة كـ APNG
جهّز مسار الإخراج واستدعِ `save` مع الخيارات المُكوّنة:

```java
String outputFilePath = "YOUR_OUTPUT_DIRECTORY/img4.tif.500ms.png";
```

```java
try (Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/img4.tif")) {
    ApngOptions op = new ApngOptions();
    op.setDefaultFrameTime(500); // Frame time set to 500 ms
    
    image.save(outputFilePath, op);
}
```

السطر `image.save(outputFilePath, op);` **يحفظ الصورة كـ APNG**. تأكد أن اسم ملف الإخراج ينتهي بـ `.png` وأن `ApngOptions` يعكس توقيت الإطارات المطلوب.

## كيفية حفظ صورة كـ APNG في Java
استدعاء `image.save` المذكور أعلاه هو الأمر الدقيق الذي تحتاجه. عدّل قيمة `setDefaultFrameTime` لتسريع أو إبطاء الرسوم المتحركة. يمكنك أيضًا تجربة صيغ مصدر مختلفة (مثل ملفات PDF متعددة الصفحات) طالما أن Aspose.Imaging يمكنه تحميلها.

## تطبيقات عملية
1. **تطوير الويب** – لافتات متحركة، أيقونات، أو مؤشرات تحميل تعمل عبر المتصفحات دون الحاجة إلى دعم GIF.  
2. **تطبيقات سطح المكتب** – إضفاء حيوية على مكوّنات Swing أو JavaFX بإشارات حركة دقيقة.  
3. **تصور البيانات** – تحريك انتقالات المخططات أو شروحات خطوة بخطوة للتقارير.

استخدم Aspose.Imaging مع مكتبات مثل Swing أو JavaFX أو Spring Boot لتقديم تجربة مستخدم سلسة.

## اعتبارات الأداء
- **إعادة التحجيم بحكمة:** الدقة العالية تزيد من استهلاك الذاكرة؛ قلل الحجم عندما يكون ذلك ممكنًا.  
- **تحرير الموارد فورًا:** استخدم `try‑with‑resources` (كما هو موضح) لتحرير الموارد الأصلية.  
- **المعالجة الدفعية:** إذا كنت تحتاج إلى إنشاء العديد من ملفات APNG، أعد استخدام كائن `License` واحد وتجنّب تحميل ملف المصدر نفسه مرارًا.

## المشكلات الشائعة والحلول
| المشكلة | السبب | الحل |
|-------|-------|-----|
| **OutOfMemoryError** عند تحميل ملفات TIFF الكبيرة | الصورة أكبر من مساحة الذاكرة المتاحة للـ JVM | زد قيمة `-Xmx` أو قلل حجم الصورة قبل المعالجة |
| **إطارات فارغة** في APNG الناتج | صفحات TIFF المصدر لها أبعاد مختلفة | أعد تحجيم جميع الصفحات إلى حجم موحد قبل الحفظ |
| **الترخيص غير مُطبق** | مسار ملف الترخيص غير صحيح | تحقق من المسار وتأكد من إمكانية قراءة الملف أثناء التشغيل |

## الأسئلة المتكررة

**س: ما هي مدة الإطار الافتراضية لـ APNG عند استخدام Aspose.Imaging؟**  
ج: يتم تحديد مدة الإطار عبر `setDefaultFrameTime(int ms)`، ويجب عليك تحديد القيمة بنفسك؛ لا توجد قيمة افتراضية تلقائية.

**س: هل يمكن تعديل سرعة الرسوم المتحركة في ملف APNG موجود؟**  
ج: نعم، يمكنك تحميل الملف، تعديل توقيت الإطارات باستخدام `ApngOptions`، ثم حفظه مرة أخرى كـ APNG.

**س: ما هي بعض المشكلات الشائعة عند تحميل الصور باستخدام Aspose.Imaging؟**  
ج: تأكد من صحة مسار الصورة وتوفر ذاكرة كافية للملفات الكبيرة. يساعد استخدام `try‑with‑resources` في تحرير الذاكرة بسرعة.

**س: كيف أحصل على ترخيص تجريبي مجاني لـ Aspose.Imaging؟**  
ج: زر [صفحة تنزيل Aspose](https://releases.aspose.com/imaging/java/) للحصول على النسخة التجريبية.

**س: هل يمكن دمج Aspose.Imaging مع مكتبات Java أخرى؟**  
ج: بالتأكيد، يمكنك استخدامها جنبًا إلى جنب مع أطر مثل Spring أو مكتبات مثل Apache Commons لتوسيع نطاق تطبيقك.

## موارد

- **التوثيق:** [Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)  
- **التنزيل:** [Latest Release Download](https://releases.aspose.com/imaging/java/)  
- **الشراء:** [Buy Aspose.Imaging](https://purchase.aspose.com/buy)  
- **التجربة المجانية:** [Get Started with Free Trial](https://releases.aspose.com/imaging/java/)  
- **الترخيص المؤقت:** [Acquire Temporary License](https://purchase.aspose.com/temporary-license/)  
- **منتدى الدعم:** [Aspose Community Support](https://forum.aspose.com/c/imaging/14)

---

**آخر تحديث:** 2026-02-22  
**تم الاختبار مع:** Aspose.Imaging 25.5 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}