---
title: การเพิ่มประสิทธิภาพการใช้แบบอักษรเริ่มต้นด้วย Aspose.Imaging สำหรับ Java
linktitle: ปรับการใช้แบบอักษรเริ่มต้นให้เหมาะสม
second_title: Aspose.Imaging Java Image Processing API
description: เรียนรู้วิธีปรับการใช้แบบอักษรเริ่มต้นให้เหมาะสมด้วย Aspose.Imaging สำหรับ Java ปรับปรุงการประมวลผลเอกสารของคุณด้วยคำแนะนำทีละขั้นตอน
weight: 10
url: /th/java/image-processing-and-enhancement/optimize-default-font-usage/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การเพิ่มประสิทธิภาพการใช้แบบอักษรเริ่มต้นด้วย Aspose.Imaging สำหรับ Java

ในโลกของการประมวลผลเอกสารและการจัดการรูปภาพ Aspose.Imaging สำหรับ Java โดดเด่นในฐานะเครื่องมืออันทรงพลัง ไลบรารี Java อเนกประสงค์นี้ช่วยให้นักพัฒนาสามารถสร้าง แก้ไข และแปลงรูปภาพได้อย่างง่ายดาย ลักษณะสำคัญประการหนึ่งในการเพิ่มประสิทธิภาพการประมวลผลเอกสารของคุณคือการปรับปรุงการใช้แบบอักษร ในคำแนะนำทีละขั้นตอนนี้ เราจะสำรวจวิธีปรับการใช้งานแบบอักษรเริ่มต้นให้เหมาะสมโดยใช้ Aspose.Imaging สำหรับ Java เราจะแบ่งแต่ละตัวอย่างออกเป็นหลายขั้นตอนเพื่อให้แน่ใจว่าคุณเข้าใจกระบวนการอย่างละเอียด

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกกระบวนการเพิ่มประสิทธิภาพ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java ที่ติดตั้งบนระบบของคุณ
-  Aspose.Imaging สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์](https://releases.aspose.com/imaging/java/).
- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม Java

## แพ็คเกจนำเข้า

หากต้องการเริ่มต้นเพิ่มประสิทธิภาพการใช้แบบอักษรเริ่มต้น คุณต้องนำเข้าแพ็คเกจที่จำเป็นจาก Aspose.Imaging สำหรับ Java นี่คือขั้นตอนในการทำเช่นนั้น:

นำเข้าไลบรารี Aspose.Imageing

ขั้นแรก รวมไลบรารี Aspose.Imaging ในโปรเจ็กต์ Java ของคุณโดยเพิ่มคำสั่งนำเข้าต่อไปนี้:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fonts.FontSettings;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.odg.OdgRasterizationOptions;
```

ตอนนี้เราได้นำเข้าแพ็คเกจที่จำเป็นแล้ว เรามาแบ่งกระบวนการปรับให้เหมาะสมออกเป็นหลายขั้นตอนกัน

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ

 ก่อนที่จะปรับการใช้แบบอักษรให้เหมาะสม คุณต้องตั้งค่าไดเร็กทอรีเอกสารของคุณก่อน แทนที่`"Your Document Directory" + "otg/"` ด้วยเส้นทางจริงไปยังไดเร็กทอรีเอกสารของคุณ ตัวอย่างเช่น:

```java
String dataDir = "C:/Documents/";
String outDir = Utils.getOutDir("DefaultFontUsageImprove");
```

## ขั้นตอนที่ 2: กำหนดการตั้งค่าแบบอักษร

หากต้องการปรับปรุงการใช้แบบอักษรเริ่มต้น ให้กำหนดการตั้งค่าแบบอักษรดังต่อไปนี้:

```java
FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
FontSettings.setGetSystemAlternativeFont(false);
```

## ขั้นตอนที่ 3: ส่งออกเป็น PNG ด้วยแบบอักษรเริ่มต้น

ตอนนี้ เรามาส่งออกเอกสารเป็นรูปภาพ PNG โดยใช้แบบอักษรเริ่มต้นที่ระบุ เรามีตัวอย่างสองตัวอย่าง ตัวอย่างหนึ่งใช้ "Arial" และอีกตัวอย่างหนึ่งใช้ "Courier New" เป็นแบบอักษรเริ่มต้น

```java
exportToPng(Path.combine(dataDir, "missing-font2.odg"), "Arial", Path.combine(outDir, "arial.png"));
exportToPng(
    Path.combine(dataDir, "missing-font2.odg"),
    "Courier New",
    Path.combine(outDir, "courier.png"));
```

## ขั้นตอนที่ 4: ส่งออกไปยังฟังก์ชัน PNG

 นี่คือ`exportToPng` ฟังก์ชั่นในการดำเนินการส่งออกจริงไปยัง PNG ด้วยแบบอักษรเริ่มต้นที่ระบุ:

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

ฟังก์ชันนี้จะตั้งค่าแบบอักษรเริ่มต้น โหลดเอกสาร กำหนดค่าตัวเลือกการส่งออก และบันทึกอิมเมจ PNG เอาต์พุต

## บทสรุป

การเพิ่มประสิทธิภาพการใช้แบบอักษรเริ่มต้นในการประมวลผลเอกสารสามารถปรับปรุงคุณภาพงานพิมพ์ของคุณได้อย่างมาก Aspose.Imaging สำหรับ Java ช่วยให้กระบวนการนี้ง่ายขึ้น ช่วยให้คุณสามารถระบุแบบอักษรและส่งออกเอกสารได้อย่างมีประสิทธิภาพ ด้วยการทำตามคำแนะนำทีละขั้นตอนที่อธิบายไว้ในบทความนี้ คุณสามารถปรับปรุงการใช้แบบอักษรของคุณได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Imaging สำหรับ Java คืออะไร

คำตอบ 1: Aspose.Imaging for Java เป็นไลบรารี Java ที่มีคุณสมบัติมากมายสำหรับการทำงานกับรูปภาพและเอกสาร รวมถึงการสร้างรูปภาพ การแปลง และการจัดการ

### คำถามที่ 2: ฉันจะรับ Aspose.Imaging สำหรับ Java ได้อย่างไร

 A2: คุณสามารถดาวน์โหลด Aspose.Imaging สำหรับ Java ได้จากเว็บไซต์ที่[ลิงค์นี้](https://releases.aspose.com/imaging/java/).

### คำถามที่ 3: มีตัวเลือกสิทธิ์การใช้งานสำหรับ Aspose.Imaging สำหรับ Java หรือไม่

 A3: ได้ คุณสามารถซื้อใบอนุญาตสำหรับ Aspose.Imaging สำหรับ Java ได้จาก[หน้าซื้อ](https://purchase.aspose.com/buy).

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

A4: ได้ คุณสามารถลองใช้ Aspose.Imaging สำหรับ Java ได้ฟรีโดยดาวน์โหลดเวอร์ชันทดลองใช้งานจาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะรับการสนับสนุนสำหรับ Aspose.Imaging สำหรับ Java ได้ที่ไหน

 A5: หากคุณต้องการความช่วยเหลือหรือมีคำถาม คุณสามารถไปที่ฟอรัมสนับสนุน Aspose.Imaging for Java ได้ที่[https://forum.aspose.com/](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
