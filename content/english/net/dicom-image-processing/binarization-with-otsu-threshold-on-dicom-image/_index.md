---
title: Binarization with Otsu Threshold on DICOM Image in Aspose.Imaging for .NET
linktitle: Binarization with Otsu Threshold on DICOM Image in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 16
url: /net/dicom-image-processing/binarization-with-otsu-threshold-on-dicom-image/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Console.WriteLine("Running example BinarizationWithOtsuThresholdOnDICOMImage");
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image = new DicomImage(fileStream))
            {
                // Binarize image with Otsu Thresholding and Save the resultant image.
                image.BinarizeOtsu();
                image.Save(dataDir + "BinarizationWithOtsuThresholdOnDICOMImage_out.bmp", new BmpOptions());
            }
            Console.WriteLine("Finished example BinarizationWithOtsuThresholdOnDICOMImage");
        }
```
