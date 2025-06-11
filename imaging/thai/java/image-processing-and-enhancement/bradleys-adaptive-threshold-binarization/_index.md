---
"description": "เรียนรู้การแปลงภาพเป็นไบนารีด้วย Aspose.Imaging สำหรับ Java แปลงภาพ DICOM ได้อย่างง่ายดาย สำรวจคำแนะนำทีละขั้นตอนพร้อมตัวอย่างโค้ด"
"linktitle": "การแปลงเกณฑ์การปรับตัวของแบรดลีย์เป็นไบนารี"
"second_title": "API การประมวลผลภาพ Java ของ Aspose.Imaging"
"title": "การแปลงภาพเป็นไบนารีด้วย Aspose.Imaging สำหรับ Java"
"url": "/th/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/"
"weight": 27
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# การแปลงภาพเป็นไบนารีด้วย Aspose.Imaging สำหรับ Java

รูปภาพมีบทบาทสำคัญในโลกดิจิทัล ไม่ว่าจะเป็นบนเว็บไซต์ เอกสาร หรือเป็นส่วนหนึ่งของแอปพลิเคชันต่างๆ การประมวลผลรูปภาพถือเป็นงานสำคัญในโดเมนเหล่านี้ และการดำเนินการพื้นฐานอย่างหนึ่งก็คือการแปลงรูปภาพเป็นไบนารี การแปลงเป็นไบนารีจะทำให้รูปภาพง่ายขึ้นโดยแปลงเป็นรูปแบบไบนารี ทำให้คอมพิวเตอร์ประมวลผลได้ง่ายขึ้น Aspose.Imaging สำหรับ Java เป็นเครื่องมือทรงพลังที่มีฟีเจอร์การจัดการรูปภาพมากมาย ในบทช่วยสอนนี้ เราจะมาสำรวจวิธีการแปลงรูปภาพเป็นไบนารีโดยใช้ Bradley's Adaptive Threshold Binarization ของ Aspose.Imaging 

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่โลกของการแปลงภาพเป็นไบนารีด้วย Aspose.Imaging สำหรับ Java โปรดตรวจสอบให้แน่ใจว่าคุณมีทุกสิ่งที่คุณต้องการก่อน:

### สภาพแวดล้อมการพัฒนา Java

คุณควรมีการตั้งค่าสภาพแวดล้อมการพัฒนา Java ไว้บนระบบของคุณแล้ว หากคุณยังไม่ได้ทำ คุณสามารถดาวน์โหลดและติดตั้ง Java Development Kit (JDK) ได้จากเว็บไซต์ของ Oracle

### Aspose.Imaging สำหรับ Java

