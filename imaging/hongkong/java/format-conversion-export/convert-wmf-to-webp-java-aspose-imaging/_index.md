---
date: '2026-06-03'
description: 了解如何使用 Aspose.Imaging for Java 將圖像儲存為 WebP 以及將 WMF 轉換為 WebP。提供逐步說明、先決條件、程式碼範例與效能技巧。
keywords:
- save image as webp
- how to convert wmf
- Aspose.Imaging Java tutorial
- WMF to WebP conversion
- image format conversion Java
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to save image as WebP and how to convert WMF to WebP using
    Aspose.Imaging for Java. Step‑by‑step guide with prerequisites, code snippets,
    and performance tips.
  headline: How to Save Image as WebP and Convert WMF to WebP in Java with Aspose.Imaging
  type: TechArticle
- description: Learn how to save image as WebP and how to convert WMF to WebP using
    Aspose.Imaging for Java. Step‑by‑step guide with prerequisites, code snippets,
    and performance tips.
  name: How to Save Image as WebP and Convert WMF to WebP in Java with Aspose.Imaging
  steps:
  - name: '**Web Development:** Serve lightweight WebP assets to improve page‑load
      speed.'
    text: '**Web Development:** Serve lightweight WebP assets to improve page‑load
      speed.'
  - name: '**Responsive Design:** Generate device‑specific sizes on the fly.'
    text: '**Responsive Design:** Generate device‑specific sizes on the fly.'
  - name: '**CMS Integration:** Automate image optimization during upload.'
    text: '**CMS Integration:** Automate image optimization during upload.'
  - name: '**Mobile Apps:** Reduce bundle size while keeping crisp icons.'
    text: '**Mobile Apps:** Reduce bundle size while keeping crisp icons.'
  - name: '**Archiving:** Store large collections of vector graphics in a compact,
      lossless WebP format.'
    text: '**Archiving:** Store large collections of vector graphics in a compact,
      lossless WebP format.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Imaging supports SVG, EMF, and WMF; just load the file with
      `Image.load()` and follow the same rasterization steps.
    question: Can I convert other vector formats (e.g., SVG) to WebP using the same
      approach?
  - answer: Aspose.Imaging can create animated WebP by adding each frame as a separate
      image to a `WebPOptions` collection before saving.
    question: Is there a way to generate animated WebP from multiple WMF frames?
  - answer: You can set the `resolution` property on `EmfRasterizationOptions` to
      control DPI; otherwise, it defaults to 96 dpi.
    question: Does the library handle DPI scaling automatically?
  - answer: The library can handle multi‑hundred‑page WMF files (up to 500 MB) without
      loading the entire document into memory, thanks to its streaming architecture.
    question: What is the maximum file size Aspose.Imaging can process?
  - answer: No, Aspose.Imaging includes a native WebP encoder, so no external dependencies
      are required.
    question: Do I need a separate WebP codec installed on the server?
  type: FAQPage
title: 如何在 Java 中使用 Aspose.Imaging 將圖像儲存為 WebP 以及將 WMF 轉換為 WebP
url: /zh-hant/java/format-conversion-export/convert-wmf-to-webp-java-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 使用 Aspose.Imaging 在 Java 中將 WMF 轉換為 WebP

## 介紹

如果您需要從 Windows Metafile（WMF）來源 **將圖像儲存為 WebP**，您來對地方了。在本教學中，我們將完整示範工作流程——載入 WMF、以正確尺寸光柵化、設定 WebP 參數，最後 **將圖像儲存為 WebP**。掌握此流程可讓圖像檔案大小縮減最高 30 %，同時保留視覺品質，這對於快速載入的網頁與回應式行動應用程式至關重要。

**您將學會的內容**
- 如何在 Java 中設定 Aspose.Imaging。
- 從 WMF **將圖像儲存為 WebP** 的完整步驟。
- 光柵化時如何保持長寬比。
- `EmfRasterizationOptions` 與 `WebPOptions` 的設定方式。
- 真實案例與效能導向的技巧。

在深入之前，請確保以下先決條件已備妥。

