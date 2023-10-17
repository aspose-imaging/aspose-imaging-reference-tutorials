---
title: Convert Range of DJVU Pages to Separate Images in Aspose.Imaging for .NET
linktitle: Convert Range of DJVU Pages to Separate Images in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 19
url: /net/image-format-conversion/convert-range-of-djvu-pages-to-separate-images/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example ConvertRangeOfDjVuPagesToSeparateImages");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Load a DjVu image
            using (DjvuImage image = (DjvuImage)Image.Load(dataDir + "Sample.djvu"))
            {
                // Create an instance of BmpOptions and Set BitsPerPixel for resultant images
                BmpOptions exportOptions = new BmpOptions();
                exportOptions.BitsPerPixel = 32;
                // Create an instance of IntRange and initialize it with range of pages to be exported
                IntRange range = new IntRange(0, 2);
                int counter = 0;
                foreach (var i in range.Range)
                {
                    // Save each page in separate file, as BMP do not support layering
                    exportOptions.MultiPageOptions = new DjvuMultiPageOptions(range.GetArrayOneItemFromIndex(counter));
                    image.Save(dataDir + string.Format("{0}_out.bmp", counter++), exportOptions);
                }
            }
            Console.WriteLine("Finished example ConvertRangeOfDjVuPagesToSeparateImages");
        }
```
