---
date: '2026-11-04'
description: 了解如何使用 Aspose Imaging 授權在 Java 中建立動畫 PNG、加入 Maven 相依性、將 TIFF 轉換為 APNG
  並儲存影像。
keywords:
- aspose imaging license
- convert tiff to apng
- tiff to png conversion
- add maven dependency java
- control animation speed java
lastmod: '2026-11-04'
og_description: 了解如何使用 Aspose Imaging 授權在 Java 中建立動畫 PNG、加入 Maven 相依性、將 TIFF 轉換為 APNG
  並控制動畫速度。
og_image_alt: Guide showing how to generate animated PNGs in Java with Aspose Imaging
og_title: 使用 Aspose Imaging 授權在 Java 中建立動畫 PNG
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to create animated PNG in Java with an Aspose Imaging license,
    add the Maven dependency, convert TIFF to APNG and save the image.
  headline: Create animated PNG in Java using an Aspose Imaging license
  type: TechArticle
- description: Learn how to create animated PNG in Java with an Aspose Imaging license,
    add the Maven dependency, convert TIFF to APNG and save the image.
  name: Create animated PNG in Java using an Aspose Imaging license
  steps:
  - name: '**Web development** – Animated banners, icons, or loading spinners that
      work across browsers without needing GIF support.'
    text: '**Web development** – Animated banners, icons, or loading spinners that
      work across browsers without needing GIF support.'
  - name: '**Desktop applications** – Enrich Swing or JavaFX UI components with subtle
      motion cues.'
    text: '**Desktop applications** – Enrich Swing or JavaFX UI components with subtle
      motion cues.'
  - name: '**Data visualization** – Animate chart transitions or step‑by‑step walkthroughs
      for reports.'
    text: '**Data visualization** – Animate chart transitions or step‑by‑step walkthroughs
      for reports.'
  type: HowTo
