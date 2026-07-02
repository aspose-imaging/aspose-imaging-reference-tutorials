---
date: '2026-05-29'
description: เรียนรู้วิธีแปลง EMF เป็น BMP, JPEG, TIFF, PNG และอื่น ๆ ด้วย Aspose.Imaging
  for Java. รวมตัวเลือก rasterization options, การตั้งค่า Gradle dependency, และ performance
  tips.
keywords:
- convert emf to bmp
- aspose gradle dependency
- how to convert emf
- convert emf to jpeg
- convert emf to tiff
- emf to png java
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to convert EMF to BMP, JPEG, TIFF, PNG and more using Aspose.Imaging
    for Java. Includes rasterization options, Gradle dependency setup, and performance
    tips.
  headline: Convert EMF to BMP and Other Formats with Aspose.Imaging Java
  type: TechArticle
- description: Learn how to convert EMF to BMP, JPEG, TIFF, PNG and more using Aspose.Imaging
    for Java. Includes rasterization options, Gradle dependency setup, and performance
    tips.
  name: Convert EMF to BMP and Other Formats with Aspose.Imaging Java
  steps:
  - name: '**Install via Dependency Management:**'
    text: '**Install via Dependency Management:**'
  - name: '**Direct Download:**'
    text: '**Direct Download:**'
  - name: '**License Acquisition:**'
    text: '**License Acquisition:**'
  - name: '**Basic Initialization:**'
    text: '**Basic Initialization:**'
  - name: '**Web Design:** Convert EMF to WebP for up to **35 % smaller** file sizes
      while keeping visual quality.'
    text: '**Web Design:** Convert EMF to WebP for up to **35 % smaller** file sizes
      while keeping visual quality.'
  - name: '**Graphic Design:** Use TIFF or PSD when you need lossless layers for print
      production.'
    text: '**Graphic Design:** Use TIFF or PSD when you need lossless layers for print
      production.'
  - name: '**Archiving:** Store high‑resolution JPEG 2000 files to achieve superior
      compression without noticeable artifacts.'
    text: '**Archiving:** Store high‑resolution JPEG 2000 files to achieve superior
      compression without noticeable artifacts.'
  - name: '**Multimedia Projects:** Generate GIFs for lightweight animations in web
      apps.'
    text: '**Multimedia Projects:** Generate GIFs for lightweight animations in web
      apps.'
  type: HowTo
