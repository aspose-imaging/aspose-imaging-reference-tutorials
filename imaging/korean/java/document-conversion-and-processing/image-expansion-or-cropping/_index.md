---
date: 2026-05-03
description: Aspose.Imaging for Java를 사용하여 이미지 자르기, 사각형 자르기 및 캔버스 확장을 포함하는 방법을 배웁니다.
  개발자를 위한 단계별 가이드.
keywords:
- how to crop image
- crop and expand image
- aspose imaging crop
- java image processing tutorial
- expand image canvas java
linktitle: 이미지 확대 또는 자르기
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java를 사용하여 이미지를 사각형으로 자르는 방법
url: /ko/java/document-conversion-and-processing/image-expansion-or-cropping/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java를 사용하여 이미지를 사각형으로 자르는 방법

## 빠른 답변
- **Java 이미지 자르기에 가장 적합한 라이브러리는?** Aspose.Imaging for Java.  
- **임의의 사각형으로 자를 수 있나요?** 예 – X, Y, 너비, 높이를 자유롭게 정의합니다.  
- **개발에 라이선스가 필요합니까?** 테스트용 무료 체험판을 사용할 수 있으며, 프로덕션에서는 라이선스가 필요합니다.  
- **이미지 확장이 가능한가요?** 물론입니다 – 자르기 전에 캔버스 크기를 늘릴 수 있습니다.  
- **지원되는 Java 버전은?** Java 8 이상.

## “이미지를 사각형으로 자르기”란?
이미지를 사각형으로 자른다는 것은 원본 비트맵에서 직사각형 영역(X‑offset, Y‑offset, 너비, 높이)으로 정의된 부분을 추출하는 것을 의미합니다. 나머지 영역은 버려지고, 필요한 영역만 포함하는 새로운 작은 이미지가 남게 됩니다.

## 왜 Aspose.Imaging for Java를 사용해야 할까요?
- **외부 종속성 없음** – 순수 Java이며 모든 플랫폼에서 작동합니다.  
- **다양한 포맷 지원** – JPEG, PNG, BMP, TIFF 등.  
- **고성능 캐싱** – `cacheData()`가 I/O 오버헤드를 감소시킵니다.  
- **간단한 API** – 로드, 사각형 정의, 저장을 한 줄 호출로 수행합니다.

## 사전 요구 사항
- **Java 개발 환경** – JDK 8 이상이 설치되고 구성되어 있어야 합니다.  
- **Aspose.Imaging for Java** – [website](https://releases.aspose.com/imaging/java/)에서 다운로드합니다.  
- **기본 Java 지식** – 클래스, try‑with‑resources, 파일 경로에 익숙해야 합니다.  
- **작업할 이미지** – 자르거나 확장하고 싶은 JPEG/PNG 파일.

## 패키지 가져오기
First, point the code to the folder that holds your source images. This snippet stays unchanged from the original tutorial.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

`"Your Document Directory"`를 머신의 절대 경로로 교체합니다.

## 단계 1: 이미지 로드
Loading the image is the foundation for any manipulation. We also call `cacheData()` to keep the bitmap in memory for fast subsequent operations.

```java
try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
{
    rasterImage.cacheData();
}
```

> **Pro tip:** Use a `try‑with‑resources` block (as shown) to ensure the image is automatically closed, preventing memory leaks.

## 단계 2: 자르기 영역 정의
Here we create a `Rectangle` that represents the exact area you want to keep. The rectangle can start outside the original bounds – Aspose.Imaging will automatically expand the canvas (useful for the **expand image canvas java** scenario).

```java
// Create an instance of Rectangle class and define X, Y, Width, and Height of the rectangle
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

- **X / Y** – 음수 값은 사각형을 왼쪽/위쪽으로 이동시켜 캔버스를 확장합니다.  
- **Width / Height** – 잘라낼 영역의 크기.

## 단계 3: 잘라낸(또는 확장된) 이미지 저장
Finally, write the result to disk. The `save` method takes the destination path, image format options, and the rectangle we defined.

```java
rasterImage.save("Your Document Directory" + "Grayscaling_out.jpg", new JpegOptions(), destRect);
```

The output file `Grayscaling_out.jpg` now contains the **crop image to rectangle** result. If the rectangle extended beyond the original image, the extra area is filled with a default background (transparent for PNG, black for JPEG).

## Aspose.Imaging for Java로 이미지 자르기
This section reiterates the core steps in a concise checklist so you can quickly reference them while coding:

1. **데이터 디렉터리 설정** – 소스 이미지가 있는 폴더를 지정합니다.  
2. `Image.load()`로 이미지를 로드하고 `cacheData()`를 호출합니다.  
3. **`Rectangle`**을 생성하여 자르기 영역(또는 캔버스 확장)을 정의합니다.  
4. `rasterImage.save()`를 사용해 새 이미지를 저장하고 사각형을 전달합니다.

## 이미지 자르기 및 확장 – 실제 사용 사례
| 시나리오 | 중요 이유 |
|----------|------------|
| **썸네일 생성** | 일관된 크기를 위해 중앙 영역을 빠르게 추출합니다. |
| **사용자 프로필 사진 자르기** | 정사각형 또는 직사각형 아바타 영역을 강제합니다. |
| **워터마크 추가 전 캔버스 확장** | 원본을 왜곡하지 않고 이미지 주변에 여백을 추가합니다. |
| **스캔 문서 일괄 처리** | 한 번에 여백을 잘라냅니다. |

## 문제 해결 및 팁
- **이미지가 로드되지 않나요?** 파일 경로를 확인하고 이미지 포맷이 지원되는지 확인합니다.  
- **확장 후 예상치 못한 검은 테두리?** `JpegOptions`에서 배경 색을 설정하거나 투명도를 위해 PNG를 사용합니다.  
- **대용량 이미지의 성능 문제?** Java 힙 크기(`-Xmx`)를 늘리거나 작은 배치로 이미지를 처리합니다.  
- **흔한 실수:** `cacheData()` 호출을 잊으면 이후 작업에서 I/O가 느려질 수 있습니다.

## 자주 묻는 질문

**Q: Aspose.Imaging for Java가 지원하는 이미지 포맷은 무엇인가요?**  
A: JPEG, PNG, BMP, TIFF, GIF, ICO, PSD 등 다수. 전체 목록은 공식 문서를 참고하세요.

**Q: Aspose.Imaging for Java로 다른 이미지 조작도 할 수 있나요?**  
A: 물론입니다! 리사이징, 회전, 필터링, 포맷 변환 등 모든 기능을 제공합니다.

**Q: Aspose.Imaging for Java가 웹 애플리케이션에 적합한가요?**  
A: 네. 라이브러리는 스레드‑안전하며 서블릿 컨테이너와 Spring Boot 서비스에서 잘 동작합니다.

**Q: Aspose.Imaging for Java 지원을 어떻게 받을 수 있나요?**  
A: 커뮤니티 도움을 위해 [forum](https://forum.aspose.com/)을 방문하거나 유효한 라이선스로 지원 티켓을 열 수 있습니다.

**Q: Aspose.Imaging for Java의 무료 체험판이 있나요?**  
A: 예, 무료 체험판으로 라이브러리를 탐색할 수 있습니다. [here](https://releases.aspose.com/)에서 다운로드하세요.

## 결론
You’ve now learned **how to crop image** to a rectangle and even **expand image canvas** using the powerful Aspose.Imaging API. By mastering these fundamentals you can build robust image‑processing pipelines, improve UI responsiveness, and deliver polished visual content across any Java application.

---

**Last Updated:** 2026-05-03  
**Tested With:** Aspose.Imaging for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}