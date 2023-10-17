---
title: DICOM Cropping by Shifts in Aspose.Imaging for .NET
linktitle: DICOM Cropping by Shifts in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 18
url: /net/dicom-image-processing/dicom-cropping-by-shifts/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image = new DicomImage(fileStream))
            {
                // Call and supply the four values to Crop method and Save the results to disk
                image.Crop(1, 1, 1, 1);              
                image.Save(dataDir + "DICOMCroppingByShifts_out.bmp", new BmpOptions());
            }
        }
```
