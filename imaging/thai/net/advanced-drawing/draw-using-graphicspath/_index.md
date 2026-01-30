---
date: 2026-01-30
description: เรียนรู้วิธีวาดข้อความบนภาพ, วาดรูปทรงบนภาพและเติมรูปทรงด้วยลวดลายโดยใช้
  Aspose.Imaging สำหรับ .NET.
linktitle: Draw Using GraphicsPath – draw text on image, shapes and patterns
second_title: Aspose.Imaging .NET Image Processing API
title: วิธีวาดข้อความบนภาพด้วย Aspose.Imaging สำหรับ .NET
url: /th/net/advanced-drawing/draw-using-graphicspath/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# วิธีวาดข้อความบนภาพด้วย Aspose.Imaging สำหรับ .NET

ในบทแนะนำนี้เราจะสาธิต **วิธีวาดข้อความบนภาพ** พร้อมกับแสดงวิธีวาดรูปบนภาพและเติมรูปด้วยลวดลายโดยใช้ไลบรารี Aspose.Imaging ที่ทรงพลัง ไม่ว่าคุณจะกำลังสร้างเครื่องมือรายงาน, ตัวสร้างแบดจ์แบบกำหนดเอง, หรือเพียงต้องการใส่คำอธิบายลงบนรูปภาพโดยอัตโนมัติ ขั้นตอนต่อไปนี้จะให้พื้นฐานที่มั่นคงแก่คุณ

## คำตอบด่วน
- **ฉันสามารถวาดอะไรได้บ้าง?** ข้อความ, รูปร่างพื้นฐาน (วงรี, สี่เหลี่ยม) และการเติมลวดลาย  
- **คลาสหลักคืออะไร? `Graphics`  
- **ต้องมีลิขสิทธิ์หรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีลิขสิทธิ์สำหรับการใช้งานจริง  
- **รองรับฟอร์แมตใดบ้าง?** BMP, PNG, JPEG, TIFF และอื่น ๆ อีกมากมายผ่าน Aspose.Imaging  
- **ข้อกำหนดเบื้องต้น?** Visual Studio, .NET 6+ (หรือ .NET Framework 4.6+), และ Aspose.Imaging for .NET  

## การวาดข้อความบนภาพด้วย Aspose.Imaging คืออะไร?
Aspose.Imaging ให้ API ระดับสูงที่ซ่อนการเรียก GDI+ ระดับล่างไว้โดยใช้วัตถุ `Graphics` ร่วมกับ `GraphicsPath` คุณสามารถสร้างการวาดแบบเวกเตอร์—ข้อความ, รูปร่าง, และการเติมลวดลาย—และเรนเดอร์ลงบนบิตแมพหรือรูปแบบภาพที่รองรับใด ๆ

## ทำไมต้องวาดรูปบนภาพและเติมรูปด้วยลวดลาย?
- **เน้นภาพให้เด่น:** ไฮไลท์พื้นที่ด้วยลวดลาย hatch ที่กำหนดเอง  
- **การสร้างแบรนด์:** เพิ่มโลโก้หรือวอเตอร์มาร์คที่ผสานข้อความและกราฟิกเข้าด้วยกัน  
- **กราฟิกแบบไดนามิก:** สร้างแผนภูมิ, แบดจ์, หรือใบรับรองแบบอัตโนมัติโดยไม่ต้องใช้เครื่องมือออกแบบภายนอก  

## ข้อกำหนดเบื้องต้น

