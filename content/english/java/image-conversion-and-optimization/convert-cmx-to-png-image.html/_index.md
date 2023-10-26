---
title: Convert CMX to PNG Image
linktitle: Convert CMX to PNG Image
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 10
url: /java/image-conversion-and-optimization/convert-cmx-to-png-image.html/
---

## Complete Source Code
```java
        
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "CMX/";
        // Example of exporting the entire document page
        String[] fileNames = new String[] {
         "Rectangle.cmx",
         "Rectangle+Fill.cmx",
         "Ellipse.cmx",
         "Ellipse+fill.cmx",
         "brushes.cmx",
         "outlines.cmx",
         "order.cmx",
         "many_images.cmx",
        };
        for (String fileName: fileNames) {
            try (Image image = Image.load(dataDir + fileName))
            {
                CmxRasterizationOptions cmxRasterizationOptions = new CmxRasterizationOptions();
                cmxRasterizationOptions.setPositioning(PositioningTypes.DefinedByDocument);
                cmxRasterizationOptions.setSmoothingMode(SmoothingMode.AntiAlias);
                PngOptions options = new PngOptions();
                options.setVectorRasterizationOptions(cmxRasterizationOptions);
                image.save("Your Document Directory" + fileName + ".docpage.png", options);
            }
        }
        
```
