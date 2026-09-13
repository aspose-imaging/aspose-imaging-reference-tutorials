---
date: '2026-09-13'
description: เรียนรู้วิธีสร้างภาพ TIFF ใน Java ด้วย Aspose.Imaging รวมถึงการบีบอัด
  ความละเอียด และการตั้งค่าสี เพื่อผลิตไฟล์ TIFF คุณภาพสูง
keywords:
- create tiff java
- maven aspose imaging dependency
- tiff options java
- aspose imaging tiff
- java image processing
lastmod: '2026-09-13'
og_description: สร้างภาพ TIFF ใน Java ด้วย Aspose.Imaging เรียนรู้การตั้งค่าการบีบอัด
  ความละเอียด และตัวเลือกสีโดยใช้การพึ่งพา Aspose Imaging ของ Maven
og_image_alt: Tutorial guide showing Java code to create and configure TIFF images
  with Aspose.Imaging
og_title: วิธีสร้าง TIFF ใน Java ด้วยไลบรารี Aspose.Imaging
schemas:
- author: Aspose
  dateModified: '2026-09-13'
  description: Learn how to create TIFF images in Java with Aspose.Imaging, covering
    compression, resolution, and color settings to produce high‑quality TIFF files.
  headline: How to create TIFF in Java using Aspose.Imaging library
  type: TechArticle
