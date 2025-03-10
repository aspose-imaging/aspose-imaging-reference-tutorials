---
title: แปลง DICOM เป็น PNG ด้วย Aspose.Imaging สำหรับ .NET
linktitle: แปลง DICOM เป็น PNG ใน Aspose.Imaging สำหรับ .NET
second_title: Aspose.Imaging .NET Image Processing API
description: แปลง DICOM เป็น PNG ได้อย่างง่ายดายด้วย Aspose.Imaging สำหรับ .NET ปรับปรุงการแบ่งปันภาพทางการแพทย์
weight: 21
url: /th/net/dicom-image-processing/convert-dicom-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DICOM เป็น PNG ด้วย Aspose.Imaging สำหรับ .NET

ในโลกของการถ่ายภาพทางการแพทย์ DICOM (การถ่ายภาพดิจิทัลและการสื่อสารทางการแพทย์) เป็นรูปแบบที่ใช้กันอย่างแพร่หลายในการจัดเก็บและแบ่งปันภาพทางการแพทย์ อย่างไรก็ตาม เมื่อคุณต้องการแปลงไฟล์ DICOM เป็นรูปแบบรูปภาพทั่วไป เช่น PNG Aspose.Imaging สำหรับ .NET จะช่วยคุณได้ บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการแปลงไฟล์ DICOM เป็น PNG โดยใช้ Aspose.Imaging สำหรับ .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกกระบวนการแปลง คุณจะต้องมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  Aspose.Imaging สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารีนี้แล้ว คุณสามารถรับได้จาก[หน้าดาวน์โหลด](https://releases.aspose.com/imaging/net/).

2. ไฟล์ DICOM: เตรียมไฟล์ DICOM ที่คุณต้องการแปลงเป็น PNG หากคุณไม่มี คุณสามารถค้นหาไฟล์ DICOM ตัวอย่างบนอินเทอร์เน็ต หรือขอได้จากแผนกภาพทางการแพทย์ของคุณ

ด้วยข้อกำหนดเบื้องต้นเหล่านี้ คุณก็พร้อมที่จะเริ่มแปลง DICOM เป็น PNG โดยใช้ Aspose.Imaging สำหรับ .NET แล้ว

## ขั้นตอนที่ 1: นำเข้าเนมสเปซ

ขั้นแรก คุณต้องนำเข้าเนมสเปซที่จำเป็นสำหรับการทำงานกับ Aspose.Imaging ในโค้ด C# ของคุณ ให้รวมเนมสเปซต่อไปนี้:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
```

## กระบวนการแปลง

ตอนนี้ เรามาแบ่งกระบวนการแปลงออกเป็นหลายขั้นตอนกัน

### ขั้นตอนที่ 2.1: โหลดไฟล์ DICOM

```csharp
string dataDir = "Your Document Directory";
string inputFile = Path.Combine(dataDir, "MultiframePage1.dicom");

using (Aspose.Imaging.FileFormats.Dicom.DicomImage image = (Aspose.Imaging.FileFormats.Dicom.DicomImage)Image.Load(inputFile))
{
    // รหัสสำหรับการแปลงของคุณจะอยู่ที่นี่
}
```

ในขั้นตอนนี้ คุณจะต้องกำหนดเส้นทางไปยังไฟล์ DICOM ของคุณ และใช้ Aspose.Imaging เพื่อโหลด

### ขั้นตอนที่ 2.2: กำหนดค่าตัวเลือก PNG

```csharp
PngOptions options = new PngOptions();
```

 ที่นี่ คุณสร้างอินสแตนซ์ของ`PngOptions`ซึ่งช่วยให้คุณระบุการตั้งค่าสำหรับรูปภาพ PNG ที่คุณจะสร้าง

### ขั้นตอนที่ 2.3: บันทึกเป็น PNG

```csharp
image.Save(dataDir + @"MultiframePage1.png", options);
```

 นี่คือจุดที่การแปลงเกิดขึ้นจริง คุณใช้`Save` วิธีการแปลงอิมเมจ DICOM ที่โหลดไปเป็นอิมเมจ PNG พร้อมตัวเลือกที่ระบุ

### ขั้นตอนที่ 2.4: การล้างข้อมูล (ไม่บังคับ)

```csharp
File.Delete(dataDir + "MultiframePage1.png");
```

หากคุณต้องการล้างไฟล์ระดับกลาง คุณสามารถลบไฟล์ PNG ที่สร้างขึ้นระหว่างกระบวนการแปลงได้

## บทสรุป

การแปลง DICOM เป็น PNG เป็นความต้องการทั่วไปในวงการแพทย์ และ Aspose.Imaging สำหรับ .NET ช่วยให้งานนี้ง่ายขึ้น ด้วยโค้ดเพียงไม่กี่บรรทัด คุณสามารถแปลงไฟล์ DICOM ของคุณเป็นรูปแบบ PNG ทำให้เข้าถึงได้ง่ายขึ้นและแชร์ได้ง่ายขึ้น Aspose.Imaging สำหรับ .NET นำเสนอโซลูชันที่ทรงพลังและยืดหยุ่นสำหรับการจัดการรูปแบบรูปภาพต่างๆ ในแอปพลิเคชัน .NET ของคุณ

 หากคุณพบปัญหาใดๆ หรือมีคำถามเกี่ยวกับ Aspose.Imaging สำหรับ .NET คุณสามารถขอความช่วยเหลือได้ที่[Aspose ฟอรั่มการถ่ายภาพ](https://forum.aspose.com/).

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Imaging สำหรับ .NET ใช้งานได้ฟรีหรือไม่

A1: Aspose.Imaging สำหรับ .NET เป็นไลบรารีเชิงพาณิชย์ และจำเป็นต้องมีใบอนุญาตที่ถูกต้องสำหรับการใช้งาน คุณสามารถรับก[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) เพื่อวัตถุประสงค์ในการประเมินผล สำหรับข้อมูลเพิ่มเติมเกี่ยวกับราคาและใบอนุญาต โปรดไปที่[หน้าซื้อ](https://purchase.aspose.com/buy).

### คำถามที่ 2: ฉันสามารถแปลงไฟล์ DICOM หลายไฟล์ในโหมดแบตช์ได้หรือไม่

A2: ใช่ Aspose.Imaging สำหรับ .NET รองรับการประมวลผลแบบแบตช์ คุณสามารถวนซ้ำไฟล์ DICOM หลายไฟล์แล้วแปลงเป็น PNG ได้ในครั้งเดียว

### คำถามที่ 3: มีข้อจำกัดใดๆ ในกระบวนการแปลง DICOM เป็น PNG หรือไม่

A3: ข้อจำกัด (ถ้ามี) จะขึ้นอยู่กับไฟล์ DICOM และตัวเลือก PNG ที่คุณเลือก Aspose.Imaging สำหรับ .NET ให้ความยืดหยุ่นในการจัดการสถานการณ์ต่างๆ แต่ข้อมูลเฉพาะอาจแตกต่างกันไป

### คำถามที่ 4: ฉันจะจัดการกับข้อผิดพลาดระหว่างกระบวนการแปลงได้อย่างไร

 A4: คุณสามารถใช้การจัดการข้อผิดพลาดในรหัส C# ของคุณเพื่อตรวจจับและจัดการข้อยกเว้น อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/imaging/net/) สำหรับแนวทางการจัดการข้อผิดพลาดโดยละเอียด

### คำถามที่ 5: ฉันสามารถแปลงไฟล์ DICOM เป็นรูปแบบรูปภาพอื่นนอกเหนือจาก PNG ได้หรือไม่

A5: ใช่ Aspose.Imaging สำหรับ .NET รองรับรูปแบบรูปภาพที่หลากหลาย คุณสามารถแปลงไฟล์ DICOM เป็นรูปแบบต่างๆ เช่น JPEG, BMP, TIFF และอื่นๆ ได้ ขึ้นอยู่กับความต้องการของคุณ
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
