---
date: '2026-11-04'
description: เรียนรู้วิธีสร้าง animated PNG ใน Java ด้วยใบอนุญาต Aspose Imaging, เพิ่ม
  dependency ของ Maven, แปลง TIFF เป็น APNG และบันทึกภาพ
keywords:
- aspose imaging license
- convert tiff to apng
- tiff to png conversion
- add maven dependency java
- control animation speed java
lastmod: '2026-11-04'
og_description: เรียนรู้วิธีสร้าง animated PNG ใน Java ด้วยใบอนุญาต Aspose Imaging,
  เพิ่ม dependency ของ Maven, แปลง TIFF เป็น APNG และควบคุมความเร็วของแอนิเมชัน
og_image_alt: Guide showing how to generate animated PNGs in Java with Aspose Imaging
og_title: สร้าง animated PNG ใน Java ด้วยใบอนุญาต Aspose Imaging
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to create animated PNG in Java with an Aspose Imaging license,
    add the Maven dependency, convert TIFF to APNG and save the image.
  headline: Create animated PNG in Java using an Aspose Imaging license
  type: TechArticle
- description: Learn how to create animated PNG in Java with an Aspose Imaging license,
    add the Maven dependency, convert TIFF to APNG and save the image.
  name: Create animated PNG in Java using an Aspose Imaging license
  steps:
  - name: '**Web development** – Animated banners, icons, or loading spinners that
      work across browsers without needing GIF support.'
    text: '**Web development** – Animated banners, icons, or loading spinners that
      work across browsers without needing GIF support.'
  - name: '**Desktop applications** – Enrich Swing or JavaFX UI components with subtle
      motion cues.'
    text: '**Desktop applications** – Enrich Swing or JavaFX UI components with subtle
      motion cues.'
  - name: '**Data visualization** – Animate chart transitions or step‑by‑step walkthroughs
      for reports.'
    text: '**Data visualization** – Animate chart transitions or step‑by‑step walkthroughs
      for reports.'
  type: HowTo
