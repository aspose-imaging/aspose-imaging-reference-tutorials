---
"date": "2025-06-03"
"description": "了解如何使用 Aspose.Imaging for .NET 按比例调整 DICOM 图像大小，以保持医学成像工作流程的质量和效率。"
"title": "使用 Aspose.Imaging for .NET 进行 DICOM 图像比例调整完整指南"
"url": "/zh/net/medical-imaging-dicom/resize-dicom-images-proportionally-aspose-imaging-net/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# 使用 Aspose.Imaging for .NET 按比例调整 DICOM 图像大小：完整指南

## 介绍
在医学成像领域，医学数字成像与通信 (DICOM) 图像对于诊断和分析至关重要。然而，这些高分辨率文件的存储或传输可能会非常繁琐。本教程将指导您使用 Aspose.Imaging for .NET（一个简化图像处理任务的多功能库）按比例调整 DICOM 图像的大小。

**您将学到什么：**
- 安装和设置 Aspose.Imaging for .NET
- 按高度和宽度调整 DICOM 图像的大小，同时保持比例
- 这些技术在医学成像工作流程中的实际应用

让我们深入探讨如何将此功能无缝集成到您的项目中。在开始之前，请确保您已准备好所有必要的资料。

## 先决条件
在开始使用 Aspose.Imaging for .NET 之前，请确保您已满足以下先决条件：

1. **所需的库和版本：**
   - 您将需要 Aspose.Imaging for .NET 库。
   - 确保您的项目针对兼容版本的 .NET 框架（例如，.NET Core 3.1 或更高版本）。

2. **环境设置：**
   - 类似 Visual Studio 的 C# 开发环境。

3. **知识前提：**
   - 对 C# 编程有基本的了解，并熟悉图像处理概念。

## 设置 Aspose.Imaging for .NET
首先，您需要在项目中安装 Aspose.Imaging 库。以下是使用不同包管理器的安装步骤：

**.NET CLI：**
```shell
dotnet add package Aspose.Imaging
```

**程序包管理器控制台：**
```shell
Install-Package Aspose.Imaging
```

**NuGet 包管理器 UI：**
- 搜索“Aspose.Imaging”并安装最新版本。

### 许可证获取
要解锁 Aspose.Imaging 的所有功能，您可能需要获取许可证。具体方法如下：

- **免费试用：** 从免费试用开始探索基本功能。
- **临时执照：** 获取临时执照 [这里](https://purchase.aspose.com/temporary-license/) 用于在开发过程中扩展访问。
- **购买：** 如果满意，请购买完整许可证 [此链接](https://purchase。aspose.com/buy).

安装后，通过在项目文件中引用该库来初始化它。

## 实施指南
让我们详细分析如何使用 Aspose.Imaging for .NET 实现 DICOM 图像按比例调整大小。我们将详细介绍高度和宽度的调整。

### 按高度比例调整 DICOM 图像大小
本节将演示如何根据 DICOM 图像的高度调整其大小，确保保留纵横比。

#### 概述
按高度按比例调整大小可保持原始纵横比，同时将图像的高度调整到指定大小 - 非常适合在不同的显示格式中保持视觉完整性。

#### 实施步骤

**步骤 1：加载 DICOM 图像**
首先，使用 Aspose.Imaging 的 `DicomImage` 班级。
```csharp
using System;
using System.IO;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;

string dataDir = "YOUR_DOCUMENT_DIRECTORY";
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// 打开 DICOM 文件进行读取
using (var fileStream = new FileStream(dataDir + "/file.dcm\

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}