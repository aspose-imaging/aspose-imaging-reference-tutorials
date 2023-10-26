---
title: Improve DJVU Image Optimization
linktitle: Improve DJVU Image Optimization
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 11
url: /java/image-conversion-and-optimization/improve-djvu-image-optimization.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        try (DjvuImage image = (DjvuImage) Image.load(Path.combine(dataDir,"test.djvu"), new LoadOptions() {{ setBufferSizeHint(50); }}))
        {
            int pageNum = 0;
            for (Image page : image.getPages())
            {
                page.save(Path.combine("Your Document Directory", "page" + pageNum + ".png"), new PngOptions());
                pageNum++;
            }
        }
        
```
