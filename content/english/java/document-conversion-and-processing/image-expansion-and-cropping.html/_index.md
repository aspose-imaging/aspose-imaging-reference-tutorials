---
title: Image Expansion and Cropping
linktitle: Image Expansion and Cropping
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 11
url: /java/document-conversion-and-processing/image-expansion-and-cropping.html/
---

## Complete Source Code
```java
		
        String dataDir = "Your Document Directory" + "ConvertingImages/";
		try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
		{
			// setting for image data to be cashed
			rasterImage.cacheData();
			// Create an instance of Rectangle class and define X,Y and Width, height of the rectangle.
			Rectangle destRect = new Rectangle(200, 200, 300, 300);
			// Save output image by passing output file name, image options and rectangle object.
			rasterImage.save("Your Document Directory" + "ExpandandCropImages_out.jpg", new JpegOptions(), destRect);
		}
		
```
