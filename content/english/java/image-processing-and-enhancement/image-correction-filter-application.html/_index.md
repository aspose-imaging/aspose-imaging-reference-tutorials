---
title: Image Correction Filter Application
linktitle: Image Correction Filter Application
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 16
url: /java/image-processing-and-enhancement/image-correction-filter-application.html/
---

## Complete Source Code
```java
		
		// The path to the documents directory.
		String dataDir = "Your Document Directory" + "ConvertingImages/";
		try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "aspose-logo.jpg"))
		{
			// Get Bounds[rectangle] of image.
			com.aspose.imaging.Rectangle rect = rasterImage.getBounds();
			// Create an instance of BilateralSmoothingFilterOptions class with size
			// parameter.
			com.aspose.imaging.imagefilters.filteroptions.BilateralSmoothingFilterOptions bilateralOptions =
					new com.aspose.imaging.imagefilters.filteroptions.BilateralSmoothingFilterOptions(3);
			// Create an instance of SharpenFilterOptions class.
			com.aspose.imaging.imagefilters.filteroptions.SharpenFilterOptions sharpenOptions = new com.aspose.imaging.imagefilters.filteroptions.SharpenFilterOptions();
			// Supply the filters to raster image.
			rasterImage.filter(rect, bilateralOptions);
			rasterImage.filter(rect, sharpenOptions);
			// Adjust the contrast accordingly.
			rasterImage.adjustContrast(-10);
			// Set brightness using Binarize Bradley
			rasterImage.binarizeBradley(80);
			// Save the results to output path.
			rasterImage.save("Your Document Directory" + "a1_out.jpg");
		}
		
```
