---
title: Draw Bezier Curve in Aspose.Imaging for .NET
linktitle: Draw Bezier Curve in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 11
url: /net/basic-drawing/draw-bezier-curve/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example DrawingBezier");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Creates an instance of FileStream
            using (FileStream stream = new FileStream(dataDir + "DrawingBezier_out.bmp", FileMode.Create))
            {
                // Create an instance of BmpOptions and set its various properties
                BmpOptions saveOptions = new BmpOptions();
                saveOptions.BitsPerPixel = 32;
                // Set the Source for BmpOptions and Create an instance of Image
                saveOptions.Source = new StreamSource(stream);
                using (Image image = Image.Create(saveOptions, 100, 100))
                {
                    // Create and initialize an instance of Graphics class and clear Graphics surface
                    Graphics graphic = new Graphics(image);
                    graphic.Clear(Color.Yellow);
                    // Initializes the instance of PEN class with black color and width
                    Pen BlackPen = new Pen(Color.Black, 3);
                    float startX = 10;
                    float startY = 25;
                    float controlX1 = 20;
                    float controlY1 = 5;
                    float controlX2 = 55;
                    float controlY2 = 10;
                    float endX = 90;
                    float endY = 25;
                    // Draw a Bezier shape by specifying the Pen object having black color and co-ordinate Points and save all changes.
                    graphic.DrawBezier(BlackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
                    image.Save();
                }
            }
            Console.WriteLine("Finished example DrawingBezier");
        }
```
