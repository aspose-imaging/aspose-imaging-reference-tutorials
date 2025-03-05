---
title: .NET용 Aspose.Imaging에서 DJVU 페이지 범위를 별도의 이미지로 변환
linktitle: .NET용 Aspose.Imaging에서 DJVU 페이지 범위를 별도의 이미지로 변환
second_title: Aspose.Imaging .NET 이미지 처리 API
description: .NET용 Aspose.Imaging을 사용하여 DJVU 페이지를 별도의 이미지로 변환하는 방법을 알아보세요. 단계별 가이드, 코드 예제 및 FAQ가 제공됩니다.
type: docs
weight: 19
url: /ko/net/image-format-conversion/convert-range-of-djvu-pages-to-separate-images/
---
이미지 변환 및 조작 작업을 처리할 강력한 .NET 라이브러리를 찾고 있다면 Aspose.Imaging for .NET이 완벽한 선택입니다. 이 튜토리얼에서는 Aspose.Imaging을 사용하여 다양한 DJVU 페이지를 별도의 이미지로 변환하는 과정을 안내합니다. 이 작업을 수행하는 데 도움이 되는 단계별 지침과 코드 조각을 찾을 수 있습니다.

## 전제 조건

변환 프로세스를 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1. .NET 라이브러리용 Aspose.Imaging

 .NET용 Aspose.Imaging이 설치되어 있어야 합니다. 아직 다운로드하지 않으셨다면, 다음 사이트에서 다운로드하실 수 있습니다.[.NET 페이지용 Aspose.Imaging](https://releases.aspose.com/imaging/net/).

2. 개발 환경

계속하려면 Visual Studio 또는 기타 .NET IDE를 사용하여 개발 환경을 설정해야 합니다.

## 필요한 네임스페이스 가져오기

먼저 Aspose.Imaging을 사용하려면 코드에 필수 네임스페이스를 포함해야 합니다. 방법은 다음과 같습니다.

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Djvu;
using Aspose.Imaging.FileFormats.Djvu.Options;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.RasterImage;
```

## DJVU 페이지 변환

이제 Aspose.Imaging for .NET을 사용하여 다양한 DJVU 페이지를 별도의 이미지로 변환하는 과정을 일련의 따라하기 쉬운 단계로 나누어 보겠습니다.

### 1단계: DJVU 이미지 로드

 시작하려면 변환하려는 DJVU 이미지를 로드해야 합니다. 바꾸다`"Your Document Directory"` DJVU 파일의 실제 경로를 사용하세요.

```csharp
string dataDir = "Your Document Directory";

// DjVu 이미지 로드
using (DjvuImage image = (DjvuImage)Image.Load(dataDir + "Sample.djvu"))
{
    // 추가 처리를 위한 코드가 여기에 표시됩니다.
}
```

### 2단계: 내보내기 옵션 설정

이제`BmpOptions` 결과 이미지에 대해 원하는 옵션을 구성합니다. 이 예에서는`BitsPerPixel` 32까지.

```csharp
BmpOptions exportOptions = new BmpOptions();
exportOptions.BitsPerPixel = 32;
```

### 3단계: 페이지 범위 정의

 내보내려는 페이지 범위를 지정하려면`IntRange` 페이지 범위로 초기화합니다. 이 경우 페이지 0에서 2를 내보냅니다.

```csharp
IntRange range = new IntRange(0, 2);
```

### 4단계: 페이지 반복

이제 지정된 범위 내의 페이지를 반복하고 각 페이지를 별도의 BMP 이미지로 저장합니다. DJVU 파일은 레이어링을 지원하지 않으므로 각 페이지를 개별적으로 저장합니다.

```csharp
int counter = 0;
foreach (var i in range.Range)
{
    exportOptions.MultiPageOptions = new DjvuMultiPageOptions(range.GetArrayOneItemFromIndex(counter));
    image.Save(dataDir + string.Format("{0}_out.bmp", counter++), exportOptions);
}
```

그리고 그게 다야! .NET용 Aspose.Imaging을 사용하여 다양한 DJVU 페이지를 별도의 이미지로 성공적으로 변환했습니다.

## 결론

.NET용 Aspose.Imaging은 이미지 변환 작업을 단순화하므로 개발자에게 탁월한 선택입니다. 이 튜토리얼에서는 DJVU 페이지를 별도의 이미지로 변환하는 과정을 단계별로 안내했습니다. 올바른 코드와 라이브러리를 사용하면 이미지 변환이 쉬워집니다.

## FAQ

### Q1: Aspose.Imaging for .NET은 무료 라이브러리인가요?

 A1: 아니요, 상업용 라이브러리입니다. 하지만 다운로드할 수 있습니다.[무료 시험판](https://releases.aspose.com/) 그 능력을 테스트하기 위해.

### Q2: Aspose.Imaging for .NET의 임시 라이선스를 구입할 수 있나요?

 A2: 네, 임시 면허를 취득할 수 있습니다.[구매 페이지](https://purchase.aspose.com/temporary-license/).

### Q3: Aspose.Imaging for .NET에 대한 설명서는 어디에서 찾을 수 있습니까?

 A3: 포괄적인 문서를 탐색할 수 있습니다.[여기](https://reference.aspose.com/imaging/net/).

### Q4: Aspose.Imaging for .NET은 어떤 이미지 형식을 지원합니까?

A4: .NET용 Aspose.Imaging은 BMP, JPEG, PNG, TIFF 등을 포함한 광범위한 이미지 형식을 지원합니다.

### Q5: 문제가 발생하면 지원을 받을 수 있나요?

 답변 5: 예, 다음 웹사이트에서 도움을 구하고 커뮤니티와 소통할 수 있습니다.[Aspose.이미징 포럼](https://forum.aspose.com/).