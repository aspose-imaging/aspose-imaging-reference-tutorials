---
date: '2026-07-08'
description: เรียนรู้วิธีส่งออก TIFF จาก DjVu ด้วย Aspose.Imaging สำหรับ Java คู่มือขั้นตอนเต็มที่ครอบคลุมการโหลด
  การเลือกหน้า และตัวเลือกการส่งออก
keywords:
- how to export tiff
- java image processing
- maven aspose imaging
- how to load djvu
lastmod: '2026-07-08'
og_description: ค้นพบวิธีส่งออก TIFF จาก DjVu ใน Java ด้วย Aspose.Imaging ปฏิบัติตามบทแนะนำขั้นตอนเต็มเพื่อการแปลงภาพที่เร็วและเชื่อถือได้
og_image_alt: Guide showing Java code to convert DjVu pages to TIFF with Aspose.Imaging
og_title: วิธีส่งออก TIFF – คู่มือ Java กับ Aspose.Imaging
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: Learn how to export TIFF from DjVu using Aspose.Imaging for Java. Step-by-step
    guide covering loading, page selection, and export options.
  headline: How to Export TIFF – Load and Export DjVu Pages in Java with Aspose.Imaging
  type: TechArticle
- description: Learn how to export TIFF from DjVu using Aspose.Imaging for Java. Step-by-step
    guide covering loading, page selection, and export options.
  name: How to Export TIFF – Load and Export DjVu Pages in Java with Aspose.Imaging
  steps:
  - name: '**Archival Systems** – Preserve scanned documents in a universally accepted
      format.'
    text: '**Archival Systems** – Preserve scanned documents in a universally accepted
      format.'
  - name: '**Document Review Workflows** – Pull out only the pages that need annotation.'
    text: '**Document Review Workflows** – Pull out only the pages that need annotation.'
  - name: '**Integration with DMS** – Feed TIFF images into existing document‑management
      pipelines that do not understand DjVu.'
    text: '**Integration with DMS** – Feed TIFF images into existing document‑management
      pipelines that do not understand DjVu.'
  type: HowTo
- questions:
  - answer: '`DjvuImage` represents a DjVu document in memory.'
    question: What is the main class for DjVu handling?
  - answer: Just two lines after loading the image.
    question: How many lines of code are needed to export a page to TIFF?
  - answer: '`com.aspose:aspose-imaging` (version 25.5+).'
    question: Which Maven artifact provides DjVu support?
  - answer: Yes, use `IntRange` to specify a range.
    question: Can I export multiple pages at once?
  - answer: A full license is required; a temporary trial is available.
    question: Do I need a license for production?
  type: FAQPage
tags:
- convert DjVu
- Aspose.Imaging
- Java image conversion
title: วิธีส่งออก TIFF – โหลดและส่งออกหน้าจาก DjVu ด้วย Java และ Aspose.Imaging
url: /th/java/format-conversion-export/load-export-djvu-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# วิธีส่งออก TIFF – โหลดและส่งออกหน้า DjVu ใน Java ด้วย Aspose.Imaging

## บทนำ

หากคุณต้องการ **how to export TIFF** จากเอกสาร DjVu ในแอปพลิเคชัน Java คุณมาถูกที่แล้ว DjVu เป็นรูปแบบที่กะทัดรัดสำหรับเอกสารสแกน แต่ระบบหลายระบบต้องการ TIFF คำแนะนำนี้จะพาคุณผ่านการโหลดไฟล์ DjVu การเลือกหน้าที่ต้องการ และการส่งออกเป็นภาพ TIFF คุณภาพสูงโดยใช้ Aspose.Imaging สำหรับ Java เมื่อเสร็จคุณจะได้โค้ดสั้นที่นำกลับมาใช้ใหม่ได้ซึ่งสามารถใส่ลงในไพรพล์ไลน์การประมวลผลภาพที่ใช้ Java ใด ๆ

**สิ่งที่คุณจะได้เรียนรู้**
- วิธีโหลดภาพ DjVu ด้วย Aspose.Imaging ใน Java  
- การส่งออกหน้าที่กำหนดของ DjVu ไปเป็นรูปแบบ TIFF  
- การกำหนดค่าตัวเลือกการส่งออกและทำความเข้าใจพารามิเตอร์สำคัญ  

ก่อนที่เราจะเริ่มลงลึก โปรดตรวจสอบให้แน่ใจว่าสภาพแวดล้อมการพัฒนาของคุณตรงตามข้อกำหนดเบื้องต้นที่ระบุด้านล่าง

