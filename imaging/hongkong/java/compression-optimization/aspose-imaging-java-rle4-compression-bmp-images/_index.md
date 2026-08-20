---
date: '2026-03-18'
description: 學習如何使用 Aspose.Imaging for Java 以 RLE4 壓縮 BMP 圖像。本 Java 圖像壓縮教學將示範如何設定每像素位元、配置調色盤，並儲存壓縮後的檔案。
keywords:
- RLE4 Compression in Java
- Aspose.Imaging for Java
- BMP Image Processing
- Java RLE4 Encoding with Aspose
- Image Compression Techniques
title: 如何使用 Aspose.Imaging for Java 以 RLE4 壓縮 BMP 圖像
url: /zh-hant/java/compression-optimization/aspose-imaging-java-rle4-compression-bmp-images/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 精通 Aspose.Imaging Java：在 BMP 圖像中實作 RLE4 壓縮

## 介紹

您是否想在 Java 應用程式中有效地管理和操作 BMP 圖像？如果您想了解 **如何壓縮 BMP** 檔案，同時完全掌控色深，本教學正適合您。我們將示範如何從目錄載入 BMP 圖像、使用 Aspose.Imaging for Java 套用 RLE4（Run‑Length Encoding 4）壓縮、**設定每像素位元數**、建立 4 位元色盤，最後將壓縮後的圖像儲存至新位置。

### 快速回答
- **RLE4 壓縮是什麼？** 一種無失真的跑長編碼方法，將像素資料以 4 位元組為單位儲存，適用於 BMP 檔案。  
- **哪個 Java 函式庫支援它？** Aspose.Imaging for Java 內建 RLE4 支援。  
- **我需要授權嗎？** 免費試用可用於測試；正式環境需購買永久授權。  
- **我可以設定色深嗎？** 可以——使用 `setBitsPerPixel(4)` 來定義 4 位元色盤。  
- **這適合嵌入式系統嗎？** 絕對適合；RLE4 能在不犧牲品質的前提下降低檔案大小。

## 什麼是「如何壓縮 BMP」的 RLE4？

RLE4 壓縮透過將連續相同顏色的像素編碼為單一值對，減少 BMP 圖像的檔案大小。此方法在需要為遊戲資產、嵌入式裝置或檔案保存提供小檔案佔用時特別有用。

## 為什麼使用 Aspose.Imaging for Java？

Aspose.Imaging 提供高階 API，抽象化 BMP 格式的底層細節，讓您專注於業務邏輯而非位元層面的操作。它同時支援多種影像格式，並在批次處理時提供可靠的效能。

## 前置條件

- **Java Development Kit (JDK)** – 8 版或更新版本。  
- **Aspose.Imaging for Java** – 提供壓縮功能的程式庫。  
- **IDE 或文字編輯器** – IntelliJ IDEA、Eclipse、VS Code，或您偏好的任何編輯器。  
- **基本的 Java 知識** – 您應熟悉 Java 語法與專案設定。

## 設定 Aspose.Imaging for Java

您可以透過 Maven、Gradle 或直接下載 JAR 的方式將 Aspose.Imaging 加入專案。

**Maven 設定**

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle 設定**

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

**直接下載**

若您偏好手動設定，請前往 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 頁面下載最新的 JAR。

### 取得授權

要解鎖完整功能：

- **免費試用** – 在有限期間內無限制探索 API。  
- **臨時授權** – 取得短期金鑰以延長測試時間。  
- **購買** – 訂閱以獲得無限制的正式使用。

