---
date: '2026-02-09'
description: เรียนรู้วิธีแปลง JPEG เป็น TIFF และสร้างภาพ TIFF แบบหลายเฟรมโดยใช้ Aspose.Imaging
  สำหรับ .NET รวมถึงการตั้งค่า การกำหนดค่า TiffOptions การโหลดภาพจากไดเรกทอรี และการจัดการเฟรม
keywords:
- create multi-frame tiff images
- Aspose.Imaging for .NET tutorial
- configure TiffOptions in .NET
title: วิธีแปลง JPEG เป็น TIFF และสร้างภาพ TIFF แบบหลายเฟรมด้วย Aspose.Imaging สำหรับ
  .NET
url: /th/net/animation-multi-frame-images/create-multi-frame-tiff-images-aspose-imaging-dotnet/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# วิธีแปลง JPEG เป็น TIFF และสร้างภาพ TIFF แบบหลายเฟรมด้วย Aspose.Imaging สำหรับ .NET

## Introduction

คุณกำลังมองหาวิธีเชี่ยวชาญการ **convert JPEG to TIFF** พร้อมกับการสร้างไฟล์ TIFF แบบหลายเฟรมโดยใช้ Aspose.Imaging สำหรับ .NET หรือไม่? คำแนะนำที่ครอบคลุมนี้จะนำคุณผ่านการตั้งค่าสภาพแวดล้อม, การกำหนดค่า `TiffOptions`, การปรับขนาดไฟล์ JPEG, และการเพิ่มเฟรมลงในภาพ TIFF — ทั้งหมดอย่างง่ายดาย ไม่ว่าคุณจะจัดการกับคลังเอกสารหรือรวมการประมวลผลภาพคุณภาพสูงเข้ากับแอปพลิเคชันซอฟต์แวร์, คู่มือนี้ออกแบบมาเพื่อเพิ่มประสิทธิภาพการทำงานของคุณ

**สิ่งที่คุณจะได้เรียนรู้:**
- วิธีตั้งค่า Aspose.Imaging สำหรับ .NET
- การกำหนดค่า `TiffOptions` สำหรับภาพขาว‑ดำโดยใช้การบีบอัด CCITT Fax Group 3
- การโหลดและปรับขนาดไฟล์ JPEG จากไดเรกทอรี
- การเพิ่มเฟรมลงในภาพ TIFF
- การบันทึกภาพ TIFF แบบหลายเฟรม

มาดูข้อกำหนดเบื้องต้นเพื่อเริ่มต้นกันเถอะ

## Quick Answers
- **What does “convert JPEG to TIFF” mean?** It means taking a JPEG raster image and saving it in the TIFF format, often with custom compression or multiple frames.  
  **คำตอบ:** หมายถึงการนำภาพ JPEG ที่เป็นแรสเตอร์มาบันทึกเป็นรูปแบบ TIFF ซึ่งมักจะใช้การบีบอัดแบบกำหนดเองหรือหลายเฟรม
- **Which library handles this best in .NET?** Aspose.Imaging for .NET provides a rich API for conversion, resizing, and multi‑frame creation.  
  **คำตอบ:** Aspose.Imaging for .NET ให้ API ที่ครบถ้วนสำหรับการแปลง, ปรับขนาด, และการสร้างหลายเฟรม
- **Do I need a license?** A free trial works for evaluation; a permanent license removes all evaluation limitations.  
  **คำตอบ:** สามารถใช้รุ่นทดลองฟรีเพื่อประเมิน; ใบอนุญาตถาวรจะลบข้อจำกัดการทดลองทั้งหมด
- **Can I load images from a directory automatically?** Yes – the tutorial shows how to enumerate JPEG files and process each one.  
  **คำตอบ:** ใช่ – คำแนะนำนี้แสดงวิธีวนลูปไฟล์ JPEG ทั้งหมดในโฟลเดอร์และประมวลผลแต่ละไฟล์
- **Is the code compatible with .NET 6+?** Absolutely – the sample uses .NET Core/5+ APIs that run on .NET 6 and later.  
  **คำตอบ:** แน่นอน – ตัวอย่างใช้ API ของ .NET Core/5+ ที่ทำงานบน .NET 6 ขึ้นไป

## What is “convert JPEG to TIFF”?
การแปลง JPEG เป็น TIFF เกี่ยวข้องกับการถอดรหัสไฟล์ JPEG, ปรับเปลี่ยนตามต้องการ (เช่น ปรับขนาดหรือเปลี่ยนความลึกสี) แล้วเข้ารหัสผลลัพธ์เป็นไฟล์ TIFF. TIFF รองรับหลายเฟรม, การบีบอัดแบบไม่มีการสูญเสีย, และเมตาดาต้าที่ JPEG ไม่มี ทำให้เหมาะสำหรับการเก็บถาวรและสถานการณ์หลายหน้า

