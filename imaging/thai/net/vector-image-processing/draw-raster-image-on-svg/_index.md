---
title: วิธีวาดภาพแรสเตอร์บน SVG ใน Aspose.Imaging สำหรับ .NET
linktitle: วาดภาพแรสเตอร์บน SVG ใน Aspose.Imaging สำหรับ .NET
second_title: Aspose.Imaging .NET Image Processing API
description: เรียนรู้วิธีการวาดภาพแรสเตอร์บน SVG โดยใช้ Aspose.Imaging สำหรับ .NET ปรับปรุงแอปพลิเคชัน .NET ของคุณด้วยรูปภาพแบบไดนามิก
weight: 11
url: /th/net/vector-image-processing/draw-raster-image-on-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีวาดภาพแรสเตอร์บน SVG ใน Aspose.Imaging สำหรับ .NET


ในโลกของการเขียนโปรแกรม .NET Aspose.Imaging ถือเป็นไลบรารี่ที่เชื่อถือได้และอเนกประสงค์สำหรับจัดการงานต่างๆ ที่เกี่ยวข้องกับรูปภาพ ความสามารถอันน่าทึ่งประการหนึ่งที่มีให้คือความสามารถในการวาดภาพแรสเตอร์บนผืนผ้าใบ SVG ในคำแนะนำทีละขั้นตอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการวาดภาพแรสเตอร์บน SVG โดยใช้ Aspose.Imaging สำหรับ .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกรายละเอียด ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.Imaging สำหรับ .NET: คุณต้องติดตั้งไลบรารี ถ้าไม่เช่นนั้นคุณสามารถดาวน์โหลดได้จาก[Aspose.Imaging สำหรับหน้าดาวน์โหลด .NET](https://releases.aspose.com/imaging/net/).

-  ไดเรกทอรีเอกสารของคุณ: แทนที่`"Your Document Directory"` พร้อมเส้นทางจริงไปยังไดเร็กทอรีการทำงานของคุณ

ตอนนี้ เรามาแบ่งกระบวนการออกเป็นขั้นตอนง่ายๆ ดังต่อไปนี้:

## ขั้นตอนที่ 1: นำเข้าเนมสเปซที่จำเป็น

คุณต้องนำเข้าเนมสเปซที่จำเป็นเพื่อทำงานกับ Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## ขั้นตอนที่ 2: โหลดรูปภาพ

- ขั้นแรก โหลดภาพแรสเตอร์ที่คุณต้องการวาดบนผืนผ้าใบ SVG

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- จากนั้น โหลดภาพแคนวาส SVG ที่คุณต้องการวาดภาพแรสเตอร์

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## ขั้นตอนที่ 3: วาดภาพบนรูปภาพ SVG

ตอนนี้คุณสามารถเริ่มวาดภาพ SVG ที่มีอยู่ได้แล้ว เมื่อต้องการทำเช่นนี้ คุณต้องสร้างอินสแตนซ์ของ`SvgGraphics2D`: :

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## ขั้นตอนที่ 4: วาดภาพแรสเตอร์

- กำหนดขอบเขตที่คุณต้องการวาดภาพแรสเตอร์ และระบุขอบเขตแหล่งที่มาจากภาพแรสเตอร์

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## ขั้นตอนที่ 5: บันทึกผลลัพธ์

หลังจากวาดภาพแรสเตอร์บนผืนผ้าใบ SVG แล้ว คุณสามารถบันทึกภาพที่ได้:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## บทสรุป

ยินดีด้วย! คุณวาดภาพแรสเตอร์บนผืนผ้าใบ SVG ได้สำเร็จโดยใช้ Aspose.Imaging สำหรับ .NET สิ่งนี้มีประโยชน์อย่างเหลือเชื่อสำหรับการสร้างรูปภาพที่สมบูรณ์และไดนามิกภายในแอปพลิเคชัน .NET ของคุณ

 สำหรับข้อมูลเพิ่มเติมและเอกสารโดยละเอียด โปรดไปที่[Aspose.Imaging สำหรับเอกสาร .NET](https://reference.aspose.com/imaging/net/).

## คำถามที่พบบ่อย

### Aspose.Imaging สำหรับ .NET คืออะไร
   Aspose.Imaging สำหรับ .NET เป็นไลบรารีการประมวลผลรูปภาพที่มีประสิทธิภาพซึ่งช่วยให้นักพัฒนาสามารถสร้าง จัดการ และแปลงรูปภาพในรูปแบบต่างๆ ภายในแอปพลิเคชัน .NET

### ฉันสามารถใช้ Aspose.Imaging สำหรับ .NET ในโครงการเชิงพาณิชย์ได้หรือไม่
    ได้ คุณสามารถใช้ Aspose.Imaging สำหรับ .NET ได้ทั้งในโครงการเชิงพาณิชย์และไม่ใช่เชิงพาณิชย์ รายละเอียดใบอนุญาตสามารถดูได้ที่[หน้าซื้อ](https://purchase.aspose.com/buy).

### มีการทดลองใช้ฟรีหรือไม่?
    ใช่ คุณสามารถทดลองใช้ Aspose.Imaging สำหรับ .NET ได้ฟรีจาก[ที่นี่](https://releases.aspose.com/).

### ฉันจะรับการสนับสนุนหรือถามคำถามได้ที่ไหน
    หากคุณมีคำถามหรือต้องการความช่วยเหลือ คุณสามารถไปที่[Aspose ฟอรั่มการถ่ายภาพ](https://forum.aspose.com/).

### ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Imaging สำหรับ .NET ได้อย่างไร
    คุณสามารถรับใบอนุญาตชั่วคราวได้จาก[ที่นี่](https://purchase.aspose.com/temporary-license/).



{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
