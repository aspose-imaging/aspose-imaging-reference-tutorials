---
"date": "2025-06-03"
"description": "เรียนรู้การแปลงไฟล์ SVG เป็น PDF ด้วย Aspose.Imaging .NET โดยยังคงรักษาคุณภาพของฟอนต์เอาไว้ เรียนรู้การตั้งค่าไดเร็กทอรี การฝังฟอนต์ และอื่นๆ อีกมากมาย"
"title": "การแปลง SVG เป็น PDF อย่างมีประสิทธิภาพโดยใช้การจัดการและเทคนิคฟอนต์ Aspose.Imaging .NET"
"url": "/th/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# การแปลง SVG เป็น PDF อย่างมีประสิทธิภาพโดยใช้ Aspose.Imaging .NET

## การแนะนำ

การแปลงกราฟิกเวกเตอร์เป็นรูปแบบต่างๆ เช่น PDF ถือเป็นสิ่งสำคัญสำหรับการแชร์เอกสารและการพิมพ์ในยุคดิจิทัลปัจจุบัน การรักษาความสมบูรณ์ของฟอนต์ระหว่างการแปลงอาจเป็นเรื่องท้าทาย บทช่วยสอนนี้จะสาธิตการแปลง SVG เป็น PDF ได้อย่างราบรื่นพร้อมรักษาคุณภาพฟอนต์โดยใช้ Aspose.Imaging สำหรับ .NET

**สิ่งที่คุณจะได้เรียนรู้:**
- การตั้งค่าไดเร็กทอรีและการส่งออกไฟล์ SVG เป็น PDF
- เทคนิคการฝังหรือส่งออกแบบอักษรภายในไฟล์ SVG
- การใช้งานตัวจัดการการโทรกลับแบบกำหนดเองสำหรับการจัดการแบบอักษร SVG ในระหว่างกระบวนการบันทึก

ด้วยทักษะเหล่านี้ คุณสามารถมั่นใจได้ว่าเอกสารของคุณจะดูเป็นมืออาชีพและสอดคล้องกันบนแพลตฟอร์มต่างๆ เริ่มต้นด้วยการตั้งค่าสภาพแวดล้อมของเรา!

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเจาะลึกโค้ด ให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

### ห้องสมุดที่จำเป็น
- **Aspose.Imaging สำหรับ .NET**: จำเป็นสำหรับการจัดการการแปลงรูปภาพ
- **เนมสเปซ System.IO**: สำหรับการดำเนินการกับไฟล์และไดเร็กทอรี

### การตั้งค่าสภาพแวดล้อม
ตรวจสอบว่าคุณมีสภาพแวดล้อมการพัฒนาที่เข้ากันได้ เช่น Visual Studio หรือ IDE ใดๆ ที่รองรับโปรเจ็กต์ .NET ความคุ้นเคยกับการเขียนโปรแกรม C# ขั้นพื้นฐานจะเป็นประโยชน์

## การตั้งค่า Aspose.Imaging สำหรับ .NET

หากต้องการใช้ Aspose.Imaging ในโครงการของคุณ ให้ปฏิบัติตามขั้นตอนการติดตั้งต่อไปนี้:

**การใช้ .NET CLI:**
```bash
dotnet add package Aspose.Imaging
```

**การใช้ตัวจัดการแพ็คเกจ:**
```powershell
Install-Package Aspose.Imaging
```

**ผ่านทาง UI ของตัวจัดการแพ็กเกจ NuGet:**
ค้นหา "Aspose.Imaging" และติดตั้งเวอร์ชันล่าสุด

### การขอใบอนุญาต
- **ทดลองใช้งานฟรี**:เริ่มต้นด้วยการทดลองใช้ฟรีเพื่อทดสอบคุณสมบัติต่างๆ
- **ใบอนุญาตชั่วคราว**: การขอใบอนุญาตชั่วคราวเพื่อการประเมินผลขยายเวลา
- **ซื้อ**:โปรดพิจารณาซื้อ หาก Aspose.Imaging ตรงตามความต้องการของคุณ

#### การเริ่มต้นและการตั้งค่า
หากต้องการใช้ Aspose.Imaging ให้เพิ่มเป็นส่วนที่ต้องพึ่งพาในโปรเจ็กต์ของคุณ นี่คือการตั้งค่าพื้นฐาน:

```csharp
using Aspose.Imaging;
```

