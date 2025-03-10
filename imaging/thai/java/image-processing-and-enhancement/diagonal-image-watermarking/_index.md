---
title: ลายน้ำภาพแนวทแยงด้วย Aspose.Imaging สำหรับ Java
linktitle: ลายน้ำภาพแนวทแยง
second_title: Aspose.Imaging Java Image Processing API
description: ปรับปรุงรูปภาพของคุณด้วยลายน้ำแนวทแยงโดยใช้ Aspose.Imaging สำหรับ Java ทำตามคำแนะนำทีละขั้นตอนนี้และสร้างภาพลายน้ำที่น่าทึ่งได้อย่างง่ายดาย
weight: 14
url: /th/java/image-processing-and-enhancement/diagonal-image-watermarking/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ลายน้ำภาพแนวทแยงด้วย Aspose.Imaging สำหรับ Java


หากคุณต้องการปรับปรุงรูปภาพของคุณด้วยลายน้ำแนวทแยงที่มีสไตล์ Aspose.Imaging for Java พร้อมให้ความช่วยเหลือ ในคำแนะนำทีละขั้นตอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการเพิ่มลายน้ำข้อความที่หมุนได้ 45 องศาให้กับรูปภาพ JPG ที่มีอยู่ คุณไม่จำเป็นต้องเป็นผู้เชี่ยวชาญในด้าน Java หรือการประมวลผลภาพเพื่อปฏิบัติตาม เราจะแบ่งแต่ละตัวอย่างออกเป็นหลายขั้นตอนเพื่อให้แน่ใจว่าคุณจะได้ผลลัพธ์ระดับมืออาชีพได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะดำดิ่งสู่โลกแห่งการใส่ลายน้ำบนรูปภาพ คุณจะต้องมีสิ่งต่อไปนี้:

