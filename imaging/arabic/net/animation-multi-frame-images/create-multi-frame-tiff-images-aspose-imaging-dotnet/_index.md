---
"date": "2025-06-02"
"description": "تعلّم كيفية إنشاء صور TIFF متعددة الإطارات باستخدام Aspose.Imaging في .NET. أتقن إعداد بيئتك، وتكوين خيارات Tiff، وتغيير حجم ملفات JPEG، وإضافة الإطارات."
"title": "كيفية إنشاء صور TIFF متعددة الإطارات باستخدام Aspose.Imaging لـ .NET"
"url": "/ar/net/animation-multi-frame-images/create-multi-frame-tiff-images-aspose-imaging-dotnet/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# كيفية إنشاء صور TIFF متعددة الإطارات باستخدام Aspose.Imaging لـ .NET

## مقدمة

هل تتطلع إلى إتقان فن إنشاء صور TIFF متعددة الإطارات باستخدام Aspose.Imaging لـ .NET؟ سيرشدك هذا البرنامج التعليمي الشامل خلال إعداد بيئتك، وتكوين خيارات Tiff، وتغيير حجم ملفات JPEG، وإضافة إطارات إلى صورة TIFF - كل ذلك بسهولة. سواء كنت تدير أرشيفات مستندات أو تدمج صورًا عالية الجودة في تطبيقات برمجية، فهذا الدليل مصمم خصيصًا لتحسين سير عملك.

**ما سوف تتعلمه:**
- كيفية إعداد Aspose.Imaging لـ .NET
- تكوين TiffOptions للصور بالأبيض والأسود باستخدام ضغط CCITT Fax Group 3
- تحميل ملفات JPEG وتغيير حجمها من دليل
- إضافة إطارات إلى صورة TIFF
- حفظ صور TIFF متعددة الإطارات

دعونا نتعمق في المتطلبات الأساسية للبدء.

## المتطلبات الأساسية

قبل البدء في إنشاء صور TIFF باستخدام Aspose.Imaging، تأكد من توفر ما يلي:

### المكتبات والتبعيات المطلوبة
- **Aspose.Imaging لـ .NET**:قم بتثبيت هذه المكتبة باستخدام NuGet أو مدير الحزم المفضل لديك.
  
### متطلبات إعداد البيئة
- بيئة تطوير تدعم C# و.NET Core/5+
  
### متطلبات المعرفة
- فهم أساسي لمفاهيم برمجة C#
- المعرفة بكيفية التعامل مع ملفات الصور في .NET

## إعداد Aspose.Imaging لـ .NET

للبدء، عليك تثبيت Aspose.Imaging. إليك الطريقة:

**.NET CLI**
```shell
dotnet add package Aspose.Imaging
```

**مدير الحزم**
```powershell
Install-Package Aspose.Imaging
```

**واجهة مستخدم مدير الحزم NuGet**
ابحث عن "Aspose.Imaging" وقم بتثبيت الإصدار الأحدث.