- questions:
  - answer: BMP, GIF, JPEG, JPEG 2000, PNG, PSD, TIFF, and WebP are fully supported.
    question: What image formats can I convert EMF files into with Aspose.Imaging
      for Java?
  - answer: A trial works for up to 10 MB per file; a purchased license removes all
      limits.
    question: Do I need a license for batch conversions?
  - answer: Use a fixed thread pool, enable embedded rasterization, and reuse a single
      `EmfRasterizationOptions` instance across calls.
    question: How can I improve conversion speed for thousands of EMF files?
  - answer: Raster formats inherently discard vector data; however, you can embed
      the original EMF as a metadata stream in TIFF using `tiffOptions.setCompression(TiffCompression.NONE)`.
    question: Is there a way to preserve vector metadata when converting to raster?
  - answer: Visit the official [documentation](https://reference.aspose.com/imaging/java/)
      for comprehensive class references and examples. The [Reference Guide](https://reference.aspose.com/imaging/java/)
      provides deeper insights.
    question: Where can I find more detailed API documentation?
  type: FAQPage
title: แปลง EMF เป็น BMP และรูปแบบอื่น ๆ ด้วย Aspose.Imaging Java
url: /th/java/format-conversion-export/convert-emf-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# แปลง EMF เป็น BMP และรูปแบบอื่นด้วย Aspose.Imaging Java

## บทนำ

การแปลงภาพ **EMF** (Enhanced Metafile) ไปเป็น **BMP**, JPEG, PNG, TIFF, WebP และรูปแบบแรสเตอร์อื่น ๆ เป็นความต้องการทั่วไปสำหรับนักพัฒนาที่สร้างแอปพลิเคชันที่เน้นกราฟิก ด้วย **Aspose.Imaging for Java** คุณสามารถทำการแปลงเหล่านี้ได้ด้วยเพียงไม่กี่บรรทัดของโค้ดพร้อมคงความแม่นยำสูง บทเรียนนี้จะพาคุณผ่านการติดตั้งไลบรารี การกำหนดค่า `EmfRasterizationOptions` และการแปลงไฟล์ EMF ไปยังหลายรูปแบบผลลัพธ์

**สิ่งที่คุณจะทำได้:**
- ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์เพื่อการเรนเดอร์ EMF ที่แม่นยำ  
- แปลง EMF เป็น BMP, GIF, JPEG, PNG, TIFF, และอื่น ๆ  
- ปรับการใช้หน่วยความจำสำหรับไฟล์เวกเตอร์ขนาดใหญ่  

ก่อนที่เราจะเริ่ม โปรดตรวจสอบว่าคุณคุ้นเคยกับพื้นฐานของ Java และมี Maven หรือ Gradle พร้อมใช้งานสำหรับการจัดการ dependencies. มาเริ่มกันเลย!

## คำตอบสั้น
- **ฉันจะเพิ่ม Aspose.Imaging ไปยังโครงการ Gradle อย่างไร?** เพิ่ม dependency `aspose-imaging` ในไฟล์ `build.gradle` ของคุณ.  
- **เมธอดใดทำการแปลง?** ใช้ `Image.save(outputPath, ImageFormat)` หลังจากทำการเรสเตอร์ไลซ์ด้วย `EmfRasterizationOptions`.  
- **ฉันสามารถแปลง EMF โดยตรงเป็น BMP ได้หรือไม่?** ได้ – ตั้งค่า `BmpOptions` แล้วเรียก `save`.  
- **ต้องการไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** รุ่นทดลองใช้ได้สำหรับการประเมิน; ไลเซนส์ถาวรจะลบข้อจำกัดการประเมิน.  
- **วิธีที่เร็วที่สุดในการจัดการไฟล์ EMF ขนาดใหญ่คืออะไร?** เปิดใช้งาน `setUseEmbeddedRasterization(true)` และประมวลผลภาพในรูปแบบสตรีมเพื่อหลีกเลี่ยงการโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ.

## การแปลง emf เป็น bmp คืออะไร?
`convert emf to bmp` อธิบายกระบวนการเรสเตอร์ไลซ์ไฟล์เวกเตอร์ EMF ให้เป็นภาพ BMP bitmap โดยใช้ไลบรารีโปรแกรมเช่น Aspose.Imaging การแปลงนี้ทำให้กราฟิกที่ปรับขนาดได้กลายเป็นรูปแบบพิกเซลที่เหมาะกับระบบเก่าและการประมวลผลภาพระดับต่ำ

## ทำไมต้องใช้ Aspose.Imaging สำหรับ Java?
Aspose.Imaging รองรับ **50+** รูปแบบอินพุตและเอาต์พุต รวมถึง BMP, GIF, JPEG, PNG, TIFF, PSD, J2K, และ WebP และสามารถจัดการไฟล์ EMF หลายร้อยหน้าโดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ทำให้การประมวลผลเร็วขึ้นถึง **30 %** เมื่อเทียบกับหลายทางเลือกโอเพนซอร์ส

## ข้อกำหนดเบื้องต้น

### ไลบรารีและ dependencies ที่จำเป็น
ตรวจสอบให้แน่ใจว่าสภาพแวดล้อมการพัฒนาของคุณมีไลบรารี Aspose.Imaging for Java อยู่

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
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### ความต้องการการตั้งค่าสภาพแวดล้อม
- Java Development Kit (JDK) 8 หรือสูงกว่า  
- IDE (IntelliJ IDEA, Eclipse, VS Code) หรือเครื่องมือแก้ไขข้อความอย่างง่าย

### ความรู้เบื้องต้นที่จำเป็น
ความคุ้นเคยกับการจัดการ classpath ของ Java และการดำเนินการไฟล์ I/O พื้นฐาน

## การตั้งค่า Aspose.Imaging สำหรับ Java

เพื่อเริ่มต้น ให้เพิ่มไลบรารี Aspose.Imaging ไปยังโครงการของคุณและรับไลเซนส์

1. **ติดตั้งผ่านการจัดการ Dependency:**  
   รวม snippet dependency ที่แสดงด้านบนสำหรับ Maven หรือ Gradle.  
2. **ดาวน์โหลดโดยตรง:**  
   ดาวน์โหลดเวอร์ชันล่าสุดโดยตรงจาก [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).  
   ตรวจสอบ [Latest Releases](https://releases.aspose.com/imaging/java/) สำหรับการอัปเดต.  
   คุณสามารถเริ่มทดลองใช้ฟรีได้ที่นี่: [Start Your Free Trial](https://releases.aspose.com/imaging/java/).  
3. **การรับไลเซนส์:**  
   ใช้การทดลองฟรีเพื่อสำรวจฟีเจอร์ จากนั้นซื้อไลเซนส์ที่ [Buy Aspose.Imaging](https://purchase.aspose.com/buy) หรือรับคีย์ชั่วคราวผ่านหน้า [Get a Temporary License](https://purchase.aspose.com/temporary-license/).  
   สำหรับการสนับสนุนจากชุมชน ให้เยี่ยมชม [Aspose forum](https://forum.aspose.com/c/imaging/14).  
4. **การเริ่มต้นพื้นฐาน:**  
   วางไฟล์ไลเซนส์ของคุณ (`Aspose.Imaging.lic`) ใน classpath และโหลดมันเมื่อแอปพลิเคชันเริ่มทำงาน.  
   สามารถดูการใช้ API อย่างละเอียดได้ใน [Reference Guide](https://reference.aspose.com/imaging/java/).

## วิธีแปลง EMF เป็น BMP?
เพื่อแปลงไฟล์ EMF เป็น BMP คุณต้องโหลดภาพเวกเตอร์ก่อน จากนั้นสร้างอ็อบเจ็กต์ `EmfRasterizationOptions` ที่กำหนดขนาดการเรนเดอร์และพื้นหลัง และสุดท้ายให้ `BmpOptions` ที่ระบุการตั้งค่าเฉพาะของ BMP ก่อนเรียก `save`. `EmfRasterizationOptions` ควบคุมวิธีการเรสเตอร์ไลซ์ข้อมูลเวกเตอร์ ในขณะที่ `BmpOptions` เก็บพารามิเตอร์ของฟอร์แมต BMP เช่น บิตต่อพิกเซล

```text
Load the EMF with `Image.load("source.emf")`.  
Create a `BmpOptions` object, set `EmfRasterizationOptions` (background, size), and invoke `save("output.bmp", bmpOptions)`.  
```

บล็อกโค้ดด้านล่าง (placeholder) แสดงการเรียก API อย่างแม่นยำ

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.imageoptions.EmfRasterizationOptions;

// Configure rasterization options for EMF conversion
com.aspose.imaging.imageoptions.EmfRasterizationOptions emfRasterizationOptions = new com.aspose.imaging.imageoptions.EmfRasterizationOptions();
emfRasterizationOptions.setBackgroundColor(Color.getPapayaWhip()); // Set a pleasant background color
emfRasterizationOptions.setPageWidth(300); // Define the width of the rasterized image
emfRasterizationOptions.setPageHeight(300); // Define the height of the rasterized image
```

## วิธีแปลง EMF เป็น GIF?
การแปลง EMF เป็น GIF ทำตามขั้นตอนสองขั้นตอนเดียวกับการแปลงเป็น BMP; คุณแทนที่ตัวเลือกการเรสเตอร์ไลซ์ด้วยอ็อบเจ็กต์ `GifOptions` ที่กำหนดพารามิเตอร์เฉพาะของ GIF เช่น ความหน่วงของเฟรมและจำนวนลูป `GifOptions` บอก Aspose.Imaging ให้สร้าง GIF แบบคงที่หรือแบบเคลื่อนไหวตามการตั้งค่าที่ให้

```text
Instantiate `GifOptions`, assign the same `EmfRasterizationOptions`, then call `save("output.gif", gifOptions)`.  
```

```java
import com.aspose.imaging.fileformats.emf.EmfImage;
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.BmpOptions;

// Specify the input file path and load the image
String filePath = "Picture1.emf"; 
try (EmfImage image = (EmfImage) Image.load("YOUR_DOCUMENT_DIRECTORY" + filePath)) {
    BmpOptions bmpOptions = new BmpOptions();
    bmpOptions.setVectorRasterizationOptions(emfRasterizationOptions); // Apply rasterization options
    image.save("YOUR_OUTPUT_DIRECTORY" + filePath + "_out.bmp", bmpOptions); // Save the BMP file
}
```

## วิธีแปลง EMF เป็น JPEG?
เมื่อแปลงเป็น JPEG หลังจากเรสเตอร์ไลซ์ด้วย `EmfRasterizationOptions` คุณสร้างอ็อบเจ็กต์ `JpegOptions` ที่สามารถตั้งค่า property `Quality` เพื่อปรับสมดุลระหว่างขนาดการบีบอัดและความคมชัดของภาพ `JpegOptions` รวมการตั้งค่าเข้ารหัสเฉพาะของ JPEG ทำให้คุณปรับแต่งผลลัพธ์สำหรับการใช้งานบนเว็บหรือการเก็บถาวรได้อย่างละเอียด

```text
Create `JpegOptions`, define `Quality` (e.g., 90), reuse the rasterization settings, and save as JPEG.  
```

```java
import com.aspose.imaging.imageoptions.GifOptions;

try (EmfImage image = (EmfImage) Image.load("YOUR_DOCUMENT_DIRECTORY" + filePath)) {
    GifOptions gifOptions = new GifOptions();
    gifOptions.setVectorRasterizationOptions(emfRasterizationOptions); // Apply rasterization options
    image.save("YOUR_OUTPUT_DIRECTORY" + filePath + "_out.gif", gifOptions); // Save the GIF file
}
```

## วิธีแปลง EMF เป็น PNG, TIFF, WebP, และอื่น ๆ?
อ็อบเจ็กต์การเรสเตอร์ไลซ์เดียวกันสามารถใช้ซ้ำได้สำหรับรูปแบบแรสเตอร์ใด ๆ; คุณเพียงสร้างอินสแตนซ์ของคลาสตัวเลือกที่เหมาะสม (`PngOptions`, `TiffOptions`, `WebPOptions` เป็นต้น) แล้วส่งให้ `save`. แต่ละคลาสตัวเลือกกำหนดพารามิเตอร์เฉพาะของฟอร์แมต—for ตัวอย่างเช่น `PngOptions` ให้คุณเลือกประเภทสี ในขณะที่ `TiffOptions` ให้คุณตั้งค่าชนิดการบีบอัด

```text
Select the appropriate Options class, configure any format‑specific settings, then invoke `save`.  
```

```java
import com.aspose.imaging.imageoptions.JpegOptions;

try (EmfImage image = (EmfImage) Image.load("YOUR_DOCUMENT_DIRECTORY" + filePath)) {
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setVectorRasterizationOptions(emfRasterizationOptions); // Apply rasterization options
    image.save("YOUR_OUTPUT_DIRECTORY" + filePath + "_out.jpeg", jpegOptions); // Save the JPEG file
}
```

## การประยุกต์ใช้งานจริง

1. **การออกแบบเว็บ:** แปลง EMF เป็น WebP เพื่อให้ขนาดไฟล์เล็กลงสูงสุด **35 %** พร้อมคงคุณภาพภาพ  
2. **การออกแบบกราฟิก:** ใช้ TIFF หรือ PSD เมื่อคุณต้องการเลเยอร์แบบไม่มีการสูญเสียสำหรับการผลิตงานพิมพ์  
3. **การเก็บถาวร:** เก็บไฟล์ JPEG 2000 ความละเอียดสูงเพื่อให้ได้การบีบอัดที่เหนือกว่าโดยไม่มีศิลปะที่สังเกตได้  
4. **โครงการมัลติมีเดีย:** สร้าง GIF สำหรับแอนิเมชันเบาที่ใช้ในเว็บแอป  

## พิจารณาด้านประสิทธิภาพ

- **การจัดการหน่วยความจำ:** สำหรับไฟล์ EMF ที่ใหญ่กว่า 20 MB ให้เปิดใช้งาน `setUseEmbeddedRasterization(true)` เพื่อประมวลผลเป็นสตรีมแทนการใช้วัตถุเต็มในหน่วยความจำ  
- **การทำงานหลายเธรด:** Aspose.Imaging ปลอดภัยต่อการทำงานหลายเธรด; คุณสามารถทำการแปลงแบบขนานผ่าน thread pool สำหรับงานแบตช์  
- **การจัดการข้อยกเว้น:** ห่อการเรียกแปลงในบล็อก try‑catch เพื่อจับ `ImageProcessingException` และให้ตรรกะสำรอง  

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|----------|
| **พื้นหลังว่าง** | ตัวเลือกการเรสเตอร์ไลซ์ไม่มีสีพื้นหลัง | ตั้งค่า `backgroundColor` ใน `EmfRasterizationOptions` เป็น `Color.WHITE`. |
| **ขนาดไม่ถูกต้อง** | ไม่ได้ระบุความกว้าง/ความสูง | ใช้ `setPageWidth` และ `setPageHeight` ให้ตรงกับขนาดผลลัพธ์ที่ต้องการ. |
| **ข้อผิดพลาดหน่วยความจำเต็ม** | ไฟล์ EMF ขนาดใหญ่ประมวลผลในเธรดเดียว | เปิดใช้งานโหมดสตรีมและเพิ่มขนาด heap ของ JVM (`-Xmx2g`). |

## คำถามที่พบบ่อย

**Q: ฉันสามารถแปลงไฟล์ EMF ไปเป็นรูปแบบภาพใดได้บ้างด้วย Aspose.Imaging for Java?**  
A: BMP, GIF, JPEG, JPEG 2000, PNG, PSD, TIFF, and WebP are fully supported.

**Q: ฉันต้องการไลเซนส์สำหรับการแปลงเป็นชุดหรือไม่?**  
A: รุ่นทดลองใช้ได้สำหรับไฟล์ขนาดสูงสุด 10 MB ต่อไฟล์; ไลเซนส์ที่ซื้อจะลบข้อจำกัดทั้งหมด

**Q: ฉันจะเพิ่มความเร็วการแปลงสำหรับไฟล์ EMF จำนวนหลายพันไฟล์ได้อย่างไร?**  
A: ใช้ thread pool คงที่, เปิดใช้งาน embedded rasterization, และใช้ `EmfRasterizationOptions` ตัวเดียวซ้ำหลายครั้งในการเรียก

**Q: มีวิธีใดที่จะรักษาเมตาดาต้าเวกเตอร์เมื่อแปลงเป็นแรสเตอร์หรือไม่?**  
A: รูปแบบแรสเตอร์โดยธรรมชาติจะละทิ้งข้อมูลเวกเตอร์; อย่างไรก็ตาม คุณสามารถฝัง EMF ดั้งเดิมเป็นสตรีมเมตาดาต้าใน TIFF โดยใช้ `tiffOptions.setCompression(TiffCompression.NONE)`.

**Q: ฉันจะหาเอกสาร API ที่ละเอียดเพิ่มเติมได้จากที่ไหน?**  
A: เยี่ยมชม [documentation](https://reference.aspose.com/imaging/java/) อย่างเป็นทางการสำหรับอ้างอิงคลาสและตัวอย่างอย่างครบถ้วน. [Reference Guide](https://reference.aspose.com/imaging/java/) ให้ข้อมูลเชิงลึกเพิ่มเติม

---

**อัปเดตล่าสุด:** 2026-05-29  
**ทดสอบด้วย:** Aspose.Imaging 24.12 for Java  
**ผู้เขียน:** Aspose

```java
// Example: Convert to PNG
import com.aspose.imaging.imageoptions.PngOptions;

try (EmfImage image = (EmfImage) Image.load("YOUR_DOCUMENT_DIRECTORY" + filePath)) {
    PngOptions pngOptions = new PngOptions();
    pngOptions.setVectorRasterizationOptions(emfRasterizationOptions); // Apply rasterization options
    image.save("YOUR_OUTPUT_DIRECTORY" + filePath + "_out.png", pngOptions); // Save the PNG file
}
```

## บทแนะนำที่เกี่ยวข้อง

- [แปลง JPEG เป็น PNG ด้วย Aspose.Imaging Java: คู่มือสำหรับนักพัฒนา](/imaging/java/format-conversion-export/convert-jpeg-to-png-aspose-imaging-java/)
- [Aspose.Imaging Java: บีบอัดและแปลง PNG เป็น TIFF ด้วย Deflate](/imaging/java/compression-optimization/master-image-compression-conversion-aspose-imaging-java/)
- [การแปลง TIFF เป็น BMP ด้วย Aspose.Imaging for Java](/imaging/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}