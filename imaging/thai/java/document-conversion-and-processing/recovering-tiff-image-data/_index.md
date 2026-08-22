---
date: 2026-05-18
description: คู่มือขั้นตอนการกู้คืนภาพ TIFF ด้วย Aspose.Imaging for Java, การกู้คืนข้อมูลภาพที่เสียอย่างรวดเร็วและเชื่อถือได้
keywords:
- how to recover tiff
- fix broken tiff
- recover corrupted tiff
- restore damaged tiff
linktitle: การกู้คืนข้อมูลภาพ TIFF
schemas:
- author: Aspose
  dateModified: '2026-05-18'
  description: Step-by-step guide on how to recover TIFF images using Aspose.Imaging
    for Java, restoring damaged image data quickly and reliably.
  headline: How to Recover TIFF Images with Aspose.Imaging for Java
  type: TechArticle
- description: Step-by-step guide on how to recover TIFF images using Aspose.Imaging
    for Java, restoring damaged image data quickly and reliably.
  name: How to Recover TIFF Images with Aspose.Imaging for Java
  steps:
  - name: Define the Document Directory
    text: Specify where the TIFF file lives on disk. Replace the placeholder with
      the actual folder on your machine.
  - name: Create LoadOptions
    text: '`DataRecoveryMode` enum defines how Aspose.Imaging attempts to reconstruct
      corrupted data. - `DataRecoveryMode.ConsistentRecover` – Attempts to reconstruct
      the image while preserving as much original data as possible. - `Color.getRed()`
      – Fills gaps with red; you can change this to any color that su'
  - name: Load the Damaged Image
    text: '`Image` (or its subclass `TiffImage`) represents the in‑memory TIFF after
      loading. Inside the block you could save the recovered image, apply further
      processing, or simply inspect its properties.'
  type: HowTo
