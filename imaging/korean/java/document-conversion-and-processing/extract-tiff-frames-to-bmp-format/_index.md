---
date: 2026-05-03
description: Aspose.Imaging을 사용하여 Java에서 다중 페이지 TIFF를 BMP 형식으로 변환하는 방법을 배웁니다. TIFF를
  효율적으로 변환하는 단계별 가이드를 따라 보세요.
keywords:
- convert multi page tiff
- how to convert tiff
- Aspose.Imaging Java
- TIFF to BMP conversion
- image processing Java
linktitle: TIFF 프레임을 BMP 형식으로 추출
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java를 사용하여 다중 페이지 TIFF를 BMP로 변환
url: /ko/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java를 사용하여 다중 페이지 TIFF를 BMP로 변환

Java 환경에서 **다중 페이지 TIFF** 파일을 개별 BMP 이미지로 변환해야 한다면, 올바른 곳에 오셨습니다. 이 튜토리얼에서는 강력한 Aspose.Imaging for Java 라이브러리를 사용하여 각 TIFF 프레임을 추출하고 BMP 파일로 저장하는 정확한 단계를 안내합니다. 끝까지 읽으면 *TIFF 파일을 프로그래밍 방식으로 변환하는 방법*뿐만 아니라 이 접근 방식이 배치 이미지 처리 작업에 왜 신뢰할 수 있는지도 이해하게 됩니다.

## 빠른 답변
- **TIFF를 BMP로 변환하기에 가장 좋은 라이브러리는?** Aspose.Imaging for Java  
- **필요한 코드 라인은 몇 줄인가요?** 논리적 단계 5개에 걸쳐 약 30줄  
- **프로덕션에 라이선스가 필요합니까?** 예, 상업용 라이선스가 필요합니다(무료 체험 가능)  
- **대용량 다중 페이지 TIFF를 처리할 수 있나요?** 예, API가 프레임을 효율적으로 스트리밍합니다  
- **지원되는 Java 버전은?** Java 8 이상  

## “다중 페이지 TIFF 변환”이란?
다중 페이지 TIFF를 변환한다는 것은 단일 TIFF 컨테이너에 저장된 각 페이지(또는 프레임)를 독립적인 이미지 파일—여기서는 BMP—로 내보내는 것을 의미합니다. 이는 문서 보관, 의료 영상 또는 추가 처리를 위해 래스터 이미지가 필요한 모든 워크플로에 유용합니다.

## 왜 Aspose.Imaging for Java를 사용하나요?
- **전체 형식 지원** – TIFF, BMP, JPEG, PNG 등 다양한 형식을 처리합니다.  
- **외부 종속성 없음** – 순수 Java이며 네이티브 라이브러리가 필요 없습니다.  
- **고성능** – 프레임에 대한 스트리밍 접근으로 메모리 사용량을 줄입니다.  
- **풍부한 API** – 픽셀 데이터, 색 깊이 및 메타데이터에 대한 세밀한 제어를 제공합니다.

