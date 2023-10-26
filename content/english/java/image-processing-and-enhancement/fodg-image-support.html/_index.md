---
title: FODG Image Support
linktitle: FODG Image Support
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 11
url: /java/image-processing-and-enhancement/fodg-image-support.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "otg/";
        String outDir = "Your Document Directory";
        String inputFile = dataDir + "sample.fodg";
        String outputFile = outDir + "sample.fodg.png";
        try (Image image = Image.load(inputFile))
        {
            OdgRasterizationOptions vector = new OdgRasterizationOptions();
            vector.setPageSize(Size.to_SizeF(image.getSize()));
            PngOptions options = new PngOptions();
            options.setVectorRasterizationOptions(vector);
            image.save(outputFile, options);
        }
        
```
