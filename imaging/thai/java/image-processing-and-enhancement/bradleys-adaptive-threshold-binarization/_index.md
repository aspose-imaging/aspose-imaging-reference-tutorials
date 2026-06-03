---
date: 2026-01-09
description: เรียนรู้วิธีทำให้ภาพเป็นแบบไบนารีโดยใช้ Aspose.Imaging สำหรับ Java คู่มือนี้ครอบคลุมเทคนิคการประมวลผลภาพด้วย
  Java สำหรับการแปลง DICOM เป็น BMP
linktitle: Bradley's Adaptive Threshold Binarization
second_title: Aspose.Imaging Java Image Processing API
title: วิธีทำให้ภาพเป็นสีขาวดำด้วย Aspose.Imaging สำหรับ Java
url: /th/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# วิธีทำให้ภาพเป็นแบบไบนารีด้วย Aspose.Imaging สำหรับ Java

ภาพมีบทบาทสำคัญในโลกดิจิทัล ไม่ว่าจะบนเว็บไซต์ เอกสาร หรือเป็นส่วนหนึ่งของแอปพลิเคชันต่าง ๆ หากคุณกำลังสงสัย **วิธีทำให้ภาพเป็นไบนารี** อย่างมีประสิทธิภาพ โดยเฉพาะสำหรับรูปแบบทางการแพทย์เช่น DICOM คุณมาถูกที่แล้ว การทำไบนารีของภาพจะทำให้ภาพง่ายขึ้นโดยแปลงเป็นสีขาว‑ดำ ซึ่งเหมาะสำหรับการวิเคราะห์ต่อไป OCR หรือการเพิ่มประสิทธิภาพการจัดเก็บ ในบทแนะนำนี้เราจะเดินผ่านกระบวนการทั้งหมดโดยใช้ Bradley’s Adaptive Threshold Binarization ของ Aspose.Imaging สำหรับ Java

## คำตอบสั้น ๆ
- **การทำไบนารีทำอะไร?** จะเปลี่ยนพิกเซลแต่ละจุดให้เป็นสีดำหรือสีขาวตามค่าเกณฑ์
- **ไลบรารีใดดีที่สุดสำหรับการประมวลผลภาพใน Java?** Aspose.Imaging สำหรับ Java มีคุณสมบัติทดลองฟรีที่แข็งแรง
- **ฉันสามารถประมวลผลไฟล์ DICOM โดยตรงได้หรือไม่?** ได้, Aspose.Imaging สามารถโหลด DICOM และส่งออกเป็น BMP, PNG ฯลฯ
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานจริงหรือไม่?** จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานที่ไม่ใช่รุ่นทดลอง
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 และใหม่กว่าเข้ากันได้เต็มที่

## ไบนารีของภาพคืออะไร?
การไบนารีของภาพคือกระบวนการแปลงภาพระดับสีเทาหรือสีเต็มเป็นภาพไบนารีที่พิกเซลแต่ละจุดเป็น 0 (สีดำ) หรือ 255 (สีขาว) ขั้นตอนนี้มักเป็นขั้นตอนแรกในสายการประมวลผลภาพทางการแพทย์ การสแกนเอกสาร และงานคอมพิวเตอร์วิทัศน์

## ทำไมต้องใช้ Aspose.Imaging สำหรับ Java?
Aspose.Imaging มี API แบบ pure‑Java ที่ **โหลด DICOM** ใช้อัลกอริธึมขั้นสูงเช่น **Bradley’s Adaptive Threshold** และบันทึกผลลัพธ์ในรูปแบบทั่วไปโดยไม่ต้องพึ่งไลบรารีเนทีฟภายนอก เหมาะสำหรับ **การประมวลผลภาพทางการแพทย์**, **แปลง DICOM เป็น BMP**, และเวิร์กโฟลว์อื่น ๆ ที่ใช้ Java

## ข้อกำหนดเบื้องต้น

ก่อนจะลงลึกในโค้ด โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมแล้ว:

- **สภาพแวดล้อมการพัฒนา Java** – ติดตั้ง JDK 8 หรือใหม่กว่า
- **Aspose.Imaging สำหรับ Java** – ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ: [Download Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/)
- **ภาพ DICOM** – ไฟล์ DICOM ตัวอย่างใด ๆ ที่คุณต้องการทำไบนารี

เมื่อทุกอย่างพร้อมแล้ว ไปสู่การทำงานกันต่อ

## วิธีทำให้ภาพเป็นไบนารี – คำแนะนำแบบขั้นตอน

### นำเข้าแพ็กเกจ
แรกสุดให้นำเข้าคลาสของ Aspose.Imaging ที่จำเป็น ส่วนนี้ยังกำหนดเส้นทางไฟล์เข้าและออกด้วย

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// Load a DICOM image in an instance of DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Binarize image with Bradley's adaptive threshold.
    image.binarizeBradley(10);
    // Save the resultant image.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

### ขั้นตอนที่ 1: กำหนดเส้นทาง
ตั้งค่าตำแหน่งไฟล์ DICOM ต้นฉบับและไฟล์ BMP ปลายทาง แทนที่ `"Your Document Directory"` ด้วยโฟลเดอร์จริงบนระบบของคุณ

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

