---
date: 2025-12-19
description: Aspose.Imaging을 사용하여 Java에서 TIFF를 BMP로 변환하는 방법을 배워보세요. 이 단계별 Java 이미지
  처리 튜토리얼은 다중 페이지 TIFF 파일의 이미지 변환 방법을 보여줍니다.
linktitle: Extract TIFF Frames to BMP Format
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java를 사용하여 TIFF를 BMP로 변환하는 방법
url: /ko/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# TIFF를 BMP로 변환하기 (Aspose.Imaging for Java)

Java 애플리케이션 내부에서 **TIFF를 BMP로 변환**해야 한다면, 바로 이곳이 맞습니다. 단일 페이지 TIFF든 다중 페이지 문서든, Aspose.Imaging for Java는 과정을 간단하고 안정적으로 만들어 줍니다. 이 튜토리얼에서는 TIFF 파일의 각 프레임을 추출하여 개별 BMP 이미지로 저장하는 방법을 단계별로 안내합니다—이미지 변환 Java 시나리오에 최적입니다.

## Quick Answers
- **어떤 라이브러리가 변환을 담당하나요?** Aspose.Imaging for Java  
- **다중 페이지 TIFF를 처리할 수 있나요?** 예 – 각 프레임이 별도의 BMP로 저장됩니다  
- **상용 환경에 라이선스가 필요합니까?** 상업적 사용을 위해서는 유효한 Aspose 라이선스가 필요합니다  
- **지원되는 Java 버전은?** 8 이상  
- **코드 실행 시간은 얼마나 걸리나요?** 일반적인 크기의 이미지라면 몇 초 내외입니다  

## Prerequisites

시작하기 전에 다음 사전 조건을 확인하십시오:

1. **Java 개발 환경** – JDK(8 이상)와 선택한 IDE 또는 빌드 도구가 설치되어 있어야 합니다.  
2. **Aspose.Imaging for Java** – 최신 JAR 파일을 [여기](https://releases.aspose.com/imaging/java/)에서 다운로드하십시오.  
3. **샘플 TIFF 이미지** – 프로젝트 작업 디렉터리에 위치한 단일 또는 다중 페이지 TIFF 파일입니다.

## Import Packages

Java 애플리케이션에서 필요한 패키지를 가져와야 합니다:

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## Step‑by‑Step Guide to convert tiff to bmp

### Step 1: Load the TIFF Image and Initialize Frame Counter

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // Create an instance of int to keep track of frames in TiffImage
    int frameCounter = 0;
```

### Step 2: Iterate Over TIFF Frames

```java
    // Iterate over the TiffFrames in TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

### Step 3: Load Pixels of TiffFrame into an Array of Colors

```java
        // Load Pixels of TiffFrame into an array of Colors
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

### Step 4: Create BMP Options and Set Bits Per Pixel

```java
        // Create an instance of bmpCreateOptions
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

### Step 5: Save BMP Image

```java
            // Set the Source of bmpCreateOptions as FileCreateSource by specifying the location where output will be saved
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // Create a new bmpImage
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // Save the bmpImage with pixels from TiffFrame
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## Why use Aspose.Imaging for Java?

- **강력한 다중 페이지 지원** – 추가 코드 없이 TIFF 프레임 수에 제한 없이 처리합니다.  
- **Pure Java 구현** – 네이티브 의존성이 없어 크로스 플랫폼 배포에 이상적입니다.  
- **고품질 BMP 출력** – 비트‑퍼‑픽셀, 압축, 색 깊이를 자유롭게 제어할 수 있습니다.  
- **포괄적인 이미지 변환 Java 툴킷** – JPEG, PNG, GIF 등 다양한 포맷을 지원합니다.

## Common Issues & Troubleshooting

| 증상 | 가능한 원인 | 해결 방법 |
|---------|--------------|-----|
| `OutOfMemoryError`가 큰 TIFF 로드 중 발생 | 전체 이미지를 메모리에 로드 | 프레임을 하나씩 처리하거나 JVM 힙 크기(`-Xmx`)를 늘리세요 |
| BMP 파일이 손상됨 | `BitsPerPixel` 값이 잘못 지정됨 | 진정한 컬러 BMP는 24 또는 32를 사용하세요 |
| 출력 파일이 생성되지 않음 | 출력 디렉터리 경로 오류 | `Your Document Directory`가 존재하는 폴더인지 확인하세요 |

## Frequently Asked Questions

### Q1: Aspose.Imaging for Java란 무엇인가요?

A1: Aspose.Imaging for Java는 다양한 이미지 포맷을 다루고 변환, 편집, 조작 등의 작업을 수행할 수 있는 포괄적인 이미지 처리 라이브러리입니다.

### Q2: Aspose.Imaging for Java를 다른 이미지 포맷과 함께 사용할 수 있나요?

A2: 예, Aspose.Imaging for Java는 TIFF, BMP, JPEG, PNG 등을 포함한 광범위한 이미지 포맷을 지원하므로 이미지 관련 작업에 다재다능합니다.

### Q3: Aspose.Imaging for Java에 대한 문서는 어디서 찾을 수 있나요?

A3: 자세한 문서는 [여기](https://reference.aspose.com/imaging/java/)에서 확인할 수 있습니다.

### Q4: Aspose.Imaging for Java의 무료 체험판이 있나요?

A4: 예, 무료 체험판은 [여기](https://releases.aspose.com/)에서 이용할 수 있습니다.

### Q5: Aspose.Imaging for Java에 대한 지원은 어떻게 받나요?

A5: 질문, 이슈 또는 지원이 필요하면 지원 포럼을 방문하십시오: [여기](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2025-12-19  
**테스트 환경:** Aspose.Imaging for Java 24.12 (최신)  
**작성자:** Aspose  

---