---
title: "Create PNG with Text and Align Strings Using Aspose.Imaging"
description: "Learn how to create PNG with text, align strings, and draw left, center, or right aligned text in .NET using Aspose.Imaging."
date: "2026-01-30"
weight: 1
url: "/net/advanced-drawing-graphics/aspose-imaging-net-string-alignment-guide/"
keywords:
- Aspose.Imaging for .NET
- string alignment in .NET
- drawing strings in C#
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Create PNG with Text and Align Strings Using Aspose.Imaging

## Introduction

If you need to **create PNG with text** and control its alignment—whether left, center, or right—this guide has you covered. In modern .NET applications, drawing text on images is a common requirement for report generation, dynamic graphics, and automated document workflows. We'll walk through the process of using **Aspose.Imaging for .NET** to draw strings, measure string size, and position them precisely on a PNG canvas.

### What You'll Learn
- How to set up Aspose.Imaging for .NET
- **How to draw text** with left, center, and right alignment
- Techniques to **measure string size C#** for perfect placement
- Ways to **center text on image** and draw left aligned text
- Performance tips for handling large image batches

Now that you know what we’ll achieve, let’s get the environment ready.

## Quick Answers
- **What does “create PNG with text” mean?** Generating a PNG image that contains rendered text.
- **Which library handles alignment?** Aspose.Imaging for .NET provides built‑in alignment support.
- **Do I need a license?** A free trial works for development; a paid license is required for production.
- **Can I center text on image?** Yes—use `StringAlignment.Center` in the `StringFormat`.
- **Is measuring string size necessary?** Absolutely; it ensures text fits and aligns correctly.

## What is “create PNG with text”?
Creating a PNG with text means programmatically generating a PNG image file and rendering one or more strings onto it. This is useful for dynamic graphics, watermarks, or custom report headers.

## Why use Aspose.Imaging for .NET?
Aspose.Imaging offers a rich API that abstracts low‑level GDI+ details, provides cross‑platform support, and includes advanced features like precise string measurement and alignment without extra dependencies.

## Prerequisites
- **Aspose.Imaging for .NET** (latest version via NuGet)
- **.NET Core 3.0** or later (including .NET 6/7)
- Basic C# knowledge and familiarity with file I/O

## Setting Up Aspose.Imaging for .NET
Getting started with Aspose.Imaging is straightforward. Follow these steps to integrate it into your project:

### Installation Information
#### Using the .NET CLI
```bash
dotnet add package Aspose.Imaging
```

#### Using Package Manager
```powershell
Install-Package Aspose.Imaging
```

#### Using the NuGet Package Manager UI
Navigate to the NuGet Package Manager in your IDE, search for "Aspose.Imaging," and install the latest version.

