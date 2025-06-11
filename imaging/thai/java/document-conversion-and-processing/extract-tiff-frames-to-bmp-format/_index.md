---
"description": "เรียนรู้วิธีแยกเฟรม TIFF เป็นรูปแบบ BMP ใน Java โดยใช้ Aspose.Imaging สำหรับ Java ทำตามคำแนะนำทีละขั้นตอนของเรา"
"linktitle": "แยกเฟรม TIFF เป็นรูปแบบ BMP"
"second_title": "API การประมวลผลภาพ Java ของ Aspose.Imaging"
"title": "การแปลงไฟล์ TIFF เป็น BMP ด้วย Aspose.Imaging สำหรับ Java"
"url": "/th/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/"
"weight": 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# การแปลงไฟล์ TIFF เป็น BMP ด้วย Aspose.Imaging สำหรับ Java

หากคุณกำลังทำงานกับไฟล์ภาพใน Java โดยเฉพาะภาพ TIFF และต้องการแยกเฟรมจากภาพเหล่านี้และบันทึกเป็นรูปแบบ BMP Aspose.Imaging สำหรับ Java เป็นเครื่องมือที่มีประสิทธิภาพและหลากหลายที่จะช่วยให้บรรลุเป้าหมายดังกล่าวได้ ในคู่มือทีละขั้นตอนนี้ เราจะแนะนำคุณเกี่ยวกับกระบวนการแยกเฟรม TIFF เป็นรูปแบบ BMP โดยใช้ Aspose.Imaging สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม โปรดตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

1. สภาพแวดล้อมการพัฒนา Java: คุณควรมีการตั้งค่าสภาพแวดล้อมการพัฒนา Java ที่ใช้งานได้บนระบบของคุณ

2. Aspose.Imaging สำหรับ Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Imaging สำหรับ Java แล้ว คุณสามารถดาวน์โหลดได้จากเว็บไซต์ [ที่นี่](https://releases-aspose.com/imaging/java/).

3. ตัวอย่างไฟล์ภาพ TIFF: มีไฟล์ภาพ TIFF ตัวอย่างที่คุณต้องการแยกเฟรมออกมา ตรวจสอบให้แน่ใจว่ามีภาพนี้อยู่ในไดเร็กทอรีการทำงานของคุณ

## แพ็คเกจนำเข้า

ในการเริ่มกระบวนการ คุณต้องนำเข้าแพ็คเกจที่จำเป็นสำหรับแอปพลิเคชัน Java ของคุณ:

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## ขั้นตอนที่ 1: โหลดภาพ TIFF และเริ่มต้นตัวนับเฟรม

```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // สร้างอินสแตนซ์ของ int เพื่อติดตามเฟรมใน TiffImage
    int frameCounter = 0;
```

## ขั้นตอนที่ 2: ทำซ้ำในเฟรม TIFF

```java
    // ทำซ้ำผ่าน TiffFrames ใน TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

## ขั้นตอนที่ 3: โหลดพิกเซลของ TiffFrame ลงในอาร์เรย์สี

```java
        // โหลดพิกเซลของ TiffFrame ลงในอาร์เรย์ของสี
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

## ขั้นตอนที่ 4: สร้างตัวเลือก BMP และตั้งค่าบิตต่อพิกเซล

```java
        // สร้างอินสแตนซ์ของ bmpCreateOptions
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

## ขั้นตอนที่ 5: บันทึกภาพ BMP

```java
            // ตั้งค่าแหล่งที่มาของ bmpCreateOptions เป็น FileCreateSource โดยระบุตำแหน่งที่จะบันทึกเอาต์พุต
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // สร้าง bmpImage ใหม่
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // บันทึก bmpImage ด้วยพิกเซลจาก TiffFrame
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้กล่าวถึงวิธีการแยกเฟรม TIFF และบันทึกเป็นภาพ BMP โดยใช้ Aspose.Imaging สำหรับ Java ด้วยข้อกำหนดเบื้องต้นที่ถูกต้องและปฏิบัติตามคำแนะนำทีละขั้นตอน คุณสามารถดำเนินการแปลงภาพนี้ในแอปพลิเคชัน Java ได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Imaging สำหรับ Java คืออะไร

A1: Aspose.Imaging สำหรับ Java คือไลบรารี Java ที่ให้ความสามารถในการประมวลผลภาพอย่างครอบคลุม ช่วยให้คุณสามารถทำงานกับรูปแบบภาพต่าง ๆ และดำเนินการต่าง ๆ เช่น การแปลง การแก้ไข และการจัดการ

### คำถามที่ 2: ฉันสามารถใช้ Aspose.Imaging สำหรับ Java กับรูปแบบภาพอื่นได้หรือไม่

A2: ใช่ Aspose.Imaging สำหรับ Java รองรับรูปแบบภาพหลากหลาย รวมถึง TIFF, BMP, JPEG, PNG และอื่นๆ อีกมากมาย ทำให้เป็นเครื่องมืออเนกประสงค์สำหรับงานที่เกี่ยวข้องกับรูปภาพ

### คำถามที่ 3: ฉันสามารถค้นหาเอกสารสำหรับ Aspose.Imaging สำหรับ Java ได้ที่ไหน

A3: คุณสามารถค้นหาเอกสารรายละเอียดสำหรับ Aspose.Imaging สำหรับ Java ได้ [ที่นี่](https://reference-aspose.com/imaging/java/).

### คำถามที่ 4: มีรุ่นทดลองใช้งานฟรีสำหรับ Aspose.Imaging สำหรับ Java หรือไม่

A4: ใช่ คุณสามารถสำรวจ Aspose.Imaging สำหรับ Java พร้อมทดลองใช้งานฟรีได้ [ที่นี่](https://releases-aspose.com/).

### คำถามที่ 5: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.Imaging สำหรับ Java ได้อย่างไร

A5: หากมีคำถาม ปัญหา หรือต้องการความช่วยเหลือเกี่ยวกับ Aspose.Imaging สำหรับ Java โปรดไปที่ฟอรัมสนับสนุน [ที่นี่](https://forum-aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}