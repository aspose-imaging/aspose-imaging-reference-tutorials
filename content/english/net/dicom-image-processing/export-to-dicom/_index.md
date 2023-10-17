---
title: Export to DICOM in Aspose.Imaging for .NET
linktitle: Export to DICOM in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 23
url: /net/dicom-image-processing/export-to-dicom/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example ExportToDicom");
            string dataDir = "Your Document Directory";
            string fileName = "sample.jpg";
            string inputFileNameSingle = Path.Combine(dataDir, fileName);
            string inputFileNameMultipage = Path.Combine(dataDir, "multipage.tif");
            string outputFileNameSingleDcm = Path.Combine(dataDir, "output.dcm");
            string outputFileNameMultipageDcm = Path.Combine(dataDir, "outputMultipage.dcm");
            // The next code sample converts JPEG image to DICOM file format
            using (var image = Image.Load(inputFileNameSingle))
            {
                image.Save(outputFileNameSingleDcm, new DicomOptions());
            }
            // DICOM format supports multipage images. You can convert GIF or TIFF images to DICOM in the same way as JPEG images
            using (var image = Image.Load(inputFileNameMultipage))
            {
                image.Save(outputFileNameMultipageDcm, new DicomOptions());
            }            
            Console.WriteLine("Finished example ExportToDicom");
        }
```
