---
title: DICOM Compression in Aspose.Imaging for .NET
linktitle: DICOM Compression in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 17
url: /net/dicom-image-processing/dicom-compression/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            // To get proper output please apply a valid Aspose.Imaging License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
            Console.WriteLine("Running example DicomCompression");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string inputFile = Path.Combine(dataDir, "original.jpg");
            string output1 = Path.Combine(dataDir, "original_Uncompressed.dcm");
            string output2 = Path.Combine(dataDir, "original_JPEG.dcm");
            string output3 = Path.Combine(dataDir, "original_JPEG2000.dcm");
            string output4 = Path.Combine(dataDir, "original_RLE.dcm");
            using (var inputImage = Image.Load(inputFile))
            {
                var options = new DicomOptions
                                  {
                                      ColorType = ColorType.Rgb24Bit,
                                      Compression = new Compression { Type = CompressionType.None }
                                  };
                inputImage.Save(output1, options);
            }
            using (var inputImage = Image.Load(inputFile))
            {
                var options = new DicomOptions
                                  {
                                      ColorType = ColorType.Rgb24Bit,
                                      Compression = new Compression { Type = CompressionType.Jpeg }
                                  };
                inputImage.Save(output2, options);
            }
            using (var inputImage = Image.Load(inputFile))
            {
                var options = new DicomOptions
                                  {
                                      ColorType = ColorType.Rgb24Bit,
                                      Compression = new Compression
                                                        {
                                                            Type = CompressionType.Jpeg2000,
                                                            Jpeg2000 = new Jpeg2000Options
                                                                           {
                                                                               Codec = Jpeg2000Codec.Jp2,
                                                                               Irreversible = false
                                                                           }
                                                        }
                                  };
                inputImage.Save(output3, options);
            }
            using (var inputImage = Image.Load(inputFile))
            {
                var options = new DicomOptions
                                  {
                                      ColorType = ColorType.Rgb24Bit,
                                      Compression = new Compression { Type = CompressionType.Rle }
                                  };
                inputImage.Save(output4, options);
            }
            File.Delete(output1);
            File.Delete(output2);
            File.Delete(output3);
            File.Delete(output4);
            Console.WriteLine("Finished example DicomCompression");
        }
```
