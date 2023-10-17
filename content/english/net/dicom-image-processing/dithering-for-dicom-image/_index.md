---
title: Dithering for DICOM Image in Aspose.Imaging for .NET
linktitle: Dithering for DICOM Image in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 22
url: /net/dicom-image-processing/dithering-for-dicom-image/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Console.WriteLine("Running example DitheringForDICOMImage");
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image = new DicomImage(fileStream))
            {
                // Peform Threshold dithering on the image and  Save the resultant image.
                image.Dither(DitheringMethod.ThresholdDithering, 1);               
                image.Save(dataDir + "DitheringForDICOMImage_out.bmp", new BmpOptions());
            }
            Console.WriteLine("Finished example DitheringForDICOMImage");
        }
```
