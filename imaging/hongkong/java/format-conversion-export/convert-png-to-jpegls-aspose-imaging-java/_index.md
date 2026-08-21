---
date: '2026-04-05'
description: 學習如何使用 Aspose Imaging Java 將 PNG 圖像轉換為 JPEG‑LS，涵蓋設定、轉換步驟以及提升 Java 圖像壓縮效率的技巧。
keywords:
- aspose imaging java
- how to convert png
- java image compression
- convert png to jpeg-ls
- load png image java
title: Aspose Imaging Java：輕鬆將 PNG 轉換為 JPEG-LS
url: /zh-hant/java/format-conversion-export/convert-png-to-jpegls-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 標題：掌握 Aspose Imaging Java 圖像轉換：將 PNG 轉換為 JPEG‑LS

## 介紹

在處理圖像處理時，您可能會遇到在不影響品質的前提下優化檔案大小的需求。這時，將圖像從一種格式轉換為另一種格式就變得至關重要。使用 **Aspose Imaging Java**，您可以輕鬆地將每個樣本 8 位元的 PNG 圖像轉換為僅使用 2 位元每樣本的 JPEG‑LS 格式。在本教學中，我們將逐步說明整個流程，解釋其重要性，並提供您可立即應用的實用技巧。

**您將學會：**
- 如何在專案中設定 Aspose Imaging for Java
- 將 PNG 圖像轉換為 JPEG‑LS 格式的流程
- 將 JPEG‑LS 轉回 PNG 以進行比較
- 主要設定選項、常見陷阱與疑難排解技巧

在深入實作之前，讓我們先了解開始所需的前置條件。

## 快速答覆
- **哪個函式庫負責轉換？** Aspose Imaging Java
- **涉及哪些格式？** PNG → JPEG‑LS 和 JPEG‑LS → PNG
- **典型的壓縮增益？** 可減少高達 80 % 的檔案大小，同時保持無損
- **最低 Java 版本？** JDK 8 或以上
- **測試是否需要授權？** 免費試用或臨時授權即可用於開發

## 什麼是 Aspose Imaging Java？
Aspose Imaging Java 是一個功能強大的 API，讓開發人員能以程式方式讀取、編輯與轉換各種圖像格式。它支援如 JPEG‑LS 等先進的壓縮方案，非常適合圖像保真度與檔案大小效率同等重要的情境。

## 為何使用 Aspose Imaging Java 進行 PNG 轉 JPEG‑LS 轉換？
- **無損或近無損壓縮** – JPEG‑LS 能完整保留每個像素細節。
- **簡易 API** – 幾行程式碼即可完成載入、設定與儲存。
- **跨平台** – 可在任何支援 Java 的作業系統上執行。
- **企業級** – 從單一圖像操作擴展至批次處理管線皆可。

## 前置條件 (H2)
為了有效跟隨本教學，請確保您具備以下條件：
- 基本的 Java 程式設計知識。
- 如 IntelliJ IDEA 或 Eclipse 等整合開發環境 (IDE)。
- 已安裝 Maven 或 Gradle 以管理相依性。
- 熟悉圖像處理概念與檔案格式。

## 為 Java 設定 Aspose Imaging (H2)

**安裝：**

