---
title: OTG File Format Support
linktitle: OTG File Format Support
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 14
url: /java/metafile-and-vector-image-handling/otg-file-format-support.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "OTG/";
        String fileName = "VariousObjectsMultiPage.otg";
        String inputFileName = dataDir + fileName;
        ImageOptionsBase[] options = { new PngOptions(), new PdfOptions() };
        for (ImageOptionsBase item : options)
        {
            String fileExt = item instanceof PngOptions ? ".png" : ".pdf";
            try (Image image = Image.load(inputFileName))
            {
                OtgRasterizationOptions otgRasterizationOptions = new OtgRasterizationOptions();
                otgRasterizationOptions.setPageSize(Size.to_SizeF(image.getSize()));
                item.setVectorRasterizationOptions(otgRasterizationOptions);
                image.save("Your Document Directory" + "output" + fileExt, item);
            }
        }
        
```
