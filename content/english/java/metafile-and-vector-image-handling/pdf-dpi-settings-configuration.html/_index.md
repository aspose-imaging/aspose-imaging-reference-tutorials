---
title: PDF DPI Settings Configuration
linktitle: PDF DPI Settings Configuration
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 13
url: /java/metafile-and-vector-image-handling/pdf-dpi-settings-configuration.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "ModifyingImages/";
        String fileName = "SampleTiff1.tiff";
        String inputFileName = dataDir + fileName;
        String outFileName = "Your Document Directory" + fileName + ".pdf";
        try (Image image = Image.load(inputFileName))
        {
            PdfOptions pdfOptions = new PdfOptions();
            pdfOptions.setPageSize(new SizeF(612, 792));
            image.save(outFileName, pdfOptions);
        }
        
```
