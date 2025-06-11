---
"date": "2025-06-03"
"description": "تعرف على كيفية تغيير حجم صور DICOM بشكل متناسب باستخدام Aspose.Imaging لـ .NET، والحفاظ على الجودة والكفاءة في سير عمل التصوير الطبي."
"title": "تغيير حجم صور DICOM المتناسبة باستخدام Aspose.Imaging لـ .NET - دليل شامل"
"url": "/ar/net/medical-imaging-dicom/resize-dicom-images-proportionally-aspose-imaging-net/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# تغيير حجم صور DICOM المتناسبة باستخدام Aspose.Imaging لـ .NET: دليل شامل

## مقدمة
في مجال التصوير الطبي، تُعدّ صور التصوير الرقمي والاتصالات في الطب (DICOM) بالغة الأهمية للتشخيص والتحليل. ومع ذلك، قد تُشكّل هذه الملفات عالية الدقة عبئًا على التخزين أو النقل. سيُرشدك هذا البرنامج التعليمي إلى كيفية تغيير حجم صور DICOM بشكل متناسب باستخدام Aspose.Imaging for .NET، وهي مكتبة متعددة الاستخدامات تُبسّط مهام معالجة الصور.

**ما سوف تتعلمه:**
- تثبيت وإعداد Aspose.Imaging لـ .NET
- تغيير حجم صور DICOM حسب الارتفاع والعرض مع الحفاظ على النسب
- التطبيقات العملية لهذه التقنيات في سير عمل التصوير الطبي

لنستعرض كيفية دمج هذه الوظيفة بسلاسة في مشاريعك. قبل أن نبدأ، تأكد من تجهيز كل ما يلزم لمتابعتها.

## المتطلبات الأساسية
قبل البدء في استخدام Aspose.Imaging لـ .NET، تأكد من أنك قمت بتغطية المتطلبات الأساسية التالية:

1. **المكتبات والإصدارات المطلوبة:**
   - ستحتاج إلى مكتبة Aspose.Imaging لـ .NET.
   - تأكد من أن مشروعك يستهدف إصدارًا متوافقًا من إطار عمل .NET (على سبيل المثال، .NET Core 3.1 أو إصدار أحدث).

2. **إعداد البيئة:**
   - بيئة تطوير AC# مثل Visual Studio.

3. **المتطلبات المعرفية:**
   - فهم أساسي لبرمجة C# والتعرف على مفاهيم معالجة الصور.

## إعداد Aspose.Imaging لـ .NET
للبدء، عليك تثبيت مكتبة Aspose.Imaging في مشروعك. إليك خطوات التثبيت باستخدام مديري حزم مختلفين:

**.NET CLI:**
```shell
dotnet add package Aspose.Imaging
```

**وحدة تحكم مدير الحزمة:**
```shell
Install-Package Aspose.Imaging
```

**واجهة مستخدم مدير حزمة NuGet:**
- ابحث عن "Aspose.Imaging" وقم بتثبيت الإصدار الأحدث.

### الحصول على الترخيص
للاستفادة من جميع ميزات Aspose.Imaging، قد تحتاج إلى الحصول على ترخيص. إليك الطريقة:

- **نسخة تجريبية مجانية:** ابدأ بإصدار تجريبي مجاني لاستكشاف الوظائف الأساسية.
- **رخصة مؤقتة:** الحصول على ترخيص مؤقت من [هنا](https://purchase.aspose.com/temporary-license/) للوصول الموسع أثناء التطوير.
- **شراء:** إذا كنت راضيًا، قم بشراء ترخيص كامل من [هذا الرابط](https://purchase.aspose.com/buy).

بمجرد التثبيت، قم بتهيئة المكتبة عن طريق الرجوع إليها في ملفات مشروعك.

## دليل التنفيذ
دعونا نشرح بالتفصيل كيفية تطبيق تغيير حجم صور DICOM بشكل متناسب باستخدام Aspose.Imaging لـ .NET. سنغطي تعديلات الارتفاع والعرض مع شرح مفصل.

### تغيير حجم صورة DICOM بشكل متناسب مع الارتفاع
سيوضح هذا القسم كيفية تغيير حجم صورة DICOM استنادًا إلى ارتفاعها، مع ضمان الحفاظ على نسبة العرض إلى الارتفاع.

#### ملخص
يحافظ تغيير الحجم النسبي حسب الارتفاع على نسبة العرض إلى الارتفاع الأصلية أثناء ضبط ارتفاع الصورة إلى حجم محدد - وهو أمر مثالي للحفاظ على سلامة الصورة عبر تنسيقات العرض المختلفة.

#### خطوات التنفيذ

**الخطوة 1: تحميل صورة DICOM**
أولاً، افتح ملف DICOM الخاص بك وقم بتحميله باستخدام Aspose.Imaging `DicomImage` فصل.
```csharp
using System;
using System.IO;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;

string dataDir = "YOUR_DOCUMENT_DIRECTORY";
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// فتح ملف DICOM للقراءة
using (var fileStream = new FileStream(dataDir + "/file.dcm\

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}