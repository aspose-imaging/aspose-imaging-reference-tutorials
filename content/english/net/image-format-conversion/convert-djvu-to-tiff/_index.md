---
title: Convert DJVU to TIFF in Aspose.Imaging for .NET
linktitle: Convert DJVU to TIFF in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 17
url: /net/image-format-conversion/convert-djvu-to-tiff/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example ConvertDjVuToTIFF");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Load a DjVu image
            using (DjvuImage image = (DjvuImage)Image.Load(dataDir + "Sample.djvu"))
            {
                // Create an instance of TiffOptions & use preset options for Black n While with Deflate compression
                TiffOptions exportOptions = new TiffOptions(TiffExpectedFormat.TiffDeflateBw);
                // Initialize the DjvuMultiPageOptions and Call Save method while passing instance of TiffOptions
                exportOptions.MultiPageOptions = new DjvuMultiPageOptions();
                image.Save(dataDir + "ConvertDjVuToTIFFFormat_out.tiff", exportOptions);
            }
            Console.WriteLine("Finished example ConvertDjVuToTIFF");
        }
```
