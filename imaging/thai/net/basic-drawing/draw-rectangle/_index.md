---
date: 2026-02-12
description: เรียนรู้วิธีสร้างภาพเปล่าโดยใช้ Aspose และวิธีวาดสี่เหลี่ยมใน .NET ด้วย
  Aspose.Imaging – คู่มือสั้นสำหรับการจัดการภาพในแอปพลิเคชัน .NET ของคุณ
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: สร้างภาพเปล่า Aspose – วาดสี่เหลี่ยมใน .NET
url: /th/net/basic-drawing/draw-rectangle/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# สร้างภาพเปล่า Aspose – วาดสี่เหลี่ยมใน .NET

การสร้างและจัดการภาพในแอปพลิเคชัน .NET อาจดูยาก, แต่ด้วย Aspose.Imaging คุณสามารถ **create blank image Aspose** ได้ในไม่กี่บรรทัดของโค้ดและจากนั้นวาดรูปทรงบนมัน ในบทแนะนำนี้เราจะเดินผ่านกระบวนการทั้งหมด — ตั้งแต่การตั้งค่าแคนวาสเปล่าไปจนถึงการวาดสี่เหลี่ยม — เพื่อให้คุณเริ่มเพิ่มกราฟิกในโครงการ .NET ของคุณได้ทันที.

## คำตอบเร็ว
- **“create blank image Aspose” หมายถึงอะไร?** It means generating an empty bitmap using the Aspose.Imaging API.  
- **วิธีวาดสี่เหลี่ยม .net ด้วย Aspose?** ใช้เมธอด `Graphics.DrawRectangle` หลังจากสร้างอ็อบเจ็กต์ `Graphics`.  
- **ต้องการแพคเกจ NuGet ใด?** `Aspose.Imaging` (รุ่นล่าสุด).  
- **ฉันสามารถบันทึกภาพเป็น PNG, JPEG หรือ BMP ได้หรือไม่?** ได้ – เพียงเปลี่ยนตัวเลือกการบันทึกภาพ (เช่น `BmpOptions`, `JpegOptions`).  
- **ต้องการไลเซนส์สำหรับการพัฒนาหรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการประเมิน; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.

## “create blank image Aspose” คืออะไร?
การสร้างภาพเปล่าหมายถึงการจัดสรรบัฟเฟอร์พิกเซลที่มีความกว้าง, ความสูง, และรูปแบบพิกเซลที่กำหนดไว้ Aspose.Imaging จัดการรายละเอียดระดับต่ำให้คุณ, ทำให้ได้แคนวาสพร้อมวาดโดยไม่ต้องจัดการกับ GDI+ หรือ System.Drawing.

## ทำไมต้องใช้ Aspose.Imaging สำหรับการวาดสี่เหลี่ยมใน .NET?
- **Cross‑platform** – ทำงานบน Windows, Linux, และ macOS.  
- **No native dependencies** – โค้ดที่จัดการโดย .NET อย่างเดียว, เหมาะสำหรับสภาพแวดล้อมเซิร์ฟเวอร์.  
- **Rich drawing API** – รองรับปากกา, แปรง, การทำ anti‑aliasing, และรูปทรงหลายประเภท.  
- **High performance** – ปรับให้ทำงานได้อย่างมีประสิทธิภาพกับภาพขนาดใหญ่และการประมวลผลเป็นชุด.

## Prerequisites

