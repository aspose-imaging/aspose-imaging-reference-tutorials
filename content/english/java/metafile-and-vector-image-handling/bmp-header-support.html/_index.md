---
title: BMP Header Support
linktitle: BMP Header Support
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 11
url: /java/metafile-and-vector-image-handling/bmp-header-support.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        Image image = Image.load(dataDir + "test.bmp");
        try
        {
            image.save("Your Document Directory" + "test.bmp.png", new PngOptions());
        }
        finally
        {
            image.dispose();
        }
        
```
