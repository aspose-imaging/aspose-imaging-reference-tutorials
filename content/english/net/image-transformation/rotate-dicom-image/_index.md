---
title: Rotate DICOM Image in Aspose.Imaging for .NET
linktitle: Rotate DICOM Image in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 11
url: /net/image-transformation/rotate-dicom-image/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Console.WriteLine("Running example RotatingDICOMImage");
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image = new DicomImage(fileStream))
            {               
                image.Rotate(10);
                image.Save(dataDir + "RotatingDICOMImage_out.bmp", new BmpOptions());
            }
            Console.WriteLine("Finished example RotatingDICOMImage");
        }
```
