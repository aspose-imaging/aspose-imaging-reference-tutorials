---
"description": "学习如何使用 Aspose.Imaging for .NET 在 SVG 上绘制光栅图像。使用动态图像增强您的 .NET 应用程序。"
"linktitle": "在 Aspose.Imaging for .NET 中在 SVG 上绘制光栅图像"
"second_title": "Aspose.Imaging .NET图像处理API"
"title": "如何在 Aspose.Imaging for .NET 中在 SVG 上绘制光栅图像"
"url": "/zh/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Imaging for .NET 中在 SVG 上绘制光栅图像


在 .NET 编程领域，Aspose.Imaging 是一个可靠且功能强大的库，可用于处理各种图像相关任务。它提供的一项引人入胜的功能是在 SVG 画布上绘制光栅图像。在本分步指南中，我们将引导您完成使用 Aspose.Imaging for .NET 在 SVG 上绘制光栅图像的过程。

## 先决条件

在深入了解细节之前，请确保您已满足以下先决条件：

- Aspose.Imaging for .NET：您必须安装该库。如果没有，您可以从 [Aspose.Imaging for .NET下载页面](https://releases。aspose.com/imaging/net/).

- 您的文档目录：替换 `"Your Document Directory"` 使用您的工作目录的实际路径。

现在，让我们将这个过程分解为易于遵循的步骤：

## 步骤 1：导入必要的命名空间

您需要导入所需的命名空间才能使用 Aspose.Imaging：

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## 第 2 步：加载图像

- 首先，加载您想要在 SVG 画布上绘制的光栅图像。

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- 接下来，在您想要绘制光栅图像的位置加载 SVG 画布图像。

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## 步骤3：在SVG图像上绘图

现在，您可以开始在现有的 SVG 图像上绘图。为此，您需要创建一个 `SvgGraphics2D`：

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## 步骤4：绘制光栅图像

- 定义要绘制光栅图像的边界并指定光栅图像的源区域。

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## 步骤5：保存结果

在 SVG 画布上绘制光栅图像后，可以保存生成的图像：

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## 结论

恭喜！您已成功使用 Aspose.Imaging for .NET 在 SVG 画布上绘制光栅图像。这对于在 .NET 应用程序中创建丰富且动态的图像非常有用。

欲了解更多信息和详细文档，请访问 [Aspose.Imaging for .NET 文档](https://reference。aspose.com/imaging/net/).

## 常见问题

### 什么是 Aspose.Imaging for .NET？
   Aspose.Imaging for .NET 是一个强大的图像处理库，允许开发人员在 .NET 应用程序内创建、操作和转换各种格式的图像。

### 我可以在商业项目中使用 Aspose.Imaging for .NET 吗？
   是的，您可以在商业和非商业项目中使用 Aspose.Imaging for .NET。许可详情请参阅 [购买页面](https://purchase。aspose.com/buy).

### 有免费试用吗？
   是的，您可以从以下位置免费试用 Aspose.Imaging for .NET [这里](https://releases。aspose.com/).

### 我可以在哪里获得支持或提出问题？
   如果您有任何疑问或需要支持，您可以访问 [Aspose.Imaging 论坛](https://forum。aspose.com/).

### 如何获得 Aspose.Imaging for .NET 的临时许可证？
   您可以从 [这里](https://purchase。aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}