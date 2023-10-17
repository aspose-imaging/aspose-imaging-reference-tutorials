---
title: BMP RLE4 in Aspose.Imaging for .NET
linktitle: BMP RLE4 in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 15
url: /net/advanced-features/bmp-rle4/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example BmpRLE4");
            string dataDir = "Your Document Directory";
            using (Image image = Image.Load(Path.Combine(dataDir,"Rle4.bmp")))
            {
                image.Save(
                    System.IO.Path.Combine(dataDir, "output.bmp"),
                    new BmpOptions()
                        {
                            Compression = BitmapCompression.Rle4,
                            BitsPerPixel = 4,
                            Palette = ColorPaletteHelper.Create4Bit()
                        });
            }
            File.Delete(System.IO.Path.Combine(dataDir, "output.bmp"));
            Console.WriteLine("Finished example BmpRLE4");
        }
```
