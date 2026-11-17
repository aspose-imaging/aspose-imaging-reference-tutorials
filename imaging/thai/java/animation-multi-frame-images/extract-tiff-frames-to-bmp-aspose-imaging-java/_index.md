---
date: '2026-11-17'
description: เรียนรู้วิธีแปลง tiff เป็น bmp ด้วย Aspose.Imaging for Java คู่มือนี้ครอบคลุมการแปลงภาพ
  Java ของไฟล์ TIFF หลายหน้า, licensing, และ frame extraction.
keywords:
- convert tiff to bmp
- java image conversion
- convert multi page tiff
- aspose imaging java
- maven aspose imaging
lastmod: '2026-11-17'
og_description: เรียนรู้วิธีแปลง tiff เป็น bmp ด้วย Aspose.Imaging for Java คู่มือนี้อธิบาย
  java image conversion, licensing, และ extracting frames จากไฟล์ TIFF หลายหน้า.
og_image_alt: 'Guide: convert tiff to bmp frames with Aspose.Imaging Java'
og_title: แปลง tiff เป็นเฟรม bmp ด้วย Aspose.Imaging for Java
schemas:
- author: Aspose
  dateModified: '2026-11-17'
  description: Learn how to convert tiff to bmp using Aspose.Imaging for Java. This
    guide covers java image conversion of multi‑page TIFFs, licensing, and frame extraction.
  headline: Convert tiff to bmp frames using Aspose.Imaging for Java
  type: TechArticle
