---
title: DICOM Simple Resizing in Aspose.Imaging for .NET
linktitle: DICOM Simple Resizing in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 19
url: /net/dicom-image-processing/dicom-simple-resizing/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Console.WriteLine("Running example DICOMSimpleResizing");
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image = new DicomImage(fileStream))
            {
                image.Resize(200, 200);
                image.Save(dataDir + "DICOMSimpleResizing_out.bmp", new BmpOptions());
            }
            Console.WriteLine("Finished example DICOMSimpleResizing");
        }
```
