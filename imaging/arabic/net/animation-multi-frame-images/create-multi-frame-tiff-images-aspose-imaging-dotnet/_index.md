---
date: '2026-02-09'
description: تعلم كيفية تحويل JPEG إلى TIFF وإنشاء صور TIFF متعددة الإطارات باستخدام
  Aspose.Imaging لـ .NET. يتضمن الإعداد، تكوين TiffOptions، تحميل الصور من الدليل،
  ومعالجة الإطارات.
keywords:
- create multi-frame tiff images
- Aspose.Imaging for .NET tutorial
- configure TiffOptions in .NET
title: كيفية تحويل JPEG إلى TIFF وإنشاء صور TIFF متعددة الإطارات باستخدام Aspose.Imaging
  لـ .NET
url: /ar/net/animation-multi-frame-images/create-multi-frame-tiff-images-aspose-imaging-dotnet/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# كيفية تحويل JPEG إلى TIFF وإنشاء صور TIFF متعددة الإطارات باستخدام Aspose.Imaging لـ .NET

## المقدمة

هل ترغب في إتقان فن **convert JPEG to TIFF** مع بناء ملفات TIFF متعددة الإطارات باستخدام Aspose.Imaging لـ .NET؟ سيوجهك هذا الدرس الشامل خلال إعداد بيئتك، وتكوين `TiffOptions`، وتغيير حجم ملفات JPEG، وإضافة إطارات إلى صورة TIFF — بكل سهولة. سواء كنت تدير أرشيف المستندات أو تدمج التصوير عالي الجودة في تطبيقات البرمجيات، فإن هذا الدليل مصمم لتعزيز سير عملك.

**ما ستتعلمه:**
- كيفية إعداد Aspose.Imaging لـ .NET
- تكوين `TiffOptions` للصور بالأبيض والأسود باستخدام ضغط CCITT Fax Group 3
- تحميل وتغيير حجم ملفات JPEG من دليل
- إضافة إطارات إلى صورة TIFF
- حفظ صور TIFF متعددة الإطارات

لنغص في المتطلبات المسبقة للبدء.

## إجابات سريعة
- **ماذا يعني “convert JPEG to TIFF”?** يعني أخذ صورة نقطية JPEG وحفظها بصيغة TIFF، غالبًا مع ضغط مخصص أو إطارات متعددة.  
- **أي مكتبة تتعامل مع هذا بأفضل شكل في .NET؟** توفر Aspose.Imaging لـ .NET واجهة برمجة تطبيقات غنية للتحويل وتغيير الحجم وإنشاء الإطارات المتعددة.  
- **هل أحتاج إلى رخصة؟** النسخة التجريبية المجانية تعمل للتقييم؛ الرخصة الدائمة تزيل جميع قيود التقييم.  
- **هل يمكنني تحميل الصور من دليل تلقائيًا؟** نعم – يوضح الدرس كيفية تعداد ملفات JPEG ومعالجة كل منها.  
- **هل الكود متوافق مع .NET 6+؟** بالتأكيد – يستخدم العينة واجهات برمجة تطبيقات .NET Core/5+ التي تعمل على .NET 6 وما بعده.

## ما هو “convert JPEG to TIFF”؟
يتضمن تحويل JPEG إلى TIFF فك ترميز ملف JPEG، وربما تحويله (مثل تغيير الحجم أو عمق اللون)، ثم ترميز النتيجة كملف TIFF. يدعم TIFF إطارات متعددة، وضغط بدون فقدان، وبيانات وصفية لا تتوفر في JPEG، مما يجعله مثاليًا للأرشفة والسيناريوهات متعددة الصفحات.

## لماذا نستخدم Aspose.Imaging لهذا التحويل؟
- **تحكم كامل** في الضغط، وتفسير الفوتومتري، وتنسيق البكسل.  
- **دعم متعدد الإطارات** – يمكنك تجميع عدة صفحات JPEG في مستند TIFF واحد.  
- **متعدد المنصات** – يعمل على Windows وLinux وmacOS مع .NET Core/5+.  
- **بدون تبعيات خارجية** – كود مُدار نقي، لا توجد ملفات DLL أصلية.

## المتطلبات المسبقة

قبل الغوص في إنشاء صور TIFF باستخدام Aspose.Imaging، تأكد من توفر ما يلي.

### المكتبات والاعتمادات المطلوبة
- **Aspose.Imaging لـ .NET**: قم بتثبيت هذه المكتبة باستخدام NuGet أو مدير الحزم المفضل لديك.

