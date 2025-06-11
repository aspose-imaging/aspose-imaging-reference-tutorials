---
"date": "2025-06-03"
"description": "أتقن تحويل ملفات SVG إلى PDF باستخدام Aspose.Imaging .NET مع الحفاظ على جودة الخط. تعلّم كيفية إعداد المجلدات، وتضمين الخطوط، والمزيد."
"title": "تحويل SVG إلى PDF بكفاءة باستخدام إدارة الخطوط وتقنيات Aspose.Imaging .NET"
"url": "/ar/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# تحويل SVG إلى PDF بكفاءة باستخدام Aspose.Imaging .NET

## مقدمة

يُعد تحويل الرسومات المتجهة إلى صيغ متعددة الاستخدامات مثل PDF أمرًا بالغ الأهمية لمشاركة المستندات وطباعتها في عصرنا الرقمي. قد يكون الحفاظ على سلامة الخط أثناء عملية التحويل أمرًا صعبًا. يوضح هذا البرنامج التعليمي تحويل SVG إلى PDF بسلاسة مع الحفاظ على جودة الخط باستخدام Aspose.Imaging لـ .NET.

**ما سوف تتعلمه:**
- إعداد الدلائل وتصدير ملفات SVG بتنسيق PDF.
- تقنيات تضمين أو تصدير الخطوط داخل ملفات SVG.
- تنفيذ معالج استدعاء مخصص لإدارة خطوط SVG أثناء عملية الحفظ.

بفضل هذه المهارات، يمكنك ضمان ظهور مستنداتك بشكل احترافي ومتناسق على مختلف المنصات. لنبدأ بإعداد بيئتنا!

## المتطلبات الأساسية

قبل الغوص في الكود، تأكد من أن لديك ما يلي:

### المكتبات المطلوبة
- **Aspose.Imaging لـ .NET**:ضروري للتعامل مع تحويلات الصور.
- **مساحة اسم System.IO**:لعمليات الملفات والمجلدات.

### إعداد البيئة
تأكد من استخدام بيئة تطوير متوافقة، مثل Visual Studio أو أي بيئة تطوير متكاملة تدعم مشاريع .NET. الإلمام بأساسيات برمجة C# مفيد.

## إعداد Aspose.Imaging لـ .NET

لاستخدام Aspose.Imaging في مشروعك، اتبع خطوات التثبيت التالية:

**استخدام .NET CLI:**
```bash
dotnet add package Aspose.Imaging
```

**استخدام مدير الحزم:**
```powershell
Install-Package Aspose.Imaging
```

**عبر واجهة مستخدم NuGet Package Manager:**
ابحث عن "Aspose.Imaging" وقم بتثبيت الإصدار الأحدث.

### الحصول على الترخيص
- **نسخة تجريبية مجانية**:ابدأ بإصدار تجريبي مجاني لاختبار الميزات.
- **رخصة مؤقتة**:الحصول على ترخيص مؤقت للتقييم الموسع.
- **شراء**:فكر في الشراء إذا كان Aspose.Imaging يلبي احتياجاتك.

#### التهيئة والإعداد
لاستخدام Aspose.Imaging، أضفه كاعتمادية في مشروعك. إليك الإعداد الأساسي:

```csharp
using Aspose.Imaging;
```

تأكد من `Aspose.Imaging` يتم تضمين مساحة الاسم في أعلى ملفك للوصول إلى فئاته وطرقه.

## دليل التنفيذ

يقوم هذا القسم بتقسيم كل ميزة إلى خطوات قابلة للإدارة.

### إعداد الدليل وتصدير SVG إلى PDF

#### ملخص
قم بتحويل ملف SVG إلى ملف PDF مع التأكد من إعداد مسارات الدليل بشكل صحيح للإخراج.

**الخطوة 1: تأكد من وجود دليل الإخراج**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*توضيح*:يتحقق مقتطف التعليمات البرمجية هذا من وجود دليل الإخراج ويقوم بإنشائه إذا لزم الأمر.

**الخطوة 2: تحميل SVG وتصديره إلى PDF**
```csharp
public void ReadAndExportToPdf(string inputFileName)
{
    string inputFile = Path.Combine(SourceFolder, inputFileName);
    string outFile = Path.Combine(OutFolder, inputFileName + ".pdf");
    
    using (Image image = Image.Load(inputFile))
    {
        image.Save(outFile,
            new PdfOptions { VectorRasterizationOptions = new SvgRasterizationOptions { PageSize = image.Size } });
    }
}
```
*توضيح*: ال `PdfOptions` السماح بتكوين تحويل محتوى SVG إلى صور نقطية، مع التأكد من أن حجم الصفحة يتطابق مع أبعاد الصورة الأصلية.

### حفظ SVG باستخدام خيارات تضمين الخط

