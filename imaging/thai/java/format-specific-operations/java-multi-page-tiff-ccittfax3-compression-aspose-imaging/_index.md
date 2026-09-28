---
date: '2026-09-28'
description: เรียนรู้วิธีใช้ ccittfax3 compression java เพื่อสร้างไฟล์ TIFF แบบหลายหน้าด้วย
  Aspose.Imaging. สแกน, เก็บถาวร, และลดขนาดไฟล์อย่างมีประสิทธิภาพสำหรับกระบวนการทำงานของเอกสาร.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: ค้นพบขั้นตอนโดยละเอียดในการใช้ ccittfax3 compression java ร่วมกับ
  Aspose.Imaging เพื่อสร้างไฟล์ TIFF แบบหลายหน้าที่มีประสิทธิภาพสำหรับการสแกนและการเก็บถาวร.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: วิธีสร้างไฟล์ TIFF แบบหลายหน้าโดยใช้ ccittfax3 compression java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: วิธีสร้างไฟล์ TIFF แบบหลายหน้าโดยใช้ ccittfax3 compression java
url: /th/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เชี่ยวชาญการสร้างไฟล์ TIFF หลายหน้าโดยใช้การบีบอัด ccittfax3 ใน Java ด้วย Aspose.Imaging

## บทนำ

หากคุณต้องการจัดเก็บเอกสารสแกนจำนวนมากโดยคงขนาดไฟล์ให้เล็ก **ccittfax3 compression java** เป็นโซลูชันที่เหมาะสมที่สุด บทเรียนนี้จะแสดงวิธีสร้างไฟล์ TIFF หลายหน้าโดยใช้การบีบอัด CCITTFAX3 ใน Java ด้วย Aspose.Imaging คุณจะได้เรียนรู้ว่าการบีบอัดนี้ทำงานได้ดีเพียงใดสำหรับการสแกนแบบโมโนโครม วิธีการตั้งค่าห้องสมุด และวิธีเพิ่มแต่ละหน้าเป็นเฟรม

**สิ่งที่คุณจะได้เรียนรู้**
- วิธีเพิ่ม Aspose.Imaging ไปยังโครงการ Java
- วิธีตั้งค่า `TiffOptions` สำหรับการบีบอัด CCITTFAX3
- วิธีสร้าง `TiffImage` ปรับขนาดภาพต้นทาง และเพิ่มเป็นเฟรม
- วิธีบันทึกไฟล์ TIFF หลายหน้าสุดท้ายอย่างมีประสิทธิภาพ

มาดูการดำเนินการอย่างเต็มรูปแบบ

## คำตอบอย่างรวดเร็ว
- **What is the main benefit of CCITTFAX3 compression?** ลดขนาดไฟล์ได้สูงสุด 80 % สำหรับการสแกนสีดำ‑ขาว  
- **Which library provides built‑in support?** Aspose.Imaging สำหรับ Java รุ่น 25.5+  
- **Do I need a license for development?** ใบอนุญาตทดลองใช้ฟรีทำงานได้ครบทุกฟีเจอร์; จำเป็นต้องมีใบอนุญาตแบบชำระเงินสำหรับการใช้งานจริง  
- **Can I process hundreds of pages?** ได้—Aspose.Imaging สตรีมหน้า ทำให้การใช้หน่วยความจำต่ำ  
- **Is the code compatible with Java 11 and later?** แน่นอน; API รองรับ Java 8+

## ccittfax3 compression java คืออะไร?
`CCITTFAX3` เป็นอัลกอริทึมการบีบอัดแบบโมโนโครมแบบไม่มีการสูญเสียข้อมูลที่ออกแบบมาสำหรับแฟกซ์และภาพเอกสารสแกน มันเข้ารหัสพิกเซลแต่ละพิกเซลเป็นบิตเดียว ให้ผลลัพธ์คุณภาพสูงในขณะที่ลดขนาดไฟล์อย่างมาก—มักลดได้ 70‑80 % เมื่อเทียบกับ TIFF ที่ไม่ได้บีบอัด ทำให้เหมาะสำหรับการจัดเก็บเอกสารสีดำ‑ขาวที่ต้องคงความแม่นยำ

## ทำไมต้องใช้ Aspose.Imaging สำหรับงานนี้?
Aspose.Imaging รองรับ **100+** รูปแบบไฟล์เข้าและออก รวมถึง PDF, PNG, JPEG, และ TIFF สถาปัตยกรรมสตรีมของมันสามารถจัดการไฟล์ TIFF **หลายร้อยหน้า** ได้โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ทำให้เหมาะกับโครงการจัดเก็บเอกสารขนาดใหญ่

## ข้อกำหนดเบื้องต้น

- **Java Development Kit (JDK)** 8 หรือใหม่กว่า ต้องติดตั้ง
- **IDE** เช่น IntelliJ IDEA หรือ Eclipse
- **Maven** หรือ **Gradle** สำหรับการจัดการ dependencies
- ความรู้พื้นฐานของ Java (คลาส, อ็อบเจ็กต์, คอลเลกชัน)

