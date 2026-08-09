---
date: '2026-06-28'
description: تعلم كيفية تحويل ODP إلى PNG باستخدام Aspose.Imaging for Java، ضبط الخطوط
  المخصصة، وتعطيل الخطوط النظامية للحصول على عرض دقيق.
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: كيفية تحويل ODP إلى PNG باستخدام Aspose.Imaging for Java – دليل الخطوط المخصصة
  والتصدير
url: /ar/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# كيفية تحويل ODP إلى PNG باستخدام Aspose.Imaging للـ Java – الخطوط المخصصة ودليل التصدير

في تطبيقات Java الحديثة، تحويل ملفات OpenDocument Presentation (ODP) إلى صور PNG عالية الجودة هو مطلب شائع—خاصة عندما تحتاج إلى الحفاظ على العلامة التجارية من خلال الخطوط المخصصة. يوضح هذا الدليل **كيفية تحويل ODP** إلى PNG باستخدام Aspose.Imaging للـ Java، ويشرح لك كيفية تعيين مجلد خطوط مخصص، وتعطيل الخطوط الاحتياطية للنظام، وضبط خيارات الرستر بدقة للحصول على أداء مثالي.

**ما ستتعلمه**
- كيفية تعيين دليل خطوط مخصص لتحويل ODP.  
- كيفية تعطيل الخطوط البديلة للنظام بحيث تُستخدم الخطوط التي تختارها فقط.  
- كيفية تصدير ملف ODP إلى PNG بأبعاد دقيقة وإعدادات الخط.  
- نصائح لتحسين السرعة واستخدام الذاكرة عند معالجة عروض تقديمية كبيرة.

## إجابات سريعة
- **هل يمكنني استخدام Maven لإضافة Aspose.Imaging؟** نعم، أضف تبعية Maven وشغّل `mvn install`.  
- **هل أحتاج إلى ترخيص للإنتاج؟** ترخيص Aspose.Imaging صالح مطلوب للاستخدام غير المحدود.  
- **هل ستحترم الخطوط المخصصة الخاصة بي؟** عيّن مجلد الخطوط وعطّل البدائل النظامية لتطبيقها.  
- **ما هي صيغ الصور المدعومة؟** يدعم Aspose.Imaging أكثر من 120 صيغة رستر ومتجه، بما في ذلك PNG و JPEG و TIFF و WebP.  
- **هل الـ API آمن للاستخدام المتعدد الخيوط؟** نعم، معظم فئات Aspose.Imaging آمنة للاستخدام المتزامن عندما تنشئ مثيلات منفصلة لكل خيط.

## ما هو “كيفية تحويل odp”؟
*“كيفية تحويل odp”* تشير إلى عملية تحويل ملف OpenDocument Presentation إلى صيغة أخرى—غالبًا PNG—مع الحفاظ على التخطيط والخطوط والدقة البصرية. يوفر Aspose.Imaging للـ Java سير عمل بطريقة واحدة يتعامل مع هذا التحويل دون الحاجة إلى أدوات خارجية، مما يتيح للمطورين دمج التحويل مباشرةً في تطبيقاتهم بأقل قدر من الشيفرة.

## لماذا نستخدم Aspose.Imaging للـ Java؟
يدعم Aspose.Imaging **أكثر من 120 صيغة إخراج** ويمكنه رستر ملفات ODP متعددة الصفحات دون تحميل المستند بالكامل في الذاكرة، مما يقلل من استهلاك الذاكرة القصوى بنسبة تصل إلى 70 % في العروض الكبيرة. كما توفر المكتبة إدارة خطوط مدمجة، مما يلغي الحاجة إلى محركات عرض من طرف ثالث.

## المتطلبات المسبقة
- **المكتبات**: Aspose.Imaging للـ Java ≥ 25.5.  
- **JDK**: الإصدار 8 أو أحدث.  
- **IDE**: IntelliJ IDEA أو Eclipse أو أي محرر متوافق مع Java.  
- **المعرفة الأساسية**: Java I/O، البرمجة الكائنية، ومفاهيم الصور.

## تعليمات التثبيت