### خطوات الحصول على الترخيص
- **نسخة تجريبية مجانية**:يمكنك الوصول إلى إصدار محدود الوظائف لاختبار الميزات.
- **رخصة مؤقتة**احصل على هذا لفترة تجريبية مطولة دون قيود على التقييم. تفضل بزيارة [رخصة مؤقتة](https://purchase.aspose.com/temporary-license/).
- **شراء**:للحصول على الوصول الكامل، فكر في شراء ترخيص من [شراء Aspose.Imaging](https://purchase.aspose.com/buy).

### التهيئة والإعداد الأساسي

```csharp
// قم بتهيئة المكتبة باستخدام الترخيص الخاص بك
Aspose.Imaging.License license = new Aspose.Imaging.License();
license.SetLicense("Path to your license file");
```

## دليل التنفيذ

دعونا نقسم التنفيذ إلى أقسام قابلة للإدارة.

### إنشاء وتكوين TiffOptions لصورة TIFF

#### ملخص
إنشاء `TiffOptions` يسمح لك الكائن بتحديد إعدادات مثل الضغط والتفسير الضوئي، وهي ضرورية لتخصيص ملفات TIFF الخاصة بك.

#### التنفيذ خطوة بخطوة

**1. استيراد مساحات الأسماء الضرورية**
تأكد من تضمين هذه المساحات الأسماء في ملفك:

```csharp
using Aspose.Imaging.FileFormats.Tiff;
using Aspose.Imaging.FileFormats.Tiff.Enums;
using Aspose.Imaging.ImageOptions;
```

**2. تكوين خيارات Tiff**
إعداد `TiffOptions` كائن ذو تكوينات محددة لصورة بالأبيض والأسود باستخدام ضغط CCITT Fax Group 3.

```csharp
// إنشاء TiffOptions بالإعدادات الافتراضية
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);

// تعيين البتات لكل عينة إلى 1 (أبيض وأسود)
outputSettings.BitsPerSample = new ushort[] { 1 };

// استخدم ضغط CCITT Fax Group 3
outputSettings.Compression = TiffCompressions.CcittFax3;

// تعريف التفسير الضوئي على أنه MinIsWhite
outputSettings.Photometric = TiffPhotometrics.MinIsWhite;

// تعيين المصدر إلى مجرى فارغ لإنشاء ملف TIFF جديد من البداية
outputSettings.Source = new Aspose.Imaging.Sources.StreamSource(new System.IO.MemoryStream());
```

### إنشاء وتكوين TiffImage بأبعاد محددة

#### ملخص
إنشاء `TiffImage` يتضمن تعيين أبعاد مخصصة، وهو أمر بالغ الأهمية عند تحديد حجم كل إطار TIFF.

**1. تحديد أبعاد الصورة**

```csharp
int newWidth = 500; // العرض لكل إطار TIFF
int newHeight = 500; // الارتفاع لكل إطار TIFF
string path = "@YOUR_OUTPUT_DIRECTORY\\AddFramesToTIFFImage_out.tif";
```

**2. إنشاء مثيل TiffImage**
تهيئة `TiffImage` مع أبعاد محددة وإعدادات الإخراج.

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    // سيتم هنا إضافة المنطق لإضافة الإطارات.
}
```

### تحميل ملفات JPEG من الدليل وتغيير حجمها

#### ملخص
يتم تبسيط عملية تحميل صور JPEG وتغيير حجمها والاستعداد للتضمين في ملف TIFF باستخدام Aspose.Imaging.

**1. تحميل صور JPEG**

```csharp
string dataDir = "@YOUR_DOCUMENT_DIRECTORY"; // الدليل الذي يحتوي على صور الإدخال

foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
{
    using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
    {
        // تغيير حجم الصورة لتتناسب مع أبعاد إطار TIFF
        ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
        
        // سيتم هنا إضافة منطق إضافي للتعامل مع الإطارات المتعددة.
    }
}
```

### إضافة إطار إلى TiffImage وحفظه

#### ملخص
تتضمن إضافة إطارات إلى صورة TIFF نسخ وحدات بكسل JPEG التي تم تغيير حجمها إلى كل إطار وحفظ صورة TIFF متعددة الإطارات بالكامل.

**1. تهيئة مثيل TiffImage**

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    int index = 0; // متتبع مؤشر الإطار
    
    foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
    {
        using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
        {
            ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
            
            TiffFrame frame = tiffImage.ActiveFrame;
            if (index > 0)
            {
                // إنشاء إطار جديد لكل صورة لاحقة
                frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            }
            
            // نسخ وحدات البكسل من ملف JPEG الذي تم تغيير حجمه إلى إطار TIFF
            frame.SavePixels(frame.Bounds, ri.LoadPixels(ri.Bounds));
            if (index > 0)
            {
                tiffImage.AddFrame(frame); // أضف إلى صورة TIFF فقط بعد الإطار الأول
            }
            index++;
        }
    }
    
    tiffImage.Save(path); // احفظ ملف TIFF النهائي مع جميع الإطارات
}
```

## التطبيقات العملية

فيما يلي بعض حالات الاستخدام الواقعية لإنشاء صور TIFF متعددة الإطارات:

1. **أرشفة المستندات**:قم بتخزين المستندات الممسوحة ضوئيًا كملفات TIFF واحدة لضمان سلامة البيانات وسهولة الوصول إليها.
2. **التصوير الطبي**:استخدم تنسيقات TIFF المضغوطة عالية الجودة لتخزين المسوحات الطبية مثل التصوير بالرنين المغناطيسي والتصوير المقطعي المحوسب.
3. **التصميم الجرافيكي**:دمج طبقات التصميم المتعددة في ملف واحد للتعامل معها بكفاءة في برامج الرسومات.
4. **التصوير الفوتوغرافي**:أرشفة ألبومات الصور متعددة الصفحات كملفات فردية لسهولة مشاركتها وتخزينها.
5. **مراقبة الجودة الصناعية**:استخدم صور TIFF لتسجيل بيانات التفتيش التفصيلية عبر إطارات متعددة.

## اعتبارات الأداء

### نصائح لتحسين الأداء
- **إدارة الذاكرة**:تخلص من كائنات الصورة بشكل صحيح بعد الاستخدام لتحرير الموارد.
- **معالجة الدفعات**:قم بمعالجة الصور على دفعات إذا كنت تتعامل مع مجموعات بيانات كبيرة لإدارة استخدام الذاكرة بشكل فعال.
- **ضغط فعال**:اختر إعدادات الضغط المناسبة استنادًا إلى متطلبات الجودة والأداء لديك.

## خاتمة

غطّى هذا البرنامج التعليمي الخطوات الأساسية لإنشاء صور TIFF متعددة الإطارات باستخدام Aspose.Imaging لـ .NET. بدءًا من التهيئة `TiffOptions` من خلال إضافة الإطارات، أصبح لديك الآن أساس متين لدمج التصوير عالي الجودة في تطبيقاتك.

**الخطوات التالية:**
- جرّب إعدادات الضغط وتنسيقات الصور المختلفة.
- استكشف الميزات الإضافية لـ Aspose.Imaging من خلال استشارة [الوثائق الرسمية](https://reference.aspose.com/imaging/net/).

حاول تنفيذ هذه الخطوات في مشاريعك، واستكشف كيف يمكن لصور TIFF متعددة الإطارات أن تعزز سير عملك.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}