---
title: Draw Raster Image on SVG in Aspose.Imaging for .NET
linktitle: Draw Raster Image on SVG in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 11
url: /net/vector-image-processing/draw-raster-image-on-svg/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example DrawRasterImageOnSVG");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Load the image to be drawn
            using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
            {
                // Load the image for drawing on it (drawing surface)
                using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
                {
                    // Drawing on an existing Svg image.
                    Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
                        new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(canvasImage);
                    // Draw a rectagular part of the raster image within the specified bounds of the vector image (drawing surface).
                    // Note that because the source size is equal to the destination one, the drawn image is not stretched.
                    graphics.DrawImage(
                        new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
                        new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
                        imageToDraw);
                    // Save the result image
                    using (SvgImage resultImage = graphics.EndRecording())
                    {
                        resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
                    }
                }
            }
            Console.WriteLine("Finished example DrawRasterImageOnSVG");
        }
```