## 사전 요구 사항
1. **Java 개발 환경** – JDK 8 이상 및 선호하는 IDE.  
2. **Aspose.Imaging for Java** – 공식 사이트에서 최신 JAR을 **[here](https://releases.aspose.com/imaging/java/)** 에서 다운로드합니다.  
3. **샘플 다중 페이지 TIFF** – 코드가 읽을 수 있는 알려진 디렉터리에 TIFF 파일(예: `sample.tiff`)을 배치합니다.

## 패키지 가져오기

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## Aspose.Imaging을 사용하여 다중 페이지 TIFF를 BMP로 변환하는 방법

### 단계 1: TIFF 이미지 로드 및 프레임 카운터 초기화

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // Create an instance of int to keep track of frames in TiffImage
    int frameCounter = 0;
```

### 단계 2: TIFF 프레임 반복

```java
    // Iterate over the TiffFrames in TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

### 단계 3: TiffFrame의 픽셀을 색 배열에 로드

```java
        // Load Pixels of TiffFrame into an array of Colors
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

### 단계 4: BMP 옵션 생성 및 비트당 픽셀 설정

```java
        // Create an instance of bmpCreateOptions
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

### 단계 5: BMP 이미지 저장

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

## 일반적인 함정 및 팁
- **메모리 사용량:** 매우 큰 TIFF 파일을 다룰 때는 전체 이미지를 메모리에 로드하는 대신 프레임을 하나씩 처리하는 것이 좋습니다(위 예시와 같이).  
- **파일 명명:** `String.format` 호출은 각 프레임에 대해 고유한 파일명을 생성합니다(`...out0.bmp`, `...out1.bmp` 등). 다른 명명 규칙이 필요하면 패턴을 조정하십시오.  
- **비트 깊이:** BMP는 다양한 비트 깊이를 지원합니다; 대부분의 경우 24비트(진정한 컬러)가 작동합니다. 8비트 그레이스케일 출력을 원하면 `setBitsPerPixel`을 변경하십시오.

## FAQ

### Q1: Aspose.Imaging for Java란?
A1: Aspose.Imaging for Java는 다양한 이미지 형식을 다루고 변환, 편집, 조작과 같은 작업을 수행할 수 있는 광범위한 이미지 처리 기능을 제공하는 Java 라이브러리입니다.

### Q2: Aspose.Imaging for Java를 다양한 이미지 형식과 함께 사용할 수 있나요?
A2: 예, Aspose.Imaging for Java는 TIFF, BMP, JPEG, PNG 등 다양한 이미지 형식을 지원하므로 이미지 관련 작업에 다재다능한 도구입니다.

### Q3: Aspose.Imaging for Java 문서는 어디에서 찾을 수 있나요?
A3: Aspose.Imaging for Java에 대한 자세한 문서는 **[here](https://reference.aspose.com/imaging/java/)** 에서 확인할 수 있습니다.

### Q4: Aspose.Imaging for Java의 무료 체험이 있나요?
A4: 예, **[here](https://releases.aspose.com/)** 에서 무료 체험을 통해 Aspose.Imaging for Java를 살펴볼 수 있습니다.

### Q5: Aspose.Imaging for Java 지원을 어떻게 받을 수 있나요?
A5: Aspose.Imaging for Java와 관련된 질문, 문제 또는 지원이 필요하면 **[here](https://forum.aspose.com/)** 에서 지원 포럼을 방문하십시오.

## 자주 묻는 질문

**Q: 동일한 방법으로 다중 페이지 TIFF를 다른 형식(예: PNG)으로 변환할 수 있나요?**  
A: 물론입니다. `BmpOptions`를 해당 옵션 클래스(예: `PngOptions`)로 교체하고 `FileCreateSource` 경로의 파일 확장자를 조정하면 됩니다.

**Q: Aspose.Imaging이 압축된 TIFF(LZW, CCITT)를 처리하나요?**  
A: 예, 라이브러리는 프레임 추출 중에 지원되는 TIFF 압축 방식을 투명하게 압축 해제합니다.

**Q: BMP로 변환할 때 EXIF 메타데이터를 보존할 수 있나요?**  
A: BMP는 EXIF 메타데이터를 지원하지 않습니다. 메타데이터를 유지해야 한다면 해당 메타데이터를 지원하는 형식(예: PNG)으로 변환하거나 변환 후 수동으로 메타데이터를 복사하십시오.

**Q: 폴더 내 여러 TIFF 파일을 배치 처리하려면 어떻게 해야 하나요?**  
A: 위 코드를 디렉터리의 `File` 객체를 순회하는 루프로 감싸고 각 파일에 대해 `dataDir` 및 소스 파일명을 업데이트하면 됩니다.

**Q: 상업적 배포를 위해 어떤 라이선스가 필요합니까?**  
A: 프로덕션 사용을 위해서는 유료 Aspose.Imaging for Java 라이선스가 필요합니다. 개발 중에는 임시 체험 라이선스를 사용할 수 있습니다.

---

**마지막 업데이트:** 2026-05-03  
**테스트 환경:** Aspose.Imaging for Java 24.12 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}