---
date: 2026-05-03
description: เรียนรู้วิธีตัดภาพด้วย Aspose.Imaging สำหรับ Java รวมถึงการตัดแบบสี่เหลี่ยมและการขยายแคนวาส
  คู่มือขั้นตอนต่อขั้นตอนสำหรับนักพัฒนา
keywords:
- how to crop image
- crop and expand image
- aspose imaging crop
- java image processing tutorial
- expand image canvas java
linktitle: การขยายภาพหรือการตัดภาพ
second_title: Aspose.Imaging Java Image Processing API
title: วิธีตัดภาพเป็นสี่เหลี่ยมโดยใช้ Aspose.Imaging สำหรับ Java
url: /th/java/document-conversion-and-processing/image-expansion-or-cropping/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# วิธีตัดรูปภาพเป็นสี่เหลี่ยมผืนผ้าด้วย Aspose.Imaging สำหรับ Java

## คำตอบด่วน
- **ไลบรารีที่ดีที่สุดสำหรับการตัดรูปภาพใน Java คืออะไร?** Aspose.Imaging for Java.  
- **ฉันสามารถตัดเป็นสี่เหลี่ยมผืนผ้าตามต้องการได้หรือไม่?** ใช่ – กำหนดค่า X, Y, ความกว้าง, และความสูงได้ตามต้องการ.  
- **ฉันต้องมีลิขสิทธิ์สำหรับการพัฒนาหรือไม่?** ทดลองใช้ฟรีสำหรับการทดสอบ; ต้องมีลิขสิทธิ์สำหรับการใช้งานจริง.  
- **การขยายแคนวาสของรูปภาพเป็นไปได้หรือไม่?** แน่นอน – สามารถเพิ่มขนาดแคนวาสก่อนตัดได้.  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 และใหม่กว่า.

## “crop image to rectangle” คืออะไร?
การตัดรูปภาพเป็นสี่เหลี่ยมผืนผ้าหมายถึงการสกัดส่วนย่อยของบิตแมปต้นฉบับโดยกำหนดพื้นที่สี่เหลี่ยม (X‑offset, Y‑offset, ความกว้าง, ความสูง). ส่วนที่เหลือของรูปภาพจะถูกละทิ้ง ทำให้ได้รูปภาพใหม่ที่เล็กลงและมีเฉพาะพื้นที่ที่ต้องการเท่านั้น.

## ทำไมต้องใช้ Aspose.Imaging สำหรับ Java?
- **ไม่มีการพึ่งพาภายนอก** – pure Java, works on any platform.  
- **รองรับรูปแบบไฟล์หลายประเภท** – JPEG, PNG, BMP, TIFF, and more.  
- **แคชประสิทธิภาพสูง** – `cacheData()` reduces I/O overhead.  
- **API ง่าย** – one‑line calls for loading, defining a rectangle, and saving.