## 快速答覆
- **我可以批次將 WMF 檔案轉換為 WebP 嗎？** 可以，遍歷檔案並重複使用相同的光柵化設定即可。  
- **需要哪個 Java 版本？** JDK 8 或更新版本。  
- **生產環境需要授權嗎？** 商業版 Aspose.Imaging 授權可移除評估限制。  
- **WebP 是無損還是有損？** 兩者皆支援；可在 `WebPOptions` 中選擇品質設定。  
- **圖像品質會受影響嗎？** 適當的光柵化會保留向量細節，品質與原始 WMF 相當。

## 什麼是「將圖像儲存為 WebP」？
**「將圖像儲存為 WebP」** 指的是將圖像物件寫入 WebP 檔案格式，該格式結合有損與無損壓縮以減少檔案大小。Aspose.Imaging 內部處理編碼，您只需呼叫 `save` 方法並傳入相應的選項即可。

## 為什麼要將 WMF 轉換為 WebP？
Aspose.Imaging 支援 **超過 50 種輸入與輸出格式**——包括 WMF、SVG、JPEG、PNG 與 WebP。將 WMF 轉換為 WebP 平均可減少最高 35 % 的檔案大小，加速頁面載入並降低頻寬成本，且無需額外的圖像處理伺服器。

## 先決條件

- **Java Development Kit (JDK)：** 已安裝 8 版或更新版本。  
- **IDE：** IntelliJ IDEA、Eclipse，或您慣用的任何編輯器。  
- **Aspose.Imaging 程式庫：** 透過 Maven 或 Gradle 加入相依性（請參閱下節）。  

## 設定 Aspose.Imaging for Java

### Maven
將以下相依性加入 `pom.xml` 檔案：
```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
在 `build.gradle` 檔案中加入此行：
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

您也可以直接從 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下載最新的 JAR。

### 授權取得
若要在無評估限制的情況下執行：
- **免費試用：** 先使用試用授權。  
- **臨時授權：** 用於延長測試。  
- **購買授權：** 取得完整訂閱以供正式上線使用。

## 如何在 Java 中將圖像儲存為 WebP？

`save` 會使用指定的選項將圖像寫入檔案。

在 `Image` 物件上呼叫 `save` 方法，傳入輸出路徑與 `WebPOptions` 實例。這一行程式碼即會將光柵化後的位圖寫入 `.webp` 檔，完成轉換。

**說明：** `save` 呼叫同時執行光柵化（使用您設定的選項）與 WebP 編碼，效率極高。

### 載入現有圖像

`Image` 類別是 Aspose.Imaging 的頂層物件，代表記憶體中的任何支援圖像格式。載入 WMF 檔案會產生可光柵化的表示，供後續操作。

```java
import com.aspose.imaging.Image;

String inputFileName = "YOUR_DOCUMENT_DIRECTORY/sample.wmf";
Image image = Image.load(inputFileName);
try {
    // The image is now loaded and ready for manipulation or conversion.
} finally {
    image.dispose();
}
```

**說明：** `Image.load()` 會將 WMF 檔讀入 `Image` 實例。將使用方式包在 `try‑finally` 區塊中，可確保圖像即時釋放原生資源。

### 計算光柵化的新尺寸

當您設定固定寬度時，必須計算高度以維持原始長寬比，避免變形並確保在各裝置上的視覺一致性。

```java
double k = (image.getWidth() * 1.00) / image.getHeight();
int newHeight = (int) Math.round(400 / k);
```

**說明：** 先以原始寬度除以原始高度，再乘上目標寬度（400 px），即可得到比例正確的高度，保持向量形狀。

### 設定 EmfRasterizationOptions

`EmfRasterizationOptions` 告訴 Aspose.Imaging 在編碼前如何將 WMF 轉換為位圖，包含寬度、高度、背景色與邊框設定。

```java
import com.aspose.imaging.imageoptions.EmfRasterizationOptions;
import com.aspose.imaging.Color;

