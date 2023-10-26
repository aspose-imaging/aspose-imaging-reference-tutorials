---
title: Otsu Threshold Binarization
linktitle: Otsu Threshold Binarization
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 22
url: /java/image-processing-and-enhancement/otsu-threshold-binarization.html/
---

## Complete Source Code
```java
		
		// The path to the documents directory.
		String dataDir = "Your Document Directory" + "ConvertingImages/";
		// Load an image in an instance of Image
		try (Image image = Image.load(dataDir + "aspose-logo.jpg"))
		{
			// Cast the image to RasterCachedImage
			RasterCachedImage rasterCachedImage = (RasterCachedImage) image;
			// Check if image is cached
			if (!rasterCachedImage.isCached())
			{
				// Cache image if not already cached
				rasterCachedImage.cacheData();
			}
			// Binarize image with Otsu Thresholding
			rasterCachedImage.binarizeOtsu();
			// Save the resultant image
			rasterCachedImage.save("Your Document Directory" + "BinarizationWithOtsuThreshold_out.jpg");
		}
		
```
