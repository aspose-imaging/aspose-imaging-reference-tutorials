---
title: Median and Wiener Filter Application
linktitle: Median and Wiener Filter Application
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 19
url: /java/image-processing-and-enhancement/median-and-wiener-filter-application.html/
---

## Complete Source Code
```java
		
		// The path to the documents directory.
		String dataDir = "Your Document Directory" + "ConvertingImages/";
		// Load the noisy image 
		try (Image image = Image.load(dataDir + "aspose-logo.gif"))
		{
			// caste the image into RasterImage
			RasterImage rasterImage = (RasterImage) image;
			// Create an instance of MedianFilterOptions class and set the size.
			MedianFilterOptions options = new MedianFilterOptions(4);
			// Apply MedianFilterOptions filter to RasterImage object.
			rasterImage.filter(image.getBounds(), options);
			// Save the resultant image
			image.save("Your Document Directory" + "median_test_denoise_out.gif");
		}
		
```
