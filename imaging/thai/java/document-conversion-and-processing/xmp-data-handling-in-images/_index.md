---
date: 2026-05-18
description: เรียนรู้วิธีใช้ไลบรารีการประมวลผลภาพ Java Aspose.Imaging เพื่อฝังและดึงข้อมูลเมตาดาต้า
  XMP ในภาพ ด้วย step‑by‑step code
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: การจัดการข้อมูล XMP ในภาพ
schemas:
- author: Aspose
  dateModified: '2026-05-18'
  description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  headline: 'Java Image Processing Library: XMP with Aspose.Imaging'
  type: TechArticle
- description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  name: 'Java Image Processing Library: XMP with Aspose.Imaging'
  steps:
  - name: Specify Image Size and Tiff Options
    text: First, define the directory where your image will be stored and create a
      `Rectangle` to specify the size of the image. In this example, we use a TIFF
      image with certain options. `TiffOptions` configures format‑specific settings
      for the TIFF image.
  - name: Create a New Image
    text: Now, create a new image with the specified options. This image will be used
      to store the XMP metadata. `TiffImage` represents a TIFF image object, and `TiffFrame`
      defines an individual frame within it.
  - name: Create XMP Header and Trailer
    text: Create instances of XMP‑Header and XMP‑Trailer for your XMP metadata. These
      headers and trailers help define the metadata structure. `XmpHeaderPi` and `XmpTrailerPi`
      represent the XMP packet’s opening and closing sections.
  - name: Create XMP Meta Information
    text: Now, create an instance of XMP meta to set different attributes. You can
      add information like the author and description. `XmpMeta` holds the core metadata
      fields such as author and description.
  - name: Create XMP Packet Wrapper
    text: '`XmpPacketWrapper` is the container that holds the XMP header, trailer,
      and meta information in a single packet. It ensures the packet conforms to the
      XMP specification. `XmpPacketWrapper` packages the header, meta, and trailer
      into a single XMP packet.'
  - name: Add Photoshop Package
    text: To store Photoshop‑specific information, create a Photoshop package and
      set its attributes, such as city, country, and color mode. Then, add this package
      to the XMP metadata. `PhotoshopPackage` stores Photoshop‑specific metadata like
      city, country, and color mode.
  - name: Add Dublin Core Package
    text: For more general information, like author, title, and additional values,
      create a DublinCore package and set its attributes. Add this package to the
      XMP metadata as well. `DublinCorePackage` contains standard Dublin Core fields
      such as title, creator, and keywords.
  - name: Update XMP Metadata in the Image
    text: Update the XMP metadata into the image using the `setXmpData` method. This
      call writes the XMP packet into the image’s metadata section. `setXmpData` writes
      the XMP packet into the image’s metadata section.
  - name: Save the Image
    text: You can now save the image with the embedded XMP metadata on the disk or
      in a memory stream.
  - name: Load the Image and Retrieve XMP Metadata
    text: To retrieve the XMP metadata from the image, load the image from the memory
      stream or disk and access the XMP data via the `getXmpData` method. `getXmpData`
      reads the embedded XMP packet from the image. Congratulations! You've successfully
      learned how to handle XMP data in images using Aspose.Imagin
  type: HowTo
