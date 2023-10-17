---
title: Measure Text in Aspose.Imaging for .NET
linktitle: Measure Text in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 10
url: /net/text-and-measurements/measure-text/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example GraphicsMeasureString");
            string dataDir = "Your Document Directory";
            string filepath = Path.Combine(dataDir, "input.jpg");
            using (Image backgoundImage = Image.Load(filepath))
            {
                Graphics gr = new Graphics(backgoundImage);
                StringFormat format = new StringFormat();
                SizeF size = gr.MeasureString("Test", new Font("Arial", 10), SizeF.Empty, format);
            }
            Console.WriteLine("Finished example GraphicsMeasureString");
        }
```
