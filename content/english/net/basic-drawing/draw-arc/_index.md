---
title: Draw Arc in Aspose.Imaging for .NET
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 10
url: /net/basic-drawing/draw-arc/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example DrawingArc");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Creates an instance of FileStream
            using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
            {
                // Create an instance of BmpOptions and set its various properties
                BmpOptions saveOptions = new BmpOptions();
                saveOptions.BitsPerPixel = 32;
                // Set the Source for BmpOptions and create an instance of Image
                saveOptions.Source = new StreamSource(stream);               
                using (Image image = Image.Create(saveOptions, 100, 100))
                {
                    // Create and initialize an instance of Graphics class and clear Graphics surface
                    Graphics graphic = new Graphics(image);
                    graphic.Clear(Color.Yellow);
                    // Draw an arc shape by specifying the Pen object having red black color and coordinates, height, width, start & end angles                 
                    int width = 100;
                    int height = 200;
                    int startAngle = 45;
                    int sweepAngle = 270;
                    // Draw arc to screen and save all changes.
                    graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);
                    image.Save();
                }
                stream.Close();
            }
            Console.WriteLine("Finished example DrawingArc");
        }
```
