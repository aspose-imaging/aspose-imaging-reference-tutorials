---
date: 2026-01-19
description: เรียนรู้วิธีแปลงเอกสารเป็น PNG และเพิ่มประสิทธิภาพการใช้ฟอนต์เริ่มต้นด้วย
  Aspose.Imaging สำหรับ Java คู่มือนี้ยังครอบคลุมการส่งออก ODG เป็น PNG และการตั้งค่าฟอนต์เริ่มต้นของ
  Aspose.
linktitle: Optimize Default Font Usage
second_title: Aspose.Imaging Java Image Processing API
title: แปลงเอกสารเป็น PNG และเพิ่มประสิทธิภาพการใช้ฟอนต์เริ่มต้นด้วย Aspose.Imaging
  สำหรับ Java
url: /th/java/image-processing-and-enhancement/optimize-default-font-usage/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# แปลงเอกสารเป็น PNG และเพิ่มประสิทธิภาพการใช้ฟอนต์เริ่มต้นด้วย Aspose.Imaging สำหรับ Java

ในกระบวนการประมวลผลเอกสารสมัยใหม่, **การแปลงเอกสารเป็น PNG** มักเป็นขั้นตอนแรกในการสร้างตัวอย่างสำหรับ, รูปย่อ, หรือสิน Java ทำให้การแปลงนี้ง่ายดายฟอนต์เริ่มต้น, และแสดงตัวอย่างที่คุณสามารถนำไปใช้ในโปรเจกต์ของคุณได้ทันที.

## คอะไรายถึงการเรนเดอร์แต่ละหน้าของเอกสารต้นฉบับ (เช่น ODG, PDF, DOCX) เป็นภาพ PNG แบบแรสเตอร์
- **ไลบรารีใดที่จัดการการแปลง?**  
  Aspose.Imaging สำหรับ Java ให้ API `Image.load` และ `PngOptions`
- **ฉันสามารถตั้งฟอนต์เริ่มต้นแบบกำหนดเองระหว่างการแปลงได้หรือไม่?**  
  ได้ – ใช้ `FontSettings.setFontName` เพื่อระบุฟอนต์สำรอง
- **ต้องใช้ไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?**  
  จำเป็นต้องมีไลเซนส์เชิงพาณิชย์ดลองฟรีสำหรับการประเมินผล
- **ฟอร์แมตใดบ้างที่รองรับการส่งออก?**  
  นอกจาก PNG แล้ว Aspose.Imaging ยังรองรับ JPEG, BMP, TIFF, และฟอร์แมตเวกเตอร์หลายประเภท

## “convert document to PNG” คืออะไร?
การแปลงเอกสารเป็น PNG จะเปลี่ยนไฟล์เวกเตอร์หรือไฟล์ที่มีเนื้อหาผสมให้เป็นรูปแบบภาพพิกเซล. PNG รองรับความโปร่งใสและการบีบอัดแบบไม่มีไม่มีอร์ให้เค้าโครงเปลี่ยนหรือข้อความอ่านไม่ออก. การกำหนด **set default font Aspose** จะช่วยให้ผลลัพธ์ภาพมีความสม่ำเสมอในทุกสภาพแวดล้อม.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในกระบวนการแปลง, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:

