---
date: '2026-06-18'
description: 了解如何使用 Aspose Imaging Convert EMF 透過 Java 匯出 EMF 文字為可縮放的 SVG 形狀或純文字。提供程式碼、技巧與效能建議的逐步指南。
keywords:
- aspose imaging convert emf
- export emf text to svg java
- aspose imaging emf to plain text
- java image conversion
- ems to svg shapes
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  headline: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  type: TechArticle
- description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  name: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  steps:
  - name: Load the Source Image
    text: '`Image` is the core class that represents any supported raster or vector
      image in memory.'
  - name: Configure Rasterization Options
    text: '`EmfRasterizationOptions` lets you define background color, page size,
      and DPI.'
  - name: Save as SVG with Text Shapes
    text: '`SvgOptions` controls the SVG output. Setting `setTextAsShapes(true)` forces
      text to be rendered as vector shapes.'
  - name: Resource Management
    text: Always call `image.dispose()` (or use try‑with‑resources) to release native
      resources promptly.
  - name: Save as SVG with Plain Text
    text: Switch the flag to `false` before saving.
  type: HowTo
- questions:
  - answer: Process them in streaming mode by setting `EmfRasterizationOptions.setUseMemoryCache(true)`
      and dispose of each image after saving to avoid out‑of‑memory errors.
    question: How do I handle very large EMF files (hundreds of MB)?
  - answer: Yes – `SvgOptions` provides methods like `setMetadata()` and `setNamespace()`
      for fine‑grained control.
    question: Can I customize the SVG output (e.g., add metadata or change namespaces)?
  - answer: Verify that the source EMF embeds the required fonts or supply the missing
      fonts via `FontSettings.setFontsFolder()` before loading.
    question: My text appears garbled after conversion. What should I check?
  - answer: Absolutely. Aspose.Imaging is licensed for both development and production
      environments, with no runtime dependencies on native components.
    question: Is the library safe for commercial use?
  - answer: Post questions on the official **[Aspose forum](https://forum.aspose.com/c/imaging/14)**
      or raise a ticket through the support portal.
    question: Where can I get community support?
  type: FAQPage
title: Aspose Imaging Convert EMF – 匯出 EMF 文字為 SVG (Java)
url: /zh-hant/java/format-conversion-export/export-emf-text-svg-shapes-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 如何使用 Aspose.Imaging for Java 將 EMF 文字匯出為 SVG 形狀或純文字  

如果您需要將 **aspose imaging convert emf** 檔案轉換為乾淨的 SVG 圖形或可編輯的文字，您來對地方了。在本教學中，您將會看到如何載入 EMF、在向量形狀輸出與純文字輸出之間做選擇，並透過幾個簡潔的 API 呼叫儲存結果。無論您是要建立批次轉換服務或單一檔案工具，以下步驟都能讓您快速上手。

## 快速解答
- **Aspose.Imaging 能將 EMF 轉換為 SVG 嗎？** Yes – just load the EMF and save with `SvgOptions`.  
- **形狀 SVG 與純文字 SVG 有何差異？** 形狀模式會將每個字形光柵化為向量路徑；純文字模式則保留原始字元。  
- **轉換是否需要授權？** 免費試用可用於開發；正式環境需要永久授權。  
- **需要哪個版本的 Java？** 完全支援 Java 8 或更新版本。  
- **是否支援批次處理？** 當然可以 – 迴圈處理檔案並重複使用相同的 `SvgOptions` 實例。  

## Aspose.Imaging for Java 是什麼？  
`Aspose.Imaging` 是一個 Java 函式庫，提供 **50+** 種輸入與輸出影像格式，包括 EMF、SVG、PNG、JPEG 與 PDF。它能在不將整個檔案載入記憶體的情況下處理數百頁文件，非常適合高吞吐量的轉換管線。

## 為何使用 Aspose Imaging 轉換 EMF？  
使用 Aspose Imaging 轉換 EMF 檔案可提供 **99 % 版面相似度**，且相較於手動光柵化工具，處理速度提升 **最高 3 倍**（根據供應商在標準 2.5 GHz CPU 上的基準測試）。API 亦會自動處理字型嵌入、色彩管理與向量精度。

## 前置條件
- **Aspose.Imaging for Java** – 版本 25.5 或更新（建議）。  
- **Java Development Kit** 8 或以上。  
- 具備 Maven/Gradle 或手動 JAR 管理的基本知識。  

## 設定 Aspose.Imaging for Java  
要將此函式庫加入專案，請選擇以下相依管理工具之一。

### 使用 Maven  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### 使用 Gradle  

```gradle
implementation 'com.aspose:aspose-imaging:25.5'
```

若手動設定，請從官方發佈頁面 **[此處](https://releases.aspose.com/imaging/java/)** 下載最新的 JAR。

### 取得授權  
Aspose.Imaging for Java 提供免費試用，可在評估期間完整存取 API。當您準備上線時：

- **免費試用：** 無功能限制，僅為暫時的評估期間。([free trial](https://releases.aspose.com/imaging/java/))
- **臨時授權：** 前往 **[此處](https://purchase.aspose.com/temporary-license/)** 取得，以延長測試時間。  
- **購買：** 透過 **[購買頁面](https://purchase.aspose.com/buy)** 取得永久授權。  
- **購買選項：** 詳情請參閱 **[購買選項](https://purchase.aspose.com/buy)**。  

取得 `.lic` 檔案後，於應用程式啟動時載入：

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("Aspose.Imaging.Java.lic");
```

## 實作指南  
我們將說明兩種情境：將文字匯出為 **向量形狀** 與匯出為 **純文字**。每個情境的載入與光柵化步驟相同，僅在 `setTextAsShapes` 旗標上有所差異。

### 如何使用 Aspose Imaging 將 EMF 文字匯出為 SVG 形狀？  
`Image` 為代表任何點陣或向量影像的核心類別，`SvgOptions` 用於設定 SVG 輸出。  
載入 EMF、設定光柵化、啟用形狀轉換，然後儲存。  

**直接回答（40‑70 字）：** 載入 EMF 使用 `Image.load("source.emf")`，設定 `SvgOptions.setTextAsShapes(true)`，然後呼叫 `image.save("output.svg", svgOptions)`。此操作會將每個字形轉換為可縮放的向量路徑，同時保留顏色、線寬與變形。整個流程一次完成，無需額外後處理。

#### 步驟 1：載入來源影像  
`Image` 是在記憶體中代表任何支援的點陣或向量影像的核心類別。  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

#### 步驟 2：設定光柵化選項  
`EmfRasterizationOptions` 讓您設定背景顏色、頁面大小與 DPI。  

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

#### 步驟 3：以文字形狀儲存為 SVG  
`SvgOptions` 控制 SVG 輸出。將 `setTextAsShapes(true)` 設為 true，會強制將文字渲染為向量形狀。  

```java
import com.aspose.imaging.Image;
// Load the source image from a specified directory
Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/picture1.emf");
```

#### 步驟 4：資源管理  
務必呼叫 `image.dispose()`（或使用 try‑with‑resources）以即時釋放原生資源。  

```java
import com.aspose.imaging.imageoptions.EmfRasterizationOptions;
import com.aspose.imaging.Color;

// Create rasterization options for EMF files
final EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions();

// Set the background color to white
emfRasterizationOptions.setBackgroundColor(Color.getWhite());

// Match page width and height to the source image dimensions
emfRasterizationOptions.setPageWidth(image.getWidth());
emfRasterizationOptions.setPageHeight(image.getHeight());
```

### 如何使用 Aspose Imaging 將 EMF 文字匯出為純文字？  
`Image` 載入 EMF，而 `SvgOptions` 決定文字是否保留為字元。  
當需要可編輯的文字時，請停用形狀轉換。  

**直接回答（40‑70 字）：** 載入 EMF 後，建立 `SvgOptions`，將 `setTextAsShapes(false)` 設為 false，然後儲存。產生的 SVG 會將每個字元保留為 `<text>` 元素，保留字型與 Unicode 值，之後可使用任何 SVG 編輯器編輯或以程式處理。

#### 重複步驟 1 與 2  
載入與光柵化程式碼與形狀情境相同。  

```java
import com.aspose.imaging.imageoptions.SvgOptions;

// Save the SVG with text as shapes enabled
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(true); // Text is exported as vector shapes
    }
});
```

#### 步驟 3：以純文字儲存為 SVG  

```java
} finally {
    image.dispose();
}
```

## 實務應用  
- **平面設計：** 形狀模式提供像素完美的向量，用於商標與圖示。  
- **網頁開發：** 純文字 SVG 允許在網頁上搜尋與選取文字。  
- **印刷：** 將 EMF 資產轉換為 SVG，以在任何列印解析度下保持清晰。  

## 效能考量  
- **記憶體管理：** 儲存後立即釋放 `Image` 物件，以降低堆積使用量。  
- **批次處理：** 將檔案分批 10–20 個處理，以平衡 CPU 使用與 GC 開銷。  
- **快取：** 轉換多個設定相同的檔案時，重複使用同一個 `SvgOptions` 實例。  

## 常見問題  
**Q: 如何處理非常大的 EMF 檔案（數百 MB）？**  
A: 透過設定 `EmfRasterizationOptions.setUseMemoryCache(true)` 以串流模式處理，並在儲存後釋放每個影像，以避免記憶體不足錯誤。  

**Q: 我可以自訂 SVG 輸出（例如加入中繼資料或變更命名空間）嗎？**  
A: 可以 – `SvgOptions` 提供 `setMetadata()` 與 `setNamespace()` 等方法，以進行精細控制。  

**Q: 轉換後文字出現亂碼，該檢查什麼？**  
A: 確認來源 EMF 是否嵌入所需字型，或在載入前透過 `FontSettings.setFontsFolder()` 提供缺少的字型。  

**Q: 此函式庫可安全用於商業用途嗎？**  
A: 絕對可以。Aspose.Imaging 已取得開發與生產環境的授權，且不依賴原生元件的執行時相依性。  

**Q: 我可以在哪裡取得社群支援？**  
A: 可在官方 **[Aspose 論壇](https://forum.aspose.com/c/imaging/14)** 發問，或透過支援入口提交工單。  

## 資源  
- **文件說明：** 前往 **[Aspose.Imaging 文件說明](https://reference.aspose.com/imaging/java/)** 探索更深入的資訊。  
- **下載：** 從 **[此處](https://releases.aspose.com/imaging/java/)** 取得最新函式庫版本。  
- **購買與試用：** 查看 **[購買選項](https://purchase.aspose.com/buy)** 與 **[免費試用](https://releases.aspose.com/imaging/java/)** 以開始使用。  

---  

**最後更新：** 2026-06-18  
**測試環境：** Aspose.Imaging for Java 25.5  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學
- [將 EMF 轉換為 PDF（使用 Aspose.Imaging Java）- 步驟指南](/imaging/java/format-conversion-export/convert-emf-to-pdf-aspose-imaging-java/)
- [將 EMF 轉換為 SVG（使用 Aspose.Imaging for Java）：完整指南](/imaging/java/format-conversion-export/convert-emf-to-svg-aspose-imaging-java/)
- [將 EMF 轉換為多種格式（使用 Aspose.Imaging Java）：完整指南](/imaging/java/format-conversion-export/convert-emf-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
// Save the SVG with text as plain text
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_text_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(false); // Text is exported as plain text
    }
});
```