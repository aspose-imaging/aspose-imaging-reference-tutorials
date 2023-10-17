---
title: Pantone Goe Coated Palette in Aspose.Imaging for .NET
linktitle: Pantone Goe Coated Palette in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 12
url: /net/advanced-features/pantone-goe-coated-palette/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example PantoneGoeCoatedPalette");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string inputFileName = dataDir + "test2.cdr";
            using (var image = (CdrImage)Image.Load(inputFileName))
            {
                image.Save(Path.Combine(dataDir,"result.png") , new PngOptions()
                                        {
                                            VectorRasterizationOptions = new CdrRasterizationOptions
                                                                             {
                                                                                 Positioning = PositioningTypes.Relative
                                                                             }
                                        });
            }
            File.Delete(dataDir + "result.png");
            Console.WriteLine("Finished example PantoneGoeCoatedPalette");
        }
```
