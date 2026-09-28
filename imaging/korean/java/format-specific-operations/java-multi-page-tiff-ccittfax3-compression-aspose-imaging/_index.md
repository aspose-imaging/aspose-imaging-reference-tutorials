---
date: '2026-09-28'
description: Aspose.Imaging을 사용하여 ccittfax3 compression java로 멀티 페이지 TIFF 파일을 만드는
  방법을 배웁니다. 문서 워크플로우에서 효율적으로 스캔하고, 보관하며, 파일 크기를 줄입니다.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Aspose.Imaging과 함께 ccittfax3 compression java를 사용하여 스캔 및 보관을 위한 효율적인
  멀티 페이지 TIFF 파일을 만드는 단계별 방법을 확인하세요.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: ccittfax3 compression java를 사용하여 멀티 페이지 TIFF를 만드는 방법
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: ccittfax3 compression java를 사용하여 멀티 페이지 TIFF를 만드는 방법
url: /ko/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging을 사용한 ccittfax3 압축 Java로 다중 페이지 TIFF 만들기 마스터하기

## 소개

대용량 스캔 문서를 보관하면서 파일 크기를 최소화해야 한다면 **ccittfax3 compression java**가 최적의 솔루션입니다. 이 튜토리얼에서는 Aspose.Imaging을 사용하여 Java에서 CCITTFAX3 압축으로 다중 페이지 TIFF 파일을 생성하는 방법을 보여줍니다. 이 압축이 흑백 스캔에 왜 효과적인지, 라이브러리를 어떻게 구성하는지, 각 페이지를 프레임으로 추가하는 방법을 배울 수 있습니다.

**배우게 될 내용**
- Java 프로젝트에 Aspose.Imaging을 추가하는 방법.
- `TiffOptions`를 CCITTFAX3 압축에 맞게 구성하는 방법.
- `TiffImage`를 생성하고, 원본 이미지를 크기 조정한 뒤 프레임으로 추가하는 방법.
- 최종 다중 페이지 TIFF를 효율적으로 저장하는 방법.

전체 구현 과정을 살펴보겠습니다.

## 빠른 답변
- **CCITTFAX3 압축의 주요 이점은 무엇인가요?** 흑백 스캔에서 파일 크기를 최대 80 %까지 감소시킵니다.  
- **어떤 라이브러리가 기본 지원을 제공하나요?** Java용 Aspose.Imaging, 버전 25.5+.  
- **개발에 라이선스가 필요합니까?** 무료 체험 라이선스로 모든 기능을 사용할 수 있으며, 프로덕션에서는 유료 라이선스가 필요합니다.  
- **수백 페이지를 처리할 수 있나요?** 예—Aspose.Imaging은 페이지를 스트리밍 처리하므로 메모리 사용량이 낮게 유지됩니다.  
- **코드가 Java 11 이상과 호환되나요?** 물론입니다; API는 Java 8+을 대상으로 합니다.

## ccittfax3 압축 Java란?
`CCITTFAX3`는 팩스 및 스캔 문서 이미지를 위해 설계된 무손실 흑백 압축 알고리즘입니다. 각 픽셀을 1비트로 인코딩하여 고품질 출력을 제공하면서 파일 크기를 크게 줄입니다—압축되지 않은 TIFF에 비해 보통 70‑80 % 정도 감소합니다. 이는 정확도가 유지되어야 하는 흑백 문서 보관에 이상적입니다.

## 이 작업에 Aspose.Imaging을 사용하는 이유
Aspose.Imaging은 PDF, PNG, JPEG, TIFF 등 **100개 이상의** 입력·출력 포맷을 지원합니다. 스트리밍 아키텍처 덕분에 **수백 페이지** TIFF 파일을 전체 문서를 메모리에 로드하지 않고도 처리할 수 있어 대규모 보관 프로젝트에 최적입니다.

## 전제 조건

- **Java Development Kit (JDK)** 8 이상이 설치되어 있음.
- IntelliJ IDEA 또는 Eclipse와 같은 **IDE**.
- 의존성 관리를 위한 **Maven** 또는 **Gradle**.
- 기본 Java 지식(클래스, 객체, 컬렉션).

## Java용 Aspose.Imaging 설정

