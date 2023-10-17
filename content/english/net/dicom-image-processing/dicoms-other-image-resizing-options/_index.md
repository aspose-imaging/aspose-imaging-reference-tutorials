---
title: DICOM's Other Image Resizing Options in Aspose.Imaging for .NET
linktitle: DICOM's Other Image Resizing Options in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 20
url: /net/dicom-image-processing/dicoms-other-image-resizing-options/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Console.WriteLine("Running example DICOMSOtherImageResizingOptions");
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image = new DicomImage(fileStream))
            {
                image.ResizeHeightProportionally(100, ResizeType.AdaptiveResample);
                image.Save(dataDir + "DICOMSOtherImageResizingOptions_out.bmp", new BmpOptions());
            }
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image1 = new DicomImage(fileStream))
            {
                image1.ResizeWidthProportionally(150, ResizeType.AdaptiveResample);
                image1.Save(dataDir + "DICOMSOtherImageResizingOptions1_out.bmp", new BmpOptions());
            }
            Console.WriteLine("Finished example DICOMSOtherImageResizingOptions");
        }
```
