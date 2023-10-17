---
title: BigTiff Load Example in Aspose.Imaging for .NET
linktitle: BigTiff Load Example in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 14
url: /net/advanced-features/bigtiff-load-example/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example BigTiffLoadExample");
            string dataDir = "Your Document Directory";
            string fileName = "input-BigTiff.tif";
            string inputFilePath = Path.Combine(dataDir, fileName);
            string outputFilePath = Path.Combine(dataDir, "result.tiff");
            using (var image = Image.Load(inputFilePath) as BigTiffImage)
            {
                image.Save(outputFilePath, new BigTiffOptions(TiffExpectedFormat.TiffLzwRgba));
            }
            File.Delete(outputFilePath);
            Console.WriteLine("Finished example BigTiffLoadExample");
        }
```
