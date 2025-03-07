---
title: Draw Raster Image on WMF in Aspose.Imaging for .NET
linktitle: Draw Raster Image on WMF in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: Learn how to draw raster images on WMF documents in .NET using Aspose.Imaging. Enhance your .NET projects with creative image overlays.
weight: 12
url: /net/vector-image-processing/draw-raster-image-on-wmf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Draw Raster Image on WMF in Aspose.Imaging for .NET


In the realm of .NET development, Aspose.Imaging stands as a versatile tool that empowers developers to manipulate and work with images in various formats. Among its many capabilities, Aspose.Imaging offers the feature of drawing raster images on Windows Metafile (WMF) documents. This functionality is extremely valuable when you need to overlay images onto vector-based documents, opening up a world of creative possibilities.

## Prerequisites

Before diving into the world of drawing raster images on WMF documents using Aspose.Imaging for .NET, there are some prerequisites you need to fulfill:

### 1. Aspose.Imaging for .NET Library

First and foremost, make sure you have Aspose.Imaging for .NET library integrated into your .NET project. You can obtain this library by [downloading it from Aspose.Releases](https://releases.aspose.com/imaging/net/).

### 2. Basic Understanding of .NET

You should have a fundamental understanding of .NET development, including how to create and manage projects, work with libraries, and write code in C#.

### 3. Image Files

Prepare the image files you want to draw onto the WMF document. You should have the source image file in a raster format (e.g., PNG) and an existing WMF document that serves as the canvas.

With these prerequisites in place, let's explore the step-by-step guide to draw a raster image on a WMF document using Aspose.Imaging for .NET.

## Import Namespaces

Before you begin, ensure that you import the necessary namespaces in your C# code:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Examples.CSharp;
using Aspose.Imaging.FileFormats.Wmf;
using Aspose.Imaging.FileFormats.Png;
using Aspose.Imaging.FileFormats.Wmf.Graphics;
using Aspose.Imaging.FileFormats.Wmf.Objects;
```

## Step 1: Load Image Files

First, you need to load the source image and the WMF document into your project. The following code demonstrates how to load these files:

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";

// Load the image to be drawn
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
{
    // Load the WMF image for drawing on it (drawing surface)
    using (WmfImage canvasImage = (WmfImage)Image.Load(dataDir + "asposenet_222_wmf_200.wmf"))
    {
        // Continue to the next step.
    }
}
```

## Step 2: Initialize Graphics

To draw the raster image onto the WMF document, you need to initialize the graphics. Here's how you can do it:

```csharp
WmfRecorderGraphics2D graphics = WmfRecorderGraphics2D.FromWmfImage(canvasImage);
```

## Step 3: Draw the Image

Now, you're ready to draw the raster image onto the WMF document. Specify the location and size of the image within the canvas, as well as the source image's dimensions. The drawn image will stretch if the source and destination sizes differ:

```csharp
graphics.DrawImage(
    imageToDraw,
    new Rectangle(67, 67, canvasImage.Width, canvasImage.Height),
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    GraphicsUnit.Pixel);
```

## Step 4: Save the Result

Once you've completed the drawing process, save the result as a new WMF document:

```csharp
using (WmfImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_222_wmf_200.DrawImage.wmf");
}
```

## Conclusion

In this step-by-step guide, we've explored how to draw a raster image on a WMF document using Aspose.Imaging for .NET. This functionality allows you to combine vector and raster images, opening up endless possibilities for creative projects.

Remember to obtain the Aspose.Imaging for .NET library from the   website, and ensure you have the necessary image files ready for your project. With these steps and the provided code snippets, you can seamlessly integrate image drawing into your .NET applications.

### Frequently Asked Questions

### Can I use Aspose.Imaging for .NET with other .NET libraries and frameworks?
   - Yes, Aspose.Imaging for .NET is compatible with various .NET libraries and frameworks, making it versatile for integration into different projects.

### Are there any limitations when drawing raster images on WMF documents?
   - While Aspose.Imaging for .NET provides powerful image manipulation capabilities, it's essential to consider the document's size and resolution to ensure optimal results.

### Can I draw multiple images on a single WMF document?
   - Yes, you can draw multiple raster images onto a WMF document by repeating the drawing steps for each image.

### How can I add text or shapes to a WMF document using Aspose.Imaging for .NET?
   - Aspose.Imaging for .NET offers a wide range of functionalities for adding text and shapes to WMF documents. You can refer to the documentation for detailed examples.

### Where can I find support and additional resources for Aspose.Imaging for .NET?
   - You can find extensive documentation and seek assistance from the Aspose.Imaging community on the [Aspose.Imaging support forum](https://forum.aspose.com/).


Now, you have the knowledge to seamlessly integrate image drawing into your .NET applications using Aspose.Imaging for .NET. This creative capability opens the door to a world of possibilities for enhancing your projects with image overlays. If you have any questions or need further assistance, don't hesitate to reach out to the Aspose.Imaging community on their support forum. Happy coding!


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
