---
title: Aspose.Imaging for .NET 中的 DICOM 压缩
linktitle: Aspose.Imaging for .NET 中的 DICOM 压缩
second_title: Aspose.Imaging .NET 图像处理 API
description: 了解如何使用 Aspose.Imaging for .NET 执行 DICOM 压缩。按照此分步指南有效存储和传输具有高诊断质量的医学图像。
type: docs
weight: 17
url: /zh/net/dicom-image-processing/dicom-compression/
---
在医学成像领域，DICOM（医学数字成像和通信）标准对于存储和共享医学图像至关重要。 Aspose.Imaging for .NET 是一个功能强大的 .NET 库，为处理 DICOM 图像提供全面的支持。本教程将指导您完成使用 Aspose.Imaging for .NET 进行 DICOM 压缩的过程。我们将分解每个步骤并详细解释该过程。

## 先决条件

在我们深入研究使用 Aspose.Imaging for .NET 进行 DICOM 压缩之前，您需要确保满足以下先决条件：

1. 视觉工作室

确保您的系统上安装了 Visual Studio。如果没有，您可以从网站下载。

2. Aspose.Imaging for .NET

您必须拥有 Aspose.Imaging for .NET 库。您可以通过以下链接获取该库：

- [下载 .NET 版 Aspose.Imaging](https://releases.aspose.com/imaging/net/)
- [购买 .NET 版 Aspose.Imaging](https://purchase.aspose.com/buy)
- [获取免费试用许可证](https://releases.aspose.com/)
- [临时牌照](https://purchase.aspose.com/temporary-license/)

满足这些先决条件后，我们就可以开始了解如何使用 Aspose.Imaging for .NET 执行 DICOM 压缩的分步指南。

## 导入命名空间

在继续之前，我们需要导入必要的名称空间来访问所需的类和方法。打开 Visual Studio 项目，然后在 C# 文件的顶部添加以下内容：

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

现在，我们准备开始 DICOM 压缩过程。

## 第1步：加载原始图像

我们首先加载要转换为 DICOM 格式的原始图像。确保更换`"Your Document Directory"`与图像目录的实际路径。

```csharp
string dataDir = "Your Document Directory";
string inputFile = Path.Combine(dataDir, "original.jpg");

using (var inputImage = Image.Load(inputFile))
{
    //您的 DICOM 压缩代码将位于此处。
}
```

## 步骤 2：执行未压缩的 DICOM 压缩

在此步骤中，我们将执行未压缩的 DICOM 压缩。这是它的代码：

```csharp
string output1 = Path.Combine(dataDir, "original_Uncompressed.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.None }
};

inputImage.Save(output1, options);
```

## 步骤 3：执行 JPEG DICOM 压缩

现在，让我们继续使用 JPEG 格式执行 DICOM 压缩：

```csharp
string output2 = Path.Combine(dataDir, "original_JPEG.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Jpeg }
};

inputImage.Save(output2, options);
```

## 步骤 4：执行 JPEG2000 DICOM 压缩

在此步骤中，我们将使用 JPEG2000 格式执行 DICOM 压缩。操作方法如下：

```csharp
string output3 = Path.Combine(dataDir, "original_JPEG2000.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression
    {
        Type = CompressionType.Jpeg2000,
        Jpeg2000 = new Jpeg2000Options
        {
            Codec = Jpeg2000Codec.Jp2,
            Irreversible = false
        }
    }
};

inputImage.Save(output3, options);
```

## 步骤 5：执行 RLE DICOM 压缩

最后，让我们使用 RLE（运行长度编码）格式执行 DICOM 压缩：

```csharp
string output4 = Path.Combine(dataDir, "original_RLE.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Rle }
};

inputImage.Save(output4, options);
```

## 结论

在本分步指南中，我们学习了如何使用 Aspose.Imaging for .NET 执行 DICOM 压缩。该库提供了一组强大的工具来处理医学图像，您可以通过参考进一步探索其功能[文档](https://reference.aspose.com/imaging/net/).

## 常见问题解答

### Q1：什么是 DICOM 压缩？

A1：DICOM 压缩是在保持诊断质量的同时减小医学图像大小的过程。它对于医疗数据的有效存储和传输至关重要。

### Q2：为什么使用 Aspose.Imaging for .NET 进行 DICOM 压缩？

A2：Aspose.Imaging for .NET 提供了一组强大的功能和用户友好的 API，用于处理 DICOM 图像，使其成为医学成像应用的绝佳选择。

### Q3：我可以使用 Aspose.Imaging for .NET 将其他图像处理操作与 DICOM 压缩结合应用吗？

A3：是的，Aspose.Imaging for .NET 提供了广泛的图像处理功能，可以与 DICOM 压缩相结合以满足特定要求。

### 问题 4：我在哪里可以获得与 Aspose.Imaging for .NET 相关的支持或提出问题？

 A4：您可以访问[Aspose.Imaging 论坛](https://forum.aspose.com/)获得支持、提出问题以及参与 Aspose.Imaging 社区。

### Q5：Aspose.Imaging for .NET 有试用版可供测试吗？

A5：是的，您可以获得[免费试用许可证](https://releases.aspose.com/)在购买之前测试 Aspose.Imaging for .NET。