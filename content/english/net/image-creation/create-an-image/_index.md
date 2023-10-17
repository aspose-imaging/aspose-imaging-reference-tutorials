---
title: Create an Image using Aspose.Imaging for .NET
linktitle: Create an Image using Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 10
url: /net/image-creation/create-an-image/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example CreatingAnImageBySettingPath");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Creates an instance of BmpOptions and set its various properties
            BmpOptions ImageOptions = new BmpOptions();
            ImageOptions.BitsPerPixel = 24;
            // Define the source property for the instance of BmpOptions  Second boolean parameter determines if the file is temporal or not
            ImageOptions.Source = new FileCreateSource(dataDir + "CreatingAnImageBySettingPath_out.bmp", false);
            // Creates an instance of Image and call Create method by passing the BmpOptions object
            using (Image image = Image.Create(ImageOptions, 500, 500))
            {
                image.Save(dataDir + "CreatingAnImageBySettingPath1_out.bmp");
            }
            Console.WriteLine("Finished example CreatingAnImageBySettingPath");
        }
```
