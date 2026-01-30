---
title: How to Draw Text on Image with Aspose.Imaging for .NET
linktitle: Draw Using GraphicsPath – draw text on image, shapes and patterns
second_title: Aspose.Imaging .NET Image Processing API
description: Learn how to draw text on image, draw shapes on image and fill shapes with pattern using Aspose.Imaging for .NET.
weight: 11
url: /net/advanced-drawing/draw-using-graphicspath/
date: 2026-01-30
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# How to Draw Text on Image with Aspose.Imaging for .NET

In this tutorial we’ll walk through **how to draw text on image** while also showing you how to draw shapes on image and fill shapes with pattern using the powerful Aspose.Imaging library. Whether you’re building a reporting tool, a custom badge generator, or just need to annotate pictures programmatically, the steps below will give you a solid foundation.

## Quick Answers
- **What can I draw?** Text, basic shapes (ellipse, rectangle) and patterned fills.  
- **Which class is central?** `GraphicsPath` combined with `Graphics`.  
- **Do I need a license?** A free trial works for development; a license is required for production.  
- **Supported formats?** BMP, PNG, JPEG, TIFF and many more via Aspose.Imaging.  
- **Prerequisites?** Visual Studio, .NET 6+ (or .NET Framework 4.6+), and Aspose.Imaging for .NET.

## What is drawing text on image with Aspose.Imaging?
Aspose.Imaging provides a high‑level API that abstracts away the low‑level GDI+ calls. By using the `Graphics` object together with a `GraphicsPath`, you can compose vector‑based drawings—text, shapes, and patterned fills—and render them onto a bitmap or any supported image format.

## Why draw shapes on image and fill shapes with pattern?
- **Visual emphasis:** Highlight regions with custom hatch patterns.  
- **Branding:** Add company logos or watermarks that combine text and graphics.  
- **Dynamic graphics:** Generate charts, badges, or certificates on the fly without external design tools.

## Prerequisites

1. **Visual Studio** – any recent edition (Community, Professional, or Enterprise).  
2. **Aspose.Imaging for .NET** – download it from the official site: [Download Aspose.Imaging for .NET](https://releases.aspose.com/imaging/net/).  
3. **Basic C# knowledge** – you should be comfortable with classes, namespaces, and the `using` directive.

## Import Namespaces

Open your project and make sure the Aspose.Imaging namespace is available:

```csharp
using Aspose.Imaging;
```

## Step 1: Setting Up the Environment

First we create a blank canvas that will host our drawing.

```csharp
public static void Run()
{
    Console.WriteLine("Running example DrawingUsingGraphicsPath");
    string dataDir = "Your Document Directory";

    // Create an instance of BmpOptions and set its various properties
    BmpOptions ImageOptions = new BmpOptions();
    ImageOptions.BitsPerPixel = 24;

    // Create an instance of FileCreateSource and assign it to Source property
    ImageOptions.Source = new FileCreateSource(dataDir + "sample_1.bmp", false);

    // Create an instance of Image and initialize an instance of Graphics
    using (Image image = Image.Create(ImageOptions, 500, 500))
    {
        Graphics graphics = new Graphics(image);
        graphics.Clear(Color.White);
```

Here we configure a 500 × 500 pixel BMP with a white background, ready for drawing.

## Step 2: Creating GraphicsPath, Adding Shapes and Text

Now we build a `GraphicsPath` that contains both shapes **and the text we want to draw on the image**.

```csharp
        GraphicsPath graphicspath = new GraphicsPath();
        Figure figure = new Figure();

        figure.AddShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
        figure.AddShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
        figure.AddShape(new TextShape("Aspose.Imaging", new RectangleF(170, 225, 170, 100), new Font("Arial", 20), StringFormat.GenericTypographic));

        graphicspath.AddFigures(new[] { figure });
```

- **EllipseShape** and **RectangleShape** let us **draw shapes on image**.  
- **TextShape** is where we **draw text on image** – the string “Aspose.Imaging” will be rendered inside the specified rectangle.

## Step 3: Drawing the Path and Filling with a Hatch Pattern

With the path ready, we outline it using a pen and then fill the interior using a hatch brush—this demonstrates **filling shapes with pattern**.

```csharp
        graphics.DrawPath(new Pen(Color.Blue), graphicspath);

        // Create an instance of HatchBrush and set its properties
        HatchBrush hatchbrush = new HatchBrush();
        hatchbrush.BackgroundColor = Color.Brown;
        hatchbrush.ForegroundColor = Color.Blue;
        hatchbrush.HatchStyle = HatchStyle.Vertical;

        graphics.FillPath(hatchbrush, graphicspath);

        image.Save();
        Console.WriteLine("Processing completed successfully.");
    }
    Console.WriteLine("Finished example DrawingUsingGraphicsPath");
}
```

The `HatchBrush` paints a vertical blue line pattern over a brown background, giving the shapes a distinctive look.

## Common Use Cases

| Scenario | How the code helps |
|----------|--------------------|
| **Badge generation** | Combine a company logo (ellipse), a border (rectangle) and the employee name (text) in one image. |
| **Dynamic charts** | Draw data‑driven shapes and annotate them with values using `TextShape`. |
| **Watermarking** | Render semi‑transparent text over an existing picture and fill a background pattern for subtle branding. |

## Troubleshooting & Tips

- **File paths** – Ensure `dataDir` points to a writable folder; otherwise `FileCreateSource` will throw an exception.  
- **Color contrast** – When using patterned fills, pick foreground/background colors that provide enough contrast for readability.  
- **Performance** – For large images, consider using `RasterImage` instead of `BmpOptions` to reduce memory consumption.

## Frequently Asked Questions

**Q: Is Aspose.Imaging for .NET compatible with the latest .NET frameworks?**  
A: Yes, the library is regularly updated to support .NET 6, .NET 7 and the latest .NET Framework versions.

**Q: Can I convert the drawn image to another format (e.g., PNG or JPEG)?**  
A: Absolutely. After saving the BMP you can load it with `Image.Load` and call `Save` with a different file extension.

**Q: Where can I find more detailed documentation?**  
A: Visit the official docs at [Aspose.Imaging documentation](https://reference.aspose.com/imaging/net/).

**Q: Is a free trial available?**  
A: Yes, you can download a trial version from [here](https://releases.aspose.com/).

**Q: How do I purchase a license for production use?**  
A: Licenses can be bought directly from the Aspose store: [this link](https://purchase.aspose.com/buy).

## Conclusion

You’ve now learned how to **draw text on image**, **draw shapes on image**, and **fill shapes with pattern** using Aspose.Imaging’s `GraphicsPath` API. With these building blocks you can create rich, programmatic graphics for reports, dashboards, or any custom visual output in your .NET applications.

If you run into any issues or want to share your creations, feel free to join the community at the [Aspose.Imaging Forum](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-30  
**Tested With:** Aspose.Imaging 24.12 for .NET  
**Author:** Aspose