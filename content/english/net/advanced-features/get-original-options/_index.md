---
title: Get Original Options in Aspose.Imaging for .NET
linktitle: Get Original Options in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: 
type: docs
weight: 10
url: /net/advanced-features/get-original-options/
---

## Complete Source Code
```csharp
        public static void Run()
        {
            Console.WriteLine("Running example GetOriginalOptions");
            string dataDir = "Your Document Directory";
            using (ApngImage image = (ApngImage)Image.Load(Path.Combine(dataDir, "SteamEngine.png")))
            {
                ApngOptions options = (ApngOptions)image.GetOriginalOptions();
                if (options.NumPlays != 0 || options.DefaultFrameTime != 10 || options.BitDepth != 8)
                {
                    Console.WriteLine("Exist some errors in default options");
                }
            }
            Console.WriteLine("Finished example GetOriginalOptions");
        }
```
