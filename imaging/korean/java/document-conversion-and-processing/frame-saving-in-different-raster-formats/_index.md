---
date: 2026-04-28
description: Aspose.Imaging for Java를 사용하여 TIFF를 PNG로 변환하는 방법과 TIFF를 다른 래스터 형식으로 변환하는
  방법을 배웁니다. 이미지 조작을 위한 단계별 가이드.
keywords:
- tiff to png java
- how to convert tiff
- Aspose.Imaging Java
linktitle: 다양한 래스터 형식에서 프레임 저장
second_title: Aspose.Imaging Java Image Processing API
title: tiff to png java – TIFF를 PNG로 변환하고 프레임을 다양한 래스터 형식으로 저장
url: /ko/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# tiff to png java – TIFF를 PNG로 변환하고 다양한 래스터 형식으로 프레임 저장

멀티 페이지 TIFF 파일을 다루는 것은 문서 중심 애플리케이션에서 흔한 시나리오입니다. **convert tiff to png**가 필요하거나 개별 프레임을 추출해 다른 래스터 형식으로 저장해야 할 경우, Aspose.Imaging for Java가 프로세스를 간단하고 효율적으로 만들어 줍니다. 이 튜토리얼에서는 TIFF를 로드하고, 프레임을 순회하며 각 프레임을 PNG로 저장하는 정확한 단계를 살펴봅니다(나중에 BMP 또는 GIF로 쉽게 전환할 수 있습니다). 마지막으로 몇 줄의 코드만으로 지원되는 모든 래스터 형식으로 **how to convert tiff**하는 방법도 확인할 수 있습니다.

## 빠른 답변
- **What does “convert tiff to png” mean?** 각 TIFF 파일의 페이지를 추출하여 PNG 래스터 이미지로 저장하는 것을 의미합니다.  
- **Which library handles this?** Aspose.Imaging for Java는 TIFF 프레임 추출 및 래스터 형식 변환을 완벽히 지원합니다.  
- **Do I need a license?** 무료 체험판은 개발에 사용할 수 있지만, 프로덕션 사용에는 정식 라이선스가 필요합니다.  
- **Can I save to BMP or GIF instead of PNG?** 예—`PngOptions`를 `BmpOptions` 또는 `GifOptions`로 교체하면 됩니다.  
- **What Java version is required?** Java 8 이상을 권장합니다.

## “convert tiff to png”란 무엇인가요?
TIFF를 PNG로 변환한다는 것은 멀티 페이지 TIFF를 디코딩하고 각 프레임에 접근한 뒤, 해당 프레임을 손실이 없고 웹 친화적이며 널리 지원되는 PNG 형식으로 인코딩하는 과정을 말합니다.

## 왜 Aspose.Imaging for Java를 사용하나요?
- **Broad format support** – TIFF, PNG, JPEG, BMP, GIF 등 다양한 형식을 처리합니다.  
- **No native dependencies** – 순수 Java 기반으로 모든 JVM 프로젝트에 쉽게 통합할 수 있습니다.  
- **High performance** – 대용량 이미지와 멀티 페이지 문서에 최적화되어 있습니다.  
- **Simple API** – 복잡한 변환을 수행하기 위해 필요한 코드는 최소 수준입니다.

## 왜 이것이 중요한가요
많은 레거시 시스템이 보관 친화적인 형식인 멀티 페이지 TIFF로 스캔 문서를 저장합니다. 그러나 최신 웹 및 모바일 애플리케이션은 빠른 렌더링과 썸네일 생성을 위해 PNG, BMP 또는 GIF를 선호합니다. TIFF 프레임을 실시간으로 변환하면 저장 비용을 절감하고 로드 시간을 단축하며 브라우저와 디바이스 간 호환성을 확대할 수 있습니다.

## 사전 요구 사항

