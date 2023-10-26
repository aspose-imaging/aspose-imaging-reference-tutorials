---
title: Convert Raster Images to PDF
linktitle: Convert Raster Images to PDF
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 15
url: /java/document-conversion-and-processing/convert-raster-images-to-pdf.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        String destFilePath = "Your Document Directory" + "transparent_orig.gif.pdf";
        Image image = Image.load(dataDir + "aspose-logo.gif");
        try
        {
            image.save(destFilePath, new PdfOptions());
        }
        finally
        {
            image.dispose();
        }
        
```
