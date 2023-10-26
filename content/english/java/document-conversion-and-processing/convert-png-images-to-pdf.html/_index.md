---
title: Convert PNG Images to PDF
linktitle: Convert PNG Images to PDF
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 14
url: /java/document-conversion-and-processing/convert-png-images-to-pdf.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "Png/";
        try (PngImage pngImage = (PngImage) Image.load(dataDir + "aspose_logo.png"))
        {
            PdfOptions exportOptions = new PdfOptions();
            exportOptions.setPdfDocumentInfo(new PdfDocumentInfo());
            pngImage.save(dataDir + "multipage_specificColor_.djvu4_ethalon.pdf", exportOptions);
        }
        
```
