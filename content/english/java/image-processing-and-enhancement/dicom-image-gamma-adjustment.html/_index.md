---
title: DICOM Image Gamma Adjustment
linktitle: DICOM Image Gamma Adjustment
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 24
url: /java/image-processing-and-enhancement/dicom-image-gamma-adjustment.html/
---

## Complete Source Code
```java
        com.aspose.imaging.examples.
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "dicom/";
        String inputFile = dataDir + "image.dcm";
        String outputFile = dataDir + "AdjustingGamma.bmp";
        File file = new File(inputFile);
        try(FileInputStream fis = new FileInputStream(file);)
        {
            // Load a DICOM image in an instance of DicomImage
            try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(fis))
            {
                // Adjust the gamma
                image.adjustGamma(50);
                // Create an instance of BmpOptions for the resultant image and Save the
                // resultant image
                image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
            }
		}
        catch (IOException ex)
        {
            com.aspose.imaging.examples.Logger.println(ex.getMessage());
            ex.printStackTrace();
        }
        com.aspose.imaging.examples.
```
