---
title: Support of CDR Format in Aspose.Imaging for .NET
linktitle: Support of CDR Format in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 13
url: /net/advanced-features/support-of-cdr-format/
---

## Complete Source Code
```csharp
        public static void Run() {
            Console.WriteLine("Running example SupportOfCDR");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string inputFileName = dataDir + "test.cdr";
            FileFormat expectedFileFormat = FileFormat.Cdr;
            using (Image image = Image.Load(inputFileName))
            {
                if (expectedFileFormat != image.FileFormat)
                {
                    throw new Exception("Image FileFormat is not {expectedFileFormat}");
                }
            }
            Console.WriteLine("Finished example SupportOfCDR");
        }
```
