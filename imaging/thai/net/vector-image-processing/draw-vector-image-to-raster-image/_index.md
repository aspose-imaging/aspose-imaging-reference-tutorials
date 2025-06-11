---
"description": "เรียนรู้วิธีการแปลงภาพเวกเตอร์เป็นภาพแรสเตอร์ใน .NET โดยใช้ Aspose.Imaging คำแนะนำทีละขั้นตอนสำหรับการประมวลผลภาพที่มีประสิทธิภาพ"
"linktitle": "วาดภาพเวกเตอร์เป็นภาพแรสเตอร์ใน Aspose.Imaging สำหรับ .NET"
"second_title": "API การประมวลผลภาพ Aspose.Imaging .NET"
"title": "วาดภาพเวกเตอร์เป็นภาพแรสเตอร์ใน Aspose.Imaging สำหรับ .NET"
"url": "/th/net/vector-image-processing/draw-vector-image-to-raster-image/"
"weight": 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# วาดภาพเวกเตอร์เป็นภาพแรสเตอร์ใน Aspose.Imaging สำหรับ .NET


คุณกำลังมองหาวิธีแปลงภาพเวกเตอร์เป็นภาพแรสเตอร์อย่างง่ายดายในแอปพลิเคชัน .NET ของคุณหรือไม่ Aspose.Imaging สำหรับ .NET มอบโซลูชันที่มีประสิทธิภาพสำหรับงานนี้ ในคู่มือทีละขั้นตอนนี้ เราจะแนะนำคุณเกี่ยวกับกระบวนการวาดภาพเวกเตอร์เป็นภาพแรสเตอร์โดยใช้ Aspose.Imaging สำหรับ .NET 

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเริ่มลงลึกในบทช่วยสอนนี้ ให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

### 1. Aspose.Imaging สำหรับ .NET

คุณควรติดตั้ง Aspose.Imaging สำหรับ .NET หากคุณยังไม่มี คุณสามารถดาวน์โหลดได้จากเว็บไซต์ที่ [ดาวน์โหลด Aspose.Imaging สำหรับ .NET](https://releases-aspose.com/imaging/net/).

### 2. สภาพแวดล้อมการพัฒนา .NET

ตรวจสอบว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา .NET บนคอมพิวเตอร์ของคุณแล้ว คุณสามารถใช้ Visual Studio หรือเครื่องมือพัฒนา .NET อื่นๆ ได้

ตอนนี้เรามาแบ่งขั้นตอนการวาดภาพเวกเตอร์เป็นภาพแรสเตอร์เป็นขั้นตอนง่ายๆ ที่ทำตามได้ง่ายกัน:

## ขั้นตอนที่ 1: เริ่มต้นโครงการของคุณ

เริ่มต้นด้วยการสร้างโปรเจ็กต์ .NET ใหม่ในสภาพแวดล้อมการพัฒนาของคุณ ตรวจสอบให้แน่ใจว่าคุณได้รวม Aspose.Imaging สำหรับ .NET ไว้ในโปรเจ็กต์ของคุณแล้ว

## ขั้นตอนที่ 2: โหลดภาพเวกเตอร์

ในขั้นตอนนี้ เราจะโหลดภาพเวกเตอร์ (ในรูปแบบ SVG) ที่คุณต้องการแปลงให้เป็นภาพแรสเตอร์

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // -
}
```

## ขั้นตอนที่ 3: แรสเตอร์ภาพเวกเตอร์

ตอนนี้เราต้องแปลงภาพ SVG เป็นรูปแบบ PNG ซึ่งเป็นขั้นตอนการแปลงจากเวกเตอร์เป็นแรสเตอร์

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## ขั้นตอนที่ 4: โหลดภาพแรสเตอร์

หลังจากการแรสเตอร์แล้ว โหลดภาพ PNG จากสตรีมเพื่อวาดเพิ่มเติม

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // -
}
```

## ขั้นตอนที่ 5: วาดภาพแรสเตอร์

ตอนนี้เราสามารถวาดภาพแรสเตอร์บนภาพ SVG ที่มีอยู่ได้แล้ว

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

สุดท้าย ให้บันทึกภาพผลลัพธ์ ตอนนี้คุณจะมีภาพแรสเตอร์ที่รวมภาพเวกเตอร์ของคุณไว้แล้ว

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้สาธิตวิธีการแปลงรูปภาพเวกเตอร์เป็นรูปภาพแรสเตอร์โดยใช้ Aspose.Imaging สำหรับ .NET ด้วยขั้นตอนง่ายๆ เหล่านี้ คุณสามารถผสานฟังก์ชันนี้เข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างง่ายดาย

### คำถามที่พบบ่อย

### Aspose.Imaging สำหรับ .NET คืออะไร?
Aspose.Imaging สำหรับ .NET เป็นไลบรารี .NET ที่ให้คุณลักษณะการประมวลผลรูปภาพอันทรงพลัง รวมถึงความสามารถในการทำงานกับรูปแบบรูปภาพต่างๆ การแปลงรูปภาพ และดำเนินการจัดการรูปภาพขั้นสูง

### ฉันสามารถค้นหาเอกสารสำหรับ Aspose.Imaging สำหรับ .NET ได้ที่ไหน
คุณสามารถค้นหาเอกสารสำหรับ Aspose.Imaging สำหรับ .NET ได้ [ที่นี่](https://reference-aspose.com/imaging/net/).

### มีเวอร์ชันทดลองใช้งานฟรีหรือไม่?
ใช่ คุณสามารถเข้าถึงรุ่นทดลองใช้งานฟรีของ Aspose.Imaging สำหรับ .NET ได้ [ที่นี่](https://releases-aspose.com/).

### ฉันจะได้รับใบอนุญาตชั่วคราวสำหรับ Aspose.Imaging สำหรับ .NET ได้อย่างไร
หากคุณต้องการใบอนุญาตชั่วคราว คุณสามารถขอรับได้ [ที่นี่](https://purchase-aspose.com/temporary-license/).

### ฉันจะได้รับการสนับสนุนสำหรับ Aspose.Imaging สำหรับ .NET ได้จากที่ไหน
สำหรับการสนับสนุนหรือข้อสงสัยใด ๆ คุณสามารถเยี่ยมชม [ฟอรั่ม Aspose.Imaging](https://forum-aspose.com/).


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}