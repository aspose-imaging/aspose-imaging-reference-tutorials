---
title: Flip DICOM Image in Aspose.Imaging for .NET
linktitle: Flip DICOM Image in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 10
url: /net/image-transformation/flip-dicom-image/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Console.WriteLine("Running example FlipDICOMImage");
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image = new DicomImage(fileStream))
            {
                // Flip Image & Save the resultant image.
                image.RotateFlip(RotateFlipType.Rotate180FlipNone);
                image.Save(dataDir + "FlipDICOMImage_out.bmp", new BmpOptions());
            }
            Console.WriteLine("Finished example FlipDICOMImage");
        }
```
