---
date: 2026-01-24
description: 學習如何使用 Aspose.Imaging for Java 將 SVG 轉換為 EMF。輕鬆保留圖像品質與可伸縮性。
linktitle: Convert SVG to Enhanced Metafile (EMF)
second_title: Aspose.Imaging Java Image Processing API
title: 使用 Aspose.Imaging for Java 將 SVG 轉換為 EMF
url: /zh-hant/java/metafile-and-vector-image-handling/convert-svg-to-enhanced-metafile/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Imaging for Java 將 SVG 轉換為 EMF

## Introduction

在不斷演變的數位圖形世界中，您常常需要 **convert SVG to EMF** 以在針對 Windows 平台的應用程式（如 Office 文件或舊版報表工具）時保持向量品質。Aspose.Imaging for Java 讓此轉換變得輕鬆，並保證產生的 Enhanced Metafile 仍具可伸縮性與清晰度。在本步驟指南中，我們將逐一說明如何快速且可靠地將 SVG 轉換為 EMF。

## Quick Answers
- **哪個函式庫負責轉換？** Aspose.Imaging for Java.
- **是否可以用單行程式碼完成轉換？** 可以 – 使用 `Image.save` 搭配 `EmfOptions`.
- **生產環境是否需要授權？** 需要有效的 Aspose.Imaging 授權才能用於非評估版建置。
- **支援哪些 Java 版本？** Java 8 及更新版本。
- **輸出是否真的是向量格式？** 是，EMF 保留向量資料，縮放不會降低品質。

## What is “convert SVG to EMF”?

將 SVG 轉換為 EMF 意指把 Scalable Vector Graphics（網頁友好、基於 XML 的向量格式）轉換成 Enhanced Metafile（Windows 原生的向量容器）。當您需要在只能辨識 EMF 的應用程式（如 Microsoft Office、Visio 或特定報表引擎）中使用高品質圖形時，此轉換非常有用。

## Why use Aspose.Imaging for Java?
- **高保真度：** 函式庫以精確的頁面尺寸光柵化 SVG，保持每條線條與曲線完整。
- **無外部相依性：** 純 Java，無需本機二進位檔。
- **批次處理：** 可輕鬆在一次執行中迴圈處理多個 SVG 檔案。
- **跨平台：** 支援 Windows、Linux 與 macOS。

## Prerequisites

1. **Java 開發環境** – 已在機器上安裝 Java 8 以上。  
2. **Aspose.Imaging for Java 函式庫** – 從供應商網站 **[here](https://purchase.aspose.com/buy)** 取得。  
3. **範例 SVG 檔案** – 使用隨 Aspose.Imaging 文件附帶的範例，或自行提供的任何 SVG。

現在所有前置作業已完成，讓我們深入程式碼。

## Import Packages

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Size;
import com.aspose.imaging.imageoptions.EmfOptions;
import com.aspose.imaging.imageoptions.SvgRasterizationOptions;
import java.io.File;
```

## Step 1: Set Up Your Project
建立一個新的 Java 專案（或開啟既有專案），並將 Aspose.Imaging JAR 加入建置路徑。Maven 使用者可於 Aspose Maven 倉庫加入相應的 `<dependency>` 條目。

## Step 2: Organize Your SVG Files
將所有欲轉換的 SVG 放入一個資料夾 – 本教學使用名為 **ConvertingImages** 的資料夾，位於您的文件目錄下。

## Step 3: Define the Output Directory

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
String outputPath = Path.combine("Your Document Directory", "output/");
File dir = new File(outputPath);
if (!dir.exists() && !dir.mkdirs()) {
    throw new AssertionError("Can not create the output directory!");
}
```

> **Pro tip:** 將 `"Your Document Directory"` 替換為您機器上的絕對路徑，以避免路徑解析問題。

## Step 4: Perform the Conversion (convert SVG to EMF)

```java
String[] testFiles = new String[]
    {
        "input.svg",
        "juanmontoya_lingerie.svg",
        "rg1024_green_grapes.svg",
        "sample_car.svg",
        "tommek_Car.svg"
    };

for (String fileName : testFiles) {
    String inputFileName = dataDir + fileName;
    String outputFileName = outputPath + fileName + ".emf";
    
    try (Image image = Image.load(inputFileName)) {
        image.save(outputFileName, new EmfOptions() {
            {
                setVectorRasterizationOptions(new SvgRasterizationOptions() {
                    {
                        setPageSize(Size.to_SizeF(image.getSize()));
                    }
                });
            }
        });
    }
}
```

此迴圈會載入每個 SVG，設定光柵化尺寸與原始 SVG 相同，並將結果以 EMF 檔案儲存至 **output** 資料夾。

## Common Issues & Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| **Output file is blank** | Wrong page size or missing rasterization options | Ensure `setPageSize(Size.to_SizeF(image.getSize()))` is set inside `SvgRasterizationOptions`. |
| **`Path.combine` not found** | Using Java 8 where `Path` is not imported | Replace with `java.nio.file.Paths.get(dir1, dir2).toString()`. |
| **License exception** | Running without a valid license in production | Load your license file at the start of the application: `License license = new License(); license.setLicense("Aspose.Imaging.Java.lic");`. |

## Frequently Asked Questions

**Q: 轉換 SVG 為 EMF 有什麼好處？**  
A: 轉換 SVG 為 EMF 能保留圖像的向量品質，使其適用於各種應用，包括列印與縮放，且不會失真。

**Q: 在哪裡可以找到 Aspose.Imaging for Java 的文件？**  
A: 您可以透過 **[here](https://reference.aspose.com/imaging/java/)** 存取文件。

**Q: 是否提供 Aspose.Imaging for Java 的免費試用版？**  
A: 有，您可從 **[here](https://releases.aspose.com/)** 取得免費試用版。

**Q: 我可以取得 Aspose.Imaging for Java 的臨時授權嗎？**  
A: 可以，請前往 **[here](https://purchase.aspose.com/temporary-license/)** 取得臨時授權。

**Q: 如何取得 Aspose.Imaging for Java 的支援或提問？**  
A: 您可造訪 Aspose.Imaging for Java 支援論壇 **[here](https://forum.aspose.com/)**。

## Conclusion

依照上述步驟，您現在已掌握使用 Aspose.Imaging for Java **convert SVG to EMF** 的可靠方法。此方式可讓您的圖形保持銳利、可伸縮，並適用於任何 Windows 為基礎的工作流程。歡迎嘗試不同的光柵化設定，或將轉換邏輯整合至更大型的批次處理管線中。

---

**Last Updated:** 2026-01-24  
**Tested With:** Aspose.Imaging for Java 24.9  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}