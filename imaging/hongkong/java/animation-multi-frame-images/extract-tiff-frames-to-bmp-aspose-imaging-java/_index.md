---
date: '2026-02-25'
description: 學習如何使用 Aspose Imaging Java 將多頁 TIFF 檔案轉換為單獨的 BMP 圖像。本分步指南涵蓋讀取 TIFF、提取影格以及套用
  Aspose 授權 Java。
keywords:
- convert tiff to bmp java
- aspose.imaging java
- extract tiff frames java
- multi-frame tiff to bmp conversion
- animation & multi-frame images
title: aspose imaging java – 將 TIFF 轉換為 BMP 影格
url: /zh-hant/java/animation-multi-frame-images/extract-tiff-frames-to-bmp-aspose-imaging-java/
weight: 1
---

", "BMP", "Aspose.Imaging", "Java", "API", etc.

Also keep "aspose license java" maybe keep as is but maybe translate surrounding text.

We need to keep "aspose license java" unchanged.

Now produce final content.

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 精通使用 Aspose.Imaging Java 將 TIFF 影格提取為 BMP 格式

## 簡介

如果你需要 **讀取 TIFF** 檔案、抽取每個影格，並將它們儲存為 BMP 圖片，**aspose imaging java** 能讓這項工作變得輕鬆。本文將一步步說明從設定函式庫、套用 **aspose license java**、處理多頁 TIFF，到轉換為 BMP 檔案的全部流程。完成後，你將擁有一段可直接嵌入任何 Java 專案的可重用程式碼。

**你將學會**
- 如何安裝與授權 Aspose.Imaging for Java  
- 讀取 **tiff** 檔案並遍歷影格的完整步驟  
- 如何將 **multi page tiff** 圖片轉換為獨立的 BMP 檔案  

先把前置需求處理好，讓你可以立即開始編寫程式。

## 快速回答
- **哪個函式庫負責 TIFF 轉 BMP？** Aspose.Imaging for Java。  
- **需要授權嗎？** 需要 – **aspose license java** 會解鎖全部功能。  
- **可以處理多頁 TIFF 嗎？** 當然可以；API 允許你遍歷每一個影格。  
- **支援哪些 Java 建置工具？** Maven、Gradle，或直接下載 JAR。  
- **需要多少程式碼？** 不到 30 行簡潔的 Java 程式。

## 什麼是 Aspose Imaging Java？
Aspose.Imaging for Java 是一套功能強大、跨平台的函式庫，支援超過 100 種影像格式。它提供高階 API，讓你在不依賴原生程式碼的情況下載入、編輯與轉換影像。

## 為什麼使用 Aspose Imaging Java 進行 TIFF 影格抽取？
- **零外部相依** – 純 Java，任何作業系統皆可執行。  
- **完整支援多影格格式**，如 TIFF、PSD、GIF。  
- **穩定的授權模式** – **aspose license java** 可移除評估限制。  
- **效能導向** – 內建記憶體管理與批次處理工具。

## 前置條件 (H2)

在開始實作之前，請確保你已具備以下條件：

### 必要函式庫、版本與相依性
- **Aspose.Imaging for Java**：版本 25.5 或更新（本教學所使用的 API 版本）。

### 環境設定需求
- 基本的 Java 知識。  
- 如 IntelliJ IDEA 或 Eclipse 等 IDE。

## 設定 Aspose.Imaging for Java (H2)

要開始使用 Aspose.Imaging，請依照你的建置系統執行以下安裝步驟：