### License Acquisition Steps
1. **Free Trial**: Start with a free trial by downloading the library from [Aspose's website](https://releases.aspose.com/imaging/net/).
2. **Temporary License**: Obtain a temporary license if you want to explore full features without limitations.
3. **Purchase**: Consider purchasing a license for production use.

### Basic Initialization and Setup
```csharp
using Aspose.Imaging;
```

Now that our setup is complete, let’s dive into the implementation.

## Implementation Guide
This section walks you through each step required to **create PNG with text** and align it correctly.

### How to Create PNG with Text and Align Strings
#### Overview
The code below demonstrates drawing left‑aligned, centered, and right‑aligned text on a PNG image. It also shows how to **measure string size C#** to position each line precisely.

#### Step‑by‑Step Instructions
##### Step 1: Define File Paths, Alignments, Fonts, and Sizes
We start by declaring the output folder, the alignment options we’ll iterate over, and a collection of fonts and sizes to showcase.
```csharp
string baseFolder = "YOUR_DOCUMENT_DIRECTORY";
string[] alignments = new[] { "Left", "Center", "Right" };
string[] fontNames = new[] { "Arial", "Times New Roman", "Bookman Old Style", "Calibri", "Comic Sans MS",
    "Courier New", "Microsoft Sans Serif", "Tahoma", "Verdana", "Proxima Nova Rg" };
float[] fontSizes = new[] { 10f, 22f, 50f, 100f };
```

##### Step 2: Create Output File and Configure Image Options
For each alignment we generate a separate PNG file. The `PngOptions` object tells Aspose.Imaging how to write the image.
```csharp
string fileName = "output_" + align + ".png";
string outputFileName = Path.Combine(baseFolder, fileName);

using (FileStream stream = new FileStream(outputFileName, FileMode.Create))
{
    Aspose.Imaging.ImageOptions.PngOptions pngOptions = new Aspose.Imaging.ImageOptions.PngOptions();
    pngOptions.Source = new Aspose.Imaging.Sources.StreamSource(stream);
}
```

##### Step 3: Initialize Graphics, Clear Background, and Prepare Brushes
We create the image canvas, clear it to white, and set up a black brush for text and a red pen for guide lines.
```csharp
using (Aspose.Imaging.Image image = Aspose.Imaging.Image.Create(pngOptions, width, height))
{
    Aspose.Imaging.Graphics graphics = new Aspose.Imaging.Graphics(image);
    graphics.Clear(Aspose.Imaging.Color.White);

    SolidBrush brush = new SolidBrush(Color.Black);
    Pen pen = new Pen(Color.Red, 1);
}
```

##### Step 4: Draw Strings with the Desired Alignment
Here we map our textual alignment choice to `StringAlignment`, create a `StringFormat`, and then render each line. This also demonstrates **how to draw text** left, center, or right aligned.
```csharp
StringAlignment alignment = align switch
{
    "Left" => StringAlignment.Near,
    "Center" => StringAlignment.Center,
    "Right" => StringAlignment.Far,
    _ => StringAlignment.Near,
};

StringFormat stringFormat = new StringFormat(StringFormatFlags.ExactAlignment) { Alignment = alignment };

foreach (var fontName in fontNames)
{
    foreach (var fontSize in fontSizes)
    {
        Font font = new Font(fontName, fontSize);
        string text = $"This is font: {fontName}, size:{fontSize}";
        SizeF textSize = graphics.MeasureString(text, font, SizeF.Empty, null); // **measure string size C#**

        graphics.DrawString(text, font, brush, new RectangleF(x, y, w, textSize.Height), stringFormat);
        y += textSize.Height;
    }

    graphics.DrawLine(pen, new Point((int)x, (int)y), new Point((int)(x + w), (int)y));
}

graphics.DrawLine(pen, new Point(lineX, 0), new Point(lineX, (int)y));
```

##### Step 5: Save the Image and Clean Up
Finally, we persist the PNG to disk and optionally delete the temporary stream file.
```csharp
image.Save();
File.Delete(outputFileName);
```

### Troubleshooting Tips
- **Image Not Saving** – Verify that the output directory exists and you have write permissions.
- **Incorrect Alignment** – Double‑check the `StringAlignment` mapping; using `StringAlignment.Near` draws left‑aligned text.
- **Unexpected Font Rendering** – Ensure the selected fonts are installed on the host machine.

## Practical Applications
1. **Report Generation** – Add left‑aligned headings, centered titles, and right‑aligned footers automatically.
2. **Dynamic Banner Creation** – Generate marketing banners where text must be precisely centered.
3. **Document Automation** – Insert aligned text into image‑based templates for invoices or certificates.

## Performance Considerations
- **Resize Images Wisely** – Choose the smallest dimensions that still meet quality requirements.
- **Dispose Objects** – Use `using` statements (as shown) to free unmanaged resources promptly.
- **Batch Process** – When creating many PNGs, reuse `PngOptions` and only change the drawing surface.

## Conclusion
You now know how to **create PNG with text**, measure string dimensions, and align the content exactly where you need it. By leveraging Aspose.Imaging’s robust API, you can add sophisticated text rendering to any .NET application.

### Next Steps
- Experiment with additional drawing features like shadows or outlines.
- Combine text rendering with image filters for richer graphics.
- Integrate this routine into a larger document‑generation pipeline.

## FAQ Section
1. **What is Aspose.Imaging for .NET?**  
   - A powerful library for processing images, including drawing text with various alignments.
2. **How do I set up Aspose.Imaging for .NET?**  
   - Install via NuGet Package Manager or CLI as described in the setup section.

**Q: Can I use this code to center text on image?**  
A: Yes—set the alignment to `StringAlignment.Center` as demonstrated in Step 4.

**Q: How do I measure string size in C#?**  
A: Use `graphics.MeasureString` which returns a `SizeF` representing the rendered dimensions.

**Q: What if I need to draw left aligned text only?**  
A: Use `StringAlignment.Near` (or `StringAlignment.Far` for right) when constructing the `StringFormat`.

**Q: Does Aspose.Imaging support other image formats?**  
A: Absolutely; you can create JPEG, BMP, TIFF, and more by swapping the `ImageOptions` class.

**Q: Is a license required for production?**  
A: Yes—purchase a license to remove the evaluation watermark and unlock full functionality.

---

**Last Updated:** 2026-01-30  
**Tested With:** Aspose.Imaging 24.12 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}