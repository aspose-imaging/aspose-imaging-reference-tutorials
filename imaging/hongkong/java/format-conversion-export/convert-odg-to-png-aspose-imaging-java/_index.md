---
date: '2026-04-05'
description: 學習如何使用 Aspose.Imaging for Java 將 ODG 檔案轉換為 PNG，內容包括向量 PNG 轉換、在 Java 中儲存
  PNG，以及臨時 Aspose 授權設定。
keywords:
- how to use aspose
- convert vector png
- maven aspose imaging
- convert odg png
- save png java
- temporary aspose license
title: 如何使用 Aspose.Imaging for Java：將 ODG 轉換為 PNG – 完整指南
url: /zh-hant/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 如何使用 Aspose.Imaging for Java：將 ODG 檔案轉換為 PNG

## 介紹

您是否在使用 Java 將 OpenDocument Graphics（ODG）檔案轉換為高品質 PNG 圖像時感到困難？您並不孤單！許多開發人員都需要一種可靠的方式 **將 ODG 轉換為 PNG**，同時保持圖形的清晰度。在本教學中，我們將示範 **如何使用 Aspose.Imaging for Java** 來載入 ODG 檔案、設定光柵化選項，並將其儲存為 PNG。完成後，您將熟悉整個工作流程，並了解為何此方法在向量轉光柵的轉換中更受青睞。

### 快速回答
- **哪個函式庫負責 ODG → PNG 轉換？** Aspose.Imaging for Java。  
- **需要授權嗎？** 臨時 Aspose 授權可用於評估；正式環境需購買完整授權。  
- **建議使用哪種建置工具？** Maven（或 Gradle）——請參考下方 *maven aspose imaging* 片段。  
- **可以控制 PNG 品質嗎？** 可以，透過 `OdgRasterizationOptions` 與 `PngOptions`。  
- **程式碼相容於 Java 8+ 嗎？** 絕對相容——可在現代 JDK 上執行。

## 使用 Aspose 轉換 ODG 為 PNG 的流程是什麼？

將 ODG 檔案轉換為 PNG 只需三個簡單步驟：

1. **載入** ODG 文件，使用 Aspose.Imaging。  
2. **設定** 光柵化選項，以在所需解析度下渲染向量圖形。  
3. **儲存** 光柵化後的影像為 PNG 檔案。

此流程可讓您 **可靠地轉換向量 png** 內容，且相同模式亦可套用於 Aspose 支援的其他向量格式。

## 為什麼選擇 Aspose.Imaging for Java？

- **完整格式支援** – ODG、SVG、EMF 等多種格式。  
- **高效能光柵化** – 可微調 DPI、頁面尺寸與色彩深度等選項。  
- **無外部相依** – 純 Java 實作，適合伺服器端處理。  
- **授權便利** – 可先使用臨時授權，之後再升級為正式授權。

## 前置條件

- **Aspose.Imaging for Java** 版本 25.5 或更新（建議使用最新版本）。  
- 已在開發機上安裝 **JDK 8+**。  
- 具備 Maven 或 Gradle 的基本使用經驗，以管理相依性。  
- 有效的 **臨時 Aspose 授權** 或正式授權檔案。

## 設定 Aspose.Imaging for Java

### 安裝資訊

使用您偏好的建置工具將函式庫加入專案。

**Maven**（*maven aspose imaging* 方式）  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

