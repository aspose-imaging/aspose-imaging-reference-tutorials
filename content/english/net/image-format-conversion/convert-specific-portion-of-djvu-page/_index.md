---
title: Convert Specific Portion of DJVU Page in Aspose.Imaging for .NET
linktitle: Convert Specific Portion of DJVU Page in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 20
url: /net/image-format-conversion/convert-specific-portion-of-djvu-page/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example ConvertSpecificPortionOfDjVuPage");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Load a DjVu image
            using (DjvuImage image = (DjvuImage)Image.Load(dataDir + "Sample.djvu"))
            {
                // Create an instance of PngOptions and Set ColorType to Grayscale
                PngOptions exportOptions = new PngOptions();
                exportOptions.ColorType = PngColorType.Grayscale;
                // Create an instance of Rectangle and specify the portion on DjVu page
                Rectangle exportArea = new Rectangle(0, 0, 500, 500);
                // Specify the DjVu page index and Initialize an instance of DjvuMultiPageOptions while passing index of DjVu page index and instance of Rectangle covering the area to be exported               
                int exportPageIndex = 2;
                exportOptions.MultiPageOptions = new DjvuMultiPageOptions(exportPageIndex, exportArea);
                image.Save(dataDir + "ConvertSpecificPortionOfDjVuPage_out.djvu", exportOptions);
            }
            Console.WriteLine("Finished example ConvertSpecificPortionOfDjVuPage");
        }
```
