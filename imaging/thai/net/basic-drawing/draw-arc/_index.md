---
date: 2026-02-09
description: เรียนรู้วิธีวาดโค้งโดยใช้ Aspose.Imaging สำหรับ .NET รวมถึงวิธีบันทึกไฟล์
  BMP ตั้งขนาดภาพ และตั้งค่าพื้นหลังของกราฟิก คู่มือขั้นตอนต่อขั้นตอนสำหรับการสร้างภาพ
  BMP.
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: วิธีวาดส่วนโค้งด้วย Aspose.Imaging สำหรับ .NET
url: /th/net/basic-drawing/draw-arc/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# วิธีวาดโค้ง (Arc) ด้วย Aspose.Imaging สำหรับ .NET

ในโลกของการประมวลผลภาพ, **วิธีวาดโค้ง** เป็นงานทั่วไปที่สามารถเพิ่มความสวยงามให้กับกราฟิกใด ๆ ได้ ด้วย Aspose.Imaging สำหรับ .NET คุณสามารถสร้างภาพ BMP, ตั้งค่าขนาดภาพ, และวาดโค้งด้วยปากกาได้เพียงไม่กี่บรรทัดของ C# โดยตอนท้ายของบทเรียนนี้คุณจะรู้วิธีวาดโค้ง, ตั้งค่าพื้นหลังกราฟิก, และบันทึกไฟล์ BMP ที่ได้อย่างง่ายดาย

## คำตอบสั้น
- **โค้ดสร้างอะไรขึ้นมา?** ภาพ BMP ขนาด 100 × 100 พิกเซลที่มีพื้นหลังสีเหลืองและโค้งสีดำ.  
- **ใช้ไลบรารีใด?** Aspose.Imaging สำหรับ .NET.  
- **ต้องการไลเซนส์หรือไม่?** รุ่นทดลองใช้ฟรีเพียงพอสำหรับการพัฒนา; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **สามารถเปลี่ยนขนาดภาพได้หรือไม่?** ได้ – ปรับพารามิเตอร์ความกว้างและความสูงในคำสั่ง `Image.Create`.  
- **รูปแบบไฟล์ผลลัพธ์คงที่หรือไม่?** ตัวอย่างบันทึกเป็นไฟล์ BMP แต่สามารถใช้รูปแบบใดก็ได้ที่ Aspose.Imaging รองรับ.

## การวาดโค้ง (arc) ใน Aspose.Imaging คืออะไร?
การวาดโค้งหมายถึงการสร้างส่วนของเส้นโค้งที่กำหนดโดยสี่เหลี่ยมขอบเขต, มุมเริ่มต้น, และมุมการสวิง. Aspose.Imaging มีเมธอด `Graphics.DrawArc` ที่ให้คุณ **วาดโค้งด้วยปากกา** และควบคุมลักษณะการแสดงผลทั้งหมด.

## ทำไมต้องใช้ Aspose.Imaging สำหรับงานนี้?
- **ควบคุมเต็มที่ต่อมิติของภาพ, ความลึกสี, และรูปแบบไฟล์**.  
- **ไม่มีการพึ่งพาไลบรารีภายนอก** – ทำงานทั้งหมดบน .NET แท้.  
- **ประสิทธิภาพสูง** สำหรับการสร้างกราฟิกจำนวนมากบนเซิร์ฟเวอร์.

## สิ่งที่ต้องเตรียม