### Maven
أضف التبعية التالية إلى ملف `pom.xml` الخاص بك وشغّل `mvn clean install`:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
قم بتضمين المكتبة في ملف `build.gradle` الخاص بك وحدث المشروع:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### التحميل المباشر
قم بتنزيل أحدث ملف JAR من [إصدارات Aspose.Imaging للـ Java](https://releases.aspose.com/imaging/java/).

## خطوات الحصول على الترخيص
لفتح جميع الوظائف، قم بتطبيق ترخيص مؤقت أو دائم:

1. **تجربة مجانية** – لا يلزم ترخيص، ميزات محدودة.  
2. **ترخيص مؤقت** – اطلب واحدًا من [موقع Aspose](https://purchase.aspose.com/temporary-license/).  
3. **شراء** – اشترِ اشتراكًا أو ترخيصًا دائمًا من [صفحة شراء Aspose](https://purchase.aspose.com/buy).

قم بتهيئة المكتبة باستخدام ملف الترخيص الخاص بك:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## كيفية تعيين دليل خطوط مخصص لتحويل ODP؟
`FontSettings` هي فئة تدير موارد الخطوط لـ Aspose.Imaging. حمّل خطوطك المخصصة قبل بدء أي معالجة للصور. يضمن ذلك أن كل شريحة تستخدم الخطوط الدقيقة التي توفرها.

عيّن مسار مجلد الخطوط باستخدام `FontSettings` الخاصة بـ Aspose.Imaging:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*مرساة التعريف*: `FontSettings.setFontsFolder` تخبر Aspose.Imaging أين يبحث عن خطوط TrueType و OpenType على نظام الملفات.

## كيفية تعطيل الخطوط البديلة للنظام أثناء تحويل ODP؟
تعطيل البدائل النظامية يجبر محرك العرض على تجاهل الخطوط المثبتة على نظام التشغيل، مما يضمن أن تُستخدم الخطوط التي تزودها فقط. هذا يلغي استبدالات الخط غير المتوقعة التي قد تغير المظهر البصري لشرائحك.

عطّل البدائل النظامية باستخدام الاستدعاء التالي:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*مرساة التعريف*: `FontSettings.setGetSystemAlternativeFont(false)` يجبر المحرك على استخدام الخطوط الموجودة فقط في المجلد الذي حددته، مما يلغي الاستبدالات غير المتوقعة.

## كيفية تصدير ملف ODP إلى PNG بخط محدد؟
`RasterizationOptions` يحدد كيفية رستر الصفحات المتجهة إلى صور نقطية. من خلال دمج إعدادات الخط مع إعدادات الرستر، يمكنك التحكم في DPI، لون الخلفية، وحجم الصفحة لكل PNG مُصدّر.

نفّذ طريقة التصدير كما هو موضح أدناه:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*مرساة التعريف*: فئة `RasterizationOptions` تتحكم في DPI، حجم الصفحة، ولون الخلفية للملفات PNG المُولدة.

### المشكلات الشائعة والحلول
- **ملفات الخط مفقودة** – تحقق من أن كل ملف `.ttf` أو `.otf` المشار إليه في ODP موجود في المجلد الذي حددته.  
- **مسارات ملفات غير صحيحة** – استخدم مسارات مطلقة أو حل المسارات النسبية بالنسبة إلى `System.getProperty("user.dir")`.  
- **أذونات غير كافية** – تأكد من أن عملية Java يمكنها قراءة مجلد الخطوط والكتابة إلى مجلد الإخراج.

## التطبيقات العملية
1. **شرائح متسقة مع العلامة التجارية** – صدّر العروض التقديمية كملفات PNG للنشر على الويب مع الحفاظ على خطوط الشركة.  
2. **إنشاء تقارير آلية** – حوّل كل شريحة إلى صورة لتضمينها في تقارير PDF أو نشرات بريدية.  
3. **إنشاء أرشيف للملفات القديمة** – احفظ محتوى ODP كملفات PNG لضمان إمكانية الوصول في المستقبل دون الحاجة إلى عارضات ODP.

## اعتبارات الأداء
- استخدم أحدث نسخة من Aspose.Imaging للاستفادة من تحسينات الرستر المتعدد الخيوط (حتى 2× أسرع على معالجات 8 نوى).  
- غلف معالجة الصور داخل كتلة `try‑with‑resources` لضمان تحرير الموارد الأصلية في الوقت المناسب.  
- عدّل `RasterizationOptions` (مثلاً، خفض DPI) عند معالجة آلاف الشرائح لتحقيق توازن بين الجودة واستهلاك الذاكرة.

## الأسئلة المتكررة
**س: ما هو الحد الأدنى لإصدار Java المطلوب؟**  
ج: يعمل Aspose.Imaging للـ Java مع JDK 8 وما بعده؛ يُنصح بـ JDK 11 للدعم طويل الأمد.

**س: هل يمكنني تحويل شرائح مختارة فقط؟**  
ج: نعم، عيّن `rasterizationOptions.setPageNumber(specificSlideIndex)` قبل استدعاء `save`.

**س: كيف أتعامل مع ملفات ODP المحمية بكلمة مرور؟**  
ج: حمّل الملف باستخدام `LoadOptions` التي تتضمن كلمة المرور، ثم استمر بنفس إعدادات الخط.

**س: هل يؤثر تعطيل خطوط النظام على الأداء؟**  
ج: يحسن السرعة قليلًا لأن المحرك يتخطى البحث عن خطوط النظام، وهو واضح خصوصًا على الأجهزة التي تحتوي على مجموعة خطوط كبيرة.

**س: أين يمكنني العثور على مزيد من أمثلة الشيفرة؟**  
ج: استكشف [وثائق Aspose.Imaging الرسمية](https://reference.aspose.com/imaging/java/) للحصول على سيناريوهات إضافية مثل التحويل الجماعي وتحويلات الصور.

## موارد إضافية
- [إصدارات Aspose.Imaging للـ Java](https://releases.aspose.com/imaging/java/)  
- [إصدارات Aspose.Imaging](https://releases.aspose.com/imaging/java/)  
- [ابدأ تجربتك المجانية](https://releases.aspose.com/imaging/java/)  
- [وثائق Aspose.Imaging](https://reference.aspose.com/imaging/java/)  
- [منتدى Aspose.Imaging](https://forum.aspose.com/c/imaging/14)  
- [شراء ترخيص Aspose](https://purchase.aspose.com/buy)  
- [التقدم بطلب للحصول على ترخيص مؤقت](https://purchase.aspose.com/temporary-license/)  

---

**آخر تحديث:** 2026-06-28  
**تم الاختبار مع:** Aspose.Imaging للـ Java 25.5  
**المؤلف:** Aspose

## دروس ذات صلة
- [تحويل ODG إلى PNG باستخدام Aspose.Imaging للـ Java: دليل شامل](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [تحويل الصور بكفاءة في Java باستخدام Aspose.Imaging: دليل شامل](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}