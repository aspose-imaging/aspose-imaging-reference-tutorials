---
title: Raster Image Frame Saving
linktitle: Raster Image Frame Saving
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 19
url: /java/image-conversion-and-optimization/raster-image-frame-saving.html/
---

## Complete Source Code
```java
        
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "ModifyingImages/";
        // Create an instance of TiffImage and load the file from disc
        try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff"))
        {
            // Initialize a variable to keep track of the frames in the image
            int i = 0;
            // Iterate over the tiff frame collection and Save the frame directly on disc in PNG format
            for  (TiffFrame tiffFrame : multiImage.getFrames())
            {
                tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
            }
        }
        
```
