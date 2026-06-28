---
date: '2026-06-28'
description: 了解如何使用 Aspose.Imaging for Java 将 ODP 转换为 PNG，设置自定义字体，并禁用系统字体以实现准确渲染。
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
title: 如何使用 Aspose.Imaging for Java 将 ODP 转换为 PNG – 自定义字体与导出指南
url: /zh/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 如何使用 Aspose.Imaging for Java 将 ODP 转换为 PNG – 自定义字体与导出指南

在现代 Java 应用程序中，将 OpenDocument Presentation（ODP）文件转换为高质量 PNG 图像是常见需求——尤其是在需要通过自定义字体保持品牌形象时。本教程展示了 **如何将 ODP 转换为 PNG**，并指导您设置自定义字体文件夹、禁用系统回退字体以及微调光栅化选项以获得最佳性能。

**您将学习**
- 如何为 ODP 转换设置自定义字体目录。  
- 如何禁用系统替代字体，以便仅使用您选择的字体。  
- 如何使用精确的尺寸和字体设置将 ODP 文件导出为 PNG。  
- 在处理大型演示文稿时提升速度和内存使用的技巧。  

## 快速回答
- **我可以使用 Maven 添加 Aspose.Imaging 吗？** 是的，添加 Maven 依赖并运行 `mvn install`。  
- **生产环境需要许可证吗？** 需要有效的 Aspose.Imaging 许可证才能无限制使用。  
- **我的自定义字体会被尊重吗？** 设置字体文件夹并禁用系统替代字体即可强制使用。  
- **支持哪些图像格式？** Aspose.Imaging 支持 120 多种光栅和矢量格式，包括 PNG、JPEG、TIFF 和 WebP。  
- **API 是线程安全的吗？** 是的，大多数 Aspose.Imaging 类在为每个线程创建独立实例时是并发安全的。  

## 什么是 “how to convert odp”？
*“How to convert odp”* 指将 OpenDocument Presentation 文件转换为另一种格式（通常为 PNG）的过程，同时保留布局、字体和视觉保真度。Aspose.Imaging for Java 提供单方法工作流，无需外部工具即可完成此转换，使开发者能够以最少的代码将转换直接集成到应用程序中。

## 为什么使用 Aspose.Imaging for Java？
Aspose.Imaging 支持 **120 多种输出格式**，并且能够在不将整个文档加载到内存中的情况下光栅化多页 ODP 文件，在大型演示文稿中将峰值内存使用降低最多 70%。该库还提供内置字体管理，免除对第三方渲染引擎的需求。

## 前提条件
- **库**：Aspose.Imaging for Java ≥ 25.5。  
- **JDK**：8 版或更高。  
- **IDE**：IntelliJ IDEA、Eclipse 或任何兼容 Java 的编辑器。  
- **基础知识**：Java I/O、面向对象编程和图像概念。  

## 安装说明

### Maven
在 `pom.xml` 中添加以下依赖并运行 `mvn clean install`：

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
在 `build.gradle` 文件中包含该库并刷新项目：

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### 直接下载
从 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下载最新的 JAR。

## 获取许可证的步骤
要解锁全部功能，请申请临时或永久许可证：