- questions:
  - answer: Yes, but you need a valid **Aspose license for Java** for production use.
    question: Can I use Aspose.Imaging for Java in commercial projects?
  - answer: It supports JPEG, PNG, GIF, PSD, and many more. See the [documentation](https://reference.aspose.com/imaging/java/)
      for a full list.
    question: What file formats does Aspose.Imaging support besides TIFF and BMP?
  - answer: Limits are hardware‑dependent; the library is designed to handle large
      multi‑frame images efficiently.
    question: Is there a limit on the number of frames I can process in a TIFF?
  - answer: Double‑check that the directories exist and that the Java process has
      read/write rights.
    question: How do I troubleshoot file‑path or permission errors?
  - answer: Absolutely. Wrap the snippet in a loop that scans a folder and processes
      each TIFF sequentially.
    question: Can this be automated for batch processing of many TIFF files?
  type: FAQPage
tags:
- convert tiff
- Aspose.Imaging
- Java image processing
- multi-frame TIFF
- BMP conversion
title: แปลง tiff เป็นเฟรม bmp ด้วย Aspose.Imaging for Java
url: /th/java/animation-multi-frame-images/extract-tiff-frames-to-bmp-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เชี่ยวชาญการแยกเฟรม TIFF เป็นรูปแบบ BMP ด้วย Aspose.Imaging Java

## บทนำ

หากคุณต้องการ **อ่านไฟล์ TIFF** ดึงแต่ละเฟรมออก และ **แปลง tiff เป็น bmp** **Aspose.Imaging for Java** ทำให้การทำงานเป็นเรื่องง่าย ในคู่มือนี้เราจะอธิบายทุกอย่างที่คุณต้องการ — ตั้งแต่การตั้งค่าห้องสมุดและการใช้ **Aspose license for Java** ไปจนถึงการจัดการ TIFF หลายหน้าและการแปลงเป็นไฟล์ BMP สุดท้ายคุณจะได้โค้ดสั้นที่นำกลับมาใช้ใหม่ได้และสามารถใส่ลงในโปรเจกต์ Java ใดก็ได้

**สิ่งที่คุณจะได้เรียนรู้**
- วิธีการติดตั้งและรับใบอนุญาต Aspose.Imaging for Java  
- ขั้นตอนที่แน่นอน **วิธีอ่าน tiff** ไฟล์และวนลูปผ่านเฟรม  
- วิธี **แปลงภาพ tiff หลายหน้า** เป็นไฟล์ BMP แยกกัน  

มาเตรียมความต้องการเบื้องต้นให้พร้อมเพื่อให้คุณเริ่มเขียนโค้ดได้ทันที

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดที่จัดการการแปลง TIFF เป็น BMP?** Aspose.Imaging for Java.  
- **ฉันต้องการใบอนุญาตหรือไม่?** ใช่ – **Aspose license for Java** จะเปิดใช้งานฟังก์ชันทั้งหมด.  
- **ฉันสามารถประมวลผล TIFF หลายหน้าได้หรือไม่?** แน่นอน; API ให้คุณวนลูปผ่านแต่ละเฟรม.  
- **เครื่องมือสร้าง Java ใดที่รองรับ?** Maven, Gradle, หรือดาวน์โหลด JAR โดยตรง.  
- **ต้องใช้โค้ดเท่าไหร่?** น้อยกว่า 30 บรรทัดของ Java ที่ตรงไปตรงมา.

## Aspose Imaging Java คืออะไร?
`Aspose.Imaging` เป็นไลบรารี API แบบ pure‑Java ที่แสดงไฟล์ภาพเดียวในหน่วยความจำ รองรับ **รูปแบบภาพกว่า 100+** และให้เมธอดระดับสูงสำหรับการโหลด, แก้ไข, และแปลงภาพโดยไม่ต้องพึ่งพาไลบรารีเนทีฟ

## ทำไมต้องใช้ Aspose Imaging Java สำหรับการแยกเฟรม TIFF?
- **ไม่มีการพึ่งพาไลบรารีภายนอก** – pure Java, ทำงานบนทุกระบบปฏิบัติการ.  
- **รองรับหลายเฟรมเต็มรูปแบบ** – จัดการ TIFF, PSD, GIF, และรูปแบบที่มีหลายเลเยอร์อื่น ๆ.  
- **การให้ใบอนุญาตที่แข็งแรง** – **Aspose license for Java** จะลบข้อจำกัดการประเมินและเปิดใช้งานการประมวลผลเป็นชุด.  
- **เน้นประสิทธิภาพ** – สามารถประมวลผล TIFF หลายร้อยหน้า ขนาดถึง 2 GB โดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ, ขอบคุณการจัดการสตรีมในตัว

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่มการทำงาน, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

### ไลบรารีที่ต้องการ, เวอร์ชัน, และการพึ่งพา
- **Aspose.Imaging for Java**: เวอร์ชัน 25.5 หรือใหม่กว่า (API ที่ใช้ในบทเรียนนี้).

### ความต้องการการตั้งค่าสภาพแวดล้อม
- ความรู้พื้นฐานของ Java.  
- IDE เช่น IntelliJ IDEA หรือ Eclipse.  

## การตั้งค่า Aspose.Imaging สำหรับ Java
เพื่อเริ่มทำงานกับ Aspose.Imaging, ทำตามขั้นตอนการติดตั้งที่เหมาะกับระบบการสร้างของคุณ:

**Maven**  
```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```  

**Gradle**  
```gradle
implementation 'com.aspose:aspose-imaging:25.5'
```  

**ดาวน์โหลดโดยตรง**  
หรือคุณสามารถ [ดาวน์โหลด Aspose.Imaging](https://releases.aspose.com/imaging/java/) หรือดาวน์โหลดเวอร์ชันล่าสุดจาก [การปล่อย Aspose.Imaging สำหรับ Java](https://releases.aspose.com/imaging/java/).

### ขั้นตอนการรับใบอนุญาต
- **Free trial** – ทดลองใช้ไลบรารีโดยไม่มีค่าใช้จ่าย.  
- **Temporary license** – มีประโยชน์ในระหว่างการพัฒนา.  
- **Purchase** – ปลดล็อกคุณสมบัติทั้งหมดสำหรับการใช้งานจริง.

เมื่อคุณมีไฟล์ใบอนุญาตแล้ว, เริ่มต้น Aspose.Imaging:

```java
// Set license to unlock full features (if applicable)
License license = new License();
license.setLicense("path/to/your/license.lic");
```  

## วิธีแปลง tiff เป็น bmp ด้วย Aspose.Imaging Java?
`Image.load` เป็นเมธอดสแตติกที่อ่านไฟล์ภาพและคืนค่าอ็อบเจ็กต์ `Image` ที่แทนภาพที่โหลดแล้ว  

โหลด TIFF หลายหน้าโดยใช้ `Image.load("source.tif")` ซึ่งจะอ่านไฟล์และคืนค่าอ็อบเจ็กต์ `Image` ที่แทนเอกสาร จากนั้นเรียก `save` บนแต่ละเฟรมโดยใช้อินสแตนซ์ของ `BmpOptions` รูปแบบสั้นนี้จะแยกทุกหน้าและเขียนเป็นไฟล์ BMP แยกแต่ละไฟล์โดยอัตโนมัติจัดการความลึกสีและการบีบอัด

ด้านล่างเราจะอธิบายสามขั้นตอนสำคัญ พร้อมตัวอย่างโค้ดสั้น ๆ

### ขั้นตอน 1: โหลดภาพ TIFF
```java
try (TiffImage multiImage = (TiffImage) Image.load("YOUR_DOCUMENT_DIRECTORY/sample.tiff")) {
    // Proceed to process each frame.
}
```  

### ขั้นตอน 2: วนลูปผ่านเฟรมของ TIFF
```java
int frameCounter = 0;
for (TiffFrame tiffFrame : multiImage.getFrames()) {
    // Process each frame.
}
```  

### ขั้นตอน 3: แยกและบันทึกแต่ละเฟรมเป็น BMP
`BmpOptions` กำหนดรูปแบบเอาต์พุตและตัวเลือกการเข้ารหัสสำหรับไฟล์ BMP.  

```java
multiImage.setActiveFrame(tiffFrame);
Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());

try (BmpOptions bmpCreateOptions = new BmpOptions()) {
    bmpCreateOptions.setBitsPerPixel(24);
    String outputPath = String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "YOUR_OUTPUT_DIRECTORY/", frameCounter);

    bmpCreateOptions.setSource(new FileCreateSource(outputPath, false));
    try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight())) {
        bmpImage.savePixels(tiffFrame.getBounds(), pixels);
        bmpImage.save(outputPath);  // Save the BMP file.
    }
}
frameCounter++;
```  

## ปัญหาทั่วไปและวิธีแก้
- **สิทธิ์การเขียน** – ตรวจสอบว่าโฟลเดอร์ปลายทางสามารถเขียนได้.  
- **เส้นทาง TIFF ไม่ถูกต้อง** – ตรวจสอบว่าไฟล์มีอยู่และเส้นทางถูกต้อง.  
- **ข้อผิดพลาด Out‑of‑memory** – ใช้ `try‑with‑resources` (ตามที่แสดง) เพื่อปล่อยทรัพยากรเนทีฟโดยเร็ว.

## การประยุกต์ใช้งานจริง
การเข้าใจว่าฟีเจอร์นี้สามารถนำไปใช้ในสถานการณ์จริงได้อย่างไรจะเพิ่มคุณค่า:

1. **การถ่ายภาพทางการแพทย์** – แยกชั้นภาพแต่ละชั้นจาก TIFF ที่แปลงจาก DICOM หลายเฟรมเพื่อการวิเคราะห์.  
2. **การจัดเก็บดิจิทัล** – แยกไฟล์ TIFF ขนาดใหญ่เป็น BMP เพื่อการแจกจ่ายที่ง่ายขึ้น.  
3. **การออกแบบกราฟิก** – แยกเฟรมสำหรับการสร้างแอนิเมชันหรือกระบวนการคอมโพสติ้ง.

## การพิจารณาประสิทธิภาพ
- **การจัดการหน่วยความจำ** – รูปแบบ `try‑with‑resources` จะทำลบบัฟเฟอร์ภาพขนาดใหญ่โดยอัตโนมัติ.  
- **การประมวลผลเป็นชุด** – วนลูปผ่านโฟลเดอร์ของไฟล์ TIFF และใช้ `BmpOptions` ตัวเดียวกันซ้ำเพื่อ ลดภาระ.

## คำถามที่พบบ่อย
**Q: ฉันสามารถใช้ Aspose.Imaging สำหรับ Java ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
A: ใช่, แต่คุณต้องมี **Aspose license for Java** ที่ถูกต้องสำหรับการใช้งานในขั้นตอนการผลิต.

**Q: Aspose.Imaging รองรับรูปแบบไฟล์อะไรบ้างนอกจาก TIFF และ BMP?**  
A: รองรับ JPEG, PNG, GIF, PSD, และอื่น ๆ อีกมาก. ดูที่ [เอกสาร Aspose.Imaging](https://reference.aspose.com/imaging/java/) เพื่อรายการเต็ม.

**Q: มีขีดจำกัดจำนวนเฟรมที่ฉันสามารถประมวลผลใน TIFF หรือไม่?**  
A: ขีดจำกัดขึ้นอยู่กับฮาร์ดแวร์; ไลบรารีออกแบบมาเพื่อจัดการภาพหลายเฟรมขนาดใหญ่อย่างมีประสิทธิภาพ.

**Q: ฉันจะแก้ไขข้อผิดพลาดเกี่ยวกับเส้นทางไฟล์หรือสิทธิ์ได้อย่างไร?**  
A: ตรวจสอบให้แน่ใจว่าไดเรกทอรีมีอยู่และกระบวนการ Java มีสิทธิ์อ่าน/เขียน.

**Q: สามารถทำให้เป็นอัตโนมัติสำหรับการประมวลผลเป็นชุดของไฟล์ TIFF จำนวนมากได้หรือไม่?**  
A: แน่นอน. ห่อโค้ดสั้นนี้ในลูปที่สแกนโฟลเดอร์และประมวลผลแต่ละ TIFF ตามลำดับ.

## แหล่งข้อมูล
- [เอกสาร Aspose.Imaging](https://reference.aspose.com/imaging/java/)
- [ดาวน์โหลด Aspose.Imaging](https://releases.aspose.com/imaging/java/)
- [ซื้อใบอนุญาต](https://purchase.aspose.com/buy)
- [ทดลองใช้ฟรี](https://releases.aspose.com/imaging/java/)
- [ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/)
- [ฟอรั่มสนับสนุน](https://forum.aspose.com/c/imaging/14)

---

**อัปเดตล่าสุด:** 2026-11-17  
**ทดสอบด้วย:** Aspose.Imaging 25.5 for Java  
**ผู้เขียน:** Aspose

## บทเรียนที่เกี่ยวข้อง
- [แปลง Multi-Frame TIFF เป็น JPEG ด้วย Aspose.Imaging for Java - คู่มือครบถ้วน](/imaging/java/image-loading-saving/convert-multi-frame-tiff-to-jpeg-aspose-imaging-java/)
- [แยกเฟรม Multi Page TIFF ด้วย Aspose.Imaging for Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)
- [ประมวลผล multi frame tiff ใน Java ด้วย Aspose.Imaging](/imaging/java/animation-multi-frame-images/java-aspose-imaging-multi-frame-tiff-processing/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}