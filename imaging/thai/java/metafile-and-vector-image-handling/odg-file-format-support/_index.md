---
date: 2026-01-24
description: เรียนรู้วิธีแปลง odg เป็น png และ pdf ด้วย Aspose.Imaging สำหรับ Java.
  ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อการแปลงที่มีประสิทธิภาพ.
linktitle: ODG File Format Support
second_title: Aspose.Imaging Java Image Processing API
title: แปลง ODG เป็น PNG และ PDF ด้วย Aspose.Imaging สำหรับ Java
url: /th/java/metafile-and-vector-image-handling/odg-file-format-support/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# แปลง ODG เป็น PNG & PDF ด้วย Aspose.Imaging สำหรับ Java

ในโลกของการแปลงเอกสาร Aspose.Imaging สำหรับ Java โดดเด่นในฐานะเครื่องมือที่ทรงพลังซึ่งช่วยให้คุณสามารถ **แปลงไฟล์ ODG (OpenDocument Graphics) ไปเป็นรูปแบบ PNG และ PDF** ได้อย่างง่ายดาย ไม่ว่าคุณจะกำลังสร้างบริการประมวลผลเป็นชุด, ยูทิลิตี้เดสก์ท็อป, หรือเว็บ API การเรียนรู้วิธีจะช่วยประหยัดเวลาและลดความจำเป็นในการใช้เครื่องมือภายนอก บทเรียนนี้จะพาคุณผ่านกระบวนการทั้งหมด ทีละขั้นตอน เพื่อให้คุณเริ่มแปลงไฟล์ ODG ได้ทันที

## คำตอบสั้น ๆ
- **บทเรียนนี้ครอบคลุมอะไร?** การแปลงไฟล์ ODG ไปเป็น PNG และ PDF ด้วย Aspose.Imaging สำหรับ Java  
- **ต้องมีลิขสิทธิ์หรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **รองรับเวอร์ชัน Java ใด?** Java 8 หรือใหม่กว่า (JDK 8+)  
- **สามารถประมวลผลหลายไฟล์พร้อมกันได้หรือไม่?** ได้ – ตัวอย่างโค้ดจะวนลูปผ่านอาร์เรย์ของไฟล์ ODG  
- **ไฟล์ผลลัพธ์จะถูกบันทึกไว้ที่ไหน?** จะแบบไม่มีการสูญเสีย ทำให้ภาพขนาดย่อ, และการประมวลผลภาพต่อ และ PDF รองรับโดยทุกระบบ, ในขณะที่ ODG มีการใช้งานจำกัด  
- **รักษาความคมชัดของภาพ:** การเรสเตอร์ ODG เป็น PNG ทำให้การออกแบบเดิมคมชัดที่ความละเอียดใดก็ได้ที่คุณเลือก  
- **สร้างเอกสารที่พิมพ์ได้:** PDF เหมาะสำหรับการพิมพ์, การเก็บถาวร, หรือการฝังกราฟิกในรายงาน  
- **อัตโนมัติ:** การใช้ Aspose.Imaging ทำให้คุณฝังการแปลงเข้าไปในแอปพลิเคชัน Java ได้โดยไม่ต้องทำขั้นตอนด้วยมือ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในกระบวนการแปลง คุณต้องตรวจสอบว่ามีข้อกำหนดต่อไปนี้พร้อมใช้งานแล้ว:

### 1. สภาพแวดล้อมการพัฒนา Java

