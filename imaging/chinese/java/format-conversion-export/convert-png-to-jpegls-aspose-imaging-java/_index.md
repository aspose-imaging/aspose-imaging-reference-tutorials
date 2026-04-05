---
date: '2026-04-05'
description: 学习如何使用 Aspose Imaging Java 将 PNG 图像转换为 JPEG‑LS，涵盖设置、转换步骤以及高效 Java 图像压缩的技巧。
keywords:
- aspose imaging java
- how to convert png
- java image compression
- convert png to jpeg-ls
- load png image java
title: Aspose Imaging Java：轻松将 PNG 转换为 JPEG-LS
url: /zh/java/format-conversion-export/convert-png-to-jpegls-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 标题：使用 Aspose Imaging Java 精通图像转换：将 PNG 转换为 JPEG-LS

## 介绍

在处理图像时，您可能需要在不牺牲质量的前提下优化文件大小。这时将图像从一种格式转换为另一种格式就显得尤为重要。借助 **Aspose Imaging Java**，您可以轻松地将每个样本 8 位的 PNG 图像转换为每个样本仅 2 位的 JPEG‑LS 格式。在本教程中，我们将完整演示整个过程，解释其意义，并提供可立即应用的实用技巧。

**您将学习的内容：**
- 如何在项目中设置 Aspose Imaging for Java
- 将 PNG 图像转换为 JPEG‑LS 格式的过程
- 将 JPEG‑LS 再转换回 PNG 以进行对比
- 关键配置选项、常见陷阱及故障排除技巧

在深入实现之前，让我们先了解开始所需的前置条件。

## 快速答案
- **哪个库负责转换？** Aspose Imaging Java
- **涉及哪些格式？** PNG → JPEG‑LS 和 JPEG‑LS → PNG
- **典型的压缩收益？** 在保持无损的前提下可降低高达 80 % 的体积
- **最低 Java 版本？** JDK 8 或更高
- **测试是否需要许可证？** 免费试用或临时许可证即可用于开发

## 什么是 Aspose Imaging Java？
Aspose Imaging Java 是一个强大的 API，允许开发者以编程方式读取、编辑和转换多种图像格式。它支持 JPEG‑LS 等高级压缩方案，非常适合对图像保真度和文件大小效率都有严格要求的场景。

## 为什么使用 Aspose Imaging Java 进行 PNG 到 JPEG‑LS 转换？
- **无损或准无损压缩** – JPEG‑LS 能保持每个像素细节完整。
- **简洁的 API** – 几行代码即可完成加载、配置和保存。
- **跨平台** – 在任何支持 Java 的操作系统上均可运行。
- **企业级** – 可从单张图像操作扩展到批量处理流水线。

## 前置条件 (H2)

要有效跟随本教程，请确保您具备：
- 基本的 Java 编程知识。
- 如 IntelliJ IDEA 或 Eclipse 等集成开发环境（IDE）。
- 已安装用于依赖管理的 Maven 或 Gradle。
- 对图像处理概念和文件格式有一定了解。

## 为 Java 设置 Aspose Imaging (H2)

**安装：**

要在 Java 项目中使用 Aspose Imaging，需要将其添加为依赖。以下示例展示了使用 Maven 或 Gradle 的方式：

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

您也可以直接从 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) 下载最新版本。

### 许可证获取

