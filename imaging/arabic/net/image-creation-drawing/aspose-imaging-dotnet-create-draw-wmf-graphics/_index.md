---
"date": "2025-06-03"
"description": "تعلّم كيفية إنشاء رسومات Windows Metafile (WMF) ومعالجتها باستخدام Aspose.Imaging لـ .NET. حسّن تطبيقاتك باستخدام الصور والأشكال والنصوص المتجهة."
"title": "إتقان رسومات WMF باستخدام Aspose.Imaging لـ .NET - إنشاء ورسم صور متجهية"
"url": "/ar/net/image-creation-drawing/aspose-imaging-dotnet-create-draw-wmf-graphics/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# إتقان رسومات WMF باستخدام Aspose.Imaging لـ .NET: إنشاء ورسم صور متجهية

## مقدمة
إنشاء رسومات ديناميكية وجذابة بصريًا قد يكون مهمة شاقة، خاصةً عند العمل ضمن قيود تنسيق Windows Metafile (WMF). سواء كنت تُطوّر تطبيقات سطح مكتب أو خدمات ويب تتطلب صورًا متجهة، يُقدّم Aspose.Imaging for .NET حلاً فعّالاً لإنشاء هذه الرسومات ومعالجتها وعرضها بسهولة.

في هذا البرنامج التعليمي، سنستكشف كيفية استخدام Aspose.Imaging لـ .NET لإنشاء وتكوين رسومات WMF. ستتعلم كيفية رسم وتعبئة أشكال متنوعة، ودمج الصور في تصميماتك، وحتى إضافة عناصر نصية باستخدام ميزات المكتبة القوية. بإتقان هذه التقنيات، يمكنك تحسين القدرات المرئية لتطبيقك مع الحفاظ على الأداء العالي وقابلية التوسع.

**ما سوف تتعلمه:**
- كيفية إعداد Aspose.Imaging لـ .NET في مشروعك.
- إنشاء لوحة رسومية WMF مع تكوينات مخصصة.
- رسم وملء الأشكال مثل المضلعات، والقطع الناقصة، والأقواس، ومحاور بيزير.
- دمج الصور في رسومات WMF.
- إضافة عناصر النص مع خيارات التصميم.
- التطبيقات العملية لهذه الميزات في سيناريوهات العالم الحقيقي.

الآن، دعونا نلقي نظرة على المتطلبات الأساسية التي ستحتاجها قبل أن نبدأ.

## المتطلبات الأساسية
قبل البدء في هذا البرنامج التعليمي، تأكد من أن لديك ما يلي:

1. **المكتبات المطلوبة:**
   - Aspose.Imaging لـ .NET
   - مساحة اسم System.Drawing (جزء من إطار عمل .NET)

2. **متطلبات إعداد البيئة:**
   - بيئة تطوير متوافقة مثل Visual Studio.
   - فهم أساسي لبرمجة C# و.NET.

3. **المتطلبات المعرفية:**
   - التعرف على مفاهيم الرسومات المتجهة.
   - المعرفة الأساسية للعمل مع الصور في تطبيقات .NET.

## إعداد Aspose.Imaging لـ .NET
لبدء استخدام Aspose.Imaging، ستحتاج إلى تثبيت المكتبة في مشروعك. إليك كيفية القيام بذلك:

**استخدام .NET CLI:**
```bash
dotnet add package Aspose.Imaging
```

**استخدام وحدة تحكم إدارة الحزم:**
```powershell
Install-Package Aspose.Imaging
```

**استخدام واجهة مستخدم NuGet Package Manager:**
- ابحث عن "Aspose.Imaging" في NuGet Package Manager وقم بتثبيت الإصدار الأحدث.

### الحصول على الترخيص
لاستخدام Aspose.Imaging، يمكنك البدء بفترة تجريبية مجانية أو طلب ترخيص مؤقت. بالنسبة للتطبيقات التجارية، يُنصح بشراء ترخيص كامل للاستفادة من جميع الميزات دون قيود.

