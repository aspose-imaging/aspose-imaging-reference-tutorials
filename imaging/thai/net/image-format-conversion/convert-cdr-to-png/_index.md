---
title: แปลง CDR เป็น PNG ด้วย Aspose.Imaging สำหรับ .NET
linktitle: แปลง CDR เป็น PNG ใน Aspose.Imaging สำหรับ .NET
second_title: Aspose.Imaging .NET Image Processing API
description: เรียนรู้วิธีแปลง CDR เป็น PNG ใน .NET โดยใช้ Aspose.Imaging คำแนะนำทีละขั้นตอนนี้ทำให้กระบวนการง่ายขึ้น
weight: 11
url: /th/net/image-format-conversion/convert-cdr-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง CDR เป็น PNG ด้วย Aspose.Imaging สำหรับ .NET

## การแนะนำ

คุณกำลังมองหาวิธีที่มีประสิทธิภาพและประสิทธิผลในการแปลงไฟล์ CorelDRAW (CDR) เป็นรูปแบบ PNG ในแอปพลิเคชัน .NET ของคุณหรือไม่? Aspose.Imaging สำหรับ .NET นำเสนอโซลูชันที่เชื่อถือได้สำหรับงานนี้ ในคำแนะนำทีละขั้นตอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแปลงไฟล์ CDR เป็น PNG โดยใช้ Aspose.Imaging คุณไม่จำเป็นต้องเป็นผู้เชี่ยวชาญใน .NET เพื่อติดตามบทช่วยสอนนี้ มาเริ่มกันเลย.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกกระบวนการแปลง ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  Aspose.Imaging for .NET: ดาวน์โหลดและติดตั้ง Aspose.Imaging for .NET จาก[เว็บไซต์](https://releases.aspose.com/imaging/net/). คุณสามารถเลือกระหว่างรุ่นทดลองใช้ฟรีหรือรุ่นที่ซื้อได้ตามความต้องการของคุณ

2. สภาพแวดล้อมการพัฒนา C#: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา C# บนระบบของคุณ รวมถึง Visual Studio หรือโปรแกรมแก้ไขโค้ดอื่น

3. ไฟล์ CDR: คุณควรมีไฟล์ CDR ที่คุณต้องการแปลงเป็น PNG คุณสามารถใช้ไฟล์ CDR ของคุณเองหรือดาวน์โหลดไฟล์เพื่อทดสอบได้

ตอนนี้ เรามาเริ่มด้วยกระบวนการแปลงจริงกันก่อน

## ขั้นตอนที่ 1: นำเข้าเนมสเปซ

ขั้นตอนแรกคือการนำเข้าเนมสเปซที่จำเป็น เนมสเปซเป็นเหมือนคอนเทนเนอร์ที่เก็บคลาสและวิธีการที่คุณจะใช้ตลอดโปรเจ็กต์ของคุณ ในไฟล์ C# ของคุณ ให้เพิ่มเนมสเปซต่อไปนี้:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Text.TextOptions;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## ขั้นตอนที่ 2: โหลดไฟล์ CDR

ในขั้นตอนนี้ คุณจะโหลดไฟล์ CDR ที่คุณต้องการแปลงเป็นโปรเจ็กต์ C# ของคุณ ตรวจสอบให้แน่ใจว่าคุณระบุเส้นทางไฟล์ที่ถูกต้อง

```csharp
string dataDir = "Your Document Directory"; // ระบุไดเร็กทอรีเอกสารของคุณ
string inputFileName = dataDir + "SimpleShapes.cdr";
using (CdrImage image = (CdrImage)Image.Load(inputFileName))
{
    // รหัสสำหรับการแปลงของคุณจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการแปลง PNG

ก่อนการแปลง คุณสามารถกำหนดค่าตัวเลือกการแปลง PNG ได้ ตัวอย่างเช่น คุณสามารถตั้งค่าประเภทสี ความละเอียด และอื่นๆ ได้ นี่คือตัวอย่าง:

```csharp
PngOptions options = new PngOptions();
options.ColorType = PngColorType.TruecolorWithAlpha;
options.VectorRasterizationOptions = (VectorRasterizationOptions)image.GetDefaultOptions(new object[] { Color.White, image.Width, image.Height });
options.VectorRasterizationOptions.TextRenderingHint = TextRenderingHint.SingleBitPerPixel;
options.VectorRasterizationOptions.SmoothingMode = SmoothingMode.None;
```

## ขั้นตอนที่ 4: ทำการแปลง

ถึงเวลาแปลงไฟล์ CDR เป็น PNG ด้วยตัวเลือกที่ระบุ:

```csharp
image.Save(dataDir + "SimpleShapes.png", options);
```

## ขั้นตอนที่ 5: ทำความสะอาด

หลังจากการแปลงเสร็จสมบูรณ์ คุณสามารถล้างข้อมูลโดยการลบไฟล์ชั่วคราวหากจำเป็น

```csharp
File.Delete(dataDir + "SimpleShapes.png");
```

## บทสรุป

ในคำแนะนำทีละขั้นตอนนี้ เราได้สำรวจวิธีการแปลงไฟล์ CDR เป็นรูปแบบ PNG โดยใช้ Aspose.Imaging สำหรับ .NET ด้วยเนมสเปซที่เหมาะสม การโหลด การกำหนดค่าตัวเลือก และการดำเนินการแปลง คุณสามารถรวมกระบวนการนี้เข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างราบรื่น Aspose.Imaging ทำให้กระบวนการแปลงง่ายขึ้นและเสนอตัวเลือกการปรับแต่งที่หลากหลาย

ตอนนี้คุณสามารถปลดล็อกพลังของ Aspose.Imaging เพื่อปรับปรุงแอปพลิเคชัน .NET ของคุณโดยการแปลงไฟล์ CDR เป็นรูปแบบ PNG ได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Imaging สำหรับ .NET คืออะไร

คำตอบ 1: Aspose.Imaging สำหรับ .NET เป็นไลบรารีที่ครอบคลุมซึ่งช่วยให้นักพัฒนาสามารถทำงานกับรูปแบบรูปภาพที่หลากหลาย รวมถึง CorelDRAW (CDR) ในแอปพลิเคชัน .NET ของตน

### คำถามที่ 2: ฉันสามารถลองใช้ Aspose.Imaging ฟรีก่อนซื้อได้หรือไม่

 ตอบ 2: ได้ คุณสามารถดาวน์โหลด Aspose.Imaging สำหรับ .NET รุ่นทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: Aspose.Imaging เหมาะสำหรับการแปลงไฟล์ CDR เป็น PNG เป็นชุดหรือไม่

A3: ใช่ Aspose.Imaging สำหรับ .NET เหมาะสำหรับการแปลงไฟล์ CDR เป็น PNG ทั้งแบบเดี่ยวและแบบชุด

### คำถามที่ 4: Aspose.Imaging รองรับรูปแบบรูปภาพอื่นใดบ้าง

A4: Aspose.Imaging รองรับรูปแบบภาพที่หลากหลาย รวมถึง BMP, JPEG, TIFF และอื่นๆ อีกมากมาย

### คำถามที่ 5: ฉันจะรับการสนับสนุนหรือถามคำถามเกี่ยวกับ Aspose.Imaging สำหรับ .NET ได้ที่ไหน

 A5: คุณสามารถเยี่ยมชม[Aspose ฟอรั่มการถ่ายภาพ](https://forum.aspose.com/) สำหรับการสนับสนุน คำถาม และการอภิปราย
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