## คำตอบอย่างรวดเร็ว
- **คลาสหลักสำหรับการจัดการ DjVu คืออะไร?** `DjvuImage` แสดงเอกสาร DjVu ในหน่วยความจำ  
- **ต้องใช้บรรทัดโค้ดกี่บรรทัดในการส่งออกหน้าหนึ่งเป็น TIFF?** เพียงสองบรรทัดหลังจากโหลดภาพ  
- **อาร์ติแฟคต์ Maven ใดที่ให้การสนับสนุน DjVu?** `com.aspose:aspose-imaging` (เวอร์ชัน 25.5+)  
- **ฉันสามารถส่งออกหลายหน้าในครั้งเดียวได้หรือไม่?** ใช่ ใช้ `IntRange` เพื่อระบุช่วง  
- **ต้องการใบอนุญาตสำหรับการผลิตหรือไม่?** จำเป็นต้องมีใบอนุญาตเต็มรูปแบบ; มีใบอนุญาตทดลองชั่วคราว  

## “How to export TIFF” คืออะไร?
**“How to export TIFF”** หมายถึงกระบวนการแปลงภาพหรือหน้าของเอกสารเป็นรูปแบบ Tagged Image File Format (TIFF) ซึ่งเป็นรูปแบบไร้การสูญเสียที่ใช้กันอย่างแพร่หลายสำหรับการเก็บถาวรและการพิมพ์ Aspose.Imaging จัดการการแปลงนี้ด้วยการเรียก API เพียงครั้งเดียวพร้อมคงความละเอียดและการตั้งค่าการบีบอัด การแปลงนี้รักษารายละเอียดภาพทั้งหมด ทำให้เหมาะสำหรับการจัดเก็บถาวรคุณภาพสูงและการประมวลผลต่อเนื่อง

## ทำไมต้องใช้ Aspose.Imaging สำหรับการประมวลผลภาพใน Java?
Aspose.Imaging รองรับรูปแบบการนำเข้าและส่งออก **150+** รูปแบบ, ประมวลผลไฟล์ได้ถึง **5,000 หน้า** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ, และให้การทำงานแบบปลอดภัยต่อเธรด ความสามารถที่วัดได้เหล่านี้ทำให้เป็นตัวเลือกที่เชื่อถือได้สำหรับงานประมวลผลภาพ Java ที่มีอัตราการทำงานสูง โดยเฉพาะเมื่อจัดการกับชุดเอกสารขนาดใหญ่ที่ต้องการการแปลงแบบชุดและใช้หน่วยความจำน้อยที่สุด

## ข้อกำหนดเบื้องต้น

- **ไลบรารี Aspose.Imaging สำหรับ Java** – เวอร์ชัน 25.5 หรือใหม่กว่า  
- **Java Development Kit (JDK)** – เวอร์ชัน 8 หรือใหม่กว่า, ตั้งค่าอย่างถูกต้องบนเครื่องของคุณ  
- **ความรู้พื้นฐาน Java** – คุณควรคุ้นเคยกับการทำ I/O ของไฟล์และการจัดการข้อยกเว้น  

## วิธีตั้งค่า Maven Aspose Imaging?
เพื่อรวม Aspose.Imaging ในโครงการ Maven ให้เพิ่มการพึ่งพาในไฟล์ `pom.xml` ของโครงการ Maven จะดาวน์โหลดไลบรารีและการพึ่งพาแบบทรานซิทีฟ ทำให้ API พร้อมใช้งานสำหรับการคอมไพล์และรันไทม์ หลังจากเพิ่มโค้ดสั้นนี้ ให้รัน `mvn clean install` เพื่อให้แน่ใจว่าอาร์ติแฟคต์ถูกแก้ไขและโครงการสร้างสำเร็จ

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

## วิธีตั้งค่า Gradle Aspose Imaging?
สำหรับการสร้างด้วย Gradle ให้ประกาศการพึ่งพา Aspose.Imaging ในไฟล์ `build.gradle` Gradle จะดึงไลบรารีจาก Maven Central ทำให้คุณสามารถใช้ API ในโค้ด Java ของคุณได้ หลังจากอัปเดตสคริปต์ ให้รีเฟรชโครงการเพื่อดาวน์โหลด JAR และซิงค์การพึ่งพา

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

