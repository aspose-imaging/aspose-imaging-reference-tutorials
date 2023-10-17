---
title: Adjust Contrast of DICOM Image in Aspose.Imaging for .NET
linktitle: Adjust Contrast of DICOM Image in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 11
url: /net/dicom-image-processing/adjust-contrast-of-dicom-image/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Console.WriteLine("Running example AdjustContrastDicom");
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image = new DicomImage(fileStream))
            {
                // Adjust the contrast and Create an instance of BmpOptions for the resultant image and Save the resultant image
                image.AdjustContrast(50);
                image.Save(dataDir + "AdjustContrastDICOM_out.bmp", new BmpOptions());
            }
            Console.WriteLine("Finished example AdjustContrastDicom");
        }
```
