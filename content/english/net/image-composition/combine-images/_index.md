---
title: Combine Images in Aspose.Imaging for .NET
linktitle: Combine Images in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 10
url: /net/image-composition/combine-images/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example CombineImages");
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Create an instance of JpegOptions and set its various properties
            JpegOptions imageOptions = new JpegOptions();
            // Create an instance of FileCreateSource and assign it to Source property
            imageOptions.Source = new FileCreateSource(dataDir + "Two_images_result_out.bmp", false);
            // Create an instance of Image and define canvas size
            using (var image = Image.Create(imageOptions, 600, 600))
            {
                // Create and initialize an instance of Graphics, Clear the image surface with white color and Draw Image
                var graphics = new Graphics(image);
                graphics.Clear(Color.White);
                graphics.DrawImage(Image.Load(dataDir + "sample_1.bmp"), 0, 0, 600, 300);
                graphics.DrawImage(Image.Load(dataDir + "File1.bmp"), 0, 300, 600, 300);
                image.Save();
            }
            Console.WriteLine("Finished example CombineImages");
        }
```
