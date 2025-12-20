---
date: 2025-12-20
description: Aspose.Imaging for Java를 사용하여 tiff를 png로 변환하고 이미지를 png, bmp 또는 gif로 저장하는
  방법을 배웁니다. 이미지 조작을 위한 단계별 가이드.
linktitle: Frame Saving in Different Raster Formats
second_title: Aspose.Imaging Java Image Processing API
title: TIFF를 PNG로 변환하고 프레임을 다양한 래스터 형식으로 저장하는 방법
url: /ko/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# TIFF를 PNG로 변환하고 다양한 래스터 형식으로 프레임 저장

다중 페이지 TIFF 파일을 다루는 것은 문서 중심 애플리케이션에서 흔한 시나리오입니다. **convert tiff to png**가 필요하거나 개별 프레임을 추출해 다른 래스터 형식으로 저장하려는 경우, Aspose.Imaging for Java는 이 과정을 간단하고 효율적으로 만들어 줍니다. 이 튜토리얼에서는 TIFF를 로드하고, 프레임을 반복하며, 각 프레임을 PNG로 저장하는 정확한 단계를 안내합니다(나중에 BMP 또는 GIF로 쉽게 전환할 수 있습니다).

## 빠른 답변
- **어떤 라이브러리가 이를 처리합니까?** Aspose.Imaging for Java provides full support for TIFF frame extraction and raster format conversion.  
- **라이선스가 필요합니까?** 무료 체험판은 개발에 사용할 수 있으며, 프로덕션 사용을 위해서는 정식 라이선스가 필요합니다.  
- **PNG 대신 BMP 또는 GIF로 저장할 수 있습니까?** 예—`PngOptions`를 `BmpOptions` 또는 `GifOptions`로 교체하면 됩니다.  
- **필요한 Java 버전은 무엇입니까?** Java 8 이상을 권장합니다.  
- **“convert tiff to png”란 무엇입니까?** 이는 TIFF 파일의 각 페이지를 추출하여 PNG 래스터 이미지로 저장하는 것을 의미합니다.

## “convert tiff to png”란 무엇입니까?
TIFF를 PNG로 변환하는 것은 다중 페이지 TIFF를 디코딩하고 각 프레임에 접근한 뒤, 해당 프레임을 손실이 없고 웹 친화적이며 널리 지원되는 PNG 형식으로 인코딩하는 과정을 포함합니다.

## 왜 Aspose.Imaging for Java를 사용합니까?
- **광범위한 형식 지원** – TIFF, PNG, JPEG, BMP, GIF 등 다양한 형식을 처리합니다.  
- **네이티브 종속성 없음** – 순수 Java이며, 모든 JVM 프로젝트에 쉽게 통합할 수 있습니다.  
- **고성능** – 대형 이미지와 다중 페이지 문서에 최적화되었습니다.  
- **간단한 API** – 복잡한 변환을 수행하기 위해 최소한의 코드만 필요합니다.

## 전제 조건
1. **Java 개발 환경** – JDK가 설치되어 있는지 확인하십시오. 아직 설치하지 않았다면 [Oracle website](https://www.oracle.com/java/technologies/javase-downloads)에서 다운로드하십시오.  
2. **Aspose.Imaging for Java 라이브러리** – API 참조는 [documentation](https://reference.aspose.com/imaging/java/)에서 확인하십시오. 라이브러리는 [download page](https://releases.aspose.com/imaging/java/)에서 다운로드할 수 있습니다. 무료 체험판은 [here](https://releases.aspose.com/)에서 제공되며, 정식 라이선스는 [here](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.  
3. **샘플 TIFF 이미지** – 처리할 다중 페이지 TIFF를 준비하십시오.

전제 조건을 모두 확인했으니, 이제 코드로 들어가 보겠습니다.

## Aspose.Imaging for Java를 사용하여 TIFF를 PNG로 변환하는 방법

### 패키지 가져오기
먼저, 필요한 Aspose.Imaging 클래스를 가져옵니다.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

### Step 1: TIFF 이미지 로드
데이터 디렉터리를 초기화하고 소스 TIFF 파일을 로드합니다.

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

### Step 2: 다양한 래스터 형식으로 프레임 저장
각 프레임을 반복하면서 **save image as png**를 수행합니다. **convert tiff to bmp** 또는 **tiff to gif conversion**을 수행하려면 `PngOptions`를 `BmpOptions` 또는 `GifOptions`로 교체하면 됩니다.

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **Pro tip:** TIFF 파일이 처리 후 적절히 해제되도록 예시와 같이 `try‑with‑resources` 블록을 유지하십시오.

## 일반적인 사용 사례
- **문서 보관:** 스캔한 TIFF 문서를 PNG로 변환하여 웹 미리보기에 사용합니다.  
- **썸네일 생성:** TIFF의 첫 번째 프레임을 추출하여 작은 PNG 썸네일로 저장합니다.  
- **형식 마이그레이션:** 레거시 TIFF 자산을 BMP 또는 GIF와 같은 최신 형식으로 이동하여 오래된 시스템과의 호환성을 확보합니다.

## 문제 해결 및 팁
- **프레임 누락:** 소스 TIFF에 실제로 여러 페이지가 포함되어 있는지 확인하십시오; 디버깅을 위해 `multiImage.getFrames().size()`를 사용하세요.  
- **메모리 부족 오류:** 전체 파일을 메모리에 로드하는 대신, 예시와 같이 큰 TIFF를 페이지별로 처리하십시오.  
- **품질 관리:** PNG는 무손실이며, 파일 크기를 줄이려면 품질 설정이 가능한 JPEG 옵션을 고려하십시오.

## 자주 묻는 질문

**Q1: Aspose.Imaging for Java에서 프레임 저장을 지원하는 래스터 형식은 무엇입니까?**  
A1: Aspose.Imaging for Java는 PNG, JPEG, BMP, GIF 등을 포함한 다양한 래스터 형식을 지원합니다. 애플리케이션 요구에 가장 적합한 형식을 선택할 수 있습니다.

**Q2: Aspose.Imaging for Java를 사용하여 다른 이미지 작업을 수행할 수 있습니까?**  
A2: 예, Aspose.Imaging for Java는 리사이징, 크롭, 다양한 필터 및 효과 적용 등 이미지 조작을 위한 포괄적인 기능을 제공합니다. 모든 이미지 처리 요구에 맞는 다목적 도구입니다.

**Q3: Aspose.Imaging for Java의 정식 라이선스를 어떻게 얻을 수 있습니까?**  
A3: Aspose.Imaging for Java의 정식 라이선스를 구매하려면 [purchase page](https://purchase.aspose.com/buy)를 방문하십시오. 프로젝트에 맞는 다양한 라이선스 옵션을 확인할 수 있습니다.

**Q4: Aspose.Imaging for Java의 무료 체험판이 있습니까?**  
A4: 예, [releases page](https://releases.aspose.com/)에서 Aspose.Imaging for Java의 무료 체험판을 이용할 수 있습니다. 구매 전에 라이브러리 기능을 살펴볼 수 있습니다.

**Q5: Aspose.Imaging for Java에 대한 지원이나 도움을 어디서 받을 수 있습니까?**  
A5: Aspose.Imaging for Java와 관련된 질문, 문제 또는 지원이 필요하면 [Aspose Imaging forum](https://forum.aspose.com/)을 방문하십시오. 커뮤니티와 지원팀이 도와드립니다.

---

**마지막 업데이트:** 2025-12-20  
**테스트 환경:** Aspose.Imaging for Java 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}