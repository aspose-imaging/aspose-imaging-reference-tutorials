---
title: Resize SVG Images
linktitle: Resize SVG Images
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 12
url: /java/image-processing-and-enhancement/resize-svg-images.html/
---

## Complete Source Code
```java
        
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "ModifyingImages/";
        String outDir = "Your Document Directory";
        // Load the image
        try (SvgImage image = (SvgImage) Image.load(dataDir + "aspose_logo.svg"))
        {
            image.resize(image.getWidth() * 10, image.getHeight() * 15);
            image.save(outDir + "Logotype_10_15_out.png", new PngOptions()
            {{
                setVectorRasterizationOptions(new SvgRasterizationOptions());
            }});
        }
        
```
