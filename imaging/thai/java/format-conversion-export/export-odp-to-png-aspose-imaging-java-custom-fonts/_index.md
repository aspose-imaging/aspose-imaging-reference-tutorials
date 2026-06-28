---
date: '2026-06-28'
description: เรียนรู้วิธีแปลง ODP เป็น PNG ด้วย Aspose.Imaging for Java, ตั้งค่า custom
  fonts, และปิดการใช้งาน system fonts เพื่อการเรนเดอร์ที่แม่นยำ
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: วิธีแปลง ODP เป็น PNG ด้วย Aspose.Imaging for Java – Custom Fonts & Export
  Guide
url: /th/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# วิธีแปลง ODP เป็น PNG ด้วย Aspose.Imaging สำหรับ Java – ฟอนต์กำหนดเองและคู่มือการส่งออก

ในแอปพลิเคชัน Java สมัยใหม่ การแปลงไฟล์ OpenDocument Presentation (ODP) ให้เป็นภาพ PNG คุณภาพสูงเป็นความต้องการทั่วไป—โดยเฉพาะเมื่อคุณต้องการรักษาแบรนด์ผ่านฟอนต์กำหนดเอง บทเรียนนี้จะแสดง **วิธีแปลง ODP** เป็น PNG ด้วย Aspose.Imaging สำหรับ Java, แนะนำการตั้งค่าโฟลเดอร์ฟอนต์กำหนดเอง, การปิดการใช้งานฟอนต์สำรองของระบบ, และการปรับแต่งตัวเลือกการเรสเตอร์ไลซ์เพื่อประสิทธิภาพที่ดีที่สุด

**สิ่งที่คุณจะได้เรียน**
- วิธีตั้งค่าไดเรกทอรีฟอนต์กำหนดเองสำหรับการแปลง ODP  
- วิธีปิดการใช้งานฟอนต์สำรองของระบบเพื่อให้ใช้ฟอนต์ที่คุณเลือกเท่านั้น  
- วิธีส่งออกไฟล์ ODP เป็น PNG ด้วยขนาดและการตั้งค่าฟอนต์ที่แม่นยำ  
- เคล็ดลับในการเพิ่มความเร็วและลดการใช้หน่วยความจำเมื่อประมวลผลงานนำเสนอขนาดใหญ่  

## คำตอบสั้น ๆ
- **Can I use Maven to add Aspose.Imaging?** Yes, add the Maven dependency and run `mvn install`.  
- **Do I need a license for production?** A valid Aspose.Imaging license is required for unlimited use.  
- **Will my custom fonts be respected?** Set the fonts folder and disable system alternatives to enforce them.  
- **What image formats are supported?** Aspose.Imaging supports 120+ raster and vector formats, including PNG, JPEG, TIFF, and WebP.  
- **Is the API thread‑safe?** Yes, most Aspose.Imaging classes are safe for concurrent use when you create separate instances per thread.

## “how to convert odp” คืออะไร?
*“How to convert odp”* หมายถึงกระบวนการแปลงไฟล์ OpenDocument Presentation ให้เป็นรูปแบบอื่น—โดยทั่วไปคือ PNG—พร้อมคงรักษาเลย์เอาต์, ฟอนต์, และความแม่นยำของภาพ Aspose.Imaging สำหรับ Java มีเวิร์กโฟลว์แบบเมธอดเดียวที่จัดการการแปลงนี้โดยไม่ต้องใช้เครื่องมือภายนอก ทำให้นักพัฒนาสามารถรวมการแปลงเข้ากับแอปพลิเคชันของตนได้โดยใช้โค้ดเพียงเล็กน้อย