#### ملخص
احفظ ملف SVG أثناء التحكم في إعدادات تضمين الخط للحفاظ على دقة الخط.

**الخطوة 1: تحديد أدلة الإخراج والخطوط**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*توضيح*:تأكد من إعداد الدلائل قبل حفظ الملفات.

**الخطوة 2: حفظ SVG باستخدام خيارات الخط المخصصة**
```csharp
public void Save(bool useEmbedded, string fileName, int expectedCountFonts)
{
    string fontStoreType = useEmbedded ? "Embedded" : "Stream";
    string inputFile = Path.Combine(SourceFolder, fileName);
    string outFileName = $"{Path.GetFileNameWithoutExtension(fileName)}_{fontStoreType}.svg";
    string outputFile = Path.Combine(OutFolder, outFileName);

    using (Image image = Image.Load(inputFile))
    {
        EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions
        {
            BackgroundColor = Color.White,
            PageWidth = image.Width,
            PageHeight = image.Height
        };

        string testingFileName = Path.GetFileNameWithoutExtension(inputFile);
        string fontFolder = Path.Combine(FontFolder, testingFileName);

        image.Save(outputFile,
            new SvgOptions
            {
                VectorRasterizationOptions = emfRasterizationOptions,
                Callback = new SvgCallbackFontTest(useEmbedded, fontFolder)
                {
                    Link = FontFolderName + "/" + testingFileName
                }
            });
    }

    if (!useEmbedded)
    {
        string[] files = Directory.GetFiles(fontFolder);
        if (files.Length != expectedCountFonts)
        {
            throw new Exception($"Expected count font files = {expectedCountFonts}, Current count font files = {files.Length}");
        }
    }
}
```
*توضيح*:تتيح لك هذه الطريقة تحديد ما إذا كان يجب تضمين الخطوط أو بثها، مما يؤثر على كيفية تخزينها والوصول إليها.

### معالج استدعاء خط SVG المخصص

#### ملخص
تنفيذ معالج مخصص لإدارة موارد الخط أثناء حفظ SVG.

**الخطوة 1: تنفيذ فئة SvgCallbackFontTest**
```csharp
public class SvgCallbackFontTest : SvgResourceKeeperCallback
{
    private readonly string outFolder;
    private readonly bool useEmbeddedFont;
    private int fontCounter = 0;

    public string Link { get; set; }

    public SvgCallbackFontTest(bool useEmbeddedFont, string outFolder)
    {
        this.useEmbeddedFont = useEmbeddedFont;
        this.outFolder = outFolder;
        
        if (Directory.Exists(outFolder))
        {
            Directory.Delete(this.outFolder, true);
        }
    }

    public override void OnFontResourceReady(FontStoringArgs args)
    {
        if (this.useEmbeddedFont)
        {
            args.FontStoreType = FontStoreType.Embedded;
        }
        else
        {
            args.FontStoreType = FontStoreType.Stream;
            string fontFolder = this.outFolder;

            if (!Directory.Exists(fontFolder))
            {
                Directory.CreateDirectory(fontFolder);
            }

            string fName = args.SourceFontFileName;
            if (!File.Exists(fName))
            {
                fName = $"font_{this.fontCounter++}.ttf";
            }

            string fileName = Path.Combine(fontFolder, Path.GetFileName(fName));
            
            args.DestFontStream = new FileStream(fileName, FileMode.OpenOrCreate);
            args.DisposeStream = true;
            args.FontFileUri = $".{this.Link}/{Path.GetFileName(fName)}";
        }
    }
}
```
*توضيح*تتولى هذه الفئة إدارة موارد الخطوط بتحديد ما إذا كان سيتم تضمينها مباشرةً أو تخزينها بشكل منفصل. وتضمن هذه الفئة الإشارة إلى الخطوط وحفظها بشكل صحيح أثناء عملية تصدير SVG.

## التطبيقات العملية

1. **إنشاء التقارير تلقائيًا**:استخدم Aspose.Imaging لتحويل مسودات التصميم إلى ملفات PDF لضمان توزيعها بشكل متسق.
2. **النشر الرقمي**:تأكد من تقديم خط عالي الجودة عند تحويل المقالات ذات الرسومات المضمنة من SVG إلى PDF.
3. **مشاركة المستندات عبر الأنظمة الأساسية**:الحفاظ على سلامة المستندات المشتركة بين أنظمة التشغيل المختلفة.

## اعتبارات الأداء

### نصائح لتحسين الأداء
- استخدم ممارسات فعالة للتعامل مع الملفات، مثل التخلص من الملفات فورًا بعد الاستخدام.
- قم بتقليل استخدام الذاكرة عن طريق مسح الكائنات والدلائل غير المستخدمة بمجرد اكتمال المعالجة.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}