---
date: '2026-06-18'
description: เรียนรู้วิธีแปลง djvu เป็น BMP ใน Java ด้วย Aspose.Imaging คู่มือนี้แสดงการตั้งค่า
  dependency ของ Aspose.Imaging ใน Maven, การกำหนดค่า, และตัวเลือกการส่งออก
keywords:
- how to convert djvu
- maven aspose imaging dependency
- djvu to bmp conversion
- aspose imaging java
- image format export
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how to convert djvu to BMP in Java using Aspose.Imaging. This
    guide shows Maven Aspose.Imaging dependency setup, configuration, and export options.
  headline: How to Convert DjVu to BMP with Aspose.Imaging for Java
  type: TechArticle
- questions:
  - answer: It is a library for processing, converting, and analyzing images across
      100+ formats, including DjVu and BMP.
    question: What is Aspose.Imaging for Java used for?
  - answer: Use `IntRange` to export only needed pages and process each page in a
      separate try‑with‑resources block to keep memory usage low.
    question: How do I handle large DjVu documents during conversion?
  - answer: Yes – adjust `BmpOptions.setBitsPerPixel()` (e.g., 24 for 16‑million colors,
      32 for true‑color with alpha).
    question: Can I customize BMP quality?
  - answer: Verify the file path, ensure the license is loaded, and check that the
      DjVu file isn’t corrupted. Review the stack trace for the exact cause.
    question: What should I do if conversion throws an exception?
  - answer: The official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      contains extensive code samples and API references.
    question: Where can I find more Aspose.Imaging examples?
  type: FAQPage
title: วิธีแปลง DjVu เป็น BMP ด้วย Aspose.Imaging สำหรับ Java
url: /th/java/format-conversion-export/export-djvu-to-bmp-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# วิธีแปลง DjVu เป็น BMP ด้วย Aspose.Imaging สำหรับ Java

## บทนำ

**วิธีแปลง djvu** ไฟล์ให้เป็นรูปแบบ BMP ที่รองรับโดยทั่วไปเป็นความต้องการทั่วไปสำหรับนักพัฒนาที่ทำงานกับเอกสารเก็บถาวร, กระบวนการประมวลผลภาพ, หรือแอปพลิเคชันข้ามแพลตฟอร์ม ในบทแนะนำนี้คุณจะได้ค้นพบวิธีที่เร็วและเชื่อถือได้ในการทำการแปลงนี้โดยใช้ Aspose.Imaging สำหรับ Java เราจะเดินผ่านการตั้งค่าสภาพแวดล้อม, การโหลดเอกสาร DjVu, การกำหนดค่า BMP, การเลือกช่วงหน้า, และสุดท้ายการบันทึกไฟล์ผลลัพธ์

**สิ่งที่คุณจะได้เรียนรู้**
- วิธีเพิ่มการพึ่งพา Maven Aspose.Imaging ลงในโปรเจกต์ของคุณ  
- การโหลดภาพ DjVu ด้วย Aspose.Imaging  
- การกำหนดค่า BMP options เพื่อคุณภาพที่ดีที่สุด  
- การส่งออกหน้าที่เลือกจากเอกสาร DjVu หลายหน้า  
- เคล็ดลับการจัดการหน่วยความจำและประสิทธิภาพ

## คำตอบอย่างรวดเร็ว
- **Can I use Maven for the dependency?** Yes – add the `aspose-imaging` artifact to your `pom.xml`.  
- **Which class loads DjVu files?** `Image.load()` reads any supported format, including DjVu.  
- **How do I set BMP quality?** Use `BmpOptions.setBitsPerPixel(32)` for true‑color output.  
- **Is page‑range export supported?** Absolutely – create an `IntRange` with the desired start and end indices.  
- **Do I need a license for production?** A commercial license removes evaluation limits; a free trial works for testing.

## Aspose.Imaging สำหรับ Java คืออะไร?
`Aspose.Imaging for Java` เป็นไลบรารีการประมวลผลภาพที่ครอบคลุมซึ่งรองรับ **100+** รูปแบบแรสเตอร์และเวกเตอร์และสามารถจัดการไฟล์ขนาดถึง **2 GB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ มันให้ API แบบรวมศูนย์สำหรับการแปลง, การแก้ไข, และการวิเคราะห์ ทำให้เหมาะสำหรับเวิร์กโฟลว์ภาพฝั่งเซิร์ฟเวอร์

