---
title: Image Expansion or Cropping
linktitle: Image Expansion or Cropping
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 12
url: /java/document-conversion-and-processing/image-expansion-or-cropping.html/
---

## Complete Source Code
```java
        
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        // Load an image in an instance of Image and Setting for image data to be cashed
        try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
        {
            rasterImage.cacheData();
            // Create an instance of Rectangle class and define X,Y and Width, height of the rectangle, and Save output image
            Rectangle destRect = new Rectangle(-200, -200, 300, 300);
            rasterImage.save("Your Document Directory" + "Grayscaling_out.jpg", new JpegOptions(), destRect);
        }
        
```
