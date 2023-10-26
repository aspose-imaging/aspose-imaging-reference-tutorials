---
title: Apply Wiener Filter to Images
linktitle: Apply Wiener Filter to Images
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 17
url: /java/image-processing-and-enhancement/apply-wiener-filter-to-images.html/
---

## Complete Source Code
```java
		
		// The path to the documents directory.
		String dataDir = "Your Document Directory" + "ConvertingImages/";
		Image image = Image.load(dataDir + "aspose-logo.gif");
		try
		{
			// caste the image into RasterImage
			RasterImage rasterImage = (RasterImage) image;
			if (rasterImage == null) {
				return;
			}
			// Create an instance of GaussWienerFilterOptions class and set the
			// radius size and smooth value.
			GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
			options.setGrayscale(true);
			// apply MedianFilterOptions filter to RasterImage object.
			rasterImage.filter(image.getBounds(), options);
			// Save the resultant image
			image.save("Your Document Directory" + "ApplyGaussWienerFilter_out.gif");
		}
		finally
		{
			image.close();
		}
		
```