## Why use Aspose.Imaging for this conversion?
- **การควบคุมเต็มรูปแบบ** บนการบีบอัด, การตีความโฟโตเมตริก, และรูปแบบพิกเซล  
- **รองรับหลายเฟรม** – คุณสามารถรวมหลายหน้า JPEG ไว้ในเอกสาร TIFF ไฟล์เดียว  
- **ข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux, และ macOS ด้วย .NET Core/5+  
- **ไม่มีการพึ่งพาไลบรารีภายนอก** – โค้ดจัดการทั้งหมดเป็น Managed Code, ไม่ต้องใช้ DLL แบบเนทีฟ

## Prerequisites

### Required Libraries and Dependencies
- **Aspose.Imaging for .NET**: Install this library using either NuGet or your preferred package manager.

### Environment Setup Requirements
- สภาพแวดล้อมการพัฒนาที่รองรับ C# และ .NET Core/5+

### Knowledge Prerequisites
- ความเข้าใจพื้นฐานเกี่ยวกับแนวคิดการเขียนโปรแกรม C#  
- ความคุ้นเคยกับการจัดการไฟล์ภาพใน .NET  

## Setting Up Aspose.Imaging for .NET

**.NET CLI**
```shell
dotnet add package Aspose.Imaging
```

**Package Manager**
```powershell
Install-Package Aspose.Imaging
```

**NuGet Package Manager UI**  
ค้นหา "Aspose.Imaging" แล้วติดตั้งเวอร์ชันล่าสุด

