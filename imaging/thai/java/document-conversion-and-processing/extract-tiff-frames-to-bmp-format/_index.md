---
date: 2026-05-03
description: เรียนรู้วิธีแปลงไฟล์ TIFF หลายหน้าเป็นรูปแบบ BMP ใน Java ด้วย Aspose.Imaging.
  ทำตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อแปลง TIFF อย่างมีประสิทธิภาพ.
keywords:
- convert multi page tiff
- how to convert tiff
- Aspose.Imaging Java
- TIFF to BMP conversion
- image processing Java
linktitle: แยกเฟรม TIFF เป็นรูปแบบ BMP
second_title: Aspose.Imaging Java Image Processing API
title: แปลง Multi Page TIFF เป็น BMP ด้วย Aspose.Imaging สำหรับ Java
url: /th/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# แปลง Multi Page TIFF เป็น BMP ด้วย Aspose.Imaging สำหรับ Java

หากคุณต้องการ **แปลงไฟล์ multi page tiff** ให้เป็นภาพ BMP แยกแต่ละไฟล์ขณะทำงานในสภาพแวดล้อม Java คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะอธิบายขั้นตอนอย่างละเอียดเพื่อดึงแต่ละเฟรมของ TIFF และบันทึกเป็นไฟล์ BMP ด้วยไลบรารี Aspose.Imaging สำหรับ Java ที่ทรงพลัง เมื่อเสร็จสิ้นคุณจะเข้าใจไม่เพียงแค่ *วิธีแปลงไฟล์ tiff* ด้วยโปรแกรมเท่านั้น แต่ยังรู้ว่าทำไมวิธีนี้จึงเชื่อถือได้สำหรับงานประมวลผลภาพแบบแบตช์

## คำตอบสั้นๆ
- **ไลบรารีใดดีที่สุดสำหรับการแปลง TIFF เป็น BMP?** Aspose.Imaging for Java  
- **ต้องใช้บรรทัดโค้ดกี่บรรทัด?** ประมาณ 30 บรรทัดแบ่งเป็นห้าขั้นตอนตรรกะ  
- **ฉันต้องการไลเซนส์สำหรับการใช้งานจริงหรือไม่?** ใช่ จำเป็นต้องมีไลเซนส์เชิงพาณิชย์ (มีการทดลองใช้ฟรี)  
- **สามารถจัดการกับ TIFF แบบหลายหน้าใหญ่ได้หรือไม่?** ใช่ API จะสตรีมเฟรมอย่างมีประสิทธิภาพ  
- **รองรับเวอร์ชัน Java ใด?** Java 8 และใหม่กว่า  

## “convert multi page tiff” คืออะไร?
การแปลง multi‑page TIFF หมายถึงการนำแต่ละหน้า (หรือเฟรม) ที่เก็บอยู่ในคอนเทนเนอร์ TIFF เดียวและส่งออกเป็นไฟล์ภาพอิสระ—ในที่นี้คือ BMP การทำเช่นนี้มีประโยชน์สำหรับการเก็บเอกสาร, การถ่ายภาพทางการแพทย์, หรือกระบวนการทำงานใด ๆ ที่ต้องการภาพราสเตอร์เพื่อการประมวลผลต่อไป

## ทำไมต้องใช้ Aspose.Imaging สำหรับ Java?
- **Full format support** – รองรับ TIFF, BMP, JPEG, PNG และอื่น ๆ อีกมาก  
- **No external dependencies** – เป็น Java แท้ ไม่ต้องพึ่งพาไลบรารีเนทีฟ  
- **High performance** – การเข้าถึงเฟรมแบบสตรีมช่วยลดการใช้หน่วยความจำ  
- **Rich API** – ให้การควบคุมระดับละเอียดของข้อมูลพิกเซล, ความลึกสี, และเมตาดาต้า  

## ข้อกำหนดเบื้องต้น

