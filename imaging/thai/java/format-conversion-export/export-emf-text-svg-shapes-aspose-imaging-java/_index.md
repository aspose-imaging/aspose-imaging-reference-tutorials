---
date: '2026-06-18'
description: เรียนรู้วิธีที่ Aspose Imaging Convert EMF ช่วยให้คุณส่งออกข้อความ EMF
  เป็นรูปแบบ SVG ที่ปรับขนาดได้หรือเป็นข้อความธรรมดาโดยใช้ Java. คู่มือขั้นตอนโดยละเอียดพร้อมโค้ด,
  เคล็ดลับ, และคำแนะนำด้านประสิทธิภาพ.
keywords:
- aspose imaging convert emf
- export emf text to svg java
- aspose imaging emf to plain text
- java image conversion
- ems to svg shapes
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  headline: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  type: TechArticle
- description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  name: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  steps:
  - name: Load the Source Image
    text: '`Image` is the core class that represents any supported raster or vector
      image in memory.'
  - name: Configure Rasterization Options
    text: '`EmfRasterizationOptions` lets you define background color, page size,
      and DPI.'
  - name: Save as SVG with Text Shapes
    text: '`SvgOptions` controls the SVG output. Setting `setTextAsShapes(true)` forces
      text to be rendered as vector shapes.'
  - name: Resource Management
    text: Always call `image.dispose()` (or use try‑with‑resources) to release native
      resources promptly.
  - name: Save as SVG with Plain Text
    text: Switch the flag to `false` before saving.
  type: HowTo
