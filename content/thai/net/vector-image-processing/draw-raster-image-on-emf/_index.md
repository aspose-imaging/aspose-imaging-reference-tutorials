---
title: วาดภาพแรสเตอร์บน EMF ด้วย Aspose.Imaging สำหรับ .NET
linktitle: วาดภาพแรสเตอร์บน EMF ใน Aspose.Imaging สำหรับ .NET
second_title: Aspose.Imaging .NET Image Processing API
description: เรียนรู้วิธีการวาดภาพแรสเตอร์บนไฟล์ EMF โดยใช้ Aspose.Imaging สำหรับ .NET สร้างภาพที่น่าทึ่งได้อย่างง่ายดาย
type: docs
weight: 10
url: /th/net/vector-image-processing/draw-raster-image-on-emf/
---

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนทีละขั้นตอนเกี่ยวกับวิธีการวาดภาพแรสเตอร์บน EMF (Enhanced Metafile) โดยใช้ Aspose.Imaging สำหรับ .NET Aspose.Imaging เป็นไลบรารีอันทรงพลังที่ช่วยให้คุณทำงานกับรูปแบบรูปภาพที่หลากหลายในแอปพลิเคชัน .NET ของคุณ ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการวาดภาพแรสเตอร์ลงบนไฟล์ EMF คุณจะได้เรียนรู้วิธีนำเข้าเนมสเปซที่จำเป็น และเราจะแบ่งแต่ละตัวอย่างออกเป็นหลายขั้นตอนเพื่อทำให้กระบวนการเรียนรู้ง่ายขึ้น

มาเริ่มกันเลย!

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน คุณควรมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. Visual Studio: คุณต้องติดตั้ง Visual Studio บนคอมพิวเตอร์ของคุณเพื่อเขียนและเรียกใช้โค้ด .NET

2.  Aspose.Imaging for .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Imaging for .NET แล้ว คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/imaging/net/).

3. ภาพแรสเตอร์: เตรียมภาพแรสเตอร์ (เช่น ไฟล์ PNG) ที่คุณต้องการวาดลงในไฟล์ EMF

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ Visual Studio ของคุณ คุณจะต้องนำเข้าเนมสเปซที่จำเป็นเพื่อทำงานกับ Aspose.Imaging เพิ่มเนมสเปซต่อไปนี้ลงในไฟล์โค้ดของคุณ:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Emf;
using Aspose.Imaging.FileFormats.Png;
using Aspose.Imaging.Graphics;
using System;
```

ตอนนี้เรามีข้อกำหนดเบื้องต้นและเนมสเปซแล้ว เรามาแบ่งตัวอย่างออกเป็นหลายขั้นตอนกัน

## ขั้นตอนที่ 1: โหลดรูปภาพที่จะวาด

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
{
    // รหัสของคุณสำหรับขั้นตอนที่ 1 อยู่ที่นี่
}
```

 ในขั้นตอนนี้ เราจะโหลดภาพแรสเตอร์ที่คุณต้องการวาดลงในไฟล์ EMF แทนที่`"Your Document Directory"` พร้อมเส้นทางสู่ภาพของคุณ

## ขั้นตอนที่ 2: โหลดพื้นผิวการวาด EMF

```csharp
using (EmfImage canvasImage = (EmfImage)Image.Load(dataDir + "input.emf"))
{
    // รหัสของคุณสำหรับขั้นตอนที่ 2 อยู่ที่นี่
}
```

 ที่นี่ เราโหลดไฟล์ EMF ที่จะทำหน้าที่เป็นพื้นผิวการวาดภาพสำหรับรูปภาพของเรา ตรวจสอบให้แน่ใจว่าได้เปลี่ยน`"input.emf"` พร้อมเส้นทางไปยังไฟล์ EMF ของคุณ

## ขั้นตอนที่ 3: สร้างกราฟิกตัวบันทึก EMF