1. **免费试用** – 无需许可证，功能受限。  
2. **临时许可证** – 在 [Aspose website](https://purchase.aspose.com/temporary-license/) 请求。  
3. **购买** – 从 [Aspose purchase page](https://purchase.aspose.com/buy) 购买订阅或永久许可证。

使用许可证文件初始化库：

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## 如何为 ODP 转换设置自定义字体目录？
`FontSettings` 是管理 Aspose.Imaging 字体资源的类。请在任何图像处理之前加载自定义字体，以确保每张幻灯片使用您提供的确切字体。

使用 Aspose.Imaging 的 `FontSettings` 设置字体文件夹路径：

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*定义锚点*：`FontSettings.setFontsFolder` 告诉 Aspose.Imaging 在文件系统中查找 TrueType 和 OpenType 字体的位置。

## 如何在 ODP 转换期间禁用系统替代字体？
禁用系统替代字体会强制渲染引擎忽略操作系统中已安装的字体，确保仅使用您提供的字体。这可消除可能改变幻灯片外观的意外字体替换。

使用以下调用禁用系统替代字体：

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*定义锚点*：`FontSettings.setGetSystemAlternativeFont(false)` 强制引擎仅使用您定义文件夹中的字体，消除意外的替换。

## 如何使用指定字体将 ODP 文件导出为 PNG？
`RasterizationOptions` 定义了向量页面如何光栅化为位图图像。通过将字体配置与光栅化设置相结合，您可以控制每个导出 PNG 的 DPI、背景颜色和页面尺寸。

按以下示例实现导出方法：

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

*定义锚点*：`RasterizationOptions` 类控制生成的 PNG 文件的 DPI、页面尺寸和背景颜色。

### 常见陷阱与解决方案
- **缺少字体文件** – 确认 ODP 中引用的每个 `.ttf` 或 `.otf` 都存在于您设置的文件夹中。  
- **文件路径不正确** – 使用绝对路径或相对于 `System.getProperty("user.dir")` 解析相对路径。  
- **权限不足** – 确保 Java 进程能够读取字体目录并写入输出文件夹。

## 实际应用
1. **品牌一致的幻灯片** – 将演示文稿导出为 PNG 用于网页发布，同时保留企业字体。  
2. **自动化报告生成** – 将每张幻灯片转换为图像，以嵌入 PDF 报告或电子邮件通讯。  
3. **遗留归档创建** – 将 ODP 内容存储为 PNG，确保未来无需 ODP 查看器即可访问。

## 性能考虑因素
- 使用最新的 Aspose.Imaging 版本，可受益于多线程光栅化改进（在 8 核 CPU 上提升至 2 倍速度）。  
- 在 try‑with‑resources 块中包装图像处理，以确保及时释放本机资源。  
- 在处理数千张幻灯片时，调整 `RasterizationOptions`（例如降低 DPI）以平衡质量和内存使用。

## 常见问题

**Q: 所需的最低 Java 版本是什么？**  
A: Aspose.Imaging for Java 支持 JDK 8 及以上版本；推荐使用 JDK 11 以获得长期支持。

**Q: 我可以只转换选定的幻灯片吗？**  
A: 可以，在调用 `save` 之前设置 `rasterizationOptions.setPageNumber(specificSlideIndex)`。

**Q: 如何处理受密码保护的 ODP 文件？**  
A: 使用包含密码的 `LoadOptions` 加载文件，然后继续使用相同的字体设置。

**Q: 禁用系统字体会影响性能吗？**  
A: 稍微提升速度，因为引擎跳过系统字体的查找，在字体库庞大的机器上尤为明显。

**Q: 在哪里可以找到更多代码示例？**  
A: 查看官方的 [Aspose.Imaging 文档](https://reference.aspose.com/imaging/java/) ，获取批量转换和图像转换等更多场景的示例。

## 其他资源
- [Aspose.Imaging for Java 发行版](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging 发行版](https://releases.aspose.com/imaging/java/)  
- [开始免费试用](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging 文档](https://reference.aspose.com/imaging/java/)  
- [Aspose.Imaging 论坛](https://forum.aspose.com/c/imaging/14)  
- [购买 Aspose 许可证](https://purchase.aspose.com/buy)  
- [申请临时许可证](https://purchase.aspose.com/temporary-license/)  

---

**最后更新：** 2026-06-28  
**测试环境：** Aspose.Imaging for Java 25.5  
**作者：** Aspose

## 相关教程

- [使用 Aspose.Imaging for Java 将 ODG 转换为 PNG：完整指南](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [使用 Aspose.Imaging 的高效图像转换（Java）：完整指南](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}