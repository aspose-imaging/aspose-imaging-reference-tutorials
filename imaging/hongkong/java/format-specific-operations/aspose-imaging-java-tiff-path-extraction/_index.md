---
date: '2026-09-02'
description: 了解如何使用 Aspose.Imaging for Java 建立裁剪路徑並從 TIFF 圖像中提取。按照一步一步的說明，將 TIFF 高效轉換為
  PSD。
keywords:
- create clipping path
- how to extract path
- how to convert tiff
- aspose imaging java
- convert tiff to psd
lastmod: '2026-09-02'
og_description: 了解如何使用 Aspose.Imaging for Java 建立裁剪路徑並從 TIFF 圖像中提取。按照一步一步的程式碼，將 TIFF
  轉換為 PSD。
og_image_alt: Guide showing how to create clipping path in TIFF using Aspose.Imaging
  Java
og_title: 使用 Aspose.Imaging for Java 在 TIFF 中建立裁剪路徑
schemas:
- author: Aspose
  dateModified: '2026-09-02'
  description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  headline: Create clipping path in TIFF with Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  name: Create clipping path in TIFF with Aspose.Imaging for Java
  steps:
  - name: '**Free trial** – start with a 30‑day trial.'
    text: '**Free trial** – start with a 30‑day trial.'
  - name: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
    text: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
  - name: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
    text: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
  - name: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
    text: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
  - name: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
    text: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
  type: HowTo
- questions:
  - answer: Yes, provided you have a valid commercial license; a free trial is available
      for evaluation.
    question: Can I use Aspose.Imaging for Java in a commercial application?
  - answer: The library supports over 100 formats, including TIFF, PSD, BMP, JPEG,
      PNG, and many more.
    question: What image formats does Aspose.Imaging support?
  - answer: Verify that the source TIFF actually contains vector path resources; use
      the `hasPathResources()` check before extraction.
    question: How do I troubleshoot path extraction errors?
  - answer: Absolutely – combine the extraction code with Java’s parallel streams
      or an executor service to handle many files efficiently.
    question: Is batch processing of multiple TIFFs possible?
  - answer: Complex shapes may need manual adjustment after creation; the API handles
      standard Bezier curves and straight lines reliably.
    question: Are there limitations when creating clipping paths in TIFF?
  type: FAQPage
tags:
- create clipping path
- TIFF processing
- Aspose.Imaging
- Java image manipulation
- PSD conversion
title: 使用 Aspose.Imaging for Java 在 TIFF 中建立裁剪路徑
url: /zh-hant/java/format-specific-operations/aspose-imaging-java-tiff-path-extraction/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 TIFF 中使用 Aspose.Imaging for Java 建立裁切路徑

在本完整指南中，您將學習如何在 TIFF 檔案中 **建立裁切路徑**，以及如何使用 Aspose.Imaging for Java 提取現有路徑。完成後，您將能將 TIFF 圖像轉換為可完全編輯的 PSD 檔案，讓其可在 Photoshop 或任何支援向量的編輯器中使用。

## 快速解答
- **什麼是裁切路徑？** 定義圖像透明與不透明區域的向量輪廓。  
- **我可以從 TIFF 中提取現有路徑嗎？** 可以 — Aspose.Imaging 能讀取嵌入的路徑資源並將其儲存為 PSD。  
- **如何新增裁切路徑？** 建立 `PathResource`，以向量記錄填充，並指派給圖像的活動框架。  
- **生產環境需要授權嗎？** 商業部署需要有效的 Aspose.Imaging 授權。  
- **需要哪個 Java 版本？** JDK 8 或以上；此函式庫支援 Java 11、17 及更高版本。

## 什麼是裁切路徑？
裁切路徑是一種基於向量的輪廓，告訴渲染引擎顯示或隱藏圖像的哪些部分。它以路徑資源的形式儲存在 TIFF 或 PSD 檔案中，且可在 Adobe Photoshop 中編輯。

