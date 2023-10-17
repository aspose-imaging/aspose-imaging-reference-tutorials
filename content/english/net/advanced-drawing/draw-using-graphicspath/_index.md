---
title: Draw Using GraphicsPath in Aspose.Imaging for .NET
linktitle: Draw Using GraphicsPath in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 11
url: /net/advanced-drawing/draw-using-graphicspath/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example DrawingUsingGraphicsPath");
            // The path to the documents directory.
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
                // Create an instance of GraphicsPath and Instance of Figure, add EllipseShape, RectangleShape and TextShape to the figure
                GraphicsPath graphicspath = new GraphicsPath();
                Figure figure = new Figure();
                figure.AddShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
                figure.AddShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
                figure.AddShape(new TextShape("Aspose.Imaging", new RectangleF(170, 225, 170, 100), new Font("Arial", 20), StringFormat.GenericTypographic));
                graphicspath.AddFigures(new[] { figure });
                graphics.DrawPath(new Pen(Color.Blue), graphicspath);
                // Create an instance of HatchBrush and set its properties also Fill path by supplying the brush and GraphicsPath objects
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
