---
title: Extract TIFF Frames to BMP Format
linktitle: Extract TIFF Frames to BMP Format
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 13
url: /java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format.html/
---

## Complete Source Code
```java
        
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
        {
            // Create an instance of int to keep track of frames in TiffImage
            int frameCounter = 0;
            // Iterate over the TiffFrames in TiffImage
            for (TiffFrame tiffFrame : multiImage.getFrames())
            {
                multiImage.setActiveFrame(tiffFrame);
                // Load Pixels of TiffFrame into an array of Colors
                Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
                // Create an instance of bmpCreateOptions
                try (BmpOptions bmpCreateOptions = new BmpOptions())
                {
                    bmpCreateOptions.setBitsPerPixel(24);
                    // Set the Source of bmpCreateOptions as FileCreateSource by specifying the location where output will be saved
                    bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
                    // Create a new bmpImage
                    try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
                    {
                        // Save the bmpImage with pixels from TiffFrame
                        bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                        bmpImage.save();
                    }
                }
                frameCounter++;
            }
        }
        
```
