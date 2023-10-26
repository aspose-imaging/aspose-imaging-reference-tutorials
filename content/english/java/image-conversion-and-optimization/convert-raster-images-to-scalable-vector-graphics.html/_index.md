---
title: Convert Raster Images to Scalable Vector Graphics
linktitle: Convert Raster Images to Scalable Vector Graphics
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 13
url: /java/image-conversion-and-optimization/convert-raster-images-to-scalable-vector-graphics.html/
---

## Complete Source Code
```java
        
		String dataDir = "Your Document Directory" + "ConvertingImages/";
        String[] paths = new String[]
                {
                        "butterfly.gif",
                        "33715-cmyk.jpeg",
                        "3.JPG",
                        "test.j2k",
                        "Rings.png",
                        "img4.TIF",
                        "Lossy5.webp"
                };
        for (String path : paths)
        {
            String destPath = "Your Document Directory" + path + ".svg";
            Image image = Image.load(dataDir + path);
            try
            {
                SvgOptions svgOptions = new SvgOptions();
                SvgRasterizationOptions svgRasterizationOptions = new SvgRasterizationOptions();
                svgRasterizationOptions.setPageWidth(image.getWidth());
                svgRasterizationOptions.setPageHeight(image.getHeight());
                svgOptions.setVectorRasterizationOptions(svgRasterizationOptions);
                image.save(destPath, svgOptions);
            }
            finally
            {
                image.dispose();
            }
        }
        
```