## ทำไมต้องแปลง DjVu เป็น BMP?
การแปลง DjVu เป็น BMP มักจำเป็นเมื่อระบบเก่าหรือเครื่องมือบน Windows ต้องการรูปแบบภาพที่ง่ายและไม่มีการบีบอัด ไฟล์ BMP เก็บข้อมูลพิกเซลของแหล่งที่มาตรง ๆ ทำให้ไม่มีการสูญเสียคุณภาพระหว่างการแปลง และสามารถอ่านได้ทั่วโลกโดยไม่ต้องใช้โค้ดคอดเพิ่มเติม ทำให้ BMP เป็นรูปแบบกลางที่ปลอดภัยสำหรับการประมวลผลต่อหรือการเก็บถาวร

- **ความเข้ากันได้กว้าง:** BMP รองรับโดยเนทีฟบน Windows, โปรแกรมแก้ไขกราฟิกหลายตัว, และระบบเก่า  
- **ผลลัพธ์ไม่มีการสูญเสีย:** BMP เก็บข้อมูลพิกเซลโดยไม่มีการบีบอัด, รักษาความคมชัดดั้งเดิมของหน้าต่าง DjVu  
- **การทำงานอัตโนมัติเป็นชุด:** Aspose.Imaging สามารถประมวลผลหลายพันหน้าในรอบเดียว, ลดความพยายามด้วยมือ

## ข้อกำหนดเบื้องต้น

- **Java Development Kit (JDK) 8+** – ตรวจสอบให้ `java -version` แสดง 1.8 หรือสูงกว่า  
- **IDE** – IntelliJ IDEA, Eclipse, หรือเครื่องมือแก้ไข Java ใด ๆ  
- **Maven** – สำหรับการจัดการการพึ่งพา (หรือ Gradle หากคุณต้องการ)  
- **ความรู้พื้นฐาน Java** – คุ้นเคยกับคลาส, เมธอด, และการจัดการข้อยกเว้น  

## การตั้งค่า Aspose.Imaging สำหรับ Java

### การพึ่งพา Maven
เพิ่มโค้ดสแนปเพ็ทต่อไปนี้ในไฟล์ `pom.xml` ของคุณ นี่คือ **Maven Aspose.Imaging dependency** ที่จำเป็นสำหรับการแปลง

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>23.12</version> <!-- Use the latest version -->
</dependency>
```
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### การพึ่งพา Gradle
หากคุณใช้ Gradle ให้แทรกบรรทัดนี้ลงในไฟล์ `build.gradle` ของคุณ

```groovy
implementation 'com.aspose:aspose-imaging:23.12'
```
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### ดาวน์โหลดโดยตรง
ดาวน์โหลดเวอร์ชันล่าสุดจาก [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/)

## ขั้นตอนการรับใบอนุญาต

เพื่อเปิดใช้งานฟังก์ชันเต็มคุณจะต้องมีไฟล์ใบอนุญาต:

- **Free Trial** – ประเมินคุณสมบัติทั้งหมดโดยไม่มีค่าใช้จ่าย  
- **Temporary License** – ขอคีย์ที่มีระยะเวลาจำกัดสำหรับการทดสอบต่อเนื่อง  
- **Full Purchase** – รับใบอนุญาตการผลิตเพื่อการใช้ไม่จำกัด

หลังจากได้รับ `Aspose.Imaging.lic` ให้วางไฟล์นี้ในโฟลเดอร์ resources ของโปรเจกต์และเริ่มต้นตามที่แสดงด้านล่าง:

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("Aspose.Imaging.lic");
```
```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path_to_your_license_file");
```

## คู่มือการดำเนินการ

ขั้นตอนการแปลงจะแบ่งเป็นส่วนย่อย ๆ แต่ละส่วนมีคำตอบสั้น ๆ ตามด้วยคำอธิบายละเอียด

### วิธีโหลดภาพ DjVu?

`Image.load` เป็นเมธอดสแตติกที่อ่านไฟล์ภาพของรูปแบบที่รองรับทั้งหมดและคืนค่าอ็อบเจ็กต์ `Image` ที่แสดงเนื้อหา ใช้บรรทัดเดียว `Image image = Image.load("sample.djvu");` เพื่อโหลดไฟล์ DjVu นี้จะสร้างการแสดงผลในหน่วยความจำที่คุณสามารถสอบถามจำนวนหน้า, ขนาด, หรือเมตาดาต้า และเป็นจุดเริ่มต้นสำหรับการประมวลผลต่อไป

