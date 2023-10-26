---
title: Monitor Document Conversion Progress
linktitle: Monitor Document Conversion Progress
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 10
url: /java/document-conversion-and-processing/monitor-document-conversion-progress.html/
---

## Complete Source Code
```java
        
        String dataDir = "Your Document Directory" + "ConvertingImages/";
        String fileName = "aspose-logo.jpg";
        String inputFileName = dataDir + fileName;
        // Example of use of separate operation progress event handlers for load/export operations
        try (Image image = Image.load(inputFileName, new LoadOptions()
        {{
            setIProgressEventHandler(new ProgressEventHandler()
            {
                @Override
                public void invoke(ProgressEventHandlerInfo info)
                {
                    progressCallback(info);
                }
            });
        }}))
        {
            image.save(
                    Path.combine("Your Document Directory", "outputFile_Baseline.jpg"),
                    new JpegOptions()
                    {{
                        setCompressionType(JpegCompressionMode.Baseline);
                        setQuality(100);
                        setProgressEventHandler(new ProgressEventHandler()
                        {
                            @Override
                            public void invoke(ProgressEventHandlerInfo info)
                            {
                                exportProgressCallback(info);
                            }
                        });
                    }});
        }
        
    }
    static void progressCallback(ProgressEventHandlerInfo info)
    {
        Logger.printf("Progress %s : %d/%d", info.getEventType(), info.getValue(), info.getMaxValue());
    }
    static void exportProgressCallback(ProgressEventHandlerInfo info)
    {
        Logger.printf("Export event %s : %d/%d", info.getEventType(), info.getValue(), info.getMaxValue());
```