## ดาวน์โหลดโดยตรง
คุณยังสามารถดาวน์โหลด JAR ล่าสุดจาก [Aspose.Imaging releases](https://releases.aspose.com/imaging/java/).

### การรับใบอนุญาต
- **ทดลองใช้ฟรี** – รับใบอนุญาตชั่วคราวเพื่อการประเมิน  
- **ซื้อ** – พิจารณาซื้อใบอนุญาตเต็มรูปแบบสำหรับการใช้งานในผลิตภัณฑ์  

## การเริ่มต้นและการตั้งค่า
ก่อนใช้ API ใด ๆ คุณต้องเริ่มต้นไลบรารี `License` เป็นคลาสที่ใช้ในการกำหนดไฟล์ใบอนุญาต Aspose.Imaging ของคุณให้กับไลบรารี เพื่อให้ทำงานเต็มรูปแบบโดยไม่มีข้อจำกัดการประเมิน

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path/to/your/license.lic");
```

## วิธีโหลด DjVu?
DjvuImage เป็นอ็อบเจ็กต์ระดับบนสุดที่แสดงไฟล์ DjVu ในหน่วยความจำ เพื่ออ่านเอกสาร DjVu ให้เรียกเมธอดสถิต `Image.load()` พร้อมเส้นทางไฟล์; เมธอดนี้จะคืนค่าอินสแตนซ์ `Image` ซึ่งคุณต้องแคสต์เป็น `DjvuImage`. `Image.load()` เป็นเมธอดสถิติที่อ่านไฟล์ภาพและคืนค่าอ็อบเจ็กต์ `Image` ที่แสดงเนื้อหาที่โหลด

```java
   String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "/Sample.djvu";
   ```

```java
   try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
       // The image is now loaded and ready for further processing.
   }
   ```

### การแก้ไขปัญหา
- ตรวจสอบให้แน่ใจว่าเส้นทางไฟล์ถูกต้องและเข้าถึงได้  
- ห่อการเรียกโหลดในบล็อก try‑catch เพื่อจัดการ `IOException` หรือ `ImageLoadException`  

## วิธีส่งออก TIFF?
การส่งออกหน้าของ DjVu เป็น TIFF เกี่ยวข้องกับการสร้างอ็อบเจ็กต์ `TiffOptions` ที่ระบุการบีบอัด ความละเอียด และการตั้งค่าอื่น ๆ จากนั้นเรียกเมธอด `save()` บนหน้าที่ต้องการ `TiffOptions` เป็นคลาสที่เก็บการกำหนดค่าการส่งออก TIFF เช่น ประเภทการบีบอัดและความลึกสี ใช้ `IntRange` เพื่อเลือกหน้าที่ต้องการแปลง แล้ววนลูปและบันทึกแต่ละหน้าเป็นไฟล์ TIFF แยกกัน

สร้างไดเรกทอรีเอาต์พุต ตั้งค่า `TiffOptions` เลือกหน้าด้วย `IntRange` และสุดท้ายบันทึกแต่ละหน้าเป็นไฟล์ TIFF

```java
   String outputDir = "YOUR_OUTPUT_DIRECTORY" + "/ConvertDjvuPagesToTiff_out.tiff";
   ```

```java
   TiffOptions exportOptions = new TiffOptions(TiffExpectedFormat.TiffDeflateBw);
   ```

```java
   IntRange range = new IntRange(0, 2); // Export the first three pages.
   exportOptions.setMultiPageOptions(new DjvuMultiPageOptions(range));
   ```

```java
   try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
       image.save(outputDir, exportOptions);
   }
   ```

### ข้อผิดพลาดทั่วไป
- ตรวจสอบให้แน่ใจว่า `outputDir` มีอยู่; มิฉะนั้น `save()` จะโยนข้อยกเว้น  
- จำไว้ว่าดัชนีหน้ามีการนับจาก **ศูนย์**; หน้า 1 มีดัชนี 0  

## การประยุกต์ใช้ในทางปฏิบัติ
การส่งออกหน้าของ DjVu ไปเป็น TIFF มีประโยชน์ในหลายสถานการณ์:

1. **ระบบจัดเก็บถาวร** – เก็บเอกสารสแกนในรูปแบบที่ยอมรับทั่วโลก  
2. **กระบวนการตรวจทานเอกสาร** – ดึงเฉพาะหน้าที่ต้องการการอธิบาย  
3. **การรวมกับ DMS** – ส่งภาพ TIFF ไปยังไพรพล์ไลน์การจัดการเอกสารที่มีอยู่ซึ่งไม่รองรับ DjVu  

## ข้อควรพิจารณาด้านประสิทธิภาพ
เมื่อจัดการไฟล์ DjVu ขนาดใหญ่:

- ใช้ **try‑with‑resources** เพื่อปิดสตรีมโดยอัตโนมัติและปล่อยหน่วยความจำ  
- ประมวลผลไฟล์เป็นชิ้นส่วน (เช่น 10 หน้าในแต่ละครั้ง) เพื่อให้การใช้หน่วยความจำของ heap ต่ำ  
- แนะนำให้ใช้ `TiffCompression.CCITT4` สำหรับการสแกนขาว‑ดำเพื่อลดขนาดไฟล์โดยไม่สูญเสียคุณภาพ  

## คำถามที่พบบ่อย

**ถาม:** ฉันจะติดตั้ง Aspose.Imaging สำหรับ Java ในโครงการของฉันอย่างไร?  
**ตอบ:** ใช้ Maven หรือ Gradle ตามที่แสดงด้านบน หรือดาวน์โหลดโดยตรงจาก [หน้า releases ของ Aspose](https://releases.aspose.com/imaging/java/)

**ถาม:** ฉันสามารถส่งออกภาพ DjVu ไปเป็นรูปแบบอื่นนอกจาก TIFF ได้หรือไม่?  
**ตอบ:** ได้, Aspose.Imaging ยังรองรับ PNG, JPEG, BMP และรูปแบบอื่น ๆ อีกหลายรูปแบบ

**ถาม:** ควรทำอย่างไรหากไฟล์ใบอนุญาตของฉันไม่ถูกจดจำ?  
**ตอบ:** ตรวจสอบให้แน่ใจว่าเส้นทางใบอนุญาตถูกต้องและคุณเรียก `License.setLicense()` ก่อนการใช้ API ใด ๆ

**ถาม:** ฉันจะจัดการไฟล์ DjVu ขนาดใหญ่อย่างมีประสิทธิภาพได้อย่างไร?  
**ตอบ:** ประมวลผลเอกสารเป็นช่วงหน้าที่เล็กลงและปล่อยแต่ละอินสแตนซ์ `DjvuImage` อย่างทันท่วงทีเพื่อหลีกเลี่ยงความกดดันของหน่วยความจำ

**ถาม:** Aspose.Imaging ใช้ได้ฟรีสำหรับการใช้งานเชิงพาณิชย์หรือไม่?  
**ตอบ:** ใบอนุญาตทดลองชั่วคราวฟรี, แต่ต้องมีใบอนุญาตที่ซื้อเพื่อการใช้งานในผลิตภัณฑ์  

## แหล่งข้อมูล
- **เอกสารอ้างอิง**: [Aspose.Imaging Java API Reference](https://reference.aspose.com/imaging/java/)  
- **ดาวน์โหลด**: [Aspose.Imaging for Java Releases](https://releases.aspose.com/imaging/java/)  
- **ซื้อ**: [Buy Aspose.Imaging](https://purchase.aspose.com/buy)  
- **ใบอนุญาตฟรี**: [Get a Free License](https://releases.aspose.com/imaging/java/)  
- **ใบอนุญาตชั่วคราว**: [Request a Temporary License](https://purchase.aspose.com/temporary-license/)  
- **สนับสนุน**: [Aspose Community Forum](https://forum.aspose.com/c/imaging/14)

ด้วยการเชี่ยวชาญขั้นตอนข้างต้น คุณสามารถ **how to export TIFF** จากไฟล์ DjVu ในโซลูชันที่ใช้ Java ใด ๆ ได้อย่างเชื่อถือได้ ขอให้เขียนโค้ดอย่างสนุก!

---

**อัปเดตล่าสุด:** 2026-07-08  
**ทดสอบด้วย:** Aspose.Imaging 25.5 for Java  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [สร้าง Multi-Page TIFF ด้วย Aspose.Imaging สำหรับ Java: คู่มือฉบับสมบูรณ์](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [แปลง DjVu เป็น PDF ด้วย Aspose.Imaging สำหรับ Java - คู่มือขั้นตอนต่อขั้นตอน](/imaging/java/image-loading-saving/convert-djvu-to-pdf-aspose-imaging-java/)
- [แปลง DJVU เป็น BMP ใน Java ด้วย Aspose.Imaging: คู่มือขั้นตอนต่อขั้นตอน](/imaging/java/format-conversion-export/export-djvu-pages-bmp-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}