**ขั้นตอนที่ 1: นำเข้าแพ็กเกจที่จำเป็น**  
```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.djvu.DjvuImage;
```

**ขั้นตอนที่ 2: โหลดภาพ DjVu**  
```java
String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "Sample.djvu"; 
try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
    // Image is loaded and ready for processing
} catch (Exception e) {
    e.printStackTrace();
}
```  
ที่นี่เราระบุเส้นทางไฟล์และเรียก `Image.load()` ตรวจสอบให้เส้นทางเป็นแบบเต็มหรือสัมพันธ์กับไดเรกทอรีทำงานของคุณ

### วิธีกำหนดค่า BMP Options เพื่อผลลัพธ์คุณภาพสูง?

`BmpOptions` เป็นคลาสที่บรรจุตั้งค่าสำหรับการส่งออก BMP เช่น bits per pixel และการบีบอัด สร้างอินสแตนซ์ `BmpOptions` แล้วตั้งค่า `BitsPerPixel` เป็น **32** สำหรับไฟล์ BMP true‑color ซึ่งรับประกันการถ่ายทอดสีที่ไม่มีการสูญเสียและให้ช่อง alpha ทางเลือกสำหรับการประมวลผลต่อ

**ขั้นตอนที่ 1: สร้าง BmpOptions**  
```java
import com.aspose.imaging.imageoptions.BmpOptions;

BmpOptions exportOptions = new BmpOptions();
```

**ขั้นตอนที่ 2: ตั้งค่า Bits Per Pixel**  
```java
exportOptions.setBitsPerPixel(32);
```  
การตั้งค่า 32 bpp ยังฝังช่อง alpha ซึ่งบางโปรแกรมดู BMP อาจละเลยแต่มีประโยชน์สำหรับการประมวลผลต่อ

### วิธีกำหนดช่วงหน้าสำหรับการส่งออก?

`IntRange` เป็นคลาสยูทิลิตี้ที่แทนช่วงจำนวนเต็มแบบรวม ใช้บ่อยเพื่อระบุช่วงหน้าหากเอกสาร DjVu ของคุณมีหลายหน้า คุณสามารถจำกัดการแปลงให้เฉพาะส่วนที่ต้องการโดยใช้ `IntRange` ตัวอย่างเช่น `new IntRange(1, 5)` จะส่งออกหน้าที่ 1‑5 ช่วยให้คุณโฟกัสส่วนสำคัญและประหยัดหน่วยความจำ

**ขั้นตอนที่ 1: สร้างอินสแตนซ์ IntRange**  
```java
import com.aspose.imaging.IntRange;

IntRange range = new IntRange(0, 2); // Export first two pages
```  
อ็อบเจ็กต์ `IntRange` กำหนดดัชนีเริ่มต้นและสิ้นสุดแบบรวม

### วิธีบันทึกหน้าของ DjVu เป็นภาพ BMP?

`Image.save` เป็นเมธอดอินสแตนซ์ที่เขียนข้อมูลภาพลงไฟล์โดยใช้ตัวเลือกที่ให้ไว้ วนลูปผ่านหน้าที่เลือก, ใช้ `BmpOptions`, และเรียก `image.save()` สำหรับแต่ละหน้า ไฟล์ผลลัพธ์จะตั้งชื่อเป็นลำดับเพื่อให้ง่ายต่อการระบุ, ทำให้มีการแมปที่ชัดเจนระหว่างหน้าต้นฉบับและไฟล์ BMP ที่สร้าง

**ขั้นตอนที่ 1: โหลดภาพและตั้งค่าตัวเลือกการส่งออก**  
```java
try (DjvuImage image = (DjvuImage) Image.load(dataDir + "Sample.djvu")) {
    BmpOptions exportOptions = new BmpOptions();
    exportOptions.setBitsPerPixel(32);
    IntRange range = new IntRange(0, 2); // Define the pages to be exported
```

