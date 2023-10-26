---
title: JPEG2000 Image Optimization Guide
linktitle: JPEG2000 Image Optimization Guide
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 12
url: /java/image-conversion-and-optimization/jpeg2000-image-optimization-guide.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        String outDir = "Your Document Directory";
        // Setting a memory limit of 10 megabytes for target loaded image
        // JP2 codec
        try (Image image = Image.load(Path.combine(dataDir, "inputFile.jp2"),new LoadOptions() {{ setBufferSizeHint(10); }}))
        {
            image.save(Path.combine(outDir, "outputFile.jp2"));
        }
        // J2K codec
        try (Image image = Image.load(Path.combine(dataDir, "inputFile.j2k"), new LoadOptions() {{ setBufferSizeHint(10); }}))
        {
            image.save(Path.combine(outDir, "outputFile.j2k"));
        }
        // Setting a memory limit of 10 megabytes for target created image
        // JP2 codec
        try(Jpeg2000Options createOptions = new Jpeg2000Options())
        {
            createOptions.setCodec(Jpeg2000Codec.Jp2);
            createOptions.setBufferSizeHint(10);
            createOptions.setSource(new FileCreateSource(Path.combine(outDir, "createdFile.jp2"), false));
            try (Image image = Image.create(createOptions, 1000, 1000))
            {
                image.save(); // save to same location
            }
        }
        // J2K codec
        try(Jpeg2000Options createOptions = new Jpeg2000Options())
        {
            createOptions.setCodec(Jpeg2000Codec.J2K);
            createOptions.setBufferSizeHint(10);
            createOptions.setSource(new FileCreateSource(Path.combine(outDir, "createdFile.j2k"), false));
            try (Image image = Image.create(createOptions, 1000, 1000))
            {
                image.save(); // save to same location
            }
        }
        
```
