---
title: Recovering TIFF Image Data
linktitle: Recovering TIFF Image Data
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 19
url: /java/document-conversion-and-processing/recovering-tiff-image-data.html/
---

## Complete Source Code
```java
        
        // The path to the documents directory.
        String dataDir = "Your Document Directory" + "ModifyingImages/";
        // Create an instance of LoadOptions and set LoadOptions properties
        LoadOptions loadOptions = new LoadOptions();
        loadOptions.setDataRecoveryMode(DataRecoveryMode.ConsistentRecover);
        loadOptions.setDataBackgroundColor(Color.getRed());
        // Create an instance of Image and load a damaged image by passing the instance of LoadOptions
        try (Image image = Image.load(dataDir + "SampleTiff1.tiff", loadOptions))
        {
            // Do some work
        }
        
```