**ขั้นตอนที่ 2: ส่งออกหน้า**  
```java
for (int i : range.getArray()) {
    exportOptions.setMultiPageOptions(new DjvuMultiPageOptions(range.getArrayOneItemFromIndex(i)));
    String output = "YOUR_OUTPUT_DIRECTORY" + "/ConvertDjvuPagesToImages_out" + i + ".bmp";
    image.save(output, exportOptions);
}
} catch (Exception e) {
    e.printStackTrace();
}
```  
แต่ละรอบจะเขียนไฟล์ BMP ไปยังโฟลเดอร์เป้าหมายโดยใช้ดัชนีหน้าเป็นส่วนหนึ่งของชื่อไฟล์

## ปัญหาและวิธีแก้ไขทั่วไป

- **OutOfMemoryError** – ใช้ try‑with‑resources เพื่อปิดอ็อบเจ็กต์ `Image` อัตโนมัติและประมวลผลหน้าแบบทีละหน้า  
- **Incorrect Colors** – ตรวจสอบให้ `BitsPerPixel` ตั้งเป็น 32; ค่าต่ำกว่าจะทำให้เกิดการลดสีของพาเลตต์  
- **Missing Pages** – ตรวจสอบให้ดัชนี `IntRange` อยู่ในช่วงจำนวนหน้าของเอกสาร (`image.getPages().size()`)

## คำถามที่พบบ่อย

**Q: Aspose.Imaging สำหรับ Java ใช้ทำอะไร?**  
A: เป็นไลบรารีสำหรับประมวลผล, แปลง, และวิเคราะห์ภาพในรูปแบบกว่า 100+, รวมถึง DjVu และ BMP

**Q: จะจัดการกับเอกสาร DjVu ขนาดใหญ่ระหว่างการแปลงอย่างไร?**  
A: ใช้ `IntRange` เพื่อส่งออกเฉพาะหน้าที่ต้องการและประมวลผลแต่ละหน้าในบล็อก try‑with‑resources แยกกันเพื่อรักษาการใช้หน่วยความจำให้ต่ำ

**Q: สามารถปรับคุณภาพ BMP ได้หรือไม่?**  
A: ได้ – ปรับ `BmpOptions.setBitsPerPixel()` (เช่น 24 สำหรับสี 16‑ล้าน, 32 สำหรับ true‑color พร้อม alpha)

**Q: จะทำอย่างไรหากการแปลงทำให้เกิดข้อยกเว้น?**  
A: ตรวจสอบเส้นทางไฟล์, ยืนยันว่าโหลดใบอนุญาตแล้ว, และตรวจสอบว่าไฟล์ DjVu ไม่เสียหาย ตรวจสอบ stack trace เพื่อหาสาเหตุที่แน่ชัด

**Q: จะหา ตัวอย่าง Aspose.Imaging เพิ่มเติมได้จากที่ไหน?**  
A: ตัวอย่างโค้ดและอ้างอิง API มีอยู่ใน [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)

## แหล่งข้อมูล

- **เอกสาร**: [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)  
- **เอกสาร**: [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)  
- **เอกสาร**: [Aspose.Imaging for Java Reference](https://reference.aspose.com/imaging/java/)  
- **ดาวน์โหลด**: [Latest Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/)  
- **ซื้อ**: [Aspose.Imaging Purchase](https://purchase.aspose.com/buy)  
- **ซื้อ**: [Buy a License](https://purchase.aspose.com/buy)  
- **ทดลองใช้ฟรี**: [Try Aspose.Imaging](https://releases.aspose.com/imaging/java/)  
- **ใบอนุญาตชั่วคราว**: [Request Here](https://purchase.aspose.com/temporary-license/)  
- **ฟอรั่มสนับสนุน**: [Aspose.Imaging Forum](https://forum.aspose.com/c/imaging/14)

---

**อัปเดตล่าสุด:** 2026-06-18  
**ทดสอบกับ:** Aspose.Imaging 23.12 for Java  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [แปลง DjVu เป็น Grayscale PNG ด้วย Aspose.Imaging สำหรับ Java | บทแนะนำการแปลงรูปแบบ](/imaging/java/format-conversion-export/export-djvu-grayscale-png-aspose-java/)
- [แปลง DjVu เป็น TIFF ใน Java ด้วย Aspose.Imaging: คู่มือขั้นตอน](/imaging/java/format-conversion-export/load-export-djvu-tiff-aspose-imaging-java/)
- [Aspose.Imaging Java: กำหนดค่า BMP Options เพื่อการประมวลผลภาพที่เหมาะสม](/imaging/java/format-specific-operations/aspose-imaging-java-set-bmp-options/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}