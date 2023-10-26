---
title: Raster Image TIFF Conversion
linktitle: Raster Image TIFF Conversion
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 20
url: /java/image-conversion-and-optimization/raster-image-tiff-conversion.html/
---

## Complete Source Code
```java
        
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "ModifyingImages/";
        // Create an instance of TiffOptions and set its various properties
        TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
        options.setBitsPerSample(new int[] { 8, 8, 8 });
        options.setPhotometric(TiffPhotometrics.Rgb);
        options.setXresolution(new TiffRational(72));
        options.setYresolution(new TiffRational(72));
        options.setResolutionUnit(TiffResolutionUnits.Inch);
        options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);
        // Set the Compression to AdobeDeflate
        options.setCompression(TiffCompressions.AdobeDeflate);
        // Or Deflate
        // Options.Compression = TiffCompressions.Deflate;
        // Load an existing image in an instance of RasterImage
        try (RasterImage image = (RasterImage) Image.load(dataDir + "SampleTiff1.tiff"))
        {
            // Create a new TiffImage from the RasterImage and Save the resultant image while passing the instance of TiffOptions
            try (TiffImage tiffImage = new TiffImage(new TiffFrame(image)))
            {
                tiffImage.save("Your Document Directory" + "SavingRasterImage_out.tiff", options);
            }
        }
        
```
