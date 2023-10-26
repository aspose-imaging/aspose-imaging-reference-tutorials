---
title: Convert WMF Metafiles to Scalable Vector Graphics
linktitle: Convert WMF Metafiles to Scalable Vector Graphics
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 15
url: /java/image-conversion-and-optimization/convert-wmf-metafiles-to-scalable-vector-graphics.html/
---

## Complete Source Code
```java
        
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "ModifyingImages/";
        // Create an instance of Image class by loading an existing .
        try (Image image = Image.load(dataDir + "input.wmf"))
        {
            // Create an instance of EmfRasterizationOptions class.
            final WmfRasterizationOptions options = new WmfRasterizationOptions();
            options.setPageWidth(image.getWidth());
            options.setPageHeight(image.getHeight());
            // Call save method to convert WMF to SVG format by passing output file name and SvgOptions class instance.
            image.save("Your Document Directory" + "ConvertWMFMetaFileToSVG_out.svg", new SvgOptions() {{ setVectorRasterizationOptions(options); }});
        }
        
```