1. **Visual Studio** – รุ่นใดก็ได้ที่ใหม่ (Community, Professional หรือ Enterprise)  
2. **Aspose.Imaging for .NET** – ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ: [Download Aspose.Imaging for .NET](https://releases.aspose.com/imaging/net/)  
3. **ความรู้พื้นฐาน C#** – ควรคุ้นเคยกับคลาส, เนมสเปซ, และคำสั่ง `using`  

## นำเข้า Namespaces

เปิดโปรเจกต์ของคุณและตรวจสอบให้แน่ใจว่าได้อ้างอิงเนมสเปซ Aspose.Imaging แล้ว:

```csharp
using Aspose.Imaging;
```

## ขั้นตอนที่ 1: ตั้งค่าสภาพแวดล้อม

แรกเริ่มเราจะสร้างแคนวาสเปล่าว่างที่จะเป็นที่วางการวาดของเรา

```csharp
public static void Run()
{
    Console.WriteLine("Running example DrawingUsingGraphicsPath");
    string dataDir = "Your Document Directory";

    // Create an instance of BmpOptions and set its various properties
    BmpOptions ImageOptions = new BmpOptions();
    ImageOptions.BitsPerPixel = 24;

    // Create an instance of FileCreateSource and assign it to Source property
    ImageOptions.Source = new FileCreateSource(dataDir + "sample_1.bmp", false);

    // Create an instance of Image and initialize an instance of Graphics
    using (Image image = Image.Create(ImageOptions, 500, 500))
    {
        Graphics graphics = new Graphics(image);
        graphics.Clear(Color.White);
```

ที่นี่เราตั้งค่า BMP ขนาด 500 × 500 พิกตอนที่ 2: สร้าง GraphicsPath, เพิ่มรูปและข้อความ

ต่อไปเราจะสร้าง `GraphicsPath` ที่บรรจุทั้งรูป **และข้อความที่ต้องการวาดบนภาพ**

```csharp
        GraphicsPath graphicspath = new GraphicsPath();
        Figure figure = new Figure();

        figure.AddShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
        figure.AddShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
        figure.AddShape(new TextShape("Aspose.Imaging", new RectangleF(170, 225, 170, 100), new Font("Arial", 20), StringFormat.GenericTypographic));

        graphicspath.AddFigures(new[] { figure });
```

- **EllipseShape** และ **RectangleShape** ช่วยให้เราสามารถ **วาดรูปบนภาพ** ได้  
- **TextShape** คือที่ที่เราจะ **วาดข้อความบนภาพ** – สตริง “Aspose.Imaging” จะถูกเรนเดอร์ภายในสี่เหลี่ยมที่กำหนด  

## ขั้นตอนที่ 3: วาด Path และเติมด้วยลวดลาย Hatch

เมื่อ Path พร้อมแล้ว เราจะร่างเส้นขอบด้วยปากกาและเติมภายในด้วยแปรง Hatch – แสดง **การเติมรูปด้วยลวดลาย**

```csharp
        graphics.DrawPath(new Pen(Color.Blue), graphicspath);

        // Create an instance of HatchBrush and set its properties
        HatchBrush hatchbrush = new HatchBrush();
        hatchbrush.BackgroundColor = Color.Brown;
        hatchbrush.ForegroundColor = Color.Blue;
        hatchbrush.HatchStyle = HatchStyle.Vertical;

        graphics.FillPath(hatchbrush, graphicspath);

        image.Save();
        Console.WriteLine("Processing completed successfully.");
    }
    Console.WriteLine("Finished example DrawingUsingGraphicsPath");
}
```

`HatchBrush` จะทาลวดลายเส้นแนวตั้งสีฟ้าบนพื้นหลังสีน้ำตาล ทำให้รูปดูมีลักษณะเฉพาะ

## กรณีการใช้งานทั่วไป

| สถานการณ์ | วิธีที่โค้ดช่วย |
|----------|----------------|
| **การสร้างแบดจ์** | ผสานโลโก้บริษัท (วงรี), กรอบ (สี่เหลี่ยม) และชื่อพนักงาน (ข้อความ) ในภาพเดียว |
| **แผนภูมิไดนามิก** | วาดรูปตามข้อมูลและใส่คำอธิบายค่าด้วย `TextShape` |
| **วอเตอร์มาร์ค** | เรนเดอร์ข้อความกึ่งโปร่งใสบนรูปภาพที่มีอยู่และเติมพื้นหลังด้วยลวดลายเพื่อแบรนด์แบบละเอียด |

## การแก้ไขปัญหาและเคล็ดลับ

- **เส้นทางไฟล์** – ตรวจสอบให้ `dataDir` ชี้ไปยังโฟลเดอร์ที่สามารถเขียนได้; มิฉะนั้น `FileCreateSource` จะโยนข้อยกเว้น  
- **ความคอนทราสต์ของสี** – เมื่อใช้การเติมลวดลาย, เลือกสีพื้นหน้า/พื้นหลังที่ให้ความคอนทราสต์เพียงพอสำหรับการอ่าน  
- **ประสิทธิภาพ** – สำหรับภาพขนาดใหญ่, พิจารณาใช้ `RasterImage` แทน `BmpOptions` เพื่อลดการใช้หน่วยความจำ  

## คำถามที่พบบ่อย

**ถาม: Aspose.Imaging for .NET รองรับ .NET framework ล่าสุดหรือไม่?**  
ตอบ: รองรับ, ไลบรารีจะอัปเดตอย่างสม่ำเสมอเพื่อสนับสนุน .NET 6, .NET 7 และเวอร์ชัน .NET Framework ล่าสุด

**ถาม: ฉันสามารถแปลงภาพที่วาดเป็นฟอร์แมตอื่นได้หรือไม่ (เช่น PNG หรือ JPEG)?**  
ตอบ: แน่นอน หลังจากบันทึก BMP คุณสามารถโหลดด้วย `Image.Load` แล้วเรียก `Save` พร้อมนามสกุลไฟล์ที่ต้องการ

**ถาม: จะหาเอกสารรายละเอียดเพิ่มเติมได้จากที่ไหน?**  
ตอบ: เยี่ยมชมเอกสารอย่างเป็นทางการที่ [Aspose.Imaging documentation](https://reference.aspose.com/imaging/net/)

**ถาม: มีเวอร์ชันทดลองฟรีหรือไม่?**  
ตอบ: มี, คุณสามารถดาวน์โหลดเวอร์ชันทดลองได้จาก [here](https://releases.aspose.com/)

**ถาม: จะซื้อไลเซนส์สำหรับการใช้งานผลิตภัณฑ์ได้อย่างไร?**  
ตอบ: สามารถซื้อไลเซนส์ได้โดยตรงจากร้าน Aspose: [this link](https://purchase.aspose.com/buy)

## สรุป

คุณได้เรียนรู้วิธี **วาดข้อความบนภาพ**, **วาดรูปบนภาพ**, และ **เติมรูปด้วยลวดลาย** ด้วย API `GraphicsPath` ของ Aspose.Imaging ด้วยบล็อกพื้นฐานเหล่านี้ คุณสามารถสร้างกราฟิกเชิงโปรแกรมที่หลากหลายสำหรับรายงาน, แดชบอร์ด, หรือผลลัพธ์ภาพใด ๆ ในแอปพลิเคชัน .NET ของคุณ

หากคุณเจอปัญหาใดหรืออยากแบ่งปันผลงานของคุณ, เชิญเข้าร่วมชุมชนที่ [Aspose.Imaging Forum](https://forum.aspose.com/)  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2026-01-30  
**ทดสอบด้วย:** Aspose.Imaging 24.12 for .NET  
**ผู้เขียน:** Aspose