1. **نسخة تجريبية مجانية:** يمكنك استكشاف معظم الوظائف عن طريق التسجيل للحصول على حساب مجاني على موقع Aspose.
2. **رخصة مؤقتة:** اطلب ترخيصًا مؤقتًا من خلال لوحة معلومات حساب Aspose الخاص بك لأغراض الاختبار الموسعة.
3. **رخصة الشراء:** للاستخدام المستمر، قم بشراء ترخيص كامل مباشرة من [صفحة شراء Aspose](https://purchase.aspose.com/buy).

### التهيئة والإعداد الأساسي
بمجرد التثبيت، قم بتهيئة المكتبة في مشروعك:

```csharp
using Aspose.Imaging.FileFormats.Wmf;
using Aspose.Imaging.FileFormats.Wmf.Graphics;
using System.Drawing;

// قم بتهيئة مسجل الرسومات WMF بالأبعاد وDPI المطلوبة
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

## دليل التنفيذ
دعونا نقسم التنفيذ إلى الميزات الرئيسية.

### إنشاء وتكوين رسومات WMF
#### ملخص
يتضمن إنشاء لوحة WMF إعداد أبعاد وخصائص، مثل لون الخلفية. يُعد هذا الإعداد أساسيًا لتحديد كيفية عرض رسوماتك.

##### خطوات:
**1. تهيئة WmfRecorderGraphics2D:**

```csharp
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
graphics.BackgroundColor = Color.WhiteSmoke;
```
*توضيح:* يقوم هذا المقطع بتهيئة كائن رسومي WMF بأبعاد 100 × 100 بكسل ويضبط لون الخلفية إلى WhiteSmoke.

### رسم وملء الأشكال
#### ملخص
يُعد رسم الأشكال أمرًا أساسيًا لإنشاء عناصر رسومية في تطبيقاتك. يدعم Aspose.Imaging أنواعًا مختلفة من الأشكال، مثل المضلعات، والقطع الناقص، والأقواس، ومكعبات بيزييه.

##### خطوات:
**1. تعريف القلم والفرشاة:**

```csharp
using Aspose.Imaging.Brushes;
using System.Drawing;

Pen pen = new Pen(Color.Blue);
Brush brush = new SolidBrush(Color.YellowGreen);
```
*توضيح:* أ `Pen` يحدد الكائن لون المخطط التفصيلي، بينما `Brush` تعيين لون التعبئة.

**2. ارسم واملأ المضلع:**

```csharp
graphics.FillPolygon(brush, new[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.DrawPolygon(pen, new[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```
*توضيح:* تستخدم هذه الطرق القلم والفرشاة المحددين لرسم وتعبئة مضلع بنقاط محددة.

**3. إنشاء HatchBrush لـ Ellipse:**

```csharp
brush = new HatchBrush { HatchStyle = HatchStyle.Cross, BackgroundColor = Color.White, ForegroundColor = Color.Silver };
graphics.FillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.DrawEllipse(pen, new Rectangle(25, 2, 20, 20));
```
*توضيح:* أ `HatchBrush` يوفر تعبئة منقوشة للقطع الناقص.

**4. ارسم قوسًا ومكعبًا من بيزير:**

```csharp
pen.DashStyle = DashStyle.Dot;
pen.Color = Color.Black;
graphics.DrawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.DashStyle = DashStyle.Solid;
pen.Color = Color.Red;
graphics.DrawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```
*توضيح:* ضبط `DashStyle` ولون القلم لتخصيص المنحنيات القوسية والمكعبة بيزير.

### رسم الصور
#### ملخص
يؤدي دمج الصور في رسومات WMF إلى تعزيز الجاذبية البصرية وتوفير سياق أو علامة تجارية إضافية.

##### خطوات:
**1. تحميل الصورة:**

```csharp
using Aspose.Imaging;
using System.Drawing;

string dataDir = "YOUR_DOCUMENT_DIRECTORY";
using (Image image = Image.Load(dataDir + "WaterMark.bmp"))
{
    RasterImage rasterImage = image as RasterImage;
    if (rasterImage != null)
    {
        graphics.DrawImage(rasterImage, new Point(50, 50));
    }
}
```
*توضيح:* يقوم هذا الكود بتحميل ملف صورة ورسمه على لوحة WMF.

### رسم الخطوط والأشكال المعقدة
#### ملخص
بالنسبة للتصاميم الأكثر تعقيدًا، فإن رسم الخطوط والأشكال المعقدة مثل الفطائر يمكن أن يضيف عمقًا إلى رسوماتك.

##### خطوات:
**1. ارسم الدائرة والخط المتعدد:**

```csharp
pen.Color = Color.DarkGoldenrod;
Brush brushPie = new SolidBrush(Color.Green);
graphics.FillPie(brushPie, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.DrawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);

Point[] polylinePoints = { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) };
graphics.DrawPolyline(pen, polylinePoints);
```
*توضيح:* تعتمد هذه الطرق على استخدام القلم والفرشاة لإنشاء أقسام دائرية وخطوط متعددة الأشكال.

### نص الرسم
#### ملخص
تعتبر عناصر النص ضرورية لنقل المعلومات أو التعليمات داخل الرسومات.

##### خطوات:
**1. تحديد الخط:**

```csharp
using System.Drawing.Text;

Font font = new Font("Arial", 12, FontStyle.Bold);
graphics.DrawString("Sample Text", font, Brushes.Black, new PointF(10, 10));
```
*توضيح:* استخدم `Font` إنشاء نص نمطي ورسمه على لوحة الرسومات.

## التطبيقات العملية لرسومات WMF
- **التقارير التجارية:** إنشاء تقارير جذابة بصريًا باستخدام المخططات والرسوم البيانية المخصصة.
- **واجهات المستخدم:** تصميم مكونات واجهة المستخدم المعتمدة على المتجهات للتطبيقات.
- **الرسومات المعمارية:** تقديم الخطط والمخططات التفصيلية بتنسيق قابل للتطوير.

## خاتمة
يقدم هذا البرنامج التعليمي دليلاً شاملاً لإنشاء رسومات WMF ومعالجتها باستخدام Aspose.Imaging لـ .NET. باستخدام هذه المهارات، يمكنك تحسين القدرات البصرية لتطبيقك من خلال دمج الصور والأشكال والنصوص المتجهة وغيرها. لمزيد من الاستكشاف، راجع [توثيق Aspose.Imaging](https://docs.aspose.com/imaging/net/).

## توصيات الكلمات الرئيسية
- "رسومات WMF"
- "Aspose.Imaging لـ .NET"
- "صور متجهة"

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}