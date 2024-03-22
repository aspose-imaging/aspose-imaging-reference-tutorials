---
title: การแปลง TIFF เป็น BMP ด้วย Aspose.Imaging สำหรับ Java
linktitle: แยกเฟรม TIFF เป็นรูปแบบ BMP
second_title: Aspose.Imaging Java Image Processing API
description: เรียนรู้วิธีแยกเฟรม TIFF เป็นรูปแบบ BMP ใน Java โดยใช้ Aspose.Imaging สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเรา
type: docs
weight: 13
url: /th/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
---
หากคุณกำลังทำงานกับไฟล์รูปภาพใน Java โดยเฉพาะรูปภาพ TIFF และจำเป็นต้องแยกเฟรมออกจากไฟล์เหล่านั้นและบันทึกในรูปแบบ BMP Aspose.Imaging for Java เป็นเครื่องมือที่ทรงพลังและอเนกประสงค์เพื่อให้บรรลุเป้าหมายนี้ ในคำแนะนำทีละขั้นตอนนี้ เราจะแนะนำคุณตลอดกระบวนการแยกเฟรม TIFF เป็นรูปแบบ BMP โดยใช้ Aspose.Imaging สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. สภาพแวดล้อมการพัฒนา Java: คุณควรตั้งค่าสภาพแวดล้อมการพัฒนา Java ที่ใช้งานได้บนระบบของคุณ

2.  Aspose.Imaging for Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Imaging for Java แล้ว คุณสามารถดาวน์โหลดได้จากเว็บไซต์[ที่นี่](https://releases.aspose.com/imaging/java/).

3. ภาพ TIFF ตัวอย่าง: มีไฟล์ภาพ TIFF ตัวอย่างที่คุณต้องการแยกเฟรมออกมา ตรวจสอบให้แน่ใจว่าจะมีรูปภาพนี้อยู่ในไดเร็กทอรีการทำงานของคุณ

## แพ็คเกจนำเข้า

ในการเริ่มต้นกระบวนการ คุณจะต้องนำเข้าแพ็คเกจที่จำเป็นสำหรับแอปพลิเคชัน Java ของคุณ:

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## ขั้นตอนที่ 1: โหลดอิมเมจ TIFF และเริ่มต้นตัวนับเฟรม

```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // สร้างอินสแตนซ์ของ int เพื่อติดตามเฟรมใน TiffImage
    int frameCounter = 0;
```

## ขั้นตอนที่ 2: วนซ้ำเฟรม TIFF

```java
    // วนซ้ำ TiffFrames ใน TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

## ขั้นตอนที่ 3: โหลดพิกเซลของ TiffFrame ลงในอาร์เรย์ของสี

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

## ขั้นตอนที่ 5: บันทึกรูปภาพ BMP

```java
            // ตั้งค่า Source ของ bmpCreateOptions เป็น FileCreateSource โดยการระบุตำแหน่งที่จะบันทึกเอาต์พุต
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

ในบทช่วยสอนนี้ เราได้กล่าวถึงวิธีการแยกเฟรม TIFF และบันทึกเป็นรูปภาพ BMP โดยใช้ Aspose.Imaging สำหรับ Java ด้วยข้อกำหนดเบื้องต้นที่เหมาะสมและปฏิบัติตามคำแนะนำทีละขั้นตอน คุณสามารถดำเนินการแปลงรูปภาพนี้ในแอปพลิเคชัน Java ของคุณได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Imaging สำหรับ Java คืออะไร

คำตอบ 1: Aspose.Imaging for Java เป็นไลบรารี Java ที่ให้ความสามารถในการประมวลผลรูปภาพที่ครอบคลุม ช่วยให้คุณสามารถทำงานกับรูปแบบรูปภาพที่หลากหลาย และทำงานต่างๆ เช่น การแปลง การแก้ไข และการจัดการ

### คำถามที่ 2: ฉันสามารถใช้ Aspose.Imaging สำหรับ Java ที่มีรูปแบบรูปภาพต่างกันได้หรือไม่

ตอบ 2: ใช่ Aspose.Imaging for Java รองรับรูปแบบรูปภาพที่หลากหลาย รวมถึง TIFF, BMP, JPEG, PNG และอื่นๆ อีกมากมาย ทำให้เป็นเครื่องมืออเนกประสงค์สำหรับงานที่เกี่ยวข้องกับรูปภาพ

### คำถามที่ 3: ฉันจะหาเอกสารสำหรับ Aspose.Imaging สำหรับ Java ได้ที่ไหน

 A3: คุณสามารถค้นหาเอกสารโดยละเอียดสำหรับ Aspose.Imaging สำหรับ Java ได้[ที่นี่](https://reference.aspose.com/imaging/java/).

### คำถามที่ 4: Aspose.Imaging สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

ตอบ 4: ได้ คุณสามารถสำรวจ Aspose.Imaging สำหรับ Java พร้อมให้ทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.Imaging สำหรับ Java ได้อย่างไร

 A5: สำหรับคำถาม ปัญหา หรือการสนับสนุนที่เกี่ยวข้องกับ Aspose.Imaging สำหรับ Java คุณสามารถไปที่ฟอรัมการสนับสนุน[ที่นี่](https://forum.aspose.com/).