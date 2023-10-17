---
title: Create Image using Stream in Aspose.Imaging for .NET
linktitle: Create Image using Stream in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 11
url: /net/image-creation/create-image-using-stream/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example CreatingImageUsingStream");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Creates an instance of BmpOptions and set its various properties
            BmpOptions ImageOptions = new BmpOptions();
            ImageOptions.BitsPerPixel = 24;
            // Create an instance of System.IO.Stream
            Stream stream = new FileStream(dataDir + "sample_out.bmp", FileMode.Create);
            // Define the source property for the instance of BmpOptions Second boolean parameter determines if the Stream is disposed once get out of scope
            ImageOptions.Source = new StreamSource(stream, true);
            // Creates an instance of Image and call Create method by passing the BmpOptions object
            using (Image image = Image.Create(ImageOptions, 500, 500))
            {
                // Do some image processing
                image.Save(dataDir + "CreatingImageUsingStream_out.bmp");
            }
            Console.WriteLine("Finished example CreatingImageUsingStream");
        }
```
