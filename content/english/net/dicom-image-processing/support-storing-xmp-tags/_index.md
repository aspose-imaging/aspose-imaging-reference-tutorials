---
title: Support Storing XMP Tags in Aspose.Imaging for .NET
linktitle: Support Storing XMP Tags in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 25
url: /net/dicom-image-processing/support-storing-xmp-tags/
---

## Complete Source Code
```csharp
        public static void Run()
        {           
            string dataDir = "Your Document Directory";
            Console.WriteLine("Running example SupportStoringXmpTags");
            using (DicomImage image = (DicomImage)Image.Load(dataDir + "file.dcm"))
            {
                XmpPacketWrapper xmpPacketWrapper = new XmpPacketWrapper();
                DicomPackage dicomPackage = new DicomPackage();
                dicomPackage.SetEquipmentInstitution("Test Institution");
                dicomPackage.SetEquipmentManufacturer("Test Manufacturer");
                dicomPackage.SetPatientBirthDate("19010101");
                dicomPackage.SetPatientId("010101");
                dicomPackage.SetPatientName("Test Name");
                dicomPackage.SetPatientSex("M");
                dicomPackage.SetSeriesDateTime("19020202");
                dicomPackage.SetSeriesDescription("Test Series Description");
                dicomPackage.SetSeriesModality("Test Modality");
                dicomPackage.SetSeriesNumber("01");
                dicomPackage.SetStudyDateTime("19030303");
                dicomPackage.SetStudyDescription("Test Study Description");
                dicomPackage.SetStudyId("02");
                dicomPackage.SetStudyPhysician("Test Physician");
                xmpPacketWrapper.AddPackage(dicomPackage);
                string outputFile = dataDir + "output.dcm";
                image.Save(outputFile, new DicomOptions() { XmpData = xmpPacketWrapper });
                using (DicomImage imageSaved = (DicomImage)Image.Load(outputFile))
                {
                    List<string> originalDicomInfo = image.FileInfo.DicomInfo;
                    List<string> imageSavedDicomInfo = imageSaved.FileInfo.DicomInfo;
                    int tagsCountDiff = Math.Abs(imageSavedDicomInfo.Count - originalDicomInfo.Count);
                }
                File.Delete(outputFile);
            }
            Console.WriteLine("Finished example SupportStoringXmpTags");
        }
```