若要在 Java 中使用 Aspose Imaging，您需要將其作為相依性加入專案。以下示範如何使用 Maven 或 Gradle 進行設定：

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
implementation(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

或者，您也可以直接從 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下載最新版本。

### 授權取得

若要開始使用 Aspose Imaging，建議取得免費試用或購買授權：
- **免費試用**：可免費探索功能。
- **臨時授權**：可透過 [Temporary License page](https://purchase.aspose.com/temporary-license/) 取得，以延長評估期間的使用。
- **購買**：長期使用時，可直接從 [Aspose’s Purchase Page](https://purchase.aspose.com/buy) 購買。

**基本初始化：**
將 Aspose Imaging 加入專案後，請進行初始化以確保所有功能皆可使用：

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path/to/your/license.lic");
```

## 使用 Aspose Imaging Java 進行 PNG 轉 JPEG‑LS 轉換 (H2)

### 將 PNG 轉換為 JPEG‑LS (H2)

此功能可將每個樣本 8 位元的 PNG 圖像壓縮為更有效率的每樣本 2 位元 JPEG‑LS 格式。

#### 概述
JPEG‑LS 以其無損與近無損壓縮能力聞名，適合在減少檔案大小的同時保存高品質圖像。本節將說明如何使用 Aspose Imaging 將 PNG 轉換為此格式。

#### 實作步驟

##### 載入原始 PNG 圖像 (H3)
首先載入來源 PNG 圖像：

```java
String originPngFileName = "YOUR_DOCUMENT_DIRECTORY/lena24b.png";
PngImage pngImage = (PngImage) Image.load(originPngFileName);
```
*為何？*: 載入圖像可讓您使用 Aspose Imaging 強大的 API 進行存取與操作。

##### 設定 JPEG 選項 (H3)
設定轉換所需的選項：

```java
int bpp = 2; // Bits per sample
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setBitsPerChannel((byte) bpp);
jpegOptions.setCompressionType(JpegCompressionMode.JpegLs);
```
*為何？*: 設定這些選項可指定輸出 JPEG‑LS 圖像的壓縮類型與品質參數。

##### 儲存圖像 (H3)
最後，儲存已轉換的圖像：

```java
String outputJpegFileName = "YOUR_OUTPUT_DIRECTORY/lena24b 2-bit Gold.jls";
pngImage.save(outputJpegFileName, jpegOptions);
```
*為何？*: 以特定格式儲存即完成轉換流程。

##### 資源管理 (H3)
處理完畢後確保釋放資源：

```java
finally {
    pngImage.dispose();
}
```
*為何？*: 釋放圖像物件有助於有效管理記憶體使用。

#### 疑難排解技巧
- **常見問題**：如果遇到 `FileNotFoundException`，請再次確認輸入與輸出檔案的路徑。
- **解決提示**：確保您的 IDE 具備對指定目錄的讀寫權限。

### 將 JPEG‑LS 轉換為 PNG (H2)

此功能可將 JPEG‑LS 圖像轉回 PNG 格式，方便視覺比較或進一步處理。

#### 概述
將圖像轉換為 JPEG‑LS 以壓縮後，可能需要將其還原，以評估品質或其他用途。本節說明如何使用 Aspose Imaging 完成此操作。

#### 實作步驟

##### 載入 JPEG‑LS 圖像 (H3)
首先載入 JPEG‑LS 檔案：

```java
String inputJpegFileName = "YOUR_OUTPUT_DIRECTORY/lena24b 2-bit Gold.jls";
JpegImage jpegImage = (JpegImage) Image.load(inputJpegFileName);
```
*為何？*: 載入圖像可為轉換至其他格式做準備。

##### 儲存為 PNG (H3)
將圖像轉換並儲存為 PNG 格式：

```java
String outputPngFileName = "YOUR_OUTPUT_DIRECTORY/lena24b 2-bit Gold.png";
jpegImage.save(outputPngFileName, new PngOptions());
```
*為何？*: 此步驟確保您的 JPEG‑LS 檔案轉回廣泛相容且無損的 PNG 格式。

##### 資源管理 (H3)
儲存後釋放圖像資源：

```java
finally {
    jpegImage.dispose();
}
```
*為何？*: 正確釋放可避免記憶體洩漏，維持應用程式效能。

## 實務應用 (H2)

1. **醫學影像** – JPEG‑LS 常用於醫學影像，因其高效的無損壓縮，可保留關鍵診斷細節。
2. **高品質影像存檔** – 檔案庫可以最小的儲存開銷保存高解析度影像。
3. **網頁開發** – 在不失真情況下降低圖像檔案大小，可提升頁面載入速度與使用者體驗。
4. **數位攝影** – 攝影師可在不影響真實度的前提下壓縮作品集。
5. **平面設計** – 設計師常需兼顧品質與檔案大小的格式，以適應各種媒體輸出。

## 效能考量 (H2)

- **最佳化記憶體使用** – 總是使用 `dispose()` 方法釋放圖像，以即時釋放資源。
- **批次處理** – 對於大型資料集，請以批次方式處理圖像，以管理記憶體消耗。
- **平行執行** – 利用 Java 的併發工具進行平行圖像處理，提升吞吐量。

## 常見問題與解決方案 (H2)

| 症狀 | 可能原因 | 解決方式 |
|---------|--------------|-----|
| `FileNotFoundException` | 檔案路徑不正確 | 核實絕對/相對路徑與資料夾權限 |
| 記憶體不足錯誤 | 以順序方式處理大型圖像 | 使用批次處理或增加 JVM 堆積大小 (`-Xmx`) |
| 輸出檔案損毀 | 缺少 `dispose()` 呼叫 | 確保在 `finally` 區塊中釋放圖像物件 |

## 常見問答 (H2)

**問：使用 Aspose Imaging 的系統需求是什麼？**  
答：Aspose Imaging 可在任何支援 Java 的平台上運行，需 JDK 8 或以上。

**問：我可以在開源專案中使用 Aspose Imaging 嗎？**  
答：可以，但必須遵守 Aspose 提供的授權條款。

**問：若圖像檔案在轉換過程中損毀會發生什麼？**  
答：在處理前驗證輸入檔案，並捕捉例外以優雅地處理錯誤。

**問：如何處理除每樣本 2 位元外的其他位深？**  
答：調整 `setBitsPerChannel()` 參數為所需的位深。

**問：Aspose Imaging 是否相容所有 Java IDE？**  
答：是的，支援常見的 IDE 如 IntelliJ IDEA、Eclipse 與 NetBeans。

## 資源

- [Aspose.Imaging for Java 文件說明](https://reference.aspose.com/imaging/java/)
- [下載 Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/)
- [購買授權](https://purchase.aspose.com/buy)
- [免費試用存取](https://releases.aspose.com/imaging/java/)
- [臨時授權申請](https://purchase.aspose.com/temporary-license/)
- [社群支援論壇](https://forum.aspose.com/c/imaging/14)

透過本完整指南，您已具備高效處理 PNG 轉 JPEG‑LS 以及相反轉換的能力，使用 **Aspose Imaging Java**。祝開發愉快！

---

**最後更新：** 2026-04-05  
**測試環境：** Aspose Imaging 25.5 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}