EmfRasterizationOptions emf = new EmfRasterizationOptions();
emf.setPageWidth(400);
emf.setPageHeight(newHeight); // Height calculated in the previous section.
emf.setBorderX(5);
emf.setBorderY(10);
emf.setBackgroundColor(Color.getWhiteSmoke());
```

**說明：** 以計算出的尺寸初始化選項物件，設定透明背景，並加上 1 像素邊框以避免裁切。

### 設定 WebPOptions 以產出檔案

`WebPOptions` 包含 WebP 專屬參數，如壓縮品質與無損模式。它同時接受先前設定的光柵化選項，確保整個流程無縫銜接。

```java
import com.aspose.imaging.imageoptions.WebPOptions;
import com.aspose.imaging.ImageOptionsBase;

ImageOptionsBase options = new WebPOptions();
options.setVectorRasterizationOptions(emf);
```

**說明：** 將 `WebPOptions` 與 `EmfRasterizationOptions` 連結後，光柵化的位圖會以完全相同的方式編碼為 WebP。

## 實務應用

1. **網站開發：** 提供輕量化的 WebP 資源以提升頁面載入速度。  
2. **回應式設計：** 即時產生符合裝置尺寸的圖像。  
3. **CMS 整合：** 圖片上傳時自動優化。  
4. **行動應用程式：** 減少套件大小，同時保留清晰圖示。  
5. **檔案保存：** 將大量向量圖以緊湊的無損 WebP 格式存檔。

## 效能考量

- **提前調整尺寸：** 在儲存前先縮放至目標尺寸，可降低記憶體使用。  
- **即時釋放資源：** 必須呼叫 `dispose()`（或使用 try‑with‑resources）以釋放原生緩衝區。  
- **平行處理：** 大量轉換時，可為每個檔案啟動獨立執行緒或使用 executor service，充分利用 CPU 核心。

## 常見問題與解決方案

- **WMF 檔損毀：** 先以檢視器驗證來源檔案；若無法解析，Aspose.Imaging 會拋出具說明性的例外。  
- **記憶體不足：** 對極大 WMF 以分段方式處理，或提升 JVM 堆積大小（`-Xmx2g`）。  
- **顏色偏移：** 確認 `EmfRasterizationOptions` 的 `backgroundColor` 與預期畫布相符（透明或白色）。

## 常見問答

**Q: 我可以使用相同方式將其他向量格式（例如 SVG）轉換為 WebP 嗎？**  
A: 可以，Aspose.Imaging 支援 SVG、EMF 與 WMF，只要以 `Image.load()` 載入檔案並遵循相同的光柵化步驟即可。

**Q: 能否從多個 WMF 幀產生動畫 WebP？**  
A: Aspose.Imaging 可透過在 `WebPOptions` 的集合中加入每個幀，建立動畫 WebP。

**Q: 程式庫會自動處理 DPI 縮放嗎？**  
A: 您可以在 `EmfRasterizationOptions` 上設定 `resolution` 屬性以控制 DPI；若未設定，預設為 96 dpi。

**Q: Aspose.Imaging 能處理的最大檔案大小是多少？**  
A: 該程式庫可處理多頁 WMF（最高約 500 MB），且採用串流架構，無需一次載入整個文件至記憶體。

**Q: 伺服器上需要額外安裝 WebP 編解碼器嗎？**  
A: 不需要，Aspose.Imaging 內建原生 WebP 編碼器，無需外部相依。

## 資源

- [Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)
- [Download Aspose.Imaging](https://releases.aspose.com/imaging/java/)
- [Purchase Subscription](https://purchase.aspose.com/buy)
- [Free Trial License](https://releases.aspose.com/imaging/java/)
- [Temporary License](https://purchase.aspose.com/temporary-license/)
- [Aspose Support Forum](https://forum.aspose.com/c/imaging/14)

---

**最後更新：** 2026-06-03  
**測試環境：** Aspose.Imaging 24.12 for Java  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [Aspose.Imaging Java: Load and Save WebP Image Frames Tutorial](/imaging/java/format-specific-operations/aspose-imaging-java-webp-frame-handling/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
String outFileName = "YOUR_OUTPUT_DIRECTORY/ConvertingWMFtoWebp_out.webp";
image.save(outFileName, options);
```