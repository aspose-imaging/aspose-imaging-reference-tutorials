---
"description": "เรียนรู้วิธีเพิ่มประสิทธิภาพการใช้แบบอักษรเริ่มต้นด้วย Aspose.Imaging สำหรับ Java ปรับปรุงการประมวลผลเอกสารของคุณด้วยคำแนะนำทีละขั้นตอน"
"linktitle": "เพิ่มประสิทธิภาพการใช้งานแบบอักษรเริ่มต้น"
"second_title": "API การประมวลผลภาพ Java ของ Aspose.Imaging"
"title": "การเพิ่มประสิทธิภาพการใช้งานฟอนต์เริ่มต้นด้วย Aspose.Imaging สำหรับ Java"
"url": "/th/java/image-processing-and-enhancement/optimize-default-font-usage/"
"weight": 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# การเพิ่มประสิทธิภาพการใช้งานฟอนต์เริ่มต้นด้วย Aspose.Imaging สำหรับ Java

ในโลกของการประมวลผลเอกสารและการจัดการรูปภาพ Aspose.Imaging สำหรับ Java ถือเป็นเครื่องมือที่มีประสิทธิภาพ ไลบรารี Java อเนกประสงค์นี้ช่วยให้ผู้พัฒนาสามารถสร้าง แก้ไข และแปลงรูปภาพได้อย่างง่ายดาย หนึ่งในประเด็นสำคัญของการปรับปรุงการประมวลผลเอกสารของคุณคือการปรับปรุงการใช้แบบอักษร ในคู่มือทีละขั้นตอนนี้ เราจะสำรวจวิธีปรับปรุงการใช้แบบอักษรเริ่มต้นโดยใช้ Aspose.Imaging สำหรับ Java เราจะแบ่งตัวอย่างแต่ละตัวอย่างออกเป็นหลายขั้นตอนเพื่อให้แน่ใจว่าคุณเข้าใจกระบวนการนี้อย่างถ่องแท้

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเจาะลึกกระบวนการเพิ่มประสิทธิภาพ โปรดตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java ติดตั้งอยู่บนระบบของคุณ
- ไลบรารี Aspose.Imaging สำหรับ Java คุณสามารถดาวน์โหลดได้จาก [เว็บไซต์](https://releases-aspose.com/imaging/java/).
- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรมภาษา Java

## แพ็คเกจนำเข้า

หากต้องการเริ่มต้นใช้งานแบบอักษรเริ่มต้นให้เหมาะสม คุณต้องนำเข้าแพ็คเกจที่จำเป็นจาก Aspose.Imaging สำหรับ Java โดยทำตามขั้นตอนต่อไปนี้:

นำเข้าไลบรารี Aspose.Imaging

ขั้นแรก รวมไลบรารี Aspose.Imaging ไว้ในโปรเจ็กต์ Java ของคุณโดยเพิ่มคำสั่งนำเข้าต่อไปนี้:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fonts.FontSettings;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.odg.OdgRasterizationOptions;
```

ตอนนี้เราได้นำเข้าแพ็คเกจที่จำเป็นแล้ว มาแบ่งกระบวนการเพิ่มประสิทธิภาพออกเป็นขั้นตอนต่างๆ กัน

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

ก่อนที่จะเพิ่มประสิทธิภาพการใช้แบบอักษร คุณต้องตั้งค่าไดเรกทอรีเอกสารของคุณก่อน แทนที่ `"Your Document Directory" + "otg/"` โดยมีเส้นทางไปยังไดเร็กทอรีเอกสารของคุณ ตัวอย่างเช่น:

```java
String dataDir = "C:/Documents/";
String outDir = Utils.getOutDir("DefaultFontUsageImprove");
```

## ขั้นตอนที่ 2: กำหนดค่าการตั้งค่าแบบอักษร

เพื่อปรับปรุงการใช้แบบอักษรเริ่มต้น ให้กำหนดค่าการตั้งค่าแบบอักษรดังต่อไปนี้:

```java
FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
FontSettings.setGetSystemAlternativeFont(false);
```

## ขั้นตอนที่ 3: ส่งออกเป็น PNG ด้วยแบบอักษรเริ่มต้น

ตอนนี้เรามาส่งออกเอกสารเป็นรูปภาพ PNG โดยใช้แบบอักษรเริ่มต้นที่ระบุไว้กัน ในที่นี้ เรามีตัวอย่างสองตัวอย่าง ตัวอย่างหนึ่งใช้ "Arial" และอีกตัวอย่างหนึ่งใช้ "Courier New" เป็นแบบอักษรเริ่มต้น

```java
exportToPng(Path.combine(dataDir, "missing-font2.odg"), "Arial", Path.combine(outDir, "arial.png"));
exportToPng(
    Path.combine(dataDir, "missing-font2.odg"),
    "Courier New",
    Path.combine(outDir, "courier.png"));
```

## ขั้นตอนที่ 4: ส่งออกไปยังฟังก์ชัน PNG

นี่คือ `exportToPng` ฟังก์ชันสำหรับดำเนินการส่งออกจริงไปยัง PNG ด้วยแบบอักษรเริ่มต้นที่ระบุ:

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

ฟังก์ชันนี้จะตั้งค่าแบบอักษรเริ่มต้น โหลดเอกสาร กำหนดค่าตัวเลือกการส่งออก และบันทึกไฟล์ภาพ PNG เอาท์พุต

## บทสรุป

การเพิ่มประสิทธิภาพการใช้แบบอักษรเริ่มต้นในการประมวลผลเอกสารสามารถปรับปรุงคุณภาพของผลลัพธ์ของคุณได้อย่างมาก Aspose.Imaging สำหรับ Java ทำให้กระบวนการนี้ง่ายขึ้น ช่วยให้คุณสามารถระบุแบบอักษรและส่งออกเอกสารได้อย่างมีประสิทธิภาพ หากปฏิบัติตามคำแนะนำทีละขั้นตอนที่ระบุไว้ในบทความนี้ คุณสามารถปรับปรุงการใช้แบบอักษรของคุณได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.Imaging สำหรับ Java คืออะไร

A1: Aspose.Imaging สำหรับ Java คือไลบรารี Java ที่มีคุณลักษณะมากมายสำหรับการทำงานกับรูปภาพและเอกสาร รวมถึงการสร้าง การแปลง และการจัดการรูปภาพ

### คำถามที่ 2: ฉันสามารถรับ Aspose.Imaging สำหรับ Java ได้อย่างไร

A2: คุณสามารถดาวน์โหลด Aspose.Imaging สำหรับ Java ได้จากเว็บไซต์ที่ [ลิงค์นี้](https://releases-aspose.com/imaging/java/).

### คำถามที่ 3: มีตัวเลือกการออกใบอนุญาตสำหรับ Aspose.Imaging สำหรับ Java หรือไม่

A3: ใช่ คุณสามารถซื้อใบอนุญาตสำหรับ Aspose.Imaging สำหรับ Java ได้จาก [หน้าการซื้อ](https://purchase-aspose.com/buy).

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

A4: ใช่ คุณสามารถทดลองใช้ Aspose.Imaging สำหรับ Java ได้ฟรีโดยดาวน์โหลดเวอร์ชันทดลองใช้จาก [ที่นี่](https://releases-aspose.com/).

### คำถามที่ 5: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.Imaging สำหรับ Java ได้จากที่ไหน

A5: หากคุณต้องการความช่วยเหลือหรือมีคำถาม คุณสามารถไปที่ฟอรัมสนับสนุน Aspose.Imaging สำหรับ Java ได้ที่ [https://forum.aspose.com/](https://forum-aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}