ให้แน่ใจว่า `Aspose.Imaging` เนมสเปซจะรวมอยู่ที่ด้านบนของไฟล์ของคุณเพื่อเข้าถึงคลาสและวิธีการของมัน

## คู่มือการใช้งาน

ในส่วนนี้จะแบ่งคุณลักษณะแต่ละอย่างออกเป็นขั้นตอนที่สามารถจัดการได้

### การตั้งค่าไดเรกทอรีและการส่งออก SVG ไปยัง PDF

#### ภาพรวม
แปลงไฟล์ SVG เป็น PDF โดยให้แน่ใจว่าเส้นทางไดเร็กทอรีได้รับการตั้งค่าอย่างถูกต้องสำหรับเอาต์พุต

**ขั้นตอนที่ 1: ตรวจสอบว่ามีไดเรกทอรีเอาต์พุตอยู่**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*คำอธิบาย*:ตัวอย่างโค้ดนี้จะตรวจสอบว่าไดเร็กทอรีเอาต์พุตมีอยู่หรือไม่ และสร้างขึ้นหากจำเป็น

**ขั้นตอนที่ 2: โหลด SVG และส่งออกเป็น PDF**
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
*คำอธิบาย*: เดอะ `PdfOptions` อนุญาตให้กำหนดค่าการแรสเตอร์เนื้อหา SVG เพื่อให้แน่ใจว่าขนาดหน้าตรงกับขนาดของภาพต้นฉบับ

### การบันทึก SVG พร้อมตัวเลือกการฝังแบบอักษร

#### ภาพรวม
บันทึกไฟล์ SVG ขณะควบคุมการตั้งค่าการฝังฟอนต์เพื่อรักษาความถูกต้องของฟอนต์

**ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอาต์พุตและแบบอักษร**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*คำอธิบาย*: ตรวจสอบให้แน่ใจว่าตั้งค่าไดเร็กทอรีเรียบร้อยแล้วก่อนบันทึกไฟล์

**ขั้นตอนที่ 2: บันทึก SVG ด้วยตัวเลือกแบบอักษรที่กำหนดเอง**
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
*คำอธิบาย*:วิธีการนี้ช่วยให้คุณระบุได้ว่าจะต้องฝังหรือสตรีมแบบอักษร ซึ่งจะส่งผลกระทบต่อวิธีการจัดเก็บและการเข้าถึงแบบอักษร

### ตัวจัดการการเรียกกลับแบบอักษร SVG ที่กำหนดเอง

#### ภาพรวม
ใช้ตัวจัดการแบบกำหนดเองเพื่อจัดการทรัพยากรแบบอักษรในระหว่างการบันทึก SVG

**ขั้นตอนที่ 1: นำคลาส SvgCallbackFontTest มาใช้**
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
*คำอธิบาย*:คลาสนี้จัดการทรัพยากรแบบอักษรโดยตัดสินใจว่าจะฝังโดยตรงหรือจัดเก็บแยกต่างหาก คลาสนี้ช่วยให้แน่ใจว่าแบบอักษรได้รับการอ้างอิงและบันทึกอย่างถูกต้องในระหว่างกระบวนการส่งออก SVG

## การประยุกต์ใช้งานจริง

1. **การสร้างรายงานอัตโนมัติ**:ใช้ Aspose.Imaging เพื่อแปลงแบบร่างการออกแบบเป็น PDF เพื่อการกระจายที่สม่ำเสมอ
2. **การจัดพิมพ์ดิจิตอล**:รับรองการแสดงผลแบบอักษรคุณภาพสูงเมื่อแปลงบทความที่มีกราฟิกฝังจาก SVG เป็น PDF
3. **การแชร์เอกสารข้ามแพลตฟอร์ม**:รักษาความสมบูรณ์ของภาพของเอกสารที่แบ่งปันระหว่างระบบปฏิบัติการที่แตกต่างกัน

## การพิจารณาประสิทธิภาพ

### เคล็ดลับการเพิ่มประสิทธิภาพการทำงาน
- ใช้แนวทางการจัดการไฟล์ที่มีประสิทธิภาพ เช่น กำจัดไฟล์ทันทีหลังใช้งาน
- ลดการใช้หน่วยความจำให้เหลือน้อยที่สุดโดยการล้างวัตถุและไดเร็กทอรีที่ไม่ได้ใช้เมื่อการประมวลผลเสร็จสิ้น

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}