1. **Java Development Environment** – JDK 8+ และ IDE ที่คุณชื่นชอบ  
2. **Aspose.Imaging for Java** – ดาวน์โหลด JAR เวอร์ชันล่าสุดจากเว็บไซต์ทางการ **[here](https://releases.aspose.com/imaging/java/)**  
3. **Sample multi‑page TIFF** – วางไฟล์ TIFF (เช่น `sample.tiff`) ในไดเรกทอรีที่รู้จักซึ่งโค้ดของคุณสามารถอ่านได้  

## นำเข้าแพ็กเกจ

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## วิธีการแปลง Multi Page TIFF เป็น BMP ด้วย Aspose.Imaging

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

## ข้อผิดพลาดทั่วไปและเคล็ดลับ

- **Memory usage:** เมื่อจัดการกับไฟล์ TIFF ขนาดใหญ่มาก ควรประมวลผลเฟรมทีละเฟรม (ตามที่แสดง) แทนการโหลดภาพทั้งหมดเข้าสู่หน่วยความจำ  
- **File naming:** คำสั่ง `String.format` จะสร้างชื่อไฟล์ที่ไม่ซ้ำกันสำหรับแต่ละเฟรม (`...out0.bmp`, `...out1.bmp`, เป็นต้น) ปรับรูปแบบหากต้องการรูปแบบการตั้งชื่ออื่น  
- **Bit depth:** BMP รองรับบิตเดพธ์หลายระดับ; 24‑bit (สีจริง) ทำงานได้ในหลายกรณี ปรับ `setBitsPerPixel` หากต้องการเอาต์พุตแบบ 8‑bit grayscale  

## คำถามที่พบบ่อย

### Q1: Aspose.Imaging for Java คืออะไร?
A1: Aspose.Imaging for Java เป็นไลบรารี Java ที่ให้ความสามารถในการประมวลผลภาพอย่างครอบคลุม ช่วยให้คุณทำงานกับรูปแบบภาพต่าง ๆ และทำงานเช่น การแปลง, การแก้ไข, และการจัดการภาพ  

### Q2: ฉันสามารถใช้ Aspose.Imaging for Java กับรูปแบบภาพอื่น ๆ ได้หรือไม่?
A2: ใช่, Aspose.Imaging for Java รองรับรูปแบบภาพหลากหลาย รวมถึง TIFF, BMP, JPEG, PNG และอื่น ๆ อีกมาก ทำให้เป็นเครื่องมือที่หลากหลายสำหรับงานที่เกี่ยวกับภาพ  

### Q3: ฉันจะหาเอกสารสำหรับ Aspose.Imaging for Java ได้จากที่ไหน?
A3: คุณสามารถค้นหาเอกสารรายละเอียดสำหรับ Aspose.Imaging for Java **[here](https://reference.aspose.com/imaging/java/)**  

### Q4: มีการทดลองใช้ฟรีสำหรับ Aspose.Imaging for Java หรือไม่?
A4: ใช่, คุณสามารถสำรวจ Aspose.Imaging for Java ด้วยการทดลองใช้ฟรีที่ **[here](https://releases.aspose.com/)**  

### Q5: ฉันจะรับการสนับสนุนสำหรับ Aspose.Imaging for Java อย่างไร?
A5: สำหรับคำถาม, ปัญหา หรือการสนับสนุนที่เกี่ยวกับ Aspose.Imaging for Java คุณสามารถเยี่ยมชมฟอรั่มสนับสนุน **[here](https://forum.aspose.com/)**  

## คำถามที่พบบ่อย

**Q: ฉันสามารถแปลง multi‑page TIFF ไปเป็นรูปแบบอื่น (เช่น PNG) ด้วยวิธีเดียวกันได้หรือไม่?**  
A: แน่นอน. แทนที่ `BmpOptions` ด้วยคลาสตัวเลือกที่เหมาะสม (เช่น `PngOptions`) และปรับส่วนขยายไฟล์ในพาธ `FileCreateSource`  

**Q: Aspose.Imaging รองรับ TIFF ที่บีบอัด (LZW, CCITT) หรือไม่?**  
A: ใช่, ไลบรารีจะทำการดีคอมเพรสสคอมเพรสชัน TIFF ที่รองรับโดยอัตโนมัติระหว่างการดึงเฟรม  

**Q: สามารถเก็บข้อมูลเมตาดาต้า EXIF ไว้เมื่อแปลงเป็น BMP ได้หรือไม่?**  
A: BMP ไม่รองรับเมตาดาต้า EXIF หากต้องการเก็บเมตาดาต้า ควรแปลงเป็นรูปแบบที่รองรับ (เช่น PNG) หรือคัดลอกเมตาดาต้าเองหลังการแปลง  

**Q: ฉันจะประมวลผลหลายไฟล์ TIFF ในโฟลเดอร์พร้อมกันอย่างไร?**  
A: ใส่โค้ดข้างต้นในลูปที่วนผ่านวัตถุ `File` ในไดเรกทอรี ปรับ `dataDir` และชื่อไฟล์ต้นทางสำหรับแต่ละไฟล์  

**Q: ต้องการไลเซนส์แบบใดสำหรับการใช้งานเชิงพาณิชย์?**  
A: จำเป็นต้องมีไลเซนส์ Aspose.Imaging for Java แบบชำระเงินสำหรับการใช้งานในผลิตภัณฑ์ ไลเซนส์ทดลองชั่วคราวสามารถใช้ได้ในระหว่างการพัฒนา  

**Last Updated:** 2026-05-03  
**Tested With:** Aspose.Imaging for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}