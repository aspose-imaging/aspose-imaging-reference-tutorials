---
title: Convert CDR to PSD Multipage in Aspose.Imaging for .NET
linktitle: Convert CDR to PSD Multipage in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 12
url: /net/image-format-conversion/convert-cdr-to-psd-multipage/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example CdrToPsdMultipageExample");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string inputFileName = dataDir + "MultiPage.cdr";
            using (Aspose.Imaging.FileFormats.Cdr.CdrImage image = (Aspose.Imaging.FileFormats.Cdr.CdrImage)Image.Load(
                inputFileName)
            )
            {
                ImageOptionsBase options = new Aspose.Imaging.ImageOptions.PsdOptions();
                // By default if image is multipage image all pages exported
                options.MultiPageOptions = new Aspose.Imaging.ImageOptions.MultiPageOptions();
                // Optional parameter that indicates to export multipage image as one
                // layer (page) otherwise it will be exported page to page
                options.MultiPageOptions.MergeLayers = true;
                // Set rasterization options for fileformat
                options.VectorRasterizationOptions = (Aspose.Imaging.ImageOptions.VectorRasterizationOptions)image.GetDefaultOptions(new object[] { Color.White, image.Width, image.Height });
                options.VectorRasterizationOptions.TextRenderingHint = TextRenderingHint.SingleBitPerPixel;
                options.VectorRasterizationOptions.SmoothingMode = SmoothingMode.None;
                image.Save(dataDir + "MultiPageOut.psd", options);
            }
            File.Delete(dataDir + "MultiPageOut.psd");
            Console.WriteLine("Finished example CdrToPsdMultipageExample");
        }
```
