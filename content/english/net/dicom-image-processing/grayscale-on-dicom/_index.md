---
title: Grayscale on DICOM in Aspose.Imaging for .NET
linktitle: Grayscale on DICOM in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 24
url: /net/dicom-image-processing/grayscale-on-dicom/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Console.WriteLine("Running example GrayscalingOnDICOM");
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image = new DicomImage(fileStream))
            {
                // Transform image to its grayscale representation and Save the resultant image.
                image.Grayscale();
                image.Save(dataDir + "GrayscalingOnDICOM_out.bmp", new BmpOptions());
            }
            Console.WriteLine("Finished example GrayscalingOnDICOM");
        }
```
