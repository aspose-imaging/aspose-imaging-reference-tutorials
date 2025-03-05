---
title: Java용 Aspose.Imaging을 사용하여 TIFF에서 BMP로 변환
linktitle: TIFF 프레임을 BMP 형식으로 추출
second_title: Aspose.Imaging Java 이미지 처리 API
description: Aspose.Imaging for Java를 사용하여 Java에서 TIFF 프레임을 BMP 형식으로 추출하는 방법을 알아보세요. 단계별 가이드를 따르세요.
type: docs
weight: 13
url: /ko/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
---
Java로 이미지 파일, 특히 TIFF 이미지를 작업하고 그 파일에서 프레임을 추출하여 BMP 형식으로 저장해야 한다면 Aspose.Imaging for Java는 이를 달성하기 위한 강력하고 다재다능한 도구입니다. 이 단계별 가이드에서는 Aspose.Imaging for Java를 사용하여 TIFF 프레임을 BMP 형식으로 추출하는 과정을 안내합니다.

## 전제 조건

시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1. Java 개발 환경: 시스템에 Java 개발 환경이 설정되어 있어야 합니다.

2.  Aspose.Imaging for Java: Aspose.Imaging for Java 라이브러리가 설치되어 있는지 확인하세요. 홈페이지에서 다운로드 받으실 수 있습니다[여기](https://releases.aspose.com/imaging/java/).

3. 샘플 TIFF 이미지: 프레임을 추출하려는 샘플 TIFF 이미지 파일이 있습니다. 작업 디렉터리에서 이 이미지를 사용할 수 있는지 확인하세요.

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
// 문서 디렉터리의 경로입니다.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // TiffImage에서 프레임을 추적하기 위해 int 인스턴스를 만듭니다.
    int frameCounter = 0;
```

## 2단계: TIFF 프레임 반복

```java
    // TiffImage에서 TiffFrames를 반복합니다.
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

## 3단계: TiffFrame의 픽셀을 색상 배열로 로드

```java
        // TiffFrame의 픽셀을 색상 배열로 로드
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

## 4단계: BMP 옵션 생성 및 픽셀당 비트 설정

```java
        // bmpCreateOptions 인스턴스 생성
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

## 5단계: BMP 이미지 저장

```java
            // 출력이 저장될 위치를 지정하여 bmpCreateOptions의 소스를 FileCreateSource로 설정합니다.
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // 새 bmpImage 만들기
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

이 튜토리얼에서는 Aspose.Imaging for Java를 사용하여 TIFF 프레임을 추출하고 BMP 이미지로 저장하는 방법을 다루었습니다. 올바른 전제 조건과 단계별 가이드를 따르면 Java 애플리케이션에서 이 이미지 변환 작업을 쉽게 수행할 수 있습니다.

## FAQ

### Q1: Java용 Aspose.Imaging이 무엇인가요?

A1: Aspose.Imaging for Java는 광범위한 이미지 처리 기능을 제공하는 Java 라이브러리로, 다양한 이미지 형식으로 작업하고 변환, 편집, 조작과 같은 작업을 수행할 수 있습니다.

### Q2: 다양한 이미지 형식으로 Java용 Aspose.Imaging을 사용할 수 있나요?

A2: 예, Aspose.Imaging for Java는 TIFF, BMP, JPEG, PNG 등을 포함한 광범위한 이미지 형식을 지원하므로 이미지 관련 작업을 위한 다목적 도구입니다.

### Q3: Aspose.Imaging for Java에 대한 설명서는 어디서 찾을 수 있나요?

 A3: Aspose.Imaging for Java에 대한 자세한 문서를 찾을 수 있습니다.[여기](https://reference.aspose.com/imaging/java/).

### Q4: Aspose.Imaging for Java에 대한 무료 평가판이 있습니까?

A4: 예, 무료 평가판을 통해 Aspose.Imaging for Java를 탐색할 수 있습니다.[여기](https://releases.aspose.com/).

### Q5: Java용 Aspose.Imaging에 대한 지원을 받으려면 어떻게 해야 합니까?

 A5: Aspose.Imaging for Java와 관련된 질문, 문제 또는 지원이 있는 경우 지원 포럼을 방문하세요.[여기](https://forum.aspose.com/).