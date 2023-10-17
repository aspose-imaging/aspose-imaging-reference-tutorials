---
title: Draw Rectangle in Aspose.Imaging for .NET
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 14
url: /net/basic-drawing/draw-rectangle/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example DrawingRectangle");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Creates an instance of FileStream
            using (FileStream stream = new FileStream(dataDir, FileMode.Create))
            {
                // Create an instance of BmpOptions and set its various properties
                BmpOptions saveOptions = new BmpOptions();
                saveOptions.BitsPerPixel = 32;
                // Set the Source for BmpOptions and Create an instance of Image
                saveOptions.Source = new StreamSource(stream);
                using (Image image = Image.Create(saveOptions, 100, 100))
                {
                    // Create and initialize an instance of Graphics class,  Clear Graphics surface, Draw a rectangle shapes and  save all changes.
                    Graphics graphic = new Graphics(image);
                    graphic.Clear(Color.Yellow);
                    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
                    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
                    image.Save();
                }
            }
            Console.WriteLine("Finished example DrawingRectangle");
        }
```
