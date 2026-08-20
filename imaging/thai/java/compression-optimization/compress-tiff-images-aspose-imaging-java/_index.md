---
date: '2026-03-20'
description: เรียนรู้วิธีใช้ Aspose.Imaging สำหรับ Java เพื่อบีบอัดภาพ TIFF ด้วยการบีบอัด
  LZW ลดขนาดไฟล์ในขณะที่รักษาคุณภาพไว้
keywords:
- compress TIFF images Java
- Aspose.Imaging LZW compression
- Java image optimization
- TIFF compression in Java with Aspose
- image compression tutorial
title: วิธีใช้ Aspose.Imaging เพื่อบีบอัดภาพ TIFF ใน Java (คู่มือการบีบอัด LZW)
url: /th/java/compression-optimization/compress-tiff-images-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# บทแนะนำ: การบีบอัดภาพ TIFF ด้วย Aspose.Imaging Java

## บทนำ

ในบทแนะนำนี้ คุณจะได้เรียนรู้ **วิธีใช้ Aspose.Imaging for Java** เพื่อบีบอัดภาพ TIFF อย่างมีประสิทธิภาพ การจัดการไฟล์ TIFF ขนาดใหญ่สามารถกินพื้นที่จัดเก็บและแบนด์วิดท์ได้อย่างรวดเร็ว แต่ด้วยการบีบอัด LZW (Lempel‑Ziv‑Welch) คุณสามารถ **ลดขนาดไฟล์ TIFF** ได้โดยไม่สูญเสียคุณภาพของภาพ เราจะอธิบายขั้นตอนการโหลด TIFF การกำหนดค่า **tiff compression LZW** และการบันทึกผลลัพธ์ที่ปรับแต่งแล้ว—เหมาะสำหรับผู้ที่สนใจ **java image optimization**  

**สิ่งที่คุณจะได้เรียนรู้**
- วิธีตั้งค่า Aspose.Imaging สำหรับ Java
- การโหลดและประมวลผลภาพ TIFF อย่างง่ายดาย
- การกำหนดค่าการบีบอัด LZW ด้วย `TiffOptions`
- การบันทึกภาพ TIFF ที่ปรับแต่งแล้วให้มีขนาดเล็กลงแต่ยังคงไม่มีการสูญเสียข้อมูล  

มาดูข้อกำหนดเบื้องต้นกันก่อน เพื่อให้คุณสามารถเริ่มบีบอัดได้ทันที  

## คำตอบอย่างรวดเร็ว
- **ไลบรารีที่ต้องการคืออะไร?** Aspose.Imaging for Java  
- **อัลกอริทึมการบีบอัดคืออะไร?** LZW (lossless)  
- **เวอร์ชัน Java ที่รองรับ?** JDK ล่าสุด (เช่น 11, 17)  
- **ต้องการไลเซนส์หรือไม่?** ไลเซนส์ทดลองหรือไลเซนส์ชั่วคราวใช้ได้สำหรับการทดสอบ; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **การลดขนาดโดยทั่วไป?** ลดได้ถึง 30‑50 % สำหรับภาพที่เหมาะสม  

## ข้อกำหนดเบื้องต้น

ก่อนที่จะนำการบีบอัดภาพไปใช้ในโปรเจกต์ Java ของคุณ ให้แน่ใจว่ามีสิ่งต่อไปนี้:
- **Aspose.Imaging for Java library** – จำเป็นสำหรับคุณลักษณะการประมวลผลภาพทั้งหมด  
- **Java Development Kit (JDK)** – เวอร์ชันล่าสุดที่เข้ากันได้กับไลบรารี Aspose  
- **Basic Java knowledge** – ความคุ้นเคยกับการทำงานกับไฟล์ I/O และแนวคิดเชิงวัตถุจะเป็นประโยชน์  

## การตั้งค่า Aspose.Imaging สำหรับ Java

เพื่อเริ่มต้น ให้เพิ่มไลบรารี Aspose.Imaging ลงในระบบการสร้างของคุณ เลือกวิธีที่ตรงกับโปรเจกต์ของคุณ  

### ใช้ Maven
เพิ่ม dependency ต่อไปนี้ในไฟล์ `pom.xml` ของคุณ:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### ใช้ Gradle
ใส่บรรทัดนี้ในไฟล์ `build.gradle` ของคุณ:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### ดาวน์โหลดโดยตรง
หรือคุณสามารถดาวน์โหลดเวอร์ชันล่าสุดได้จาก [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/)  