請依照 [官方文件](https://reference.aspose.com/imaging/java/) 中的步驟套用授權檔案。

## 如何使用 Aspose.Imaging 以 RLE4 壓縮 BMP 圖像

以下是逐步說明，完整展示 **如何壓縮 BMP** 檔案、**設定每像素位元數**，以及配置色盤的過程。

### 步驟 1：載入 BMP 圖像

首先，從磁碟載入來源 BMP 檔案。`Image.load()` 方法會回傳一個 `Image` 物件，您可以在 try‑with‑resources 區塊內使用它。

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.bmp.BitmapCompression;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.ColorPaletteHelper;

// Load the BMP image
Image.load("YOUR_DOCUMENT_DIRECTORY\\Rle4.bmp").use(image -> {
    // Proceed to configuration steps...
});
```

**為什麼重要：** 載入圖像會在記憶體中建立可在儲存前修改的表示。

### 步驟 2：設定 BmpOptions – 設定每像素位元數與色盤

建立 `BmpOptions` 實例，指示使用 RLE4 壓縮、將每像素位元數設為 4，並指定 4 位元色盤。

```java
// Create an instance of BmpOptions
BmpOptions options = new BmpOptions();
options.setCompression(BitmapCompression.Rle4);
options.setBitsPerPixel(4);
options.setPalette(ColorPaletteHelper.create4Bit());
```

**為什麼重要：** `setBitsPerPixel(4)` 告訴編碼器每個像素僅使用 4 位元，符合 RLE4 演算法的需求。色盤則確保 16 種可能的顏色正確對應。

### 步驟 3：儲存壓縮後的 BMP

最後，使用已配置的選項將修改後的圖像寫入輸出資料夾。

```java
image.save("YOUR_OUTPUT_DIRECTORY\\output.bmp", options);
```

**為什麼重要：** 儲存時會套用所有先前設定，產生使用 RLE4 壓縮的緊湊 BMP 檔案。

## 設定每像素位元數 – 更深入探討（Java 影像壓縮教學）

當您呼叫 `options.setBitsPerPixel(4)` 時，Aspose.Imaging 會自動將原始色深截斷為 4 位元每像素。這對 RLE4 至關重要，因為演算法需要半位元（nibble）對齊的資料。若需其他深度（例如 8 位元），只要更改數值即可，但請記得 RLE4 專門針對 4 位元影像。

## 常見使用情境

1. **遊戲圖形** – 減少資產大小，以加快主機與行動裝置的載入速度。  
2. **嵌入式系統** – 在閃存有限的裝置上儲存 UI 圖示。  
3. **數位檔案** – 讓歷史 BMP 掃描檔保持輕量，同時保留精確像素資料。

## 效能技巧

- **批次處理** – 迴圈遍歷 BMP 目錄，一次性壓縮所有檔案。  
- **記憶體管理** – 如範例所示使用 `use` 方法，確保即時關閉串流。  
- **非同步 I/O** – 對於 UI 應用程式，於背景執行緒執行載入/儲存，以保持介面回應。

## 疑難排解技巧

- **路徑錯誤** – 確認 `YOUR_DOCUMENT_DIRECTORY` 與 `YOUR_OUTPUT_DIRECTORY` 為絕對路徑或相對於工作目錄正確。  
- **版本不匹配** – 確保 Aspose.Imaging JAR 版本與 API 呼叫相符（程式碼以 25.5 版為目標）。  
- **記憶體不足** – 對於非常大的 BMP，考慮分塊處理或增大 JVM 堆積大小。

## 常見問題

**Q: 什麼是 RLE4 壓縮？**  
A: 它是一種無失真的技術，將相同的 4 位元像素值以連續方式儲存，能大幅縮小 BMP 檔案大小而不損失品質。

**Q: 我可以免費使用 Aspose.Imaging 嗎？**  
A: 可以，提供免費試用版，但正式部署需購買授權。

**Q: 系統需求是什麼？**  
A: 需要 JDK 8 以上的執行環境、足夠的記憶體以容納圖像大小，並將 Aspose.Imaging JAR 放在 classpath 中。

**Q: 如何處理非常大的 BMP 檔案？**  
A: 可分批處理、監控記憶體使用，並考慮增大 JVM 堆積 (`-Xmx` 參數)。

**Q: 哪裡可以找到更多範例？**  
A: 官方的 [Aspose.Imaging Java Reference](https://reference.aspose.com/imaging/java/) 提供豐富的程式碼範例與 API 文件。

## 資源

- **文件說明**： [Aspose.Imaging Java Reference](https://reference.aspose.com/imaging/java/)  
- **下載**： [取得最新版本](https://releases.aspose.com/imaging/java/)  
- **購買授權**： [Buy Aspose.Imaging](https://purchase.aspose.com/buy)  
- **免費試用**： [Start Your Free Trial](https://releases.aspose.com/imaging/java/)  
- **臨時授權**： [Obtain a Temporary License](https://purchase.aspose.com/temporary-license/)  
- **支援**： [Aspose Support Forum](https://forum.aspose.com/c/imaging/14)

---

**最後更新：** 2026-03-18  
**測試環境：** Aspose.Imaging 25.5 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}