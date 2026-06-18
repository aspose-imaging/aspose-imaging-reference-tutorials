---
date: '2026-06-18'
description: เรียนรู้วิธีใช้ Aspose Imaging Maven dependency เพื่อแปลงไฟล์ DJVU เป็นภาพ
  BMP ใน Java คู่มือแบบขั้นตอนต่อขั้นตอนพร้อมการตั้งค่า ตัวเลือก และการส่งออกช่วงหน้า
keywords:
- aspose imaging maven dependency
- how to convert djvu
- convert djvu to bmp java
- aspose imaging java setup
- djvu page export bmp
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how to use the Aspose Imaging Maven dependency to convert DJVU
    files to BMP images in Java. Step‑by‑step guide with setup, options, and page‑range
    export.
  headline: Aspose Imaging Maven Dependency – Convert DJVU to BMP in Java
  type: TechArticle
- description: Learn how to use the Aspose Imaging Maven dependency to convert DJVU
    files to BMP images in Java. Step‑by‑step guide with setup, options, and page‑range
    export.
  name: Aspose Imaging Maven Dependency – Convert DJVU to BMP in Java
  steps:
  - name: '**Archiving:** Convert DJVU files to BMP for easier archival and retrieval.'
    text: '**Archiving:** Convert DJVU files to BMP for easier archival and retrieval.'
  - name: '**Document Sharing:** Share individual images from DJVU documents without
      requiring specialized viewers.'
    text: '**Document Sharing:** Share individual images from DJVU documents without
      requiring specialized viewers.'
  - name: '**Web Development:** Use BMP images for web projects that need lossless
      graphics.'
    text: '**Web Development:** Use BMP images for web projects that need lossless
      graphics.'
  - name: '**Education:** Provide students with accessible image formats for study
      materials.'
    text: '**Education:** Provide students with accessible image formats for study
      materials.'
  - name: '**Integration:** Embed this conversion process into larger Java applications
      for automated workflows.'
    text: '**Integration:** Embed this conversion process into larger Java applications
      for automated workflows.'
  type: HowTo
