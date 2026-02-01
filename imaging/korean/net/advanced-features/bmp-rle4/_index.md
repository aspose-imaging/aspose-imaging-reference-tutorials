---
date: 2026-02-01
description: Aspose.Imaging for .NET에서 RLE4 압축을 사용하여 BMP 이미지를 압축하고 품질 손실 없이 BMP 크기를
  줄이는 방법을 배워보세요.
linktitle: BMP RLE4 in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: .NET용 Aspose.Imaging에서 RLE4를 사용하여 BMP 이미지 압축
url: /ko/net/advanced-features/bmp-rle4/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET에서 RLE4를 사용하여 BMP 이미지 압축하기

시각적 품질을 유지하면서 **BMP 이미지를 압축**해야 한다면, RLE4 압축 방식은 특히 4‑bit 이미지에 적합한 가볍고 무손실(Loss‑less) 솔루션입니다. 이 튜토리얼에서는 .NET 프로젝트 설정부터 Aspose.Imaging을 사용해 RLE4 압축으로 BMP 파일을 저장하는 방법까지 모든 과정을 단계별로 안내합니다. 끝까지 따라오면 **BMP 크기를 크게 감소**시킬 수 있으며, 이 기술을 모든 C# 애플리케이션에 통합할 수 있게 됩니다.

## Quick Answers
- **What is the primary library?** Aspose.Imaging for .NET  
- **Which compression does this guide cover?** BMP RLE4 (4‑bit)  
- **Can I use it in .NET Core?** Yes, the API is fully compatible  
- **Do I need a license for testing?** A temporary license is sufficient for evaluation  
- **Typical size reduction?** Up to 60 % for 4‑bit BMPs with repetitive patterns  

## What is BMP RLE4 compression?
RLE4(런‑길이 인코딩 4‑bit)는 같은 색을 공유하는 연속된 픽셀을 하나의 개수/값 쌍으로 저장합니다. 이 방식은 픽셀 데이터를 손실 없이 파일 크기를 줄여주어 아이콘, 단순 그래픽 또는 4‑bit 팔레트만으로 충분한 이미지에 이상적입니다.

## Why compress BMP image with RLE4 in .NET?
- **Loss‑less** – 원본 픽셀 데이터를 완전히 복원할 수 있습니다.  
- **Fast processing** – 최소한의 CPU 오버헤드로 실시간 시나리오에 적합합니다.  
- **Cross‑platform** – Windows, Linux, macOS에서 .NET 5/6/7과 함께 작동합니다.  
- **Integrates with Aspose.Imaging** – 압축 외에도 풍부한 이미지 조작 기능을 제공합니다.

## Prerequisites
1. **Aspose.Imaging for .NET** – 최신 패키지는 [공식 사이트](https Visual Studio, Rider, 또는 .NET 지식** – 이미지를 로드하고 저장하기 위해 몇 줄의 C# 코드를 작성하게 됩니다.  
4. **문서 디렉터리** – 스니펫의 `"Your Document Directory"`를 BMP 파일이 위치한 경로로 교체하십시오.

## Import.

### Step 1: Import Aspose.Imaging Namespace
```csharp
using Aspose.Imaging;
```
이 지시문을 통해 `Image`, `BmpOptions`## BMP RLE4 Compression in Aspose.Imaging for .NET

아래는 전체 워크플로우를 단계별로 안내합니다.

### Step 2: Initialize Your Data Directory
```csharp
string dataDir = "Your Document Directory";
```
`dataDir`을 소스 BMP(`Rle4.bmp`)가 들어 있는 폴더와 출력 파일이 기록될 폴더로 설정합니다.

### Step 3: Load the Image
```csharp
using (Image image = Image.Load(Path.Combine(dataDir, "Rle4.bmp")))
{
    // Your code for image processing goes here
}
```
`Image.Load`는 BMP 형식을 자동으로 감지하고 이후 작업을 위해 준비합니다.

### Step 4: Apply BMP RLE4 Compression
```csharp
image.Save(
    System.IO.Path.Combine(dataDir, "output.bmp"),
    new BmpOptions()
    {
        Compression = BitmapCompression.Rle4,
        BitsPerPixel = 4,
        Palette = ColorPaletteHelper.Create4Bit()
    });
```
여기서는:
- `Compression`을 `BitmapCompression.Rle4`를 강제합니다.  
- `ColorPaletteHelper.Create4Bit()`를 사용해 4### Step 5: Clean Up (Optional)
```csharp
File.Delete(System.IO.Path.Combine(dataDir, "output.bmp"));
```
테스트용으로만 사용했다면 임- **Convert BMP format** – `BmpOptions`를 `PngOptions` 또는 `JpegOptions`로 교체하면 출력 형식을 PNG, JPEG 등으로 변경 JPEG, TIFF, WebP 압축도 지원하므로 모든 일반 이미지 형식을 하나의 API로 처리할 수 있습니다.  
- **BMP compression C#** – 8‑bit 이미지에 `과 팔레트를 적절히 조정하면 됩니다.

## Common Pitfalls & Troubleshooting
| 문제 | 원인 | 해결책 |
|------|------|--------|
| 출력 파일이 원본보다 큼 | 필요 이상으로 많은 색상의하도록 확인하십시오 (RLE4의 경우 4). |
| `Save` 시 `ArgumentException` | `using System.IO;` 누락 | 파일 상단에 `using System가 이미 4‑bit이며 연속된 픽셀이 거의 없음 | RLE는 반복되는 픽셀 패턴에 가장 효과적이므로 아이콘이나 단순 그래픽으로 테스트하십시오. |

## Frequently Asked Questions

**Q: BMP RLE4 압축이 픽셀을 하나의 개수/값 쌍으로 인코딩합니다. 색상이 많이 반복되는 4‑bit 이미지, 예를 들어 아이콘이나 단순 그래픽에 가장 적합합니다.

**Q:환할 수 있나요?**  
A: 네, 라이브러리는 JPEG, PNG, TIFF 등 다양한 형식으로 변환을 지원합니다. BMP를 로드한 뒤 원하는 옵션으로 저장하면 됩니다.

**Q: Aspose.Imaging for .NET이 Windows와 .NET Core 애플리케이션 모두에 적합한가요?**  
A: 물론입니다. 이 API는 .NET Framework, .NET Core, 그리고 .NET 5/6/7을 포함한 모든 주요 운영 체제에서 동작합니다.

**Q: Aspose.Imagingose 전문가와 소통하려면 [Aspose.Imaging 지원 포럼](https://forum.aspose.com/)을 방문하십시오.

**Q: Aspose.Imaging for .NET의 임시 라이선스를 어떻게 받을 수 있나요?**  
A: Aspose 웹사이트의 [임시 라이선스 페이지](https://purchase.aspose.com/temporary-license/)에서 요청할 수 있습니다.

## Conclusion
이제 Aspose.Imaging for .NET을 사용해 RLE4 방식을 통해 **BMP 이미지를 압축**하는 방법을 익혔습니다. 이 방법을 사용하면 품질을 손상시키지 않고 **BMP 크기를 감소**시킬 수 있으며, .NET Framework든 .NET Core든 모든 C# 프로젝트에 자연스럽게 통합됩니다. 다양한 팔레트와 이미지 소스를 실험해 보면서 여러분의 사용 사례에 가장 적합한 결과를 찾아보세요.

자세한 내용은 전체 [Aspose.Imaging for .NET 문서](https://reference.aspose.com/imaging/net/)를 확인하십시오.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2026- Aspose.Imaging for .NET 24.11 (latest at time of writing)  
**작성자:** Aspose