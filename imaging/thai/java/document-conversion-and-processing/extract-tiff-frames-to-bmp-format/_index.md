---
date: 2025-12-19
description: เรียนรู้วิธีแปลงไฟล์ TIFF เป็น BMP ใน Java ด้วย Aspose.Imaging บทเรียนการประมวลผลภาพด้วย
  Java ขั้นตอนต่อขั้นตอนนี้แสดงการแปลงภาพใน Java สำหรับไฟล์ TIFF แบบหลายหน้า
linktitle: Extract TIFF Frames to BMP Format
second_title: Aspose.Imaging Java Image Processing API
title: วิธีแปลง tiff เป็น bmp ด้วย Aspose.Imaging สำหรับ Java
url: /th/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# แปลง tiff เป็น bmp ด้วย Aspose.Imaging สำหรับ Java

หากคุณต้องการ **convert tiff to bmp** ภายในแอปพลิเคชัน Java, คุณมาถูกที่แล้ว ไม่ว่าคุณจะจัดการกับ TIFF หน้าหนึ่งหรือเอกสารหลายหน้า, Aspose.Imaging for Java ทำให้กระบวนการเป็นเรื่องง่ายและเชื่อถือได้ ในบทเรียนนี้เราจะอธิบายขั้นตอนการดึงแต่ละเฟรมจากไฟล์ TIFF และบันทึกเป็นภาพ BMP แยกแต่ละไฟล์—เหมาะสำหรับสถานการณ์การแปลงภาพใน Java

## คำตอบด่วน
- **ไลบรารีใดจัดการการแปลง?** Aspose.Imaging for Java  
- **สามารถประมวลผล TIFF หลายหน้าได้หรือไม่?** ได้ – แต่ละเฟรมจะถูกบันทึกเป็น BMP แยกไฟล์  
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** จำเป็นต้องมีลิขสิทธิ์ Aspose ที่ถูกต้องสำหรับการใช้งานเชิงพาณิชย์  
- **รองรับเวอร์ชัน Java ใด?** Java 8 หรือสูงกว่า  
- **โค้ดใช้เวลารันนานเท่าไหร่?** ปกติใช้เวลาไม่กี่วินาทีสำหรับภาพขนาดมาตรฐาน  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:

