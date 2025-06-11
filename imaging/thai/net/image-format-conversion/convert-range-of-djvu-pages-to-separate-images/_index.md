---
"description": "ค้นพบวิธีการแปลงหน้า DJVU เป็นรูปภาพแยกด้วย Aspose.Imaging สำหรับ .NET มีคำแนะนำทีละขั้นตอน ตัวอย่างโค้ด และคำถามที่พบบ่อยให้"
"linktitle": "แปลงช่วงของหน้า DJVU ให้เป็นรูปภาพแยกใน Aspose.Imaging สำหรับ .NET"
"second_title": "API การประมวลผลภาพ Aspose.Imaging .NET"
"title": "แปลงช่วงของหน้า DJVU ให้เป็นรูปภาพแยกใน Aspose.Imaging สำหรับ .NET"
"url": "/th/net/image-format-conversion/convert-range-of-djvu-pages-to-separate-images/"
"weight": 19
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# แปลงช่วงของหน้า DJVU ให้เป็นรูปภาพแยกใน Aspose.Imaging สำหรับ .NET

หากคุณกำลังมองหาไลบรารี .NET ที่ทรงพลังสำหรับจัดการงานการแปลงและจัดการรูปภาพ Aspose.Imaging สำหรับ .NET ถือเป็นตัวเลือกที่สมบูรณ์แบบ ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการแปลงเพจ DJVU ต่างๆ ให้เป็นรูปภาพแยกกันโดยใช้ Aspose.Imaging คุณจะพบคำแนะนำทีละขั้นตอนและตัวอย่างโค้ดเพื่อช่วยให้คุณบรรลุภารกิจนี้ได้

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเริ่มกระบวนการแปลง โปรดตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

1. Aspose.Imaging สำหรับไลบรารี .NET

