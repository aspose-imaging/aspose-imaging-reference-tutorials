---
title: การสร้างอิมเมจ WMF ด้วย Aspose.Imaging สำหรับ Java
linktitle: สร้างอิมเมจ WMF Metafile
second_title: Aspose.Imaging Java Image Processing API
description: เรียนรู้วิธีสร้างอิมเมจเมตาไฟล์ WMF ใน Java โดยใช้ Aspose.Imaging ปฏิบัติตามคำแนะนำทีละขั้นตอนนี้เพื่อความสามารถในการสร้างภาพอันทรงพลัง
weight: 10
url: /th/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การสร้างอิมเมจ WMF ด้วย Aspose.Imaging สำหรับ Java

คุณต้องการสร้างอิมเมจ WMF (Windows Metafile) ด้วยแอปพลิเคชัน Java ของคุณหรือไม่? Aspose.Imaging for Java เป็นเครื่องมืออันทรงพลังที่ช่วยให้คุณสามารถสร้างอิมเมจ WMF ได้อย่างง่ายดาย ในคำแนะนำทีละขั้นตอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการใช้ Aspose.Imaging สำหรับ Java เพื่อสร้างอิมเมจเมตาไฟล์ WMF 

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java ที่ตั้งค่าบนคอมพิวเตอร์ของคุณ
-  ติดตั้ง Aspose.Imaging สำหรับไลบรารี Java แล้ว คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์](https://releases.aspose.com/imaging/java/).
- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม Java

## แพ็คเกจนำเข้า

ขั้นแรก นำเข้าแพ็คเกจที่จำเป็นสำหรับแอปพลิเคชัน Java ของคุณเพื่อใช้ Aspose.Imaging สำหรับ Java:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.color.*;
import com.aspose.imaging.coreexceptions.ImageLoadException;
import com.aspose.imaging.imageoptions.WmfOptions;
import com.aspose.imaging.internal.system.drawing.*;
import com.aspose.imaging.internal.system.drawing.imaging.*;
import com.aspose.imaging.pen.*;
import com.aspose.imaging.system.drawing.*;
```

## ขั้นตอนที่ 1: สร้างแคนวาส

 ในการเริ่มสร้างภาพ WMF คุณต้องสร้างผืนผ้าใบที่คุณสามารถวาดรูปร่างได้ ที่`WmfRecorderGraphics2D` คลาสมอบผืนผ้าใบนี้ให้กับคุณ ต่อไปนี้คือวิธีที่คุณสามารถสร้างอินสแตนซ์ได้:

```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

ในโค้ดด้านบน เราระบุขนาดแคนวาส (100x100) และความละเอียด (96 DPI)

## ขั้นตอนที่ 2: ตั้งค่าสีพื้นหลัง

 จากนั้น กำหนดสีพื้นหลังสำหรับแคนวาสของคุณ คุณสามารถใช้`setBackgroundColor` วิธีการตั้งค่าสีพื้นหลัง:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

ในตัวอย่างนี้ เราตั้งค่าสีพื้นหลังเป็นควันสีขาว

## ขั้นตอนที่ 3: กำหนดปากกาและแปรง

หากต้องการวาดรูปทรงบนผืนผ้าใบ คุณต้องกำหนดปากกาและแปรง ปากกาใช้สำหรับวาดโครงร่าง และใช้แปรงสำหรับเติมรูปทรง ต่อไปนี้เป็นวิธีสร้างปากกาและแปรงทึบ:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

ในโค้ดนี้ เราสร้างปากกาสีน้ำเงินและแปรงทึบสีเหลืองเขียว

## ขั้นตอนที่ 4: เติมและวาดรูปร่าง

ตอนนี้ มาเติมและวาดรูปทรงพื้นฐานบนผืนผ้าใบกันดีกว่า เราจะเริ่มต้นด้วยรูปหลายเหลี่ยม:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

ที่นี่ เราเติมและวาดรูปหลายเหลี่ยมโดยใช้ปากกาและแปรงที่ระบุ คุณสามารถปรับพิกัดและรูปร่างได้ตามต้องการ

## ขั้นตอนที่ 5: ใช้ HatchBrush

 หากต้องการเพิ่มพื้นผิวให้กับรูปร่างของคุณ คุณสามารถใช้`HatchBrush`. ตัวอย่างเช่น:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

ในโค้ดนี้ เราสร้างแปรงแบบ cross-hatch ที่มีสีขาวและสีเงิน

## ขั้นตอนที่ 6: เติมและวาดวงรี

มาเติมและวาดวงรีบนผืนผ้าใบกัน:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

คุณสามารถปรับตำแหน่งและขนาดของวงรีได้ตามต้องการ

## ขั้นตอนที่ 7: วาดส่วนโค้งและลูกบาศก์ Bezier

การวาดรูปทรงที่ซับซ้อนยิ่งขึ้นก็สามารถทำได้เช่นกัน ต่อไปนี้เป็นวิธีวาดส่วนโค้งและเส้นโค้ง Bezier ลูกบาศก์:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

ในโค้ดด้านบน อันดับแรกเราวาดส่วนโค้งด้วยเส้นประ จากนั้นจึงวาดเส้นโค้ง Bezier ลูกบาศก์ด้วยปากกาสีแดงทึบ

## ขั้นตอนที่ 8: เพิ่มรูปภาพ

คุณยังสามารถเพิ่มรูปภาพลงในไฟล์เมตา WMF ของคุณได้ ต่อไปนี้เป็นวิธีดำเนินการ:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

ในขั้นตอนนี้ เราจะโหลดรูปภาพและวางไว้บนผืนผ้าใบตามพิกัดที่ระบุ (50, 50)

## ขั้นตอนที่ 9: วาดเส้นและพาย

หากต้องการเพิ่มเส้นและรูปร่างวงกลม คุณสามารถทำตามตัวอย่างเหล่านี้:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

ที่นี่ เราวาดเส้นและเติม/วาดรูปร่างพายโดยใช้ปากกาและแปรงที่ระบุ

## ขั้นตอนที่ 10: วาดเส้นหลายเส้นและข้อความ

การเพิ่มข้อความและเส้นหลายบรรทัดนั้นตรงไปตรงมา:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

คุณสามารถปรับแต่งแบบอักษร ข้อความ และจุดโพลีไลน์ได้ตามต้องการ

## ขั้นตอนที่ 11: บันทึกอิมเมจ WMF

เมื่อคุณสร้างอิมเมจ WMF แล้ว ก็ถึงเวลาบันทึก:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

รหัสนี้จะบันทึกอิมเมจ WMF ไปยังไดเร็กทอรีที่ระบุ

แค่นั้นแหละ! คุณสร้างอิมเมจไฟล์เมตา WMF โดยใช้ Aspose.Imaging สำหรับ Java สำเร็จแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจวิธีสร้างอิมเมจเมตาไฟล์ WMF โดยใช้ Aspose.Imaging สำหรับ Java เราครอบคลุมข้อกำหนดเบื้องต้นที่จำเป็น แพ็คเกจที่นำเข้า และให้คำแนะนำทีละขั้นตอนสำหรับการวาดรูปทรงต่างๆ การเพิ่มพื้นผิว การแทรกรูปภาพ และการบันทึกภาพสุดท้าย Aspose.Imaging for Java นำเสนอชุดเครื่องมืออันทรงพลังสำหรับการจัดการและการสร้างรูปภาพ ทำให้เป็นทรัพยากรอันมีค่าสำหรับแอปพลิเคชัน Java ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: รูปแบบภาพ WMF คืออะไร

A1: WMF ย่อมาจาก Windows Metafile ซึ่งเป็นรูปแบบกราฟิกแบบเวกเตอร์ที่ใช้สำหรับจัดเก็บรูปภาพ ภาพวาด และข้อมูลกราฟิกอื่นๆ โดยทั่วไปจะใช้ในแอปพลิเคชัน Windows และสามารถปรับขนาดได้อย่างง่ายดายโดยไม่สูญเสียคุณภาพ

### คำถามที่ 2: ฉันจะดาวน์โหลด Aspose.Imaging สำหรับ Java ได้ที่ไหน

 A2: คุณสามารถดาวน์โหลด Aspose.Imaging สำหรับ Java ได้จากไฟล์[เว็บไซต์](https://releases.aspose.com/imaging/java/).

### คำถามที่ 3: ฉันจำเป็นต้องมีทักษะการเขียนโปรแกรมขั้นสูงเพื่อใช้ Aspose.Imaging สำหรับ Java หรือไม่

ตอบ 3: แม้ว่าจะต้องมีความรู้พื้นฐานด้านการเขียนโปรแกรม Java แต่ Aspose.Imaging for Java ก็มี API ที่ใช้งานง่าย ซึ่งช่วยลดความยุ่งยากในการจัดการและสร้างภาพ

### คำถามที่ 4: ฉันสามารถใช้ Aspose.Imaging สำหรับ Java เพื่อวัตถุประสงค์ทางการค้าได้หรือไม่

 ตอบ 4: ใช่ Aspose.Imaging for Java มอบใบอนุญาตเชิงพาณิชย์สำหรับธุรกิจและนักพัฒนา คุณสามารถซื้อใบอนุญาตได้จาก[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 5: ฉันจะรับการสนับสนุนหรือถามคำถามเกี่ยวกับ Aspose.Imaging สำหรับ Java ได้ที่ไหน

 A5: คุณสามารถค้นหาการสนับสนุนและมีส่วนร่วมกับชุมชน Aspose ได้ที่[Aspose ฟอรั่มการถ่ายภาพ](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