#### การขอรับไลเซนส์
คุณสามารถรับไลเซนส์ทดลองฟรีหรือขอไลเซนส์ชั่วคราวเพื่อประเมินความสามารถของ Aspose.Imaging อย่างเต็มที่ก่อนการซื้อ  

## วิธีใช้ Aspose.Imaging สำหรับการบีบอัด TIFF ใน Java

ตอนนี้เราจะอธิบายการดำเนินการทีละขั้นตอน แต่ละบล็อกโค้ดยังคงเหมือนเดิมจากบทแนะนำต้นฉบับ เราจะเพิ่มบริบทที่ชัดเจนขึ้นรอบ ๆ โค้ด  

### การโหลดภาพ TIFF

**ทำไมเรื่องนี้ถึงสำคัญ:** การโหลดภาพอย่างถูกต้องจะสร้างอ็อบเจ็กต์ `Image` ที่ถูกต้องซึ่งจะใช้ในขั้นตอนต่อ ๆ ไป  

#### ขั้นตอนที่ 1: นำเข้าคลาส Image
```java
import com.aspose.imaging.Image;
```

#### ขั้นตอนที่ 2: โหลดภาพจากดิสก์
```java
String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "/sample.tiff";
Image image = Image.load(dataDir);
```

### การสร้าง TiffOptions สำหรับการบีบอัดภาพ

**ทำไมเรื่องนี้ถึงสำคัญ:** `TiffOptions` ช่วยให้คุณกำหนดวิธีการเข้ารหัส TIFF ที่ส่งออกอย่างแม่นยำ รวมถึงการตั้งค่า **tiff compression LZW**  

#### ขั้นตอนที่ 1: นำเข้า enums และคลาส options ที่จำเป็น
```java
import com.aspose.imaging.fileformats.tiff.enums.TiffCompressions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.imaging.imageoptions.TiffOptions;
```

#### ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการบีบอัด
```java
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);
outputSettings.setBitsPerSample(new int[] { 4 });
outputSettings.setCompression(TiffCompressions.Lzw);
outputSettings.setPhotometric(TiffPhotometrics.Palette);
```

### การตั้งค่า Palette แบบ grayscale (ไม่บังคับแต่เป็นประโยชน์)

การใช้ palette แบบ grayscale 4‑bit สามารถช่วย **ลดขนาดไฟล์ TIFF** ได้อีก โดยเฉพาะสำหรับการสแกนแบบโมโนโครม  

#### ขั้นตอนที่ 1: นำเข้า palette helper
```java
import com.aspose.imaging.ColorPaletteHelper;
```

#### ขั้นตอนที่ 2: กำหนด palette แบบ grayscale
```java
outputSettings.setPalette(ColorPaletteHelper.create4BitGrayscale(false));
```

### การบันทึกภาพ TIFF ที่บีบอัดแล้ว

**ทำไมเรื่องนี้ถึงสำคัญ:** คำสั่ง `save` จะเขียนภาพลงดิสก์โดยใช้ตัวเลือกทั้งหมดที่คุณกำหนด ทำให้ได้ไฟล์ที่เล็กลงและบีบอัดด้วย LZW  

#### ขั้นตอนที่ 1: กำหนดเส้นทางเอาต์พุต
```java
String outputDir = "YOUR_OUTPUT_DIRECTORY" + "/SampleTiff_out.tiff";
```

#### ขั้นตอนที่ 2: บันทึกด้วยการตั้งค่าการบีบอัด
```java
image.save(outputDir, outputSettings);
```

## การประยุกต์ใช้งานจริง

ต่อไปนี้เป็นสถานการณ์จริงที่การ **บีบอัด tiff** ด้วย LZW สามารถเป็นตัวเปลี่ยนเกม:
1. **การเก็บเอกสาร** – จัดเก็บ PDF หรือ TIFF ที่สแกนได้อย่างมีประสิทธิภาพมากขึ้น  
2. **การถ่ายภาพทางการแพทย์** – รักษารายละเอียดการวินิจฉัยขณะทำให้ขนาดไฟล์อยู่ในระดับที่จัดการได้  
3. **คลังภาพถ่าย** – เก็บไฟล์ต้นฉบับความละเอียดสูงโดยไม่ทำให้พื้นที่จัดเก็บบวมเกินไป  
4. **แอปพลิเคชันเว็บ** – ให้บริการภาพที่เล็กลงเพื่อโหลดหน้าเร็วขึ้นและลดค่าแบนด์วิดท์  

## การพิจารณาประสิทธิภาพ

