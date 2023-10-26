---
title: Convert SVG Images to Raster Format
linktitle: Convert SVG Images to Raster Format
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 14
url: /java/image-conversion-and-optimization/convert-svg-images-to-raster-format.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        // Load the image
        try(SvgImage image = (SvgImage) Image.load(dataDir + "aspose-logo.Svg"))
        {
            // Create an instance of PNG options
            PngOptions pngOptions = new PngOptions();
            // Save the results to disk
            image.save("Your Document Directory" + "ConvertingSVGToRasterImages_out.png", pngOptions);
        }
        
```