빌드 파일에 라이브러리를 추가합니다.

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```  

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

### 직접 다운로드

최신 JAR 파일은 [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/)에서 다운로드할 수 있습니다.

### 라이선스 획득

무료 체험 라이선스는 [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/)에서 제공됩니다. 프로덕션 사용을 위해서는 영구 라이선스를 구매하거나 [Aspose Purchase](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 요청하십시오.

자세한 API 사용법은 Aspose.Imaging for Java [documentation](https://reference.aspose.com/imaging/java/)을 참고하십시오.

### 기본 초기화

종속성을 추가한 후 아래와 같이 라이브러리를 초기화합니다.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## 다중 페이지 TIFF를 위한 ccittfax3 압축 Java 구성 방법

`TiffOptions`는 TIFF 파일의 출력 포맷과 압축 설정을 정의하는 클래스입니다. `CCITTGroup3FaxCompression` 열거형을 사용해 `TiffOptions` 객체를 로드한 뒤 출력 파일 소스를 설정합니다. 이 두 단계 구성은 흑백 압축을 위한 작성자를 준비하고, 이후 추가되는 모든 페이지가 CCITTFAX3 알고리즘으로 인코딩되어 이미지 품질을 유지하면서 크기를 크게 줄입니다.

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## Java에서 TiffImage 인스턴스 생성 방법

`TiffImage`는 메모리 내에서 다중 페이지 TIFF 문서를 나타내며 프레임을 조작하는 메서드를 제공합니다. 먼저 모든 페이지가 공유할 너비와 높이를 정의합니다. 그런 다음 앞서 만든 `TiffOptions`를 사용해 `TiffImage`를 인스턴스화합니다. `TiffImage` 객체는 개별 프레임을 담는 컨테이너 역할을 하여 최종 파일을 저장하기 전에 페이지를 추가·제거·재정렬할 수 있게 해줍니다.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## 폴더에서 원본 이미지를 로드하고 크기 조정하는 방법

대상 디렉터리에서 JPEG 파일을 필터링하고 각 이미지를 읽어 TIFF 캔버스에 맞게 크기 조정합니다. 프레임을 추가하기 전에 크기 조정하면 메모리 사용량이 감소하고 저장 작업이 빨라집니다. 각 원본 이미지를 필요한 차원과 픽셀 형식으로 변환함으로써 페이지 레이아웃을 일관되게 유지하고 프레임을 TIFF 문서에 추가할 때 런타임 오류를 방지합니다.

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## 각 이미지를 프레임으로 다중 페이지 TIFF에 추가하는 방법

`TiffFrame`은 TIFF 내에서 단일 페이지 이미지와 해당 메타데이터를 보관하는 객체입니다. 크기 조정된 이미지들을 순회하면서 새 `TiffFrame`을 생성하고 이를 `TiffImage`에 추가합니다. 각 프레임은 최종 문서의 별도 페이지가 되며, 라이브러리는 페이지 수와 오프셋 같은 메타데이터 업데이트를 자동으로 처리해 유효한 다중 페이지 TIFF 구조를 보장합니다.

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## 최종 다중 페이지 TIFF 파일 저장 방법

`TiffImage` 인스턴스에서 `save` 메서드를 호출하고 원하는 출력 경로를 전달합니다. 라이브러리는 CCITTFAX3 압축을 사용해 모든 프레임을 자동으로 기록하고 데이터를 효율적으로 디스크에 스트리밍하며, 사용된 리소스를 모두 닫습니다. 저장이 완료되면 결과 파일에는 지정된 압축이 적용된 모든 페이지가 포함되어 배포 또는 보관에 바로 사용할 수 있습니다.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## 실제 적용 사례

- **문서 보관:** 스캔한 계약서, 청구서 또는 법적 기록을 최소한의 저장 공간으로 보관.
- **의료 영상:** 진단 세부 정보를 유지하면서 방사선 스캔을 압축.
- **인쇄 생산:** 프린터가 직접 처리할 수 있는 다중 페이지 인쇄 작업 생성.

## 성능 고려 사항

- `ResizeOptions`를 사용하여 종횡비를 유지하고 왜곡을 방지하십시오.
- 프레임을 추가한 후 각 `Image` 객체를 닫아 네이티브 메모리를 해제하십시오.
- 대용량 배치의 경우 파일을 병렬 스트림으로 처리하고 각 TIFF 세그먼트를 비동기적으로 기록하십시오.

## 일반적인 함정 및 문제 해결

- **잘못된 픽셀 형식:** CCITTFAX3은 1비트(흑백) 이미지에서만 작동합니다. 색상 이미지를 크기 조정 전에 그레이스케일로 변환하십시오.
- **메모리 누수:** 임시 `Image` 객체에 항상 `dispose()`를 호출하십시오; 그렇지 않으면 네이티브 버퍼가 할당된 상태로 남습니다.
- **파일 크기가 감소하지 않음:** `TiffOptions` 압축 속성이 설정되어 있는지 확인하십시오; 그렇지 않으면 기본값(압축 없음)이 사용됩니다.

## 자주 묻는 질문

**Q: 이 방법을 컬러 이미지에 사용할 수 있나요?**  
A: CCITTFAX3은 단색 데이터에만 제한됩니다; 컬러의 경우 JPEG 또는 LZW 압축을 사용하십시오.

**Q: Aspose.Imaging은 대용량 TIFF에 대한 스트리밍을 지원하나요?**  
A: 예—라이브러리는 각 프레임을 직접 출력 스트림에 기록하므로 수천 페이지에서도 메모리 사용량이 낮게 유지됩니다.

**Q: 프로그래밍 방식으로 임시 라이선스를 적용하려면 어떻게 해야 하나요?**  
A: `.lic` 파일을 `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`와 같이 로드합니다.

**Q: 저장하기 전에 TIFF를 미리 볼 수 있는 방법이 있나요?**  
A: 각 `TiffFrame`을 `BufferedImage`로 렌더링한 뒤 Swing 컴포넌트에 표시할 수 있습니다.

**Q: 공식적으로 지원되는 Java 버전은 어떤 것인가요?**  
A: Aspose.Imaging은 Java 8부터 Java 21까지, LTS 릴리스를 포함해 지원합니다.

## 결론

이제 Aspose.Imaging을 사용해 **ccittfax3 compression java**로 다중 페이지 TIFF 파일을 생성하는 완전하고 프로덕션 준비된 워크플로우를 갖추었습니다. 위 단계들을 따르면 대용량 문서 컬렉션을 효율적으로 보관하면서 저장 비용을 낮추고 이미지 품질을 높게 유지할 수 있습니다. OCR, 메타데이터 처리, 포맷 변환 등 추가 Aspose.Imaging 기능을 탐색하여 문서 처리 파이프라인을 더욱 강화해 보세요.

---

**마지막 업데이트:** 2026-09-28  
**테스트 대상:** Aspose.Imaging 25.5 for Java  
**작성자:** Aspose

## 관련 튜토리얼

- [Aspose.Imaging for Java를 사용한 다중 페이지 TIFF 생성 방법 – 완전 가이드](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Java에서 LZW 압축으로 이미지 파일 크기 줄이기](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Aspose.Imaging for Java로 다중 페이지 TIFF 프레임 분할](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}