---
title: 使用 Aspose.Imaging for .NET 调整 DICOM 图像大小
linktitle: Aspose.Imaging for .NET 中的 DICOM 简单调整大小
second_title: Aspose.Imaging .NET 图像处理 API
description: 了解如何使用 Aspose.Imaging for .NET（医学图像处理的强大工具）调整 DICOM 图像的大小。简单的步骤即可获得精确的结果。
type: docs
weight: 19
url: /zh/net/dicom-image-processing/dicom-simple-resizing/
---
在不断发展的医学成像领域，处理 DICOM（医学数字成像和通信）文件时的灵活性和精确度至关重要。 Aspose.Imaging for .NET 作为一个强大的解决方案出现，提供了一整套用于处理医学图像的工具。在本教程中，我们将探索使用 Aspose.Imaging for .NET 调整 DICOM 图像大小的简单过程。 

## 先决条件

在我们深入了解分步指南之前，请确保您具备以下先决条件：

1. Aspose.Imaging for .NET：您必须在开发环境中安装 Aspose.Imaging for .NET 库。如果您还没有，您可以从以下位置下载[这里](https://releases.aspose.com/imaging/net/).

2. .NET 开发环境：需要 C# 和 .NET 开发环境的应用知识。

3. DICOM 图像文件：您应该有一个要调整大小的 DICOM 图像文件。如果您需要样本 DICOM 图像进行测试，您可以轻松地在网上找到一个。

4. Visual Studio（可选）：虽然不是强制性的，但在本教程中使用 Visual Studio 将增强您的开发体验。

现在，让我们将调整 DICOM 图像大小的过程分解为简单、可操作的步骤。

## 第 1 步：导入命名空间

第一步是导入使用 Aspose.Imaging 所需的命名空间。在您的 C# 项目中，包含以下命名空间：

```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

通过导入这些命名空间，您可以访问处理 DICOM 图像所需的功能。

## 第 2 步：调整 DICOM 图像大小

现在，让我们将 DICOM 图像调整大小过程分解为几个易于管理的步骤。

### 步骤2.1：设置文档目录

在 C# 代码中，指定 DICOM 文件所在的目录。你应该更换`"Your Document Directory"`与文件目录的实际路径。

```csharp
string dataDir = "Your Document Directory";
```

### 步骤2.2：打开DICOM文件

接下来，使用打开 DICOM 文件`FileStream`。确保更换`"file.dcm"`与您的 DICOM 文件的名称。

```csharp
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
{
    //您的图像处理代码位于此处
}
```

### 步骤2.3：加载DICOM图像

从以下位置加载 DICOM 图像`fileStream`。这允许您访问图像并对其执行操作。

```csharp
using (DicomImage image = new DicomImage(fileStream))
{
    //您的图像处理代码位于此处
}
```

### 步骤 2.4：调整 DICOM 图像大小

加载 DICOM 图像后，您现在可以将其调整为所需的尺寸。在此示例中，我们将其大小调整为 200x200 像素。

```csharp
image.Resize(200, 200);
```

### 步骤2.5：保存调整大小的图像

最后，将调整大小的 DICOM 图像保存到指定的输出目录。在此示例中，我们将其另存为 BMP 文件。

```csharp
image.Save(dataDir + "DICOMSimpleResizing_out.bmp", new BmpOptions());
```

## 结论

恭喜！您已使用 Aspose.Imaging for .NET 成功调整了 DICOM 图像的大小。通过这些简单的步骤，您可以有效地处理医学图像以满足您的特定要求。

如果您遇到任何问题或对 Aspose.Imaging for .NET 有疑问，请随时向支持社区寻求帮助：[Aspose论坛](https://forum.aspose.com/).

## 常见问题解答

### Q1：什么是DICOM？

A1：DICOM 代表医学数字成像和通信。它是存储、传输和共享医学图像及相关信息的标准。

### Q2：我也可以将 Aspose.Imaging 用于其他图像格式吗？

A2：是的，Aspose.Imaging for .NET 支持 DICOM 以外的多种图像格式，包括 BMP、JPEG、PNG 等。

### Q3：打开调整大小的图像是否需要 DICOM 查看器？

A3：不需要，一旦您使用Aspose.Imaging调整了DICOM图像的大小，生成的图像就是标准图像格式（例如BMP），并且可以使用常见的图像查看器来查看。

### Q4：Aspose.Imaging for .NET 是否与所有版本的 .NET Framework 兼容？

A4：Aspose.Imaging for .NET 与.NET Framework 的各个版本兼容，包括.NET Core 和.NET Standard。请务必检查文档以了解详细信息。

### Q5：在哪里可以找到更多 Aspose.Imaging for .NET 教程？

 A5：你可以探索官方[Aspose.Imaging for .NET 文档](https://reference.aspose.com/imaging/net/)获取广泛的教程和示例。