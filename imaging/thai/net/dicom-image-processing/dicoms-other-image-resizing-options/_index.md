---
title: ตัวเลือกการปรับขนาดรูปภาพอื่น ๆ ของ DICOM ใน Aspose.Imaging สำหรับ .NET
linktitle: ตัวเลือกการปรับขนาดรูปภาพอื่น ๆ ของ DICOM ใน Aspose.Imaging สำหรับ .NET
second_title: Aspose.Imaging .NET Image Processing API
description: เรียนรู้วิธีปรับขนาดอิมเมจ DICOM โดยใช้ Aspose.Imaging สำหรับ .NET คำแนะนำทีละขั้นตอนสำหรับการปรับแต่งภาพทางการแพทย์อย่างมีประสิทธิภาพ
weight: 20
url: /th/net/dicom-image-processing/dicoms-other-image-resizing-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตัวเลือกการปรับขนาดรูปภาพอื่น ๆ ของ DICOM ใน Aspose.Imaging สำหรับ .NET

คุณต้องการทำงานกับอิมเมจ DICOM (Digital Imaging and Communications in Medicine) ในแอปพลิเคชัน .NET ของคุณหรือไม่? Aspose.Imaging สำหรับ .NET มอบชุดเครื่องมืออันทรงพลังเพื่อจัดการอิมเมจ DICOM ได้อย่างมีประสิทธิภาพ ในบทช่วยสอนนี้ เราจะเจาะลึก "ตัวเลือกการปรับขนาดรูปภาพอื่นๆ ของ DICOM" โดยใช้ Aspose.Imaging สำหรับ .NET เราจะครอบคลุมข้อกำหนดเบื้องต้น นำเข้าเนมสเปซ และให้คำแนะนำทีละขั้นตอนเพื่อช่วยให้คุณเข้าใจและใช้การปรับขนาดรูปภาพ DICOM ได้อย่างมีประสิทธิภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. ติดตั้ง Aspose.Imaging สำหรับ .NET
หากต้องการทำงานกับอิมเมจ DICOM โดยใช้ Aspose.Imaging สำหรับ .NET คุณต้องติดตั้งไลบรารี คุณสามารถดาวน์โหลดได้จากเว็บไซต์

