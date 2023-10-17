---
title: Convert DJVU to PDF in Aspose.Imaging for .NET
linktitle: Convert DJVU to PDF in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 16
url: /net/image-format-conversion/convert-djvu-to-pdf/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example ConvertDjVuToPDF");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Load a DjVu image
            using (DjvuImage image = (DjvuImage)Image.Load(dataDir + "Sample.djvu"))
            {
                // Create an instance of PdfOptions and Initialize the metadata for Pdf document
                PdfOptions exportOptions = new PdfOptions();
                exportOptions.PdfDocumentInfo = new PdfDocumentInfo();
                // Create an instance of IntRange and initialize it with the range of DjVu pages to be exported
                IntRange range = new IntRange(0, 5); //Export first 5 pages
                // Initialize an instance of DjvuMultiPageOptions with range of DjVu pages to be exported and Save the result in PDF format
                exportOptions.MultiPageOptions = new DjvuMultiPageOptions(range);
                image.Save(dataDir + "ConvertDjVuToPDFFormat_out.pdf", exportOptions);
            }
            Console.WriteLine("Finished example ConvertDjVuToPDF");
        }
```