## การตั้งค่า Aspose.Imaging สำหรับ Java

เพิ่มไลบรารีลงในไฟล์ build ของคุณ

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```  

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

### ดาวน์โหลดโดยตรง

คุณสามารถดาวน์โหลด JAR เวอร์ชันล่าสุดได้จาก [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### การรับใบอนุญาต

ใบอนุญาตทดลองใช้ฟรีพร้อมให้ดาวน์โหลดจาก [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/). สำหรับการใช้งานในผลิตภัณฑ์ ให้ซื้อใบอนุญาตถาวรหรือขอใบอนุญาตชั่วคราวที่ [Aspose Purchase](https://purchase.aspose.com/temporary-license/).

สำหรับการใช้งาน API อย่างละเอียด ดู [documentation](https://reference.aspose.com/imaging/java/) ของ Aspose.Imaging สำหรับ Java

### การเริ่มต้นพื้นฐาน

หลังจากเพิ่ม dependency แล้ว ให้เริ่มต้นไลบรารีตามตัวอย่างด้านล่าง

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## วิธีกำหนดค่า ccittfax3 compression java สำหรับ TIFF หลายหน้า?

`TiffOptions` เป็นคลาสที่กำหนดรูปแบบเอาต์พุตและการตั้งค่าการบีบอัดสำหรับไฟล์ TIFF โหลดอ็อบเจ็กต์ `TiffOptions` ด้วย enum `CCITTGroup3FaxCompression` แล้วตั้งค่าแหล่งไฟล์เอาต์พุต การกำหนดค่าสองขั้นตอนนี้เตรียมตัวเขียนสำหรับการบีบอัดโมโนโครมและรับประกันว่าหน้าทุกหน้าที่เพิ่มต่อมาจะถูกเข้ารหัสด้วยอัลกอริทึม CCITTFAX3 ทำให้ขนาดไฟล์ลดลงอย่างมีนัยสำคัญในขณะที่คงคุณภาพภาพ

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## วิธีสร้างอินสแตนซ์ TiffImage ใน Java?

`TiffImage` แทนเอกสาร TIFF หลายหน้าในหน่วยความจำและให้เมธอดสำหรับจัดการเฟรมของมัน ก่อนอื่นกำหนดความกว้างและความสูงที่ทุกหน้าจะใช้ร่วมกัน จากนั้นสร้างอินสแตนซ์ `TiffImage` ด้วย `TiffOptions` ที่สร้างไว้ก่อนหน้า อ็อบเจ็กต์ `TiffImage` ทำหน้าที่เป็นคอนเทนเนอร์สำหรับเฟรมแต่ละอัน ให้คุณเพิ่ม, ลบ หรือจัดลำดับหน้าใหม่ก่อนบันทึกไฟล์สุดท้าย

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## วิธีโหลดและปรับขนาดภาพต้นทางจากโฟลเดอร์?

กรองไดเรกทอรีเป้าหมายเพื่อหาไฟล์ JPEG, อ่านแต่ละภาพและปรับขนาดให้ตรงกับแคนวาสของ TIFF การปรับขนาดก่อนเพิ่มเฟรมช่วยลดการใช้หน่วยความจำและเร่งการบันทึก โดยการแปลงภาพต้นทางแต่ละภาพให้เป็นขนาดและรูปแบบพิกเซลที่ต้องการ คุณจะได้เลย์เอาต์หน้าที่สม่ำเสมอและหลีกเลี่ยงข้อผิดพลาดขณะรันไทม์เมื่อเพิ่มเฟรมลงในเอกสาร TIFF

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## วิธีเพิ่มแต่ละภาพเป็นเฟรมใน TIFF หลายหน้า?

`TiffFrame` เป็นอ็อบเจ็กต์ที่เก็บภาพหน้าเดียวและเมตาดาต้าที่เกี่ยวข้องภายใน TIFF ทำการวนลูปภาพที่ปรับขนาดแล้ว, สร้าง `TiffFrame` ใหม่และเพิ่มลงใน `TiffImage` แต่ละเฟรมจะกลายเป็นหน้าต่างๆ ในเอกสารสุดท้าย และไลบรารีจะจัดการอัปเดตเมตาดาต้าที่จำเป็นโดยอัตโนมัติ เช่น จำนวนหน้าและออฟเซ็ต เพื่อให้โครงสร้าง TIFF หลายหน้าถูกต้อง

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## วิธีบันทึกไฟล์ TIFF หลายหน้าสุดท้าย?

เรียกเมธอด `save` ของอินสแตนซ์ `TiffImage` พร้อมระบุเส้นทางเอาต์พุตที่ต้องการ ไลบรารีจะเขียนทุกเฟรมโดยใช้การบีบอัด CCITTFAX3, สตรีมข้อมูลไปยังดิสก์อย่างมีประสิทธิภาพและปิดทรัพยากรที่อยู่ภายใต้ หลังจากการบันทึกเสร็จ ไฟล์ที่ได้จะมีทุกหน้าที่บีบอัดตามที่กำหนด พร้อมใช้งานสำหรับการแจกจ่ายหรือการจัดเก็บ

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## การประยุกต์ใช้ในทางปฏิบัติ

- **Document archiving:** เก็บสัญญา, ใบแจ้งหนี้ หรือบันทึกทางกฎหมายที่สแกนไว้ด้วยพื้นที่จัดเก็บที่น้อยที่สุด  
- **Medical imaging:** บีบอัดภาพรังสีวิทยาโดยคงรายละเอียดการวินิจฉัย  
- **Print production:** สร้างงานพิมพ์หลายหน้าที่เครื่องพิมพ์สามารถรับได้โดยตรง  

## พิจารณาด้านประสิทธิภาพ

- ใช้ `ResizeOptions` ที่รักษาอัตราส่วนภาพเพื่อหลีกเลี่ยงการบิดเบือน  
- ปิดอ็อบเจ็กต์ `Image` แต่ละอันหลังจากเพิ่มเฟรมเพื่อคืนหน่วยความจำเนทีฟ  
- สำหรับชุดข้อมูลขนาดใหญ่มาก ให้ประมวลผลไฟล์ใน parallel streams และเขียนแต่ละส่วนของ TIFF อย่างอะซิงโครนัส  

## ข้อผิดพลาดทั่วไปและการแก้ไขปัญหา

- **Incorrect pixel format:** CCITTFAX3 ทำงานได้เฉพาะภาพ 1‑bit (สีดำ‑ขาว) ให้แปลงภาพสีเป็นระดับสีเทาก่อนปรับขนาด  
- **Memory leaks:** ควรเรียก `dispose()` บน `Image` ชั่วคราวเสมอ; มิฉะนั้นบัฟเฟอร์เนทีฟจะยังคงถูกจัดสรร  
- **File size not reduced:** ตรวจสอบให้แน่ใจว่าคุณสมบัติการบีบอัดของ `TiffOptions` ถูกตั้งค่า; มิฉะนั้นจะใช้ค่าเริ่มต้น (ไม่มีการบีบอัด)  

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้วิธีนี้กับภาพสีได้หรือไม่?**  
A: CCITTFAX3 จำกัดไว้ที่ข้อมูลโมโนโครม; สำหรับสีให้ใช้การบีบอัด JPEG หรือ LZW แทน  

**Q: Aspose.Imaging รองรับการสตรีมสำหรับ TIFF ขนาดใหญ่หรือไม่?**  
A: ใช่—ไลบรารีเขียนแต่ละเฟรมโดยตรงไปยังสตรีมเอาต์พุต ทำให้การใช้หน่วยความจำน้อยแม้จะมีหลายพันหน้า  

**Q: ฉันจะใช้ใบอนุญาตชั่วคราวแบบโปรแกรมได้อย่างไร?**  
A: โหลดไฟล์ `.lic` ด้วย `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.  

