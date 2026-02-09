---
title: How to Draw Arc with Aspose.Imaging for .NET
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: Learn how to draw arc using Aspose.Imaging for .NET, including how to save BMP file, set image size, and set graphics background. Step‑by‑step guide for generating BMP images.
weight: 10
url: /net/basic-drawing/draw-arc/
date: 2026-02-09
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# How to Draw Arc with Aspose.Imaging for .NET

In the world of image processing, **how to draw arc** is a common task that can add visual flair to any graphic. With Aspose.Imaging for .NET you can generate BMP images, set the image size, and draw an arc with a pen in just a few lines of C#. By the end of this tutorial you’ll know exactly how to draw an arc, set the graphics background, and save the resulting BMP file effortlessly.

## Quick Answers
- **What does the code produce?** A 100 × 100 pixel BMP image with a yellow background and a black arc.  
- **Which library is used?** Aspose.Imaging for .NET.  
- **Do I need a license?** A free trial works for development; a commercial license is required for production.  
- **Can I change the image size?** Yes – modify the width and height parameters in the `Image.Create` call.  
- **Is the output format fixed?** The example saves a BMP file, but any format supported by Aspose.Imaging can be used.

## What is “how to draw arc” in Aspose.Imaging?
Drawing an arc means rendering a curved line segment defined by a bounding rectangle, a start angle, and a sweep angle. Aspose.Imaging provides the `Graphics.DrawArc` method, which lets you **draw arc with pen** and control every visual aspect.

## Why use Aspose.Imaging for this task?
- **Full control** over image dimensions, color depth, and file format.  
- **No external dependencies** – everything runs on pure .NET.  
- **High performance** for generating large numbers of graphics on the server side.  

## Prerequisites

Before we dive into the code, make sure you have the following:

1. **Aspose.Imaging for .NET** – download it from the official site [here](https://releases.aspose.com/imaging/net/).  
2. **A .NET development environment** (Visual Studio, VS Code, or any C# compiler).  

Now that we have our prerequisites ready, let’s start drawing!

## Importing Necessary Namespaces

To work with Aspose.Imaging you need to bring the relevant namespaces into scope:

### Step 1: Import the Namespaces

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

These `using` statements give you access to image creation, graphics handling, and file I/O classes.

## How to Draw Arc with Aspose.Imaging for .NET

We’ll break the process into three clear steps: create the image, prepare the graphics surface, and finally draw the arc.

### Step 1: Set Up the Image (set image size & generate BMP image)

```csharp
// Specify the directory where you want to save the image
string dataDir = "Your Document Directory";

// Create an instance of FileStream to save the image
using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
{
    // Create an instance of BmpOptions and set its properties
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;

    // Set the source for BmpOptions and create an instance of Image
    saveOptions.Source = new StreamSource(stream);
    using (Image image = Image.Create(saveOptions, 100, 100))
    {
```

Here we **set image size** to 100 × 100 pixels and configure the BMP options. The `FileStream` ensures we **save BMP file** to the desired location.

### Step 2: Initialize Graphics and Set Graphics Background

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

The `Graphics` object lets us paint on the image. By calling `Clear(Color.Yellow)` we **set graphics background** to a bright yellow, making the arc stand out.

### Step 3: Define Arc Parameters and Draw Arc with Pen

```csharp
        // Define the parameters for the arc
        int width = 100;
        int height = 200;
        int startAngle = 45;
        int sweepAngle = 270;

        // Draw the arc
        graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);

        // Save the changes
        image.Save();
    }
    stream.Close();
}
```

- `width` and `height` define the bounding rectangle, effectively **set image size** for the arc.  
- The `Pen` object is what lets us **draw arc with pen** in black.  
- After drawing, `image.Save()` writes the **BMP file** to disk.

## Common Issues & Tips

- **Arc not visible?** Make sure the pen color contrasts with the background (e.g., black on yellow).  
- **Incorrect dimensions?** Remember that the arc’s bounding rectangle can be larger than the image; adjust `width`/`height` or the image size accordingly.  
- **Performance tip:** Reuse a single `Graphics` instance if you need to draw multiple shapes on the same image.

## FAQ's

### Q1: Where can I find the documentation for Aspose.Imaging for .NET?

A1: You can refer to the documentation [here](https://reference.aspose.com/imaging/net/) for comprehensive information on Aspose.Imaging for .NET.

### Q2: How can I download Aspose.Imaging for .NET?

A2: You can download Aspose.Imaging for . .NET from the website [here](https://releases.aspose.com/imaging/net/).

### Q3: Is there a free trial available for Aspose.Imaging for .NET?

A3: Yes, you can get a free trial version [here](https://releases.aspose.com/) to try out Aspose.Imaging for .NET.

### Q4: Do I need a temporary license for Aspose.Imaging for .NET?

A4: If you need a temporary license, you can obtain one [here](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I seek support or ask questions about Aspose.Imaging for .NET?

A5: You can visit the Aspose.Imaging forum for support and discussions [here](https://forum.aspose.com/).

---

**Last Updated:** 2026-02-09  
**Tested With:** Aspose.Imaging 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}