คุณจะต้องติดตั้ง Aspose.Imaging สำหรับ .NET หากคุณยังไม่ได้ติดตั้ง คุณสามารถดาวน์โหลดได้จาก [หน้า Aspose.Imaging สำหรับ .NET](https://releases-aspose.com/imaging/net/).

2. สภาพแวดล้อมการพัฒนา

หากต้องการปฏิบัติตาม คุณควรมีการตั้งค่าสภาพแวดล้อมการพัฒนาด้วย Visual Studio หรือ .NET IDE อื่นๆ

## การนำเข้าเนมสเปซที่จำเป็น

ขั้นแรก คุณต้องรวมเนมสเปซที่จำเป็นในโค้ดของคุณเพื่อทำงานกับ Aspose.Imaging คุณสามารถทำได้ดังนี้:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Djvu;
using Aspose.Imaging.FileFormats.Djvu.Options;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.RasterImage;
```

## การแปลงหน้า DJVU

ตอนนี้ มาแบ่งขั้นตอนการแปลงหน้า DJVU หลายๆ หน้าเป็นรูปภาพแยกกันโดยใช้ Aspose.Imaging สำหรับ .NET ออกเป็นขั้นตอนที่ทำตามได้ง่าย ๆ ทีละขั้นตอน

### ขั้นตอนที่ 1: โหลดภาพ DJVU

ในการเริ่มต้น คุณควรโหลดไฟล์ภาพ DJVU ที่คุณต้องการแปลง แทนที่ `"Your Document Directory"` พร้อมเส้นทางจริงไปยังไฟล์ DJVU ของคุณ

```csharp
string dataDir = "Your Document Directory";

// โหลดภาพ DjVu
using (DjvuImage image = (DjvuImage)Image.Load(dataDir + "Sample.djvu"))
{
    // โค้ดของคุณสำหรับการประมวลผลเพิ่มเติมจะอยู่ที่นี่
}
```

### ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการส่งออก

ตอนนี้สร้างอินสแตนซ์ของ `BmpOptions` และกำหนดค่าตัวเลือกที่ต้องการสำหรับภาพผลลัพธ์ ในตัวอย่างนี้ เราตั้งค่า `BitsPerPixel` ถึง 32.

```csharp
BmpOptions exportOptions = new BmpOptions();
exportOptions.BitsPerPixel = 32;
```

### ขั้นตอนที่ 3: กำหนดช่วงของหน้า

เพื่อระบุช่วงของหน้าที่คุณต้องการส่งออก ให้สร้างอินสแตนซ์ของ `IntRange` และเริ่มต้นด้วยช่วงหน้า ในกรณีนี้ เราจะส่งออกหน้า 0 ถึง 2

```csharp
IntRange range = new IntRange(0, 2);
```

### ขั้นตอนที่ 4: วนซ้ำผ่านหน้าต่างๆ

ตอนนี้ ให้วนซ้ำหน้าต่างๆ ภายในช่วงที่ระบุ และบันทึกแต่ละหน้าเป็นไฟล์ BMP แยกกัน ไฟล์ DJVU ไม่รองรับการแบ่งเลเยอร์ ดังนั้นเราจึงบันทึกแต่ละหน้าทีละหน้า

```csharp
int counter = 0;
foreach (var i in range.Range)
{
    exportOptions.MultiPageOptions = new DjvuMultiPageOptions(range.GetArrayOneItemFromIndex(counter));
    image.Save(dataDir + string.Format("{0}_out.bmp", counter++), exportOptions);
}
```

และเสร็จเรียบร้อย! คุณได้แปลงหน้า DJVU หลายๆ หน้าเป็นรูปภาพแยกกันสำเร็จแล้วโดยใช้ Aspose.Imaging สำหรับ .NET

## บทสรุป

Aspose.Imaging สำหรับ .NET ช่วยลดความซับซ้อนของงานแปลงรูปภาพ ทำให้เป็นตัวเลือกที่ยอดเยี่ยมสำหรับนักพัฒนา ในบทช่วยสอนนี้ เราจะแนะนำคุณเกี่ยวกับขั้นตอนการแปลงหน้า DJVU เป็นรูปภาพแยกทีละขั้นตอน เมื่อมีโค้ดและไลบรารีที่เหมาะสม การแปลงรูปภาพจะกลายเป็นเรื่องง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Imaging สำหรับ .NET เป็นไลบรารีฟรีหรือไม่

A1: ไม่ใช่ มันเป็นห้องสมุดเชิงพาณิชย์ แต่คุณสามารถดาวน์โหลดได้ [ทดลองใช้งานฟรี](https://releases.aspose.com/) เพื่อทดสอบศักยภาพของมัน

### คำถามที่ 2: ฉันสามารถซื้อใบอนุญาตชั่วคราวสำหรับ Aspose.Imaging สำหรับ .NET ได้หรือไม่

A2: ใช่ คุณสามารถขอใบอนุญาตชั่วคราวได้จาก [หน้าการซื้อ](https://purchase-aspose.com/temporary-license/).

### คำถามที่ 3: ฉันสามารถหาเอกสารสำหรับ Aspose.Imaging สำหรับ .NET ได้จากที่ใด

A3: คุณสามารถสำรวจเอกสารที่ครอบคลุมได้ [ที่นี่](https://reference-aspose.com/imaging/net/).

### คำถามที่ 4: Aspose.Imaging สำหรับ .NET รองรับรูปแบบภาพอะไรบ้าง

A4: Aspose.Imaging สำหรับ .NET รองรับรูปแบบรูปภาพหลากหลาย เช่น BMP, JPEG, PNG, TIFF และอื่นๆ

### คำถามที่ 5: ฉันจะได้รับการสนับสนุนและความช่วยเหลือหากประสบปัญหาได้หรือไม่

A5: ใช่ คุณสามารถขอความช่วยเหลือและเชื่อมต่อกับชุมชนได้ที่ [ฟอรั่ม Aspose.Imaging](https://forum-aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}