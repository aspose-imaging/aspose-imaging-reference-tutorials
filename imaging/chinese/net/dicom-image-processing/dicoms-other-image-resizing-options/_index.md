---
"description": "学习如何使用 Aspose.Imaging for .NET 调整 DICOM 图像的大小。高效医学图像处理的分步指南。"
"linktitle": "Aspose.Imaging for .NET 中的 DICOM 其他图像调整大小选项"
"second_title": "Aspose.Imaging .NET图像处理API"
"title": "Aspose.Imaging for .NET 中的 DICOM 其他图像调整大小选项"
"url": "/zh/net/dicom-image-processing/dicoms-other-image-resizing-options/"
"weight": 20
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET 中的 DICOM 其他图像调整大小选项

您是否希望在 .NET 应用程序中处理 DICOM（医学数字成像和通信）图像？Aspose.Imaging for .NET 提供了一套强大的工具，可以高效地处理 DICOM 图像。在本教程中，我们将使用 Aspose.Imaging for .NET 深入探讨“DICOM 的其他图像大小调整选项”。我们将介绍先决条件、导入命名空间，并提供分步指南，帮助您理解和有效地实现 DICOM 图像大小调整。

## 先决条件

在开始之前，请确保您已满足以下先决条件：

1. 安装 Aspose.Imaging for .NET
要使用 Aspose.Imaging for .NET 处理 DICOM 图像，您需要安装该库。您可以从网站下载。

[下载 Aspose.Imaging for .NET](https://releases.aspose.com/imaging/net/)

2. 设置开发环境
确保您已设置 .NET 开发环境，包括 Visual Studio 或任何其他兼容的 IDE。

3. DICOM图像
您应该有一个 DICOM 图像文件（例如“file.dcm”），并且想要使用 Aspose.Imaging for .NET 调整其大小。

## 导入命名空间

在您的 C# 代码中，您需要导入必要的命名空间才能使用 Aspose.Imaging。操作方法如下：

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
```

现在，让我们将图像调整大小的过程分解为多个步骤。

## 步骤 1：加载 DICOM 图像
首先，您需要从文件系统加载 DICOM 图像。

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
{
    // 您的代码在这里
}
```

## 步骤 2：按高度按比例调整大小
您可以通过指定高度（以像素为单位）和调整大小类型来按比例调整 DICOM 图像的大小。在本例中，我们使用“AdaptiveResample”作为调整大小类型。

```csharp
image.ResizeHeightProportionally(100, ResizeType.AdaptiveResample);
```

## 步骤 3：保存调整大小后的图像
调整图像大小后，您可以将其保存为所需的格式。在这里，我们将其保存为 BMP 图像。

```csharp
image.Save(dataDir + "DICOMSOtherImageResizingOptions_out.bmp", new BmpOptions());
```

## 步骤 4：按宽度按比例调整大小
您还可以通过指定像素宽度和调整大小类型来按比例调整 DICOM 图像的大小。

```csharp
image1.ResizeWidthProportionally(150, ResizeType.AdaptiveResample);
```

## 步骤 5：保存调整大小后的图像
将调整大小的图像保存为 BMP 图像，就像上一步一样。

```csharp
image1.Save(dataDir + "DICOMSOtherImageResizingOptions1_out.bmp", new BmpOptions());
```

恭喜！您已成功使用 Aspose.Imaging for .NET 调整了 DICOM 图像的大小。该库提供了多种处理 DICOM 图像的选项，使其成为医疗保健和医学成像应用的宝贵工具。

## 结论

在本教程中，我们使用 Aspose.Imaging for .NET 探索了“DICOM 的其他图像大小调整选项”。我们介绍了先决条件、导入的命名空间，并提供了调整 DICOM 图像大小的分步指南。Aspose.Imaging for .NET 简化了医学图像的处理流程，为医疗保健应用提供了丰富的功能。

对 Aspose.Imaging for .NET 还有其他疑问或需要帮助？请查看文档或访问 Aspose 社区论坛获取支持：

- [Aspose.Imaging for .NET 文档](https://reference.aspose.com/imaging/net/)
- [Aspose.Imaging for .NET 支持](https://forum.aspose.com/)

## 常见问题解答

### 问题1：什么是DICOM？

A1：DICOM 是医学数字成像和通信的缩写。它是一种以数字格式传输、存储和共享医学图像（例如 X 光片、MRI 和 CT 扫描）的标准。

### 问题2：我可以免费使用 Aspose.Imaging for .NET 吗？

答2：Aspose.Imaging for .NET 是一个商业库。您可以下载免费试用版来评估其功能，但需要许可证才能完全使用。

### 问题3：Aspose.Imaging for .NET 还提供哪些其他图像处理选项？

A3：Aspose.Imaging for .NET 提供了丰富的图像处理选项，包括格式转换、图像增强以及图像绘图。您可以在文档中探索所有功能。

### 问题4：Aspose.Imaging for .NET 适合医疗保健应用吗？

A4：是的，Aspose.Imaging for .NET 通常用于医疗保健应用程序中处理 DICOM 图像，使其成为医学成像软件开发的宝贵工具。

### 问题5：我可以获得 Aspose.Imaging for .NET 的临时许可证吗？
西
A5：是的，您可以申请临时许可证用于测试和评估。请访问 [Aspose 的临时许可证页面](https://purchase.aspose.com/temporary-license/) 了解更多信息。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}