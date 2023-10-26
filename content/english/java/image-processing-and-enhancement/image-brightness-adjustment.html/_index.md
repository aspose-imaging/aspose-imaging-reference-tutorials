---
title: Image Brightness Adjustment
linktitle: Image Brightness Adjustment
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 25
url: /java/image-processing-and-enhancement/image-brightness-adjustment.html/
---

## Complete Source Code
```java
        
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "dicom/";
        String inputFile = dataDir + "image.dcm";
        String outputFile = "Your Document Directory" + "AdjustingBrightness_out.bmp";
        // Load a DICOM image in an instance of DicomImage
        try (DicomImage image = (DicomImage) Image.load(inputFile))
        {
            //yar Image image = Image.load(dataDir + "aspose-logo.dxf");
            // Adjust the brightness
            image.adjustBrightness(50);
            // Create an instance of BmpOptions for the resultant image and Save the
            // resultant image
            image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
        }
        
```
