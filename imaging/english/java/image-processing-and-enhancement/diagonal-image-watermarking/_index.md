---
title: How to Add Watermark – Diagonal Image Watermarking (Java)
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
description: Learn how to add watermark to images with Aspose.Imaging for Java. This java image processing tutorial shows step‑by‑step how to create a diagonal watermark quickly.
weight: 14
date: 2026-01-09
url: /java/image-processing-and-enhancement/diagonal-image-watermarking/
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# How to Add Watermark – Diagonal Image Watermarking (Java)

If you're looking to **how to add watermark** to your pictures with a stylish diagonal orientation, Aspose.Imaging for Java makes it painless. In this step‑by‑step tutorial we’ll walk through adding a 45‑degree rotated text watermark to a JPG (or any supported) image. You don’t need to be a Java wizard – each block is explained in plain language so you can replicate the result in minutes.

## Quick Answers
- **What library is used?** Aspose.Imaging for Java  
- **Which primary keyword is covered?** how to add watermark  
- **Supported image formats?** JPEG, PNG, BMP, TIFF, GIF and more  
- **How much code is required?** Only seven concise code blocks  
- **Do I need a license for testing?** A free trial is available; a license is required for production  

## What is “how to add watermark” in image processing?
Adding a watermark means overlaying semi‑transparent text or graphics onto an image to protect ownership or convey branding. A diagonal watermark is especially effective because it spans the whole picture and is harder to crop out.

## Why use Aspose.Imaging for Java?
Aspose.Imaging provides a high‑level API that abstracts low‑level pixel manipulation, supports dozens of formats, and works on any Java runtime. It lets you focus on *what* you want to achieve—like adding a diagonal watermark—without worrying about image‑format quirks.

## Prerequisites

Before we dive in, make sure you have the following:

1. **Aspose.Imaging for Java** – download the latest version from the official site **[here](https://releases.aspose.com/imaging/java/)**.  
2. **Java Development Environment** – JDK 8+ and your favorite IDE (IntelliJ, Eclipse, VS Code, etc.).  
3. **An image to watermark** – place a sample JPG/TIFF/PNG in a folder you’ll reference in the code.

## Import Packages

First, import the classes you’ll need. Keeping imports together makes the code easier to read and maintain.

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Step 1: Load an Existing Image

We start by loading the source picture. The `Image.load` method automatically detects the format.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **Pro tip:** Wrap the `Image` object in a try‑with‑resources block (as shown) so it’s disposed automatically, preventing memory leaks.

## Step 2: Prepare Watermark Text and Graphics

Create a `Graphics` object linked to the loaded image and store the image size for later calculations.

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## Step 3: Define Font and Brush

Choose a font that stands out and a brush that defines the watermark’s colour and opacity. Adjust the opacity to make the watermark semi‑transparent.

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Step 4: Format Your Text

Set alignment and formatting flags so the text is centred when drawn.

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Step 5: Apply Transformation

A transformation matrix lets us move the origin to the centre of the image and then rotate the text by ‑45° (clockwise).

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## Step 6: Draw and Save

Finally, render the string onto the image and write the result to disk.

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

When you open `AddDiagonalWatermarkToImage_out.jpg` you’ll see the red, semi‑transparent text slanted across the centre of the picture.

## Common Issues & Solutions

| Problem | Reason | Fix |
|---------|--------|-----|
| Watermark appears too faint | Opacity set to 0 (fully transparent) | Increase opacity, e.g., `brush.setOpacity(0.5f);` |
| Text is clipped at edges | Translation not centered for non‑square images | Use `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` as shown, then adjust rotation angle if needed |
| Unsupported image format error | Using an older Aspose.Imaging version | Update to the latest Aspose.Imaging release |

## Frequently Asked Questions

### Q1: Is Aspose.Imaging for Java suitable for beginners?

**A:** Absolutely! The API is intuitive, and the documentation provides clear examples. Even developers new to image processing can follow this tutorial and produce professional results quickly.

### Q2: Can I customize the watermark text and style?

**A:** Yes. Change the `theString` variable, pick a different `Font`, modify `brush.setColor(...)`, or adjust the rotation angle in the matrix to suit your branding.

### Q3: Does Aspose.Imaging for Java support other image formats besides JPG?

**A:** Yes. The library works with BMP, PNG, GIF, TIFF, PSD, and many more. Just point the `Image.load` method at the appropriate file.

### Q4: Is there a free trial available for Aspose.Imaging for Java?

**A:** Yes, you can try Aspose.Imaging for Java with a free trial. Get it **[here](https://releases.aspose.com/)**.

### Q5: Where can I find help or support for Aspose.Imaging for Java?

**A:** For questions, bug reports, or best‑practice advice, visit the Aspose.Imaging for Java support forum **[here](https://forum.aspose.com/)**.

---

**Last Updated:** 2026-01-09  
**Tested With:** Aspose.Imaging for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}