1. **Aspose.Imaging for .NET** – ดาวน์โหลดจาก [download page](https://releases.aspose.com/imaging/net/).  
2. **Development Environment** – Visual Studio, VS Code, หรือ IDE ที่รองรับ .NET ใดก็ได้.  
3. **.NET runtime** – .NET 6+ หรือ .NET Framework 4.7.2+.  

เมื่อเราตั้งค่าทุกอย่างเรียบร้อยแล้ว, มาเริ่มดูโค้ดกันเลย.

## วิธีสร้างภาพเปล่า Aspose ใน .NET

### ขั้นตอนที่ 1: นำเข้า namespace ที่จำเป็น

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Namespace เหล่านี้ให้คุณเข้าถึงคลาสภาพหลัก, ชนิดของแปรง, และตัวเลือกการบันทึกภาพ.

### ขั้นตอนที่ 2: สร้างภาพเปล่า (แคนวาส)

```csharp
string dataDir = "Your Document Directory";  // Set the path to your document directory
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Your drawing code will go here
        image.Save();
    }
}
```

ในบล็อกนี้เราจะ:
* กำหนดตำแหน่งเอาต์พุต (`dataDir`).  
* ตั้งค่า `BmpOptions` ให้ใช้รูปแบบพิกเซล 32‑bit.  
* สร้าง **blank image** ขนาด 100 × 100 พิกเซล.  

### ขั้นตอนที่ 3: วิธีวาดสี่เหลี่ยม .net ด้วย Aspose.Imaging

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` เติมสีพื้นหลังให้แคนวาส (สีเหลืองในตัวอย่างนี้).  
* `DrawRectangle` วาดสี่เหลี่ยมสองรูป — หนึ่งด้วยปากกาสีแดงธรรมดา, อีกหนึ่งด้วยแปรงสีฟ้าแบบทึบ, เพื่อให้เห็นความแตกต่าง.

### ขั้นตอนที่ 4: บันทึกภาพ

```csharp
image.Save();
```

การเรียก `Save` จะเขียนบิตแมปไปยังระบบไฟล์โดยใช้ตัวเลือกที่กำหนดไว้ก่อนหน้า.

## ปัญหาทั่วไป & เคล็ดลับ

| Issue | Reason | Fix |
|-------|--------|-----|
| **ภาพเปล่าแสดงเป็นสีดำ** | พื้นหลังไม่ได้ถูกเคลียร์ | เรียก `graphic.Clear(Color.YourColor)` ก่อนวาด. |
| **ข้อยกเว้นไฟล์ไม่พบ** | `dataDir` ชี้ไปยังโฟลเดอร์ที่ไม่มีอยู่ | ตรวจสอบให้แน่ใจว่าโฟลเดอร์มีอยู่หรือใช้ `Path.Combine` กับ `Environment.CurrentDirectory`. |
| **สีไม่ถูกต้อง** | ใช้ `System.Drawing.Color` แทน `Aspose.Imaging.Color` | ควรนำเข้า `Aspose.Imaging.Color` เสมอ. |
| **การทำงานช้าบนภาพขนาดใหญ่** | ใช้ `BmpOptions` เริ่มต้นที่มีบิตต่อพิกเซลสูง | เปลี่ยนเป็น `JpegOptions` หรือ `PngOptions` เพื่อบีบอัด. |

## คำถามที่พบบ่อย (ขยายเพิ่มเติม)

**ถาม: ฉันสามารถวาดรูปทรงอื่นนอกจากสี่เหลี่ยมได้หรือไม่?**  
ตอบ: ได้แน่นอน. Aspose.Imaging มีเมธอดเช่น `DrawEllipse`, `DrawLine`, และ `DrawPolygon`.

**ถาม: ไลบรารีนี้ฟรีสำหรับการใช้งานเชิงพาณิชย์หรือไม่?**  
ตอบ: ไม่, Aspose.Imaging เป็นผลิตภัณฑ์เชิงพาณิชย์, แต่คุณสามารถประเมินได้ด้วยรุ่นทดลองฟรีที่มีให้ [here](https://releases.aspose.com/).

**ถาม: วิธีนี้ทำงานได้ทั้งบน Windows และแอปพลิเคชันเว็บหรือไม่?**  
ตอบ: ใช่, โค้ดเดียวกันทำงานใน ASP.NET, Blazor, และแอปคอนโซล.

**ถาม: ฉันจะเปลี่ยนรูปแบบเอาต์พุตเป็น PNG ได้อย่างไร?**  
ตอบ: แทนที่ `BmpOptions` ด้วย `PngOptions` และปรับนามสกุลไฟล์ให้สอดคล้อง.

**ถาม: ฉันจะหาเอกสารรายละเอียดเพิ่มเติมได้จากที่ไหน?**  
ตอบ: เข้าถึงเอกสารอ้างอิง API เต็มรูปแบบ [here](https://reference.aspose.com/imaging/net/) และเข้าร่วมชุมชนใน [Aspose.Imaging forum](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2026-02-12  
**ทดสอบด้วย:** Aspose.Imaging 24.12 for .NET  
**ผู้เขียน:** Aspose