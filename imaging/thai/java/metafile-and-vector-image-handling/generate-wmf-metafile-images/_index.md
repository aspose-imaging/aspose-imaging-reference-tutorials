---
"description": "เรียนรู้วิธีสร้างภาพเมตาไฟล์ WMF ใน Java โดยใช้ Aspose.Imaging ปฏิบัติตามคำแนะนำทีละขั้นตอนนี้เพื่อความสามารถในการสร้างภาพที่มีประสิทธิภาพ"
"linktitle": "สร้างภาพ WMF Metafile"
"second_title": "API การประมวลผลภาพ Java ของ Aspose.Imaging"
"title": "การสร้างภาพ WMF ด้วย Aspose.Imaging สำหรับ Java"
"url": "/th/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/"
"weight": 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# การสร้างภาพ WMF ด้วย Aspose.Imaging สำหรับ Java

คุณกำลังมองหาวิธีสร้างภาพ WMF (Windows Metafile) ด้วยแอปพลิเคชัน Java อยู่หรือไม่ Aspose.Imaging for Java เป็นเครื่องมืออันทรงพลังที่ช่วยให้คุณสร้างภาพ WMF ได้อย่างง่ายดาย ในคู่มือทีละขั้นตอนนี้ เราจะแนะนำคุณเกี่ยวกับขั้นตอนการใช้ Aspose.Imaging for Java เพื่อสร้างภาพเมตาไฟล์ WMF 

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น โปรดตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java ที่ถูกตั้งค่าบนคอมพิวเตอร์ของคุณ
- ติดตั้งไลบรารี Aspose.Imaging สำหรับ Java แล้ว คุณสามารถดาวน์โหลดได้จาก [เว็บไซต์](https://releases-aspose.com/imaging/java/).
- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรมภาษา Java

## แพ็คเกจนำเข้า

ขั้นแรก นำเข้าแพ็กเกจที่จำเป็นสำหรับแอปพลิเคชัน Java ของคุณเพื่อใช้ Aspose.Imaging สำหรับ Java:

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

## ขั้นตอนที่ 1: สร้างผืนผ้าใบ

ในการเริ่มสร้างภาพ WMF คุณต้องสร้างผืนผ้าใบที่คุณสามารถวาดรูปทรงได้ `WmfRecorderGraphics2D` คลาสนี้มอบผืนผ้าใบนี้ให้กับคุณ คุณสามารถสร้างอินสแตนซ์ของผืนผ้าใบนี้ได้ดังนี้:

```java
// เส้นทางไปยังไดเร็กทอรีเอกสาร
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

ในโค้ดด้านบน เราได้ระบุขนาดผ้าใบ (100x100) และความละเอียด (96 DPI)

## ขั้นตอนที่ 2: ตั้งค่าสีพื้นหลัง

ขั้นตอนต่อไป กำหนดสีพื้นหลังให้กับผืนผ้าใบของคุณ คุณสามารถใช้ `setBackgroundColor` วิธีการตั้งค่าสีพื้นหลัง:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

ในตัวอย่างนี้ เราตั้งค่าสีพื้นหลังเป็นควันสีขาว

## ขั้นตอนที่ 3: กำหนดปากกาและแปรง

ในการวาดรูปทรงบนผืนผ้าใบ คุณต้องกำหนดปากกาและพู่กัน ปากกาใช้สำหรับวาดโครงร่าง และพู่กันใช้สำหรับเติมรูปทรง ต่อไปนี้คือวิธีสร้างปากกาและพู่กันทึบ:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

ในโค้ดนี้ เราสร้างปากกาสีน้ำเงินและแปรงทึบสีเหลืองเขียว

## ขั้นตอนที่ 4: เติมและวาดรูปทรง

ตอนนี้เรามาเติมและวาดรูปทรงพื้นฐานบนผืนผ้าใบกัน เราจะเริ่มต้นด้วยรูปหลายเหลี่ยม:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

ที่นี่ เราจะเติมและวาดรูปหลายเหลี่ยมโดยใช้ปากกาและแปรงที่ระบุ คุณสามารถปรับพิกัดและรูปร่างตามต้องการได้

## ขั้นตอนที่ 5: ใช้ HatchBrush

หากต้องการเพิ่มพื้นผิวให้กับรูปร่างของคุณ คุณสามารถใช้ `HatchBrush`. ตัวอย่างเช่น:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

ในโค้ดนี้ เราสร้างแปรงเส้นไขว้ด้วยสีขาวและสีเงิน

## ขั้นตอนที่ 6: เติมและวาดวงรี

มาเติมและวาดรูปวงรีบนผืนผ้าใบกัน:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

คุณสามารถปรับตำแหน่งและขนาดของวงรีได้ตามต้องการ

## ขั้นตอนที่ 7: วาดส่วนโค้งและลูกบาศก์เบเซียร์

การวาดรูปทรงที่ซับซ้อนยิ่งขึ้นก็ทำได้เช่นเดียวกัน ต่อไปนี้คือวิธีการวาดส่วนโค้งและเส้นโค้งเบซิเยร์ลูกบาศก์:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

ในโค้ดด้านบน ขั้นแรก เราจะวาดส่วนโค้งด้วยเส้นประ จากนั้นจึงวาดเส้นโค้งเบซิเยร์ลูกบาศก์ด้วยปากกาสีแดงทึบ

## ขั้นตอนที่ 8: เพิ่มรูปภาพ

คุณสามารถเพิ่มรูปภาพลงในเมตาไฟล์ WMF ได้เช่นกัน โดยทำได้ดังนี้:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

ในขั้นตอนนี้ เราจะโหลดรูปภาพและวางบนผืนผ้าใบตามพิกัดที่ระบุ (50, 50)

## ขั้นตอนที่ 9: วาดเส้นและวงกลม

หากต้องการเพิ่มเส้นและรูปร่างวงกลม คุณสามารถทำตามตัวอย่างเหล่านี้:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

ที่นี่ เราวาดเส้นและเติม/วาดรูปวงกลมโดยใช้ปากกาและแปรงที่ระบุ

## ขั้นตอนที่ 10: วาดเส้นโพลีไลน์และข้อความ

การเพิ่มข้อความและเส้นโพลีไลน์นั้นเป็นเรื่องง่าย:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

คุณสามารถปรับแต่งแบบอักษร ข้อความ และจุดโพลีไลน์ตามต้องการได้

## ขั้นตอนที่ 11: บันทึกภาพ WMF

เมื่อคุณสร้างภาพ WMF เสร็จแล้ว ก็ถึงเวลาบันทึกมัน:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

โค้ดนี้จะบันทึกภาพ WMF ไปยังไดเร็กทอรีที่ระบุ

เสร็จเรียบร้อย! คุณได้สร้างภาพเมตาไฟล์ WMF โดยใช้ Aspose.Imaging สำหรับ Java สำเร็จแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้ศึกษาวิธีการสร้างภาพเมตาไฟล์ WMF โดยใช้ Aspose.Imaging สำหรับ Java เราได้ครอบคลุมข้อกำหนดเบื้องต้นที่จำเป็น แพ็คเกจที่นำเข้า และให้คำแนะนำแบบทีละขั้นตอนสำหรับการวาดรูปทรงต่างๆ การเพิ่มพื้นผิว การแทรกภาพ และการบันทึกภาพสุดท้าย Aspose.Imaging สำหรับ Java นำเสนอชุดเครื่องมืออันทรงพลังสำหรับการจัดการและสร้างภาพ ทำให้เป็นทรัพยากรที่มีค่าสำหรับแอปพลิเคชัน Java ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: รูปแบบภาพ WMF คืออะไร

A1: WMF ย่อมาจาก Windows Metafile ซึ่งเป็นรูปแบบกราฟิกแบบเวกเตอร์ที่ใช้สำหรับจัดเก็บรูปภาพ ภาพวาด และข้อมูลกราฟิกอื่นๆ โดยทั่วไปแล้วจะใช้ WMF ในแอปพลิเคชัน Windows และสามารถปรับขนาดได้อย่างง่ายดายโดยไม่สูญเสียคุณภาพ

### คำถามที่ 2: ฉันสามารถดาวน์โหลด Aspose.Imaging สำหรับ Java ได้ที่ไหน

A2: คุณสามารถดาวน์โหลด Aspose.Imaging สำหรับ Java ได้จาก [เว็บไซต์](https://releases-aspose.com/imaging/java/).

### คำถามที่ 3: ฉันจำเป็นต้องมีทักษะการเขียนโปรแกรมขั้นสูงเพื่อใช้ Aspose.Imaging สำหรับ Java หรือไม่

A3: แม้ว่าจะต้องมีความรู้พื้นฐานด้านการเขียนโปรแกรม Java แต่ Aspose.Imaging สำหรับ Java นั้นมี API ที่ใช้งานง่ายซึ่งทำให้การจัดการและสร้างภาพนั้นง่ายขึ้น

### คำถามที่ 4: ฉันสามารถใช้ Aspose.Imaging สำหรับ Java เพื่อวัตถุประสงค์เชิงพาณิชย์ได้หรือไม่

A4: ใช่ Aspose.Imaging สำหรับ Java นำเสนอใบอนุญาตเชิงพาณิชย์สำหรับธุรกิจและนักพัฒนา คุณสามารถซื้อใบอนุญาตได้จาก [ที่นี่](https://purchase-aspose.com/buy).

### คำถามที่ 5: ฉันจะได้รับการสนับสนุนหรือถามคำถามเกี่ยวกับ Aspose.Imaging สำหรับ Java ได้จากที่ไหน

A5: คุณสามารถค้นหาการสนับสนุนและมีส่วนร่วมกับชุมชน Aspose ได้ที่ [ฟอรั่ม Aspose.Imaging](https://forum-aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}