- questions:
  - answer: The background color fills pixels that cannot be reconstructed, making
      damaged areas instantly visible and preserving a consistent visual output.
    question: What is the significance of setting the background color in data recovery?
  - answer: Yes – the library supports JPEG, PNG, BMP, PSD, RAW, and 150+ other formats.
      The same recovery workflow applies; just change the file extension.
    question: Can I recover other image formats apart from TIFF using Aspose.Imaging
      for Java?
  - answer: Recovery depends on corruption severity and available RAM. Aspose.Imaging
      can handle multi‑hundred‑page TIFFs while keeping memory usage under 200 MB
      by streaming data instead of loading the whole file.
    question: Is there a limit to the size of the TIFF image that can be recovered?
  - answer: Absolutely. The API includes resizing, cropping, filtering, format conversion,
      and metadata editing, allowing you to both recover and enhance images in a single
      pipeline.
    question: Are there additional image‑manipulation tools within Aspose.Imaging
      for Java?
  - answer: Yes – a commercial license is required for production deployments. You
      can obtain a license **[here](https://purchase.aspose.com/buy)**.
    question: Can I use Aspose.Imaging for Java in commercial projects?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: วิธีกู้คืนภาพ TIFF ด้วย Aspose.Imaging for Java
url: /th/java/document-conversion-and-processing/recovering-tiff-image-data/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# วิธีกู้คืนภาพ TIFF ด้วย Aspose.Imaging for Java

เมื่อคุณต้องการ **วิธีกู้คืน tiff** ไฟล์ที่ไม่สามารถอ่านได้อีกต่อไป คุณไม่จำเป็นต้องเริ่มจากศูนย์ ไม่ว่าคุณจะทำงานกับภาพถ่ายความละเอียดสูง เอกสารสแกนเก่า หรือเอกสารหลายหน้าขนาดใหญ่ Aspose.Imaging for Java ให้โซลูชันแบบ pure‑Java ที่ไม่มีการพึ่งพา native สามารถอ่านสตรีมที่เสียหาย สร้างข้อมูลพิกเซลที่หายไปใหม่ และให้ภาพที่ใช้งานได้เพียงไม่กี่บรรทัดของโค้ด ในคู่มือนี้เราจะเดินผ่านขั้นตอนการกู้คืนทั้งหมด อธิบายว่าทำไมไลบรารีนี้ถึงเป็นตัวเลือกที่เชื่อถือได้ที่สุด และแสดงวิธีปรับแต่งกระบวนการให้เหมาะกับโครงการของคุณ

## คำตอบสั้น
- **ต้องใช้ไลบรารีอะไร?** Aspose.Imaging for Java  
- **กู้คืน TIFF ที่เสียหายได้หรือไม่?** ได้ – ใช้ตัวเลือก `DataRecoveryMode` เพื่อสร้างภาพใหม่  
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานในโปรดักชันหรือไม่?** ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานที่ไม่ใช่ trial  
- **รองรับเวอร์ชัน Java ใด?** Java 8 หรือใหม่กว่า (เข้ากันได้กับ Java 21)  
- **สีพื้นหลังเป็นตัวเลือกหรือไม่?** ใช่ – คุณสามารถตั้งค่า `Color` ใดก็ได้ตามต้องการสำหรับพิกเซลที่ไม่สามารถกู้คืนได้  

## การกู้คืนภาพ TIFF คืออะไร?
การกู้คืนภาพ TIFF คือกระบวนการสร้างไฟล์ TIFF ที่เสียหายให้กลับมาเปิดและใช้งานได้อีกครั้ง  
เมื่อไฟล์ TIFF มีสตรีมที่เสียหายหรือแผ่นภาพหาย การกู้คืนจะอ่านข้อมูลที่เหลืออยู่ พยายามสร้างส่วนที่หายใหม่ และอาจเติมช่องว่างด้วยสีพื้นหลังที่ผู้ใช้กำหนด ซึ่งช่วยให้คุณสามารถกอบกู้ทรัพย์สินภาพที่มีค่าโดยไม่ต้องแก้ไขพิกเซลด้วยตนเอง  

## ทำไมต้องใช้ Aspose.Imaging for Java?
โหลดไฟล์ที่เสียหายด้วย Aspose.Imaging และรับโหมดการกู้คืนในตัว ไลบรารีรองรับรูปแบบกว่า 150 รูปแบบ (JPEG, PNG, BMP, PSD, RAW) และสามารถประมวลผล TIFF หลายร้อยหน้าโดยไม่ต้องโหลดเอกสารทั้งหมด ลดการใช้ heap สูงสุดถึง 70 % เมื่อเทียบกับวิธีแบบดั้งเดิม Pure Java หมายความว่าไม่มี DLL หรือการติดตั้งเฉพาะแพลตฟอร์ม เหมาะสำหรับเซิร์ฟเวอร์ข้ามแพลตฟอร์ม  

## วิธีกู้คืนภาพ TIFF ด้วย Aspose.Imaging for Java?
โหลด TIFF ที่เสียหายโดยใช้ `LoadOptions` ที่กำหนดไว้สำหรับการกู้คืนที่สอดคล้องกัน แล้วบันทึกผลลัพธ์ ขั้นตอนหลักคือ:
1. ตั้งค่าเส้นทางไฟล์  
2. สร้างอินสแตนซ์ `LoadOptions` เปิดใช้งาน `DataRecoveryMode.ConsistentRecover` และเลือกสีพื้นหลังสำหรับพิกเซลที่ไม่สามารถกู้คืนได้  
3. เปิดภาพภายในบล็อก `try‑with‑resources` เพื่อให้แน่ใจว่ามีการจัดการทรัพยากรอย่างเหมาะสม  
4. บันทึกภาพที่กู้คืนเป็นไฟล์ใหม่หรือดำเนินการต่อในหน่วยความจำ  

## ข้อกำหนดเบื้องต้น

- **Aspose.Imaging for Java** – ดาวน์โหลด JAR ล่าสุดจากเว็บไซต์อย่างเป็นทางการ **[ที่นี่](https://releases.aspose.com/imaging/java/)**  
- **สภาพแวดล้อมการพัฒนา Java** – JDK 8 หรือใหม่กว่า พร้อม Maven, Gradle หรือ IDE ที่คุณชื่นชอบ  

เมื่อเราครอบคลุมพื้นฐานแล้ว ให้ดำดิ่งสู่โค้ดจริง

## นำเข้าแพ็กเกจ

`DataRecoveryMode`, `Image`, `Color` และ `LoadOptions` เป็นคลาสหลักของ Aspose.Imaging ที่ใช้กำหนดค่าการกู้คืนและการจัดการภาพ  

```java
import com.aspose.imaging.DataRecoveryMode;
import com.aspose.imaging.Image;
import com.aspose.imaging.Color;
import com.aspose.imaging.LoadOptions;
```

## วิธีกู้คืนภาพ TIFF – ภาพรวม

ต่อไปนี้เราจะตั้งค่าเส้นทางไฟล์ กำหนดตัวเลือกการกู้คืน และสุดท้ายโหลด TIFF ที่เสียหาย แต่ละขั้นตอนอธิบายด้วยภาษาง่าย ๆ เพื่อให้คุณปรับใช้กับโครงการของตนเองได้

### ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอกสาร

ระบุที่ตั้งของไฟล์ TIFF บนดิสก์ แทนที่ตัวแปร placeholder ด้วยโฟลเดอร์จริงบนเครื่องของคุณ  

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
```

### ขั้นตอนที่ 2: สร้าง LoadOptions

enum `DataRecoveryMode` กำหนดวิธีที่ Aspose.Imaging พยายามสร้างข้อมูลที่เสียหายใหม่  

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setDataRecoveryMode(DataRecoveryMode.ConsistentRecover);
loadOptions.setDataBackgroundColor(Color.getRed());
```

- `DataRecoveryMode.ConsistentRecover` – พยายามสร้างภาพใหม่โดยรักษาข้อมูลเดิมให้มากที่สุดเท่าที่เป็นไปได้  
- `Color.getRed()` – เติมช่องว่างด้วยสีแดง; คุณสามารถเปลี่ยนเป็นสีใดก็ได้ตามกระบวนการทำงานของคุณ  

### ขั้นตอนที่ 3: โหลดภาพที่เสียหาย

`Image` (หรือคลาสย่อย `TiffImage`) แทนภาพ TIFF ที่อยู่ในหน่วยความจำหลังจากโหลด  

```java
try (Image image = Image.load(dataDir + "SampleTiff1.tiff", loadOptions)) {
    // Do some work on the recovered image
}
```

ภายในบล็อกนี้คุณสามารถบันทึกภาพที่กู้คืน, ทำการประมวลผลต่อ, หรือเพียงแค่ตรวจสอบคุณสมบัติต่าง ๆ  

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|--------|
| **OutOfMemoryError** | TIFF ขนาดใหญ่มากเกินกว่าที่ heap จะรับได้ | เพิ่มค่า JVM `-Xmx` หรือประมวลผลภาพเป็นแผ่นย่อย |
| **ไม่มีข้อมูลที่กู้คืน** | ไฟล์เสียหายอย่างรุนแรงเกินโหมดการกู้คืนที่เลือก | ลองใช้ `DataRecoveryMode.PartialRecover` หรือใช้สำเนาสำรอง |
| **สีพื้นหลังไม่ตรง** | สีเริ่มต้นอาจผสมกับภาพ | เรียก `loadOptions.setDataBackgroundColor(Color.getWhite())` หรือกำหนด `Color` ใดก็ได้ตามต้องการ |

## คำถามที่พบบ่อย

**ถาม: ความสำคัญของการตั้งค่าสีพื้นหลังในการกู้คืนข้อมูลคืออะไร?**  
ตอบ: สีพื้นหลังเติมพิกเซลที่ไม่สามารถสร้างใหม่ได้ ทำให้พื้นที่เสียหายปรากฏชัดเจนและรักษาความสอดคล้องของผลลัพธ์ภาพ

**ถาม: สามารถกู้คืนรูปแบบภาพอื่นนอกจาก TIFF ด้วย Aspose.Imaging for Java ได้หรือไม่?**  
ตอบ: ได้ – ไลบรารีรองรับ JPEG, PNG, BMP, PSD, RAW และรูปแบบอื่นกว่า 150 รูปแบบ กระบวนการกู้คืนเหมือนกัน เพียงเปลี่ยนนามสกุลไฟล์

**ถาม: มีขีดจำกัดขนาดของภาพ TIFF ที่สามารถกู้คืนได้หรือไม่?**  
ตอบ: การกู้คืนขึ้นอยู่กับระดับความเสียหายและ RAM ที่มี Aspose.Imaging สามารถจัดการ TIFF หลายร้อยหน้าโดยใช้หน่วยความจำต่ำกว่า 200 MB ด้วยการสตรีมข้อมูลแทนการโหลดทั้งหมด

**ถาม: มีเครื่องมือการจัดการภาพเพิ่มเติมใน Aspose.Imaging for Java หรือไม่?**  
ตอบ: มีแน่นอน API มีฟังก์ชันการปรับขนาด, ครอบ, ฟิลเตอร์, แปลงรูปแบบ, และแก้ไขเมตาดาต้า ช่วยให้คุณกู้คืนและปรับปรุงภาพในขั้นตอนเดียว

**ถาม: สามารถใช้ Aspose.Imaging for Java ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
ตอบ: ได้ – ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในโปรดักชัน คุณสามารถรับลิขสิทธิ์ **[ที่นี่](https://purchase.aspose.com/buy)**

**ถาม: วิธีบันทึกภาพที่กู้คืนเป็นไฟล์ใหม่คืออะไร?**  
ตอบ: หลังจากโหลดแล้วเรียก `image.save("RecoveredImage.tiff");` ภายในบล็อก `try` คุณยังสามารถบันทึกเป็นรูปแบบอื่นเช่น PNG โดยเปลี่ยนนามสกุลไฟล์ได้

## สรุป

การกู้คืนข้อมูลภาพ TIFF มีความสำคัญสำหรับผู้ที่จัดการกราฟิกความละเอียดสูงหรือเอกสารเก่า ด้วยการใช้ `DataRecoveryMode` ของ Aspose.Imaging for Java พร้อมตัวเลือกสีพื้นหลังที่ปรับได้ คุณสามารถฟื้นฟูไฟล์ที่เสียหายด้วยโค้ดสั้น ๆ และไม่มีการพึ่งพา native ใช้ขั้นตอนข้างต้นเป็นแม่แบบ ปรับเส้นทางและสีให้ตรงกับกระบวนการทำงานของคุณ เพื่อให้ทรัพย์สินภาพของคุณปลอดภัยและพร้อมใช้งานต่อไป

---

**อัปเดตล่าสุด:** 2026-05-18  
**ทดสอบด้วย:** Aspose.Imaging for Java 24.11 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทเรียนที่เกี่ยวข้อง

- [บีบอัดภาพ TIFF ใน Java ด้วย Aspose.Imaging: คู่มือการบีบอัด LZW](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [รวมภาพ TIFF ใน Java ด้วย Aspose.Imaging: คู่มือฉบับสมบูรณ์](/imaging/java/format-specific-operations/concatenate-tiff-images-java-aspose-imaging/)
- [การประมวลผลภาพ TIFF ขั้นสูงใน Java ด้วย Aspose.Imaging](/imaging/java/format-specific-operations/mastering-tiff-image-processing-java-aspose-imaging/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}