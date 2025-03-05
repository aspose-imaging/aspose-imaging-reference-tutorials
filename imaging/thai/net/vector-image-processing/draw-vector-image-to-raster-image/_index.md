---
title: วาดภาพเวกเตอร์เป็นภาพแรสเตอร์ใน Aspose.Imaging สำหรับ .NET
linktitle: วาดภาพเวกเตอร์เป็นภาพแรสเตอร์ใน Aspose.Imaging สำหรับ .NET
second_title: Aspose.Imaging .NET Image Processing API
description: เรียนรู้วิธีแปลงภาพเวกเตอร์เป็นภาพแรสเตอร์ใน .NET โดยใช้ Aspose.Imaging คำแนะนำทีละขั้นตอนเพื่อการประมวลผลภาพที่มีประสิทธิภาพ
type: docs
weight: 13
url: /th/net/vector-image-processing/draw-vector-image-to-raster-image/
---

คุณต้องการแปลงภาพเวกเตอร์เป็นภาพแรสเตอร์อย่างง่ายดายในแอปพลิเคชัน .NET ของคุณหรือไม่? Aspose.Imaging สำหรับ .NET มอบโซลูชันที่มีประสิทธิภาพสำหรับงานนี้ ในคำแนะนำทีละขั้นตอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการวาดภาพเวกเตอร์เป็นภาพแรสเตอร์โดยใช้ Aspose.Imaging สำหรับ .NET 

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

### 1. Aspose.Imaging สำหรับ .NET

 คุณควรติดตั้ง Aspose.Imaging สำหรับ .NET แล้ว หากยังไม่มีก็สามารถดาวน์โหลดได้จากเว็บไซต์ที่[ดาวน์โหลด Aspose.Imaging สำหรับ .NET](https://releases.aspose.com/imaging/net/).

### 2. สภาพแวดล้อมการพัฒนา .NET

ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา .NET บนคอมพิวเตอร์ของคุณ คุณสามารถใช้ Visual Studio หรือเครื่องมือพัฒนา .NET อื่นๆ ได้

ตอนนี้ เรามาแจกแจงขั้นตอนการวาดภาพเวกเตอร์เป็นภาพแรสเตอร์เป็นขั้นตอนง่ายๆ และปฏิบัติตามง่าย:

## ขั้นตอนที่ 1: เริ่มต้นโครงการของคุณ

เริ่มต้นด้วยการสร้างโครงการ .NET ใหม่ในสภาพแวดล้อมการพัฒนาของคุณ ตรวจสอบให้แน่ใจว่าคุณได้รวม Aspose.Imaging สำหรับ .NET ไว้ในโปรเจ็กต์ของคุณ

## ขั้นตอนที่ 2: โหลดภาพเวกเตอร์

ในขั้นตอนนี้ เราจะโหลดภาพเวกเตอร์ (ในรูปแบบ SVG) ที่คุณต้องการแปลงเป็นภาพแรสเตอร์

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## ขั้นตอนที่ 3: แรสเตอร์ภาพเวกเตอร์

ตอนนี้ เราต้องแรสเตอร์รูปภาพ SVG เป็นรูปแบบ PNG นี่คือจุดที่การแปลงจากเวกเตอร์เป็นแรสเตอร์เกิดขึ้น

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## ขั้นตอนที่ 4: โหลดภาพแรสเตอร์

หลังจากการแรสเตอร์แล้ว ให้โหลดรูปภาพ PNG จากสตรีมเพื่อวาดภาพเพิ่มเติม

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## ขั้นตอนที่ 5: วาดภาพแรสเตอร์

ตอนนี้เราสามารถวาดภาพแรสเตอร์บนรูปภาพ SVG ที่มีอยู่ได้แล้ว

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## ขั้นตอนที่ 6: บันทึกผลลัพธ์

สุดท้ายให้บันทึกภาพผลลัพธ์ ตอนนี้คุณมีภาพแรสเตอร์ที่มีภาพเวกเตอร์ของคุณแล้ว

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้สาธิตวิธีการแปลงภาพเวกเตอร์เป็นภาพแรสเตอร์โดยใช้ Aspose.Imaging สำหรับ .NET ด้วยขั้นตอนง่ายๆ เหล่านี้ คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างง่ายดาย

### คำถามที่พบบ่อย

### Aspose.Imaging สำหรับ .NET คืออะไร
Aspose.Imaging สำหรับ .NET คือไลบรารี .NET ที่ให้คุณลักษณะการประมวลผลรูปภาพที่มีประสิทธิภาพ รวมถึงความสามารถในการทำงานกับรูปแบบรูปภาพต่างๆ แปลงรูปภาพ และดำเนินการจัดการรูปภาพขั้นสูง

### ฉันจะหาเอกสารประกอบสำหรับ Aspose.Imaging สำหรับ .NET ได้ที่ไหน
 คุณสามารถค้นหาเอกสารประกอบสำหรับ Aspose.Imaging สำหรับ .NET ได้[ที่นี่](https://reference.aspose.com/imaging/net/).

### มีรุ่นทดลองใช้ฟรีหรือไม่?
 ใช่ คุณสามารถเข้าถึง Aspose.Imaging สำหรับ .NET รุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### ฉันจะได้รับใบอนุญาตชั่วคราวสำหรับ Aspose.Imaging สำหรับ .NET ได้อย่างไร
 หากคุณต้องการใบอนุญาตชั่วคราว คุณสามารถขอรับได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### ฉันจะรับการสนับสนุนสำหรับ Aspose.Imaging สำหรับ .NET ได้ที่ไหน
 สำหรับการสนับสนุนหรือข้อสงสัยใด ๆ คุณสามารถไปที่[Aspose ฟอรั่มการถ่ายภาพ](https://forum.aspose.com/).
