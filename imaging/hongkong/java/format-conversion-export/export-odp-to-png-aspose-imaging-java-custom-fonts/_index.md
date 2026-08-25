---
date: '2026-06-28'
description: 了解如何使用 Aspose.Imaging for Java 將 ODP 轉換為 PNG、設定自訂字型，並停用系統字型以確保渲染精確。
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: 使用 Aspose.Imaging for Java 將 ODP 轉換為 PNG 的方法 – 自訂字型與匯出指南
url: /zh-hant/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 如何使用 Aspose.Imaging for Java 將 ODP 轉換為 PNG – 自訂字型與匯出指南

在現代 Java 應用程式中，將 OpenDocument Presentation（ODP）檔案轉換為高品質 PNG 圖像是常見需求——尤其在需要透過自訂字型保留品牌形象時。本教學說明 **如何將 ODP** 轉換為 PNG，並指導您設定自訂字型資料夾、停用系統備援字型，以及微調光柵化選項以獲得最佳效能。

**您將學習**
- 如何為 ODP 轉換設定自訂字型目錄。  
- 如何停用系統替代字型，使僅使用您選擇的字體。  
- 如何將 ODP 檔案匯出為 PNG，並設定精確的尺寸與字型。  
- 提升大型簡報處理速度與記憶體使用的技巧。

## 快速解答
- **我可以使用 Maven 加入 Aspose.Imaging 嗎？** 是的，加入 Maven 依賴並執行 `mvn install`。  
- **我需要授權才能在正式環境使用嗎？** 需要有效的 Aspose.Imaging 授權才能無限制使用。  
- **我的自訂字型會被遵守嗎？** 設定字型資料夾並停用系統替代字型以強制使用。  
- **支援哪些影像格式？** Aspose.Imaging 支援超過 120 種點陣與向量格式，包括 PNG、JPEG、TIFF 與 WebP。  
- **API 是否為執行緒安全？** 是的，當您為每個執行緒建立獨立實例時，大多數 Aspose.Imaging 類別皆可安全並行使用。

## 什麼是「如何將 odp 轉換」？
*「How to convert odp」* 指的是將 OpenDocument Presentation 檔案轉換為其他格式（常見為 PNG）的過程，同時保留版面配置、字型與視覺忠實度。Aspose.Imaging for Java 提供單一方法工作流程，無需外部工具即可完成此轉換，讓開發者能以最少程式碼直接將轉換整合至應用程式中。

## 為何使用 Aspose.Imaging for Java？
Aspose.Imaging 支援 **120+ 輸出格式**，且能在不將整個文件載入記憶體的情況下光柵化多頁 ODP 檔案，於大型簡報上可將峰值 RAM 使用量降低至 70 %。此函式庫亦提供內建字型管理，免除第三方渲染引擎的需求。

## 前置條件
- **函式庫**：Aspose.Imaging for Java ≥ 25.5。  
- **JDK**：版本 8 或更新。  
- **IDE**：IntelliJ IDEA、Eclipse 或任何相容 Java 的編輯器。  
- **基礎知識**：Java I/O、物件導向程式設計與影像概念。

## 安裝說明

