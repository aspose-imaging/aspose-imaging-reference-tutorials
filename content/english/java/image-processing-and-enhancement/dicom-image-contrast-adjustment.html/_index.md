---
title: DICOM Image Contrast Adjustment
linktitle: DICOM Image Contrast Adjustment
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 23
url: /java/image-processing-and-enhancement/dicom-image-contrast-adjustment.html/
---

## Complete Source Code
```java
        
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "dicom/";
        String inputFile = dataDir + "image.dcm";
        String outputFile = "Your Document Directory" + "AdjustingContrast_out.bmp";
        // Load a DICOM image in an instance of DicomImage
        File file = new File(inputFile);
        try(FileInputStream fis = new FileInputStream(file))
        {
            // Load a DICOM image in an instance of DicomImage
            try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(fis))
            {
                // Adjust the contrast
                image.adjustContrast(50);
                // Create an instance of BmpOptions for the resultant image and Save the
                // resultant image
                image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
            }
        }
        catch (IOException ex)
        {
            Logger.println(ex.getMessage());
            ex.printStackTrace();
        }
        
```