## ข้อกำหนดเบื้องต้น
- **สภาพแวดล้อมการพัฒนา Java** – JDK 8+ installed and configured.  
- **Aspose.Imaging for Java** – download from the [website](https://releases.aspose.com/imaging/java/).  
- **ความรู้พื้นฐาน Java** – familiarity with classes, try‑with‑resources, and file paths.  
- **รูปภาพสำหรับทำงาน** – any JPEG/PNG you’d like to crop or expand.

## การนำเข้าแพ็กเกจ
ก่อนอื่น ให้ชี้โค้ดไปยังโฟลเดอร์ที่เก็บรูปภาพต้นฉบับของคุณ โค้ดส่วนนี้จะคงเดิมเหมือนในบทแนะนำต้นฉบับ.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

แทนที่ `"Your Document Directory"` ด้วยเส้นทางเต็มบนเครื่องของคุณ.

## ขั้นตอนที่ 1: โหลดรูปภาพ
การโหลดรูปภาพเป็นพื้นฐานสำหรับการปรับแต่งใด ๆ เรายังเรียก `cacheData()` เพื่อเก็บบิตแมปในหน่วยความจำสำหรับการดำเนินการต่อไปที่เร็วขึ้น.

```java
try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
{
    rasterImage.cacheData();
}
```

> **เคล็ดลับ:** ใช้บล็อก `try‑with‑resources` (ตามที่แสดง) เพื่อให้แน่ใจว่ารูปภาพจะถูกปิดโดยอัตโนมัติ ป้องกันการรั่วไหลของหน่วยความจำ.

## ขั้นตอนที่ 2: กำหนดพื้นที่สำหรับการตัด
ที่นี่เราจะสร้าง `Rectangle` ที่แสดงถึงพื้นที่ที่ต้องการเก็บไว้ สี่เหลี่ยมอาจเริ่มนอกขอบเขตเดิม – Aspose.Imaging จะขยายแคนวาสโดยอัตโนมัติ (มีประโยชน์สำหรับสถานการณ์ **expand image canvas java**).

```java
// Create an instance of Rectangle class and define X, Y, Width, and Height of the rectangle
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

- **X / Y** – ค่าติดลบจะเลื่อนสี่เหลี่ยมไปทางซ้าย/บน ทำให้แคนวาสขยายออก.  
- **Width / Height** – ขนาดของพื้นที่ที่ตัด.

## ขั้นตอนที่ 3: บันทึกรูปภาพที่ตัด (หรือขยาย)
สุดท้ายให้เขียนผลลัพธ์ลงดิสก์ วิธี `save` รับพาธปลายทาง, ตัวเลือกรูปแบบภาพ, และสี่เหลี่ยมที่กำหนดไว้.

```java
rasterImage.save("Your Document Directory" + "Grayscaling_out.jpg", new JpegOptions(), destRect);
```

ไฟล์ผลลัพธ์ `Grayscaling_out.jpg` ตอนนี้มีผลลัพธ์ของ **crop image to rectangle** หากสี่เหลี่ยมขยายเกินขอบภาพเดิม พื้นที่ส่วนเกินจะเติมด้วยพื้นหลังค่าเริ่มต้น (โปร่งใสสำหรับ PNG, สีดำสำหรับ JPEG).

## วิธีตัดรูปภาพด้วย Aspose.Imaging สำหรับ Java
ส่วนนี้สรุปขั้นตอนหลักในรูปแบบเช็คลิสต์สั้น ๆ เพื่อให้คุณอ้างอิงได้อย่างรวดเร็วขณะเขียนโค้ด:

1. **ตั้งค่าไดเรกทอรีข้อมูล** – ชี้ไปยังโฟลเดอร์ที่มีรูปภาพต้นฉบับ.  
2. **โหลดรูปภาพ** ด้วย `Image.load()` และเรียก `cacheData()`.  
3. **สร้าง `Rectangle`** ที่กำหนดพื้นที่ตัด (หรือการขยายแคนวาส).  
4. **บันทึก** รูปภาพใหม่โดยใช้ `rasterImage.save()` และส่งสี่เหลี่ยมที่กำหนด.

## การตัดและขยายรูปภาพ – กรณีใช้งานจริง
| สถานการณ์ | เหตุผลที่สำคัญ |
|----------|----------------|
| **การสร้างภาพย่อ** | ดึงส่วนกลางอย่างรวดเร็วเพื่อให้ได้ขนาดที่สม่ำเสมอ. |
| **การตัดรูปภาพโปรไฟล์ผู้ใช้** | บังคับให้มีพื้นที่อวาตาร์เป็นสี่เหลี่ยมหรือสี่เหลี่ยมผืนผ้า. |
| **การขยายแคนวาสก่อนเพิ่มลายน้ำ** | เพิ่มพื้นที่รอบรูปภาพโดยไม่ทำให้รูปเดิมบิดเบือน. |
| **การประมวลผลชุดของเอกสารสแกน** | ตัดขอบกระดาษออกในครั้งเดียว. |

## การแก้ไขปัญหา & เคล็ดลับ
- **รูปภาพไม่โหลด?** ตรวจสอบเส้นทางไฟล์และให้แน่ใจว่ารูปแบบรูปภาพได้รับการสนับสนุน.  
- **ขอบสีดำที่ไม่คาดคิดหลังการขยาย?** ตั้งค่าสีพื้นหลังใน `JpegOptions` หรือใช้ PNG เพื่อความโปร่งใส.  
- **กังวลเรื่องประสิทธิภาพกับรูปภาพขนาดใหญ่?** เพิ่มขนาด heap ของ Java (`-Xmx`) หรือประมวลผลรูปภาพเป็นชุดเล็ก ๆ.  
- **ข้อผิดพลาดทั่วไป:** ลืมเรียก `cacheData()` อาจทำให้ I/O ช้าลงในการดำเนินการต่อไป.

## คำถามที่พบบ่อย

**ถาม: Aspose.Imaging for Java รองรับรูปแบบภาพอะไรบ้าง?**  
A: JPEG, PNG, BMP, TIFF, GIF, ICO, PSD, และอื่น ๆ อีกมากมาย ดูเอกสารอย่างเป็นทางการสำหรับรายการทั้งหมด.

**ถาม: ฉันสามารถทำการปรับแต่งรูปภาพอื่น ๆ ด้วย Aspose.Imaging for Java ได้หรือไม่?**  
A: แน่นอน! การปรับขนาด การหมุน การกรอง และการแปลงรูปแบบทั้งหมดพร้อมใช้งาน.

**ถาม: Aspose.Imaging for Java เหมาะกับแอปพลิเคชันเว็บหรือไม่?**  
A: ใช่ ไลบรารีนี้ปลอดภัยต่อการทำงานหลายเธรดและทำงานได้ดีใน servlet containers และบริการ Spring Boot.

**ถาม: ฉันจะรับการสนับสนุนสำหรับ Aspose.Imaging for Java อย่างไร?**  
A: เยี่ยมชม [forum](https://forum.aspose.com/) เพื่อรับความช่วยเหลือจากชุมชน หรือเปิดตั๋วสนับสนุนพร้อมใบอนุญาตที่ถูกต้อง.

**ถาม: มีการทดลองใช้งานฟรีสำหรับ Aspose.Imaging for Java หรือไม่?**  
A: มี คุณสามารถสำรวจไลบรารีด้วยการทดลองใช้งานฟรี ดาวน์โหลดได้จาก [here](https://releases.aspose.com/).

## สรุป
คุณได้เรียนรู้ **วิธีตัดรูปภาพ** เป็นสี่เหลี่ยมผืนผ้าและแม้กระทั่ง **การขยายแคนวาสของรูปภาพ** ด้วย API ที่ทรงพลังของ Aspose.Imaging ด้วยการเชี่ยวชาญพื้นฐานเหล่านี้ คุณสามารถสร้างสายงานการประมวลผลภาพที่แข็งแรง ปรับปรุงความตอบสนองของ UI และมอบเนื้อหาภาพที่สวยงามในแอปพลิเคชัน Java ใด ๆ

---

**Last Updated:** 2026-05-03  
**Tested With:** Aspose.Imaging for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}