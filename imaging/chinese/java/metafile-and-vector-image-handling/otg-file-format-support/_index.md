---
date: 2026-01-24
description: 学习如何使用 Aspose.Imaging for Java 将 OTG 转换为 PDF。本分步指南展示了如何将图像保存为 PDF 并高效处理图像。
linktitle: OTG File Format Support
second_title: Aspose.Imaging Java Image Processing API
title: 使用 Aspose.Imaging for Java 将 OTG 转换为 PDF
url: /zh/java/metafile-and-vector-image-handling/otg-file-format-support/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Imaging for Java 将 OTG 转换为 PDF

如果您需要 **快速可靠地将 OTG 转换为 PDF**，您来对地方了。在本教程中，我们将一步步演示从环境搭建、导入正确的包，到实际将 OTG（OpenDocument Drawing Template）文件转换为 PNG 和 PDF 格式的全部过程。完成后，您将能够熟练使用这款 **Java 图像处理库** 来 *将图像保存为 PDF* 并处理其他图像格式的转换。

## 快速答疑
- **“将 OTG 转换为 PDF” 是什么意思？** 它将 OpenDocument Drawing Template 转换为 PDF 文档，并将矢量数据栅格化为页面。  
- **使用哪个库来完成？** Aspose.Imaging for Java，一款强大的 **java image processing library**。  
- **需要许可证吗？** 开发阶段可以使用免费试用版；生产环境需要商业许可证。  
- **还能生成 PNG 文件吗？** 可以——同一段代码即可 **save image as PDF** 并 **save image as PNG**。  
- **需要哪个 Java 版本？** Java 8 或更高（任何支持该库的 JDK）。

## 什么是 “将 OTG 转换为 PDF”？
将 OTG 文件转换为 PDF 意味着加载 OTG 文档、对每页进行栅格化，然后将结果写入 PDF 容器。当您需要与仅拥有 PDF 查看器的用户共享图纸时，这非常有用。

## 为什么选择 Aspose.Imaging for Java 来完成此任务？
- **完整格式支持** – 开箱即支持 OTG、PNG、PDF洁 API** 在任何运行+ 运行时上运行。

### 2. Aspose.Imaging for Java 库
从官方站点下载最新库：[Download Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/)。

### 3. 文档目录
在机器上创建一个文件夹，用于存放 OTG 源文件和生成的输出文件。记住绝对路径——我们将在代码中引用它。

## 导入包

在 Java 源文件顶部添加所需的导入，以便编译器能够找到相应的类：

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Size;
import com.aspose.imaging.imageoptions.ImageOptionsBase;
import com.aspose.imaging.imageoptions.otg.OtgRasterizationOptions;
import com.aspose.imaging.imageoptions.pdf.PdfOptions;
import com.aspose.imaging.imageoptions.png.PngOptions;
```

## 将 OTG 转换为 PDF 的分步指南

### 步骤 1：定义数据目录
指向包含 OTG 文件的文件夹。

```java
String dataDir = "Your Document Directory" + "OTG/";
```

将 `"Your Document Directory"` 替换为您机器上的实际路径。

### 步骤 2：指定 OTG 文件名
告诉程序要处理哪个 OTG 文件。

```java
String fileName = "VariousObjectsMultiPage.otg";
```

您可以使用任意已有的 OTG 文件。

### 步骤 3：准备输出选项
创建一个数组，指示 Aspose.Imaging 同时生成 PNG 和 PDF 文件。

```java
ImageOptionsBase[] options = { new PngOptions(), new PdfOptions() };
```

这使您能够 **create PDF from image** 并在一次运行中生成 PNG 缩略图。

### 步骤 4：加载 OTG 图像
使用 `Image.load` 方法打开 OTG 文件。

```java
try (Image image = Image.load(inputFileName))
```

`inputFileName` 应为 OTG 文件的完整路径（例如 `dataDir + fileName`）。

### 步骤 5：配置栅格化选项
设置栅格化尺寸，使输出与原始尺寸匹配。

```java
OtgRasterizationOptions otgRasterizationOptions = new OtgRasterizationOptions();
otgRasterizationOptions.setPageSize(Size.to_SizeF(image.getSize()));
```

这些选项对于在 **convert OTG to PDF** 时实现精确渲染至关重要。

### 步骤 6：保存转换后的图像
遍历选项数组并写入每个输出文件。

```java
image.save("Your Document Directory" + "output" + fileExt, item);
```

- `"output"` 可以是任意您喜欢的名称。  
- `fileExt` 会根据循环中当前的 `item` 自动设置为 `.png` 或 `.pdf`。

循环结束后，您将拥有原始 OTG 图纸的 PDF 和 PNG 两个版本。

## 常见问题与排查

| 症状 | 可能原因 | 解决办法 |
|------|----------|----------|
| **在 `image.getSize()` 上抛出 NullPointerException** | OTG 文件未正确加载（路径错误）。 | 确认 `inputFileName` 指向实际的 OTG 文件。 |
| **生成的 PDF 空白** | 栅格化选项未设置或页面尺寸不匹配。 | 确保 `otgRasterizationOptions.setPageSize(...)` 使用图像的尺寸。 |
| **未创建输出文件** | 目标文件夹缺少写入权限。 | 以足够的文件系统权限运行程序，或选择可写目录。 |

## 常见问答

**问：什么是 Aspose.Imaging for Java？**  
答：Aspose.Imaging for Java 是一款 **java image processing library**，支持超过 100 种图像格式，能够进行转换并提供高级栅格化功能。

**问：在哪里可以找到 Aspose.Imaging for Java 的文档？**  
答：文档链接如下：[Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/)。

**问：是否有 Aspose.Imaging for Java 的免费试用版？**  
答：有，您可以从 [这里](https://releases.aspose.com/) 下载免费试用版。

**问：如何获取 Aspose.Imaging for Java 的临时许可证？**  
答：访问 [此链接](https://purchase.aspose.com/temporary-license/) 获取临时许可证。

**问：在哪里可以获得 Aspose.Imaging for Java 的支持与帮助？**  
答：如有疑问或遇到问题，可前往 Aspose.Imaging for Java 支持论坛：[Aspose Forum](https://forum.aspose.com/)。

### 其他快速问答

**问：我可以使用此代码将其他格式（如 JPEG） **save image as PDF** 吗？换成 JPEG，保持 `PdfOptions` 在 `options` 数组中，库会自动完成转换。

**问：Aspose.Imaging 是否支持批量处理多个 OTG 文件？**  
答：支持。只需将加载与保存逻辑放入遍历文件名列表的循环中即可。

## 结论

现在，您已经掌握了一套完整、可投入生产的 **convert OTG to PDF**（并可选生成 PNG）方案，使用 Aspose.Imaging for Java 实现。该方案利用强大的 **java convert image formats** 引擎，仅需几行代码即可 **save image as PDF**。您可以进一步扩展示例以处理多文件、集成到 Web 服务，或与其他 Aspose 产品结合，实现更丰富的文档工作流。

---

**最后更新：** 2026-01-24  
**测试环境：** Aspose.Imaging for Java 24.12（撰写时最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}