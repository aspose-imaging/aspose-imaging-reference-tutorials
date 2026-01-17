---
date: 2026-01-17
description: เรียนรู้วิธีใช้ Median Filter ใน Java กับ Aspose.Imaging เพื่อลบสัญญาณรบกวนในภาพ
  การสอนแบบขั้นตอนนี้ครอบคลุมการใช้ฟิลเตอร์ Median และ Wiener สำหรับการลดสัญญาณรบกวนของภาพ
linktitle: Median Filter Java – Apply Median and Wiener Filters
second_title: Aspose.Imaging Java Image Processing API
title: ฟิลเตอร์มัธยฐาน Java – ใช้ฟิลเตอร์มัธยฐานและวินเนอร์
url: /th/java/image-processing-and-enhancement/median-and-wiener-filter-application/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Median Filter Java – ใช้ Median และ Wiener Filters

ในโลกของการประมวลผลภาพ การกำจัดสัญญาณรบกวนและการปรับปรุงคุณภาพภาพเป็นงานที่สำคัญ ด้วย **median filter java** คุณสามารถทำความสะอาดภาพที่มีสัญญาณรบกวนได้อย่างมีประสิทธิภาพโดยใช้ Aspose.Imaging for Java ในบทแนะนำนี้ เราจะพาคุณผ่านขั้นตอนการใช้ Median และ Wiener filters เพื่อลดสัญญาณรบกวนของภาพ เพื่อให้คุณได้ผลลัพธ์ระดับมืออาชีพโดยไม่ต้องเขียนโค้ดซับซ้อน

## คำตอบอย่างรวดเร็ว
- **Median filter ทำอะไร?** มันจะแทนที่พิกเซลแต่ละจุดด้วยค่ามีเดียนของเพื่อนบ้านรอบข้าง, เพื่อลบสัญญาณรบกวนแบบ impulse ในขณะที่ยังคงรักษาขอบภาพไว้  
- **ไลบรารีใดสนับสนุน median filter java?** Aspose.Imaging for Java มีคลาส `MedianFilterOptions` ที่พร้อมใช้งาน  
- **ฉันต้องมีลิขสิทธิ์เพื่อรันโค้ดหรือไม่?** รุ่นทดลองฟรีใช้ได้สำหรับการประเมิน; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **ฉันสามารถต่อเชื่อม median filter กับฟิลเตอร์อื่นได้หรือไม่?** ใช่, คุณสามารถใช้ฟิลเตอร์เพิ่มเติมเช่น Wiener หลังจากขั้นตอน median  
- **ฟอร์แมตภาพใดที่รองรับ?** ฟอร์แมตแรสเตอร์ส่วนใหญ่ (PNG, JPEG, BMP, TIFF ฯลฯ) ได้รับการสนับสนุนเต็มที่  

## Median Filter Java คืออะไร?
Median filter เป็นเทคนิคการกรองดิจิทัลแบบไม่เชิงเส้นที่มักใช้เพื่อ **remove image noise**. ใน Java, Aspose.Imaging ใช้ฟิลเตอร์นี้ผ่านคลาส `MedianFilterOptions` ซึ่งให้คุณกำหนดขนาดเคอร์เนลที่ระบุจำนวนพิกเซลเพื่อนบ้านที่พิจารณา

## ทำไมต้องใช้ Median Filter Java สำหรับการลดสัญญาณรบกวนภาพ?
- **Preserves edges** ดีกว่าฟิลเตอร์เฉลี่ยแบบง่าย  
- **Simple API** – เพียงไม่กี่บรรทัดของโค้ดก็สามารถลบ speckle และ salt‑and‑pepper noise  
- **Works on any raster image** ที่โหลดด้วย Aspose.Imaging ทำให้เหมาะสำหรับการประมวลผลฝั่งเซิร์ฟเวอร์  