หากต้องการทำตามบทช่วยสอนนี้ คุณต้องติดตั้ง Aspose.Imaging สำหรับ Java ก่อน คุณสามารถดาวน์โหลดได้จากเว็บไซต์ Aspose โดยใช้ลิงก์ต่อไปนี้: [ดาวน์โหลด Aspose.Imaging สำหรับ Java](https://releases-aspose.com/imaging/java/).

### ภาพ DICOM

คุณจะต้องมีไฟล์ภาพ DICOM ที่ต้องการแปลงเป็นไบนารี หากไม่มีไฟล์ภาพ DICOM คุณสามารถค้นหาตัวอย่างไฟล์ภาพ DICOM ออนไลน์ หรือคุณสามารถใช้ไฟล์ภาพ DICOM ของคุณเองได้

ตอนนี้คุณมีข้อกำหนดเบื้องต้นแล้ว มาดูขั้นตอนถัดไปกันเลย

## แพ็คเกจนำเข้า

ในส่วนนี้ เราจะนำเข้าแพ็คเกจที่จำเป็นจาก Aspose.Imaging สำหรับ Java แพ็คเกจเหล่านี้ประกอบด้วยคลาสและวิธีการที่จำเป็นในการดำเนินการ Bradley's Adaptive Threshold Binarization บนภาพ DICOM

```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// โหลดภาพ DICOM ในอินสแตนซ์ของ DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // แปลงภาพเป็นไบนารีด้วยเกณฑ์การปรับตัวของแบรดลีย์
    image.binarizeBradley(10);
    // บันทึกรูปภาพที่ได้
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

## ขั้นตอนที่ 1: กำหนดเส้นทาง

ขั้นแรก ให้กำหนดเส้นทางสำหรับภาพ DICOM อินพุตและภาพไบนารีเอาต์พุต แทนที่ `"Your Document Directory"` พร้อมเส้นทางจริงไปยังไดเร็กทอรีของคุณ

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

## ขั้นตอนที่ 2: โหลดภาพ DICOM

ใช้ Aspose.Imaging เพื่อโหลดภาพ DICOM ที่ระบุโดย `inputFile`การดำเนินการนี้จะสร้างอินสแตนซ์ของ `DicomImage` ระดับ.

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // ขั้นตอนการประมวลผลภาพจะดำเนินไปที่นี่
}
```

## ขั้นตอนที่ 3: ดำเนินการ Binarization

ดำเนินการ Adaptive Threshold Binarization ของ Bradley บนภาพ DICOM ที่โหลด ในตัวอย่างนี้ ขีดจำกัดของ `10` ได้ถูกนำมาประยุกต์ใช้

```java
image.binarizeBradley(10);
```

## ขั้นตอนที่ 4: บันทึกภาพแบบไบนารี

บันทึกภาพไบนารีผลลัพธ์ไปยังไฟล์เอาท์พุตที่ระบุโดยใช้รูปแบบ BMP

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## บทสรุป

ขอแสดงความยินดี! คุณได้เรียนรู้วิธีการแปลงภาพเป็นไบนารีด้วย Aspose.Imaging สำหรับ Java โดยใช้ Bradley's Adaptive Threshold Binarization สำเร็จแล้ว เครื่องมืออันทรงพลังนี้ช่วยให้คุณปรับปรุงความสามารถในการประมวลผลภาพ ทำให้เป็นเครื่องมือที่มีค่าในแอปพลิเคชันต่างๆ

อย่าลืมสำรวจเอกสารประกอบที่ครอบคลุมของ Aspose.Imaging เพื่อดูความเป็นไปได้ในการประมวลผลภาพเพิ่มเติม: [เอกสารประกอบ Aspose.Imaging สำหรับ Java](https://reference-aspose.com/imaging/java/).

## คำถามที่พบบ่อย

### คำถามที่ 1: DICOM คืออะไร และเหตุใดจึงมีความสำคัญในระบบถ่ายภาพทางการแพทย์

A1: DICOM ย่อมาจาก Digital Imaging and Communications in Medicine ซึ่งเป็นรูปแบบมาตรฐานสำหรับภาพทางการแพทย์และข้อมูลที่เกี่ยวข้อง DICOM มีบทบาทสำคัญในการจัดเก็บ แลกเปลี่ยน และตีความภาพทางการแพทย์ จึงมีความสำคัญอย่างยิ่งสำหรับผู้เชี่ยวชาญด้านการดูแลสุขภาพและระบบถ่ายภาพทางการแพทย์

### คำถามที่ 2: ฉันสามารถใช้ Aspose.Imaging สำหรับ Java ในโปรเจ็กต์เชิงพาณิชย์ของฉันได้หรือไม่

A2: ใช่ Aspose.Imaging สำหรับ Java มีทั้งรุ่นทดลองใช้งานฟรีและใบอนุญาตเชิงพาณิชย์ คุณสามารถสำรวจตัวเลือกต่างๆ และรับใบอนุญาตที่จำเป็นได้จาก [เว็บไซต์ของ Aspose](https://purchase-aspose.com/buy).

### คำถามที่ 3: มีใบอนุญาตชั่วคราวสำหรับวัตถุประสงค์ในการทดสอบหรือไม่

A3: ใช่ คุณสามารถขอรับใบอนุญาตชั่วคราวสำหรับการทดสอบและประเมินผล Aspose.Imaging สำหรับ Java ได้ เยี่ยมชม [ลิงค์นี้](https://purchase.aspose.com/temporary-license/) สำหรับข้อมูลเพิ่มเติม

### คำถามที่ 4: ฉันสามารถขอความช่วยเหลือหรือหารือปัญหาที่เกี่ยวข้องกับ Aspose.Imaging สำหรับ Java ได้ที่ไหน

A4: สำหรับการสนับสนุนและการสนทนาของชุมชน คุณสามารถเยี่ยมชม [ฟอรั่ม Aspose.Imaging](https://forum.aspose.com/)เป็นสถานที่ที่ยอดเยี่ยมในการค้นหาคำตอบสำหรับคำถามของคุณและเชื่อมต่อกับผู้ใช้รายอื่น

### คำถามที่ 5: Aspose.Imaging สำหรับ Java เหมาะกับการประมวลผลภาพในแอปพลิเคชันอื่นๆ ที่ใช้ Java หรือไม่

A5: ใช่ Aspose.Imaging สำหรับ Java มีความหลากหลายและสามารถใช้ในแอปพลิเคชันต่างๆ ที่ใช้ Java รวมถึงแอปพลิเคชันเว็บ ซอฟต์แวร์เดสก์ท็อป และอื่นๆ อีกมากมาย

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}