## ทำไมต้องใช้ Aspose.Imaging สำหรับ Java?
Aspose.Imaging รองรับ **รูปแบบผลลัพธ์กว่า 120** แบบและสามารถเรสเตอร์ไลซ์ไฟล์ ODP หลายหน้าโดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ลดการใช้ RAM สูงสุดได้ถึง 70 % สำหรับงานนำเสนอขนาดใหญ่ ไลบรารียังมีการจัดการฟอนต์ในตัว ทำให้ไม่ต้องพึ่งเอนจินการเรนเดอร์ของบุคคลที่สาม

## ข้อกำหนดเบื้องต้น
- **Libraries**: Aspose.Imaging for Java ≥ 25.5.  
- **JDK**: Version 8 หรือใหม่กว่า.  
- **IDE**: IntelliJ IDEA, Eclipse, หรือเครื่องมือแก้ไข Java ใด ๆ.  
- **Basic Knowledge**: Java I/O, object‑oriented programming, and image concepts.

## คำแนะนำการติดตั้ง

### Maven
เพิ่ม dependency ด้านล่างลงในไฟล์ `pom.xml` ของคุณและรัน `mvn clean install`:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
ใส่ไลบรารีในไฟล์ `build.gradle` ของคุณและรีเฟรชโปรเจกต์:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Direct Download
ดาวน์โหลด JAR ล่าสุดจาก [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

## ขั้นตอนการรับไลเซนส์
เพื่อเปิดใช้งานฟังก์ชันเต็มรูปแบบ ให้ใช้ไลเซนส์แบบชั่วคราวหรือถาวร:

1. **Free Trial** – ไม่ต้องใช้ไลเซนส์, ฟีเจอร์จำกัด.  
2. **Temporary License** – ขอรับได้จาก [Aspose website](https://purchase.aspose.com/temporary-license/).  
3. **Purchase** – ซื้อการสมัครหรือไลเซนส์ถาวรจาก [Aspose purchase page](https://purchase.aspose.com/buy).

เริ่มต้นใช้งานไลบรารีด้วยไฟล์ไลเซนส์ของคุณ:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## วิธีตั้งค่าโฟลเดอร์ฟอนต์กำหนดเองสำหรับการแปลง ODP?
`FontSettings` เป็นคลาสที่จัดการทรัพยากรฟอนต์สำหรับ Aspose.Imaging โหลดฟอนต์กำหนดเองของคุณก่อนเริ่มการประมวลผลภาพใด ๆ เพื่อให้ทุกสไลด์ใช้แบบอักษรที่คุณกำหนด

ตั้งค่าเส้นทางโฟลเดอร์ฟอนต์โดยใช้ `FontSettings` ของ Aspose.Imaging:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Definition anchor*: `FontSettings.setFontsFolder` บอก Aspose.Imaging ให้มองหาไฟล์ TrueType และ OpenType บนระบบไฟล์

## วิธีปิดการใช้งานฟอนต์สำรองของระบบระหว่างการแปลง ODP?
การปิดฟอนต์สำรองของระบบทำให้เอนจินการเรนเดอร์ละเลยฟอนต์ที่ติดตั้งบน OS, รับประกันว่าจะใช้เฉพาะฟอนต์ที่คุณจัดเตรียมไว้เท่านั้น ซึ่งช่วยหลีกเลี่ยงการแทนที่ฟอนต์ที่อาจทำให้สไลด์เปลี่ยนแปลงลักษณะ

ปิดฟอนต์สำรองของระบบด้วยคำสั่งต่อไปนี้:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Definition anchor*: `FontSettings.setGetSystemAlternativeFont(false)` บังคับให้เอนจินใช้ฟอนต์จากโฟลเดอร์ที่กำหนดเท่านั้น, ไม่ให้มีการแทนที่โดยอัตโนมัติ

## วิธีส่งออกไฟล์ ODP เป็น PNG พร้อมกำหนดฟอนต์?
`RasterizationOptions` กำหนดวิธีการเรสเตอร์ไลซ์หน้าเวกเตอร์เป็นภาพบิตแมพ โดยการรวมการตั้งค่าฟอนต์กับตัวเลือกการเรสเตอร์ไลซ์ คุณสามารถควบคุม DPI, สีพื้นหลัง, และขนาดหน้าได้สำหรับแต่ละ PNG ที่ส่งออก

ดำเนินการเมธอดการส่งออกตามตัวอย่างด้านล่าง:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*Definition anchor*: คลาส `RasterizationOptions` ควบคุม DPI, ขนาดหน้า, และสีพื้นหลังของไฟล์ PNG ที่สร้างขึ้น

### ข้อผิดพลาดทั่วไป & วิธีแก้
- **Missing font files** – ตรวจสอบให้แน่ใจว่าไฟล์ `.ttf` หรือ `.otf` ทุกไฟล์ที่อ้างอิงใน ODP มีอยู่ในโฟลเดอร์ที่ตั้งค่าไว้.  
- **Incorrect file paths** – ใช้เส้นทางแบบ absolute หรือแก้ไขเส้นทาง relative เทียบกับ `System.getProperty("user.dir")`.  
- **Insufficient permissions** – ตรวจสอบให้กระบวนการ Java สามารถอ่านโฟลเดอร์ฟอนต์และเขียนไปยังโฟลเดอร์ผลลัพธ์ได้.

## การประยุกต์ใช้ในเชิงปฏิบัติ
1. **Brand‑consistent slide decks** – ส่งออกงานนำเสนอเป็น PNG สำหรับการเผยแพร่บนเว็บโดยคงฟอนต์องค์กร.  
2. **Automated report generation** – แปลงแต่ละสไลด์เป็นภาพเพื่อใส่ในรายงาน PDF หรือจดหมายข่าวอีเมล.  
3. **Legacy archive creation** – เก็บเนื้อหา ODP เป็น PNG เพื่อรับประกันการเข้าถึงในอนาคตโดยไม่ต้องใช้โปรแกรมดู ODP.

## พิจารณาด้านประสิทธิภาพ
- ใช้เวอร์ชันล่าสุดของ Aspose.Imaging เพื่อรับประโยชน์จากการเรสเตอร์ไลซ์แบบหลายเธรด (เร็วขึ้นถึง 2× บน CPU 8‑core).  
- ห่อการประมวลผลภาพในบล็อก `try‑with‑resources` เพื่อรับประกันการปล่อยทรัพยากรเนทีฟทันเวลา.  
- ปรับ `RasterizationOptions` (เช่น ลด DPI) เมื่อประมวลผลสไลด์หลายพันสไลด์เพื่อสมดุลคุณภาพและการใช้หน่วยความจำ.

## คำถามที่พบบ่อย

**Q: What is the minimum Java version required?**  
A: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended for long‑term support.

**Q: Can I convert only selected slides?**  
A: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before calling `save`.

**Q: How do I handle password‑protected ODP files?**  
A: Load the file with `LoadOptions` that includes the password, then proceed with the same font settings.

**Q: Does disabling system fonts affect performance?**  
A: It marginally improves speed because the engine skips the lookup of system fonts, especially noticeable on machines with large font collections.

**Q: Where can I find more code samples?**  
A: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/) for additional scenarios such as batch conversion and image transformations.

## แหล่งข้อมูลเพิ่มเติม
- [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/)  
- [Start Your Free Trial](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)  
- [Aspose.Imaging Forum](https://forum.aspose.com/c/imaging/14)  
- [Buy Aspose Licensing](https://purchase.aspose.com/buy)  
- [Apply for a Temporary License](https://purchase.aspose.com/temporary-license/)  

---

**Last Updated:** 2026-06-28  
**Tested With:** Aspose.Imaging for Java 25.5  
**Author:** Aspose

## บทเรียนที่เกี่ยวข้อง

- [Convert ODG to PNG with Aspose.Imaging for Java: A Complete Guide](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)  
- [Efficient Image Conversion in Java with Aspose.Imaging: A Complete Guide](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}