1. **Java Development Environment** – JDK가 설치되어 있는지 확인하십시오. 아직 설치하지 않았다면 [Oracle website](https://www.oracle.com/java/technologies/javase-downloads)에서 다운로드하세요.  
2. **Aspose.Imaging for Java Library** – API 레퍼런스는 [documentation](https://reference.aspose.com/imaging/java/)에서 확인할 수 있습니다. 라이브러리는 [download page](https://releases.aspose.com/imaging/java/)에서 얻을 수 있습니다. 무료 체험판은 [here](https://releases.aspose.com/)에서 제공되며, 정식 라이선스는 [here](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.  
3. **Sample TIFF Image** – 처리할 멀티 페이지 TIFF 파일을 준비하십시오.

이제 사전 요구 사항이 충족되었으니, 코드로 들어가 보겠습니다.

## Aspose.Imaging for Java를 사용하여 TIFF를 PNG로 변환하는 방법

### 패키지 가져오기
먼저 필요한 Aspose.Imaging 클래스를 가져옵니다.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

### 단계 1: TIFF 이미지 로드
데이터 디렉터리를 초기화하고 소스 TIFF 파일을 로드합니다.

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

### 단계 2: 다양한 래스터 형식으로 프레임 저장
각 프레임을 순회하면서 **save image as png**합니다. **convert tiff to bmp** 또는 **tiff to gif conversion**을 수행하려면 `PngOptions`를 `BmpOptions` 또는 `GifOptions`로 교체하면 됩니다.

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **Pro tip:** `try‑with‑resources` 블록을 그대로 유지하면 TIFF 파일이 처리 후 적절히 해제됩니다.

## 일반적인 사용 사례
- **Document archiving:** 스캔한 TIFF 문서를 웹 미리보기를 위해 PNG로 변환합니다.  
- **Thumbnail generation:** TIFF의 첫 번째 프레임을 추출하여 작은 PNG 썸네일로 저장합니다.  
- **Format migration:** 레거시 TIFF 자산을 BMP 또는 GIF와 같은 최신 형식으로 이동시켜 오래된 시스템과의 호환성을 확보합니다.

## 문제 해결 및 팁
- **Missing frames:** 소스 TIFF에 실제로 여러 페이지가 포함되어 있는지 확인하고, `multiImage.getFrames().size()`를 사용해 디버그합니다.  
- **Out‑of‑memory errors:** 전체 파일을 메모리에 로드하는 대신, 예시와 같이 페이지별로 처리하여 메모리 사용량을 최소화합니다.  
- **Quality control:** PNG는 무손실이므로 파일 크기를 줄이려면 품질 설정이 가능한 JPEG 옵션을 고려하십시오.

## 자주 묻는 질문

**Q1: What are the supported raster formats for frame saving in Aspose.Imaging for Java?**  
A1: Aspose.Imaging for Java는 PNG, JPEG, BMP, GIF 등 다양한 래스터 형식을 지원합니다. 애플리케이션 요구에 맞는 형식을 선택하면 됩니다.

**Q2: Can I perform other image operations using Aspose.Imaging for Java?**  
A2: 예, Aspose.Imaging for Java는 이미지 리사이징, 크롭, 다양한 필터 및 효과 적용 등 포괄적인 이미지 처리 기능을 제공합니다. 모든 이미지 처리 요구에 활용할 수 있는 다목적 도구입니다.

**Q3: How can I obtain a full license for Aspose.Imaging for Java?**  
A: 정식 라이선스를 구매하려면 [purchase page](https://purchase.aspose.com/buy)를 방문하십시오. 프로젝트에 맞는 다양한 라이선스 옵션을 확인할 수 있습니다.

**Q4: Is there a free trial available for Aspose.Imaging for Java?**  
A: 예, [releases page](https://releases.aspose.com/)에서 Aspose.Imaging for Java의 무료 체험판을 이용할 수 있습니다. 구매 전에 라이브러리 기능을 충분히 평가해 보세요.

**Q5: Where can I seek support or get assistance with Aspose.Imaging for Java?**  
A: 질문이나 문제가 있으면 [Aspose Imaging forum](https://forum.aspose.com/)을 방문하십시오. 커뮤니티와 지원 팀이 도움을 드립니다.

---

**마지막 업데이트:** 2026-04-28  
**테스트 대상:** Aspose.Imaging for Java 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}