开始使用 Aspose Imaging 时，可考虑获取免费试用或购买许可证：
- **免费试用**：无需费用即可探索全部功能。
- **临时许可证**：通过 [Temporary License page](https://purchase.aspose.com/temporary-license/) 获取，适用于评估期间的延长使用。
- **购买**：长期使用请直接在 [Aspose’s Purchase Page](https://purchase.aspose.com/buy) 购买。

**基本初始化：**

在项目中引入 Aspose Imaging 后，需要进行初始化以确保所有功能可用：

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path/to/your/license.lic");
```

## 使用 Aspose Imaging Java 将 PNG 转换为 JPEG‑LS (H2)

### 将 PNG 转换为 JPEG‑LS (H2)

此功能可将每个样本 8 位的 PNG 图像压缩为更高效的每个样本 2 位的 JPEG‑LS 格式。

#### 概述
JPEG‑LS 以其无损和准无损压缩能力著称，适合在保持高质量的同时减小文件体积。本节将指导您使用 Aspose Imaging 将 PNG 转换为该格式。

#### 实现步骤

##### 加载原始 PNG 图像 (H3)
首先加载源 PNG 图像：

```java
String originPngFileName = "YOUR_DOCUMENT_DIRECTORY/lena24b.png";
PngImage pngImage = (PngImage) Image.load(originPngFileName);
```
*为什么？*：加载图像后即可使用 Aspose Imaging 强大的 API 对其进行访问和操作。

##### 配置 JPEG 选项 (H3)
设置转换所需的选项：

```java
int bpp = 2; // Bits per sample
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setBitsPerChannel((byte) bpp);
jpegOptions.setCompressionType(JpegCompressionMode.JpegLs);
```
*为什么？*：配置这些选项可指定输出 JPEG‑LS 图像的压缩类型和质量参数。

##### 保存图像 (H3)
最后，保存转换后的图像：

```java
String outputJpegFileName = "YOUR_OUTPUT_DIRECTORY/lena24b 2-bit Gold.jls";
pngImage.save(outputJpegFileName, jpegOptions);
```
*为什么？*：以特定格式保存即完成转换过程。

##### 资源管理 (H3)
处理完毕后确保释放资源：

```java
finally {
    pngImage.dispose();
}
```
*为什么？*：释放图像对象有助于有效管理内存使用。

#### 故障排除提示

- **常见问题**：如果出现 `FileNotFoundException`，请仔细检查输入和输出文件的路径。
- **解决方案**：确保 IDE 对指定目录拥有读取和写入权限。

### 将 JPEG‑LS 转换回 PNG (H2)

此功能可将 JPEG‑LS 图像转换回 PNG，便于进行视觉对比或后续处理。

#### 概述
在将图像压缩为 JPEG‑LS 之后，可能需要将其恢复为 PNG 以评估质量或用于其他用途。本节说明如何使用 Aspose Imaging 完成此操作。

#### 实现步骤

##### 加载 JPEG‑LS 图像 (H3)
首先加载 JPEG‑LS 文件：

```java
String inputJpegFileName = "YOUR_OUTPUT_DIRECTORY/lena24b 2-bit Gold.jls";
JpegImage jpegImage = (JpegImage) Image.load(inputJpegFileName);
```
*为什么？*：加载图像后即可进行格式转换。

##### 保存为 PNG (H3)
将图像转换并保存为 PNG 格式：

```java
String outputPngFileName = "YOUR_OUTPUT_DIRECTORY/lena24b 2-bit Gold.png";
jpegImage.save(outputPngFileName, new PngOptions());
```
*为什么？*：此步骤确保 JPEG‑LS 文件被转换回兼容且无损的 PNG 格式。

##### 资源管理 (H3)
保存后释放图像资源：

```java
finally {
    jpegImage.dispose();
}
```
*为什么？*：正确释放可避免内存泄漏，保持应用性能。

## 实际应用场景 (H2)

1. **医学影像** – JPEG‑LS 常用于医学影像，因其高效的无损压缩能够保留关键诊断细节。
2. **高质量图像归档** – 档案机构可在最小存储开销下保存高分辨率图像。
3. **网页开发** – 在不损失质量的前提下降低图像文件大小，可提升页面加载速度和用户体验。
4. **数码摄影** – 摄影师可在不影响真实感的情况下压缩作品集。
5. **平面设计** – 设计师常需在质量与文件大小之间取得平衡，以适配多种媒体输出。

## 性能考虑 (H2)

- **优化内存使用** – 始终使用 `dispose()` 方法释放图像，以及时回收资源。
- **批量处理** – 对大规模数据集进行批量处理，可有效控制内存消耗。
- **并行执行** – 利用 Java 并发工具实现并行图像处理，提升吞吐量。

## 常见问题与解决方案 (H2)

| 症状 | 可能原因 | 解决办法 |
|---------|--------------|-----|
| `FileNotFoundException` | 文件路径错误 | 核实绝对/相对路径并检查文件夹权限 |
| 内存溢出错误 | 顺序处理大图像 | 使用批量处理或增大 JVM 堆大小（`-Xmx`） |
| 输出文件损坏 | 未调用 `dispose()` | 确保在 `finally` 块中释放图像对象 |

## 常见问答 (H2)

**问：使用 Aspose Imaging 的系统要求是什么？**  
答：Aspose Imaging 可在任何支持 Java 的平台上运行，需 JDK 8 或更高版本。

**问：我可以在开源项目中使用 Aspose Imaging 吗？**  
答：可以，但必须遵守 Aspose 提供的许可条款。

**问：如果图像文件在转换过程中损坏怎么办？**  
答：在处理前验证输入文件，并捕获异常以优雅地处理错误。

**问：如何处理除 2 位每样本之外的其他位深？**  
答：将 `setBitsPerChannel()` 参数设置为所需的位深即可。

**问：Aspose Imaging 是否兼容所有 Java IDE？**  
答：是的，兼容主流 IDE，如 IntelliJ IDEA、Eclipse 和 NetBeans。

## 资源

- [Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/)
- [Download Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/)
- [Purchase License](https://purchase.aspose.com/buy)
- [Free Trial Access](https://releases.aspose.com/imaging/java/)
- [Temporary License Application](https://purchase.aspose.com/temporary-license/)
- [Community Support Forum](https://forum.aspose.com/c/imaging/14)

通过本完整指南，您已掌握使用 **Aspose Imaging Java** 高效完成 PNG 与 JPEG‑LS 之间相互转换的技巧。祝编码愉快！

---

**最后更新：** 2026-04-05  
**测试环境：** Aspose Imaging 25.5 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}