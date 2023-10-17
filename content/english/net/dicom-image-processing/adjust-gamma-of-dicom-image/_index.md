---
title: Adjust Gamma of DICOM Image in Aspose.Imaging for .NET
linktitle: Adjust Gamma of DICOM Image in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 12
url: /net/dicom-image-processing/adjust-gamma-of-dicom-image/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Console.WriteLine("Running example AdjustGammaDicom");
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image = new DicomImage(fileStream))
            {
                // Adjust the gamma and Create an instance of BmpOptions for the resultant image and Save the resultant image
                image.AdjustGamma(50);
                image.Save(dataDir + "AdjustGammaDICOM_out.bmp", new BmpOptions());
            }
            Console.WriteLine("Finished example AdjustGammaDicom");
        }
```