**Maven**
```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

**Gradle**
```gradle
implementation 'com.aspose:aspose-imaging:25.5'
```

**直接下載**
亦可從 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下載最新版本。

### 取得授權步驟

- **免費試用** – 無需付費即可探索函式庫。  
- **臨時授權** – 開發階段的便利選項。  
- **正式購買** – 為正式上線解鎖全部功能。

取得授權檔案後，初始化 Aspose.Imaging：

```java
// Set license to unlock full features (if applicable)
License license = new License();
license.setLicense("path/to/your/license.lic");
```

## 實作指南

本節將逐步說明如何使用 Aspose.Imaging Java 將 TIFF 影格轉換為 BMP 檔案。

### 功能：抽取並儲存 TIFF 影格為 BMP (H2)

#### 概述
我們會載入一個 **multi‑page TIFF**，遍歷每個影格，並將每個影格寫出為 BMP 圖片。此模式非常適合需要單獨處理影格的情境，例如醫學影像或檔案保存專案。

##### 步驟 1：載入 TIFF 影像

```java
try (TiffImage multiImage = (TiffImage) Image.load("YOUR_DOCUMENT_DIRECTORY/sample.tiff")) {
    // Proceed to process each frame.
}
```

##### 步驟 2：遍歷 TIFF 影格

```java
int frameCounter = 0;
for (TiffFrame tiffFrame : multiImage.getFrames()) {
    // Process each frame.
}
```

##### 步驟 3：抽取並儲存每個影格為 BMP

```java
multiImage.setActiveFrame(tiffFrame);
Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());

try (BmpOptions bmpCreateOptions = new BmpOptions()) {
    bmpCreateOptions.setBitsPerPixel(24);
    String outputPath = String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "YOUR_OUTPUT_DIRECTORY/", frameCounter);

    bmpCreateOptions.setSource(new FileCreateSource(outputPath, false));
    try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight())) {
        bmpImage.savePixels(tiffFrame.getBounds(), pixels);
        bmpImage.save(outputPath);  // Save the BMP file.
    }
}
frameCounter++;
```

### 常見問題與解決方案 (H2)

- **寫入權限** – 確認輸出資料夾具備寫入權限。  
- **TIFF 路徑無效** – 確認檔案存在且路徑正確。  
- **記憶體不足** – 如範例所示使用 `try‑with‑resources` 立即釋放本機資源。

### 實務應用 (H2)

了解此功能在真實情境中的應用，可提升其價值：

1. **醫學影像** – 從多影格 DICOM 轉換的 TIFF 中抽取單獨切片進行分析。  
2. **數位保存** – 將大型 TIFF 檔案拆分為 BMP，以便更容易分發。  
3. **平面設計** – 為動畫或合成工作流程分離影格。

### 效能考量 (H2)

- **記憶體管理** – `try‑with‑resources` 模式會自動釋放大型影像緩衝區。  
- **批次處理** – 迭代資料夾內的 TIFF 檔案，重複使用同一個 `BmpOptions` 實例以降低開銷。

## 常見問答 (FAQ) (H2)

1. **可以在商業專案中使用 Aspose.Imaging for Java 嗎？**  
   - 可以，但必須擁有有效的 **aspose license java** 以供正式環境使用。

2. **除了 TIFF 與 BMP，Aspose.Imaging 還支援哪些檔案格式？**  
   - 支援 JPEG、PNG、GIF、PSD 等多種格式。完整清單請參考 [documentation](https://reference.aspose.com/imaging/java/)。

3. **處理 TIFF 時，影格數量有上限嗎？**  
   - 上限取決於硬體；函式庫設計能有效處理大型多影格影像。

4. **如何排除檔案路徑或權限錯誤？**  
   - 再次確認目錄是否存在，且 Java 程序具備讀寫權限。

5. **能否自動化批次處理多個 TIFF 檔案？**  
   - 完全可以。將程式碼包在迴圈中，掃描資料夾並依序處理每個 TIFF。

## 資源

- [Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)
- [Download Aspose.Imaging](https://releases.aspose.com/imaging/java/)
- [Purchase Licenses](https://purchase.aspose.com/buy)
- [Free Trial](https://releases.aspose.com/imaging/java/)
- [Temporary License](https://purchase.aspose.com/temporary-license/)
- [Support Forum](https://forum.aspose.com/c/imaging/14)

---

**最後更新：** 2026-02-25  
**測試環境：** Aspose.Imaging 25.5 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}