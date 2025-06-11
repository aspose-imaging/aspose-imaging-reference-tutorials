---
"description": "Aspose.Imaging for Java를 사용하여 Java에서 TIFF 프레임을 BMP 형식으로 추출하는 방법을 알아보세요. 단계별 가이드를 따라 해 보세요."
"linktitle": "TIFF 프레임을 BMP 형식으로 추출"
"second_title": "Aspose.Imaging Java 이미지 처리 API"
"title": "Aspose.Imaging for Java를 사용한 TIFF-BMP 변환"
"url": "/ko/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/"
"weight": 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java를 사용한 TIFF-BMP 변환

Java에서 이미지 파일, 특히 TIFF 이미지를 작업하고 프레임을 추출하여 BMP 형식으로 저장해야 하는 경우, Aspose.Imaging for Java는 강력하고 다재다능한 도구입니다. 이 단계별 가이드에서는 Aspose.Imaging for Java를 사용하여 TIFF 프레임을 BMP 형식으로 추출하는 과정을 안내합니다.

## 필수 조건

시작하기에 앞서 다음과 같은 전제 조건이 충족되었는지 확인하세요.

1. Java 개발 환경: 시스템에 작동하는 Java 개발 환경이 설정되어 있어야 합니다.

2. Aspose.Imaging for Java: Aspose.Imaging for Java 라이브러리가 설치되어 있는지 확인하세요. 웹사이트에서 다운로드할 수 있습니다. [여기](https://releases.aspose.com/imaging/java/).

3. 샘플 TIFF 이미지: 프레임을 추출할 샘플 TIFF 이미지 파일을 준비하세요. 작업 디렉터리에 이 이미지를 준비해 두세요.

## 패키지 가져오기

프로세스를 시작하려면 Java 애플리케이션에 필요한 패키지를 가져와야 합니다.

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## 1단계: TIFF 이미지 로드 및 프레임 카운터 초기화

```java
// 문서 디렉토리의 경로입니다.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // TiffImage의 프레임을 추적하기 위해 int 인스턴스를 생성합니다.
    int frameCounter = 0;
```

## 2단계: TIFF 프레임 반복

```java
    // TiffImage의 TiffFrames를 반복합니다.
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

## 3단계: TiffFrame의 픽셀을 색상 배열에 로드합니다.

```java
        // TiffFrame의 픽셀을 색상 배열에 로드합니다.
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

## 4단계: BMP 옵션 생성 및 픽셀당 비트 설정

```java
        // bmpCreateOptions 인스턴스를 생성합니다.
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

## 5단계: BMP 이미지 저장

```java
            // 출력이 저장될 위치를 지정하여 bmpCreateOptions의 소스를 FileCreateSource로 설정합니다.
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // 새로운 bmpImage를 만듭니다
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // TiffFrame의 픽셀로 bmpImage를 저장합니다.
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## 결론

이 튜토리얼에서는 Aspose.Imaging for Java를 사용하여 TIFF 프레임을 추출하고 BMP 이미지로 저장하는 방법을 살펴보았습니다. 적절한 사전 요구 사항을 충족하고 단계별 가이드를 따르면 Java 애플리케이션에서 이 이미지 변환 작업을 쉽게 수행할 수 있습니다.

## 자주 묻는 질문

### Q1: Java용 Aspose.Imaging이란 무엇인가요?

A1: Aspose.Imaging for Java는 광범위한 이미지 처리 기능을 제공하는 Java 라이브러리로, 다양한 이미지 형식으로 작업하고 변환, 편집, 조작과 같은 작업을 수행할 수 있습니다.

### 질문 2: Aspose.Imaging for Java를 다양한 이미지 포맷으로 사용할 수 있나요?

A2: 네, Aspose.Imaging for Java는 TIFF, BMP, JPEG, PNG 등 다양한 이미지 형식을 지원하므로 이미지 관련 작업에 유용한 도구입니다.

### 질문 3: Java용 Aspose.Imaging에 대한 문서는 어디에서 찾을 수 있나요?

A3: Aspose.Imaging for Java에 대한 자세한 설명서를 찾을 수 있습니다. [여기](https://reference.aspose.com/imaging/java/).

### 질문 4: Aspose.Imaging for Java에 대한 무료 평가판이 있나요?

A4: 네, 무료 평가판을 통해 Aspose.Imaging for Java를 탐색할 수 있습니다. [여기](https://releases.aspose.com/).

### 질문 5: Java용 Aspose.Imaging에 대한 지원은 어떻게 받을 수 있나요?

A5: Aspose.Imaging for Java 관련 질문, 문제 또는 지원이 필요한 경우 지원 포럼을 방문하세요. [여기](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}