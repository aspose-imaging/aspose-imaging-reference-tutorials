---
title: Convert Various Image Formats to SVG
linktitle: Convert Various Image Formats to SVG
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 16
url: /java/image-conversion-and-optimization/convert-various-image-formats-to-svg.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        Image image = Image.load(dataDir + "mysvg.svg");
        try
        {
            image.save("Your Document Directory" + "yoursvg.svg");
        }
        finally
        {
            image.dispose();
        }
        
```
