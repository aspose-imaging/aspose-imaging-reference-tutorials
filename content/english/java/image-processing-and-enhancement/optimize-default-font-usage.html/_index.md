---
title: Optimize Default Font Usage
linktitle: Optimize Default Font Usage
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 10
url: /java/image-processing-and-enhancement/optimize-default-font-usage.html/
---

## Complete Source Code
```java
        Logger.startExample();
        String dataDir = "Your Document Directory" + "otg/";
        String outDir = Utils.getOutDir("DefaultFontUsageImprove");
        FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
        FontSettings.setGetSystemAlternativeFont(false);
        exportToPng(Path.combine(dataDir, "missing-font2.odg"), "Arial", Path.combine(outDir, "arial.png"));
        exportToPng(
                Path.combine(dataDir, "missing-font2.odg"),
                "Courier New",
                Path.combine(outDir, "courier.png"));
        
    }
    private static void exportToPng(String filePath, String defaultFontName, String outfileName)
    {
        FontSettings.setDefaultFontName(defaultFontName);
        try (com.aspose.imaging.Image document = com.aspose.imaging.Image.load(filePath))
        {
            PngOptions saveOptions = new PngOptions();
            final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
            rasterizationOptions.setPageWidth(1000);
            rasterizationOptions.setPageHeight(1000);
            saveOptions.setVectorRasterizationOptions(rasterizationOptions);
            document.save(outfileName, saveOptions);
        }
        Utils.deleteFile(outfileName);
```
