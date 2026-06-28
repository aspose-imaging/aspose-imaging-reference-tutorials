---
date: '2026-06-28'
description: Aspose.Imaging for Java를 사용하여 ODP를 PNG로 변환하는 방법을 배우고, custom fonts를 설정하며
  정확한 렌더링을 위해 system fonts를 비활성화하는 방법을 알아보세요.
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: Aspose.Imaging for Java를 사용하여 ODP를 PNG로 변환하는 방법 – custom fonts & Export Guide
url: /ko/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# ODP를 PNG로 변환하는 방법 – Aspose.Imaging for Java 사용, 사용자 정의 폰트 및 내보내기 가이드

현대 Java 애플리케이션에서는 OpenDocument Presentation (ODP) 파일을 고품질 PNG 이미지로 변환하는 것이 일반적인 요구 사항이며, 특히 사용자 정의 폰트를 통해 브랜드를 유지해야 할 때 중요합니다. 이 튜토리얼에서는 Aspose.Imaging for Java를 사용하여 **ODP를 PNG로 변환하는 방법**을 보여주고, 사용자 정의 폰트 폴더 설정, 시스템 대체 폰트 비활성화, 최적 성능을 위한 래스터화 옵션 미세 조정 방법을 안내합니다.

**What You’ll Learn**
- ODP 변환을 위한 사용자 정의 폰트 디렉터리를 설정하는 방법.  
- 시스템 대체 폰트를 비활성화하여 선택한 폰트만 사용하도록 하는 방법.  
- 정확한 크기와 폰트 설정으로 ODP 파일을 PNG로 내보내는 방법.  
- 대용량 프레젠테이션을 처리할 때 속도와 메모리 사용량을 개선하는 팁.

## 빠른 답변
- **Maven을 사용하여 Aspose.Imaging을 추가할 수 있나요?** 예, Maven 의존성을 추가하고 `mvn install`을 실행하십시오.  
- **프로덕션에 라이선스가 필요합니까?** 무제한 사용을 위해서는 유효한 Aspose.Imaging 라이선스가 필요합니다.  
- **내 사용자 정의 폰트가 적용되나요?** 폰트 폴더를 설정하고 시스템 대체 폰트를 비활성화하면 적용됩니다.  
- **지원되는 이미지 형식은 무엇인가요?** Aspose.Imaging은 PNG, JPEG, TIFF, WebP 등을 포함한 120개 이상의 래스터 및 벡터 형식을 지원합니다.  
- **API가 스레드 안전한가요?** 예, 대부분의 Aspose.Imaging 클래스는 스레드당 별도 인스턴스를 생성하면 동시 사용이 안전합니다.

## “how to convert odp”란 무엇인가요?
*“How to convert odp”*는 OpenDocument Presentation 파일을 다른 형식(주로 PNG)으로 변환하면서 레이아웃, 폰트 및 시각적 충실도를 유지하는 과정을 의미합니다. Aspose.Imaging for Java는 외부 도구 없이도 이 변환을 처리하는 단일 메서드 워크플로를 제공하여 개발자가 최소한의 코드로 변환을 애플리케이션에 직접 통합할 수 있게 합니다.

## 왜 Aspose.Imaging for Java를 사용해야 할까요?
Aspose.Imaging은 **120개 이상의 출력 형식**을 지원하며 전체 문서를 메모리에 로드하지 않고 다중 페이지 ODP 파일을 래스터화할 수 있어 대형 프레젠테이션에서 피크 RAM 사용량을 최대 70 %까지 감소시킵니다. 또한 라이브러리는 내장 폰트 관리 기능을 제공하여 타사 렌더링 엔진이 필요 없게 합니다.

## 사전 요구 사항
- **라이브러리**: Aspose.Imaging for Java ≥ 25.5.  
- **JDK**: 버전 8 이상.  
- **IDE**: IntelliJ IDEA, Eclipse 또는 Java 호환 편집기.  
- **기본 지식**: Java I/O, 객체 지향 프로그래밍 및 이미지 개념.

## 설치 안내