**直接下載：** 也可從官方發佈頁面取得 JAR 檔案：[Aspose.Imaging for Java 版本發佈](https://releases.aspose.com/imaging/java/)。

### 授權取得

開始之前，請設定 **臨時 Aspose 授權**（或正式授權），以免 API 受評估限制：

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path/to/your/license.lic");
```

## 實作指南

### 載入 ODG 檔案

首先，匯入核心 `Image` 類別並載入 ODG 文件：

```java
import com.aspose.imaging.Image;
```

```java
String fileName = "YOUR_DOCUMENT_DIRECTORY/example.odg";
try (Image image = Image.load(fileName)) {
    // Further processing will occur here
}
```

### 設定光柵化選項

建立 `OdgRasterizationOptions` 實例，並定義輸出尺寸：

```java
import com.aspose.imaging.imageoptions.OdgRasterizationOptions;

OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
```

```java
rasterizationOptions.setPageSize(new SizeF(image.getWidth(), image.getHeight()));
```

### 儲存為 PNG 影像

設定 `PngOptions` 使用光柵化設定，然後將結果儲存：

```java
import com.aspose.imaging.imageoptions.PngOptions;

String outFileName = "YOUR_OUTPUT_DIRECTORY/example.png";
image.save(outFileName, new PngOptions() {
{
    setVectorRasterizationOptions(rasterizationOptions);
}
});
```

## 疑難排解技巧

- 確認 ODG 檔案路徑正確且檔案可存取。  
- 確保使用 **Aspose.Imaging 25.5** 或更新版本；舊版可能不支援完整 ODG 功能。  
- 若 PNG 品質偏低，請在 `OdgRasterizationOptions` 中增大頁面尺寸或 DPI。  
- 記得關閉影像資源（`try‑with‑resources` 區塊會自動處理）。

## 實務應用

1. **網站開發：** 將向量圖形轉為 PNG，以確保在各瀏覽器上的一致呈現。  
2. **文件存檔：** 透過轉換將舊有 ODG 插圖保存為廣泛支援的 PNG 格式。  
3. **出版與印刷：** 從 ODG 設計檔產生適合列印的 PNG 圖檔。

## 效能考量

- **記憶體管理：** 大型 ODG 檔案可能佔用大量記憶體，請一次處理單一檔案並及時釋放資源。  
- **資源利用率：** 使用上方示範的 `try‑with‑resources` 模式以避免記憶體泄漏。  
- **品質與速度的平衡：** 較高 DPI 會產生更銳利的 PNG，但會增加處理時間——請依使用情境選擇適當設定。

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| *找不到檔案* | 再次確認檔案路徑，並確保副檔名為 `.odg`。 |
| *輸出 PNG 模糊* | 增加 `PageSize` 尺寸或在 `OdgRasterizationOptions` 中設定更高 DPI。 |
| *授權未生效* | 檢查授權檔案路徑，並確保在任何影像操作之前初始化 `License` 類別。 |
| *OutOfMemoryError* | 逐一處理檔案，必要時提升 JVM 堆積大小（`-Xmx`）。 |

## 常見問答

1. **如何取得 Aspose.Imaging 的臨時授權？**  
   - 前往 [臨時授權頁面](https://purchase.aspose.com/temporary-license/) 申請。

2. **可以使用 Aspose.Imaging 批次轉換影像嗎？**  
   - 可以，您可以遍歷 ODG 檔案目錄，對每個檔案套用相同的轉換邏輯。

3. **如果 PNG 輸出品質不如預期該怎麼辦？**  
   - 檢查光柵化設定（頁面尺寸、DPI），確保與來源尺寸相符。

4. **Aspose.Imaging for Java 可以免費使用嗎？**  
   - 提供試用版，但正式功能與生產環境需購買授權。

5. **在哪裡可以找到更多 Aspose.Imaging 的文件？**  
   - 完整指南與 API 參考可於 [Aspose 文件中心](https://reference.aspose.com/imaging/java/) 取得。

## 其他常見問答

**Q: 可以在不使用 Gradle 的 Maven 專案中使用此程式碼嗎？**  
A: 當然可以——上方的 Maven 相依性片段已足夠。

**Q: 函式庫是否支援其他向量格式，例如 SVG？**  
A: 支援，Aspose.Imaging 可光柵化 SVG、EMF、WMF 等多種向量格式。

**Q: 如何為 PNG 輸出設定自訂 DPI？**  
A: 在儲存前，於 `OdgRasterizationOptions` 上調整 `Resolution` 屬性。

**Q: 有沒有方法批次處理多個 ODG 檔案？**  
A: 可將載入、光柵化與儲存的程式碼放入迴圈，遍歷目錄中的檔案。

**Q: 本教學測試使用的版本是？**  
A: 本程式碼已於 Aspose.Imaging for Java 25.5 版本測試通過。

## 資源

- **文件參考：** [Aspose.Imaging for Java 參考文件](https://reference.aspose.com/imaging/java/)  
- **下載：** [最新發佈版](https://releases.aspose.com/imaging/java/)  
- **購買授權：** [購買授權](https://purchase.aspose.com/buy)  
- **免費試用：** [試用 Aspose.Imaging](https://releases.aspose.com/imaging/java/)  
- **臨時授權申請：** [申請臨時授權](https://purchase.aspose.com/temporary-license/)  
- **支援論壇：** [Aspose 支援社群](https://forum.aspose.com/c/imaging/14)

---

**最後更新：** 2026-04-05  
**測試環境：** Aspose.Imaging for Java 25.5  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}