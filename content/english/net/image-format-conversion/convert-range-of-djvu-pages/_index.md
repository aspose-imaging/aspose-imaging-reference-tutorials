---
title: Convert Range of DJVU Pages in Aspose.Imaging for .NET
linktitle: Convert Range of DJVU Pages in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 18
url: /net/image-format-conversion/convert-range-of-djvu-pages/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example ConvertRangeOfDjVuPages");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Load a DjVu image
            using (DjvuImage image = (DjvuImage)Image.Load(dataDir + "Sample.djvu"))
            {
                // Create an instance of TiffOptions with preset options and IntRange and initialize it with range of pages to be exported
                TiffOptions exportOptions = new TiffOptions(TiffExpectedFormat.TiffDeflateBw);
                IntRange range = new IntRange(0, 2);
                // Initialize an instance of DjvuMultiPageOptions while passing instance of IntRange and  Call Save method while passing instance of TiffOptions
                exportOptions.MultiPageOptions = new DjvuMultiPageOptions(range);
                image.Save(dataDir + "ConvertRangeOfDjVuPages_out.djvu", exportOptions);
            }
            Console.WriteLine("Finished example ConvertRangeOfDjVuPages");
        }
```