1.  Aspose.Imaging for Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Imaging for Java แล้ว คุณสามารถค้นหาลิงค์ดาวน์โหลด[ที่นี่](https://releases.aspose.com/imaging/java/).

2. สภาพแวดล้อมการพัฒนา Java: คุณควรตั้งค่าสภาพแวดล้อมการพัฒนา Java ที่ใช้งานได้บนคอมพิวเตอร์ของคุณ

3. รูปภาพเป็นลายน้ำ: เตรียมรูปภาพที่คุณต้องการใส่ลายน้ำและจัดเก็บไว้ในไดเร็กทอรี คุณสามารถใช้ภาพตัวอย่างสำหรับบทช่วยสอนนี้

## แพ็คเกจนำเข้า

ขั้นแรก นำเข้าแพ็คเกจที่จำเป็นเพื่อเตรียมโปรเจ็กต์ Java ของคุณให้พร้อมสำหรับลายน้ำรูปภาพ ด้านล่างนี้เป็นแพ็คเกจสำคัญที่คุณต้องมี:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## ขั้นตอนที่ 1: โหลดรูปภาพที่มีอยู่

โหลดภาพที่คุณต้องการใส่ลายน้ำ ในตัวอย่างนี้ เราถือว่าคุณมีรูปภาพ JPG ชื่อ "SampleTiff1.tiff" ในไดเร็กทอรี "ModifyingImages" ของคุณ

```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory" + "ModifyingImages/";

// โหลดรูปภาพ JPG ที่มีอยู่
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // รหัสที่เหลืออยู่ที่นี่
}
```

## ขั้นตอนที่ 2: เตรียมข้อความและกราฟิกลายน้ำ

ตอนนี้ เรามาประกาศข้อความลายน้ำของคุณและตั้งค่ากราฟิกสำหรับลายน้ำ

```java
// ประกาศวัตถุ String ด้วยข้อความลายน้ำ
String theString = "45 Degree Rotated Text";

// สร้างและเริ่มต้นอินสแตนซ์ของคลาสกราฟิก
Graphics graphics = new Graphics(image);

// เริ่มต้นวัตถุขนาด F เพื่อจัดเก็บขนาดภาพ
Size sz = graphics.getImage().getSize();
```

## ขั้นตอนที่ 3: กำหนดแบบอักษรและแปรง

ตั้งค่าแบบอักษรและแปรงสำหรับลายน้ำของคุณ คุณสามารถปรับแต่งแบบอักษร ขนาด และสไตล์ให้ตรงกับความต้องการของคุณได้

```java
// สร้างอินสแตนซ์ของแบบอักษร เริ่มต้นด้วยหน้าแบบอักษร ขนาด และสไตล์
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// สร้างอินสแตนซ์ของ SolidBrush และตั้งค่าคุณสมบัติต่างๆ
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## ขั้นตอนที่ 4: จัดรูปแบบข้อความของคุณ

กำหนดรูปแบบสำหรับข้อความลายน้ำของคุณ รวมถึงการจัดตำแหน่งและการจัดรูปแบบธง

```java
// เริ่มต้นวัตถุของคลาส StringFormat และตั้งค่าคุณสมบัติต่างๆ
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## ขั้นตอนที่ 5: ใช้การเปลี่ยนแปลง

สร้างเมทริกซ์การแปลงเพื่อวางตำแหน่งและหมุนข้อความลายน้ำ ในตัวอย่างนี้ เราจะหมุนข้อความ 45 องศา

```java
// สร้างอ็อบเจ็กต์ของคลาส Matrix สำหรับการแปลง
Matrix matrix = new Matrix();
//ขั้นแรกให้แปลแล้วจึงหมุนเวียน
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// ตั้งค่าการแปลงผ่านเมทริกซ์
graphics.setTransform(matrix);
```

## ขั้นตอนที่ 6: วาดและบันทึก

ตอนนี้ได้เวลาเพิ่มข้อความลงในรูปภาพแล้วบันทึกรูปภาพที่มีลายน้ำไปยังตำแหน่งที่คุณต้องการ

```java
// วาดเส้นบนรูปภาพ
graphics.drawString(theString, font, brush, 0, 0, format);

// บันทึกเอาต์พุตลงดิสก์
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

ยินดีด้วย! คุณได้เพิ่มลายน้ำแนวทแยงให้กับรูปภาพของคุณสำเร็จแล้วโดยใช้ Aspose.Imaging สำหรับ Java

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีปรับปรุงรูปภาพของคุณด้วยลายน้ำแนวทแยงโดยใช้ Aspose.Imaging สำหรับ Java เป็นเครื่องมือที่ทรงพลังในการเพิ่มความเป็นมืออาชีพให้กับรูปภาพของคุณ ด้วยขั้นตอนง่ายๆ เพียงไม่กี่ขั้นตอน คุณสามารถสร้างภาพลายน้ำอันน่าทึ่งที่โดดเด่นกว่าที่อื่นได้

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Imaging สำหรับ Java เหมาะสำหรับผู้เริ่มต้นหรือไม่

A1: แน่นอน! Aspose.Imaging สำหรับ Java นำเสนออินเทอร์เฟซที่เป็นมิตรต่อผู้ใช้และเอกสารประกอบที่ครอบคลุม แม้แต่ผู้เริ่มต้นก็สามารถเริ่มต้นการประมวลผลภาพได้อย่างรวดเร็ว

### คำถามที่ 2: ฉันสามารถปรับแต่งข้อความและสไตล์ลายน้ำได้หรือไม่

A2: ได้ คุณสามารถปรับแต่งข้อความลายน้ำ แบบอักษร ขนาด สี และมุมการหมุนเพื่อให้ตรงกับความต้องการและแบรนด์ของคุณได้อย่างง่ายดาย

### คำถามที่ 3: Aspose.Imaging สำหรับ Java รองรับรูปแบบรูปภาพอื่นนอกเหนือจาก JPG หรือไม่

A3: ใช่ Aspose.Imaging สำหรับ Java รองรับรูปแบบภาพที่หลากหลาย รวมถึง BMP, PNG, GIF และอื่นๆ

### คำถามที่ 4: Aspose.Imaging สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 ตอบ 4: ได้ คุณสามารถลองใช้ Aspose.Imaging สำหรับ Java ได้ด้วยการทดลองใช้ฟรี รับมัน[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะขอความช่วยเหลือหรือสนับสนุน Aspose.Imaging สำหรับ Java ได้ที่ไหน

 A5: หากคุณมีคำถามหรือต้องการความช่วยเหลือ โปรดไปที่ฟอรัมสนับสนุน Aspose.Imaging for Java[ที่นี่](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
