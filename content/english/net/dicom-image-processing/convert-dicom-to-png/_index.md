---
title: Convert DICOM to PNG in Aspose.Imaging for .NET
linktitle: Convert DICOM to PNG in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 21
url: /net/dicom-image-processing/convert-dicom-to-png/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example DicomToPngExample");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string inputFile = Path.Combine(dataDir, "MultiframePage1.dicom");
            using (Aspose.Imaging.FileFormats.Dicom.DicomImage image =
                (Aspose.Imaging.FileFormats.Dicom.DicomImage)Image.Load(inputFile))
            {
                PngOptions options = new PngOptions();
                image.Save(dataDir + @"MultiframePage1.png", options);
            }
            File.Delete(dataDir + "MultiframePage1.png");
            Console.WriteLine("Finished example DicomToPngExample");
        }
```
