---
title: แปลงช่วงของเพจ DJVU เพื่อแยกรูปภาพใน Aspose.Imaging สำหรับ .NET
linktitle: แปลงช่วงของเพจ DJVU เพื่อแยกรูปภาพใน Aspose.Imaging สำหรับ .NET
second_title: Aspose.Imaging .NET Image Processing API
description: ค้นพบวิธีแปลงเพจ DJVU เพื่อแยกรูปภาพด้วย Aspose.Imaging สำหรับ .NET มีคำแนะนำทีละขั้นตอน ตัวอย่างโค้ด และคำถามที่พบบ่อย
type: docs
weight: 19
url: /th/net/image-format-conversion/convert-range-of-djvu-pages-to-separate-images/
---
หากคุณกำลังมองหาไลบรารี .NET ที่ทรงพลังเพื่อจัดการการแปลงรูปภาพและงานการจัดการ Aspose.Imaging for .NET เป็นตัวเลือกที่สมบูรณ์แบบ ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแปลงหน้า DJVU หลายหน้าให้เป็นรูปภาพแยกกันโดยใช้ Aspose.Imaging คุณจะพบคำแนะนำทีละขั้นตอนและข้อมูลโค้ดเพื่อช่วยให้คุณบรรลุภารกิจนี้

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกกระบวนการแปลง ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. Aspose.Imaging สำหรับไลบรารี .NET

 คุณจะต้องติดตั้ง Aspose.Imaging สำหรับ .NET หากคุณยังไม่มี คุณสามารถดาวน์โหลดได้จาก[Aspose.Imaging สำหรับเพจ .NET](https://releases.aspose.com/imaging/net/).

2. การพัฒนาสภาพแวดล้อม

เพื่อปฏิบัติตาม คุณควรมีสภาพแวดล้อมการพัฒนาที่ตั้งค่าด้วย Visual Studio หรือ .NET IDE อื่นๆ

## การนำเข้าเนมสเปซที่จำเป็น

ขั้นแรก คุณต้องรวมเนมสเปซที่จำเป็นในโค้ดของคุณเพื่อทำงานกับ Aspose.Imaging ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Djvu;
using Aspose.Imaging.FileFormats.Djvu.Options;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.RasterImage;
```

## การแปลงเพจ DJVU

ตอนนี้ เรามาแจกแจงขั้นตอนการแปลงช่วงของเพจ DJVU ให้เป็นอิมเมจแยกกันโดยใช้ Aspose.Imaging สำหรับ .NET ให้เป็นชุดขั้นตอนที่ปฏิบัติตามได้ง่าย

### ขั้นตอนที่ 1: โหลดอิมเมจ DJVU

 ในการเริ่มต้น คุณควรโหลดอิมเมจ DJVU ที่คุณต้องการแปลง แทนที่`"Your Document Directory"` ด้วยเส้นทางจริงไปยังไฟล์ DJVU ของคุณ

```csharp
string dataDir = "Your Document Directory";

// โหลดอิมเมจ DjVu
using (DjvuImage image = (DjvuImage)Image.Load(dataDir + "Sample.djvu"))
{
    // รหัสของคุณสำหรับการประมวลผลเพิ่มเติมจะอยู่ที่นี่
}
```

### ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการส่งออก

ตอนนี้สร้างอินสแตนซ์ของ`BmpOptions` และกำหนดค่าตัวเลือกที่ต้องการสำหรับรูปภาพผลลัพธ์ ในตัวอย่างนี้ เราตั้งค่า`BitsPerPixel` ถึง 32

```csharp
BmpOptions exportOptions = new BmpOptions();
exportOptions.BitsPerPixel = 32;
```

### ขั้นตอนที่ 3: กำหนดช่วงของหน้า

 หากต้องการระบุช่วงของเพจที่คุณต้องการส่งออก ให้สร้างอินสแตนซ์`IntRange` และเริ่มต้นด้วยช่วงหน้า ในกรณีนี้ เราจะส่งออกหน้าที่ 0 ถึง 2

```csharp
IntRange range = new IntRange(0, 2);
```

### ขั้นตอนที่ 4: วนซ้ำหน้าต่างๆ

ตอนนี้ วนซ้ำหน้าต่างๆ ภายในช่วงที่ระบุและบันทึกแต่ละหน้าเป็นอิมเมจ BMP แยกต่างหาก ไฟล์ DJVU ไม่รองรับการแบ่งชั้น ดังนั้นเราจึงบันทึกแต่ละหน้าแยกกัน

```csharp
int counter = 0;
foreach (var i in range.Range)
{
    exportOptions.MultiPageOptions = new DjvuMultiPageOptions(range.GetArrayOneItemFromIndex(counter));
    image.Save(dataDir + string.Format("{0}_out.bmp", counter++), exportOptions);
}
```

แค่นั้นแหละ! คุณได้แปลงหน้า DJVU หลายหน้าเป็นรูปภาพแยกกันสำเร็จโดยใช้ Aspose.Imaging สำหรับ .NET

## บทสรุป

Aspose.Imaging สำหรับ .NET ช่วยให้งานการแปลงรูปภาพง่ายขึ้น ทำให้เป็นตัวเลือกที่ยอดเยี่ยมสำหรับนักพัฒนา ในบทช่วยสอนนี้ เราได้แนะนำคุณตลอดกระบวนการแปลงหน้า DJVU เพื่อแยกรูปภาพทีละขั้นตอน ด้วยโค้ดและไลบรารีที่เหมาะสม การแปลงรูปภาพจึงกลายเป็นเรื่องง่าย

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Imaging สำหรับ .NET เป็นไลบรารี่ฟรีหรือไม่

 A1: ไม่ใช่ มันเป็นห้องสมุดเชิงพาณิชย์ แต่คุณสามารถดาวน์โหลดได้[ทดลองฟรี](https://releases.aspose.com/) เพื่อทดสอบความสามารถของตน

### คำถามที่ 2: ฉันสามารถซื้อใบอนุญาตชั่วคราวสำหรับ Aspose.Imaging สำหรับ .NET ได้หรือไม่

 A2: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้จาก[หน้าซื้อ](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 3: ฉันจะหาเอกสารสำหรับ Aspose.Imaging สำหรับ .NET ได้ที่ไหน

 A3: คุณสามารถสำรวจเอกสารประกอบที่ครอบคลุมได้[ที่นี่](https://reference.aspose.com/imaging/net/).

### คำถามที่ 4: Aspose.Imaging สำหรับ .NET รองรับรูปแบบรูปภาพใดบ้าง

A4: Aspose.Imaging สำหรับ .NET รองรับรูปแบบรูปภาพที่หลากหลาย รวมถึง BMP, JPEG, PNG, TIFF และอื่นๆ

### คำถามที่ 5: ฉันสามารถรับการสนับสนุนและความช่วยเหลือได้หรือไม่หากฉันประสบปัญหา

 A5: ได้ คุณสามารถขอความช่วยเหลือและเชื่อมต่อกับชุมชนได้ที่[Aspose ฟอรั่มการถ่ายภาพ](https://forum.aspose.com/).