## 為什麼要將 TIFF 轉換為 PSD？
將 TIFF 轉換為 PSD 可實現無損編輯圖層、遮色片與裁切路徑。Aspose.Imaging 支援 **50+ 輸入與輸出格式**，且能在不將整個檔案載入記憶體的情況下處理數百頁的 TIFF，提供高效能的批次轉換。

## 前置條件
- **Java Development Kit (JDK)** 8 或更新版本已安裝。  
- **Aspose.Imaging for Java** 函式庫（透過 Maven、Gradle 或直接下載加入）。  
- 具備基本的 Java 程式概念。

## 如何設定 Aspose.Imaging for Java
在加入任何程式碼之前，請確保函式庫已在建置系統中正確引用，且您擁有有效的授權檔案。這可確保 API 在無評估限制的情況下運作，並且所有功能（包括路徑操作）皆可使用。

### Maven
在您的 `pom.xml` 檔案中加入以下相依性：
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle
在您的 `build.gradle` 檔案中加入此行：
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### 直接下載
從 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下載最新版本。

#### 取得授權
1. **免費試用** – 開始 30 天的試用。  
2. **臨時授權** – 從 [temporary license page](https://purchase.aspose.com/temporary-license/) 取得。  
3. **購買** – 在 [Aspose's website](https://purchase.aspose.com/buy) 購買完整授權。

安裝並授權後，在您的專案中初始化 Aspose.Imaging：
```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path_to_license_file");
```

## 如何從 TIFF 提取裁切路徑？
提取裁切路徑的過程包括載入 TIFF、定位任何嵌入的路徑資源，並將這些資源寫入新的 PSD 檔案。此流程直接從來源圖像讀取向量資料，保留精確度且避免光柵化轉換。

載入 TIFF，遍歷其路徑資源，並將結果儲存為 PSD。此操作一次性讀取嵌入的向量資料並寫入新檔案。
```java
String filePath = "YOUR_DOCUMENT_DIRECTORY/SupportExtractingPathsFromTiff/Sample.tif";
try (TiffImage image = (TiffImage) com.aspose.imaging.Image.load(filePath)) {
    // Proceed with extraction steps...
}
```

遍歷活動框架中的路徑資源並收集它們：
```java
for (PathResource path : image.getActiveFrame().getPathResources()) {
    System.out.println(path.getName());  // Output the name of each path resource found.
}
```

將帶有提取路徑的圖像儲存為新的 PSD 檔案：
```java
String outFilePath = "YOUR_OUTPUT_DIRECTORY/SampleWithPaths.psd";
image.save(outFilePath);
```

## 如何在 TIFF 中建立裁切路徑？
建立裁切路徑需要構造一個描述所需向量輪廓的 `PathResource`，將其附加到 TIFF 的活動框架，然後將圖像（或其副本）儲存為 PSD，以保留路徑。此方法允許您以程式方式向光柵檔案添加向量遮罩。

PathResource 代表儲存在圖像檔案內的向量路徑。  
使用所需屬性初始化新的 `PathResource`：
```java
final PathResource pathResource = new PathResource();
pathResource.setBlockId((short) 2000); // Set Block ID per Photoshop specs
pathResource.setName("My Clipping Path"); // Name your clipping path for easy identification

// Create and add vector path records using the provided coordinates.
pathResource.setRecords(createRecords(0.2f, 0.2f, 0.8f, 0.2f, 0.8f, 0.8f, 0.2f, 0.8f));
```

將建立的路徑資源指派給圖像的活動框架：
```java
List<PathResource> list = new LinkedList<>();
list.add(pathResource);
image.getActiveFrame().setPathResources(list);
```

將修改後的 TIFF 儲存為包含裁切路徑的 PSD：
```java
String outFilePath2 = "YOUR_OUTPUT_DIRECTORY/ImageWithPath.psd";
image.save(outFilePath2);
```

## 輔助方法

### 建立記錄
使用貝塞爾節點與長度記錄產生向量路徑記錄：
```java
private static List<VectorPathRecord> createRecords(float ... coordinates) {
    List<VectorPathRecord> records = createBezierRecords(coordinates); 
    LengthRecord lr = new LengthRecord();
    lr.setOpen(false);
    lr.setRecordCount(records.size());
    
    records.add(0, lr);
    return records;
}
```

### 建立貝塞爾記錄
將座標陣列轉換為貝塞爾向量路徑記錄：
```java
private static List<VectorPathRecord> createBezierRecords(float[] coordinates) {
    final List<VectorPathRecord> list = new LinkedList<>();
    
    for (int index = 0; index < coordinates.length - 1; index += 2) {
        PointF point = new PointF(coordinates[index], coordinates[index + 1]);
        list.add(createBezierRecord(point));
    }
    
    return list;
}
```

### 建立單一貝塞爾記錄
定義單一貝塞爾節點向量路徑記錄：
```java
private static VectorPathRecord createBezierRecord(PointF point) {
    BezierKnotRecord it = new BezierKnotRecord();
    it.setPathPoints(new PointF[] { point, point, point });
    return it;
}
```

## 實務應用
1. **平面設計工作流程** – 將 TIFF 轉換為 PSD，以在 Photoshop 中編輯圖層與遮色片。  
2. **自動化影像管線** – 批次處理數千個 TIFF，即時提取或新增路徑。  
3. **資料驅動的視覺化** – 使用向量路徑從光柵來源生成精確的圖表或示意圖。

## 效能考量
- **記憶體管理** – 使用 try‑with‑resources 確保即時釋放圖像物件。  
- **批次處理** – 使用 Java 的 `ForkJoinPool` 平行化轉換，以處理大型圖像集合。  
- **解析度處理** – 僅在必要時調整 DPI，以在保持品質的同時降低處理時間。

## 結論
您現在已了解如何在 TIFF 檔案中 **建立裁切路徑**，以及使用 Aspose.Imaging for Java 提取現有路徑。這些技術讓您能將高階影像操作整合至任何基於 Java 的工作流程，無論是桌面工具還是企業級處理管線。

### 後續步驟
- 嘗試不同的向量形狀與路徑屬性。  
- 探索其他 Aspose.Imaging 功能，如浮水印、格式轉換與中繼資料處理。

## 常見問題

**Q: 我可以在商業應用程式中使用 Aspose.Imaging for Java 嗎？**  
A: 可以，只要您擁有有效的商業授權；亦提供免費試用供評估。

**Q: Aspose.Imaging 支援哪些影像格式？**  
A: 此函式庫支援超過 100 種格式，包括 TIFF、PSD、BMP、JPEG、PNG 等等。

**Q: 如何排除路徑提取錯誤？**  
A: 確認來源 TIFF 確實包含向量路徑資源；在提取前使用 `hasPathResources()` 檢查。

**Q: 能否批次處理多個 TIFF？**  
A: 完全可以 — 將提取程式碼與 Java 的平行串流或執行服務結合，以高效處理大量檔案。

**Q: 在 TIFF 中建立裁切路徑有什麼限制嗎？**  
A: 複雜形狀可能在建立後需要手動調整；API 能可靠處理標準的貝塞爾曲線與直線。

---

**最後更新：** 2026-09-02  
**測試環境：** Aspose.Imaging for Java 24.12  
**作者：** Aspose  

## 資源

- [Aspose.Imaging 文件](https://reference.aspose.com/imaging/java/)
- [下載 Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/)
- [購買授權](https://purchase.aspose.com/buy)
- [免費試用](https://releases.aspose.com/imaging/java/)
- [臨時授權](https://purchase.aspose.com/temporary-license/)
- [Aspose 支援論壇](https://forum.aspose.com/c/imaging/14)

## 相關教學

- [使用 Aspose.Imaging for Java 將影像轉換為 PSD – 步驟指南](/imaging/java/format-conversion-export/convert-images-to-psd-using-aspose-imaging-java-guide/)
- [如何使用 Aspose.Imaging Java 將 TIFF 轉換為 GraphicsPath](/imaging/java/advanced-drawing-graphics/aspose-imaging-java-tiff-graphicspath-conversion/)
- [使用 Aspose.Imaging 在 Java 中高效載入與儲存 TIFF 影像](/imaging/java/image-loading-saving/aspose-imaging-java-tiff-image-saving/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}