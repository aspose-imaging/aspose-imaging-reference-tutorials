---
title: How to Draw a Raster Image on SVG in Aspose.Imaging for .NET
linktitle: Draw Raster Image on SVG in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: Learn how to draw raster images on SVG using Aspose.Imaging for .NET. Enhance your .NET applications with dynamic images.
weight: 11
url: /net/vector-image-processing/draw-raster-image-on-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Draw a Raster Image on SVG in Aspose.Imaging for .NET


In the world of .NET programming, Aspose.Imaging stands as a reliable and versatile library for handling various image-related tasks. One fascinating capability it offers is the ability to draw a raster image on an SVG canvas. In this step-by-step guide, we will walk you through the process of drawing a raster image on an SVG using Aspose.Imaging for .NET.

## Prerequisites

Before we dive into the details, make sure you have the following prerequisites in place:

- Aspose.Imaging for .NET: You must have the library installed. If not, you can download it from the [Aspose.Imaging for .NET download page](https://releases.aspose.com/imaging/net/).

- Your Document Directory: Replace `"Your Document Directory"` with the actual path to your working directory.

Now, let's break down the process into easy-to-follow steps:

## Step 1: Import Necessary Namespaces

You need to import the required namespaces to work with Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Step 2: Load the Images

- First, load the raster image that you want to draw on the SVG canvas.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Next, load the SVG canvas image where you want to draw the raster image.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Step 3: Drawing on the SVG Image

Now, you can start drawing on the existing SVG image. To do this, you need to create an instance of `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Step 4: Draw the Raster Image

- Define the bounds where you want to draw the raster image and specify the source region from the raster image.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Step 5: Save the Result

After drawing the raster image on the SVG canvas, you can save the resulting image:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Conclusion

Congratulations! You've successfully drawn a raster image on an SVG canvas using Aspose.Imaging for .NET. This can be incredibly useful for creating rich and dynamic images within your .NET applications.

For more information and detailed documentation, visit the [Aspose.Imaging for .NET documentation](https://reference.aspose.com/imaging/net/).

## Frequently Asked Questions

### What is Aspose.Imaging for .NET?
   Aspose.Imaging for .NET is a powerful image processing library that allows developers to create, manipulate, and convert images in various formats within .NET applications.

### Can I use Aspose.Imaging for .NET in commercial projects?
   Yes, you can use Aspose.Imaging for .NET in both commercial and non-commercial projects. Licensing details can be found on the [purchase page](https://purchase.aspose.com/buy).

### Is there a free trial available?
   Yes, you can get a free trial of Aspose.Imaging for .NET from [here](https://releases.aspose.com/).

### Where can I get support or ask questions?
   If you have any questions or need support, you can visit the [Aspose.Imaging forum](https://forum.aspose.com/).

### How can I obtain a temporary license for Aspose.Imaging for .NET?
   You can get a temporary license from [here](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
