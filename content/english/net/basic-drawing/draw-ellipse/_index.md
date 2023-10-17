---
title: Draw Ellipse in Aspose.Imaging for .NET
linktitle: Draw Ellipse in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 12
url: /net/basic-drawing/draw-ellipse/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example DrawingEllipse");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Creates an instance of FileStream
            using (FileStream stream = new FileStream(dataDir + "DrawingEllipse_out.bmp", FileMode.Create))
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
                    // Draw a dotted ellipse shape by specifying the Pen object having red color and a surrounding Rectangle
                    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
                    // Draw a continuous ellipse shape by specifying the Pen object having solid brush with blue color and a surrounding Rectangle
                    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
                    image.Save();
                }
                stream.Close();
            }
            Console.WriteLine("Finished example DrawingEllipse");
        }
```
