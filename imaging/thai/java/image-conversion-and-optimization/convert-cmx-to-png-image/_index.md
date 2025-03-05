---
title: แปลง CMX เป็น PNG ด้วย Aspose.Imaging สำหรับ Java
linktitle: แปลง CMX เป็นรูปภาพ PNG
second_title: Aspose.Imaging Java Image Processing API
description: เรียนรู้วิธีแปลงภาพ CMX เป็น PNG โดยใช้ Aspose.Imaging สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการแปลงภาพที่ราบรื่น
type: docs
weight: 10
url: /th/java/image-conversion-and-optimization/convert-cmx-to-png-image/
---
คุณต้องการแปลงไฟล์ CMX เป็นภาพ PNG โดยใช้ Java หรือไม่? Aspose.Imaging for Java เป็นเครื่องมือที่ทรงพลังและอเนกประสงค์ที่สามารถช่วยให้คุณบรรลุเป้าหมายนี้ได้อย่างง่ายดาย ในคำแนะนำทีละขั้นตอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแปลงไฟล์ CMX เป็นภาพ PNG โดยใช้ Aspose.Imaging สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. สภาพแวดล้อมการพัฒนาจาวา

คุณควรตั้งค่าสภาพแวดล้อมการพัฒนา Java บนระบบของคุณ ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java Development Kit (JDK) ล่าสุดแล้ว

2. Aspose.Imaging สำหรับ Java

 ดาวน์โหลดและติดตั้ง Aspose.Imaging สำหรับ Java คุณสามารถค้นหาแพ็คเกจที่จำเป็นและคำแนะนำในการติดตั้งได้ที่[ที่นี่](https://releases.aspose.com/imaging/java/).

3. ไฟล์ CMX

คุณจะต้องมีไฟล์ CMX ที่คุณต้องการแปลงเป็นภาพ PNG ตรวจสอบให้แน่ใจว่าคุณได้เก็บไฟล์เหล่านี้ไว้ในไดเร็กทอรี

## แพ็คเกจนำเข้า

หากต้องการเริ่มต้นการแปลง คุณต้องนำเข้าแพ็คเกจที่จำเป็นจาก Aspose.Imaging ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.CmxRasterizationOptions;
import com.aspose.imaging.system.drawing.SmoothingMode;
import com.aspose.imaging.positioning.PositioningTypes;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีข้อมูลของคุณ

คุณจะต้องระบุเส้นทางไปยังไดเร็กทอรีข้อมูลซึ่งมีไฟล์ CMX ของคุณอยู่ แทนที่`"Your Document Directory" + "CMX/"` พร้อมเส้นทางจริงไปยังไดเร็กทอรีของคุณ

```java
String dataDir = "Your Document Directory" + "CMX/";
```

## ขั้นตอนที่ 2: เตรียมรายการไฟล์ CMX

สร้างอาร์เรย์ของชื่อไฟล์ CMX ที่คุณต้องการแปลงเป็นรูปภาพ PNG ตรวจสอบให้แน่ใจว่าชื่อไฟล์ถูกต้องและตรงกับไฟล์ในไดเรกทอรีของคุณ

```java
String[] fileNames = new String[] {
    "Rectangle.cmx",
    "Rectangle+Fill.cmx",
    "Ellipse.cmx",
    "Ellipse+fill.cmx",
    "brushes.cmx",
    "outlines.cmx",
    "order.cmx",
    "many_images.cmx"
};
```

## ขั้นตอนที่ 3: แปลง CMX เป็น PNG

ตอนนี้ เรามาดำดิ่งลงสู่กระบวนการแปลง สำหรับไฟล์ CMX แต่ละไฟล์ในรายการ เราจะทำการแปลงเป็นรูปแบบ PNG

```java
for (String fileName : fileNames) {
    try (Image image = Image.load(dataDir + fileName)) {
        CmxRasterizationOptions cmxRasterizationOptions = new CmxRasterizationOptions();
        cmxRasterizationOptions.setPositioning(PositioningTypes.DefinedByDocument);
        cmxRasterizationOptions.setSmoothingMode(SmoothingMode.AntiAlias);
        PngOptions options = new PngOptions();
        options.setVectorRasterizationOptions(cmxRasterizationOptions);
        image.save("Your Document Directory" + fileName + ".docpage.png", options);
    }
}
```

ทำซ้ำขั้นตอนนี้สำหรับไฟล์ CMX แต่ละไฟล์ในรายการของคุณ รูปภาพ PNG ที่แปลงแล้วจะถูกบันทึกในไดเร็กทอรีที่ระบุ

ยินดีด้วย! คุณได้แปลงไฟล์ CMX เป็นภาพ PNG โดยใช้ Aspose.Imaging สำหรับ Java เรียบร้อยแล้ว ตอนนี้คุณสามารถใช้รูปภาพ PNG เหล่านี้เพื่อวัตถุประสงค์ต่างๆ ได้ เช่น การแสดงบนเว็บไซต์หรือรวมไว้ในเอกสารของคุณ

## บทสรุป

ในคู่มือที่ครอบคลุมนี้ เราได้สำรวจวิธีใช้ Aspose.Imaging สำหรับ Java เพื่อแปลงไฟล์ CMX เป็นภาพ PNG ด้วยข้อกำหนดเบื้องต้นที่เหมาะสมและโดยทำตามคำแนะนำทีละขั้นตอน คุณสามารถดำเนินการแปลงนี้ได้อย่างมีประสิทธิภาพและเพิ่มความสามารถในการประมวลผลภาพในแอปพลิเคชัน Java ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Imaging สำหรับ Java คืออะไร

คำตอบ 1: Aspose.Imaging for Java เป็นไลบรารี Java ที่ช่วยให้นักพัฒนาสามารถทำงานกับรูปแบบรูปภาพที่หลากหลาย ทำการแก้ไขรูปภาพ และงานการแปลง

### คำถามที่ 2: ฉันจะหาเอกสารสำหรับ Aspose.Imaging สำหรับ Java ได้ที่ไหน

 A2: คุณสามารถค้นหาเอกสารประกอบสำหรับ Aspose.Imaging สำหรับ Java ได้[ที่นี่](https://reference.aspose.com/imaging/java/). ให้ข้อมูลเชิงลึกเกี่ยวกับคุณสมบัติและฟังก์ชันของห้องสมุด

### คำถามที่ 3: Aspose.Imaging สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถทดลองใช้ Aspose.Imaging สำหรับ Java ได้ฟรี[ที่นี่](https://releases.aspose.com/). ช่วยให้คุณสามารถสำรวจความสามารถของห้องสมุดก่อนตัดสินใจซื้อ

### คำถามที่ 4: ฉันจะรับสิทธิ์ใช้งานชั่วคราวสำหรับ Aspose.Imaging สำหรับ Java ได้อย่างไร

A4: คุณสามารถขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.Imaging สำหรับ Java ได้โดยไปที่[ลิงค์นี้](https://purchase.aspose.com/temporary-license/). เป็นตัวเลือกที่สะดวกสำหรับการใช้งานระยะสั้น

### คำถามที่ 5: กรณีการใช้งานทั่วไปในการแปลงภาพ CMX เป็น PNG มีอะไรบ้าง

A5: กรณีการใช้งานทั่วไป ได้แก่ การสร้างกราฟิกบนเว็บ การเตรียมภาพสำหรับการพิมพ์ และการแปลงกราฟิกแบบเวกเตอร์เพื่อใช้ในแอปพลิเคชันต่างๆ