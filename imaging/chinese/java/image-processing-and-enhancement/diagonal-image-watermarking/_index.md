---
date: 2026-01-09
description: 学习如何使用 Aspose.Imaging for Java 为图像添加水印。本 Java 图像处理教程逐步展示如何快速创建对角线水印。
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: 如何添加水印 – 对角线图像水印（Java）
url: /zh/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 如何添加水印 – 对角线图像水印（Java）

如果您想要 **how to add watermark** 到图片，并且希望采用时尚的对角线方向，Aspose.Imaging for Java 能让这变得轻而易举。在本分步教程中，我们将演示如何向 JPG（或任何受支持的）图像添加 45 度旋转的文字水印。您不需要是 Java 大师——每个代码块都用通俗的语言解释，您可以在几分钟内复制出相同的效果。

## 快速答案
- **使用的库是什么？** Aspose.Imaging for Java  
- **覆盖的主要关键词是什么？** how to add watermark  
- **支持的图像格式？** JPEG, PNG, BMP, TIFF, GIF and more  
- **需要多少代码？** Only seven concise code blocks  
- **测试是否需要许可证？** A free trial is available; a license is required for production  

## 什么是图像处理中的 “how to add watermark”
添加水印是指在图像上覆盖半透明的文字或图形，以保护所有权或传达品牌信息。对角线水印尤其有效，因为它覆盖整张图片，且更难被裁剪掉。

## 为什么使用 Aspose.Imaging for Java？
Aspose.Imaging 提供了高级 API，抽象了底层像素操作，支持数十种格式，并可在任何 Java 运行时上运行。它让您专注于 *要实现的目标*——例如添加对角线水印——而无需担心图像格式的细节问题。

## 前置条件

在开始之前，请确保您具备以下条件：

1. **Aspose.Imaging for Java** – 从官方站点 **[here](https://releases.aspose.com/imaging/java/)** 下载最新版本。  
2. **Java Development Environment** – JDK 8+ 和您喜欢的 IDE（IntelliJ、Eclipse、VS Code 等）。  
3. **An image to watermark** – 将示例 JPG/TIFF/PNG 放在代码中引用的文件夹中。

## 导入包

首先，导入您需要的类。将 import 语句集中放置可以使代码更易阅读和维护。

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## 步骤 1：加载已有图像

我们首先加载源图片。`Image.load` 方法会自动检测格式。

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **专业提示：** 将 `Image` 对象放在 try‑with‑resources 块中（如示例所示），这样可以自动释放，防止内存泄漏。

## 步骤 2：准备水印文本和图形

创建一个与已加载图像关联的 `Graphics` 对象，并保存图像尺寸以供后续计算使用。

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## 步骤 3：定义字体和画刷

选择一种醒目的字体和一个定义水印颜色与不透明度的画刷。调整不透明度，使水印呈半透明效果。

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## 步骤 4：格式化文本

设置对齐和格式化标志，使绘制时文本居中。

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## 步骤 5：应用变换

变换矩阵可以让我们将原点移动到图像中心，然后将文本顺时针旋转 ‑45°。

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## 步骤 6：绘制并保存

最后，将字符串渲染到图像上并将结果写入磁盘。

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

当您打开 `AddDiagonalWatermarkToImage_out.jpg` 时，您会看到红色的半透明文字斜斜地跨越图片中心。

## 常见问题与解决方案

| Problem | Reason | Fix |
|---------|--------|-----|
| Watermark appears too faint | Opacity set to 0 (fully transparent) | Increase opacity, e.g., `brush.setOpacity(0.5f);` |
| Text is clipped at edges | Translation not centered for non‑square images | Use `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` as shown, then adjust rotation angle if needed |
| Unsupported image format error | Using an older Aspose.Imaging version | Update to the latest Aspose.Imaging release |

翻译后表格：

| 问题 | 原因 | 解决方案 |
|------|------|----------|
| 水印太淡 | 不透明度设为 0（完全透明） | 增加不透明度，例如 `brush.setOpacity(0.5f);` |
| 文字在边缘被裁剪 | 非正方形图像的平移未居中 | 如示例使用 `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);`，必要时调整旋转角度 |
| 不支持的图像格式错误 | 使用了较旧的 Aspose.Imaging 版本 | 升级到最新的 Aspose.Imaging 版本 |

## 常见问答

### Q1：Aspose.Imaging for Java 适合初学者吗？

**答：** 当然！API 直观，文档提供了清晰的示例。即使是图像处理新手也能按照本教程快速产出专业效果。

### Q2：我可以自定义水印文字和样式吗？

**答：** 可以。修改 `theString` 变量，选择不同的 `Font`，更改 `brush.setColor(...)`，或在矩阵中调整旋转角度，以符合您的品牌需求。

### Q3：Aspose.Imaging for Java 除了 JPG 之外还支持其他图像格式吗？

**答：** 支持。该库可处理 BMP、PNG、GIF、TIFF、PSD 等多种格式。只需将 `Image.load` 方法指向相应文件即可。

### Q4：Aspose.Imaging for Java 有免费试用吗？

**答：** 有，您可以通过免费试用体验 Aspose.Imaging for Java。获取地址 **[here](https://releases.aspose.com/)**。

### Q5：在哪里可以获得 Aspose.Imaging for Java 的帮助或支持？

**答：** 如有疑问、错误报告或最佳实践建议，请访问 Aspose.Imaging for Java 支持论坛 **[here](https://forum.aspose.com/)**。

---

**最后更新：** 2026-01-09  
**测试环境：** Aspose.Imaging for Java 24.11（撰写时的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}