---
title: Add Image Alpha Blending
linktitle: Add Image Alpha Blending
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 13
url: /java/image-processing-and-enhancement/add-image-alpha-blending.html/
---

## Complete Source Code
```java
        Logger.startExample();
        // The path to the documents' directory.
        String dataDir = "Your Document Directory" + "Png/";
        String outDir = Utils.getOutDir("Png");
        try (RasterImage background = (RasterImage) Image.load(dataDir + "image0.png"))
        {
            try (RasterImage overlay = (RasterImage) Image.load(dataDir + "aspose_logo.png"))
            {
                Point center = new Point((background.getWidth() - overlay.getWidth()) / 2,
                        (background.getHeight() - overlay.getHeight()) / 2);
                background.blend(center, overlay, overlay.getBounds(), (byte) 127);
                background.save(outDir + "/blended.png");
            }
        }
        Utils.deleteFile(outDir + "/blended.png");
        
```
