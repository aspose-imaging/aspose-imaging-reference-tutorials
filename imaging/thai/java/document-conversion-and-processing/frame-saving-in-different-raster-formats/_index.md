---
date: 2025-12-20
description: เรียนรู้วิธีแปลงไฟล์ TIFF เป็น PNG และบันทึกรูปภาพเป็น PNG, BMP หรือ
  GIF ด้วย Aspose.Imaging สำหรับ Java คู่มือแบบขั้นตอนสำหรับการจัดการรูปภาพ
linktitle: Frame Saving in Different Raster Formats
second_title: Aspose.Imaging Java Image Processing API
title: วิธีแปลง TIFF เป็น PNG และบันทึกเฟรมในรูปแบบเรสเตอร์ต่าง ๆ
url: /th/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# แปลง TIFF เป็น PNG และบันทึกเฟรมในรูปแบบ Raster ต่าง ๆ

การทำงานกับไฟล์ TIFF แบบหลายหน้าเป็นสถานการณ์ทั่วไปในแอปพลิเคชันที่ต้องจัดการเอกสารจำนวนมาก หากคุณต้องการ **convert tiff to png** หรือดึงเฟรมแต่ละเฟรมออกมาและจัดเก็บในรูปแบบ raster อื่น ๆ Aspose.Imaging for Java ทำให้กระบวนการนี้ง่ายและมีประสิทธิภาพ ในบทเรียนนี้เราจะอธิบายขั้นตอนที่ต้องทำเพื่อโหลดไฟล์ TIFF, วนลูปผ่านเฟรมต่าง ๆ, และบันทึกแต่ละเฟรมเป็น PNG (คุณสามารถสลับเป็น BMP หรือ GIF ได้ในภายหลัง)

## คำตอบสั้น ๆ
- **“convert tiff to png” หมายถึงอะไร?** หมายถึงการดึงแต่ละหน้าของไฟล์ TIFF แล้วบันทึกออกเป็นภาพ raster แบบ PNG.  
- **ไลบรารีที่ทำหน้าที่นี้คืออะไร?** Aspose.Imaging for Java ให้การสนับสนุนเต็มรูปแบบสำหรับการดึงเฟรมจาก TIFF และการแปลงรูปแบบ raster.  
- **ต้องมีลิขสิทธิ์หรือไม่?** รุ่นทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีลิขสิทธิ์เต็มสำหรับการใช้งานในผลิตภัณฑ์.  
- **สามารถบันทึกเป็น BMP หรือ GIF แทน PNG ได้หรือไม่?** ได้—เพียงเปลี่ยน `PpngOptions` เป็น `BmpOptions` หรือ `GifOptions`.  
- **ต้องใช้ Java เวอร์ชันใด?** แนะนำให้ใช้ Java 8 หรือสูงกว่า.

## “convert tiff to png” คืออะไร?
การแปลง TIFF เป็น PNG เกี่ยวข้องกับการถอดรหัสไฟล์ TIFF แบบหลายหน้า, เข้าถึงแต่ละเฟรม, แล้วเข้ารหัสเฟรมนั้นเป็นรูปแบบ PNG ซึ่งเป็นรูปแบบที่ไม่มีการสูญเสียข้อมูล, เหมาะกับเว็บ, และได้รับการสนับสนุนอย่างกว้างขวาง.

## ทำไมต้องใช้ Aspose.Imaging for Java?
- **รองรับรูปแบบหลากหลาย** – รองรับ TIFF, PNG, JPEG, BMP, GIF, และรูปแบบอื่น ๆ อีกมาก.  
- **ไม่มีการพึ่งพาเนทีฟ** – เป็น Java แท้ ๆ, ผสานรวมง่ายกับโครงการ JVM ใดก็ได้.  
- **ประสิทธิภาพสูง** – ปรับแต่งสำหรับภาพขนาดใหญ่และเอกสารหลายหน้า.  
- **API ง่าย** – ต้องเขียนโค้ดเพียงเล็กน้อยเพื่อทำการแปลงที่ซับซ้อน.

## ข้อกำหนดเบื้องต้น

