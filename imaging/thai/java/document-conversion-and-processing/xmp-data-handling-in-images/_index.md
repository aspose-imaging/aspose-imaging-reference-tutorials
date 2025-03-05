---
title: การจัดการข้อมูล XMP ในภาพด้วย Aspose.Imaging สำหรับ Java
linktitle: การจัดการข้อมูล XMP ในภาพ
second_title: Aspose.Imaging Java Image Processing API
description: เรียนรู้วิธีจัดการข้อมูลเมตา XMP ในรูปภาพโดยใช้ Aspose.Imaging สำหรับ Java ฝังและดึงข้อมูลเมตาเพื่อปรับปรุงไฟล์ภาพของคุณ
type: docs
weight: 16
url: /th/java/document-conversion-and-processing/xmp-data-handling-in-images/
---
Aspose.Imaging for Java เป็นไลบรารีอเนกประสงค์และทรงพลังสำหรับการทำงานกับรูปภาพในรูปแบบต่างๆ บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการจัดการข้อมูล XMP (Extensible Metadata Platform) ในรูปภาพโดยใช้ Aspose.Imaging สำหรับ Java XMP เป็นมาตรฐานสำหรับการฝังข้อมูลเมตาลงในไฟล์ภาพ ซึ่งช่วยให้คุณสามารถจัดเก็บข้อมูลอันมีค่า เช่น ผู้แต่ง คำอธิบาย และอื่นๆ ได้

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java ที่ตั้งค่าบนคอมพิวเตอร์ของคุณ
-  ติดตั้ง Aspose.Imaging สำหรับไลบรารี Java แล้ว คุณสามารถดาวน์โหลดได้จาก[Aspose.Imaging สำหรับเว็บไซต์ Java](https://releases.aspose.com/imaging/java/).
- ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java

## การนำเข้าแพ็คเกจ

เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ คุณสามารถเพิ่มคำสั่งนำเข้าต่อไปนี้ที่จุดเริ่มต้นของรหัสของคุณ:

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

ตอนนี้ เรามาแบ่งตัวอย่างออกเป็นคำแนะนำทีละขั้นตอน:

## ขั้นตอนที่ 1: ระบุขนาดรูปภาพและตัวเลือก Tiff

ขั้นแรก กำหนดไดเร็กทอรีที่จะจัดเก็บรูปภาพของคุณ และสร้างสี่เหลี่ยมผืนผ้าเพื่อระบุขนาดของรูปภาพ ในตัวอย่างนี้ เราใช้รูปภาพ Tiff พร้อมตัวเลือกบางอย่าง

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## ขั้นตอนที่ 2: สร้างภาพใหม่

ตอนนี้ สร้างภาพใหม่ด้วยตัวเลือกที่ระบุ รูปภาพนี้จะใช้เพื่อจัดเก็บข้อมูลเมตา XMP

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## ขั้นตอนที่ 3: สร้างส่วนหัวและตัวอย่าง XMP

สร้างอินสแตนซ์ของ XMP-Header และ XMP-Trailer สำหรับข้อมูลเมตา XMP ของคุณ ส่วนหัวและส่วนท้ายเหล่านี้ช่วยกำหนดโครงสร้างข้อมูลเมตา

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## ขั้นตอนที่ 4: สร้างข้อมูลเมตา XMP

ตอนนี้ ให้สร้างอินสแตนซ์ของเมตา XMP เพื่อตั้งค่าแอตทริบิวต์ต่างๆ คุณสามารถเพิ่มข้อมูล เช่น ผู้แต่งและคำอธิบายได้

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## ขั้นตอนที่ 5: สร้าง XMP Packet Wrapper

สร้างอินสแตนซ์ของ XmpPacketWrapper ที่มีส่วนหัว XMP ตัวอย่าง และข้อมูลเมตา

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## ขั้นตอนที่ 6: เพิ่มแพ็คเกจ Photoshop

หากต้องการจัดเก็บข้อมูลเฉพาะของ Photoshop ให้สร้างแพ็คเกจ Photoshop และตั้งค่าคุณลักษณะ เช่น เมือง ประเทศ และโหมดสี จากนั้น เพิ่มแพ็คเกจนี้ลงในข้อมูลเมตา XMP

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## ขั้นตอนที่ 7: เพิ่มแพ็คเกจ Dublin Core

สำหรับข้อมูลทั่วไปเพิ่มเติม เช่น ผู้แต่ง ชื่อเรื่อง และค่าเพิ่มเติม ให้สร้างแพ็คเกจ DublinCore และตั้งค่าแอตทริบิวต์ เพิ่มแพ็คเกจนี้ไปยังข้อมูลเมตา XMP เช่นกัน

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## ขั้นตอนที่ 8: อัปเดตข้อมูลเมตา XMP ในรูปภาพ

 อัปเดตข้อมูลเมตา XMP ลงในรูปภาพโดยใช้ไฟล์`setXmpData` วิธี.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## ขั้นตอนที่ 9: บันทึกรูปภาพ

ตอนนี้คุณสามารถบันทึกรูปภาพด้วยข้อมูลเมตา XMP ที่ฝังอยู่บนดิสก์หรือในสตรีมหน่วยความจำ

```java
    image.save(ms);
```

## ขั้นตอนที่ 10: โหลดรูปภาพและดึงข้อมูลเมตา XMP

หากต้องการดึงข้อมูลเมตา XMP จากรูปภาพ ให้โหลดรูปภาพจากสตรีมหน่วยความจำหรือดิสก์ และเข้าถึงข้อมูล XMP

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // ใช้ข้อมูลแพ็กเกจ ...
        }
    }
}
```

ยินดีด้วย! คุณได้เรียนรู้วิธีจัดการข้อมูล XMP ในรูปภาพโดยใช้ Aspose.Imaging สำหรับ Java เรียบร้อยแล้ว ซึ่งจะทำให้คุณสามารถจัดเก็บและเรียกข้อมูลเมตาอันมีค่าภายในไฟล์ภาพของคุณได้

## บทสรุป

ในบทช่วยสอนนี้ เราได้ศึกษาวิธีทำงานกับข้อมูลเมตา XMP ในรูปภาพโดยใช้ Aspose.Imaging สำหรับ Java ด้วยการทำตามคำแนะนำทีละขั้นตอน คุณสามารถฝังและดึงข้อมูลเมตาภายในไฟล์ภาพของคุณได้อย่างง่ายดาย ปรับปรุงข้อมูลและการใช้งาน

## คำถามที่พบบ่อย

### คำถามที่ 1: เมตาดาต้า XMP คืออะไร

A1: XMP (Extensible Metadata Platform) เป็นมาตรฐานสำหรับการฝังข้อมูลเมตาลงในไฟล์ประเภทต่างๆ รวมถึงรูปภาพด้วย ช่วยให้คุณสามารถจัดเก็บข้อมูล เช่น ผู้แต่ง ชื่อเรื่อง คำอธิบาย และอื่นๆ ภายในไฟล์ได้

### คำถามที่ 2: เหตุใดข้อมูลเมตา XMP จึงมีความสำคัญ

ตอบ 2: เมตาดาต้า XMP เป็นสิ่งจำเป็นสำหรับการจัดระเบียบและจัดหมวดหมู่สินทรัพย์ดิจิทัล ช่วยในการระบุความเป็นเจ้าของ การอธิบายเนื้อหา และเพิ่มบริบทให้กับไฟล์ เช่น รูปภาพ ทำให้เข้าถึงได้และมีความหมายมากขึ้น

### คำถามที่ 3: ฉันสามารถแก้ไขข้อมูลเมตา XMP หลังจากฝังลงในรูปภาพได้หรือไม่

A3: ได้ คุณสามารถแก้ไขข้อมูลเมตา XMP ได้หลังจากฝังลงในรูปภาพแล้ว Aspose.Imaging for Java มีเครื่องมือสำหรับการแก้ไขและอัปเดตแอตทริบิวต์ข้อมูลเมตาตามต้องการ

### คำถามที่ 4: Aspose.Imaging สำหรับ Java เป็นเครื่องมือฟรีหรือไม่

 ตอบ 4: Aspose.Imaging for Java มีเวอร์ชันทดลองใช้ฟรี แต่สำหรับฟังก์ชันการทำงานเต็มรูปแบบและการใช้งานแบบขยาย จำเป็นต้องมีใบอนุญาตแบบชำระเงิน คุณสามารถสำรวจตัวเลือกต่างๆ บน[Aspose.Imaging สำหรับเว็บไซต์ Java](https://purchase.aspose.com/buy).

### คำถามที่ 5: ฉันจะรับความช่วยเหลือและการสนับสนุนสำหรับ Aspose.Imaging สำหรับ Java ได้ที่ไหน

 A5: หากคุณพบปัญหาใดๆ หรือมีคำถามเกี่ยวกับ Aspose.Imaging สำหรับ Java คุณสามารถไปที่[Aspose ฟอรั่มการถ่ายภาพ](https://forum.aspose.com/) สำหรับการสนับสนุนและคำแนะนำจากชุมชน



## กรอกซอร์สโค้ดให้สมบูรณ์
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// ระบุขนาดของภาพโดยการกำหนดสี่เหลี่ยมผืนผ้า
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// สร้างภาพลักษณ์ใหม่เพื่อจุดประสงค์ตัวอย่างเท่านั้น
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// สร้างอินสแตนซ์ของ XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// สร้างอินสแตนซ์ของ Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// สร้างอินสแตนซ์ของคลาสเมตา XMP เพื่อตั้งค่าแอตทริบิวต์ที่แตกต่างกัน
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	//สร้างอินสแตนซ์ของ XmpPacketWrapper ที่มีข้อมูลเมตาทั้งหมด
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// สร้างอินสแตนซ์ของแพ็คเกจ Photoshop และตั้งค่าคุณสมบัติของ Photoshop
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// เพิ่มแพ็คเกจ Photoshop ลงในข้อมูลเมตา XMP
	xmpData.addPackage(photoshopPackage);
	// สร้างอินสแตนซ์ของแพ็คเกจ DublinCore และตั้งค่าแอตทริบิวต์ dublinCore
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// เพิ่มแพ็คเกจ dublinCore ลงในข้อมูลเมตา XMP
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// อัปเดตข้อมูลเมตา XMP ลงในรูปภาพ
	image.setXmpData(xmpData);
	// บันทึกภาพบนดิสก์หรือในสตรีมหน่วยความจำ
	image.save(ms);
	// โหลดรูปภาพจากสตรีมหน่วยความจำหรือจากดิสก์เพื่ออ่าน/รับข้อมูลเมตา
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// รับข้อมูลเมตา XMP
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// ใช้ข้อมูลแพ็กเกจ ...
		}
	}
}
        
```