### Maven
다음 의존성을 `pom.xml`에 추가하고 `mvn clean install`을 실행하십시오:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
`build.gradle` 파일에 라이브러리를 포함하고 프로젝트를 새로 고치십시오:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### 직접 다운로드
[Aspose.Imaging for Java 릴리스](https://releases.aspose.com/imaging/java/)에서 최신 JAR를 다운로드하십시오.

## 라이선스 획득 단계
전체 기능을 사용하려면 임시 또는 영구 라이선스를 적용하십시오:

1. **무료 체험** – 라이선스가 필요 없으며 기능이 제한됩니다.  
2. **임시 라이선스** – [Aspose 웹사이트](https://purchase.aspose.com/temporary-license/)에서 요청하십시오.  
3. **구매** – [Aspose 구매 페이지](https://purchase.aspose.com/buy)에서 구독 또는 영구 라이선스를 구매하십시오.

라이선스 파일로 라이브러리를 초기화하십시오:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## ODP 변환을 위한 사용자 정의 폰트 디렉터리 설정 방법
`FontSettings`는 Aspose.Imaging의 폰트 리소스를 관리하는 클래스입니다. 이미지 처리를 시작하기 전에 사용자 정의 폰트를 로드하십시오. 이렇게 하면 모든 슬라이드가 제공한 정확한 폰트를 사용합니다.

Aspose.Imaging의 `FontSettings`를 사용하여 폰트 폴더 경로를 설정하십시오:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*정의*: `FontSettings.setFontsFolder`는 Aspose.Imaging에게 파일 시스템에서 TrueType 및 OpenType 폰트를 찾을 위치를 알려줍니다.

## ODP 변환 중 시스템 대체 폰트 비활성화 방법
시스템 대체 폰트를 비활성화하면 렌더링 엔진이 운영 체제에 설치된 폰트를 무시하도록 강제하여 제공한 폰트만 사용하도록 보장합니다. 이는 슬라이드의 시각적 모양을 변경할 수 있는 예기치 않은 폰트 대체를 방지합니다.

다음 호출로 시스템 대체 폰트를 비활성화하십시오:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*정의*: `FontSettings.setGetSystemAlternativeFont(false)`는 엔진이 정의한 폴더에 있는 폰트만 사용하도록 강제하여 예기치 않은 대체를 방지합니다.

## 지정된 폰트로 ODP 파일을 PNG로 내보내는 방법
`RasterizationOptions`는 벡터 페이지를 비트맵 이미지로 래스터화하는 방식을 정의합니다. 폰트 설정과 래스터화 옵션을 결합하면 각 PNG 내보내기에 대해 DPI, 배경색 및 페이지 크기를 제어할 수 있습니다.

아래와 같이 내보내기 메서드를 구현하십시오:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*정의*: `RasterizationOptions` 클래스는 생성된 PNG 파일의 DPI, 페이지 크기 및 배경색을 제어합니다.

### 일반적인 함정 및 해결책
- **폰트 파일 누락** – ODP에서 참조된 모든 `.ttf` 또는 `.otf` 파일이 설정한 폴더에 존재하는지 확인하십시오.  
- **잘못된 파일 경로** – 절대 경로를 사용하거나 `System.getProperty("user.dir")`를 기준으로 상대 경로를 해결하십시오.  
- **권한 부족** – Java 프로세스가 폰트 디렉터리를 읽고 출력 폴더에 쓸 수 있는지 확인하십시오.

## 실용적인 적용 사례
1. **브랜드 일관성 슬라이드** – 기업 폰트를 유지하면서 웹 게시용으로 프레젠테이션을 PNG로 내보냅니다.  
2. **자동 보고서 생성** – 각 슬라이드를 이미지로 변환하여 PDF 보고서 또는 이메일 뉴스레터에 포함합니다.  
3. **레거시 아카이브 생성** – ODP 콘텐츠를 PNG로 저장하여 ODP 뷰어 없이도 향후 접근성을 보장합니다.

## 성능 고려 사항
- 최신 Aspose.Imaging 버전을 사용하여 다중 스레드 래스터화 개선(8코어 CPU에서 최대 2배 빠름)의 이점을 누리십시오.  
- 이미지 처리를 try‑with‑resources 블록으로 감싸 네이티브 리소스가 적시에 해제되도록 보장하십시오.  
- 수천 개의 슬라이드를 처리할 때는 `RasterizationOptions`(예: 낮은 DPI) 를 조정하여 품질과 메모리 사용량의 균형을 맞추십시오.

## 자주 묻는 질문

**Q: 최소 Java 버전은 무엇인가요?**  
A: Aspose.Imaging for Java는 JDK 8 및 그 이후 버전에서 작동하며, 장기 지원을 위해 JDK 11을 권장합니다.

**Q: 선택한 슬라이드만 변환할 수 있나요?**  
A: 예, `save`를 호출하기 전에 `rasterizationOptions.setPageNumber(specificSlideIndex)`를 설정하십시오.

**Q: 비밀번호로 보호된 ODP 파일을 어떻게 처리하나요?**  
A: 비밀번호가 포함된 `LoadOptions`로 파일을 로드한 후 동일한 폰트 설정으로 진행하십시오.

**Q: 시스템 폰트를 비활성화하면 성능에 영향을 미치나요?**  
A: 엔진이 시스템 폰트 조회를 건너뛰므로 속도가 약간 향상되며, 특히 폰트가 많은 머신에서 눈에 띕니다.

**Q: 더 많은 코드 샘플은 어디서 찾을 수 있나요?**  
A: 배치 변환 및 이미지 변환과 같은 추가 시나리오를 위해 공식 [Aspose.Imaging 문서](https://reference.aspose.com/imaging/java/)를 살펴보십시오.

## 추가 리소스
- [Aspose.Imaging for Java 릴리스](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging 릴리스](https://releases.aspose.com/imaging/java/)  
- [무료 체험 시작](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging 문서](https://reference.aspose.com/imaging/java/)  
- [Aspose.Imaging 포럼](https://forum.aspose.com/c/imaging/14)  
- [Aspose 라이선스 구매](https://purchase.aspose.com/buy)  
- [임시 라이선스 신청](https://purchase.aspose.com/temporary-license/)  

---

**Last Updated:** 2026-06-28  
**Tested With:** Aspose.Imaging for Java 25.5  
**Author:** Aspose

## 관련 튜토리얼

- [Aspose.Imaging for Java를 사용한 ODG를 PNG로 변환: 완전 가이드](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Aspose.Imaging을 사용한 Java 효율적인 이미지 변환: 완전 가이드](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}