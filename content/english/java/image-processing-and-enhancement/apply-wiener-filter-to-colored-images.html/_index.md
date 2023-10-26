---
title: Apply Wiener Filter to Colored Images
linktitle: Apply Wiener Filter to Colored Images
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 18
url: /java/image-processing-and-enhancement/apply-wiener-filter-to-colored-images.html/
---

## Complete Source Code
```java
		
		// The path to the documents directory.
		String dataDir = "Your Document Directory" + "ConvertingImages/";
		try (Image image = Image.load(dataDir + "aspose-logo.gif"))
		{
			// caste the image into RasterImage
			RasterImage rasterImage = (RasterImage) image;
			// Create an instance of GaussWienerFilterOptions class and set the
			// radius size and smooth value.
			GaussWienerFilterOptions options = new GaussWienerFilterOptions(5, 1.5);
			options.setBrightness(1);
			// apply MedianFilterOptions filter to RasterImage object.
			rasterImage.filter(image.getBounds(), options);
			// Save the resultant image
			image.save("Your Document Directory" + "ApplyGaussWienerFilter_out.gif");
		}
		
```
