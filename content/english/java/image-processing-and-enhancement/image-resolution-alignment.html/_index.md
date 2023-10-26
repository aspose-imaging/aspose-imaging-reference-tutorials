---
title: Image Resolution Alignment
linktitle: Image Resolution Alignment
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 15
url: /java/image-processing-and-enhancement/image-resolution-alignment.html/
---

## Complete Source Code
```java
        
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        try (TiffImage image = (TiffImage) com.aspose.imaging.Image.load(dataDir + "sample.tiff"))
        {
            image.alignResolutions();
            // Save the results to output path.
            image.save("Your Document Directory" + "AligHorizontalAndVeticalResolutions_out.tiff");
            TiffFrame[] frames = image.getFrames();
            for (TiffFrame frame : frames)
            {
                // All resolutions after alignment must be equal
                System.out.println("Horizontal and vertical resolutions are equal:"
                        + ((int) frame.getVerticalResolution() == (int) frame.getHorizontalResolution()));
            }
        }
        
```