- questions:
  - answer: You must set the value yourself with `setDefaultFrameTime(int ms)`; there
      is no hidden default.
    question: What is the default frame duration for APNG using Aspose.Imaging?
  - answer: Yes—load the file, modify the frame timings via `ApngOptions`, and save
      it again.
    question: Can I adjust animation speed in an existing APNG file?
  - answer: Ensure the image path is correct, allocate enough heap memory for large
      files, and use `try‑with‑resources` to release resources promptly.
    question: What are common pitfalls when loading images with Aspose.Imaging?
  - answer: Visit [Aspose's download page](https://releases.aspose.com/imaging/java/)
      to request a trial.
    question: How do I obtain a free trial license for Aspose.Imaging?
  - answer: Absolutely—you can combine it with Spring, Apache Commons, or any UI framework
      such as JavaFX.
    question: Is Aspose.Imaging compatible with other Java libraries?
  type: FAQPage
tags:
- aspose imaging
- animated png java
- tiff conversion
- maven dependency
- java image processing
title: 使用 Aspose Imaging 授權在 Java 中建立動畫 PNG
url: /zh-hant/java/animation-multi-frame-images/aspose-imaging-java-animated-png-guide/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose Imaging 授權在 Java 中建立動畫 PNG

## 介紹

如果您需要 **在 Java 中建立動畫 PNG**，且希望有可靠、可投入生產的解決方案，**Aspose Imaging 授權** 可讓您完整存取此函式庫的高效能 API。無論您是建置網站入口、桌面 UI，或是資料視覺化儀表板，動畫 PNG（APNG）都能提供平滑的動態效果，且不會像 GIF 那樣有顏色與檔案大小的限制。本教學將帶您一步步加入 Maven 相依性、將多頁 TIFF 轉換為 APNG，並控制影格時間，讓您快速交付精緻的動畫。

## 快速解答
- **哪個函式庫能在 Java 中建立 APNG？** Aspose.Imaging 搭配 Aspose Imaging Maven 相依性。  
- **哪種格式可以轉換為 APNG？** 多頁 TIFF 檔案可轉換為動畫 PNG。  
- **如何控制動畫速度？** 設定 `ApngOptions.setDefaultFrameTime(milliseconds)`。  
- **生產環境是否需要授權？** 需要——Aspose Imaging 授權會移除評估限制並解鎖全部功能。  
- **可以使用 Maven 或 Gradle 嗎？** 兩者皆支援，只要加入相應的相依性即可。

## 什麼是 Aspose Imaging 授權？

**Aspose Imaging 授權** 是一個檔案，可解鎖 Aspose.Imaging for Java 函式庫的完整、無限制功能，移除評估水印與使用上限。您只需在應用程式啟動時載入授權檔，之後所有 API 呼叫皆不受試用限制。

## 為什麼使用 Aspose.Imaging 來製作 APNG？

Aspose.Imaging 支援 **150+ 影像格式**（包括 JPEG、PNG、TIFF、BMP、WebP），且能處理數百頁的文件，同時在一般 8 GB JVM 上的記憶體使用量保持在 200 MB 以下。其原生 APNG 編碼器保留透明度、完整色深與每影格時間設定，無需外部工具，是 Java 開發者最快、最可靠的選擇。

## 前置條件
- 已安裝 Java 8 或更高版本。  
- 使用 IntelliJ IDEA 或 Eclipse 等 IDE。  
- 使用 Maven 或 Gradle 進行相依性管理（或直接使用 JAR 檔案）。  

## 新增 Aspose Imaging 的 Maven 相依性

### Maven

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

若偏好直接下載，您可以從 [Aspose's download page](https://releases.aspose.com/imaging/java/) 取得最新版本。亦可前往 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 查看發佈說明。

## 授權取得

若要解除評估限制、完整開啟功能：

- **免費試用：** 先使用免費試用版測試功能。  
- **臨時授權：** 在開發期間取得臨時授權以延長存取。  
- **購買：** 長期使用請購買商業授權。

在程式碼中初始化授權：

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path/to/your/license/file.lic");
```

`License` 會載入 Aspose.Imaging 授權檔，以解鎖全部功能。

## 如何使用 Aspose.Imaging 將 TIFF 轉換為 APNG？

載入來源 TIFF、設定 APNG 選項，然後儲存結果。函式庫會將每一頁 TIFF 取出作為獨立影格，寫入符合標準的動畫 PNG。此過程亦允許您設定預設影格時間、選擇壓縮等級，甚至在儲存前調整影格尺寸，讓您完整掌控最終動畫品質與檔案大小。

### 載入影像

`Image` 是 Aspose.Imaging 中代表影像物件的基礎類別。

```java
import com.aspose.imaging.Image;
```

```java
String inputFilePath = "YOUR_DOCUMENT_DIRECTORY/img4.tif";

try (Image image = Image.load(inputFilePath)) {
    // The image is now loaded and ready for manipulation.
}
```

### 設定 APNG 的預設影格持續時間

`ApngOptions` 用於設定將影像儲存為動畫 PNG 時的各項參數。

```java
import com.aspose.imaging.imageoptions.ApngOptions;
```

```java
ApngOptions op = new ApngOptions();
op.setDefaultFrameTime(500); // Default frame time set to 500 milliseconds
```

### 將影像儲存為 APNG

準備輸出路徑，並以設定好的選項呼叫 `save`：

```java
String outputFilePath = "YOUR_OUTPUT_DIRECTORY/img4.tif.500ms.png";
```

```java
try (Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/img4.tif")) {
    ApngOptions op = new ApngOptions();
    op.setDefaultFrameTime(500); // Frame time set to 500 ms
    
    image.save(outputFilePath, op);
}
```

程式碼 `image.save(outputFilePath, op);` **會將影像儲存為 APNG**。請確保輸出檔案以 `.png` 結尾，且 `ApngOptions` 內的設定符合您想要的影格時間。

## 如何在 Java 中將影像儲存為 APNG？

呼叫 `image.save` 並傳入設定好預設影格時間的 `ApngOptions` 實例。調整 `setDefaultFrameTime` 即可加快或放慢動畫，也可將相同呼叫套用於其他多頁來源（如 PDF）。使用 try‑with‑resources 區塊可確保影像資源即時釋放，避免批次處理時發生記憶體洩漏。

## 實務應用
1. **Web 開發** – 動畫橫幅、圖示或載入指示器，可在各瀏覽器上運作且不需 GIF 支援。  
2. **桌面應用程式** – 為 Swing 或 JavaFX UI 元件加入細緻的動態提示。  
3. **資料視覺化** – 為圖表過渡或報告的逐步說明加入動畫效果。

將 Aspose.Imaging 與 Swing、JavaFX 或 Spring Boot 等函式庫結合，即可提供無縫的使用者體驗。

## 效能考量
- **明智縮放：** 高解析度會增加記憶體使用量，盡可能下調尺寸。  
- **即時釋放：** 如範例所示，使用 `try‑with‑resources` 釋放本機資源。  
- **批次處理：** 重複使用單一 `License` 實例，避免在大量產生 APNG 時重複載入相同來源檔案。

## 常見問題與解決方案
| 問題 | 原因 | 解決方式 |
|-------|-------|-----|
| **OutOfMemoryError** 在載入大型 TIFF 時 | 影像尺寸超過 JVM 堆積容量 | 增加 `-Xmx` 設定或在處理前先縮小尺寸 |
| **Blank frames** 出現在輸出 APNG 中 | 來源 TIFF 各頁尺寸不同 | 在儲存前將所有頁面調整為相同大小 |
| **License not applied** | 授權檔路徑不正確 | 核對路徑，確保執行時檔案可讀取 |

## 常見問答

**Q: 使用 Aspose.Imaging 時，APNG 的預設影格持續時間是多少？**  
A: 必須自行使用 `setDefaultFrameTime(int ms)` 設定，沒有隱藏的預設值。

**Q: 能否調整已存在的 APNG 檔案的動畫速度？**  
A: 可以——載入檔案後，透過 `ApngOptions` 修改影格時間，再重新儲存。

**Q: 使用 Aspose.Imaging 載入影像時常見的陷阱是什麼？**  
A: 確認影像路徑正確、為大型檔案配置足夠的堆積記憶體，並使用 `try‑with‑resources` 及時釋放資源。

**Q: 如何取得 Aspose.Imaging 的免費試用授權？**  
A: 前往 [Aspose's download page](https://releases.aspose.com/imaging/java/) 申請試用。

**Q: Aspose.Imaging 能否與其他 Java 函式庫相容？**  
A: 完全可以——您可以將它與 Spring、Apache Commons，或任何 UI 框架（如 JavaFX）結合使用。

## 資源

- **文件說明：** [Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)  
- **下載：** [Latest Release Download](https://releases.aspose.com/imaging/java/)  
- **購買：** [Buy Aspose.Imaging](https://purchase.aspose.com/buy)  
- **免費試用：** [Get Started with Free Trial](https://releases.aspose.com/imaging/java/)  
- **臨時授權：** [Acquire Temporary License](https://purchase.aspose.com/temporary-license/)  
- **支援論壇：** [Aspose Community Support](https://forum.aspose.com/c/imaging/14)

---

**最後更新：** 2026-11-04  
**測試環境：** Aspose.Imaging 25.5 for Java  
**作者：** Aspose

## 相關教學

- [如何使用 Aspose.Imaging Java 建立動畫 GIF：影格與迴圈控制](/imaging/java/animation-multi-frame-images/gif-manipulation-java-aspose-imaging-guide/)
- [如何使用 Aspose.Imaging for Java 建立多頁 TIFF——完整指南](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [在 Java 中使用 Aspose.Imaging 處理多影格 TIFF](/imaging/java/animation-multi-frame-images/java-aspose-imaging-multi-frame-tiff-processing/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}