## ข้อกำหนดเบื้องต้น
ก่อนเริ่มทำงาน, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:
1. **Java Development Environment** – ติดตั้ง JDK 8 หรือใหม่กว่า  
2. **Aspose.Imaging for Java** – ดาวน์โหลดและติดตั้งไลบรารีจาก [here](https://releases.aspose.com/imaging/java/).  
3. **Sample Noisy Image** – ภาพใดก็ได้ที่คุณต้องการทำความสะอาด; สำหรับคู่มือนี้เราจะใช้ `your‑noisy‑image.png`.  

## นำเข้าแพ็กเกจ
ในโปรเจกต์ Java ของคุณ, เริ่มต้นด้วยการนำเข้าคลาส Aspose.Imaging ที่จำเป็น:
```java
import com.aspose.imaging.Image;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.imagefilters.filteroptions.MedianFilterOptions;
```

## วิธีใช้ Median Filter Java
ด้านล่างเป็นขั้นตอนแบบทีละขั้นตอน. แต่ละขั้นตอนมีคำอธิบายสั้น ๆ ตามด้วยโค้ดที่ต้องคัดลอกโดยตรง

### ขั้นตอนที่ 1: โหลดภาพที่มีสัญญาณรบกวน
แรกสุด, โหลดภาพที่คุณต้องการลดสัญญาณรบกวน. นี้เป็นการสาธิต **load image java** ด้วยเมธอด `Image.load` ของ Aspose.Imaging.
```java
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (Image image = Image.load(dataDir + "your-noisy-image.png"))
{
    // Cast the image into RasterImage
    RasterImage rasterImage = (RasterImage) image;
```

### ขั้นตอนที่ 2: สร้างและกำหนดค่า Median Filter
สร้างอินสแตนซ์ของ `MedianFilterOptions` และตั้งค่าขนาดเคอร์เนล. ขนาดที่ใหญ่ขึ้นจะลบสัญญาณรบกวนได้มากขึ้นแต่อาจทำให้รายละเอียดเบลอ
```java
    // Create an instance of MedianFilterOptions class and set the size.
    MedianFilterOptions options = new MedianFilterOptions(4);
```

### ขั้นตอนที่ 3: ใช้ Median Filter
ใช้ฟิลเตอร์กับขอบเขตของภาพทั้งหมด. นี่คือการทำงานหลักของ **apply median filter**
```java
    // Apply Median filter to RasterImage object.
    rasterImage.filter(image.getBounds(), options);
```

### ขั้นตอนที่ 4: บันทึกภาพผลลัพธ์
สุดท้าย, เขียนภาพที่ลดสัญญาณรบกวนลงดิสก์. ตอนนี้คุณสามารถเห็นผลของ median filter ได้แล้ว
```java
    // Save the resultant image
    image.save("Your Document Directory" + "denoised-image.png");
}
```

## ปัญหาทั่วไปและวิธีแก้
- **Kernel size too large** – ภาพอาจดูเบลอเกินไป. ลองใช้ค่าระหว่าง 3‑5 สำหรับภาพส่วนใหญ่  
- **Unsupported image format** – ตรวจสอบว่าไฟล์เป็นฟอร์แมตแรสเตอร์ที่ Aspose.Imaging รองรับ  
- **OutOfMemoryError** – ประมวลผลภาพขนาดใหญ่เป็นส่วนย่อย ๆ ด้วยเมธอด `crop` ของ `RasterImage` ก่อนทำการฟิลเตอร์  

## สรุป
ในคู่มือนี้เราได้สาธิต **how to denoise image** ด้วยวิธี **median filter java** ที่ให้โดย Aspose.Imaging. ด้วยการทำตามขั้นตอนข้างต้น, คุณสามารถรวมการกำจัดสัญญาณรบกวนเข้าไปใน pipeline การประมวลผลภาพที่ใช้ Java ได้อย่างรวดเร็ว, และยังสามารถปรับปรุงผลลัพธ์เพิ่มเติมโดยการต่อเชื่อม Wiener filter หรือเทคนิคขั้นสูงอื่น ๆ  

## คำถามที่พบบ่อย

**Q1: Aspose.Imaging for Java คืออะไร?**  
A1: Aspose.Imaging for Java เป็นไลบรารี Java ที่ช่วยให้นักพัฒนาสามารถทำงานกับภาพและทำงานประมวลผลภาพต่าง ๆ อย่างโปรแกรมเมติก  

**Q2: ฉันสามารถใช้ Aspose.Imaging for Java ได้ฟรีหรือไม่?**  
A2: Aspose.Imaging for Java เป็นไลบรารีเชิงพาณิชย์, แต่คุณสามารถรับรุ่นทดลองฟรีจาก [here](https://releases.aspose.com/). อย่างไรก็ตามสำหรับการใช้งานต่อเนื่อง, คุณจะต้องซื้อไลเซนส์จาก [here](https://purchase.aspose.com/buy).  

**Q3: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.Imaging for Java อย่างไร?**  
A3: คุณสามารถขอความช่วยเหลือจากชุมชนและผู้เชี่ยวชาญของ Aspose.Imaging ได้ที่ [Aspose.Imaging Forum](https://forum.aspose.com/).  

**Q4: มีเทคนิคการปรับปรุงภาพอื่น ๆ อะไรบ้าง?**  
A4: นอกจาก Median filter, เทคนิคการปรับปรุงภาพรวมถึง Wiener filtering, Gaussian blurring, และ contrast stretching เป็นต้น  

**Q5: ฉันสามารถใช้ Aspose.Imaging for Java ในเว็บแอปพลิเคชันของฉันได้หรือไม่?**  
A5: ใช่, คุณสามารถรวม Aspose.Imaging for Java เข้าไปในเว็บแอปพลิเคชันของคุณเพื่อการประมวลผลภาพฝั่งเซิร์ฟเวอร์ได้  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2026-01-17  
**ทดสอบด้วย:** Aspose.Imaging for Java 24.11  
**ผู้เขียน:** Aspose