---
date: 2026-01-12
description: DICOM 이미지에서 대비를 조정하는 방법을 배우세요 – Aspose.Imaging for Java를 사용한 대비 조정 단계별
  가이드 및 DICOM을 BMP로 변환하는 방법.
linktitle: DICOM Image Contrast Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java를 사용하여 DICOM 이미지의 대비 조정 방법
url: /ko/java/image-processing-and-enhancement/dicom-image-contrast-adjustment/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java를 사용한 DICOM 이미지 대비 조정 방법

현대 의료 영상에서 **대비 조정 방법**은 명확한 진단과 놓친 세부 사항 사이의 차이를 만들 수 있습니다. 이 튜토리얼에서는 Aspose.Imaging for Java를 사용하여 DICOM 파일의 대비를 조정하는 정확한 단계들을 안내하고, 해당 DICOM 이미지를 BMP로 변환하여 쉽게 보기 또는 추가 처리할 수 있는 방법을 보여줍니다. 끝까지 진행하면 모든 Java 프로젝트에 바로 삽입할 수 있는 사용 준비가 된 코드 스니펫을 얻게 됩니다.

## 빠른 답변
- **대비 조정은 무엇을 하나요?** 어두운 픽셀과 밝은 픽셀 사이의 범위를 확장하여 구조가 돋보이게 합니다.
- **필요한 라이브러리는?** Aspose.Imaging for Java.
- **BMP로 출력할 수 있나요?** 예 – 대비를 조정한 후 DICOM을 BMP로 변환할 수 있습니다.
- **프로덕션에 라이선스가 필요합니까?** 평가용이 아닌 사용을 위해서는 상업용 라이선스가 필요합니다.
- **지원되는 Java 버전은?** Java 8 및 그 이후 버전.

## 대비 조정이란 무엇이며 왜 중요한가?
대비 조정은 해부학적 특징 간의 시각적 구분을 강화하여 방사선 전문의가 이상을 더 빠르게 발견하도록 돕습니다. DICOM 워크플로우에서 변환 전에 대비를 조정하면 BMP 출력이 보고서 작성이나 보관에 필요한 진단 품질을 유지합니다.

## 사전 요구 사항

코드에 들어가기 전에 다음이 준비되어 있는지 확인하십시오:

1. **Aspose.Imaging for Java** – 공식 사이트에서 [here](https://releases.aspose.com/imaging/java/)를 통해 다운로드하십시오.  
2. **Java Development Environment** – JDK 8 이상 및 선호하는 IDE(IntelliJ, Eclipse, VS Code 등).  
3. **DICOM 이미지** – 향상시키고 싶은 .dcm 파일이면 언제든지; 샘플 파일은 온라인에서 구할 수 있거나 자체 임상 데이터를 사용할 수 있습니다.

## 패키지 가져오기

다음 import 구문을 통해 DICOM 처리 및 BMP 저장 기능을 사용할 수 있습니다.

```java
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
```

## DICOM 이미지에서 대비 조정 방법

아래는 전체 단계별 워크플로우입니다. 각 단계는 쉬운 언어로 설명되어 있어 Aspose.Imaging에 익숙하지 않아도 따라 할 수 있습니다.

### 단계 1: 파일 경로 지정

입력 DICOM 위치와 원하는 출력 BMP 경로를 설정합니다. 자리표시자를 실제 머신의 디렉터리 경로로 교체하십시오.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingContrast_out.bmp";
```

### 단계 2: DICOM 이미지 로드

`FileInputStream`을 사용하여 DICOM 파일을 엽니다. `try‑with‑resources` 블록은 스트림을 자동으로 닫아줍니다.

```java
File file = new File(inputFile);

try (FileInputStream fis = new FileInputStream(file)) {
    try (DicomImage image = (DicomImage) Image.load(fis)) {
        // All further processing happens inside this block
    }
} catch (IOException ex) {
    Logger.println(ex.getMessage());
    ex.printStackTrace();
}
```

### 단계 3: 대비 조정

내부 `try` 블록 안에서 `adjustContrast`를 호출합니다. 값은 **‑100**(감소)부터 **+100**(증가)까지 가능합니다. 이 예제에서는 대비를 50 단위 상승시킵니다.

```java
image.adjustContrast(50);
```

### 단계 4: DICOM을 BMP로 변환하고 이미지 저장

대비를 조정한 후 `BmpOptions` 인스턴스를 생성하고 결과를 BMP 파일로 저장합니다. 이 단계는 **DICOM을 BMP로 변환**하여 널리 지원되는 래스터 형식을 제공합니다.

```java
image.save(outputFile, new BmpOptions());
```

## 일반적인 문제 및 팁
- **잘못된 DICOM 파일** – .dcm 파일이 지원되지 않는 전송 구문으로 압축되지 않았는지 확인하십시오. Aspose.Imaging은 대부분의 표준 DICOM 인코딩을 지원합니다.
- **대비 값 범위 초과** – ±100을 초과하는 값은 제한됩니다; 이미지 히스토그램에 맞는 값을 선택하십시오.
- **메모리 사용량** – 대용량 DICOM 시리즈는 많은 RAM을 소모할 수 있습니다. `OutOfMemoryError`가 발생하면 한 번에 한 슬라이스씩 처리하십시오.

## 결론

이제 Aspose.Imaging for Java를 사용하여 DICOM 이미지에서 **대비를 조정하는 방법**과 **DICOM을 BMP로 변환하는 방법**을 배웠습니다. 이 워크플로우는 빠르고 신뢰할 수 있으며, PACS 뷰어, 연구 도구 또는 자동 보고 시스템을 구축하든 큰 의료 이미지 파이프라인에 통합할 수 있습니다.

Aspose.Imaging for Java는 저수준 DICOM 처리를 추상화하여 이미지의 임상적 가치에 집중할 수 있게 합니다.

## 자주 묻는 질문

**Q: DICOM이 무엇이며 왜 의료 영상의 표준인가요?**  
A: DICOM(Digital Imaging and Communications in Medicine)은 의료 이미지를 저장, 전송 및 공유하기 위한 범용 포맷으로, 장치와 기관 간의 상호 운용성을 보장합니다.

**Q: 밝기와 대비를 동시에 조정할 수 있나요?**  
A: 예, `adjustBrightness(int value)` 메서도 유사하게 작동하며 저장 전에 체인 형태로 사용할 수 있습니다.

**Q: Aspose.Imaging이 BMP 외에 다른 출력 포맷을 지원하나요?**  
A: 물론입니다 – 해당 `*Options` 클래스를 사용하여 PNG, JPEG, TIFF 등 다양한 포맷으로 내보낼 수 있습니다.

**Q: 프로덕션 사용에 상업용 라이선스가 필요합니까?**  
A: 예. 라이선스는 [here](https://purchase.aspose.com/buy)에서 구매하거나 임시 평가 라이선스는 [here](https://purchase.aspose.com/temporary-license/)에서 얻을 수 있습니다.

**Q: 더 많은 도움과 예제를 어디서 찾을 수 있나요?**  
A: Aspose.Imaging for Java 커뮤니티 포럼에서 풍부한 문서와 샘플 코드를 제공합니다: [Aspose.Imaging for Java forum](https://forum.aspose.com/).

---

**마지막 업데이트:** 2026-01-12  
**테스트 환경:** Aspose.Imaging for Java 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}