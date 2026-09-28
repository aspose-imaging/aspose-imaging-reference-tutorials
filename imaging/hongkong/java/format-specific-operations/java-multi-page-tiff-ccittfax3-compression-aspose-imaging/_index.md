---
date: '2026-09-28'
description: 了解如何使用 ccittfax3 compression java 與 Aspose.Imaging 建立多頁 TIFF 檔案。高效掃描、存檔，並減少文件工作流程中的檔案大小。
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: 一步一步探索如何使用 ccittfax3 compression java 搭配 Aspose.Imaging，打造高效的多頁 TIFF
  檔案，用於掃描與存檔。
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: 如何使用 ccittfax3 compression java 建立多頁 TIFF
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: 如何使用 ccittfax3 compression java 建立多頁 TIFF
url: /zh-hant/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 精通使用 ccittfax3 compression java 於 Aspose.Imaging 建立多頁 TIFF

## 介紹

如果您需要在保持檔案尺寸低的情況下歸檔大量掃描文件，**ccittfax3 compression java** 是首選解決方案。本教學將示範如何使用 Aspose.Imaging 在 Java 中以 CCITTFAX3 壓縮產生多頁 TIFF 檔案。您將了解為何此壓縮對單色掃描特別有效、如何設定函式庫，以及如何將每一頁加入為框架。

**您將學習**
- 如何將 Aspose.Imaging 加入 Java 專案。
- 如何為 CCITTFAX3 壓縮設定 `TiffOptions`。
- 如何建立 `TiffImage`、調整來源圖像大小，並將其作為框架加入。
- 如何有效地儲存最終的多頁 TIFF。

讓我們一步步走過完整實作。

## 快速回答
- **CCITTFAX3 壓縮的主要好處是什麼？** 黑白掃描的檔案大小可減少最高 80%。
- **哪個函式庫提供內建支援？** Aspose.Imaging for Java，版本 25.5+。
- **開發時需要授權嗎？** 免費試用授權可使用所有功能；正式上線需購買授權。
- **可以處理數百頁嗎？** 可以——Aspose.Imaging 以串流方式處理頁面，記憶體使用量保持低。
- **程式碼是否相容於 Java 11 及以上版本？** 完全相容；API 目標為 Java 8+。

## ccittfax3 compression java 是什麼？
`CCITTFAX3` 是一種無損的單色壓縮演算法，專為傳真與掃描文件影像設計。它將每個像素編碼為單一位元，提供高品質輸出，同時大幅縮減檔案大小——相較未壓縮的 TIFF 常可減少 70‑80%。此特性使其成為需保留真實度的黑白文件歸檔的理想選擇。

## 為何在此任務使用 Aspose.Imaging？
Aspose.Imaging 支援 **100+** 種輸入與輸出格式，包括 PDF、PNG、JPEG 與 TIFF。其串流架構能處理 **數百頁** 的 TIFF 檔案，而無需將整個文件載入記憶體，非常適合大規模歸檔專案。

## 前置條件
- **Java Development Kit (JDK)** 8 或更新版本已安裝。
- **IDE** 如 IntelliJ IDEA 或 Eclipse。
- **Maven** 或 **Gradle** 用於相依管理。
- 基本的 Java 知識（類別、物件、集合）。