**Q: มีวิธีดูตัวอย่าง TIFF ก่อนบันทึกหรือไม่?**  
A: คุณสามารถเรนเดอร์แต่ละ `TiffFrame` ไปยัง `BufferedImage` แล้วแสดงในคอมโพเนนต์ Swing.  

**Q: เวอร์ชัน Java ใดที่รองรับอย่างเป็นทางการ?**  
A: Aspose.Imaging รองรับ Java 8 ถึง Java 21 รวมถึงรุ่น LTS  

## สรุป

ตอนนี้คุณมีเวิร์กโฟลว์ที่ครบถ้วนและพร้อมใช้งานในผลิตภัณฑ์สำหรับสร้างไฟล์ TIFF หลายหน้าด้วย **ccittfax3 compression java** โดยใช้ Aspose.Imaging โดยทำตามขั้นตอนข้างต้น คุณสามารถจัดเก็บคอลเลกชันเอกสารขนาดใหญ่ได้อย่างมีประสิทธิภาพพร้อมลดค่าใช้จ่ายในการจัดเก็บและคงคุณภาพภาพสูง สำรวจฟีเจอร์เพิ่มเติมของ Aspose.Imaging เช่น OCR, การจัดการเมตาดาต้า และการแปลงรูปแบบ เพื่อเพิ่มประสิทธิภาพให้กับกระบวนการประมวลผลเอกสารของคุณ

---

**Last Updated:** 2026-09-28  
**Tested With:** Aspose.Imaging 25.5 for Java  
**Author:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [วิธีสร้าง Multi-Page TIFF ด้วย Aspose.Imaging สำหรับ Java – คู่มือเต็ม](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [วิธีลดขนาดไฟล์ภาพด้วยการบีบอัด LZW ใน Java](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [แยกเฟรม Multi Page TIFF ด้วย Aspose.Imaging สำหรับ Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}