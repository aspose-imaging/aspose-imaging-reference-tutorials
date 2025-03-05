---
title: Image Binarization ด้วย Aspose.Imaging สำหรับ Java
linktitle: การแบ่งแยกเกณฑ์แบบอะแดปทีฟของแบรดลีย์
second_title: Aspose.Imaging Java Image Processing API
description: เรียนรู้การสร้างภาพแบบไบนาไรเซชันด้วย Aspose.Imaging สำหรับ Java แปลงภาพ DICOM ได้อย่างง่ายดาย สำรวจคำแนะนำทีละขั้นตอนพร้อมตัวอย่างโค้ด
type: docs
weight: 27
url: /th/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
---
รูปภาพมีบทบาทสำคัญในโลกดิจิทัล ไม่ว่าจะบนเว็บไซต์ ในเอกสาร หรือเป็นส่วนหนึ่งของแอปพลิเคชันต่างๆ การประมวลผลภาพเป็นงานสำคัญในโดเมนเหล่านี้ และการดำเนินการพื้นฐานประการหนึ่งคือการไบนาไรเซชันของภาพ การแปลงไบนารีทำให้รูปภาพง่ายขึ้นโดยการแปลงเป็นรูปแบบไบนารี ทำให้คอมพิวเตอร์ประมวลผลได้ง่ายขึ้น Aspose.Imaging สำหรับ Java เป็นเครื่องมืออันทรงพลังที่ให้ฟีเจอร์การจัดการรูปภาพที่หลากหลาย และในบทช่วยสอนนี้ เราจะมาดูวิธีดำเนินการไบนารี่ของรูปภาพโดยใช้ Aspose.Imaging's Adaptive Threshold Binarization ของ Bradley 

## ข้อกำหนดเบื้องต้น

ก่อนที่จะดำดิ่งสู่โลกแห่งการสร้างภาพแบบไบนาไรเซชันด้วย Aspose.Imaging สำหรับ Java เรามาตรวจสอบให้แน่ใจว่าคุณมีทุกสิ่งที่คุณต้องการ:

### สภาพแวดล้อมการพัฒนาจาวา

คุณควรตั้งค่าสภาพแวดล้อมการพัฒนา Java บนระบบของคุณ หากคุณยังไม่ได้ดาวน์โหลด คุณสามารถดาวน์โหลดและติดตั้ง Java Development Kit (JDK) ได้จากเว็บไซต์ Oracle

### Aspose.Imaging สำหรับ Java

