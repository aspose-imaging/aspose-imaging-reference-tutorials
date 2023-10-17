---
title: Binarization with Fixed Threshold on DICOM Image in Aspose.Imaging for .NET
linktitle: Binarization with Fixed Threshold on DICOM Image in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 15
url: /net/dicom-image-processing/binarization-with-fixed-threshold-on-dicom-image/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Console.WriteLine("Running example BinarizationWithFixedThresholdOnDICOMImage");
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image = new DicomImage(fileStream))
            {
                // Binarize image with predefined fixed threshold and Save the resultant image.
                image.BinarizeFixed(100);
                image.Save(dataDir + "BinarizationWithFixedThresholdOnDICOMImage_out.bmp", new BmpOptions());
            }
            Console.WriteLine("Finished example BinarizationWithFixedThresholdOnDICOMImage");
        }
```
