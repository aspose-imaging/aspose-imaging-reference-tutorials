---
title: Apply Wiener Filter to Motion Images
linktitle: Apply Wiener Filter to Motion Images
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 20
url: /java/image-processing-and-enhancement/apply-wiener-filter-to-motion-images.html/
---

## Complete Source Code
```java
		
		// The path to the documents directory.
		String dataDir = "Your Document Directory" + "ConvertingImages/";
		try (Image image = Image.load(dataDir + "aspose-logo.gif"))
		{
			// caste the image into RasterImage
			RasterImage rasterImage = (RasterImage) image;
			// Create an instance of MotionWienerFilterOptions class and set the
			// length, smooth value and angle.
			MotionWienerFilterOptions options = new MotionWienerFilterOptions(50, 9, 90);
			options.setGrayscale(true);
			// apply MedianFilterOptions filter to RasterImage object.
			rasterImage.filter(image.getBounds(), options);
			// Save the resultant image
			image.save("Your Document Directory" + "ApplyingMotionWienerFilter_out.gif");
		}
		
```
