---
title: Convert CDR to PNG in Aspose.Imaging for .NET
linktitle: Convert CDR to PNG in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 11
url: /net/image-format-conversion/convert-cdr-to-png/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example CdrToPngExample");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string inputFileName = dataDir + "SimpleShapes.cdr";
            using (Aspose.Imaging.FileFormats.Cdr.CdrImage image = (Aspose.Imaging.FileFormats.Cdr.CdrImage)Image.Load(
                inputFileName)
            )
            {
                PngOptions options = new Aspose.Imaging.ImageOptions.PngOptions();
                options.ColorType = Aspose.Imaging.FileFormats.Png.PngColorType.TruecolorWithAlpha;
                // Set rasterization options for fileformat
                options.VectorRasterizationOptions = (Aspose.Imaging.ImageOptions.VectorRasterizationOptions)image.GetDefaultOptions(new object[] { Color.White, image.Width, image.Height });
                options.VectorRasterizationOptions.TextRenderingHint = TextRenderingHint.SingleBitPerPixel;
                options.VectorRasterizationOptions.SmoothingMode = SmoothingMode.None;
                image.Save(dataDir + "SimpleShapes.png", options);
            }
            File.Delete(dataDir + "SimpleShapes.png");
            Console.WriteLine("Finished example CdrToPngExample");
        }
```