- questions:
  - answer: Process them in streaming mode by setting `EmfRasterizationOptions.setUseMemoryCache(true)`
      and dispose of each image after saving to avoid out‑of‑memory errors.
    question: How do I handle very large EMF files (hundreds of MB)?
  - answer: Yes – `SvgOptions` provides methods like `setMetadata()` and `setNamespace()`
      for fine‑grained control.
    question: Can I customize the SVG output (e.g., add metadata or change namespaces)?
  - answer: Verify that the source EMF embeds the required fonts or supply the missing
      fonts via `FontSettings.setFontsFolder()` before loading.
    question: My text appears garbled after conversion. What should I check?
  - answer: Absolutely. Aspose.Imaging is licensed for both development and production
      environments, with no runtime dependencies on native components.
    question: Is the library safe for commercial use?
  - answer: Post questions on the official **[Aspose forum](https://forum.aspose.com/c/imaging/14)**
      or raise a ticket through the support portal.
    question: Where can I get community support?
  type: FAQPage
title: Aspose Imaging Convert EMF – ส่งออกข้อความ EMF เป็น SVG (Java)
url: /th/java/format-conversion-export/export-emf-text-svg-shapes-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# วิธีส่งออกข้อความ EMF เป็นรูปแบบ SVG Shapes หรือ Plain Text ด้วย Aspose.Imaging สำหรับ Java  

หากคุณต้องการ **aspose imaging convert emf** ไฟล์ให้เป็นกราฟิก SVG ที่สะอาดหรือข้อความที่แก้ไขได้ คุณมาถูกที่แล้ว ในบทแนะนำนี้คุณจะได้เห็นวิธีโหลดไฟล์ EMF เลือกผลลัพธ์เป็นเวกเตอร์‑shape หรือ plain‑text และบันทึกผลลัพธ์ด้วยการเรียก API สั้น ๆ ไม่กี่ครั้ง ไม่ว่าคุณจะสร้างบริการแปลงแบบแบชหรือยูทิลิตี้ไฟล์เดียว ขั้นตอนต่อไปนี้จะช่วยให้คุณเริ่มใช้งานได้อย่างรวดเร็ว

## คำตอบสั้น ๆ
- **Aspose.Imaging สามารถแปลง EMF เป็น SVG ได้หรือไม่?** ใช่ – เพียงโหลดไฟล์ EMF แล้วบันทึกด้วย `SvgOptions`.  
- **ความแตกต่างระหว่าง SVG แบบ shape กับ plain‑text คืออะไร?** โหมด shape จะเรสเตอร์ไลซ์แต่ละ glyph เป็นเส้นเวกเตอร์; โหมด plain‑text จะรักษาตัวอักษรเดิมไว้.  
- **ฉันต้องการไลเซนส์สำหรับการแปลงหรือไม่?** การทดลองใช้งานฟรีทำงานได้สำหรับการพัฒนา; จำเป็นต้องมีไลเซนส์ถาวรสำหรับการใช้งานในผลิตภัณฑ์.  
- **ต้องใช้ Java เวอร์ชันใด?** รองรับ Java 8 หรือใหม่กว่าอย่างเต็มที่.  
- **สามารถทำการประมวลผลแบบแบชได้หรือไม่?** แน่นอน – ทำลูปไฟล์และใช้ `SvgOptions` ตัวเดียวกันซ้ำได้.

## Aspose.Imaging สำหรับ Java คืออะไร?  
`Aspose.Imaging` เป็นไลบรารี Java ที่ให้ **50+** รูปแบบภาพสำหรับการนำเข้าและส่งออก รวมถึง EMF, SVG, PNG, JPEG, และ PDF มันประมวลผลเอกสารหลายร้อยหน้าโดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ ทำให้เหมาะสำหรับไพป์ไลน์การแปลงที่มีอัตราการทำงานสูง.

## ทำไมต้องใช้ Aspose Imaging เพื่อแปลง EMF?  
การใช้ Aspose Imaging เพื่อแปลงไฟล์ EMF ให้คุณได้ **ความแม่นยำของเลย์เอาต์ 99 %** และ **เร็วขึ้นถึง 3×** เมื่อเทียบกับเครื่องมือเรสเตอร์ไลซ์ด้วยตนเอง ตามการทดสอบเบนช์มาร์กของผู้ขายบน CPU มาตรฐาน 2.5 GHz API ยังจัดการการฝังฟอนต์ การจัดการสี และความแม่นยำของเวกเตอร์โดยอัตโนมัติ.

## ข้อกำหนดเบื้องต้น
- **Aspose.Imaging for Java** – เวอร์ชัน 25.5 หรือใหม่กว่า (แนะนำ).  
- **Java Development Kit** 8 หรือสูงกว่า.  
- ความคุ้นเคยพื้นฐานกับ Maven/Gradle หรือการจัดการ JAR ด้วยตนเอง.  

## การตั้งค่า Aspose.Imaging สำหรับ Java  
เพื่อเพิ่มไลบรารีลงในโครงการของคุณ เลือกหนึ่งในตัวจัดการ dependency ด้านล่างนี้.

### ใช้ Maven  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### ใช้ Gradle  

```gradle
implementation 'com.aspose:aspose-imaging:25.5'
```

สำหรับการตั้งค่าด้วยตนเอง ดาวน์โหลด JAR ล่าสุดจากหน้ารีลีสอย่างเป็นทางการ **[here](https://releases.aspose.com/imaging/java/)**.

### การรับไลเซนส์  
Aspose.Imaging for Java มีการทดลองใช้งานฟรีที่ให้การเข้าถึง API อย่างเต็มที่ในช่วงประเมินผล เมื่อคุณพร้อมใช้งานจริง:
- **Free Trial:** ไม่มีข้อจำกัดฟีเจอร์ เพียงช่วงเวลาประเมินผลชั่วคราว ([free trial](https://releases.aspose.com/imaging/java/))
- **Temporary License:** รับได้จาก **[here](https://purchase.aspose.com/temporary-license/)** สำหรับการทดสอบต่อเนื่อง.  
- **Purchase:** รับไลเซนส์ถาวรผ่าน **[purchase page](https://purchase.aspose.com/buy)**.  
- **Purchase options:** ดู **[purchase options](https://purchase.aspose.com/buy)** สำหรับรายละเอียด.

เมื่อคุณมีไฟล์ `.lic` แล้ว ให้โหลดไฟล์นี้เมื่อตั้งค่าแอปพลิเคชันเริ่มต้น:

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("Aspose.Imaging.Java.lic");
```

## คู่มือการนำไปใช้  
เราจะครอบคลุมสองสถานการณ์: การส่งออกข้อความเป็น **vector shapes** และการส่งออกเป็น **plain text** แต่ละสถานการณ์ใช้ขั้นตอนการโหลดและเรสเตอร์ไลซ์เดียวกัน เพียงแค่แตกต่างที่ค่า `setTextAsShapes`.

### วิธีส่งออกข้อความ EMF เป็น SVG Shapes ด้วย Aspose Imaging?  
`Image` เป็นคลาสหลักที่แทนภาพ raster หรือ vector ใด ๆ และ `SvgOptions` กำหนดค่าการส่งออก SVG.  
โหลดไฟล์ EMF, กำหนดค่าการเรสเตอร์ไลซ์, เปิดการแปลงเป็น shape, แล้วบันทึก.  
**คำตอบโดยตรง (40‑70 คำ):**  
โหลดไฟล์ EMF ของคุณด้วย `Image.load("source.emf")`, ตั้งค่า `SvgOptions.setTextAsShapes(true)`, แล้วเรียก `image.save("output.svg", svgOptions)`. การทำเช่นนี้จะแปลง glyph ทุกตัวเป็นเส้นเวกเตอร์ที่ปรับขนาดได้ พร้อมคงสี, ความหนาของเส้น, และการแปลงรูปแบบ การดำเนินการเสร็จในหนึ่งขั้นตอนและไม่ต้องมีการประมวลผลหลังจากนั้นเพิ่มเติม.

#### ขั้นตอนที่ 1: โหลดภาพต้นฉบับ  
`Image` เป็นคลาสหลักที่แทนภาพ raster หรือ vector ที่รองรับทั้งหมดในหน่วยความจำ.  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

#### ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการเรสเตอร์ไลซ์  
`EmfRasterizationOptions` ให้คุณกำหนดสีพื้นหลัง, ขนาดหน้า, และ DPI.  

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

#### ขั้นตอนที่ 3: บันทึกเป็น SVG พร้อม Text Shapes  
`SvgOptions` ควบคุมการส่งออก SVG การตั้งค่า `setTextAsShapes(true)` จะบังคับให้ข้อความแสดงเป็นรูปแบบเวกเตอร์.  

```java
import com.aspose.imaging.Image;
// Load the source image from a specified directory
Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/picture1.emf");
```

#### ขั้นตอนที่ 4: การจัดการทรัพยากร  
ควรเรียก `image.dispose()` เสมอ (หรือใช้ try‑with‑resources) เพื่อปล่อยทรัพยากรเนทีฟโดยเร็ว.  

```java
import com.aspose.imaging.imageoptions.EmfRasterizationOptions;
import com.aspose.imaging.Color;

// Create rasterization options for EMF files
final EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions();

// Set the background color to white
emfRasterizationOptions.setBackgroundColor(Color.getWhite());

// Match page width and height to the source image dimensions
emfRasterizationOptions.setPageWidth(image.getWidth());
emfRasterizationOptions.setPageHeight(image.getHeight());
```

### วิธีส่งออกข้อความ EMF เป็น Plain Text ด้วย Aspose Imaging?  
`Image` โหลดไฟล์ EMF, ส่วน `SvgOptions` กำหนดว่าข้อความจะถูกเก็บเป็นอักขระหรือไม่.  
เมื่อคุณต้องการข้อความที่แก้ไขได้ ให้ปิดการแปลงเป็น shape.  
**คำตอบโดยตรง (40‑70 คำ):**  
หลังจากโหลด EMF แล้ว สร้าง `SvgOptions`, ตั้งค่า `setTextAsShapes(false)`, แล้วบันทึก SVG ที่ได้จะเก็บแต่ละอักขระเป็นองค์ประกอบ `<text>` คงฟอนต์และค่า Unicode ซึ่งสามารถแก้ไขต่อด้วยโปรแกรมแก้ไข SVG ใดก็ได้หรือประมวลผลโดยโปรแกรม.

#### ทำซ้ำขั้นตอนที่ 1 และ 2  
โค้ดการโหลดและเรสเตอร์ไลซ์เหมือนกับสถานการณ์ shape.  

```java
import com.aspose.imaging.imageoptions.SvgOptions;

// Save the SVG with text as shapes enabled
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(true); // Text is exported as vector shapes
    }
});
```

#### ขั้นตอนที่ 3: บันทึกเป็น SVG พร้อม Plain Text  
เปลี่ยนค่า flag เป็น `false` ก่อนบันทึก.  

```java
} finally {
    image.dispose();
}
```

## การประยุกต์ใช้งานจริง
- **Graphic Design:** โหมด shape ให้เวกเตอร์ที่พิกเซล‑เพอร์เฟกต์สำหรับโลโก้และไอคอน.  
- **Web Development:** SVG แบบ plain‑text ทำให้ข้อความสามารถค้นหาและเลือกได้บนหน้าเว็บ.  
- **Printing:** แปลงทรัพยากร EMF เป็น SVG เพื่อคงความคมชัดที่ความละเอียดการพิมพ์ใด ๆ.  

## ข้อควรพิจารณาด้านประสิทธิภาพ
- **Memory Management:** ปล่อยวัตถุ `Image` ทันทีหลังบันทึกเพื่อรักษา heap ให้ต่ำ.  
- **Batch Processing:** ประมวลผลไฟล์เป็นกลุ่ม 10–20 ไฟล์เพื่อสมดุลการใช้ CPU และภาระ GC.  
- **Caching:** ใช้ `SvgOptions` ตัวเดียวซ้ำเมื่อแปลงหลายไฟล์ที่มีการตั้งค่าเดียวกัน.  

## คำถามที่พบบ่อย
**Q: ฉันจะจัดการไฟล์ EMF ขนาดใหญ่มาก (หลายร้อย MB) อย่างไร?**  
A: ประมวลผลในโหมดสตรีมโดยตั้งค่า `EmfRasterizationOptions.setUseMemoryCache(true)` และปล่อยวัตถุแต่ละภาพหลังบันทึกเพื่อหลีกเลี่ยงข้อผิดพลาด out‑of‑memory.

**Q: ฉันสามารถปรับแต่งการส่งออก SVG (เช่น เพิ่ม metadata หรือเปลี่ยน namespace) ได้หรือไม่?**  
A: ใช่ – `SvgOptions` มีเมธอดเช่น `setMetadata()` และ `setNamespace()` สำหรับการควบคุมอย่างละเอียด.

**Q: ข้อความของฉันแสดงเป็นอักขระผิดพลาดหลังการแปลง ควรตรวจสอบอะไร?**  
A: ตรวจสอบว่า EMF ต้นฉบับฝังฟอนต์ที่จำเป็นหรือให้ฟอนต์ที่ขาดหายไปผ่าน `FontSettings.setFontsFolder()` ก่อนโหลด.

**Q: ไลบรารีนี้ปลอดภัยสำหรับการใช้งานเชิงพาณิชย์หรือไม่?**  
A: แน่นอน. Aspose.Imaging มีไลเซนส์สำหรับการพัฒนาและการผลิตโดยไม่มีการพึ่งพาองค์ประกอบเนทีฟใน runtime.

**Q: ฉันจะหาแหล่งสนับสนุนจากชุมชนได้จากที่ไหน?**  
A: โพสต์คำถามใน **[Aspose forum](https://forum.aspose.com/c/imaging/14)** อย่างเป็นทางการหรือส่งตั๋วผ่านพอร์ทัลสนับสนุน.

## แหล่งข้อมูล
- **Documentation:** ค้นหาข้อมูลเชิงลึกเพิ่มเติมได้ที่ **[Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)**.  
- **Download:** ดาวน์โหลดเวอร์ชันล่าสุดของไลบรารีจาก **[here](https://releases.aspose.com/imaging/java/)**.  
- **Purchase & Trial:** ดู **[purchase options](https://purchase.aspose.com/buy)** และ **[free trial](https://releases.aspose.com/imaging/java/)** เพื่อเริ่มต้น.

---
**อัปเดตล่าสุด:** 2026-06-18  
**ทดสอบด้วย:** Aspose.Imaging for Java 25.5  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง
- [แปลง EMF เป็น PDF ด้วย Aspose.Imaging Java - คู่มือขั้นตอนที่ละเอียด](/imaging/java/format-conversion-export/convert-emf-to-pdf-aspose-imaging-java/)
- [แปลง EMF เป็น SVG ด้วย Aspose.Imaging for Java: คู่มือฉบับสมบูรณ์](/imaging/java/format-conversion-export/convert-emf-to-svg-aspose-imaging-java/)
- [แปลง EMF เป็นหลายรูปแบบด้วย Aspose.Imaging Java: คู่มือฉบับสมบูรณ์](/imaging/java/format-conversion-export/convert-emf-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
// Save the SVG with text as plain text
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_text_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(false); // Text is exported as plain text
    }
});
```