---
"description": "เรียนรู้วิธีการวาดภาพแรสเตอร์บน SVG โดยใช้ Aspose.Imaging สำหรับ .NET ปรับปรุงแอปพลิเคชัน .NET ของคุณด้วยภาพไดนามิก"
"linktitle": "วาดภาพแรสเตอร์บน SVG ใน Aspose.Imaging สำหรับ .NET"
"second_title": "API การประมวลผลภาพ Aspose.Imaging .NET"
"title": "วิธีวาดภาพแรสเตอร์บน SVG ใน Aspose.Imaging สำหรับ .NET"
"url": "/th/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# วิธีวาดภาพแรสเตอร์บน SVG ใน Aspose.Imaging สำหรับ .NET


ในโลกของการเขียนโปรแกรม .NET Aspose.Imaging เป็นไลบรารีที่เชื่อถือได้และใช้งานได้หลากหลายสำหรับจัดการงานต่างๆ ที่เกี่ยวข้องกับรูปภาพ ความสามารถที่น่าสนใจอย่างหนึ่งที่ Aspose.Imaging มอบให้คือความสามารถในการวาดภาพแรสเตอร์บนแคนวาส SVG ในคู่มือทีละขั้นตอนนี้ เราจะแนะนำคุณเกี่ยวกับขั้นตอนการวาดภาพแรสเตอร์บน SVG โดยใช้ Aspose.Imaging สำหรับ .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกรายละเอียด โปรดตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

- Aspose.Imaging สำหรับ .NET: คุณต้องติดตั้งไลบรารี หากไม่มี คุณสามารถดาวน์โหลดได้จาก [หน้าดาวน์โหลด Aspose.Imaging สำหรับ .NET](https://releases-aspose.com/imaging/net/).

- ไดเรกทอรีเอกสารของคุณ: แทนที่ `"Your Document Directory"` พร้อมเส้นทางจริงไปยังไดเร็กทอรีการทำงานของคุณ

ตอนนี้เรามาแบ่งกระบวนการออกเป็นขั้นตอนที่ทำตามได้ง่าย ๆ:

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

- ขั้นตอนต่อไป โหลดภาพ SVG Canvas ที่คุณต้องการวาดภาพแรสเตอร์

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## ขั้นตอนที่ 3: การวาดภาพบนภาพ SVG

ตอนนี้คุณสามารถเริ่มวาดภาพ SVG ที่มีอยู่ได้แล้ว ในการดำเนินการนี้ คุณต้องสร้างอินสแตนซ์ของ `SvgGraphics2D`-

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## ขั้นตอนที่ 4: วาดภาพแรสเตอร์

- กำหนดขอบเขตที่คุณต้องการวาดภาพแรสเตอร์และระบุภูมิภาคแหล่งที่มาจากภาพแรสเตอร์

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## ขั้นตอนที่ 5: บันทึกผลลัพธ์

หลังจากวาดภาพแรสเตอร์บนผืนผ้าใบ SVG แล้ว คุณสามารถบันทึกรูปภาพที่ได้:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## บทสรุป

ขอแสดงความยินดี! คุณได้วาดภาพแรสเตอร์บนผืนผ้าใบ SVG สำเร็จแล้วโดยใช้ Aspose.Imaging สำหรับ .NET วิธีนี้มีประโยชน์อย่างยิ่งในการสร้างภาพที่มีมิติและมีชีวิตชีวาภายในแอปพลิเคชัน .NET ของคุณ

สำหรับข้อมูลเพิ่มเติมและเอกสารรายละเอียด โปรดไปที่ [เอกสาร Aspose.Imaging สำหรับ .NET](https://reference-aspose.com/imaging/net/).

## คำถามที่พบบ่อย

### Aspose.Imaging สำหรับ .NET คืออะไร?
   Aspose.Imaging สำหรับ .NET เป็นไลบรารีประมวลผลรูปภาพอันทรงพลังที่ช่วยให้นักพัฒนาสามารถสร้าง จัดการ และแปลงรูปภาพในรูปแบบต่างๆ ภายในแอปพลิเคชัน .NET ได้

### ฉันสามารถใช้ Aspose.Imaging สำหรับ .NET ในโครงการเชิงพาณิชย์ได้หรือไม่
   ใช่ คุณสามารถใช้ Aspose.Imaging สำหรับ .NET ในโปรเจ็กต์ทั้งเชิงพาณิชย์และไม่ใช่เชิงพาณิชย์ รายละเอียดการอนุญาตสิทธิ์สามารถดูได้ที่ [หน้าการซื้อ](https://purchase-aspose.com/buy).

### มีการทดลองใช้ฟรีหรือไม่?
   ใช่ คุณสามารถรับรุ่นทดลองใช้ Aspose.Imaging สำหรับ .NET ได้ฟรีจาก [ที่นี่](https://releases-aspose.com/).

### ฉันจะได้รับการสนับสนุนหรือถามคำถามได้ที่ไหน
   หากคุณมีคำถามหรือต้องการความช่วยเหลือ คุณสามารถเยี่ยมชมได้ที่ [ฟอรั่ม Aspose.Imaging](https://forum-aspose.com/).

### ฉันจะรับใบอนุญาตชั่วคราวสำหรับ Aspose.Imaging สำหรับ .NET ได้อย่างไร
   คุณสามารถรับใบอนุญาตชั่วคราวได้จาก [ที่นี่](https://purchase-aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}