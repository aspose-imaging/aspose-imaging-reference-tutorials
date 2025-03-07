---
title: .NET용 Aspose.Imaging의 래스터 이미지에 벡터 이미지 그리기
linktitle: .NET용 Aspose.Imaging의 래스터 이미지에 벡터 이미지 그리기
second_title: Aspose.Imaging .NET 이미지 처리 API
description: Aspose.Imaging을 사용하여 .NET에서 벡터 이미지를 래스터 이미지로 변환하는 방법을 알아보세요. 효율적인 이미지 처리를 위한 단계별 가이드입니다.
weight: 13
url: /ko/net/vector-image-processing/draw-vector-image-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.Imaging의 래스터 이미지에 벡터 이미지 그리기


.NET 애플리케이션에서 벡터 이미지를 래스터 이미지로 쉽게 변환하고 싶으십니까? Aspose.Imaging for .NET은 이 작업에 효율적인 솔루션을 제공합니다. 이 단계별 가이드에서는 Aspose.Imaging for .NET을 사용하여 벡터 이미지를 래스터 이미지로 그리는 과정을 안내합니다. 

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

### 1. .NET용 Aspose.Imaging

 .NET용 Aspose.Imaging이 설치되어 있어야 합니다. 없으시면 홈페이지에서 다운받으시면 됩니다[.NET용 Aspose.Imaging 다운로드](https://releases.aspose.com/imaging/net/).

### 2. .NET 개발 환경

컴퓨터에 .NET 개발 환경이 설정되어 있는지 확인하세요. Visual Studio 또는 기타 .NET 개발 도구를 사용할 수 있습니다.

이제 벡터 이미지를 래스터 이미지로 그리는 과정을 간단하고 따라하기 쉬운 단계로 나누어 보겠습니다.

## 1단계: 프로젝트 초기화

개발 환경에서 새 .NET 프로젝트를 만드는 것부터 시작하세요. 프로젝트에 Aspose.Imaging for .NET이 통합되어 있는지 확인하세요.

## 2단계: 벡터 이미지 로드

이 단계에서는 래스터 이미지로 변환하려는 벡터 이미지(SVG 형식)를 로드합니다.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## 3단계: 벡터 이미지 래스터화

이제 SVG 이미지를 PNG 형식으로 래스터화해야 합니다. 여기서 벡터에서 래스터로의 변환이 발생합니다.

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## 4단계: 래스터 이미지 로드

래스터화 후 추가 그리기를 위해 스트림에서 PNG 이미지를 로드합니다.

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## 5단계: 래스터 이미지 그리기

이제 기존 SVG 이미지 위에 래스터 이미지를 그릴 수 있습니다.

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## 6단계: 결과 저장

마지막으로 결과 이미지를 저장합니다. 이제 벡터 이미지를 포함하는 래스터 이미지가 생겼습니다.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## 결론

이 튜토리얼에서는 Aspose.Imaging for .NET을 사용하여 벡터 이미지를 래스터 이미지로 변환하는 방법을 보여주었습니다. 이러한 간단한 단계를 통해 이 기능을 .NET 애플리케이션에 손쉽게 통합할 수 있습니다.

### 자주 묻는 질문

### .NET용 Aspose.Imaging이란 무엇입니까?
Aspose.Imaging for .NET은 다양한 이미지 형식으로 작업하고, 이미지를 변환하고, 고급 이미지 조작 작업을 수행하는 기능을 포함하여 강력한 이미지 처리 기능을 제공하는 .NET 라이브러리입니다.

### .NET용 Aspose.Imaging에 대한 설명서는 어디서 찾을 수 있나요?
 .NET용 Aspose.Imaging에 대한 설명서를 찾을 수 있습니다.[여기](https://reference.aspose.com/imaging/net/).

### 무료 평가판을 사용할 수 있나요?
 예, .NET용 Aspose.Imaging 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### .NET용 Aspose.Imaging의 임시 라이선스를 어떻게 얻나요?
 임시 라이센스가 필요한 경우, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### .NET용 Aspose.Imaging에 대한 지원은 어디서 받을 수 있나요?
 지원이나 문의 사항이 있는 경우 다음을 방문하세요.[Aspose.이미징 포럼](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
