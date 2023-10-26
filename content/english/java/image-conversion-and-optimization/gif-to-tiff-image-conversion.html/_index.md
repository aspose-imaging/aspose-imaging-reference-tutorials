---
title: GIF to TIFF Image Conversion
linktitle: GIF to TIFF Image Conversion
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 18
url: /java/image-conversion-and-optimization/gif-to-tiff-image-conversion.html/
---

## Complete Source Code
```java
		
		String dataDir = "Your Document Directory" + "ConvertingImages/";
		// Load a GIF image
		try (Image objImage = Image.load(dataDir + "aspose-logo.gif"))
		{
			// Convert the image to GIF image
			GifImage gif = (GifImage) objImage;
			// iterate through arry of blocks in the GIF image
			IGifBlock[] blocks = gif.getBlocks();
			for (int i = 0; i < blocks.length; i++)
			{
				// Check if gif block is then ignore it
				if (!(blocks[i] instanceof GifFrameBlock))
				{
					continue;
				}
				// convert block to GifFrameBlock class instance
				GifFrameBlock gifBlock = ((GifFrameBlock) (blocks[i]));
				// Create an instance of TIFF Option class
				TiffOptions objTiff = new TiffOptions(TiffExpectedFormat.Default);
				// Save the GIFF block as TIFF image
				gifBlock.save("Your Document Directory" + "asposelogo" + i + "_out.tif", objTiff);
			}
		}
		
```
