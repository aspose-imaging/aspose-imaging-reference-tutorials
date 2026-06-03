---
date: 2026-01-09
description: เรียนรู้วิธีเพิ่มลายน้ำลงในภาพด้วย Aspose.Imaging สำหรับ Java บทเรียนการประมวลผลภาพด้วย
  Java นี้แสดงขั้นตอนโดยละเอียดในการสร้างลายน้ำแนวทแยงอย่างรวดเร็ว.
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: วิธีเพิ่มลายน้ำ – การใส่ลายน้ำแบบทแยงบนภาพ (Java)
url: /th/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเพิ่มลายน้ำ – การใส่ลายน้ำภาพแบบทแยง (Java)

หากคุณกำลังมองหา **how to add watermark** ให้กับรูปภาพของคุณด้วยการจัดวางแบบทแยงที่สวยงาม Aspose.Imaging for Java ทำให้เป็นเรื่องง่าย ในบทแนะนำแบบขั้นตอนนี้ เราจะอธิบายการเพิ่มลายน้ำข้อความที่หมุน 45 องศาให้กับไฟล์ JPG (หรือไฟล์ที่รองรับ) คุณไม่จำเป็นต้องเป็นผู้เชี่ยวชาญ Java – แต่ละบล็อกอธิบายด้วยภาษาง่าย ๆ เพื่อให้คุณทำตามได้ในไม่กี่นาที.

## คำตอบด่วน
- **ไลบรารีที่ใช้คืออะไร?** Aspose.Imaging for Java  
- **คีย์เวิร์ดหลักที่ครอบคลุมคืออะไร?** how to add watermark  
- **รูปแบบภาพที่รองรับ?** JPEG, PNG, BMP, TIFF, GIF และอื่น ๆ  
- **ต้องใช้โค้ดเท่าไหร่?** มีเพียงเจ็ดบล็อกโค้ดสั้น ๆ  
- **ต้องการไลเซนส์สำหรับการทดสอบหรือไม่?** มีรุ่นทดลองฟรี; จำเป็นต้องมีไลเซนส์สำหรับการใช้งานจริง  

## “how to add watermark” คืออะไรในการประมวลผลภาพ?
การเพิ่มลายน้ำหมายถึงการวางข้อความหรือกราฟิกที่มีความโปร่งแสงบางส่วนบนภาพเพื่อปกป้องลิขสิทธิ์หรือสื่อแบรนด์ ลายน้ำแบบทแยงมีประสิทธิภาพเป็นพิเศษเพราะครอบคลุมภาพทั้งหมดและยากต่อการตัดออก.

