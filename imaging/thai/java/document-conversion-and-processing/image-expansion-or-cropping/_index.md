---
date: 2025-12-20
description: เรียนรู้วิธีการครอบภาพเป็นสี่เหลี่ยมและขยายภาพโดยใช้ Java กับ Aspose.Imaging
  คู่มือขั้นตอนต่อขั้นตอนสำหรับนักพัฒนา
linktitle: Image Expansion or Cropping
second_title: Aspose.Imaging Java Image Processing API
title: ตัดรูปภาพเป็นสี่เหลี่ยมโดยใช้ Aspose.Imaging สำหรับ Java
url: /th/java/document-conversion-and-processing/image-expansion-or-cropping/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# ตัดรูปภาพเป็นสี่เหลี่ยมผืนผ้าด้วย Aspose.Imaging สำหรับ Java

ในโลกดิจิทัลที่เคลื่อนที่อย่างรวดเร็วในทุกวันนี้ การสามารถ **crop image to rectangle** อย่างรวดเร็วและเชื่อถือได้เป็นความต้องการหลักสำหรับกระบวนการทำงานกับภาพที่ใช้ Java ไม่ว่าจะคุณกำลังสร้างเว็บเซอร์วิสที่ต้องตัดรูปภาพที่ผู้ใช้อัปโหลด, สร้างภาพย่อสำหรับแคตาล็อกอีคอมเมิร์ซ, หรือเพียงแค่เตรียมทรัพยากรสำหรับแคมเปญการตลาด, Aspose.Imaging สำหรับ Java ให้ API ที่สะอาดและมีประสิทธิภาพสูงเพื่อทำงานให้สำเร็จ ในบทแนะนำนี้เราจะพาไปผ่านการตัดสี่เหลี่ยมจากภาพและการขยายแคนวาสภาพด้วย Java—เหมาะสำหรับผู้ที่ต้องการเชี่ยวชาญเทคนิค **how to crop image java**

## คำตอบอย่างรวดเร็ว
- **What library is best for Java image cropping?** Aspose.Imaging for Java.
- **Can I crop to an arbitrary rectangle?** Yes – define any X, Y, width, and height.
- **Do I need a license for development?** A free trial works for testing; a license is required for production.
- **Is expanding an image possible?** Absolutely – you can increase canvas size before cropping.
- **Which Java version is supported?** Java 8 and newer.

## “crop image to rectangle” คืออะไร
การตัดรูปภาพเป็นสี่เหลี่ยมผืนผ้าหมายถึงการดึงส่วนย่อยของบิตแมปต้นฉบับที่กำหนดโดยพื้นที่สี่เหลี่ยม (X‑offset, Y‑offset, ความกว้าง, ความสูง) ส่วนที่เหลือของภาพจะถูกละทิ้ง ทำให้คุณได้ภาพใหม่ที่เล็กลงซึ่งมีเฉพาะพื้นที่ที่ต้องการเท่านั้น

## ทำไมต้องใช้ Aspose.Imaging สำหรับ Java?
- **No external dependencies** – pure Java, works on any platform.
- **Broad format support** – JPEG, PNG, BMP, TIFF, and more.
- **High‑performance caching** – `cacheData()` reduces I/O overhead.
- **Simple API** – one‑line calls for loading, defining a rectangle, and saving.

