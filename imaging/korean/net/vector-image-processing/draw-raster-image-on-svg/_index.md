---
title: .NET용 Aspose.Imaging에서 SVG에 래스터 이미지를 그리는 방법
linktitle: .NET용 Aspose.Imaging에서 SVG에 래스터 이미지 그리기
second_title: Aspose.Imaging .NET 이미지 처리 API
description: .NET용 Aspose.Imaging을 사용하여 SVG에 래스터 이미지를 그리는 방법을 알아보세요. 동적 이미지로 .NET 애플리케이션을 강화하세요.
weight: 11
url: /ko/net/vector-image-processing/draw-raster-image-on-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.Imaging에서 SVG에 래스터 이미지를 그리는 방법


.NET 프로그래밍 세계에서 Aspose.Imaging은 다양한 이미지 관련 작업을 처리하기 위한 안정적이고 다재다능한 라이브러리입니다. 그것이 제공하는 흥미로운 기능 중 하나는 SVG 캔버스에 래스터 이미지를 그리는 기능입니다. 이 단계별 가이드에서는 Aspose.Imaging for .NET을 사용하여 SVG에 래스터 이미지를 그리는 과정을 안내합니다.

## 전제 조건

세부 사항을 살펴보기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET용 Aspose.Imaging: 라이브러리가 설치되어 있어야 합니다. 그렇지 않은 경우 다음에서 다운로드할 수 있습니다.[.NET 다운로드 페이지용 Aspose.Imaging](https://releases.aspose.com/imaging/net/).

-  귀하의 문서 디렉토리: 교체`"Your Document Directory"` 작업 디렉터리의 실제 경로를 사용하세요.

이제 프로세스를 따라하기 쉬운 단계로 나누어 보겠습니다.

## 1단계: 필요한 네임스페이스 가져오기

Aspose.Imaging을 사용하려면 필수 네임스페이스를 가져와야 합니다.

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## 2단계: 이미지 로드

- 먼저, SVG 캔버스에 그리려는 래스터 이미지를 로드합니다.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- 다음으로 래스터 이미지를 그리려는 곳에 SVG 캔버스 이미지를 로드합니다.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## 3단계: SVG 이미지에 그리기

이제 기존 SVG 이미지에 그리기를 시작할 수 있습니다. 이렇게 하려면 다음 인스턴스를 생성해야 합니다.`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## 4단계: 래스터 이미지 그리기

- 래스터 이미지를 그리려는 경계를 정의하고 래스터 이미지에서 소스 영역을 지정합니다.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## 5단계: 결과 저장

SVG 캔버스에 래스터 이미지를 그린 후 결과 이미지를 저장할 수 있습니다.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## 결론

축하해요! .NET용 Aspose.Imaging을 사용하여 SVG 캔버스에 래스터 이미지를 성공적으로 그렸습니다. 이는 .NET 애플리케이션 내에서 풍부하고 동적인 이미지를 생성하는 데 매우 유용할 수 있습니다.

 자세한 내용과 자세한 문서를 보려면 다음을 방문하세요.[.NET 문서용 Aspose.Imaging](https://reference.aspose.com/imaging/net/).

## 자주 묻는 질문

### .NET용 Aspose.Imaging이란 무엇입니까?
   Aspose.Imaging for .NET은 개발자가 .NET 애플리케이션 내에서 다양한 형식의 이미지를 생성, 조작 및 변환할 수 있는 강력한 이미지 처리 라이브러리입니다.

### 상업용 프로젝트에서 .NET용 Aspose.Imaging을 사용할 수 있나요?
    예, 상업용 및 비상업적 프로젝트 모두에서 Aspose.Imaging for .NET을 사용할 수 있습니다. 라이선스 세부정보는 다음에서 확인할 수 있습니다.[구매 페이지](https://purchase.aspose.com/buy).

### 무료 평가판이 제공되나요?
    예, 다음에서 Aspose.Imaging for .NET의 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).

### 어디서 지원을 받거나 질문을 할 수 있나요?
    질문이 있거나 지원이 필요한 경우 다음 사이트를 방문하세요.[Aspose.이미징 포럼](https://forum.aspose.com/).

### .NET용 Aspose.Imaging의 임시 라이선스를 어떻게 얻을 수 있나요?
    임시면허를 받을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).



{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
