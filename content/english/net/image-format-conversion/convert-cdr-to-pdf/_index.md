---
title: Convert CDR to PDF in Aspose.Imaging for .NET
linktitle: Convert CDR to PDF in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 10
url: /net/image-format-conversion/convert-cdr-to-pdf/
---

## Complete Source Code
```csharp
        private static VectorRasterizationOptions[] CreatePageOptions<TOptions>(VectorMultipageImage image) where TOptions : VectorRasterizationOptions
        { 
            // Create page rasterization options for each page in the image
            return image.Pages.Select(x => x.Size).Select(CreatePageOptions<TOptions>).ToArray();
        }
        private static VectorRasterizationOptions CreatePageOptions<TOptions>(Size pageSize) where TOptions : VectorRasterizationOptions
        {
            // Create the instance of rasterization options
            var options = Activator.CreateInstance<TOptions>();
            // Set the page size
            options.PageSize = pageSize;
            return options;
        }
        public static void Run()
        {
            Console.WriteLine("Running example CdrToPdfExample");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string inputFileName = dataDir + "MultiPage2.cdr";
            using (var image = (VectorMultipageImage)Image.Load(inputFileName))
            {
                // Create page rasterization options
                var pageOptions = CreatePageOptions<CdrRasterizationOptions>(image);
                // Create PDF options
                var options = new PdfOptions { MultiPageOptions = new MultiPageOptions { PageRasterizationOptions = pageOptions } };
                // Export image to PDF format
                image.Save(dataDir + "MultiPage2.cdr.pdf", options);
            }
            File.Delete(dataDir + "MultiPage2.cdr.pdf");
            Console.WriteLine("Finished example CdrToPdfExample");
        }
```
