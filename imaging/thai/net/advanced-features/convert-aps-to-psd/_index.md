---
title: แปลง APS เป็น PSD ด้วย Aspose.Imaging สำหรับ .NET
linktitle: แปลง APS เป็น PSD ใน Aspose.Imaging สำหรับ .NET
second_title: Aspose.Imaging .NET Image Processing API
description: แปลง APS เป็น PSD ด้วย Aspose.Imaging สำหรับ .NET รักษาคุณสมบัติเวกเตอร์ระหว่างการแปลง
weight: 11
url: /th/net/advanced-features/convert-aps-to-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง APS เป็น PSD ด้วย Aspose.Imaging สำหรับ .NET

คุณต้องการแปลงไฟล์ APS เป็นรูปแบบ PSD ได้อย่างง่ายดายโดยยังคงรักษาคุณสมบัติเวกเตอร์ไว้หรือไม่? Aspose.Imaging สำหรับ .NET พร้อมแล้วเพื่อทำให้งานของคุณง่ายขึ้น ในคำแนะนำทีละขั้นตอนนี้ เราจะแสดงวิธีบรรลุการแปลงนี้ 

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกกระบวนการนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  Aspose.Imaging สำหรับ .NET Library: คุณต้องดาวน์โหลดและติดตั้งไลบรารี Aspose.Imaging สำหรับ .NET คุณสามารถรับได้จาก[หน้าดาวน์โหลด](https://releases.aspose.com/imaging/net/).

2. Your Document Directory: ตรวจสอบให้แน่ใจว่าคุณมีเส้นทางไปยังไดเร็กทอรีเอกสารของคุณพร้อม นี่คือตำแหน่งของไฟล์ APS

3. ความรู้พื้นฐานของ C#: ความคุ้นเคยกับภาษาการเขียนโปรแกรม C# เป็นสิ่งจำเป็นต่อการดำเนินการแปลง

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นเพื่อทำงานกับ Aspose.Imaging สำหรับ .NET ตรวจสอบให้แน่ใจว่าคุณได้เพิ่มการอ้างอิงไปยังไลบรารี Aspose.Imaging ในโปรเจ็กต์ของคุณ

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Vectorization;
```

## ขั้นตอนที่ 1: โหลดไฟล์ APS

เริ่มต้นด้วยการโหลดไฟล์ APS ที่คุณต้องการแปลงเป็น PSD คุณจะต้องระบุเส้นทางไปยังไดเร็กทอรีเอกสารซึ่งมีไฟล์ APS อยู่

```csharp
string dataDir = "Your Document Directory";
string inputFileName = dataDir + "SimpleShapes.cdr";

using (Image image = Image.Load(inputFileName))
{
    // รหัสของคุณอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการแปลง

ในขั้นตอนนี้ คุณจะต้องตั้งค่าตัวเลือกการแปลงสำหรับการส่งออกไฟล์ APS เป็นรูปแบบ PSD Aspose.Imaging มีตัวเลือกต่างๆ สำหรับการแปลงภาพเวกเตอร์

```csharp
PsdOptions imageOptions = new PsdOptions()
{
    VectorRasterizationOptions = new VectorRasterizationOptions(),
    VectorizationOptions = new PsdVectorizationOptions()
    {
        VectorDataCompositionMode = VectorDataCompositionMode.SeparateLayers
    }
};

imageOptions.VectorRasterizationOptions.PageWidth = image.Width;
imageOptions.VectorRasterizationOptions.PageHeight = image.Height;
```

## ขั้นตอนที่ 3: บันทึกไฟล์ PSD

ถึงเวลาบันทึกไฟล์ PSD ที่แปลงแล้วไปยังตำแหน่งที่คุณต้องการ

```csharp
image.Save(dataDir + "result.psd", imageOptions);
```

## ขั้นตอนที่ 4: ทำความสะอาด

หลังจากการแปลงเสร็จสมบูรณ์ คุณอาจต้องการลบไฟล์ PSD ชั่วคราวที่สร้างขึ้นระหว่างกระบวนการ

```csharp
File.Delete(dataDir + "result.psd");
```

## บทสรุป

การแปลงรูปแบบ APS เป็น PSD ด้วย Aspose.Imaging สำหรับ .NET นั้นตรงไปตรงมาและมีประสิทธิภาพ ไลบรารีอันทรงพลังนี้ช่วยให้คุณสามารถรักษาคุณสมบัติเวกเตอร์ในระหว่างการแปลง ทำให้เป็นเครื่องมือที่มีค่าสำหรับนักออกแบบกราฟิกและนักพัฒนา

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Imaging สำหรับ .NET เป็นไลบรารี่ฟรีหรือไม่

 A1: Aspose.Imaging สำหรับ .NET เป็นไลบรารีเชิงพาณิชย์ คุณสามารถสำรวจตัวเลือกใบอนุญาตได้ที่[หน้าซื้อ](https://purchase.aspose.com/buy).

### คำถามที่ 2: ฉันสามารถลองใช้ Aspose.Imaging สำหรับ .NET ก่อนที่จะซื้อได้หรือไม่

 A2: ได้ คุณสามารถขอรับ Aspose.Imaging สำหรับ .NET รุ่นทดลองใช้ฟรีได้จาก[หน้าทดลอง](https://releases.aspose.com/imaging/net/).

### คำถามที่ 3: รูปแบบภาพเวกเตอร์ใดบ้างที่รองรับการแปลงเป็น PSD

A3: Aspose.Imaging สำหรับ .NET รองรับการแปลงรูปแบบภาพเวกเตอร์ เช่น CDR, EMF, EPS, ODG, SVG และ WMF เป็นรูปแบบ PSD

### คำถามที่ 4: มีข้อจำกัดใด ๆ เกี่ยวกับความซับซ้อนของรูปร่างระหว่างการแปลงหรือไม่

A4: ในปัจจุบัน Aspose.Imaging รองรับการส่งออกรูปร่างที่ไม่ซับซ้อนมากนักโดยไม่ต้องใช้แปรงพื้นผิวหรือรูปร่างแบบเปิดที่มีเส้นขีด อย่างไรก็ตาม อาจมีการปรับปรุงให้ดีขึ้นในรุ่นต่อๆ ไป

### คำถามที่ 5: ฉันจะรับการสนับสนุนหรือถามคำถามที่เกี่ยวข้องกับ Aspose.Imaging สำหรับ .NET ได้ที่ไหน

 A5: หากคุณมีคำถามหรือต้องการความช่วยเหลือ คุณสามารถไปที่[Aspose ฟอรั่มการถ่ายภาพ](https://forum.aspose.com/)สำหรับความช่วยเหลือ.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
