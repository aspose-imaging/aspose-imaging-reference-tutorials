---
title: Understanding RGB Color System
linktitle: Understanding RGB Color System
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 17
url: /java/document-conversion-and-processing/understanding-rgb-color-system.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        String sourceFilePath = "testTileDeflate.tif";
        String outputFilePath = "testTileDeflate Cmyk.tif";
        TiffOptions options = new TiffOptions(TiffExpectedFormat.TiffLzwCmyk);
        Image image = Image.load(dataDir + sourceFilePath);
        try
        {
            image.save("Your Document Directory" + outputFilePath, options);
        }
        finally
        {
            image.dispose();
        }
        
```
