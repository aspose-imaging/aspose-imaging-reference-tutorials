---
title: Apply Filter on DICOM Image in Aspose.Imaging for .NET
linktitle: Apply Filter on DICOM Image in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 13
url: /net/dicom-image-processing/apply-filter-on-dicom-image/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Console.WriteLine("Running example ApplyFilterDicom");
            using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
            using (DicomImage image = new DicomImage(fileStream))
            {
                // Supply the filters to DICOM image and Save the results to output path.
                image.Filter(image.Bounds, new MedianFilterOptions(8));
                image.Save(dataDir + "ApplyFilterOnDICOMImage_out.bmp", new BmpOptions());
            }
            Console.WriteLine("Finished example ApplyFilterDicom");
        }
```
