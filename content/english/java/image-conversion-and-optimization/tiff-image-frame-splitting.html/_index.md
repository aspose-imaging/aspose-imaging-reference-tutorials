---
title: TIFF Image Frame Splitting
linktitle: TIFF Image Frame Splitting
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 21
url: /java/image-conversion-and-optimization/tiff-image-frame-splitting.html/
---

## Complete Source Code
```java
        
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "ModifyingImages/";
        // Create an instance of TiffImage and load the file from disc
        try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff"))
        {
            // Initialize a variable to keep track of the frames in the image, Iterate over the tiff frame collection and Save the image
            int i = 0;
            for (TiffFrame tiffFrame : multiImage.getFrames())
            {
                tiffFrame.save("Your Document Directory" + i + "_out.tiff", new TiffOptions(TiffExpectedFormat.TiffJpegRgb));
            }
        }
        
```