### ขั้นตอนที่ 2: โหลดภาพ DICOM
ใช้ Aspose.Imaging เพื่อ **โหลดภาพ dicom** เข้าอ็อบเจ็กต์ `DicomImage` ซึ่งให้การเข้าถึงข้อมูลพิกเซลและเมธอดการประมวลผลทั้งหมด

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // The image processing steps will go here.
}
```

### ขั้นตอนที่ 3: ทำการไบนารี
เรียกใช้ Bradley’s Adaptive Threshold algorithm พารามิเตอร์ (`10` ในตัวอย่าง) ควบคุมความไวของเกณฑ์; คุณสามารถทดลองค่าต่าง ๆ เพื่อให้ได้ผลลัพธ์ที่ดีที่สุด

```java
image.binarizeBradley(10);
```

### ขั้นตอนที่ 4: บันทึกภาพที่ทำไบนารีแล้ว
สุดท้ายให้ส่งออกภาพที่ประมวลผลแล้ว ที่นี่เราใช้รูปแบบ BMP แต่ Aspose.Imaging รองรับ PNG, JPEG, TIFF และอื่น ๆ อีกมาก

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## ปัญหาที่พบบ่อยและการแก้ไข

- **FileNotFoundException** – ตรวจสอบให้แน่ใจว่าเส้นทาง `dataDir` ลงท้ายด้วยเครื่องหมายทับและชื่อไฟล์ DICOM ตรงกันอย่างแม่นยำ
- **OutOfMemoryError** – ไฟล์ DICOM ขนาดใหญ่อาจต้องเพิ่มขนาด heap ของ JVM (`-Xmx2g` หรือมากกว่า)
- **Threshold ไม่เหมาะสม** – หากผลลัพธ์ดูมืดหรือสว่างเกินไป ปรับค่าจำนวนเต็มที่ส่งให้ `binarizeBradley()` (เช่น 5‑15)

## คำถามที่พบบ่อย

### Q1: DICOM คืออะไรและทำไมจึงสำคัญในภาพทางการแพทย์?
**A:** DICOM ย่อมาจาก Digital Imaging and Communications in Medicine เป็นมาตรฐานสากลสำหรับการจัดเก็บ ส่งต่อ และจัดการภาพทางการแพทย์ ทำให้ระบบและอุปกรณ์ต่าง ๆ สามารถทำงานร่วมกันได้

### Q2: ฉันสามารถใช้ Aspose.Imaging สำหรับ Java ในโครงการเชิงพาณิชย์ได้หรือไม่?
**A:** ได้, Aspose.Imaging สำหรับ Java มีทั้งรุ่นทดลองฟรีและลิขสิทธิ์เชิงพาณิชย์ คุณสามารถสำรวจตัวเลือกและรับลิขสิทธิ์ที่จำเป็นจาก [Aspose's website](https://purchase.aspose.com/buy)

### Q3: มีลิขสิทธิ์ชั่วคราวสำหรับการทดสอบหรือไม่?
**A:** มี, คุณสามารถขอรับลิขสิทธิ์ชั่วคราวเพื่อทดสอบและประเมิน Aspose.Imaging สำหรับ Java ได้ที่ [this link](https://purchase.aspose.com/temporary-license/)

### Q4: ฉันจะหาความช่วยเหลือหรือพูดคุยเกี่ยวกับปัญหา Aspose.Imaging สำหรับ Java ได้จากที่ไหน?
**A:** สำหรับการสนับสนุนชุมชนและการสนทนา คุณสามารถเยี่ยมชม [Aspose.Imaging forum](https://forum.aspose.com/) ซึ่งเป็นแหล่งที่ดีในการค้นหาคำตอบและเชื่อมต่อกับผู้ใช้คนอื่น ๆ

### Q5: Aspose.Imaging สำหรับ Java เหมาะกับการประมวลผลภาพในแอปพลิเคชัน Java‑อื่น ๆ หรือไม่?
**A:** แน่นอน, ไลบรารีนี้ทำงานได้ดีในเว็บแอปพลิเคชัน, ซอฟต์แวร์เดสก์ท็อป, เครื่องมือประมวลผลแบบแบตช์, และอื่น ๆ อีกมาก โดยให้ API ที่สอดคล้องกันข้ามแพลตฟอร์ม

## สรุป
คุณได้เรียนรู้ **วิธีทำให้ภาพเป็นไบนารี** ด้วย Aspose.Imaging สำหรับ Java โดยใช้ Bradley’s Adaptive Threshold เทคนิคนี้มีคุณค่าอย่างยิ่งสำหรับ **การประมวลผลภาพทางการแพทย์**, ช่วยให้คุณแปลงไฟล์ DICOM เป็น BMP (หรือรูปแบบอื่น) ที่มีน้ำหนักเบาสำหรับการวิเคราะห์หรือจัดเก็บ ทดลองปรับค่า Threshold ต่าง ๆ และสำรวจคุณสมบัติเพิ่มเติมของ Aspose.Imaging ที่เต็มเปี่ยม

สำหรับการเรียนรู้เชิงลึกเกี่ยวกับการจัดการภาพ โปรดดูเอกสารอย่างเป็นทางการ: [Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/)

---

**อัปเดตล่าสุด:** 2026-01-09  
**ทดสอบด้วย:** Aspose.Imaging สำหรับ Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}