## 設定 Aspose.Imaging for Java
將函式庫加入您的建置檔案。

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```  

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

### 直接下載
您亦可從 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下載最新的 JAR。

### 授權取得
可於 [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/) 取得免費試用授權。正式使用時，請於 [Aspose Purchase](https://purchase.aspose.com/temporary-license/) 購買永久授權或申請臨時授權。

欲了解 API 詳細用法，請參閱 Aspose.Imaging for Java [documentation](https://reference.aspose.com/imaging/java/)。

### 基本初始化
加入相依後，請依下列方式初始化函式庫。

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## 如何為多頁 TIFF 設定 ccittfax3 compression java？
`TiffOptions` 是用來定義 TIFF 檔案輸出格式與壓縮設定的類別。先以 `CCITTGroup3FaxCompression` 列舉載入 `TiffOptions` 物件，接著設定輸出檔案來源。此兩步驟的設定會為單色壓縮做好寫入器準備，並確保之後加入的每一頁皆以 CCITTFAX3 演算法編碼，從而在保留影像品質的同時大幅減少檔案大小。

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## 如何在 Java 中建立 TiffImage 實例？
`TiffImage` 代表記憶體中的多頁 TIFF 文件，並提供操作其框架的方法。首先，定義所有頁面共用的寬度與高度。然後使用先前建立的 `TiffOptions` 例項化 `TiffImage`。`TiffImage` 物件充當各個框架的容器，讓您在儲存最終檔案前能加入、移除或重新排序頁面。

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## 如何從資料夾載入並調整來源圖像大小？
篩選目標目錄中的 JPEG 檔案，讀取每張圖像，並將其調整大小以符合 TIFF 畫布。於加入框架前先調整大小可降低記憶體使用並加速儲存操作。將每個來源圖像轉換為所需的尺寸與像素格式，可確保頁面版面一致，並避免在將框架附加至 TIFF 文件時發生執行時錯誤。

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## 如何將每張圖像作為框架加入多頁 TIFF？
`TiffFrame` 是在 TIFF 中保存單一頁面圖像及其相關中繼資料的物件。遍歷已調整大小的圖像，建立新的 `TiffFrame`，並將其附加至 `TiffImage`。每個框架會成為最終文件中的獨立頁面，函式庫會自動處理必要的中繼資料更新，如頁數與偏移量，確保產生有效的多頁 TIFF 結構。

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## 如何儲存最終的多頁 TIFF 檔案？
在 `TiffImage` 實例上呼叫 `save` 方法，並傳入目標輸出路徑。函式庫會自動以 CCITTFAX3 壓縮寫入所有框架，並有效率地將資料串流至磁碟，同時關閉任何底層資源。儲存完成後，產生的檔案將包含所有頁面且已套用指定的壓縮，隨時可供分發或歸檔使用。

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## 實務應用
- **文件歸檔：** 以最小的儲存開銷保存掃描的合約、發票或法律紀錄。
- **醫學影像：** 壓縮放射影像同時保留診斷細節。
- **印刷製作：** 產生印表機可直接使用的多頁列印工作。

## 效能考量
- 使用保留長寬比的 `ResizeOptions` 以避免變形。
- 在加入框架後關閉每個 `Image` 物件，以釋放原生記憶體。
- 對於極大量批次，請使用平行串流處理檔案，並非同步寫入每個 TIFF 段落。

## 常見陷阱與故障排除
- **像素格式不正確：** CCITTFAX3 僅支援 1 位元（黑白）圖像。請在調整大小前將彩色圖像轉為灰階。
- **記憶體洩漏：** 必須對暫時的 `Image` 物件呼叫 `dispose()`，否則原生緩衝區會持續佔用。
- **檔案大小未減少：** 請確認已設定 `TiffOptions` 的 compression 屬性，否則會使用預設（無壓縮）。

## 常見問答
**問：我可以將此方法用於彩色圖像嗎？**  
**答：CCITTFAX3 僅限於單色資料；若需彩色，請改用 JPEG 或 LZW 壓縮。**

**問：Aspose.Imaging 是否支援巨型 TIFF 的串流？**  
**答：是的——函式庫會直接將每個框架寫入輸出串流，即使是上千頁也能保持低記憶體使用。**

**問：如何以程式方式套用臨時授權？**  
**答：載入 `.lic` 檔案，例如 `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`。**

**問：有沒有方法在儲存前預覽 TIFF？**  
**答：可以將每個 `TiffFrame` 轉換為 `BufferedImage`，再於 Swing 元件中顯示。**

**問：官方支援哪些 Java 版本？**  
**答：Aspose.Imaging 支援 Java 8 至 Java 21（含 LTS 版）。**

## 結論
您現在已掌握使用 **ccittfax3 compression java** 於 Aspose.Imaging 建立多頁 TIFF 檔案的完整、可投入生產的工作流程。依循上述步驟，即可高效歸檔龐大的文件集合，同時降低儲存成本並保持高影像品質。進一步探索 Aspose.Imaging 的其他功能——如 OCR、元資料處理與格式轉換——以進一步強化您的文件處理管線。

---

**Last Updated:** 2026-09-28  
**Tested With:** Aspose.Imaging 25.5 for Java  
**Author:** Aspose

## 相關教學

- [How to Create Multi-Page TIFF with Aspose.Imaging for Java – A Complete Guide](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [How to Reduce Image File Size with LZW Compression in Java](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Split Multi Page TIFF Frames with Aspose.Imaging for Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}