- questions:
  - answer: XMP is an XML‑based standard for embedding descriptive information directly
      inside files, enabling consistent metadata across applications.
    question: What is XMP metadata?
  - answer: It lets you tag images with author, copyright, keywords, and custom data,
      improving searchability and asset management without external databases.
    question: Why is XMP metadata important?
  - answer: Yes, Aspose.Imaging for Java provides methods to modify existing XMP packets
      and write them back to the file.
    question: Can I edit XMP metadata after embedding it in an image?
  - answer: A free trial is available for evaluation, but a paid license is required
      for production use. You can explore options on the [Aspose.Imaging for Java
      website](https://purchase.aspose.com/buy).
    question: Is Aspose.Imaging for Java a free tool?
  - answer: Visit the [Aspose.Imaging forums](https://forum.aspose.com/) for community
      assistance, or contact Aspose support directly for paid‑license customers.
    question: Where can I get help and support for Aspose.Imaging for Java?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: 'ไลบรารีการประมวลผลภาพ Java: XMP กับ Aspose.Imaging'
url: /th/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# การจัดการข้อมูล XMP ในภาพด้วย Aspose.Imaging สำหรับ Java

Aspose.Imaging เป็น **java image processing library** ที่ให้คุณทำงานกับรูปแบบเรสเตอร์และเวกเตอร์หลายสิบรูปแบบ ในบทเรียนนี้คุณจะได้เรียนรู้วิธีฝังและดึงข้อมูล XMP (Extensible Metadata Platform) ในภาพโดยใช้ Aspose.Imaging สำหรับ Java เมื่อเสร็จแล้วคุณจะสามารถเก็บข้อมูลผู้เขียน คำอธิบาย และเมตาดาต้ากำหนดเองโดยตรงในไฟล์ภาพของคุณ ทำให้ไฟล์สามารถค้นหาและอธิบายตัวเองได้

## คำตอบสั้น
- **What is XMP?** XMP คือรูปแบบมาตรฐานที่ใช้ XML สำหรับฝังเมตาดาต้าในไฟล์ต่าง ๆ เช่น ภาพ, PDF, และวิดีโอ.  
- **Which library handles XMP in Java?** Aspose.Imaging for Java ให้ API ครบวงจรสำหรับการอ่านและเขียนแพ็กเกจ XMP.  
- **Do I need a license?** การทดลองใช้ฟรีทำงานสำหรับการพัฒนา; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **How many image formats are supported?** รองรับมากกว่า 150 รูปแบบ รวมถึง TIFF, JPEG, PNG, PSD, และ RAW.  
- **Can I process large images?** ใช่ – ไลบรารีสามารถจัดการไฟล์ขนาดถึง 2 GB โดยไม่ต้องโหลดภาพทั้งหมดเข้าสู่หน่วยความจำ.

## XMP metadata คืออะไร
XMP metadata เป็นมาตรฐานที่ใช้ XML เพื่อฝังข้อมูลอธิบายลงในไฟล์ดิจิทัลโดยตรง มันช่วยให้การจัดเก็บข้อมูลผู้เขียน ลิขสิทธิ์ คำสำคัญ และข้อมูลกำหนดเองเป็นไปอย่างสอดคล้องกันระหว่างแอปพลิเคชันต่าง ๆ เนื่องจากเป็น XML ทำให้ XMP สามารถขยายด้วย namespace กำหนดเองได้ ซึ่งนักพัฒนาสามารถเพิ่มฟิลด์ที่เป็นกรรมสิทธิ์ของตนเองได้โดยยังคงเข้ากันได้กับเครื่องมือที่รองรับสคีมาหลัก ทำให้ XMP เหมาะสำหรับการจัดการสินทรัพย์ระยะยาวและการทำงานร่วมกันข้ามแอปพลิเคชัน

## ทำไมต้องใช้ Java image processing library สำหรับ XMP
Aspose.Imaging for Java รองรับ **150+ image formats** และสามารถประมวลผลไฟล์หลายกิกะไบต์ในโหมดสตรีมมิ่ง ลดการใช้หน่วยความจำได้ถึง 80 % เมื่อเทียบกับการโหลดภาพทั้งหมด API ยังรับประกันว่าแพ็กเกจ XMP จะสอดคล้องตามมาตรฐาน ทำให้เข้ากันได้กับ Adobe Photoshop, Lightroom และเครื่องมืออื่น ๆ

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมอยู่แล้ว:

- สภาพแวดล้อมการพัฒนา Java ตั้งค่าไว้บนคอมพิวเตอร์ของคุณ.  
- ไลบรารี Aspose.Imaging for Java ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้จาก [Aspose.Imaging for Java website](https://releases.aspose.com/imaging/java/).  
- ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java.

## การนำเข้าแพ็กเกจ

เริ่มต้นด้วยการนำเข้าแพ็กเกจที่จำเป็นเข้าสู่โครงการ Java ของคุณ คุณสามารถเพิ่มคำสั่ง import ต่อไปนี้ที่ส่วนเริ่มต้นของโค้ด:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.xmp.XmpPackage;
import com.aspose.imaging.xmp.XmpPacketWrapper;
import com.aspose.imaging.xmp.XmpMeta;
import com.aspose.imaging.xmp.photoshop.ColorMode;
import com.aspose.imaging.xmp.photoshop.PhotoshopPackage;
import com.aspose.imaging.xmp.dc.DublinCorePackage;
import com.aspose.imaging.xmp.header.XmpHeaderPi;
import com.aspose.imaging.xmp.trailer.XmpTrailerPi;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

ตอนนี้เราจะทำการแยกตัวอย่างเป็นขั้นตอนตามลำดับ:

## วิธีฝัง XMP metadata ด้วย Java image processing library

โหลดภาพของคุณ สร้างแพ็กเกจ XMP แนบแพ็กเกจเข้ากับภาพ แล้วบันทึก – ทั้งหมดในไม่กี่บรรทัดสั้น ๆ เมธอด `setXmpData` ของ Aspose.Imaging จะเขียนแพ็กเกจโดยตรงลงในไฟล์โดยไม่ต้องใช้ไฟล์เมตาดาต้าแยก กระบวนการทำงานได้ทั้งกับภาพที่มาจากไฟล์และสตรีม ทำให้เหมาะกับบริการเว็บและงานแบตช์

### ขั้นตอนที่ 1: ระบุขนาดภาพและตัวเลือก Tiff

ก่อนอื่นกำหนดไดเรกทอรีที่ภาพจะถูกจัดเก็บและสร้าง `Rectangle` เพื่อระบุขนาดของภาพ ในตัวอย่างนี้เราใช้ภาพ TIFF พร้อมตัวเลือกบางอย่าง `TiffOptions` ตั้งค่าการกำหนดรูปแบบเฉพาะสำหรับภาพ TIFF.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### ขั้นตอนที่ 2: สร้างภาพใหม่

ต่อไปสร้างภาพใหม่ด้วยตัวเลือกที่กำหนดไว้ ภาพนี้จะใช้เก็บเมตาดาต้า XMP `TiffImage` แทนวัตถุภาพ TIFF และ `TiffFrame` กำหนดเฟรมแต่ละเฟรมภายในภาพ

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### ขั้นตอนที่ 3: สร้าง XMP Header และ Trailer

สร้างอินสแตนซ์ของ XMP‑Header และ XMP‑Trailer สำหรับเมตาดาต้า XMP ของคุณ Header และ Trailer นี้ช่วยกำหนดโครงสร้างเมตาดาต้า `XmpHeaderPi` และ `XmpTrailerPi` แทนส่วนเปิดและปิดของแพ็กเกจ XMP

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### ขั้นตอนที่ 4: สร้าง XMP Meta Information

สร้างอินสแตนซ์ของ XMP meta เพื่อกำหนดแอตทริบิวต์ต่าง ๆ คุณสามารถเพิ่มข้อมูลเช่นผู้เขียนและคำอธิบาย `XmpMeta` เก็บฟิลด์เมตาดาต้าแกนเช่นผู้เขียนและคำอธิบาย

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### ขั้นตอนที่ 5: สร้าง XMP Packet Wrapper

`XmpPacketWrapper` เป็นคอนเทนเนอร์ที่เก็บ XMP header, trailer และข้อมูลเมตาไว้ในแพ็กเกจเดียว มันทำให้แน่ใจว่าแพ็กเกจสอดคล้องตามสเปคของ XMP `XmpPacketWrapper` จัดแพ็กเกจ header, meta, trailer ให้เป็นแพ็กเกจ XMP เดียว

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### ขั้นตอนที่ 6: เพิ่ม Photoshop Package

เพื่อเก็บข้อมูลเฉพาะของ Photoshop สร้าง Photoshop package และกำหนดแอตทริบิวต์ เช่น เมือง, ประเทศ, และโหมดสี แล้วเพิ่มแพ็กเกจนี้ลงในเมตาดาต้า XMP `PhotoshopPackage` เก็บเมตาดาต้าเฉพาะของ Photoshop เช่น เมือง, ประเทศ, และโหมดสี

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### ขั้นตอนที่ 7: เพิ่ม Dublin Core Package

สำหรับข้อมูลทั่วไป เช่น ผู้เขียน, ชื่อเรื่อง, และค่าต่าง ๆ เพิ่ม DublinCore package และกำหนดแอตทริบิวต์ของมัน แล้วเพิ่มแพ็กเกจนี้ลงในเมตาดาต้า XMP ด้วย `DublinCorePackage` มีฟิลด์มาตรฐานของ Dublin Core เช่น ชื่อเรื่อง, ผู้สร้าง, และคำสำคัญ

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### ขั้นตอนที่ 8: อัปเดต XMP Metadata ในภาพ

อัปเดตเมตาดาต้า XMP ลงในภาพโดยใช้เมธอด `setXmpData` คำสั่งนี้จะเขียนแพ็กเกจ XMP ลงในส่วนเมตาดาต้าของภาพ `setXmpData` เขียนแพ็กเกจ XMP ลงในส่วนเมตาดาต้าของภาพ

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### ขั้นตอนที่ 9: บันทึกภาพ

ตอนนี้คุณสามารถบันทึกภาพพร้อมเมตาดาต้า XMP ที่ฝังไว้ลงบนดิสก์หรือในสตรีมหน่วยความจำ

```java
    image.save(ms);
```

### ขั้นตอนที่ 10: โหลดภาพและดึง XMP Metadata

เพื่อดึงเมตาดาต้า XMP จากภาพ โหลดภาพจากสตรีมหรือดิสก์และเข้าถึงข้อมูล XMP ผ่านเมธอด `getXmpData` `getXmpData` อ่านแพ็กเกจ XMP ที่ฝังอยู่จากภาพ

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

ขอแสดงความยินดี! คุณได้เรียนรู้วิธีจัดการข้อมูล XMP ในภาพด้วย Aspose.Imaging for Java เรียบร้อยแล้ว ซึ่งทำให้คุณสามารถเก็บและดึงเมตาดาต้าที่มีคุณค่าในไฟล์ภาพของคุณได้

## ปัญหาทั่วไปและวิธีแก้

- **Metadata not appearing in Photoshop:** ตรวจสอบให้แน่ใจว่าแพ็กเกจ XMP ปฏิบัติตามสคีมาของ XML อย่างถูกต้อง; Aspose.Imaging จะตรวจสอบอัตโนมัติ แต่ namespace กำหนดเองอาจต้องลงทะเบียน.  
- **Large TIFF files cause OutOfMemoryError:** ใช้ `TiffOptions` พร้อมตั้งค่า `Compression` เป็น `LZW` และเปิดใช้งานสตรีมมิ่ง (`loadOptions.setBufferSize`) เพื่อลดการใช้หน่วยความจำ.  
- **Unexpected character encoding:** XMP ต้องการ UTF‑8; ส่งสตริงโดยใช้ `StandardCharsets.UTF_8` เสมอเพื่อหลีกเลี่ยงข้อมูลที่เสียหาย.

## คำถามที่พบบ่อย

**Q: XMP metadata คืออะไร?**  
A: XMP เป็นมาตรฐานที่ใช้ XML สำหรับฝังข้อมูลอธิบายลงในไฟล์โดยตรง ทำให้เมตาดาต้าสอดคล้องกันระหว่างแอปพลิเคชันต่าง ๆ

**Q: ทำไม XMP metadata ถึงสำคัญ?**  
A: มันช่วยให้คุณแท็กภาพด้วยผู้เขียน, ลิขสิทธิ์, คำสำคัญ, และข้อมูลกำหนดเอง เพิ่มความสามารถในการค้นหาและการจัดการสินทรัพย์โดยไม่ต้องใช้ฐานข้อมูลภายนอก

**Q: สามารถแก้ไข XMP metadata หลังจากฝังลงในภาพได้หรือไม่?**  
A: ได้, Aspose.Imaging for Java มีเมธอดสำหรับแก้ไขแพ็กเกจ XMP ที่มีอยู่และเขียนกลับไปยังไฟล์

**Q: Aspose.Imaging for Java เป็นเครื่องมือฟรีหรือไม่?**  
A: มีการทดลองใช้ฟรีสำหรับการประเมินผล, แต่ต้องมีลิขสิทธิ์แบบชำระเงินสำหรับการใช้งานในผลิตภัณฑ์ คุณสามารถสำรวจตัวเลือกได้ที่ [Aspose.Imaging for Java website](https://purchase.aspose.com/buy)

**Q: จะหาแหล่งช่วยเหลือและสนับสนุนสำหรับ Aspose.Imaging for Java ได้จากที่ไหน?**  
A: เยี่ยมชม [Aspose.Imaging forums](https://forum.aspose.com/) เพื่อรับความช่วยเหลือจากชุมชน หรือ ติดต่อฝ่ายสนับสนุนของ Aspose โดยตรงสำหรับลูกค้าที่มีลิขสิทธิ์แบบชำระเงิน

## สรุป

ในบทเรียนนี้ เราได้สำรวจวิธีทำงานกับ XMP metadata ในภาพโดยใช้ Aspose.Imaging for Java ซึ่งเป็น **java image processing library** ชั้นนำ โดยทำตามคู่มือขั้นตอน คุณสามารถฝัง, อัปเดต, และดึงข้อมูล XMP ได้อย่างง่ายดาย ทำให้สินทรัพย์ดิจิทัลของคุณมีเมตาดาต้าที่ค้นหาได้และสอดคล้องตามมาตรฐาน

---

**อัปเดตล่าสุด:** 2026-05-18  
**ทดสอบด้วย:** Aspose.Imaging for Java 24.12  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทเรียนที่เกี่ยวข้อง

- [เชี่ยวชาญการประมวลผลภาพ Java: แก้ไขข้อมูล EXIF ด้วย Aspose.Imaging](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [การประมวลผลภาพ Java ด้วย Aspose.Imaging: โหลด, ปรับปรุงและบันทึกภาพ](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [การประมวลผลภาพ Java ขั้นสูงด้วย Aspose.Imaging Library](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Specify the size of image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// create the brand new image just for sample purposes
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// create an instance of XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// create an instance of Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// create an instance of XMP meta class to set different attributes
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// create an instance of XmpPacketWrapper that contains all metadata
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// create an instance of Photoshop package and set photoshop attributes
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// add photoshop package into XMP metadata
	xmpData.addPackage(photoshopPackage);
	// create an instance of DublinCore package and set dublinCore attributes
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// add dublinCore Package into XMP metadata
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// update XMP metadata into image
	image.setXmpData(xmpData);
	// Save image on the disk or in memory stream
	image.save(ms);
	// Load the image from memory stream or from disk to read/get the metadata
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Getting the XMP metadata
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Use package data ...
		}
	}
}
        
```