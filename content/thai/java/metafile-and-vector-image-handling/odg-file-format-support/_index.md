---
title: แปลง ODG เป็น PNG และ PDF ด้วย Aspose.Imaging สำหรับ Java
linktitle: รองรับรูปแบบไฟล์ ODG
second_title: Aspose.Imaging Java Image Processing API
description: เรียนรู้วิธีแปลงไฟล์ ODG เป็น PNG และ PDF ด้วย Aspose.Imaging สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการแปลงที่มีประสิทธิภาพ
type: docs
weight: 12
url: /th/java/metafile-and-vector-image-handling/odg-file-format-support/
---
ในโลกของการแปลงเอกสาร Aspose.Imaging สำหรับ Java โดดเด่นในฐานะเครื่องมืออันทรงพลังที่ช่วยให้คุณแปลงไฟล์ ODG (OpenDocument Graphics) เป็นรูปแบบ PNG และ PDF ได้อย่างง่ายดาย บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการทีละขั้นตอนโดยใช้ Aspose.Imaging สำหรับ Java ไม่ว่าคุณจะเป็นนักพัฒนาหรือเพียงแค่คนที่ต้องการแปลงไฟล์ ODG บทความนี้จะช่วยให้คุณบรรลุเป้าหมาย

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกกระบวนการแปลง คุณจะต้องตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

### 1. สภาพแวดล้อมการพัฒนาจาวา

 ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนระบบของคุณ คุณสามารถดาวน์โหลดและติดตั้ง Java Development Kit (JDK) ล่าสุดได้จาก[เว็บไซต์ออราเคิล](https://www.oracle.com/java/technologies/javase-downloads).

### 2. Aspose.Imaging สำหรับ Java

 คุณจะต้องดาวน์โหลดและติดตั้ง Aspose.Imaging สำหรับ Java คุณสามารถค้นหาเวอร์ชันล่าสุดได้ที่[Aspose.Imaging สำหรับหน้าดาวน์โหลด Java](https://releases.aspose.com/imaging/java/).

### 3. ไฟล์ ODG

แน่นอน คุณจะต้องมีไฟล์ ODG ที่คุณต้องการแปลง ตรวจสอบให้แน่ใจว่าคุณมีไฟล์เหล่านี้อยู่ในไดเร็กทอรีในระบบของคุณ

## แพ็คเกจนำเข้า

เมื่อคุณมีข้อกำหนดเบื้องต้นแล้ว เรามาเริ่มด้วยการนำเข้าแพ็คเกจที่จำเป็นในโปรเจ็กต์ Java ของคุณกันดีกว่า แพ็คเกจเหล่านี้จะช่วยให้คุณทำงานกับ Aspose.Imaging สำหรับ Java ได้อย่างมีประสิทธิภาพ

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.SizeF;
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
```

ตอนนี้เราจะแบ่งกระบวนการแปลงเป็นขั้นตอนง่ายๆ เพื่อให้ง่ายต่อการปฏิบัติตาม สำหรับแต่ละขั้นตอน เราจะให้หัวข้อและคำอธิบาย

## ขั้นตอนที่ 1: กำหนดไดเร็กทอรีข้อมูลของคุณ

 เริ่มต้นด้วยการระบุไดเร็กทอรีที่มีไฟล์ ODG ของคุณอยู่ คุณจะต้องเปลี่ยน`"Your Document Directory"` พร้อมเส้นทางจริงไปยังไดเร็กทอรีของคุณ

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

## ขั้นตอนที่ 2: ระบุไฟล์ ODG

สร้างอาร์เรย์ของชื่อไฟล์ ODG ที่คุณต้องการแปลง แทนที่ชื่อไฟล์ตัวอย่างด้วยชื่อไฟล์ ODG ของคุณ

```java
String[] files = new String[] {"example.odg", "example1.odg"};
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการแรสเตอร์

ตั้งค่าตัวเลือกการแรสเตอร์สำหรับไฟล์ ODG ตัวเลือกเหล่านี้จะกำหนดขนาดหน้าและการตั้งค่าแรสเตอร์เวกเตอร์

```java
final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
```

## ขั้นตอนที่ 4: วนซ้ำไฟล์ ODG

ตอนนี้ วนซ้ำไฟล์ ODG แต่ละไฟล์ โหลด และแปลงเป็นทั้งรูปแบบ PNG และ PDF

```java
for (String file : files) {
    String fileName = dataDir + file;
    try (Image image = Image.load(fileName)) {
        rasterizationOptions.setPageSize(new SizeF(image.getWidth(), image.getHeight()));

        // แปลงเป็น PNG
        String outFileName = "Your Document Directory" + file.replace(".odg", ".png");
        image.save(outFileName, new PngOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});

        // แปลงเป็น PDF
        outFileName = "Your Document Directory" + file.replace(".odg", ".pdf");
        image.save(outFileName, new PdfOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});
    }
}
```

ยินดีด้วย! คุณได้แปลงไฟล์ ODG ของคุณเป็นรูปแบบ PNG และ PDF สำเร็จโดยใช้ Aspose.Imaging สำหรับ Java

## บทสรุป

Aspose.Imaging สำหรับ Java ช่วยลดความยุ่งยากในการแปลงไฟล์ ODG เป็นรูปแบบรูปภาพที่รองรับอย่างกว้างขวาง เช่น PNG และ PDF ด้วยการทำตามขั้นตอนที่ระบุไว้ในบทช่วยสอนนี้ คุณสามารถทำการแปลงเหล่านี้ในโปรเจ็กต์ Java ของคุณได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Imaging สำหรับ Java เป็นเครื่องมือฟรีหรือไม่

 ตอบ 1: ไม่ Aspose.Imaging for Java เป็นไลบรารีเชิงพาณิชย์ และคุณสามารถดูข้อมูลราคาได้จาก[หน้าซื้อ](https://purchase.aspose.com/buy).

### คำถามที่ 2: ฉันสามารถลองใช้ Aspose.Imaging สำหรับ Java ก่อนซื้อได้หรือไม่

 A2: ได้ คุณสามารถดาวน์โหลดเวอร์ชันทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.Imaging สำหรับ Java ได้อย่างไร

 A3: คุณสามารถขอความช่วยเหลือและถามคำถามได้ที่[Aspose ฟอรั่มการถ่ายภาพ](https://forum.aspose.com/).

### คำถามที่ 4: Aspose.Imaging for Java สามารถจัดการไฟล์รูปแบบอื่นใดได้บ้าง

 A4: Aspose.Imaging สำหรับ Java รองรับรูปภาพและรูปแบบเอกสารที่หลากหลาย รวมถึง BMP, JPEG, TIFF, PDF และอื่นๆ อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/imaging/java/) สำหรับรายการที่ครอบคลุม

### คำถามที่ 5: ฉันสามารถใช้ Aspose.Imaging สำหรับ Java ในโปรเจ็กต์เชิงพาณิชย์ของฉันได้หรือไม่

A5: ได้ คุณสามารถใช้ Aspose.Imaging สำหรับ Java ในโครงการเชิงพาณิชย์ได้หลังจากซื้อใบอนุญาตที่เหมาะสมแล้ว