ก่อนที่เราจะลงลึกในโค้ด, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Aspose.Imaging สำหรับ .NET** – ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ [ที่นี่](https://releases.aspose.com/imaging/net/).  
2. **สภาพแวดล้อมการพัฒนา .NET** (Visual Studio, VS Code หรือคอมไพเลอร์ C# ใดก็ได้).  

เมื่อเรามีสิ่งที่จำเป็นพร้อมแล้ว, มาเริ่มวาดกันเถอะ!

## การนำเข้าเนมสเปซที่จำเป็น

เพื่อทำงานกับ Aspose.Imaging คุณต้องนำเนมสเปซที่เกี่ยวข้องเข้ามาในสโคป:

### ขั้นตอนที่ 1: นำเข้าเนมสเปซ

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

คำสั่ง `using` เหล่านี้ทำให้คุณเข้าถึงคลาสสำหรับสร้างภาพ, จัดการกราฟิก, และการอ่าน/เขียนไฟล์

## วิธีวาดโค้ง (Arc) ด้วย Aspose.Imaging สำหรับ .NET

เราจะแบ่งกระบวนการออกเป็นสามขั้นตอนที่ชัดเจน: สร้างภาพ, เตรียมพื้นผิวกราฟิก, และสุดท้ายวาดโค้ง.

### ขั้นตอนที่ 1: ตั้งค่าภาพ (กำหนดขนาดภาพและสร้างภาพ BMP)

```csharp
// Specify the directory where you want to save the image
string dataDir = "Your Document Directory";

// Create an instance of FileStream to save the image
using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
{
    // Create an instance of BmpOptions and set its properties
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;

    // Set the source for BmpOptions and create an instance of Image
    saveOptions.Source = new StreamSource(stream);
    using (Image image = Image.Create(saveOptions, 100, 100))
    {
```

ที่นี่เราจะ **กำหนดขนาดภาพ** เป็น 100 × 100 พิกเซลและตั้งค่าตัวเลือก BMP. `FileStream` ทำให้เรามั่นใจว่า **บันทึกไฟล์ BMP** ไปยังตำแหน่งที่ต้องการ.

### ขั้นตอนที่ 2: เริ่มต้น Graphics และตั้งค่าพื้นหลังกราฟิก

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

อ็อบเจ็กต์ `Graphics` ให้เราวาดบนภาพได้. โดยการเรียก `Clear(Color.Yellow)` เรา **ตั้งค่าพื้นหลังกราฟิก** เป็นสีเหลืองสด ทำให้โค้งเด่นชัด.

### ขั้นตอนที่ 3: กำหนดพารามิเตอร์ของโค้งและวาดโค้งด้วยปากกา

```csharp
        // Define the parameters for the arc
        int width = 100;
        int height = 200;
        int startAngle = 45;
        int sweepAngle = 270;

        // Draw the arc
        graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);

        // Save the changes
        image.Save();
    }
    stream.Close();
}
```

- `width` และ `height` กำหนดสี่เหลี่ยมขอบเขต, ซึ่งโดยอ้อมเป็นการ **กำหนดขนาดภาพ** สำหรับโค้ง.  
- อ็อบเจ็กต์ `Pen` คือสิ่งที่ทำให้เราสามารถ **วาดโค้งด้วยปากกา** สีดำได้.  
- หลังจากวาดเสร็จ, `image.Save()` จะเขียน **ไฟล์ BMP** ลงดิสก์.

## ปัญหาที่พบบ่อยและเคล็ดลับ

- โค้งไม่แสดง? ตรวจสอบให้แน่ใจว่าสีปากกาตรงกันข้ามกับพื้นหลัง (เช่น สีดำบนสีเหลือง).  
- ขนาดไม่ถูกต้อง? จำไว้ว่าสี่เหลี่ยมขอบเขตของโค้งอาจใหญ่กว่าภาพ; ปรับ `width`/`height` หรือขนาดภาพให้เหมาะสม.  
- เคล็ดลับประสิทธิภาพ: ใช้อ็อบเจ็กต์ `Graphics` ตัวเดียวซ้ำหากต้องการวาดหลายรูปบนภาพเดียว.

## คำถามที่พบบ่อย

### Q1: จะหาเอกสารประกอบของ Aspose.Imaging สำหรับ .NET ได้จากที่ไหน?

A1: คุณสามารถอ้างอิงเอกสารได้ที่ [นี่](https://reference.aspose.com/imaging/net/) สำหรับข้อมูลโดยละเอียดเกี่ยวกับ Aspose.Imaging สำหรับ .NET.

### Q2: จะดาวน์โหลด Aspose.Imaging สำหรับ .NET ได้อย่างไร?

A2: คุณสามารถดาวน์โหลด Aspose.Imaging สำหรับ .NET จากเว็บไซต์ [ที่นี่](https://releases.aspose.com/imaging/net/).

### Q3: มีรุ่นทดลองใช้ฟรีสำหรับ Aspose.Imaging สำหรับ .NET หรือไม่?

A3: ใช่, คุณสามารถรับรุ่นทดลองใช้ฟรีได้ที่ [นี่](https://releases.aspose.com/) เพื่อทดลอง Aspose.Imaging สำหรับ .NET.

### Q4: ต้องการไลเซนส์ชั่วคราวสำหรับ Aspose.Imaging สำหรับ .NET หรือไม่?

A4: หากคุณต้องการไลเซนส์ชั่วคราว, คุณสามารถรับได้ที่ [นี่](https://purchase.aspose.com/temporary-license/).

### Q5: จะหาการสนับสนุนหรือถามคำถามเกี่ยวกับ Aspose.Imaging สำหรับ .NET ได้จากที่ไหน?

A5: คุณสามารถเยี่ยมชมฟอรั่ม Aspose.Imaging เพื่อรับการสนับสนุนและการสนทนาได้ที่ [นี่](https://forum.aspose.com/).

---

**Last Updated:** 2026-02-09  
**Tested With:** Aspose.Imaging 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}