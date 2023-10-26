---
title: XMP Data Handling in Images
linktitle: XMP Data Handling in Images
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 16
url: /java/document-conversion-and-processing/xmp-data-handling-in-images.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        // Specify the size of image by defining a Rectangle
        Rectangle rect = new Rectangle(0, 0, 100, 200);
        TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
        tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
        tiffOptions.setBitsPerSample(new int[] { 8 });
        // create the brand new image just for sample purposes
        try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
        {
            // create an instance of XMP-Header
            XmpHeaderPi xmpHeader = new XmpHeaderPi();
            xmpHeader.setGuid(dataDir);
            // create an instance of Xmp-TrailerPi
            XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
            // create an instance of XMP meta class to set different attributes
            XmpMeta xmpMeta = new XmpMeta();
            xmpMeta.addAttribute("Author", "Mr Smith");
            xmpMeta.addAttribute("Description", "The fake metadata value");
            // create an instance of XmpPacketWrapper that contains all metadata
            XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
            // create an instance of Photoshop package and set photoshop attributes
            PhotoshopPackage photoshopPackage = new PhotoshopPackage();
            photoshopPackage.setCity("London");
            photoshopPackage.setCountry("England");
            photoshopPackage.setColorMode(ColorMode.Rgb);
            // add photoshop package into XMP metadata
            xmpData.addPackage(photoshopPackage);
            // create an instance of DublinCore package and set dublinCore attributes
            DublinCorePackage dublinCorePackage = new DublinCorePackage();
            dublinCorePackage.setAuthor("Charles Bukowski");
            dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
            dublinCorePackage.addValue("dc:movie", "Barfly");
            // add dublinCore Package into XMP metadata
            xmpData.addPackage(dublinCorePackage);
            ByteArrayOutputStream ms = new ByteArrayOutputStream();
            // update XMP metadata into image
            image.setXmpData(xmpData);
            // Save image on the disk or in memory stream
            image.save(ms);
            // Load the image from memory stream or from disk to read/get the metadata
            try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
            {
                // Getting the XMP metadata
                XmpPacketWrapper imgXmpData = img.getXmpData();
                for (XmpPackage pack : imgXmpData.getPackages())
                {
                    // Use package data ...
                }
            }
        }
        
```
