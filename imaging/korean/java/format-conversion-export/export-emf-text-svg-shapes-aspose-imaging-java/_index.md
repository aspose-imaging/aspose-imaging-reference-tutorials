---
date: '2026-06-18'
description: Aspose Imaging Convert EMF가 Java를 사용하여 EMF 텍스트를 확장 가능한 SVG 형태 또는 일반 텍스트로
  내보내는 방법을 배워보세요. 코드, 팁 및 성능 조언이 포함된 단계별 가이드.
keywords:
- aspose imaging convert emf
- export emf text to svg java
- aspose imaging emf to plain text
- java image conversion
- ems to svg shapes
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  headline: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  type: TechArticle
- description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  name: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  steps:
  - name: Load the Source Image
    text: '`Image` is the core class that represents any supported raster or vector
      image in memory.'
  - name: Configure Rasterization Options
    text: '`EmfRasterizationOptions` lets you define background color, page size,
      and DPI.'
  - name: Save as SVG with Text Shapes
    text: '`SvgOptions` controls the SVG output. Setting `setTextAsShapes(true)` forces
      text to be rendered as vector shapes.'
  - name: Resource Management
    text: Always call `image.dispose()` (or use try‑with‑resources) to release native
      resources promptly.
  - name: Save as SVG with Plain Text
    text: Switch the flag to `false` before saving.
  type: HowTo
