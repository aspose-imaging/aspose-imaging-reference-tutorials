---
title: Convert CMX to PNG in Aspose.Imaging for .NET
linktitle: Convert CMX to PNG in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 14
url: /net/image-format-conversion/convert-cmx-to-png/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example CMXToPNGConversion");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string[] fileNames = new string[] {
             "Rectangle.cmx",
             "Rectangle+Fill.cmx",
             "Ellipse.cmx",
             "Ellipse+fill.cmx",
             "brushes.cmx",
             "outlines.cmx",
             "order.cmx",
             "many_images.cmx",
            };
            foreach (string fileName in fileNames)
            {
                using (Image image = Image.Load(dataDir + fileName))
                {
                    image.Save(
                     dataDir + fileName + ".docpage.png",
                     new PngOptions
                     {
                         VectorRasterizationOptions =
                       new CmxRasterizationOptions()
                       {
                           Positioning = PositioningTypes.DefinedByDocument,
                           SmoothingMode = SmoothingMode.AntiAlias
                       }
                     });
                }
            }
            Console.WriteLine("Finished example CMXToPNGConversion");
        }
```