- questions:
  - answer: DJVU is a highly compressed file format designed for storing scanned documents,
      images, and multi‑page publications while maintaining visual fidelity.
    question: What is a DJVU file?
  - answer: Yes, modify the `IntRange` parameters to target any start and end indices
      you require.
    question: Can I convert other page ranges besides the first two pages?
  - answer: Increase the bits‑per‑pixel setting in `BmpOptions` to 32 and ensure the
      source DJVU pages are not downscaled during loading.
    question: My BMP files look blurry—how can I improve quality?
  - answer: Process the file in chunks, dispose of each `DjvuImage` after saving,
      and consider streaming pages rather than loading the entire document at once.
    question: How do I handle very large DJVU files efficiently?
  - answer: Visit the [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      or the [Aspose.Imaging Java Documentation](https://reference.aspose.com/imaging/java/)
      for comprehensive guides, API references, and sample projects. For community
      help, see [Aspose.Imaging Support](https://forum.aspose.com/c/imaging/14).
    question: Where can I find more Aspose.Imaging resources?
  type: FAQPage
title: Aspose Imaging Maven Dependency – แปลง DJVU เป็น BMP ใน Java
url: /th/java/format-conversion-export/export-djvu-pages-bmp-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# คู่มือฉบับสมบูรณ์: การใช้ Aspose.Imaging Java เพื่อส่งออกหน้า DJVU เป็นไฟล์ BMP

## บทนำ

ในยุคดิจิทัล การจัดการและแปลงรูปแบบเอกสารอย่างมีประสิทธิภาพเป็นสิ่งสำคัญสำหรับการแชร์เนื้อหาและการเก็บถาวรอย่างราบรื่น **Aspose Imaging Maven dependency** ทำให้การแปลงไฟล์ DJVU เป็นภาพ BMP ที่เข้าถึงได้ง่ายขึ้นโดยไม่ต้องเขียนโค้ดการพาร์สระดับต่ำ tutorial นี้จะพาคุณผ่านขั้นตอนการโหลดเอกสาร DJVU การกำหนดค่าตัวเลือกการส่งออก BMP การเลือกหน้าที่ต้องการ และการบันทึกแต่ละหน้าเป็นไฟล์ BMP แยกกัน—ทั้งหมดด้วยไม่กี่บรรทัดของ Java

**สิ่งที่คุณจะได้เรียนรู้**

- วิธีเพิ่ม Aspose Imaging Maven dependency ไปยังโปรเจกต์ของคุณ  
- วิธีโหลดและประมวลผลไฟล์ DJVU ด้วย Aspose.Imaging for Java  
- วิธีกำหนดค่าตัวเลือกการส่งออก BMP เช่น ความลึกสี  
- วิธีกำหนดช่วงหน้าที่กำหนดเองและส่งออกหน้าดังกล่าวเป็นไฟล์ BMP แยกกัน  

เมื่อจบคู่มือนี้ คุณจะสามารถรวมการแปลง DJVU‑to‑BMP เข้าไปในแอปพลิเคชัน Java ใด ๆ ได้ ปรับปรุงกระบวนการทำงานกับเอกสารและลดการพึ่งพาโปรแกรมดูไฟล์จากบุคคลที่สาม

## คำตอบอย่างรวดเร็ว
- **Maven artifact ที่เพิ่ม Aspose.Imaging คืออะไร?** `com.aspose:aspose-imaging`  
- **ฉันสามารถส่งออกเฉพาะหน้าที่เลือกได้หรือไม่?** ใช่, ใช้ `IntRange` เพื่อระบุดัชนีหน้า  
- **ความลึกสี BMP ที่แนะนำคืออะไร?** 32 บิตต่อพิกเซลสำหรับคุณภาพแบบไม่มีการสูญเสีย  
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** ต้องมี, ลิขสิทธิ์ที่ซื้อจะลบข้อจำกัดการประเมินผล  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 ขึ้นไป  

## Aspose Imaging Maven Dependency คืออะไร?
**Aspose Imaging Maven dependency** เป็นแพ็กเกจที่เข้ากันได้กับ Maven ซึ่งให้ API ครบวงจรสำหรับการอ่าน ประมวลผล และแปลงรูปแบบภาพและเอกสารกว่า 100 รูปแบบโดยตรงจากโค้ด Java การเพิ่ม dependency นี้ลงใน `pom.xml` ของคุณจะทำให้คุณเข้าถึงคลาสเช่น `Image`, `DjvuImage`, และ `IntRange` ได้ทันทีโดยไม่ต้องจัดการ JAR ด้วยตนเอง

## ทำไมต้องใช้ Aspose.Imaging สำหรับการแปลง DJVU เป็น BMP?
Aspose.Imaging รองรับ **รูปแบบเข้าและออกกว่า 100+ รูปแบบ** และสามารถประมวลผลไฟล์ DJVU ที่มีหลายร้อยหน้าโดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ลดการใช้ RAM ได้ถึง 70 % เมื่อเทียบกับวิธีการแบบธรรมดา ตัวเข้ารหัส BMP ของมันรักษาความแม่นยำของสีเต็มรูปแบบ ทำให้เหมาะสำหรับการสกัดภาพระดับการเก็บถาวร

## ข้อกำหนดเบื้องต้น
- **Aspose.Imaging for Java** เวอร์ชัน 25.5 (หรือใหม่กว่า)  
- **Java Development Kit** 8 หรือใหม่กว่า  
- ความคุ้นเคยกับเครื่องมือสร้าง Maven หรือ Gradle  
- ลิขสิทธิ์ Aspose.Imaging ที่ถูกต้อง (รุ่นทดลองใช้ได้สำหรับการประเมิน)

## การตั้งค่า Aspose.Imaging for Java

### ข้อมูลการติดตั้ง

**Maven:**  
เพิ่ม dependency ต่อไปนี้ลงใน `pom.xml` ของคุณ:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

**Gradle:**  
สำหรับผู้ใช้ Gradle ให้เพิ่มไลบรารีด้วยบรรทัดนี้ใน `build.gradle`:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

**Direct Download:**  
หรือคุณสามารถดาวน์โหลดรุ่นล่าสุดได้จาก [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/). คุณอาจดูหน้า [Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/) เพื่อดูประวัติเวอร์ชัน

### การรับลิขสิทธิ์

เพื่อใช้ Aspose.Imaging อย่างเต็มที่:

- **Free Trial:** เริ่มต้นด้วยรุ่นทดลองฟรีเพื่อสำรวจความสามารถ ([Start Your Free Trial](https://releases.aspose.com/imaging/java/))  
- **Temporary License:** รับลิขสิทธิ์ชั่วคราวหากต้องการเวลาประเมินเพิ่มเติม ([Get a Temporary License](https://purchase.aspose.com/temporary-license/))  
- **Purchase:** สำหรับการใช้งานระยะยาว พิจารณาซื้อไลเซนส์ ([Buy Aspose.Imaging](https://purchase.aspose.com/buy))

**Basic Initialization:**  
หลังจากตั้งค่าสภาพแวดล้อมและรับลิขสิทธิ์ (หากจำเป็น) ให้เริ่มต้น Aspose.Imaging ดังนี้:

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path/to/your/license/file.lic");
```

## วิธีแปลง DJVU เป็น BMP ด้วย Java?

โหลดไฟล์ DJVU ของคุณด้วย `Image.load("source.djvu")` กำหนดตัวเลือกการส่งออก BMP ระบุช่วงหน้าที่ต้องการ แล้วเรียก `save` สำหรับแต่ละหน้า – การแปลงทั้งหมดสามารถทำได้ในไม่ถึงสิบบรรทัดของโค้ด วิธีนี้จัดการความลึกสี การจัดทำดัชนีหน้า และการทำ I/O ของไฟล์โดยอัตโนมัติ ให้คุณโฟกัสที่ตรรกะธุรกิจแทนการพาร์สภาพ

### โหลดและประมวลผลไฟล์ DJVU

**Overview:**  
การโหลดไฟล์ DJVU เป็นขั้นตอนแรกในกระบวนการของเรา Aspose.Imaging for Java ทำให้ขั้นตอนนี้ง่ายขึ้น ช่วยให้คุณจัดการเอกสาร DJVU ได้อย่างสะดวก

เมธอด `Image.load` จะอ่านไฟล์ DJVU เข้าเป็นอ็อบเจกต์ `DjvuImage` ซึ่งเป็นตัวแทนของเอกสารหลายหน้าในหน่วยความจำ

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.djvu.DjvuImage;

String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "Sample.djvu";
try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
    // The DjVuImage object now holds the loaded DJVU file and can be processed further.
}
```

**Explanation:**  
- **`Image.load`:** โหลดไฟล์ DJVU ของคุณและคืนค่าเป็นอินสแตนซ์ `DjvuImage` เพื่อการประมวลผลต่อไป  

### ตั้งค่าตัวเลือกการส่งออกสำหรับรูปแบบ BMP

**Overview:**  
การกำหนดค่าตัวเลือกการส่งออกช่วยให้ไฟล์ BMP ที่ได้ตรงตามความต้องการคุณภาพของคุณ

`BmpOptions` ให้คุณกำหนดคุณสมบัติต่าง ๆ เช่น bits‑per‑pixel, compression, และ resolution ก่อนบันทึก

```java
import com.aspose.imaging.imageoptions.BmpOptions;

BmpOptions exportOptions = new BmpOptions();
exportOptions.setBitsPerPixel(32);
```

**Explanation:**  
- **`setBitsPerPixel`:** ตั้งค่าความลึกสีของภาพที่ส่งออก การใช้ 32 bits per pixel จะให้ไฟล์ BMP แบบไม่มีการสูญเสียคุณภาพและเหมาะสำหรับการเก็บถาวร  

### กำหนดช่วงหน้าที่จะส่งออก

**Overview:**  
การระบุหน้าที่ต้องการส่งออกช่วยให้คุณโฟกัสเฉพาะเนื้อหาที่สำคัญ

`IntRange` สร้างช่วงของดัชนีหน้าแบบศูนย์‑ฐาน; ในตัวอย่างนี้เราจะเลือกสองหน้าตแรก

```java
import com.aspose.imaging.IntRange;

IntRange range = new IntRange(0, 2);
```

**Explanation:**  
- **`IntRange`:** แสดงช่วงต่อเนื่องของหมายเลขหน้า ปรับค่าเริ่มต้นและสิ้นสุดเพื่อส่งออกส่วนย่อยของหน้าใดก็ได้ที่คุณต้องการ  

### ส่งออกหน้าที่ระบุเป็นไฟล์ BMP แยกกัน

**Overview:**  
ขั้นตอนสุดท้ายคือการส่งออกหน้าที่เลือกเป็นไฟล์ BMP แยกแต่ละไฟล์

`DjvuMultiPageOptions` กำหนดการส่งออกสำหรับแต่ละหน้า และ `image.save` จะเขียนไฟล์ BMP ไปยังไดเรกทอรีเป้าหมาย

```java
import com.aspose.imaging.imageoptions.DjvuMultiPageOptions;

int counter = 0;
for (int i : range.getRange()) {
    exportOptions.setMultiPageOptions(new DjvuMultiPageOptions(range.getArrayOneItemFromIndex(counter)));
    image.save("YOUR_OUTPUT_DIRECTORY" + (counter++) + ".bmp", exportOptions);
}
```

**Explanation:**  
- **`DjvuMultiPageOptions`:** เก็บข้อมูลช่วงหน้าและตัวเลือก BMP สำหรับการส่งออกหลายหน้า  
- **`image.save`:** บันทึกแต่ละหน้าที่เลือกเป็นไฟล์ BMP แยกบนดิสก์  

## การประยุกต์ใช้งานจริง

1. **การเก็บถาวร:** แปลงไฟล์ DJVU เป็น BMP เพื่อการเก็บและเรียกคืนที่ง่ายขึ้น  
2. **การแชร์เอกสาร:** แชร์ภาพแยกจากเอกสาร DJVU โดยไม่ต้องใช้โปรแกรมดูไฟล์พิเศษ  
3. **การพัฒนาเว็บ:** ใช้ภาพ BMP สำหรับโครงการเว็บที่ต้องการกราฟิกแบบไม่มีการสูญเสียคุณภาพ  
4. **การศึกษา:** ให้ผู้เรียนเข้าถึงรูปแบบภาพที่เข้าถึงง่ายสำหรับสื่อการศึกษา  
5. **การบูรณาการ:** ฝังกระบวนการแปลงนี้เข้าในแอปพลิเคชัน Java ขนาดใหญ่เพื่อเวิร์กโฟลว์อัตโนมัติ  

## พิจารณาด้านประสิทธิภาพ

- **เพิ่มประสิทธิภาพการใช้หน่วยความจำ:** ปิดอ็อบเจกต์ `DjvuImage` อย่างทันท่วงทีด้วย `close()` เพื่อปลดปล่อยทรัพยากรเนทีฟ  
- **การประมวลผลเป็นชุด:** ประมวลผลหลายไฟล์ DJVU ในลูปเพื่อกระจายค่าโอเวอร์เฮดของ I/O  
- **การประมวลผลแบบขนาน:** ใช้ `ExecutorService` ของ Java เพื่อแปลงหลายหน้าพร้อมกันบนเซิร์ฟเวอร์หลายคอร์  

## ปัญหาทั่วไปและวิธีแก้

- **OutOfMemoryError กับไฟล์ DJVU ขนาดใหญ่:** ใช้ `image.dispose()` หลังบันทึกแต่ละหน้าและพิจารณาเพิ่มขนาด heap ของ JVM ตามความจำเป็นเท่านั้น  
- **BMP คุณภาพต่ำ:** ตรวจสอบให้แน่ใจว่าได้ตั้ง `BmpOptions.setBitsPerPixel(32)` ค่าอื่น ๆ จะลดความแม่นยำของสี  
- **หน้าหายไปในผลลัพธ์:** ตรวจสอบว่าดัชนี `IntRange` ตรงกับจำนวนหน้าจริง (`djvuImage.getPages().size()`)  

## คำถามที่พบบ่อย

**Q: DJVU คือไฟล์ประเภทใด?**  
A: DJVU เป็นรูปแบบไฟล์ที่บีบอัดสูงออกแบบมาเพื่อเก็บเอกสารสแกน, ภาพ, และสิ่งพิมพ์หลายหน้าโดยคงคุณภาพการมองเห็นไว้

**Q: ฉันสามารถแปลงช่วงหน้าอื่นนอกจากสองหน้าตแรกได้หรือไม่?**  
A: ได้, ปรับพารามิเตอร์ของ `IntRange` เพื่อกำหนดช่วงเริ่มต้นและสิ้นสุดตามที่ต้องการ

**Q: ไฟล์ BMP ของฉันดูเบลอ—จะปรับคุณภาพอย่างไร?**  
A: เพิ่มค่าความลึกสีใน `BmpOptions` เป็น 32 และตรวจสอบให้แน่ใจว่าไม่มีการลดขนาดหน้าต้นฉบับ DJVU ระหว่างการโหลด

**Q: จะจัดการไฟล์ DJVU ขนาดใหญ่อย่างมีประสิทธิภาพอย่างไร?**  
A: ประมวลผลไฟล์เป็นชิ้น ๆ ปิด `DjvuImage` หลังบันทึกแต่ละหน้า และพิจารณาใช้การสตรีมหน้าต่าง ๆ แทนการโหลดเอกสารทั้งหมดพร้อมกัน

**Q: จะหาแหล่งข้อมูลเพิ่มเติมเกี่ยวกับ Aspose.Imaging ได้จากที่ไหน?**  
A: เยี่ยมชม [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/) หรือ [Aspose.Imaging Java Documentation](https://reference.aspose.com/imaging/java/) เพื่อดูคู่มือเชิงลึก, API reference, และตัวอย่างโครงการ สำหรับการช่วยเหลือจากชุมชน ดูที่ [Aspose.Imaging Support](https://forum.aspose.com/c/imaging/14)

**Last Updated:** 2026-06-18  
**Tested With:** Aspose.Imaging 25.5 for Java  
**Author:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [Convert DjVu to Grayscale PNG with Aspose.Imaging for Java | Format Conversion Tutorial](/imaging/java/format-conversion-export/export-djvu-grayscale-png-aspose-java/)  
- [Convert DjVu to TIFF in Java with Aspose.Imaging: Step-by-Step Guide](/imaging/java/format-conversion-export/load-export-djvu-tiff-aspose-imaging-java/)  
- [Convert DjVu to PDF using Aspose.Imaging for Java - Step-by-Step Guide](/imaging/java/image-loading-saving/convert-djvu-to-pdf-aspose-imaging-java/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}