## ทำไมต้องใช้ Aspose.Imaging for Java?
Aspose.Imaging ให้ API ระดับสูงที่ซ่อนการจัดการพิกเซลระดับล่าง, รองรับหลายสิบรูปแบบ, และทำงานบน Java runtime ใดก็ได้ มันทำให้คุณมุ่งเน้นที่ *สิ่งที่* ต้องการทำ—เช่นการเพิ่มลายน้ำแบบทแยง—โดยไม่ต้องกังวลเกี่ยวกับข้อแตกต่างของรูปแบบภาพ.

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่ม, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Aspose.Imaging for Java** – ดาวน์โหลดเวอร์ชันล่าสุดจากเว็บไซต์ทางการ **[here](https://releases.aspose.com/imaging/java/)**.  
2. **Java Development Environment** – JDK 8+ และ IDE ที่คุณชื่นชอบ (IntelliJ, Eclipse, VS Code, ฯลฯ).  
3. **An image to watermark** – วางไฟล์ JPG/TIFF/PNG ตัวอย่างในโฟลเดอร์ที่คุณจะอ้างอิงในโค้ด.

## นำเข้าแพ็กเกจ
ก่อนอื่น, นำเข้าคลาสที่คุณต้องการ การจัดกลุ่ม import ไว้ด้วยกันทำให้โค้ดอ่านง่ายและบำรุงรักษาง่ายขึ้น.

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## ขั้นตอนที่ 1: โหลดภาพที่มีอยู่
เราเริ่มด้วยการโหลดรูปภาพต้นฉบับ เมธอด `Image.load` จะตรวจจับรูปแบบโดยอัตโนมัติ.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **Pro tip:** ห่อวัตถุ `Image` ด้วย try‑with‑resources block (ตามที่แสดง) เพื่อให้มันถูกทำลายโดยอัตโนมัติ, ป้องกันการรั่วของหน่วยความจำ.

## ขั้นตอนที่ 2: เตรียมข้อความและกราฟิกลายน้ำ
สร้างอ็อบเจ็กต์ `Graphics` ที่เชื่อมต่อกับภาพที่โหลดและบันทึกขนาดภาพไว้สำหรับการคำนวณต่อไป.

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## ขั้นตอนที่ 3: กำหนดฟอนต์และแปรง
เลือกฟอนต์ที่โดดเด่นและแปรงที่กำหนดสีและความทึบของลายน้ำ ปรับความทึบเพื่อทำให้ลายน้ำเป็นกึ่งโปร่งแสง.

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## ขั้นตอนที่ 4: จัดรูปแบบข้อความของคุณ
ตั้งค่าการจัดแนวและแฟล็กการจัดรูปแบบเพื่อให้ข้อความอยู่กึ่งกลางเมื่อวาด.

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## ขั้นตอนที่ 5: ใช้การแปลง
เมทริกซ์การแปลงทำให้เราย้ายจุดเริ่มต้นไปยังศูนย์กลางของภาพและจากนั้นหมุนข้อความที่ ‑45° (ตามเข็มนาฬิกา).

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## ขั้นตอนที่ 6: วาดและบันทึก
สุดท้าย, เรนเดอร์สตริงลงบนภาพและบันทึกผลลัพธ์ลงดิสก์.

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

เมื่อคุณเปิดไฟล์ `AddDiagonalWatermarkToImage_out.jpg` คุณจะเห็นข้อความสีแดงกึ่งโปร่งแสงที่เอียงผ่านศูนย์กลางของภาพ.

## ปัญหาทั่วไปและวิธีแก้
| ปัญหา | สาเหตุ | วิธีแก้ |
|---------|--------|-----|
| ลายน้ำดูจางเกินไป | ตั้งค่าความทึบเป็น 0 (โปร่งใสเต็มที่) | เพิ่มความทึบ, เช่น `brush.setOpacity(0.5f);` |
| ข้อความถูกตัดที่ขอบ | การแปลตำแหน่งไม่อยู่กึ่งกลางสำหรับภาพที่ไม่เป็นสี่เหลี่ยมจัตุรัส | ใช้ `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` ตามที่แสดง, แล้วปรับมุมการหมุนหากจำเป็น |
| ข้อผิดพลาดรูปแบบภาพที่ไม่รองรับ | ใช้เวอร์ชัน Aspose.Imaging ที่เก่า | อัปเดตเป็นเวอร์ชันล่าสุดของ Aspose.Imaging |

## คำถามที่พบบ่อย

### Q1: Aspose.Imaging for Java เหมาะสำหรับผู้เริ่มต้นหรือไม่?
**A:** แน่นอน! API ใช้งานง่ายและเอกสารให้ตัวอย่างที่ชัดเจน แม้แต่ผู้พัฒนาที่ใหม่กับการประมวลผลภาพก็สามารถทำตามบทแนะนำนี้และสร้างผลลัพธ์ระดับมืออาชีพได้อย่างรวดเร็ว.

### Q2: ฉันสามารถปรับแต่งข้อความและสไตล์ของลายน้ำได้หรือไม่?
**A:** ได้. เปลี่ยนตัวแปร `theString`, เลือก `Font` อื่น, ปรับ `brush.setColor(...)`, หรือปรับมุมการหมุนในเมทริกซ์ให้สอดคล้องกับแบรนด์ของคุณ.

### Q3: Aspose.Imaging for Java รองรับรูปแบบภาพอื่น ๆ นอกจาก JPG หรือไม่?
**A:** ใช่. ไลบรารีทำงานกับ BMP, PNG, GIF, TIFF, PSD และอื่น ๆ อีกมากมาย เพียงชี้เมธอด `Image.load` ไปที่ไฟล์ที่ต้องการ.

### Q4: มีรุ่นทดลองฟรีสำหรับ Aspose.Imaging for Java หรือไม่?
**A:** มี, คุณสามารถทดลองใช้ Aspose.Imaging for Java ด้วยรุ่นทดลองฟรี ดาวน์โหลดได้ **[here](https://releases.aspose.com/)**.

### Q5: ฉันจะหาแนวทางช่วยเหลือหรือสนับสนุนสำหรับ Aspose.Imaging for Java ได้จากที่ไหน?
**A:** สำหรับคำถาม, รายงานบั๊ก, หรือคำแนะนำการปฏิบัติที่ดีที่สุด, เยี่ยมชมฟอรั่มสนับสนุน Aspose.Imaging for Java **[here](https://forum.aspose.com/)**.

---

**อัปเดตล่าสุด:** 2026-01-09  
**ทดสอบด้วย:** Aspose.Imaging for Java 24.11 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}