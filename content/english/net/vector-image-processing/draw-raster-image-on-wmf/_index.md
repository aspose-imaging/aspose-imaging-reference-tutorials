---
title: Draw Raster Image on WMF in Aspose.Imaging for .NET
linktitle: Draw Raster Image on WMF in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 12
url: /net/vector-image-processing/draw-raster-image-on-wmf/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example DrawRasterImageOnWMF");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Load the image to be drawn
            using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
            {
                // Load the image for drawing on it (drawing surface)
                using (WmfImage canvasImage = (WmfImage)Image.Load(dataDir + "asposenet_222_wmf_200.wmf"))
                {
                    WmfRecorderGraphics2D graphics = WmfRecorderGraphics2D.FromWmfImage(canvasImage);
                    // Draw a rectagular part of the raster image within the specified bounds of the vector image (drawing surface).
                    // Note that because the source size is not equal to the destination one, the drawn image is stretched horizontally and vertically.
                    graphics.DrawImage(
                        imageToDraw,
                        new Rectangle(67, 67, canvasImage.Width, canvasImage.Height),
                        new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
                        GraphicsUnit.Pixel);
                    // Save the result image
                    using (WmfImage resultImage = graphics.EndRecording())
                    {
                        resultImage.Save(dataDir + "asposenet_222_wmf_200.DrawImage.wmf");
                    }
                }
            }
            Console.WriteLine("Finished example DrawRasterImageOnWMF");
        }
```