### Maven
將以下相依性加入您的 `pom.xml`，然後執行 `mvn clean install`：

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
在您的 `build.gradle` 檔案中加入函式庫，然後重新整理專案：

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### 直接下載
從 [Aspose.Imaging for Java 版本](https://releases.aspose.com/imaging/java/) 下載最新的 JAR。

## 取得授權步驟
若要解鎖完整功能，請套用臨時或永久授權：

1. **免費試用** – 無需授權，功能受限。  
2. **臨時授權** – 可於 [Aspose 網站](https://purchase.aspose.com/temporary-license/) 申請。  
3. **購買** – 從 [Aspose 購買頁面](https://purchase.aspose.com/buy) 購買訂閱或永久授權。

使用您的授權檔案初始化函式庫：

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## 如何為 ODP 轉換設定自訂字型目錄？
`FontSettings` 是管理 Aspose.Imaging 字型資源的類別。請在任何影像處理開始前載入自訂字型，以確保每張投影片皆使用您提供的精確字體。

使用 Aspose.Imaging 的 `FontSettings` 設定字型資料夾路徑：

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*定義說明*：`FontSettings.setFontsFolder` 告訴 Aspose.Imaging 在檔案系統中尋找 TrueType 與 OpenType 字型的路徑。

## 如何在 ODP 轉換期間停用系統替代字型？
停用系統替代字型會迫使渲染引擎忽略作業系統已安裝的字型，確保僅使用您提供的字型。此舉可消除可能改變投影片視覺外觀的意外字型替換。

使用以下呼叫停用系統替代字型：

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*定義說明*：`FontSettings.setGetSystemAlternativeFont(false)` 強制引擎僅使用您定義資料夾中的字型，消除意外的替換。

## 如何使用指定字型將 ODP 檔案匯出為 PNG？
`RasterizationOptions` 定義向量頁面如何光柵化為點陣圖像。結合字型設定與光柵化選項，即可控制每個匯出 PNG 的 DPI、背景色與頁面尺寸。

依照以下範例實作匯出方法：

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*定義說明*：`RasterizationOptions` 類別控制產生的 PNG 檔案之 DPI、頁面尺寸與背景色。

### 常見陷阱與解決方案
- **缺少字型檔案** – 請確認 ODP 中引用的每個 `.ttf` 或 `.otf` 均存在於您設定的資料夾中。  
- **檔案路徑不正確** – 使用絕對路徑或以 `System.getProperty("user.dir")` 為基礎解析相對路徑。  
- **權限不足** – 確保 Java 程序能讀取字型資料夾並寫入輸出資料夾。

## 實務應用
1. **品牌一致的投影片** – 將簡報匯出為 PNG 用於網站發佈，同時保留企業字型。  
2. **自動化報告產生** – 將每張投影片轉換為影像，以納入 PDF 報告或電子報。  
3. **舊版檔案存檔** – 將 ODP 內容儲存為 PNG，確保未來可在不需 ODP 檢視器的情況下存取。

## 效能考量
- 使用最新的 Aspose.Imaging 版本，以受惠於多執行緒光柵化的改進（在 8 核心 CPU 上可提升至 2 倍速度）。  
- 將影像處理包於 try‑with‑resources 區塊，以確保及時釋放原生資源。  
- 在處理數千張投影片時，調整 `RasterizationOptions`（例如降低 DPI）以在品質與記憶體使用之間取得平衡。

## 常見問答

**問：最低需要哪個 Java 版本？**  
答：Aspose.Imaging for Java 支援 JDK 8 及以上版本；建議使用 JDK 11 以獲得長期支援。

**問：我可以只轉換特定投影片嗎？**  
答：可以，在呼叫 `save` 前設定 `rasterizationOptions.setPageNumber(specificSlideIndex)` 即可。

**問：如何處理受密碼保護的 ODP 檔案？**  
答：使用包含密碼的 `LoadOptions` 載入檔案，然後照常使用相同的字型設定。

**問：停用系統字型會影響效能嗎？**  
答：會略微提升速度，因為引擎會跳過系統字型的查找，於字型數量龐大的機器上尤為明顯。

**問：在哪裡可以找到更多程式碼範例？**  
答：請參閱官方的 [Aspose.Imaging 文件](https://reference.aspose.com/imaging/java/)，了解批次轉換與影像變換等其他情境。

## 其他資源
- [Aspose.Imaging for Java 版本](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging 版本發佈](https://releases.aspose.com/imaging/java/)  
- [開始免費試用](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging 文件](https://reference.aspose.com/imaging/java/)  
- [Aspose.Imaging 論壇](https://forum.aspose.com/c/imaging/14)  
- [購買 Aspose 授權](https://purchase.aspose.com/buy)  
- [申請臨時授權](https://purchase.aspose.com/temporary-license/)  

---

**最後更新:** 2026-06-28  
**測試環境:** Aspose.Imaging for Java 25.5  
**作者:** Aspose

## 相關教學

- [使用 Aspose.Imaging for Java 將 ODG 轉換為 PNG：完整指南](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [使用 Aspose.Imaging 在 Java 中高效影像轉換：完整指南](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}