- description: Learn how to create TIFF images in Java with Aspose.Imaging, covering
    compression, resolution, and color settings to produce high‑quality TIFF files.
  name: How to create TIFF in Java using Aspose.Imaging library
  steps:
  - name: '**Free trial** – download and evaluate without restrictions. See the **[Free
      Trial](https://releases.aspose.com/imaging/java/)** page.'
    text: '**Free trial** – download and evaluate without restrictions. See the **[Free
      Trial](https://releases.aspose.com/imaging/java/)** page.'
  - name: '**Temporary license** – request from Aspose for extended evaluation via
      the **[Temporary License Request](https://purchase.aspose.com/temporary-license/)**.'
    text: '**Temporary license** – request from Aspose for extended evaluation via
      the **[Temporary License Request](https://purchase.aspose.com/temporary-license/)**.'
  - name: '**Purchase license** – obtain a permanent license via the **[Purchase License](https://purchase.aspose.com/buy)**
      or the **[purchase page](https://purchase.aspose.com/buy)**.'
    text: '**Purchase license** – obtain a permanent license via the **[Purchase License](https://purchase.aspose.com/buy)**
      or the **[purchase page](https://purchase.aspose.com/buy)**.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Imaging supports over 150 formats, including PNG, JPEG, BMP,
      and GIF. See the **[Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)**
      for details.
    question: Can I use this code with other image formats?
  - answer: No, Gradle users can add the same coordinates in their `build.gradle`
      file; the underlying library is identical.
    question: Do I need the Maven Aspose Imaging dependency for Gradle projects?
  - answer: The library can stream TIFF files up to several gigabytes, limited only
      by available disk space, because it never loads the whole image into RAM.
    question: How large a TIFF can Aspose.Imaging process?
  - answer: Enable `LoadOptions` with `useMemoryCache = true` or process the image
      in tiles to keep memory usage low.
    question: What if I encounter an `OutOfMemoryError`?
  - answer: A free trial works for development, but a licensed version removes evaluation
      watermarks and unlocks full performance optimisations.
    question: Is a license required for development builds?
  type: FAQPage
tags:
- create tiff
- Aspose.Imaging
- Java image processing
title: วิธีสร้าง TIFF ใน Java ด้วยไลบรารี Aspose.Imaging
url: /th/java/format-specific-operations/create-tiff-images-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีสร้างไฟล์ TIFF ใน Java ด้วย Aspose.Imaging

## บทนำ

การสร้างไฟล์ TIFF ด้วยโปรแกรมอาจเป็นเรื่องท้าทาย โดยเฉพาะเมื่อคุณต้องการควบคุมการบีบอัด ความละเอียด และการตีความสีอย่างละเอียด ในบทเรียนนี้คุณจะได้เรียนรู้วิธี **สร้างไฟล์ TIFF ใน Java** ด้วย Aspose.Imaging ตั้งค่าตัวเลือก TIFF ที่พบบ่อยที่สุด และจัดการข้อมูลพิกเซล ไม่ว่าคุณจะกำลังสร้างระบบจัดเก็บดิจิทัล ระบบพิมพ์ หรือแอปพลิเคชันการแพทย์ การทำตามขั้นตอนด้านล่างจะให้วิธีการที่พร้อมใช้งานในระดับการผลิต

**สิ่งที่คุณจะได้เรียนรู้**

- วิธีกำหนดตัวเลือก TIFF เช่น การบีบอัด ความละเอียด และการตีความสี  
- กระบวนการสร้างภาพ TIFF ใหม่และจัดการพิกเซลใน Java  
- การประยุกต์ใช้ Aspose.Imaging ในการจัดการไฟล์ TIFF

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดที่รองรับการสร้าง TIFF ใน Java?** Aspose.Imaging for Java.  
- **ต้องมีใบอนุญาตสำหรับการผลิตหรือไม่?** ใช่ ใบอนุญาตที่ซื้อจะลบข้อจำกัดของรุ่นทดลองออกไป  
- **เครื่องมือสร้างใดที่สามารถใช้ได้?** Maven หรือ Gradle ผ่านการอ้างอิง Maven Aspose Imaging  
- **สามารถตั้งค่าการบีบอัดและความละเอียดได้หรือไม่?** แน่นอน—ใช้คุณสมบัติของ `TiffOptions`  
- **โค้ดนี้เข้ากันได้กับ JDK 8+ หรือไม่?** ใช่ ทำงานบน JDK 8 และรุ่นใหม่กว่า

## ข้อกำหนดเบื้องต้น

เพื่อทำตามบทเรียนนี้ โปรดตรวจสอบว่าคุณมี:

- **Java Development Kit (JDK)** 8 หรือสูงกว่า  
- **Maven** หรือ **Gradle** สำหรับการจัดการการอ้างอิง  
- ความคุ้นเคยพื้นฐานกับ Java และแนวคิดการประมวลผลภาพ

## การตั้งค่า Aspose.Imaging สำหรับ Java

ก่อนเริ่มเขียนโค้ด ให้เพิ่มไลบรารี Aspose.Imaging ลงในโปรเจกต์ของคุณ

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
implementation(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

หากคุณต้องการดาวน์โหลดด้วยตนเอง ให้รับรุ่นล่าสุดจาก [การปล่อย Aspose.Imaging สำหรับ Java](https://releases.aspose.com/imaging/java/). คุณยังสามารถใช้ลิงก์ทั่วไป **[ดาวน์โหลดเวอร์ชันล่าสุด](https://releases.aspose.com/imaging/java/)**

### การขอรับใบอนุญาต

รุ่นทดลองฟรีใช้ได้สำหรับการพัฒนา แต่ต้องมีใบอนุญาตสำหรับการใช้งานจริง

1. **ทดลองใช้ฟรี** – ดาวน์โหลดและประเมินโดยไม่มีข้อจำกัด ดูหน้า **[ทดลองใช้ฟรี](https://releases.aspose.com/imaging/java/)**  
2. **ใบอนุญาตชั่วคราว** – ขอจาก Aspose เพื่อขยายการทดลองผ่าน **[คำขอใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/)**  
3. **ซื้อใบอนุญาต** – รับใบอนุญาตถาวรผ่าน **[ซื้อใบอนุญาต](https://purchase.aspose.com/buy)** หรือ **[หน้าซื้อสินค้า](https://purchase.aspose.com/buy)**

### การเริ่มต้น

นำเข้าคลาสที่จำเป็นและเริ่มต้นไลบรารี:

```java
import com.aspose.imaging.imageoptions.TiffOptions;
```

## TiffOptions คืออะไร?

`TiffOptions` เป็นคลาสใน Aspose.Imaging ที่กำหนดวิธีการเข้ารหัสไฟล์ TIFF รวมถึงการบีบอัด ความละเอียด และการตั้งค่าสี มันให้คุณระบุลักษณะเฉพาะของไฟล์ผลลัพธ์ก่อนบันทึก

คุณจะกำหนดค่าอินสแตนซ์ `TiffOptions` ก่อนบันทึกภาพ เพื่อให้ไฟล์ที่ได้ตรงตามคุณภาพและความเข้ากันได้ที่ต้องการ การปรับคุณสมบัติต่าง ๆ จะทำให้คุณสามารถปรับ TIFF ให้สอดคล้องกับมาตรฐานการเก็บรักษา การพิมพ์ หรือการแพทย์ได้

## วิธีตั้งค่า TIFF options ใน Java?

เพื่อกำหนดค่า TIFF options คุณสร้างอ็อบเจ็กต์ `TiffOptions` แล้วกำหนดค่าต่าง ๆ เช่น `bitsPerSample`, `photometric`, `resolutionUnit`, `xResolution`, `yResolution` และ `compression`. การกำหนดค่านี้จะถูกนำไปใช้เมื่อเขียนภาพลงดิสก์ ทำให้ไฟล์ตรงตามสเปคที่ต้องการ

### การตั้งค่า properties ของ TiffOptions

ฟีเจอร์นี้แสดงวิธีกำหนดคุณสมบัติต่าง ๆ เพื่อสร้างไฟล์ TIFF ตามสเปคที่ต้องการ

#### ภาพรวม

การกำหนดค่า `TiffOptions` ช่วยให้คุณปรับผลลัพธ์ TIFF ให้สอดคล้องกับมาตรฐานอุตสาหกรรมสำหรับการเก็บรักษา การพิมพ์ หรือการแพทย์

##### การกำหนด bits per sample

```java
// Create an instance of TiffOptions
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);

// Set bits per sample for RGB configuration
options.setBitsPerSample(new int[] { 8, 8, 8 });
```

โค้ดนี้ตั้งค่าความลึกสีเป็น 24‑bit RGB ซึ่งเป็นมาตรฐานสำหรับภาพคุณภาพสูง

##### การตั้งค่า photometric interpretation

```java
// Use RGB photometric interpretation
options.setPhotometric(TiffPhotometrics.Rgb);
```

เมธอด `setPhotometric` ระบุว่าภาพใช้พาเลตต์ RGB

##### การกำหนดความละเอียดและหน่วย

```java
// Set resolution to 72 DPI for both X and Y axes
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));

// Specify resolution unit as inches
options.setResolutionUnit(TiffResolutionUnits.Inch);
```

การตั้งค่าเหล่านี้ทำให้ภาพมีขนาดการแสดงผลที่สม่ำเสมอบนอุปกรณ์ต่าง ๆ

##### การกำหนดการบีบอัด

```java
// Set compression to AdobeDeflate for efficient storage
options.setCompression(TiffCompressions.AdobeDeflate);
```

การใช้ `AdobeDeflate` ลดขนาดไฟล์โดยไม่สูญเสียคุณภาพ ทำให้เหมาะสำหรับการเก็บรักษา

## TiffImage คืออะไร?

`TiffImage` เป็นคลาสของ Aspose.Imaging ที่แสดงเอกสาร TIFF ในหน่วยความจำ ทำให้คุณสามารถจัดการระดับพิกเซลก่อนบันทึกได้ มันมีเมธอดสำหรับเข้าถึงและแก้ไขพิกเซล ชั้น และเมตาดาต้าแต่ละรายการ

การสร้าง `TiffImage` ด้วย `TiffOptions` ที่กำหนดไว้ให้คุณควบคุมเนื้อหาและเมตาดาต้าของภาพได้อย่างเต็มที่ ทำให้สามารถสร้างไฟล์ TIFF แบบกำหนดเองได้โดยอัตโนมัติ

## วิธีสร้างและจัดการภาพ TIFF?

เพื่อสร้างและจัดการภาพ TIFF คุณต้องสร้างอินสแตนซ์ `TiffImage` เติมบัฟเฟอร์พิกเซลด้วยข้อมูลที่ต้องการ แล้วบันทึกด้วย `TiffOptions` ที่กำหนดไว้ การทำงานนี้ทำให้ภาพถูกสร้างตามที่คุณตั้งค่าไว้ทั้งหมด

### การสร้างและจัดการ TiffImage

ตอนนี้ตัวเลือกได้ถูกตั้งค่าแล้ว ให้เราสร้างภาพโดยใช้การกำหนดเหล่านี้

#### ภาพรวม

การสร้างภาพ TIFF ประกอบด้วยการเริ่มต้น `TiffImage` ตั้งค่าพิกเซล และบันทึกผลลัพธ์ กระบวนการนี้ง่ายดายด้วย Aspose.Imaging

##### การเริ่มต้น TiffImage ใหม่

```java
try (TiffImage tiffImage = new TiffImage(new TiffFrame(options, 100, 100))) {
    // Loop over each pixel to set it to red color
    for (int i = 0; i < 100; i++) {
        tiffImage.getActiveFrame().setPixel(i, i, Color.getRed());
    }
    
    // Save the image to your desired output directory
    tiffImage.save("YOUR_OUTPUT_DIRECTORY" + "/CreatingTIFFImageWithCompression.tiff");
}
```

ในโค้ดส่วนนี้ เราสร้างภาพ TIFF ขนาด 100 × 100 พิกเซลและเติมพิกเซลสีแดงโดยใช้การตั้งค่าที่กำหนดไว้ล่วงหน้า

## การประยุกต์ใช้งานจริง

การเข้าใจวิธีตั้งค่า TIFF options และสร้างภาพโดยอัตโนมัติเป็นประโยชน์ในหลายสถานการณ์:

- **การเก็บรักษาดิจิทัล** – รักษาเอกสารหรืองานศิลปะในรูปแบบคุณภาพสูง  
- **การพิมพ์ระดับมืออาชีพ** – ทำให้การพิมพ์ตรงตามมาตรฐานอุตสาหกรรมสำหรับความแม่นยำของสี  
- **การแพทย์** – จัดการข้อมูลภาพละเอียดที่ต้องการการกำหนดค่าเฉพาะ

## ข้อพิจารณาด้านประสิทธิภาพ

เมื่อทำงานกับการประมวลผลภาพ ประสิทธิภาพเป็นสิ่งสำคัญ Aspose.Imaging สามารถจัดการ **รูปแบบภาพกว่า 150 ประเภท** และประมวลผล **TIFF หลายร้อยหน้า** โดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ ลดความเสี่ยงของข้อผิดพลาด OutOfMemory

- **เพิ่มประสิทธิภาพการใช้หน่วยความจำ** – ใช้ API สตรีมของ Aspose.Imaging สำหรับไฟล์ขนาดใหญ่  
- **ประมวลผลเป็นชุด** – ประมวลผลหลายภาพในรอบเดียวเพื่อลดค่าใช้จ่ายของการทำงาน  
- **การบีบอัดที่มีประสิทธิภาพ** – เลือก `AdobeDeflate` เพื่อสมดุลคุณภาพ‑ขนาดที่ดี

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้โค้ดนี้กับรูปแบบภาพอื่นได้หรือไม่?**  
A: ใช่ Aspose.Imaging รองรับรูปแบบกว่า 150 รูปแบบ รวมถึง PNG, JPEG, BMP, และ GIF ดู **[เอกสาร Aspose.Imaging](https://reference.aspose.com/imaging/java/)** สำหรับรายละเอียด

**Q: ฉันต้องการการอ้างอิง Maven Aspose Imaging สำหรับโครงการ Gradle หรือไม่?**  
A: ไม่ ผู้ใช้ Gradle สามารถเพิ่มพิกัดเดียวกันในไฟล์ `build.gradle` ของตนได้; ไลบรารีพื้นฐานเหมือนกัน

**Q: Aspose.Imaging สามารถประมวลผล TIFF ขนาดเท่าไหร่?**  
A: ไลบรารีสามารถสตรีมไฟล์ TIFF ขนาดหลายกิกะไบต์ได้ จำกัดเพียงพื้นที่ดิสก์ที่มี เนื่องจากไม่เคยโหลดภาพทั้งหมดเข้าสู่ RAM

**Q: จะทำอย่างไรหากเจอ `OutOfMemoryError`?**  
A: เปิดใช้งาน `LoadOptions` ด้วย `useMemoryCache = true` หรือประมวลผลภาพเป็นส่วนย่อย (tiles) เพื่อลดการใช้หน่วยความจำ

**Q: จำเป็นต้องมีใบอนุญาตสำหรับการสร้างรุ่นพัฒนาไหม?**  
A: รุ่นทดลองฟรีใช้ได้สำหรับการพัฒนา แต่ใบอนุญาตเต็มจะลบลายน้ำการประเมินและเปิดใช้งานการปรับประสิทธิภาพเต็มรูปแบบ

**Q: จะหาแนวทางช่วยเหลือได้จากที่ไหนหากเจอปัญหา?**  
A: เยี่ยมชม **[ฟอรั่มสนับสนุน Aspose](https://forum.aspose.com/c/imaging/14)** เพื่อรับความช่วยเหลือจากชุมชนและการสนับสนุนอย่างเป็นทางการ

## สรุป

คุณมีคู่มือที่พร้อมใช้งานสำหรับ **การสร้างไฟล์ TIFF ใน Java** ด้วย Aspose.Imaging แล้ว โดยการกำหนดค่า `TiffOptions` และทำงานกับ `TiffImage` คุณสามารถสร้างไฟล์ TIFF คุณภาพสูงที่ตรงตามมาตรฐานการเก็บรักษา การพิมพ์ หรือการแพทย์ได้อย่างครบถ้วน

**ขั้นตอนต่อไป**

- สำรวจ `TiffOptions` เพิ่มเติม เช่น `extraSamples` และ `predictor` สำหรับกรณีการใช้งานเฉพาะ  
- ทดลองใช้ API ของ Aspose.Imaging เพื่อแปลงรูปแบบ เพิ่มลายน้ำ หรือดึงเมตาดาต้า

---

**อัปเดตล่าสุด:** 2026-09-13  
**ทดสอบกับ:** Aspose.Imaging 24.12 for Java  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [เชี่ยวชาญการประมวลผลภาพ TIFF ใน Java ด้วย Aspose.Imaging](/imaging/java/image-loading-saving/load-save-tiff-images-aspose-imaging-java/)
- [การประมวลผลภาพ TIFF ขั้นสูงใน Java ด้วย Aspose.Imaging](/imaging/java/format-specific-operations/mastering-tiff-image-processing-java-aspose-imaging/)
- [การประมวลผลภาพ Java ด้วย Aspose.Imaging: โหลด, ปรับปรุง & บันทึกภาพ](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}