ตรวจสอบว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณแล้ว คุณสามารถดาวน์โหลดและติดตั้ง Java Development Kit (JDK) ล่าสุดจาก [เว็บไซต์ Oracle](https://www.oracle.com/java/technologies/javase-downloads)

### 2. Aspose.Imaging สำหรับ Java

คุณต้องดาวน์โหลดและติดตั้ง Aspose.Imaging สำหรับ Java คุณสามารถค้นหาเวอร์ชันล่าสุดได้ที่ [หน้าดาวน์โหลด Aspose.Imaging สำหรับ Java](https://releases.aspose.com/imaging/java/)

### 3. ไฟล์ ODG

แน่นอนว่าคุณต้องมีไฟล์ ODG ที่ต้องการแปลง ตรวจสอบให้แน่ใจว่าไฟล์เหล่านี้อยู่ในไดเรกทอรีบนระบบของคุณ

## การนำเข้าแพ็กเกจ

เมื่อคุณมีข้อกำหนดครบแล้ว ให้เริ่มนำเข้าแพ็กเกจที่จำเป็นในโปรเจกต์ Java ของคุณ แพ็กเกจเหล่านี้จะช่วยให้คุณทำงานกับ Aspose.Imaging สำหรับ Java ได้อย่างมีประสิทธิภาพ

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.SizeF;
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
```

เราจะแบ่งกระบวนการแปลงออกเป็นขั้นตอนง่าย ๆ เพื่อให้คุณตามได้สะดวก สำหรับแต่ละขั้นตอน เราจะให้หัวข้อและคำอธิบาย

## ขั้นตอนที่ 1: กำหนดไดเรกทอรีข้อมูลของคุณ

เริ่มต้นโดยระบุไดเรกทอรีที่เก็บไฟล์ ODG ของคุณ คุณต้องแทนที่ `"Your Document Directory"` ด้วยพาธจริงของไดเรกทอรีของคุณ

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

## ขั้นตอนที่ 2: ระบุไฟล์ ODG

สร้างอาร์เรย์ของชื่อไฟล์ ODG ที่ต้องการแปลง แทนที่ชื่อไฟล์ตัวอย่างด้วยชื่อไฟล์ ODG ของคุณเอง

```java
String[] files = new String[] {"example.odg", "example1.odg"};
```

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการเรสเตอร์

กำหนดตัวเลือกการเรสเตอร์สำหรับไฟล์ ODG ตัวเลือกเหล่านี้จะกำหนดขนาดหน้าและการตั้งค่าเรสเตอร์เวกเตอร์

```java
final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
```

## ขั้นตอนที่ 4: วนลูปผ่านไฟล์ ODG

ตอนนี้ให้ทำการวนลูปผ่านแต่ละไฟล์ ODG, โหลดไฟล์, และแปลงเป็นทั้งรูปแบบ PNG และ PDF

```java
for (String file : files) {
    String fileName = dataDir + file;
    try (Image image = Image.load(fileName)) {
        rasterizationOptions.setPageSize(new SizeF(image.getWidth(), image.getHeight()));

        // Convert to PNG
        String outFileName = "Your Document Directory" + file.replace(".odg", ".png");
        image.save(outFileName, new PngOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});

        // Convert to PDF
        outFileName = "Your Document Directory" + file.replace(".odg", ".pdf");
        image.save(outFileName, new PdfOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});
    }
}
```

> **เคล็ดลับ:** ปรับ `rasterizationOptions.setPageSize(...)` หากคุณต้องการ DPI หรืออัตราสเกลเฉพาะสำหรับการสร้าง PNG ความละเอียดสูง

ยินดีด้วย! คุณได้แปลงไฟล์ ODG เป็นรูปแบบ PNG และ PDF สำเร็จแล้วโดยใช้ Aspose.Imaging สำหรับ Java

## ข้อผิดพลาดทั่วไปและวิธีหลีกเลี่ยง

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|--------|
| **PNG ผลลัพธ์เป็นสีขาว** | ตัวเลือกการเรสเตอร์ไม่ได้ตั้งค่าก่อนการบันทึก | เรียก `setPageSize` (หรือ `setResolution`) ก่อน `save` ครั้งแรก |
| **หน่วยความจำไม่พอสำหรับ ODG ขนาดใหญ่** | การโหลดกราฟิกเวกเตอร์ขนาดใหญ่ใช้ RAM มาก | ประมวลผลไฟล์ทีละไฟล์ภายในบล็อก `try‑with‑resources` (ตามตัวอย่าง) |
| **พาธไฟล์ไม่ถูกต้อง** | ขาดเครื่องหมาย `/` ปิดท้ายใน `dataDir` | ตรวจสอบสตริงไดเรกทอรีว่าจบด้วย `/` หรือใช้ `Paths.get` |

## คำถามที่พบบ่อย

### Q1: Aspose.Imaging สำหรับ Java เป็นเครื่องมือฟรีหรือไม่?

A1: ไม่, Aspose.Imaging สำหรับ Java เป็นไลบรารีเชิงพาณิชย์ คุณสามารถดูข้อมูลราคาได้ที่ [หน้าซื้อสินค้า](https://purchase.aspose.com/buy)

### Q2: สามารถทดลองใช้ Aspose.Imaging สำหรับ Java ก่อนซื้อได้หรือไม่?

A2: ได้, คุณสามารถดาวน์โหลดเวอร์ชันทดลองฟรีได้จาก [ที่นี่](https://releases.aspose.com/)

### Q3: จะขอรับการสนับสนุนสำหรับ Aspose.Imaging สำหรับ Java ได้อย่างไร?

A3: คุณสามารถขอความช่วยเหลือและตั้งคำถามได้ใน [ฟอรั่ม Aspose.Imaging](https://forum.aspose.com/)

### Q4: Aspose.Imaging สำหรับ Java รองรับรูปแบบไฟล์อื่น ๆ อะไรบ้าง?

A4: Aspose.Imaging สำหรับ Java รองรับรูปแบบภาพและเอกสารหลากหลาย รวมถึง BMP, JPEG, TIFF, PDF และอื่น ๆ ดูรายละเอียดเพิ่มเติมใน [เอกสารอ้างอิง](https://reference.aspose.com/imaging/java/)

### Q5: สามารถใช้ Aspose.Imaging สำหรับ Java ในโครงการเชิงพาณิชย์ของฉันได้หรือไม่?

A5: ได้, คุณสามารถใช้ Aspose.Imaging สำหรับ Java ในโครงการเชิงพาณิชย์ได้หลังจากซื้อไลเซนส์ที่เหมาะสม

## สรุป

โดยทำตามขั้นตอนข้างต้น คุณจะมีวิธีที่เชื่อถือได้ในการ **แปลง odg เป็น png** และสร้างเวอร์ชัน PDF ของกราฟิกทั้งหมดจากโค้ด Java วิธีนี้ช่วยลดการพึ่งพาเครื่องมือของบุคคลที่สาม, ให้คุณควบคุมคุณภาพผลลัพธ์ได้เต็มที่, และสามารถรวมเข้าไปในงานประมวลผลชุดหรือบริการเว็บได้อย่างง่ายดาย สำรวจคุณสมบัติอื่น ๆ ของ Aspose.Imaging เช่น การปรับขนาดภาพ, การแปลงรูปแบบ, และการใส่ลายน้ำ เพื่อเพิ่มประสิทธิภาพการทำงานของคุณต่อไป

---

**อัปเดตล่าสุด:** 2026-01-24  
**ทดสอบด้วย:** Aspose.Imaging สำหรับ Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}