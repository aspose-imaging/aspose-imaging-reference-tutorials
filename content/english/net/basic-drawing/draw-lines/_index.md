---
title: Draw Lines in Aspose.Imaging for .NET
linktitle: Draw Lines in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 13
url: /net/basic-drawing/draw-lines/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example DrawingLines");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Creates an instance of FileStream
            using (FileStream stream = new FileStream(dataDir, FileMode.Create))
            {
                // Create an instance of BmpOptions and set its various properties
                BmpOptions saveOptions = new BmpOptions();
                saveOptions.BitsPerPixel = 32;
                saveOptions.Source = new StreamSource(stream);
                // Create an instance of Image
                using (Image image = Image.Create(saveOptions, 100, 100))
                {
                    // Create and initialize an instance of Graphics class and Clear Graphics surface
                    Graphics graphic = new Graphics(image);
                    graphic.Clear(Color.Yellow);
                    // Draw two dotted diagonal lines by specifying the Pen object having blue color and co-ordinate Points
                    graphic.DrawLine(new Pen(Color.Blue), 9, 9, 90, 90);
                    graphic.DrawLine(new Pen(Color.Blue), 9, 90, 90, 9);
                    // Draw a four continuous line by specifying the Pen object having Solid Brush with red color and two point structures
                    graphic.DrawLine(new Pen(new SolidBrush(Color.Red)), new Point(9, 9), new Point(9, 90));
                    graphic.DrawLine(new Pen(new SolidBrush(Color.Aqua)), new Point(9, 90), new Point(90, 90));
                    graphic.DrawLine(new Pen(new SolidBrush(Color.Black)), new Point(90, 90), new Point(90, 9));
                    graphic.DrawLine(new Pen(new SolidBrush(Color.White)), new Point(90, 9), new Point(9, 9));
                    image.Save();
                }
            }
            Console.WriteLine("Finished example DrawingLines");
        }
```