1. **สภาพแวดล้อมการพัฒนา Java** – ตรวจสอบให้แน่ใจว่าได้ติดตั้ง JDK แล้ว ดาวน์โหลดได้จาก [Oracle website](https://www.oracle.com/java/technologies/javase-downloads) หากยังไม่มี.  
2. **Aspose.Imaging for Java Library** – เข้าถึงเอกสารอ้างอิง API ที่ [documentation](https://reference.aspose.com/imaging/java/). ดาวน์โหลดไลบรารีจาก [download page](https://releases.aspose.com/imaging/java/). มีรุ่นทดลองฟรีให้ใช้ [here](https://releases.aspose.com/), และสามารถซื้อไลเซนส์เต็มได้ [here](https://purchase.aspose.com/buy).  
3. **ตัวอย่างภาพ TIFF** – เตรียมไฟล์ TIFF แบบหลายหน้าที่พร้อมสำหรับการประมวลผล.

เมื่อข้อกำหนดเบื้องต้นพร้อมแล้ว, ไปที่ขั้นตอนโค้ดกันเลย.

## วิธีแปลง TIFF เป็น PNG ด้วย Aspose.Imaging for Java

### นำเข้าแพคเกจ
เริ่มต้นด้วยการนำเข้าคลาสของ Aspose.Imaging ที่จำเป็น.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

### ขั้นตอนที่ 1: โหลดภาพ TIFF
กำหนดไดเรกทอรีข้อมูลและโหลดไฟล์ TIFF ต้นฉบับ.

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

### ขั้นตอนที่ 2: บันทึกเฟรมในรูปแบบ Raster ต่าง ๆ
วนลูปแต่ละเฟรมและ **save image as png**. หากต้องการ **convert tiff to bmp** หรือทำ **tiff to gif conversion**, เพียงเปลี่ยน `PngOptions` เป็น `BmpOptions` หรือ `GifOptions`.

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **เคล็ดลับ:** ควรใช้บล็อก `try‑with‑resources` ตามตัวอย่างเพื่อให้แน่ใจว่าไฟล์ TIFF ถูกปล่อยทรัพยากรอย่างถูกต้องหลังการประมวลผล.

## กรณีการใช้งานทั่วไป
- **การจัดเก็บเอกสาร:** แปลงเอกสารสแกนแบบ TIFF เป็น PNG เพื่อแสดงตัวอย่างบนเว็บ.  
- **การสร้างภาพย่อ:** ดึงเฟรมแรกของ TIFF แล้วบันทึกเป็นภาพย่อ PNG ขนาดเล็ก.  
- **การย้ายรูปแบบ:** ย้ายทรัพยากร TIFF เก่าไปยังรูปแบบสมัยใหม่เช่น BMP หรือ GIF เพื่อความเข้ากันได้กับระบบที่เก่า.

## การแก้ไขปัญหาและเคล็ดลับ
- **เฟรมหาย:** ตรวจสอบว่า TIFF ต้นฉบับมีหลายหน้าจริงหรือไม่; ใช้ `multiImage.getFrames().size()` เพื่อตรวจสอบ.  
- **ข้อผิดพลาด Out‑of‑memory:** ประมวลผล TIFF ขนาดใหญ่แบบหน้า‑ต่อหน้า ตามที่แสดงแทนการโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ.  
- **การควบคุมคุณภาพ:** PNG ไม่มีการสูญเสียข้อมูล; หากต้องการไฟล์ขนาดเล็กกว่า, พิจารณาใช้ตัวเลือก JPEG พร้อมการตั้งค่าคุณภาพ.

## คำถามที่พบบ่อย

**Q1: รูปแบบ raster ที่รองรับสำหรับการบันทึกเฟรมใน Aspose.Imaging for Java มีอะไรบ้าง?**  
A1: Aspose.Imaging for Java รองรับรูปแบบ raster หลากหลาย รวมถึง PNG, JPEG, BMP, GIF, และอื่น ๆ อีกมาก คุณสามารถเลือกรูปแบบที่เหมาะกับความต้องการของแอปพลิเคชันของคุณได้.

**Q2: สามารถทำการประมวลผลภาพอื่น ๆ ด้วย Aspose.Imaging for Java ได้หรือไม่?**  
A2: ได้, Aspose.Imaging for Java มีชุดคุณสมบัติครบถ้วนสำหรับการจัดการภาพ เช่น การปรับขนาด, การครอป, และการใช้ฟิลเตอร์หรือเอฟเฟกต์ต่าง ๆ เป็นเครื่องมืออเนกประสงค์สำหรับความต้องการการประมวลผลภาพทั้งหมดของคุณ.

**Q3: จะขอรับลิขสิทธิ์เต็มสำหรับ Aspose.Imaging for Java ได้อย่างไร?**  
A: เพื่อซื้อไลเซนส์เต็มสำหรับ Aspose.Imaging for Java, เยี่ยมชม [purchase page](https://purchase.aspose.com/buy). คุณจะพบตัวเลือกการให้ลิขสิทธิ์ที่หลากหลายเพื่อให้เหมาะกับโครงการของคุณ.

**Q4: มีรุ่นทดลองฟรีสำหรับ Aspose.Imaging for Java หรือไม่?**  
A: มี, คุณสามารถเข้าถึงรุ่นทดลองฟรีของ Aspose.Imaging for Java ได้จาก [releases page](https://releases.aspose.com/). รุ่นทดลองนี้ช่วยให้คุณสำรวจความสามารถของไลบรารีก่อนตัดสินใจซื้อ.

**Q5: จะหาการสนับสนุนหรือขอความช่วยเหลือเกี่ยวกับ Aspose.Imaging for Java ได้จากที่ไหน?**  
A: สำหรับคำถาม, ปัญหา, หรือการขอความช่วยเหลือเกี่ยวกับ Aspose.Imaging for Java, คุณสามารถเยี่ยมชม [Aspose Imaging forum](https://forum.aspose.com/). ชุมชนและทีมสนับสนุนพร้อมให้ความช่วยเหลือคุณ.

---

**อัปเดตล่าสุด:** 2025-12-20  
**ทดสอบด้วย:** Aspose.Imaging for Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}