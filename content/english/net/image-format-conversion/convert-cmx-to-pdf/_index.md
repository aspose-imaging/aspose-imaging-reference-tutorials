---
title: Convert CMX to PDF in Aspose.Imaging for .NET
linktitle: Convert CMX to PDF in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 13
url: /net/image-format-conversion/convert-cmx-to-pdf/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example CmxToPdfExample");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string inputFile = Path.Combine(dataDir, "MultiPage.cmx");
            using (Aspose.Imaging.FileFormats.Cmx.CmxImage image =
                (Aspose.Imaging.FileFormats.Cmx.CmxImage)Image.Load(inputFile))
            {
                Aspose.Imaging.ImageOptions.PdfOptions options = new PdfOptions();
                options.PdfDocumentInfo = new Aspose.Imaging.FileFormats.Pdf.PdfDocumentInfo();
                // Set rasterization options for fileformat
                options.VectorRasterizationOptions = (Aspose.Imaging.ImageOptions.VectorRasterizationOptions)image.GetDefaultOptions(new object[] { Color.White, image.Width, image.Height });
                options.VectorRasterizationOptions.TextRenderingHint = TextRenderingHint.SingleBitPerPixel;
                options.VectorRasterizationOptions.SmoothingMode = SmoothingMode.None;
                image.Save(dataDir + "MultiPage.pdf", options);
            }
            File.Delete(dataDir + "MultiPage.pdf");
            Console.WriteLine("Finished example CmxToPdfExample");
        }
```