```csharp
EmfRecorderGraphics2D graphics = EmfRecorderGraphics2D.FromEmfImage(canvasImage);
```

 ในขั้นตอนนี้ เราจะสร้างอินสแตนซ์ของ`EmfRecorderGraphics2D` จากภาพ EMF ซึ่งช่วยให้เราสามารถบันทึกการดำเนินการวาดภาพได้

## ขั้นตอนที่ 4: วาดภาพแรสเตอร์

```csharp
graphics.DrawImage(
    imageToDraw,
    new Rectangle(67, 67, canvasImage.Width, canvasImage.Height),
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    GraphicsUnit.Pixel);
```

 ในขั้นตอนนี้เราใช้`DrawImage`วิธีการวาดภาพแรสเตอร์ที่โหลดลงบนไฟล์ EMF คุณสามารถระบุสี่เหลี่ยมต้นทางและปลายทางเพื่อควบคุมตำแหน่งและขนาดของภาพที่วาดได้

## ขั้นตอนที่ 5: บันทึกรูปภาพผลลัพธ์

```csharp
using (EmfImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "input.DrawImage.emf");
}
```

 สุดท้าย เราจะบันทึกภาพ EMF ที่เป็นผลลัพธ์พร้อมกับภาพแรสเตอร์ที่วาดลงในไฟล์ ไฟล์จะถูกบันทึกด้วยชื่อ "input.DrawImage.emf" ในไดเร็กทอรีที่ระบุโดย`dataDir`.

ยินดีด้วย! คุณวาดภาพแรสเตอร์บนไฟล์ EMF ได้สำเร็จโดยใช้ Aspose.Imaging สำหรับ .NET รู้สึกอิสระที่จะสำรวจและทดลองกับสี่เหลี่ยมต้นทางและปลายทางที่แตกต่างกันเพื่อให้ได้เอฟเฟกต์ที่ต้องการ

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีใช้ Aspose.Imaging สำหรับ .NET เพื่อวาดภาพแรสเตอร์ลงบนไฟล์ EMF ด้วยการทำตามคำแนะนำทีละขั้นตอน คุณสามารถรวมฟังก์ชันนี้เข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างง่ายดาย

ขอให้สนุกกับการสร้างสรรค์ภาพที่น่าทึ่งด้วย Aspose.Imaging!

## คำถามที่พบบ่อย

### 1. ฉันสามารถวาดภาพหลายภาพในไฟล์ EMF เดียวกันได้หรือไม่

ได้ คุณสามารถวาดภาพหลายภาพในไฟล์ EMF เดียวกันได้โดยการทำซ้ำขั้นตอนการวาดภาพด้วยแหล่งที่มาและปลายทางที่แตกต่างกัน

### 2. Aspose.Imaging เข้ากันได้กับ .NET Core หรือไม่

ใช่ Aspose.Imaging สำหรับ .NET เข้ากันได้กับทั้ง .NET Framework และ .NET Core

### 3. ฉันจะใช้การแปลงกับภาพที่วาด เช่น การหมุนหรือการปรับขนาดได้อย่างไร

 คุณสามารถใช้การแปลงได้โดยจัดการสี่เหลี่ยมต้นทางและปลายทางใน`DrawImage` วิธี.

### 4. ฉันสามารถวาดกราฟิกแบบเวกเตอร์บนไฟล์ EMF ได้หรือไม่

ได้ คุณสามารถวาดกราฟิกและรูปร่างแบบเวกเตอร์ได้ นอกเหนือจากภาพแรสเตอร์โดยใช้ Aspose.Imaging สำหรับ .NET

### 5. ฉันจะรับการสนับสนุนสำหรับ Aspose.Imaging ได้ที่ไหน

 สำหรับการสนับสนุนและความช่วยเหลือ คุณสามารถไปที่ฟอรัม Aspose.Imaging[ที่นี่](https://forum.aspose.com/).