1. **Java Development Environment** – JDK ที่ทำงานได้ (เวอร์ชัน 8 หรือใหม่กว่า) พร้อม IDE หรือเครื่องมือสร้างที่คุณเลือก  
2. **Aspose.Imaging for Java** – ดาวน์โหลด JAR ล่าสุดจากเว็บไซต์ [here](https://releases.aspose.com/imaging/java/)  
3. **Sample TIFF Image** – ไฟล์ TIFF (หน้าเดียวหรือหลายหน้า) ที่วางไว้ในไดเรกทอรีทำงานของโครงการของคุณ  

## นำเข้าแพ็กเกจ

เพื่อเริ่มกระบวนการ, คุณต้องนำเข้าแพ็กเกจที่จำเป็นสำหรับแอปพลิเคชัน Java ของคุณ:

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## คู่มือขั้นตอนการแปลง tiff เป็น bmp

### ขั้นตอนที่ 1: โหลดภาพ TIFF และกำหนดตัวนับเฟรม

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // Create an instance of int to keep track of frames in TiffImage
    int frameCounter = 0;
```

### ขั้นตอนที่ 2: วนลูปผ่านเฟรมของ TIFF

```java
    // Iterate over the TiffFrames in TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

### ขั้นตอนที่ 3: โหลดพิกเซลของ TiffFrame ลงในอาเรย์ของสี

```java
        // Load Pixels of TiffFrame into an array of Colors
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

### ขั้นตอนที่ 4: สร้าง BMP Options และตั้งค่า Bits Per Pixel

```java
        // Create an instance of bmpCreateOptions
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

### ขั้นตอนที่ 5: บันทึกภาพ BMP

```java
            // Set the Source of bmpCreateOptions as FileCreateSource by specifying the location where output will be saved
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // Create a new bmpImage
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // Save the bmpImage with pixels from TiffFrame
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## ทำไมต้องใช้ Aspose.Imaging for Java?

- **รองรับหลายหน้าอย่างแข็งแกร่ง** – จัดการกับจำนวนเฟรมของ TIFF ใด ๆ โดยไม่ต้องเขียนโค้ดเพิ่มเติม  
- **การทำงานแบบ Pure Java** – ไม่มีการพึ่งพา native library ทำให้เหมาะสำหรับการปรับใช้ข้ามแพลตฟอร์ม  
- **ผลลัพธ์ BMP คุณภาพสูง** – คุณสามารถควบคุม bits‑per‑pixel, การบีบอัด, และความลึกของสีได้  
- **ชุดเครื่องมือการแปลงภาพใน Java ครบวงจร** – รองรับ JPEG, PNG, GIF, และรูปแบบอื่น ๆ อีกมากมาย  

## ปัญหาทั่วไป & การแก้ไข

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ไข |
|---------|--------------|-----|
| `OutOfMemoryError` ขณะโหลด TIFF ขนาดใหญ่ | โหลดภาพทั้งหมดเข้าสู่หน่วยความจำ | ประมวลผลเฟรมทีละหนึ่งตามที่แสดง หรือเพิ่มขนาด heap ของ JVM (`-Xmx`) |
| ไฟล์ BMP เสียหาย | ค่า `BitsPerPixel` ไม่ถูกต้อง | ใช้ค่า 24 หรือ 32 สำหรับ BMP สีเต็ม |
| ไม่มีไฟล์ผลลัพธ์ถูกสร้าง | เส้นทางไดเรกทอรีผลลัพธ์ผิด | ตรวจสอบว่า `Your Document Directory` ชี้ไปยังโฟลเดอร์ที่มีอยู่ |

## คำถามที่พบบ่อย

### Q1: Aspose.Imaging for Java คืออะไร?

A1: Aspose.Imaging for Java เป็นไลบรารี Java ที่ให้ความสามารถในการประมวลผลภาพอย่างครอบคลุม, ช่วยให้คุณทำงานกับรูปแบบภาพต่าง ๆ และทำงานเช่นการแปลง, การแก้ไข, และการจัดการภาพได้

### Q2: ฉันสามารถใช้ Aspose.Imaging for Java กับรูปแบบภาพอื่น ๆ ได้หรือไม่?

A2: ได้, Aspose.Imaging for Java รองรับรูปแบบภาพหลากหลายรวมถึง TIFF, BMP, JPEG, PNG, และอื่น ๆ อีกมากมาย ทำให้เป็นเครื่องมือที่หลากหลายสำหรับงานที่เกี่ยวกับภาพ

### Q3: ฉันจะหาเอกสารสำหรับ Aspose.Imaging for Java ได้จากที่ไหน?

A3: คุณสามารถค้นหาเอกสารรายละเอียดสำหรับ Aspose.Imaging for Java [here](https://reference.aspose.com/imaging/java/)

### Q4: มีการทดลองใช้ฟรีสำหรับ Aspose.Imaging for Java หรือไม่?

A4: มี, คุณสามารถสำรวจ Aspose.Imaging for Java ด้วยการทดลองใช้ฟรีที่ [here](https://releases.aspose.com/)

### Q5: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.Imaging for Java อย่างไร?

A5: สำหรับคำถาม, ปัญหา หรือการสนับสนุนที่เกี่ยวกับ Aspose.Imaging for Java, คุณสามารถเยี่ยมชมฟอรั่มสนับสนุนได้ที่ [here](https://forum.aspose.com/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2025-12-19  
**ทดสอบด้วย:** Aspose.Imaging for Java 24.12 (latest)  
**ผู้เขียน:** Aspose