- questions:
  - answer: You must set the value yourself with `setDefaultFrameTime(int ms)`; there
      is no hidden default.
    question: What is the default frame duration for APNG using Aspose.Imaging?
  - answer: Yes—load the file, modify the frame timings via `ApngOptions`, and save
      it again.
    question: Can I adjust animation speed in an existing APNG file?
  - answer: Ensure the image path is correct, allocate enough heap memory for large
      files, and use `try‑with‑resources` to release resources promptly.
    question: What are common pitfalls when loading images with Aspose.Imaging?
  - answer: Visit [Aspose's download page](https://releases.aspose.com/imaging/java/)
      to request a trial.
    question: How do I obtain a free trial license for Aspose.Imaging?
  - answer: Absolutely—you can combine it with Spring, Apache Commons, or any UI framework
      such as JavaFX.
    question: Is Aspose.Imaging compatible with other Java libraries?
  type: FAQPage
tags:
- aspose imaging
- animated png java
- tiff conversion
- maven dependency
- java image processing
title: สร้าง animated PNG ใน Java ด้วยใบอนุญาต Aspose Imaging
url: /th/java/animation-multi-frame-images/aspose-imaging-java-animated-png-guide/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้างไฟล์ PNG แบบเคลื่อนไหวใน Java ด้วยลิขสิทธิ์ Aspose Imaging

## บทนำ

หากคุณต้องการ **สร้างไฟล์ PNG แบบเคลื่อนไหวใน Java** และต้องการโซลูชันที่เชื่อถือได้พร้อมใช้งานในระดับการผลิต, **ลิขสิทธิ์ Aspose Imaging** จะให้การเข้าถึง API ที่มีประสิทธิภาพสูงของไลบรารีอย่างเต็มที่ ไม่ว่าคุณจะกำลังสร้างพอร์ทัลเว็บ, UI บนเดสก์ท็อป, หรือแดชบอร์ดการแสดงผลข้อมูล, PNG แบบเคลื่อนไหว (APNG) จะเพิ่มการเคลื่อนไหวที่ราบรื่นโดยไม่มีข้อเสียของ GIFs บทแนะนำนี้จะพาคุณผ่านการเพิ่ม dependency ของ Maven, การแปลงไฟล์ TIFF หลายหน้าเป็น APNG, และการควบคุมเวลาเฟรม, เพื่อให้คุณสามารถส่งมอบแอนิเมชันที่ดูเป็นมืออาชีพได้อย่างรวดเร็ว

## คำตอบสั้น
- **ไลบรารีใดที่ทำให้สามารถสร้าง APNG ใน Java ได้?** Aspose.Imaging พร้อมกับ dependency ของ Aspose Imaging Maven.  
- **รูปแบบใดที่สามารถแปลงเป็น APNG ได้?** ไฟล์ TIFF หลายหน้าสามารถแปลงเป็น PNG แบบเคลื่อนไหวได้.  
- **ฉันจะควบคุมความเร็วของแอนิเมชันได้อย่างไร?** ตั้งค่า `ApngOptions.setDefaultFrameTime(milliseconds)`.  
- **ต้องการลิขสิทธิ์สำหรับการผลิตหรือไม่?** ใช่—ลิขสิทธิ์ Aspose Imaging จะลบข้อจำกัดของรุ่นทดลองและเปิดใช้งานฟีเจอร์ทั้งหมด.  
- **สามารถใช้ Maven หรือ Gradle ได้หรือไม่?** รองรับทั้งสอง; เพียงเพิ่ม dependency ที่เหมาะสม.

## ลิขสิทธิ์ Aspose Imaging คืออะไร?

**ลิขสิทธิ์ Aspose Imaging** คือไฟล์ที่ปลดล็อกชุดฟีเจอร์เต็มรูปแบบของไลบรารี Aspose.Imaging for Java, ทำให้ไม่มีลายน้ำรุ่นทดลองและไม่มีการจำกัดการใช้งาน คุณโหลดลิขสิทธิ์ครั้งเดียวเมื่อแอปพลิเคชันเริ่มทำงาน, และการเรียก API ทั้งหมดต่อจากนั้นจะทำงานโดยไม่มีข้อจำกัดของรุ่นทดลอง

## ทำไมต้องใช้ Aspose.Imaging สำหรับ APNG?

Aspose.Imaging รองรับ **รูปภาพกว่า 150 รูปแบบ** (รวมถึง JPEG, PNG, TIFF, BMP, และ WebP) และสามารถจัดการเอกสารหลายร้อยหน้าได้โดยคงการใช้หน่วยความจำต่ำกว่า 200 MB บน JVM 8 GB ปกติ ตัวเข้ารหัส APNG ของไลบรารีนี้รักษาความโปร่งใส, ความลึกสีเต็ม, และการตั้งค่าเวลาแต่ละเฟรมโดยไม่ต้องใช้เครื่องมือภายนอก, ทำให้เป็นตัวเลือกที่เร็วที่สุดและเชื่อถือได้ที่สุดสำหรับนักพัฒนา Java

## ข้อกำหนดเบื้องต้น
- ติดตั้ง Java 8 หรือสูงกว่า.  
- IDE เช่น IntelliJ IDEA หรือ Eclipse.  
- Maven หรือ Gradle สำหรับการจัดการ dependency (หรือไฟล์ JAR).  

## การเพิ่ม dependency ของ Maven สำหรับ Aspose Imaging

### Maven

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

สำหรับผู้ที่ต้องการดาวน์โหลดโดยตรง, คุณสามารถรับเวอร์ชันล่าสุดจาก [หน้าดาวน์โหลดของ Aspose](https://releases.aspose.com/imaging/java/). คุณยังสามารถเยี่ยมชม [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) เพื่อดูบันทึกการปล่อยเวอร์ชัน

## การจัดหาใบอนุญาต

เพื่อปลดล็อกชุดฟีเจอร์เต็มโดยไม่มีข้อจำกัดของรุ่นทดลอง:

- **ทดลองฟรี:** เริ่มต้นด้วยการทดลองฟรีเพื่อทดสอบฟังก์ชัน.  
- **ลิขสิทธิ์ชั่วคราว:** รับลิขสิทธิ์ชั่วคราวเพื่อเข้าถึงระยะยาวระหว่างการพัฒนา.  
- **ซื้อ:** สำหรับการใช้งานระยะยาว, ซื้อใบอนุญาตเชิงพาณิชย์.

เริ่มต้นลิขสิทธิ์ในโค้ดของคุณ:

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path/to/your/license/file.lic");
```

`License` โหลดไฟล์ลิขสิทธิ์ Aspose.Imaging เพื่อปลดล็อกฟีเจอร์ทั้งหมด

## วิธีแปลง TIFF เป็น APNG ด้วย Aspose.Imaging?

โหลด TIFF ต้นฉบับ, ตั้งค่า APNG options, และบันทึกผลลัพธ์ ไลบรารีจะดึงแต่ละหน้าของ TIFF เป็นเฟรมแยกและเขียนเป็น PNG แบบเคลื่อนไหวที่เป็นมาตรฐาน กระบวนการนี้ยังอนุญาตให้คุณตั้งค่าเวลาเฟรมเริ่มต้น, เลือกระดับการบีบอัด, และปรับขนาดเฟรมก่อนบันทึก, ให้คุณควบคุมคุณภาพแอนิเมชันและขนาดไฟล์ได้อย่างเต็มที่

### การโหลดภาพ

`Image` เป็นคลาสฐานที่แทนวัตถุภาพใน Aspose.Imaging

```java
import com.aspose.imaging.Image;
```

```java
String inputFilePath = "YOUR_DOCUMENT_DIRECTORY/img4.tif";

try (Image image = Image.load(inputFilePath)) {
    // The image is now loaded and ready for manipulation.
}
```

### การตั้งค่าเวลาเฟรมเริ่มต้นสำหรับ APNG

`ApngOptions` กำหนดการตั้งค่าสำหรับการบันทึกภาพเป็น PNG แบบเคลื่อนไหว

```java
import com.aspose.imaging.imageoptions.ApngOptions;
```

```java
ApngOptions op = new ApngOptions();
op.setDefaultFrameTime(500); // Default frame time set to 500 milliseconds
```

### การบันทึกภาพเป็น APNG

เตรียมเส้นทางไฟล์ผลลัพธ์และเรียก `save` พร้อมตัวเลือกที่กำหนด:

```java
String outputFilePath = "YOUR_OUTPUT_DIRECTORY/img4.tif.500ms.png";
```

```java
try (Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/img4.tif")) {
    ApngOptions op = new ApngOptions();
    op.setDefaultFrameTime(500); // Frame time set to 500 ms
    
    image.save(outputFilePath, op);
}
```

บรรทัด `image.save(outputFilePath, op);` **บันทึกภาพเป็น APNG**. ตรวจสอบให้แน่ใจว่าไฟล์ผลลัพธ์ลงท้ายด้วย `.png` และ `ApngOptions` สะท้อนเวลาฟรมที่คุณต้องการ

## วิธีบันทึกภาพเป็น APNG ใน Java?

เรียก `image.save` พร้อมอินสแตนซ์ `ApngOptions` ที่ระบุเวลาเฟรมเริ่มต้น ปรับ `setDefaultFrameTime` เพื่อเร่งหรือชะลอแอนิเมชัน, และคุณสามารถใช้การเรียกเดียวกันนี้กับรูปแบบแหล่งอื่น ๆ เช่น PDF หลายหน้า ใช้บล็อก `try‑with‑resources` เพื่อให้ทรัพยากรภาพถูกปล่อยอย่างรวดเร็ว, ป้องกันการรั่วของหน่วยความจำระหว่างการประมวลผลเป็นชุด

## การใช้งานเชิงปฏิบัติ
1. **การพัฒนาเว็บ** – แบนเนอร์, ไอคอน, หรือสปินเนอร์โหลดที่ทำงานข้ามเบราว์เซอร์โดยไม่ต้องพึ่งพา GIF.  
2. **แอปพลิเคชันเดสก์ท็อป** – เพิ่มความเคลื่อนไหวอ่อนโยนให้กับคอมโพเนนท์ Swing หรือ JavaFX.  
3. **การแสดงผลข้อมูล** – ทำแอนิเมชันการเปลี่ยนแปลงแผนภูมิหรือขั้นตอนการสาธิตรายงาน.

ผสาน Aspose.Imaging กับไลบรารีเช่น Swing, JavaFX, หรือ Spring Boot เพื่อมอบประสบการณ์ผู้ใช้ที่ราบรื่น

## พิจารณาด้านประสิทธิภาพ
- **ปรับขนาดอย่างชาญฉลาด:** ความละเอียดที่ใหญ่ขึ้นเพิ่มการใช้หน่วยความจำ; ลดขนาดเมื่อเป็นไปได้.  
- **ปล่อยทรัพยากรทันที:** ใช้ `try‑with‑resources` (ตามตัวอย่าง) เพื่อปล่อยทรัพยากรเนทีฟ.  
- **การประมวลผลเป็นชุด:** ใช้อินสแตนซ์ `License` เพียงหนึ่งครั้งและหลีกเลี่ยงการโหลดไฟล์ต้นฉบับซ้ำเมื่อสร้าง APNG จำนวนมาก.

## ปัญหาที่พบบ่อยและวิธีแก้
| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| **OutOfMemoryError** ขณะโหลด TIFF ขนาดใหญ่ | ภาพใหญ่เกินขนาด heap ของ JVM | เพิ่มค่า `-Xmx` หรือปรับขนาดภาพก่อนประมวลผล |
| **เฟรมสีขาว** ใน APNG ที่ได้ | หน้า TIFF มีขนาดต่างกัน | ปรับขนาดทุกหน้าให้เท่ากันก่อนบันทึก |
| **ลิขสิทธิ์ไม่ทำงาน** | เส้นทางไฟล์ลิขสิทธิ์ไม่ถูกต้อง | ตรวจสอบเส้นทางและให้แน่ใจว่าไฟล์สามารถอ่านได้ใน runtime |

## คำถามที่พบบ่อย

**ถาม: เวลาเฟรมเริ่มต้นของ APNG ใน Aspose.Imaging คือเท่าไหร่?**  
ตอบ: คุณต้องตั้งค่าด้วยตนเองโดยใช้ `setDefaultFrameTime(int ms)`; ไม่มีค่าเริ่มต้นที่ซ่อนอยู่

**ถาม: สามารถปรับความเร็วของแอนิเมชันในไฟล์ APNG ที่มีอยู่ได้หรือไม่?**  
ตอบ: ได้—โหลดไฟล์, แก้ไขเวลาเฟรมผ่าน `ApngOptions`, แล้วบันทึกใหม่

**ถาม: ข้อผิดพลาดทั่วไปเมื่อโหลดภาพด้วย Aspose.Imaging มีอะไรบ้าง?**  
ตอบ: ตรวจสอบให้แน่ใจว่าเส้นทางภาพถูกต้อง, จัดสรร heap เพียงพอสำหรับไฟล์ขนาดใหญ่, และใช้ `try‑with‑resources` เพื่อปล่อยทรัพยากรอย่างทันท่วงที

**ถาม: จะขอรับลิขสิทธิ์ทดลองฟรีสำหรับ Aspose.Imaging ได้อย่างไร?**  
ตอบ: เยี่ยมชม [หน้าดาวน์โหลดของ Aspose](https://releases.aspose.com/imaging/java/) เพื่อขอทดลอง

**ถาม: Aspose.Imaging เข้ากันได้กับไลบรารี Java อื่นหรือไม่?**  
ตอบ: แน่นอน—คุณสามารถผสานกับ Spring, Apache Commons, หรือเฟรมเวิร์ก UI ใด ๆ เช่น JavaFX

## แหล่งข้อมูล

- **เอกสาร:** [Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)  
- **ดาวน์โหลด:** [Latest Release Download](https://releases.aspose.com/imaging/java/)  
- **ซื้อ:** [Buy Aspose.Imaging](https://purchase.aspose.com/buy)  
- **ทดลองฟรี:** [Get Started with Free Trial](https://releases.aspose.com/imaging/java/)  
- **ลิขสิทธิ์ชั่วคราว:** [Acquire Temporary License](https://purchase.aspose.com/temporary-license/)  
- **ฟอรั่มสนับสนุน:** [Aspose Community Support](https://forum.aspose.com/c/imaging/14)

---

**อัปเดตล่าสุด:** 2026-11-04  
**ทดสอบด้วย:** Aspose.Imaging 25.5 for Java  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [วิธีสร้าง GIF แบบเคลื่อนไหวด้วย Aspose.Imaging Java: การควบคุมเฟรมและลูป](/imaging/java/animation-multi-frame-images/gif-manipulation-java-aspose-imaging-guide/)
- [วิธีสร้าง TIFF หลายหน้าด้วย Aspose.Imaging for Java – คู่มือฉบับสมบูรณ์](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [ประมวลผล TIFF หลายเฟรมใน Java ด้วย Aspose.Imaging](/imaging/java/animation-multi-frame-images/java-aspose-imaging-multi-frame-tiff-processing/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}