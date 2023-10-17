---
title: Binarization with Bradley's Adaptive Threshold on DICOM Image in Aspose.Imaging for .NET
linktitle: Binarization with Bradley's Adaptive Threshold on DICOM Image in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 14
url: /net/dicom-image-processing/binarization-with-bradleys-adaptive-threshold-on-dicom-image/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string inputFile = dataDir + "image.dcm";
            Console.WriteLine("Running example BinarizationWithBradleysAdaptiveThreshold");
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image = new DicomImage(fileStream))
            {
                // Binarize image with bradley's adaptive threshold and Save the resultant image.
                image.BinarizeBradley(10);
                image.Save(dataDir + "BinarizationWithBradleysAdaptiveThreshold_out.bmp", new BmpOptions());
            }
            Console.WriteLine("Finished example BinarizationWithBradleysAdaptiveThreshold");
       }
```