เมื่อทำงานกับภาพขนาดใหญ่ ให้คำนึงถึงเคล็ดลับต่อไปนี้เพื่อรักษาประสิทธิภาพที่ดีที่สุด:
- **การจัดการหน่วยความจำ:** ปล่อยอ็อบเจ็กต์ `Image` ขนาดใหญ่โดยเร็ว (`image.dispose()`) หากคุณประมวลผลหลายไฟล์ในลูป  
- **การปรับความลึกบิต:** ปรับ `BitsPerSample` ให้เป็นค่าต่ำสุดที่ยอมรับได้สำหรับการใช้งานของคุณ  
- **การประมวลผลเป็นกลุ่ม:** สำหรับการทำงานเป็นจำนวนมาก พิจารณาใช้ multithreading แต่ต้องตรวจสอบการใช้ heap ของ JVM  

## ปัญหาที่พบบ่อยและวิธีแก้

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|--------------|-----|
| OutOfMemoryError ระหว่างการโหลด TIFF ขนาดใหญ่มาก | โหลดภาพเต็มลงในหน่วยความจำ | ใช้ `Image.load(dataDir, new LoadOptions { BufferSize = … })` หรือประมวลผลเป็นส่วนย่อย |
| ไฟล์ที่บันทึกมีขนาดใหญ่กว่าต้นฉบับ | `BitsPerSample` ไม่ถูกต้องหรือ palette ไม่ตรงกัน | ตรวจสอบว่า `setBitsPerSample` ตรงกับความลึกสีของภาพต้นฉบับ |
| Palette แบบ grayscale แสดงผลไม่ถูกต้อง | ไม่ได้กำหนด palette ก่อนบันทึก | ตรวจสอบว่าได้เรียก `outputSettings.setPalette(...)` **ก่อน** `image.save` |

## คำถามที่พบบ่อย

**ถาม: LZW compression คืออะไร?**  
**ตอบ:** การบีบอัด Lempel‑Ziv‑Welch (LZW) เป็นอัลกอริทึมแบบ lossless ที่ลดขนาดไฟล์โดยไม่สูญเสียข้อมูลภาพใด ๆ  

**ถาม: ฉันสามารถใช้ Aspose.Imaging for Java ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
**ตอบ:** ได้ คุณสามารถซื้อไลเซนส์เพื่อใช้ในเชิงพาณิชย์ได้ เยี่ยมชม [Aspose Purchase](https://purchase.aspose.com/buy) สำหรับรายละเอียด  

**ถาม: ไลบรารีนี้เข้ากันได้กับทุกเวอร์ชันของ JDK หรือไม่?**  
**ตอบ:** รองรับ JDK เวอร์ชันล่าสุดส่วนใหญ่ ตรวจสอบเอกสารอย่างเป็นทางการเพื่อดูความเข้ากันได้ของเวอร์ชันที่แน่นอน  

**ถาม: ฉันจะจัดการกับภาพขนาดใหญ่โดยไม่ให้หน่วยความจำหมดได้อย่างไร?**  
**ตอบ:** ใช้แนวปฏิบัติการจัดการหน่วยความจำอย่างมีประสิทธิภาพ เช่น ปล่อยอ็อบเจ็กต์ `Image` อย่างเร็วและประมวลผลภาพเป็นชิ้นย่อยเมื่อทำได้  

**ถาม: Aspose.Imaging รองรับรูปแบบไฟล์อื่น ๆ อะไรบ้าง?**  
**ตอบ:** ไลบรารีรองรับ BMP, JPEG, PNG, GIF และอื่น ๆ อีกมากมาย สำรวจรายการเต็มได้ที่ [documentation site](https://reference.aspose.com/imaging/java/)  

## แหล่งข้อมูล

- **เอกสารอ้างอิง:** [Aspose.Imaging Java Reference](https://reference.aspose.com/imaging/java/)  
- **ดาวน์โหลด:** [Latest Releases](https://releases.aspose.com/imaging/java/)  
- **ซื้อ:** [Buy Now](https://purchase.aspose.com/buy)  
- **ทดลองใช้ฟรี:** [Start Here](https://releases.aspose.com/imaging/java/)  
- **ไลเซนส์ชั่วคราว:** [Request Here](https://purchase.aspose.com/temporary-license/)  
- **สนับสนุน:** สำหรับความช่วยเหลือเพิ่มเติม เยี่ยมชม [Aspose Forum](https://forum.aspose.com/c/imaging/14)

---  

**อัปเดตล่าสุด:** 2026-03-20  
**ทดสอบด้วย:** Aspose.Imaging 25.5 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}