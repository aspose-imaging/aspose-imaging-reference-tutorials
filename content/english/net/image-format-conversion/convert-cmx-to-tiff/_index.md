---
title: Convert CMX to TIFF in Aspose.Imaging for .NET
linktitle: Convert CMX to TIFF in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 15
url: /net/image-format-conversion/convert-cmx-to-tiff/
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
            Console.WriteLine("Running example CmxToTiffExample");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string inputFile = Path.Combine(dataDir, "MultiPage2.cmx");
            using (var image = (VectorMultipageImage)Image.Load(inputFile))
            {
                // Create page rasterization options
                var pageOptions = CreatePageOptions<CmxRasterizationOptions>(image);
                // Create TIFF options
                var options = new TiffOptions(TiffExpectedFormat.TiffDeflateRgb) { MultiPageOptions = new MultiPageOptions { PageRasterizationOptions = pageOptions } };
                // Export image to TIFF format
                image.Save(dataDir + "MultiPage2.cmx.tiff", options);
            }
            File.Delete(dataDir + "MultiPage2.cmx.tiff");
            Console.WriteLine("Finished example CmxToTiffExample");
        }
```