- สภาพแวดล้อมการพัฒนา Java ที่ติดตั้งบนระบบของคุณ
- ไลบรารี Aspose.Imaging สำหรับ Java. คุณสามารถดาวน์โหลดได้จาก [website](https://releases.aspose.com/imaging/java/)
- ความรู้พื้นฐานด้านการเขียนโปรแกรม Java

## นำเข้าแพ็กเกจ

เพื่อเริ่มต้นการเพิ่มประสิทธิภาพการใช้ฟอนต์เริ่มต้น, คุณต้องนำเข้าแพ็กเกจที่จำเป็นจาก Aspose.Imaging สำหรับ Java. ดำเนินตามขั้นตอนต่อไปนี้:

นำเข้าไลบรารี Aspose.Imaging

ก่อนอื่น, ให้เพิ่มไลบรารี Aspose.Imaging ในโปรเจกต์ Java ของคุณโดยใส่คำสั่ง import ดังนี้:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fonts.FontSettings;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.odg.OdgRasterizationOptions;
```

ตอนนี้เราได้ทำการนำเข้าแพ็กเกจที่ต้องการแล้ว, เราจะอธิบายกระบวนการแปลงและการเพิ่มประสิทธิภาพฟอนต์เป็นขั้นตอนที่ชัดเจน.

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

ก่อนทำการแปลง, คุณต้องระบุตำแหน่งโฟลเดอร์ที่เก็บไฟล์ต้นฉบับและที่ที่จะบันทึกไฟล์ PNG ผลลัพธ์.

```java
String dataDir = "C:/Documents/";
String outDir = Utils.getOutDir("DefaultFontUsageImprove");
```

> **เคล็ดลับ:** เก็บฟอนต์ของคุณในโฟลเดอร์ย่อย (เช่น `fonts/`) ภายใน `dataDir` เพื่อให้ง่ายต่อการอ้างอิง

## ขั้นตอนที่ 2: กำหนดค่าการตั้งค่าฟอนต์

เพื่อปรับปรุงการใช้ฟอนต์เริ่มต้น, กำหนดค่าการตั้งค่าฟอนต์ดังต่อไปนี้. ที่นี่เราจะ **set default font Aspose** สำหรับเซสชันการแปลง.

```java
FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
FontSettings.setGetSystemAlternativeFont(false);
```

กัน.ให้ใช้ “Arial” เทียบกับ “Courier New”.

```java
exportToPng(Path.combine(dataDir, "missing-font2.odg"), "Arial", Path.combine(outDir, "arial.png"));
exportToPng(
    Path.combine(dataDir, "missing-font2.odg"),
    "Courier New",
    Path.combine(outDir, "courier.png"));
```

## ขั้นตอนที่ 4: ฟังก์ชัน Export to PNG (ตรรกะการแปลงหลัก)

นี่คือเมธอด `exportToPng` ที่ทำการ **แปลงเอกสารเป็น PNG** จริงโดยใช้ฟอนต์เริ่มต้นที่เลือก.

```java
private static void exportToPng(String filePath, String defaultFontName, String outfileName)
{
    FontSettings.setDefaultFontName(defaultFontName);
    try (Image document = Image.load(filePath))
    {
        PngOptions saveOptions = new PngOptions();
        final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
        rasterizationOptions.setPageWidth(1000);
        rasterizationOptions.setPageHeight(1000);
        saveOptions.setVectorRasterizationOptions(rasterizationOptions);
        document.save(outfileName, saveOptions);
    }
    Utils.deleteFile(outfileName);
}
```

เมธอดนี้ตั้งค่าฟอนต์เริ่มต้น, โหลดไฟล์ ODG ต้นฉบับ, กำหนดตัวเลือกการส่งออก PNG, และบันทึกภาพที่แรสเตอร์ลงดิสก์.

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| ตัวอักษรหายใน PNG | ฟอนต์ไม่พบในโฟลเดอร์ที่ระบุ | ตรวจสอบให้แน่ใจว่า ` | ปรับ `rasterizationOptions.setPageWidth/Height` ให้ตรงกับขนาดเอกสารต้นฉบับ |
| การแปลงช้าเมื่อไฟล์ขนาดใหญ่ | ตั้งค่าความละเอียดสูง | ลด `PageWidth`/`PageHeight` หรือประมวลผลหน้าเป็นชุด |

## คำถามที่พบบ่อย

**Q: Aspose.Imaging สำหรับ Java คืออะไร?**  
A: Aspose.Imaging สำหรับ Java เป็นไลบรารีที่ครอบคลุมซึ่งช่วยให้คุณสร้าง, แปลง, และจัดการภาพแรสเตอร์และเวกเตอร์ในรูปแบบกว่า 100 ฟอร์แมต.

**Q: จะได้ Aspose.Imaging สำหรับ Java อย่างไร?**  
A: คุณสามารถดาวน์โหลด Aspose.Imaging สำหรับ Java ได้จากเว็บไซต์ที่ [this link](https://releases.aspose.com/imaging/java/).

**Q: มีตัวเลือกไลเซนส์สำหรับ Aspose.Imaging สำหรับ Java หรือไม่?**  
A: มี, คุณสามารถซื้อไลเซนส์สำหรับ Aspose.Imaging สำหรับ Java ได้จาก [purchase page](https://purchase.aspose.com/buy).

**Q: มีเวอร์ชันทดลองฟรีหรือไม่?**  
A: มี, คุณสามารถลอง Aspose.Imaging สำหรับ Java ฟรีโดยดาวน์โหลดเวอร์ชันทดลองจาก [here](https://releases.aspose.com/).

**Q: จะขอรับการสนับสนุนสำหรับ Aspose.Imaging สำหรับ Java ได้จากที่ไหน?**  
A: หากต้องการความช่วยเหลือหรือมีคำถาม, คุณสามารถเยี่ยมชมฟอรั่มสนับสนุน Aspose.Imaging สำหรับ Java ที่ [https://forum.aspose.com/](https://forum.aspose.com/).

---

**อัปเดตล่าสุด:** 2026-01-19  
**ทดสอบด้วย:** Aspose.Imaging สำหรับ Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}