## ข้อกำหนดเบื้องต้น
- **Java Development Environment** – JDK 8+ installed and configured.
- **Aspose.Imaging for Java** – download from the [website](https://releases.aspose.com/imaging/java/).
- **Basic Java Knowledge** – familiarity with classes, try‑with‑resources, and file paths.
- **Image to Work With** – any JPEG/PNG you’d like to crop or expand.

## การนำเข้าแพ็กเกจ
First, point the code to the folder that holds your source images. This snippet stays unchanged from the original tutorial.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

Replace `"Your Document Directory"` with the absolute path on your machine.

## ขั้นตอนที่ 1: โหลดภาพ
Loading the image is the foundation for any manipulation. We also call `cacheData()` to keep the bitmap in memory for fast subsequent operations.

```java
try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
{
    rasterImage.cacheData();
}
```

> **Pro tip:** Use a `try‑with‑resources` block (as shown) to ensure the image is automatically closed, preventing memory leaks.

## ขั้นตอนที่ 2: กำหนดพื้นที่สำหรับการตัด
Here we create a `Rectangle` that represents the exact area you want to keep. The rectangle can start outside the original bounds – Aspose.Imaging will automatically expand the canvas (useful for the **expand image using java** scenario).

```java
// Create an instance of Rectangle class and define X, Y, Width, and Height of the rectangle
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

- **X / Y** – negative values shift the rectangle left/up, causing the canvas to expand.
- **Width / Height** – size of the cropped region.

## ขั้นตอนที่ 3: บันทึกภาพที่ถูกตัด (หรือขยาย)
Finally, write the result to disk. The `save` method takes the destination path, image format options, and the rectangle we defined.

```java
rasterImage.save("Your Document Directory" + "Grayscaling_out.jpg", new JpegOptions(), destRect);
```

The output file `Grayscaling_out.jpg` now contains the **crop image to rectangle** result. If the rectangle extended beyond the original image, the extra area is filled with a default background (transparent for PNG, black for JPEG).

## กรณีการใช้งานทั่วไป

| Scenario | Why It Matters |
|----------|----------------|
| **Thumbnail generation** | Quickly extract a central region for consistent sizing. |
| **User‑profile picture cropping** | Enforce a square or rectangular avatar area. |
| **Canvas expansion before adding watermarks** | Add space around an image without distorting the original. |
| **Batch processing of scanned documents** | Crop out margins in one pass. |

## การแก้ไขปัญหาและเคล็ดลับ
- **Image not loading?** Verify the file path and ensure the image format is supported.
- **Unexpected black borders after expansion?** Set a background color in `JpegOptions` or use PNG for transparency.
- **Performance concerns with large images?** Increase the Java heap size (`-Xmx`) or process images in smaller batches.

## คำถามที่พบบ่อย

**Q: Aspose.Imaging for Java รองรับรูปแบบภาพอะไรบ้าง?**  
A: JPEG, PNG, BMP, TIFF, GIF, ICO, PSD และอื่น ๆ อีกมากมาย ดูเอกสารอย่างเป็นทางการสำหรับรายการเต็ม

**Q: ฉันสามารถทำการปรับแต่งภาพอื่น ๆ ด้วย Aspose.Imaging for Java ได้หรือไม่?**  
A: แน่นอน! การปรับขนาด, การหมุน, การกรอง, และการแปลงรูปแบบทั้งหมดพร้อมใช้งาน

**Q: Aspose.Imaging for Java เหมาะสำหรับแอปพลิเคชันเว็บหรือไม่?**  
A: ใช่. ไลบรารีนี้ปลอดภัยต่อการทำงานหลายเธรดและทำงานได้ดีในคอนเทนเนอร์เซอร์วิลท์และบริการ Spring Boot

**Q: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.Imaging for Java ได้อย่างไร?**  
A: เยี่ยมชม [forum](https://forum.aspose.com/) เพื่อรับความช่วยเหลือจากชุมชน หรือเปิดตั๋วสนับสนุนพร้อมใบอนุญาตที่ถูกต้อง

**Q: มีการทดลองใช้งานฟรีสำหรับ Aspose.Imaging for Java หรือไม่?**  
A: มี, คุณสามารถสำรวจไลบรารีด้วยการทดลองใช้งานฟรี ดาวน์โหลดได้จาก [here](https://releases.aspose.com/).

## สรุป
You’ve now learned how to **crop image to rectangle** and even **expand image using Java** with the powerful Aspose.Imaging API. By mastering these fundamentals you can build robust image‑processing pipelines, improve UI responsiveness, and deliver polished visual content across any Java application.

---

**อัปเดตล่าสุด:** 2025-12-20  
**ทดสอบด้วย:** Aspose.Imaging for Java 24.11 (latest at time of writing)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}