### License Acquisition Steps
- **Free Trial**: Access a limited functionality version to test out features.  
- **Temporary License**: Obtain this for an extended trial without evaluation limitations. Visit [Temporary License](https://purchase.aspose.com/temporary-license/).  
- **Purchase**: For full access, consider purchasing a license at [Purchase Aspose.Imaging](https://purchase.aspose.com/buy).

### Basic Initialization and Setup

```csharp
// Initialize the library with your license
Aspose.Imaging.License license = new Aspose.Imaging.License();
license.SetLicense("Path to your license file");
```

## How to Convert JPEG to TIFF and Add Multiple Frames

มาดูการทำงานเป็นขั้นตอนย่อย ๆ กัน

### Create and Configure TiffOptions for TIFF Image

#### Overview
การสร้างอ็อบเจกต์ `TiffOptions` ช่วยให้คุณกำหนดค่าต่าง ๆ เช่น การบีบอัดและการตีความโฟโตเมตริก, ซึ่งจำเป็นสำหรับการปรับแต่งไฟล์ TIFF ของคุณ

#### Step‑by‑Step Implementation

**1. Import Necessary Namespaces**  
Ensure you have these namespaces included in your file:

```csharp
using Aspose.Imaging.FileFormats.Tiff;
using Aspose.Imaging.FileFormats.Tiff.Enums;
using Aspose.Imaging.ImageOptions;
```

**2. Configure TiffOptions**  
Set up the `TiffOptions` object with specific configurations for a black‑and‑white image using CCITT Fax Group 3 compression.

```csharp
// Create TiffOptions with default settings
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);

// Set bits per sample to 1 (black and white)
outputSettings.BitsPerSample = new ushort[] { 1 };

// Use CCITT Fax Group 3 compression
outputSettings.Compression = TiffCompressions.CcittFax3;

// Define photometric interpretation as MinIsWhite
outputSettings.Photometric = TiffPhotometrics.MinIsWhite;

// Set source to an empty stream for creating new TIFF from scratch
outputSettings.Source = new Aspose.Imaging.Sources.StreamSource(new System.IO.MemoryStream());
```

### Create and Configure TiffImage with Specific Dimensions

#### Overview
การสร้าง `TiffImage` เกี่ยวข้องกับการกำหนดขนาดที่กำหนดเอง, ซึ่งสำคัญเมื่อกำหนดขนาดของแต่ละเฟรมใน TIFF

**1. Define Image Dimensions**

```csharp
int newWidth = 500; // Width for each TIFF frame
int newHeight = 500; // Height for each TIFF frame
string path = "@YOUR_OUTPUT_DIRECTORY\\AddFramesToTIFFImage_out.tif";
```

**2. Create a TiffImage Instance**  
Initialize the `TiffImage` with specified dimensions and output settings.

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    // Logic to add frames will be added here.
}
```

### Load JPEG Files from Directory and Resize Them

#### Overview
การโหลดภาพ JPEG, ปรับขนาด, และเตรียมสำหรับการใส่ลงในไฟล์ TIFF ทำได้อย่างราบรื่นด้วย Aspose.Imaging

**1. Load JPEG Images**

```csharp
string dataDir = "@YOUR_DOCUMENT_DIRECTORY"; // Directory containing input images

foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
{
    using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
    {
        // Resize image to match TIFF frame dimensions
        ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
        
        // Additional logic for handling multiple frames will be added here.
    }
}
```

> **Pro tip:** The phrase **load images from directory** is exactly what the loop above does – it enumerates every JPEG file in the target folder.

### Add Frame to TiffImage and Save It

#### Overview
การเพิ่มเฟรมลงในภาพ TIFF เกี่ยวข้องกับการคัดลอกพิกเซล JPEG ที่ปรับขนาดแล้วเข้าไปในแต่ละเฟรมและบันทึก TIFF แบบหลายเฟรมที่สมบูรณ์

**1. Initialize the TiffImage Instance**

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    int index = 0; // Frame index tracker
    
    foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
    {
        using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
        {
            ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
            
            TiffFrame frame = tiffImage.ActiveFrame;
            if (index > 0)
            {
                // Create a new frame for each subsequent image
                frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            }
            
            // Copy pixels from the resized JPEG into the TIFF frame
            frame.SavePixels(frame.Bounds, ri.LoadPixels(ri.Bounds));
            if (index > 0)
            {
                tiffImage.AddFrame(frame); // Add to TIFF image only after the first frame
            }
            index++;
        }
    }
    
    tiffImage.Save(path); // Save the final TIFF with all frames
}
```

## Practical Applications

1. **Document Archiving** – Store scanned documents as a single TIFF file to ensure data integrity and ease of access.  
   **การเก็บเอกสาร** – เก็บเอกสารสแกนเป็นไฟล์ TIFF เดียวเพื่อความสมบูรณ์ของข้อมูลและการเข้าถึงที่ง่าย
2. **Medical Imaging** – Use high‑quality, compressed TIFF formats for storing scans like MRIs and CTs.  
   **การถ่ายภาพทางการแพทย์** – ใช้รูปแบบ TIFF คุณภาพสูงและบีบอัดสำหรับเก็บสแกนเช่น MRI และ CT
3. **Graphic Design** – Combine multiple design layers into a single file for efficient handling in graphic software.  
   **การออกแบบกราฟิก** – รวมหลายเลเยอร์การออกแบบเป็นไฟล์เดียวเพื่อการจัดการที่มีประสิทธิภาพในซอฟต์แวร์กราฟิก
4. **Photography** – Archive multi‑page photo albums as single files for easy sharing and storage.  
   **การถ่ายภาพ** – เก็บอัลบั้มภาพหลายหน้เป็นไฟล์เดียวเพื่อการแชร์และจัดเก็บที่ง่าย
5. **Industrial Quality Control** – Record detailed inspection data across multiple frames in a TIFF image.  
   **การควบคุมคุณภาพในอุตสาหกรรม** – บันทึกข้อมูลการตรวจสอบละเอียดหลายเฟรมในภาพ TIFF

## Performance Considerations

### Tips for Optimizing Performance
- **Memory Management** – Dispose of image objects promptly (`using` statements) to free resources.  
  **การจัดการหน่วยความจำ** – ปิดวัตถุภาพโดยเร็ว (`using` statements) เพื่อปล่อยทรัพยากร
- **Batch Processing** – Process images in batches if dealing with large datasets to keep memory usage predictable.  
  **การประมวลผลเป็นชุด** – ประมวลผลภาพเป็นชุดเมื่อทำงานกับข้อมูลจำนวนมากเพื่อควบคุมการใช้หน่วยความจำ
- **Efficient Compression** – Choose compression settings that balance quality and speed for your scenario.  
  **การบีบอัดที่มีประสิทธิภาพ** – เลือกการตั้งค่าการบีบอัดที่สมดุลระหว่างคุณภาพและความเร็วตามกรณีของคุณ

## Frequently Asked Questions

**Q: Can I convert JPEG to TIFF without losing quality?**  
A: Yes. By using lossless compression options (e.g., LZW or CCITT Fax) and preserving the original pixel data, the conversion can be lossless.

**Q: Do I need to resize images before adding them as frames?**  
A: All frames in a TIFF must share the same dimensions, so resizing each JPEG to the target width and height is required.

**Q: How many frames can a TIFF file contain?**  
A: Practically unlimited; the limit is governed by file size and available memory.

**Q: Is the generated TIFF compatible with common viewers?**  
A: The example uses standard CCITT Fax Group 3 compression, which is widely supported by most TIFF viewers and editors.

**Q: What if I want to add a different compression for color images?**  
A: Replace `TiffCompressions.CcittFax3` with `TiffCompressions.Lzw` or `TiffCompressions.Jpeg` and adjust `BitsPerSample` accordingly.

## Conclusion

บทแนะนำนี้ครอบคลุมขั้นตอนสำคัญสำหรับ **convert JPEG to TIFF** และการสร้างภาพ TIFF แบบหลายเฟรมด้วย Aspose.Imaging สำหรับ .NET ตั้งแต่การกำหนดค่า `TiffOptions` ไปจนถึงการเพิ่มเฟรม คุณมีพื้นฐานที่มั่นคงเพื่อผสานการประมวลผลภาพคุณภาพสูงเข้าสู่แอปพลิเคชันของคุณแล้ว

**Next Steps**  
- ทดลองใช้ประเภทการบีบอัดและความลึกสีอื่น ๆ  
- สำรวจคุณลักษณะเพิ่มเติมของ Aspose.Imaging เช่น การจัดการเมตาดาต้าหรือการแปลงเป็น PDF  
- ดูเอกสาร [official documentation](https://reference.aspose.com/imaging/net/) เพื่อเรียนรู้เชิงลึกเพิ่มเติม

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-02-09  
**Tested With:** Aspose.Imaging for .NET (latest stable version)  
**Author:** Aspose