### متطلبات إعداد البيئة
- بيئة تطوير تدعم C# و .NET Core/5+

### المتطلبات المعرفية
- فهم أساسي لمفاهيم برمجة C#
- الإلمام بالتعامل مع ملفات الصور في .NET

## إعداد Aspose.Imaging لـ .NET

للبدء، تحتاج إلى تثبيت Aspose.Imaging. إليك الطريقة:

**.NET CLI**
```shell
dotnet add package Aspose.Imaging
```

**Package Manager**
```powershell
Install-Package Aspose.Imaging
```

**واجهة مدير حزم NuGet**  
ابحث عن "Aspose.Imaging" وقم بتثبيت أحدث نسخة.

### خطوات الحصول على الرخصة
- **نسخة تجريبية مجانية**: الوصول إلى نسخة ذات وظائف محدودة لاختبار الميزات.  
- **رخصة مؤقتة**: احصل عليها لتجربة ممتدة بدون قيود التقييم. زر [رخصة مؤقتة](https://purchase.aspose.com/temporary-license/).  
- **شراء**: للوصول الكامل، فكر في شراء رخصة عبر [شراء Aspose.Imaging](https://purchase.aspose.com/buy).

### التهيئة الأساسية والإعداد

```csharp
// Initialize the library with your license
Aspose.Imaging.License license = new Aspose.Imaging.License();
license.SetLicense("Path to your license file");
```

## كيفية تحويل JPEG إلى TIFF وإضافة إطارات متعددة

دعنا نقسم التنفيذ إلى أقسام قابلة للإدارة.

### إنشاء وتكوين TiffOptions لصورة TIFF

#### نظرة عامة
إنشاء كائن `TiffOptions` يتيح لك تحديد إعدادات مثل الضغط وتفسير الفوتومتري، وهو أمر أساسي لتخصيص ملفات TIFF الخاصة بك.

#### تنفيذ خطوة بخطوة

**1. استيراد المساحات الاسمية الضرورية**  
تأكد من تضمين هذه المساحات الاسمية في ملفك:

```csharp
using Aspose.Imaging.FileFormats.Tiff;
using Aspose.Imaging.FileFormats.Tiff.Enums;
using Aspose.Imaging.ImageOptions;
```

**2. تكوين TiffOptions**  
قم بإعداد كائن `TiffOptions` بتكوينات محددة لصورة بالأبيض والأسود باستخدام ضغط CCITT Fax Group 3.

```csharp
// Create TiffOptions with default settings
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);

// Set bits per sample to 1 (black and white)
outputSettings.BitsPerSample = new ushort[] { 1 };

// Use CCITT Fax Group 3 compression
outputSettings.Compression = TiffCompressions.CcittFax3;

// Define photometric interpretation as MinIsWhite
outputSettings.Photometric = TiffPhotometrics.MinIsWhite;

// Set source to an empty stream for creating new TIFF from scratch
outputSettings.Source = new Aspose.Imaging.Sources.StreamSource(new System.IO.MemoryStream());
```

### إنشاء وتكوين TiffImage بأبعاد محددة

#### نظرة عامة
إنشاء `TiffImage` يتضمن تعيين أبعاد مخصصة، وهو أمر حاسم عند تحديد حجم كل إطار TIFF.

**1. تعريف أبعاد الصورة**

```csharp
int newWidth = 500; // Width for each TIFF frame
int newHeight = 500; // Height for each TIFF frame
string path = "@YOUR_OUTPUT_DIRECTORY\\AddFramesToTIFFImage_out.tif";
```

**2. إنشاء مثال TiffImage**  
قم بتهيئة `TiffImage` بالأبعاد المحددة وإعدادات الإخراج.

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    // Logic to add frames will be added here.
}
```

### تحميل ملفات JPEG من الدليل وتغيير حجمها

#### نظرة عامة
تحميل صور JPEG، وتغيير حجمها، والتحضير لإدراجها في ملف TIFF يتم بسلاسة باستخدام Aspose.Imaging.

**1. تحميل صور JPEG**

```csharp
string dataDir = "@YOUR_DOCUMENT_DIRECTORY"; // Directory containing input images

foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
{
    using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
    {
        // Resize image to match TIFF frame dimensions
        ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
        
        // Additional logic for handling multiple frames will be added here.
    }
}
```

> **نصيحة احترافية:** العبارة **load images from directory** هي بالضبط ما يفعله الحلقة أعلاه – إنها تعد كل ملف JPEG في المجلد المستهدف.

### إضافة إطار إلى TiffImage وحفظه

#### نظرة عامة
إضافة إطارات إلى صورة TIFF يتضمن نسخ بكسلات JPEG المعاد تحجيمها إلى كل إطار وحفظ TIFF متعدد الإطارات بالكامل.

**1. تهيئة مثال TiffImage**

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    int index = 0; // Frame index tracker
    
    foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
    {
        using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
        {
            ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
            
            TiffFrame frame = tiffImage.ActiveFrame;
            if (index > 0)
            {
                // Create a new frame for each subsequent image
                frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            }
            
            // Copy pixels from the resized JPEG into the TIFF frame
            frame.SavePixels(frame.Bounds, ri.LoadPixels(ri.Bounds));
            if (index > 0)
            {
                tiffImage.AddFrame(frame); // Add to TIFF image only after the first frame
            }
            index++;
        }
    }
    
    tiffImage.Save(path); // Save the final TIFF with all frames
}
```

## التطبيقات العملية

1. **أرشفة المستندات** – تخزين المستندات الممسوحة كملف TIFF واحد لضمان سلامة البيانات وسهولة الوصول.  
2. **التصوير الطبي** – استخدام صيغ TIFF عالية الجودة ومضغوطة لتخزين الفحوصات مثل MRIs وCTs.  
3. **التصميم الجرافيكي** – دمج طبقات تصميم متعددة في ملف واحد لتسهيل التعامل في برامج التصميم.  
4. **التصوير الفوتوغرافي** – أرشفة ألبومات صور متعددة الصفحات كملفات واحدة لتسهيل المشاركة والتخزين.  
5. **التحكم الصناعي في الجودة** – تسجيل بيانات الفحص التفصيلية عبر إطارات متعددة في صورة TIFF.

## اعتبارات الأداء

### نصائح لتحسين الأداء
- **إدارة الذاكرة** – تخلص من كائنات الصورة فورًا (عبارات `using`) لتحرير الموارد.  
- **المعالجة الدفعية** – عالج الصور على دفعات إذا كنت تتعامل مع مجموعات بيانات كبيرة للحفاظ على استهلاك الذاكرة متوقعًا.  
- **ضغط فعال** – اختر إعدادات الضغط التي توازن بين الجودة والسرعة وفقًا لسيناريوك.

## الأسئلة المتكررة

**س: هل يمكنني تحويل JPEG إلى TIFF دون فقدان الجودة؟**  
ج: نعم. باستخدام خيارات ضغط بدون فقدان (مثل LZW أو CCITT Fax) والحفاظ على بيانات البكسل الأصلية، يمكن أن يكون التحويل بدون فقدان.

**س: هل أحتاج إلى تغيير حجم الصور قبل إضافتها كإطارات؟**  
ج: يجب أن تشترك جميع الإطارات في TIFF في نفس الأبعاد، لذا يلزم تغيير حجم كل JPEG إلى العرض والارتفاع المستهدف.

**س: كم عدد الإطارات التي يمكن أن يحتويها ملف TIFF؟**  
ج: عمليًا غير محدود؛ الحد يتحكم فيه حجم الملف والذاكرة المتاحة.

**س: هل ملف TIFF المُنتج متوافق مع المشاهدين الشائعين؟**  
ج: يستخدم المثال ضغط CCITT Fax Group 3 القياسي، وهو مدعوم على نطاق واسع من قبل معظم مشغلات ومحررات TIFF.

**س: ماذا لو أردت إضافة ضغط مختلف للصور الملونة؟**  
ج: استبدل `TiffCompressions.CcittFax3` بـ `TiffCompressions.Lzw` أو `TiffCompressions.Jpeg` واضبط `BitsPerSample` وفقًا لذلك.

## الخلاصة

غطى هذا الدرس الخطوات الأساسية لـ **convert JPEG to TIFF** وإنشاء صور TIFF متعددة الإطارات باستخدام Aspose.Imaging لـ .NET. من تكوين `TiffOptions` إلى إضافة الإطارات، لديك الآن أساس قوي لتكامل التصوير عالي الجودة في تطبيقاتك.

**الخطوات التالية**  
- تجربة أنواع ضغط أخرى وعمق ألوان مختلف.  
- استكشاف ميزات Aspose.Imaging إضافية مثل معالجة البيانات الوصفية أو تحويل PDF.  
- راجع [الوثائق الرسمية](https://reference.aspose.com/imaging/net/) للحصول على رؤى أعمق.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-02-09  
**تم الاختبار مع:** Aspose.Imaging for .NET (latest stable version)  
**المؤلف:** Aspose