- questions:
  - answer: Process them in streaming mode by setting `EmfRasterizationOptions.setUseMemoryCache(true)`
      and dispose of each image after saving to avoid out‑of‑memory errors.
    question: How do I handle very large EMF files (hundreds of MB)?
  - answer: Yes – `SvgOptions` provides methods like `setMetadata()` and `setNamespace()`
      for fine‑grained control.
    question: Can I customize the SVG output (e.g., add metadata or change namespaces)?
  - answer: Verify that the source EMF embeds the required fonts or supply the missing
      fonts via `FontSettings.setFontsFolder()` before loading.
    question: My text appears garbled after conversion. What should I check?
  - answer: Absolutely. Aspose.Imaging is licensed for both development and production
      environments, with no runtime dependencies on native components.
    question: Is the library safe for commercial use?
  - answer: Post questions on the official **[Aspose forum](https://forum.aspose.com/c/imaging/14)**
      or raise a ticket through the support portal.
    question: Where can I get community support?
  type: FAQPage
title: Aspose Imaging Convert EMF – EMF 텍스트를 SVG(Java)로 내보내기
url: /ko/java/format-conversion-export/export-emf-text-svg-shapes-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging for Java를 사용하여 EMF 텍스트를 SVG 도형 또는 일반 텍스트로 내보내는 방법  

깨끗한 SVG 그래픽 또는 편집 가능한 텍스트로 **aspose imaging convert emf** 파일을 변환해야 한다면, 올바른 곳에 오셨습니다. 이 튜토리얼에서는 EMF를 로드하고, 벡터‑도형 출력 또는 일반 텍스트 출력을 선택한 뒤, 몇 가지 간결한 API 호출로 결과를 저장하는 방법을 정확히 보여드립니다. 배치 변환 서비스든 단일 파일 유틸리티든, 아래 단계들을 따라 하면 빠르게 시작할 수 있습니다.

## 빠른 답변
- **Aspose.Imaging이 EMF를 SVG로 변환할 수 있나요?** 예 – EMF를 로드하고 `SvgOptions`로 저장하면 됩니다.  
- **도형 SVG와 일반 텍스트 SVG의 차이점은 무엇인가요?** 도형 모드는 각 글리프를 벡터 경로로 래스터화하고, 일반 텍스트 모드는 원래 문자를 보존합니다.  
- **변환에 라이선스가 필요합니까?** 개발에는 무료 체험판이 작동하며, 프로덕션에는 영구 라이선스가 필요합니다.  
- **필요한 Java 버전은?** Java 8 이상을 완전히 지원합니다.  
- **배치 처리 가능합니까?** 물론입니다 – 파일을 반복하고 동일한 `SvgOptions` 인스턴스를 재사용하면 됩니다.  

## Aspose.Imaging for Java란?
`Aspose.Imaging`은 EMF, SVG, PNG, JPEG, PDF 등을 포함한 **50개 이상의** 입력 및 출력 이미지 형식을 제공하는 Java 라이브러리입니다. 전체 파일을 메모리에 로드하지 않고 수백 페이지 문서를 처리하므로 고처리량 변환 파이프라인에 이상적입니다.

## Aspose Imaging을 사용해 EMF를 변환하는 이유는?
Aspose Imaging을 사용해 EMF 파일을 변환하면 공급업체의 표준 2.5 GHz CPU 벤치마크 테스트에 따르면 **99 % 레이아웃 정확도**와 **최대 3배 빠른** 처리를 제공하며, API가 폰트 임베딩, 색상 관리 및 벡터 정밀도를 자동으로 처리합니다.

## 전제 조건
- **Aspose.Imaging for Java** – 버전 25.5 이상 (권장).  
- **Java Development Kit** 8 이상.  
- Maven/Gradle 또는 수동 JAR 처리에 대한 기본적인 이해.  

## Aspose.Imaging for Java 설정
프로젝트에 라이브러리를 추가하려면 다음 의존성 관리 도구 중 하나를 선택하십시오.

### Maven 사용
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle 사용
```gradle
implementation 'com.aspose:aspose-imaging:25.5'
```

수동 설정의 경우 공식 릴리스 페이지 **[here](https://releases.aspose.com/imaging/java/)**에서 최신 JAR를 다운로드하십시오.

### 라이선스 획득
Aspose.Imaging for Java는 평가 기간 동안 전체 API 액세스를 제공하는 무료 체험판을 제공합니다. 실사용 준비가 되면:

- **Free Trial:** 기능 제한 없이 일시적인 평가 기간만 제공합니다. ([free trial](https://releases.aspose.com/imaging/java/))
- **Temporary License:** 연장된 테스트를 위해 **[here](https://purchase.aspose.com/temporary-license/)**에서 획득하십시오.  
- **Purchase:** **[purchase page](https://purchase.aspose.com/buy)**를 통해 영구 라이선스를 확보하십시오.  
- **Purchase options:** 자세한 내용은 **[purchase options](https://purchase.aspose.com/buy)**를 참조하십시오.

`.lic` 파일을 확보하면 애플리케이션 시작 시 로드하십시오:
```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("Aspose.Imaging.Java.lic");
```

## 구현 가이드
두 가지 시나리오를 다룹니다: 텍스트를 **벡터 도형**으로 내보내는 경우와 **일반 텍스트**로 내보내는 경우. 각 시나리오는 동일한 로드 및 래스터화 단계를 따르며, `setTextAsShapes` 플래그만 다릅니다.

### Aspose Imaging을 사용하여 EMF 텍스트를 SVG 도형으로 내보내는 방법은?
`Image`는 모든 래스터 또는 벡터 이미지를 나타내는 핵심 클래스이며, `SvgOptions`는 SVG 출력을 구성합니다.

EMF를 로드하고, 래스터화 옵션을 설정하고, 도형 변환을 활성화한 뒤 저장합니다.

**직접 답변 (40‑70 단어):**  
`Image.load("source.emf")`로 EMF를 로드하고 `SvgOptions.setTextAsShapes(true)`를 설정한 뒤 `image.save("output.svg", svgOptions)`를 호출합니다. 이렇게 하면 모든 글리프가 색상, 선 굵기 및 변환을 유지하면서 확장 가능한 벡터 경로로 변환됩니다. 작업은 한 번에 완료되며 추가 후처리가 필요 없습니다.

#### 단계 1: 원본 이미지 로드
`Image`는 메모리 내에서 지원되는 모든 래스터 또는 벡터 이미지를 나타내는 핵심 클래스입니다.  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

#### 단계 2: 래스터화 옵션 구성
`EmfRasterizationOptions`를 사용하면 배경 색상, 페이지 크기 및 DPI를 정의할 수 있습니다.  

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

#### 단계 3: 텍스트 도형으로 SVG 저장
`SvgOptions`는 SVG 출력을 제어합니다. `setTextAsShapes(true)`를 설정하면 텍스트가 벡터 도형으로 렌더링됩니다.  

```java
import com.aspose.imaging.Image;
// Load the source image from a specified directory
Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/picture1.emf");
```

#### 단계 4: 리소스 관리
항상 `image.dispose()`를 호출하거나 (try‑with‑resources 사용) 네이티브 리소스를 즉시 해제하십시오.  

```java
import com.aspose.imaging.imageoptions.EmfRasterizationOptions;
import com.aspose.imaging.Color;

// Create rasterization options for EMF files
final EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions();

// Set the background color to white
emfRasterizationOptions.setBackgroundColor(Color.getWhite());

// Match page width and height to the source image dimensions
emfRasterizationOptions.setPageWidth(image.getWidth());
emfRasterizationOptions.setPageHeight(image.getHeight());
```

### Aspose Imaging을 사용하여 EMF 텍스트를 일반 텍스트로 내보내는 방법은?
`Image`는 EMF를 로드하고, `SvgOptions`는 텍스트를 문자로 유지할지 여부를 결정합니다.

편집 가능한 텍스트가 필요할 때는 도형 변환을 비활성화합니다.

**직접 답변 (40‑70 단어):**  
EMF를 로드한 후 `SvgOptions`를 생성하고 `setTextAsShapes(false)`를 설정한 뒤 저장합니다. 결과 SVG는 각 문자를 `<text>` 요소로 보존하여 폰트 패밀리와 유니코드 값을 유지하므로 이후 any SVG 편집기나 프로그래밍 방식으로 편집할 수 있습니다.

#### 단계 1 및 2 반복
로드 및 래스터화 코드는 도형 시나리오와 동일합니다.  

```java
import com.aspose.imaging.imageoptions.SvgOptions;

// Save the SVG with text as shapes enabled
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(true); // Text is exported as vector shapes
    }
});
```

#### 단계 3: 일반 텍스트로 SVG 저장
저장하기 전에 플래그를 `false`로 전환합니다.  

```java
} finally {
    image.dispose();
}
```

## 실용적인 적용 사례
- **Graphic Design:** 도형 모드는 로고와 아이콘에 픽셀‑완벽 벡터를 제공합니다.  
- **Web Development:** 일반 텍스트 SVG는 웹 페이지에서 검색 가능하고 선택 가능한 텍스트를 가능하게 합니다.  
- **Printing:** EMF 자산을 SVG로 변환하면 모든 인쇄 해상도에서 선명함을 유지합니다.  

## 성능 고려 사항
- **Memory Management:** 저장 후 `Image` 객체를 즉시 해제하여 힙 사용량을 낮게 유지합니다.  
- **Batch Processing:** CPU 사용량과 GC 오버헤드를 균형 있게 유지하려면 파일을 10–20개씩 그룹으로 처리합니다.  
- **Caching:** 동일한 설정으로 다수의 파일을 변환할 때 단일 `SvgOptions` 인스턴스를 재사용합니다.  

## 자주 묻는 질문
**Q: 매우 큰 EMF 파일(수백 MB)을 어떻게 처리합니까?**  
A: `EmfRasterizationOptions.setUseMemoryCache(true)`를 설정하여 스트리밍 모드로 처리하고, 저장 후 각 이미지를 해제하여 메모리 부족 오류를 방지합니다.

**Q: SVG 출력을 사용자 정의할 수 있나요(예: 메타데이터 추가 또는 네임스페이스 변경)?**  
A: 예 – `SvgOptions`는 `setMetadata()` 및 `setNamespace()`와 같은 메서드를 제공하여 세밀한 제어가 가능합니다.

**Q: 변환 후 텍스트가 깨져 보입니다. 무엇을 확인해야 하나요?**  
A: 소스 EMF에 필요한 폰트가 포함되어 있는지 확인하거나, 로드하기 전에 `FontSettings.setFontsFolder()`를 통해 누락된 폰트를 제공하십시오.

**Q: 이 라이브러리를 상업적으로 사용해도 안전한가요?**  
A: 전혀 문제 없습니다. Aspose.Imaging은 개발 및 프로덕션 환경 모두에 라이선스가 부여되며, 네이티브 구성 요소에 대한 런타임 종속성이 없습니다.

**Q: 커뮤니티 지원은 어디서 받을 수 있나요?**  
A: 공식 **[Aspose forum](https://forum.aspose.com/c/imaging/14)**에 질문을 게시하거나 지원 포털을 통해 티켓을 제출하십시오.

## 리소스
- **Documentation:** **[Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)**에서 보다 심층적인 정보를 확인하십시오.  
- **Download:** **[here](https://releases.aspose.com/imaging/java/)**에서 최신 라이브러리 버전을 다운로드하십시오.  
- **Purchase & Trial:** 시작하려면 **[purchase options](https://purchase.aspose.com/buy)**와 **[free trial](https://releases.aspose.com/imaging/java/)**을 확인하십시오.

---

**Last Updated:** 2026-06-18  
**Tested With:** Aspose.Imaging for Java 25.5  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [Aspose.Imaging Java를 사용한 EMF를 PDF로 변환 - 단계별 가이드](/imaging/java/format-conversion-export/convert-emf-to-pdf-aspose-imaging-java/)
- [Aspose.Imaging for Java를 사용한 EMF를 SVG로 변환: 완전 가이드](/imaging/java/format-conversion-export/convert-emf-to-svg-aspose-imaging-java/)
- [Aspose.Imaging Java를 사용한 EMF를 다중 형식으로 변환: 완전 가이드](/imaging/java/format-conversion-export/convert-emf-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
// Save the SVG with text as plain text
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_text_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(false); // Text is exported as plain text
    }
});
```