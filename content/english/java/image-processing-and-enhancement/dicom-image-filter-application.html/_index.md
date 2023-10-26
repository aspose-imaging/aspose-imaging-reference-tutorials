---
title: DICOM Image Filter Application
linktitle: DICOM Image Filter Application
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 26
url: /java/image-processing-and-enhancement/dicom-image-filter-application.html/
---

## Complete Source Code
```java
        
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "dicom/";
        String inputFile = dataDir + "image.dcm";
        String outputFile = "Your Document Directory" + "ApplyFilterOnDICOMImage_out.bmp";
        File file = new File(inputFile);
        try(FileInputStream fis = new FileInputStream(file))
        {
            // Load a DICOM image in an instance of DicomImage
            try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(fis))
            {
                // Supply the filters to DICOM image.
                image.filter(image.getBounds(), new com.aspose.imaging.imagefilters.filteroptions.MedianFilterOptions(8));
                // Save the results to output path.
                image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
            }
		}
        catch (IOException ex)
        {
            Logger.println(ex.getMessage());
            ex.printStackTrace();
        }
        
```
