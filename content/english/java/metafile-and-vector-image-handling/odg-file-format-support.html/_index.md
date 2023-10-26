---
title: ODG File Format Support
linktitle: ODG File Format Support
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 12
url: /java/metafile-and-vector-image-handling/odg-file-format-support.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        String[] files = new String[] {"example.odg", "example1.odg"};
        final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
        for (String file : files)
        {
            String fileName = dataDir + file;
            try(Image image = Image.load(fileName))
            {
                rasterizationOptions.setPageSize(new SizeF(image.getWidth(), image.getHeight()));
                String outFileName = "Your Document Directory" + file.replace(".odg", ".png");
                image.save(outFileName,  new PngOptions()
                                {{
                                    setVectorRasterizationOptions(rasterizationOptions);
                                }});
                outFileName = "Your Document Directory" + file.replace(".odg", ".pdf");
                image.save(outFileName, new PdfOptions()
                                {{
                                    setVectorRasterizationOptions(rasterizationOptions);
                                }});
            }
        }
        
```
