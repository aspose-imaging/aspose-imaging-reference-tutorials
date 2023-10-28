---
title: Diagonal Image Watermarking with Aspose.Imaging for Java
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
description: Enhance your images with a diagonal watermark using Aspose.Imaging for Java. Follow this step-by-step guide and create stunning watermarked images effortlessly.
type: docs
weight: 14
url: /java/image-processing-and-enhancement/diagonal-image-watermarking.html/
---

If you're looking to enhance your images with a stylish diagonal watermark, Aspose.Imaging for Java is here to help. In this step-by-step guide, we'll walk you through the process of adding a 45-degree rotated text watermark to an existing JPG image. You don't need to be an expert in Java or image processing to follow along – we'll break down each example into multiple steps to ensure you can easily achieve professional results.

## Prerequisites

Before we dive into the exciting world of image watermarking, you'll need a few things in place:

1. Aspose.Imaging for Java: Make sure you have Aspose.Imaging for Java installed. You can find the download link [here](https://releases.aspose.com/imaging/java/).

2. Java Development Environment: You should have a working Java development environment set up on your computer.

3. An Image to Watermark: Prepare the image you want to watermark and store it in a directory. You can use a sample image for this tutorial.

## Import Packages

First, import the necessary packages to get your Java project ready for image watermarking. Below are the essential packages you need to include:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Step 1: Load an Existing Image

Load the image you want to watermark. In this example, we assume you have a JPG image named "SampleTiff1.tiff" in your "ModifyingImages" directory.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

## Step 2: Prepare Watermark Text and Graphics

Now, let's declare your watermark text and set up the graphics for the watermark.

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## Step 3: Define Font and Brush

Set the font and brush for your watermark. You can customize the font, size, and style to match your preferences.

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Step 4: Format Your Text

Define the format for your watermark text, including alignment and format flags.

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Step 5: Apply Transformation

Create a transformation matrix to position and rotate the watermark text. In this example, we'll rotate the text by 45 degrees.

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

Now, it's time to add the text to the image, and save the watermarked image to your desired location.

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Congratulations! You've successfully added a diagonal watermark to your image using Aspose.Imaging for Java.

## Conclusion

In this tutorial, we've learned how to enhance your images with a diagonal watermark using Aspose.Imaging for Java. It's a powerful tool for adding a professional touch to your images. With just a few simple steps, you can create stunning watermarked images that stand out from the rest.

## FAQ's

### Q1: Is Aspose.Imaging for Java suitable for beginners?

A1: Absolutely! Aspose.Imaging for Java offers a user-friendly interface and comprehensive documentation. Even beginners can quickly get started with image processing.

### Q2: Can I customize the watermark text and style?

A2: Yes, you can easily customize the watermark text, font, size, color, and rotation angle to match your preferences and branding.

### Q3: Does Aspose.Imaging for Java support other image formats besides JPG?

A3: Yes, Aspose.Imaging for Java supports a wide range of image formats, including BMP, PNG, GIF, and more.

### Q4: Is there a free trial available for Aspose.Imaging for Java?

A4: Yes, you can try Aspose.Imaging for Java with a free trial. Get it [here](https://releases.aspose.com/).

### Q5: Where can I find help or support for Aspose.Imaging for Java?

A5: If you have any questions or need assistance, visit the Aspose.Imaging for Java support forum [here](https://forum.aspose.com/).
