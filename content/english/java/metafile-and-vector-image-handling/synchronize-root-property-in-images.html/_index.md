---
title: Synchronize Root Property in Images
linktitle: Synchronize Root Property in Images
second_title: Aspose.Imaging Java Image Processing API
description: 
type: docs
weight: 16
url: /java/metafile-and-vector-image-handling/synchronize-root-property-in-images.html/
---

## Complete Source Code
```java
        
        // To get proper output please apply a valid Aspose.Imaging License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx."
        // create new synchronized two-way stream
        com.aspose.imaging.StreamContainer streamContainer = new com.aspose.imaging.StreamContainer(new java.io.ByteArrayInputStream(new byte[0]));
        try
        {
            // check if the access to the stream source is synchronized.
            synchronized (streamContainer.getSyncRoot())
            {
                // do work
                // now access to streamContainer is synchronized
            }
        }
        finally
        {
            streamContainer.dispose();
        }
        
```
