---
title: Convert SVG to Enhanced Metafile (EMF)
linktitle: Convert SVG to Enhanced Metafile (EMF)
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 15
url: /java/metafile-and-vector-image-handling/convert-svg-to-enhanced-metafile.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        String[] testFiles = new String[]
                {
                        "input.svg",
                        "juanmontoya_lingerie.svg",
                        "rg1024_green_grapes.svg",
                        "sample_car.svg",
                        "tommek_Car.svg"
                };
        String outputPath = Path.combine("Your Document Directory", "output/");
        File dir = new File(outputPath);
        if (!dir.exists() && !dir.mkdirs())
        {
            throw new AssertionError("Can not create output directory!");
        }
        for (String fileName : testFiles)
        {
            String inputFileName = dataDir + fileName;
            String outputFileName = outputPath + fileName + ".emf";
            try (Image image = Image.load(inputFileName))
            {
                image.save(outputFileName, new EmfOptions()
                {{
                    setVectorRasterizationOptions(new SvgRasterizationOptions()
                    {{
                        setPageSize(Size.to_SizeF(image.getSize()));
                    }});
                }});
            }
        }
        
```