หากต้องการปฏิบัติตามบทช่วยสอนนี้ คุณจะต้องติดตั้ง Aspose.Imaging for Java คุณสามารถดาวน์โหลดได้จากเว็บไซต์ Aspose โดยใช้ลิงก์ต่อไปนี้:[ดาวน์โหลด Aspose.Imaging สำหรับ Java](https://releases.aspose.com/imaging/java/).

### รูปภาพ DICOM

คุณจะต้องมีอิมเมจ DICOM ที่คุณต้องการสร้างไบนารี หากคุณไม่มี คุณสามารถค้นหาตัวอย่างรูปภาพ DICOM ทางออนไลน์ หรือใช้รูปภาพ DICOM ของคุณเองก็ได้

ตอนนี้คุณมีข้อกำหนดเบื้องต้นแล้ว เรามาต่อกันที่ขั้นตอนถัดไป

## แพ็คเกจนำเข้า

ในส่วนนี้ เราจะนำเข้าแพ็คเกจที่จำเป็นจาก Aspose.Imaging สำหรับ Java แพ็คเกจเหล่านี้ประกอบด้วยคลาสและวิธีการที่จำเป็นในการดำเนินการ Adaptive Threshold Binarization ของ Bradley บนอิมเมจ DICOM

```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// โหลดอิมเมจ DICOM ในอินสแตนซ์ของ DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // แปลงภาพเป็นสองเท่าด้วยเกณฑ์การปรับตัวของ Bradley
    image.binarizeBradley(10);
    // บันทึกภาพที่ได้
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

## ขั้นตอนที่ 1: กำหนดเส้นทาง

 ขั้นแรก กำหนดเส้นทางสำหรับอิมเมจ DICOM อินพุตของคุณและอิมเมจไบนาไรซ์เอาต์พุต แทนที่`"Your Document Directory"` พร้อมเส้นทางจริงไปยังไดเร็กทอรีของคุณ

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

## ขั้นตอนที่ 2: โหลดอิมเมจ DICOM

ใช้ Aspose.Imaging เพื่อโหลดอิมเมจ DICOM ที่ระบุโดย`inputFile` . การดำเนินการนี้จะสร้างอินสแตนซ์ของ`DicomImage` ระดับ.

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // ขั้นตอนการประมวลผลภาพจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 3: ดำเนินการ Binarization

 ดำเนินการ Adaptive Threshold Binarization ของ Bradley บนอิมเมจ DICOM ที่โหลด ในตัวอย่างนี้ เกณฑ์ของ`10` ถูกนำไปใช้

```java
image.binarizeBradley(10);
```

## ขั้นตอนที่ 4: บันทึกภาพ Binarized

บันทึกอิมเมจไบนารี่ที่ได้ผลลัพธ์ไปยังไฟล์เอาต์พุตที่ระบุโดยใช้รูปแบบ BMP

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีดำเนินการไบนารี่ของรูปภาพด้วย Aspose.Imaging สำหรับ Java โดยใช้ Adaptive Threshold Binarization ของ Bradley เรียบร้อยแล้ว เครื่องมืออันทรงพลังนี้ช่วยให้คุณสามารถเพิ่มความสามารถในการประมวลผลภาพ ทำให้เป็นทรัพย์สินที่มีค่าในการใช้งานต่างๆ

 อย่าลืมสำรวจเอกสารประกอบที่ครอบคลุมของ Aspose.Imaging เพื่อความเป็นไปได้ในการประมวลผลภาพเพิ่มเติม:[Aspose.Imaging สำหรับเอกสาร Java](https://reference.aspose.com/imaging/java/).

## คำถามที่พบบ่อย

### คำถามที่ 1: DICOM คืออะไร และเหตุใดจึงมีความสำคัญในการถ่ายภาพทางการแพทย์

คำตอบ 1: DICOM ย่อมาจาก Digital Imaging and Communications in Medicine และเป็นรูปแบบมาตรฐานสำหรับรูปภาพทางการแพทย์และข้อมูลที่เกี่ยวข้อง โดยมีบทบาทสำคัญในการจัดเก็บ แลกเปลี่ยน และตีความภาพทางการแพทย์ ทำให้มีความสำคัญสำหรับบุคลากรทางการแพทย์และระบบภาพทางการแพทย์

### คำถามที่ 2: ฉันสามารถใช้ Aspose.Imaging สำหรับ Java ในโปรเจ็กต์เชิงพาณิชย์ของฉันได้หรือไม่

 ตอบ 2: ใช่ Aspose.Imaging สำหรับ Java มีทั้งรุ่นทดลองใช้ฟรีและใบอนุญาตเชิงพาณิชย์ คุณสามารถสำรวจตัวเลือกของคุณและขอรับใบอนุญาตที่จำเป็นได้จาก[เว็บไซต์ของ Aspose](https://purchase.aspose.com/buy).

### คำถามที่ 3: มีใบอนุญาตชั่วคราวสำหรับการทดสอบหรือไม่

 ตอบ 3: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวสำหรับการทดสอบและประเมินผล Aspose.Imaging สำหรับ Java ได้ เยี่ยม[ลิงค์นี้](https://purchase.aspose.com/temporary-license/) สำหรับข้อมูลเพิ่มเติม.

### คำถามที่ 4: ฉันจะขอความช่วยเหลือหรือหารือเกี่ยวกับปัญหาที่เกี่ยวข้องกับ Aspose.Imaging for Java ได้ที่ไหน

 A4: สำหรับการสนับสนุนและการอภิปรายของชุมชน คุณสามารถไปที่[Aspose ฟอรั่มการถ่ายภาพ](https://forum.aspose.com/). เป็นสถานที่ที่ดีเยี่ยมในการค้นหาคำตอบสำหรับคำถามของคุณและเชื่อมต่อกับผู้ใช้รายอื่น

### คำถามที่ 5: Aspose.Imaging สำหรับ Java เหมาะสำหรับการประมวลผลภาพในแอปพลิเคชันที่ใช้ Java อื่นๆ หรือไม่

A5: ใช่ Aspose.Imaging สำหรับ Java มีความหลากหลายและสามารถใช้ในแอปพลิเคชันที่ใช้ Java ได้หลากหลาย รวมถึงเว็บแอปพลิเคชัน ซอฟต์แวร์เดสก์ท็อป และอื่นๆ