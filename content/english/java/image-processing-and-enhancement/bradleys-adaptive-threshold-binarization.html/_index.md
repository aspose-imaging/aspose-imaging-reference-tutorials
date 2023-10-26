---
title: Bradley's Adaptive Threshold Binarization
linktitle: Bradley's Adaptive Threshold Binarization
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 27
url: /java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization.html/
---

## Complete Source Code
```java
		
		// The path to the documents directory.
		String dataDir = "Your Document Directory" + "dicom/";
        String inputFile = dataDir + "image.dcm";
        String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
		// Load a DICOM image in an instance of DicomImage
		try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
		{
			// Binarize image with bradley's adaptive threshold.
			image.binarizeBradley(10);
			// Save the resultant image.
			image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
		}
		
```