[ดาวน์โหลด Aspose.Imaging สำหรับ .NET](https://releases.aspose.com/imaging/net/)

2. ตั้งค่าสภาพแวดล้อมการพัฒนา
ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา .NET รวมถึง Visual Studio หรือ IDE อื่นๆ ที่เข้ากันได้

3. รูปภาพ DICOM
คุณควรมีไฟล์รูปภาพ DICOM (เช่น "file.dcm") ที่คุณต้องการปรับขนาดโดยใช้ Aspose.Imaging สำหรับ .NET

## นำเข้าเนมสเปซ

ในโค้ด C# ของคุณ คุณจะต้องนำเข้าเนมสเปซที่จำเป็นเพื่อใช้ Aspose.Imaging ต่อไปนี้เป็นวิธีดำเนินการ:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
```

ตอนนี้ เรามาแบ่งกระบวนการปรับขนาดรูปภาพออกเป็นหลายขั้นตอนกัน

## ขั้นตอนที่ 1: โหลดอิมเมจ DICOM
ในการเริ่มต้น คุณต้องโหลดอิมเมจ DICOM จากระบบไฟล์ของคุณ

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
{
    // รหัสของคุณที่นี่
}
```

## ขั้นตอนที่ 2: ปรับขนาดตามความสูงตามสัดส่วน
คุณสามารถปรับขนาดรูปภาพ DICOM ตามสัดส่วนได้โดยการระบุความสูงเป็นพิกเซลและประเภทการปรับขนาด ในตัวอย่างนี้ เราใช้ "AdaptiveResample" เป็นประเภทการปรับขนาด

```csharp
image.ResizeHeightProportionally(100, ResizeType.AdaptiveResample);
```

## ขั้นตอนที่ 3: บันทึกภาพที่ปรับขนาดแล้ว
หลังจากปรับขนาดภาพแล้ว คุณสามารถบันทึกเป็นรูปแบบที่ต้องการได้ ที่นี่เราบันทึกเป็นภาพ BMP

```csharp
image.Save(dataDir + "DICOMSOtherImageResizingOptions_out.bmp", new BmpOptions());
```

## ขั้นตอนที่ 4: ปรับขนาดตามความกว้างตามสัดส่วน
คุณยังสามารถปรับขนาดรูปภาพ DICOM ตามสัดส่วนโดยระบุความกว้างเป็นพิกเซลและประเภทการปรับขนาด

```csharp
image1.ResizeWidthProportionally(150, ResizeType.AdaptiveResample);
```

## ขั้นตอนที่ 5: บันทึกภาพที่ปรับขนาดแล้ว
บันทึกรูปภาพที่ปรับขนาดแล้วเป็นรูปภาพ BMP เช่นเดียวกับในขั้นตอนก่อนหน้า

```csharp
image1.Save(dataDir + "DICOMSOtherImageResizingOptions1_out.bmp", new BmpOptions());
```

ยินดีด้วย! คุณปรับขนาดอิมเมจ DICOM สำเร็จแล้วโดยใช้ Aspose.Imaging สำหรับ .NET ไลบรารีนี้มีตัวเลือกมากมายสำหรับการจัดการภาพ DICOM ทำให้เป็นเครื่องมือที่มีคุณค่าสำหรับแอปพลิเคชันด้านการดูแลสุขภาพและการถ่ายภาพทางการแพทย์

## บทสรุป

ในบทช่วยสอนนี้ เราได้ศึกษา "ตัวเลือกการปรับขนาดรูปภาพอื่นๆ ของ DICOM" โดยใช้ Aspose.Imaging สำหรับ .NET เราครอบคลุมข้อกำหนดเบื้องต้น เนมสเปซที่นำเข้า และให้คำแนะนำทีละขั้นตอนสำหรับการปรับขนาดอิมเมจ DICOM Aspose.Imaging สำหรับ .NET ทำให้กระบวนการทำงานกับภาพทางการแพทย์ง่ายขึ้น โดยนำเสนอคุณสมบัติที่หลากหลายสำหรับการใช้งานด้านการดูแลสุขภาพ

มีคำถามเพิ่มเติมหรือต้องการความช่วยเหลือเกี่ยวกับ Aspose.Imaging สำหรับ .NET หรือไม่ ตรวจสอบเอกสารหรือเยี่ยมชมฟอรั่มชุมชน Aspose เพื่อรับการสนับสนุน:

- [Aspose.Imaging สำหรับเอกสาร .NET](https://reference.aspose.com/imaging/net/)
- [Aspose.Imaging สำหรับการสนับสนุน .NET](https://forum.aspose.com/)

## คำถามที่พบบ่อย

### คำถามที่ 1: DICOM คืออะไร

คำตอบ 1: DICOM ย่อมาจาก Digital Imaging and Communications in Medicine เป็นมาตรฐานสำหรับการส่ง จัดเก็บ และแบ่งปันภาพทางการแพทย์ เช่น ภาพเอ็กซ์เรย์ MRI และซีทีสแกน ในรูปแบบดิจิทัล

### คำถามที่ 2: ฉันสามารถใช้ Aspose.Imaging สำหรับ .NET ได้ฟรีหรือไม่

A2: Aspose.Imaging สำหรับ .NET เป็นไลบรารีเชิงพาณิชย์ คุณสามารถดาวน์โหลดเวอร์ชันทดลองใช้ฟรีเพื่อประเมินคุณลักษณะต่างๆ ได้ แต่จำเป็นต้องมีใบอนุญาตสำหรับการใช้งานเต็มรูปแบบ

### คำถามที่ 3: Aspose.Imaging สำหรับ .NET มีตัวเลือกการจัดการรูปภาพอื่นๆ ใดบ้าง

A3: Aspose.Imaging สำหรับ .NET มีตัวเลือกการประมวลผลภาพที่หลากหลาย รวมถึงการแปลงรูปแบบ การปรับปรุงรูปภาพ และการวาดภาพบนรูปภาพ คุณสามารถสำรวจคุณสมบัติทั้งหมดได้ในเอกสารประกอบ

### คำถามที่ 4: Aspose.Imaging สำหรับ .NET เหมาะสำหรับการใช้งานด้านการดูแลสุขภาพหรือไม่

ตอบ 4: ใช่ Aspose.Imaging สำหรับ .NET มักใช้ในแอปพลิเคชันด้านการดูแลสุขภาพเพื่อจัดการอิมเมจ DICOM ทำให้เป็นเครื่องมือที่มีคุณค่าสำหรับการพัฒนาซอฟต์แวร์เกี่ยวกับอิมเมจทางการแพทย์

### คำถามที่ 5: ฉันสามารถขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Imaging สำหรับ .NET ได้หรือไม่
ว
 A5: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวเพื่อวัตถุประสงค์ในการทดสอบและประเมินผลได้ เยี่ยม[หน้าใบอนุญาตชั่วคราวของ Aspose](https://purchase.aspose.com/temporary-license/) สำหรับข้อมูลเพิ่มเติม.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
