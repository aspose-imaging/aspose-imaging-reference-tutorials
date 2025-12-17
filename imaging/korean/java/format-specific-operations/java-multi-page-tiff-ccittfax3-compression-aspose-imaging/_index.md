---
"date": "2025-06-04"
"description": "Aspose.Imaging을 사용하여 Java에서 CCITTFAX3 압축을 사용하여 다중 페이지 TIFF 파일을 만드는 방법을 배우고, 효율적인 문서 스캔 및 보관 기술을 익혀보세요."
"title": "Aspose.Imaging을 사용하여 Java에서 CCITTFAX3 압축으로 다중 페이지 TIFF 만들기"
"url": "/ko/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging을 사용하여 Java에서 CCITTFAX3 압축을 통한 다중 페이지 TIFF 생성 마스터하기

## 소개

여러 페이지로 구성된 TIFF 파일을 생성하여 문서 스캔 및 보관 프로세스를 효율적으로 관리하고 싶으신가요? Aspose.Imaging for Java를 사용하면 이 작업이 훨씬 수월해집니다. 이 가이드에서는 CCITTFAX3 압축 방식을 사용하여 여러 페이지로 구성된 TIFF 파일을 만드는 방법을 안내합니다. 이 압축 방식은 스캔 문서와 같은 단색 이미지에 이상적입니다. 이러한 기술을 숙달하면 대용량 이미지 데이터를 효과적으로 처리할 수 있는 역량을 갖추게 될 것입니다.

**배울 내용:**
- Java 프로젝트에 Aspose.Imaging을 설정합니다.
- CCITTFAX3 압축을 사용하여 TiffOptions를 만듭니다.
- 새로운 TiffImage 인스턴스를 생성하고 구성합니다.
- TIFF 파일에 이미지를 로드하고 크기를 조정하고 프레임으로 추가합니다.
- 여러 페이지로 구성된 TIFF 파일을 저장하고 최적화합니다.

Java 애플리케이션에서 이러한 기능을 구현하는 방법을 살펴보겠습니다.

## 필수 조건

시작하기에 앞서 다음과 같은 전제 조건이 충족되었는지 확인하세요.

### 필수 라이브러리
- **Java용 Aspose.Imaging**현재 모든 기능을 사용하려면 버전 25.5 이상을 사용하는 것이 좋습니다.
  
### 환경 설정 요구 사항
- 컴퓨터에 Java 개발 키트(JDK)가 설치되어 있어야 합니다.
- IntelliJ IDEA나 Eclipse와 같은 IDE.

### 지식 전제 조건
- Java 프로그래밍과 객체 지향 개념에 대한 기본적인 이해가 있습니다.
- 종속성 관리를 위해 Maven/Gradle을 잘 알고 있습니다.

## Java용 Aspose.Imaging 설정

프로젝트에서 Aspose.Imaging을 사용하려면 종속성으로 포함해야 합니다. 다양한 빌드 도구를 사용하여 이 작업을 수행하는 방법은 다음과 같습니다.

**메이븐:**
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**그래들:**
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### 직접 다운로드

또는 최신 버전을 다음에서 직접 다운로드할 수 있습니다. [Java 릴리스용 Aspose.Imaging](https://releases.aspose.com/imaging/java/).

### 라이센스 취득

제한 없이 모든 기능을 탐색할 수 있는 무료 평가판 라이선스를 얻으려면 여기를 방문하세요. [Aspose 무료 체험 페이지](https://releases.aspose.com/imaging/java/). 장기간 사용 시 라이센스 구매 또는 임시 라이센스 신청을 고려해 보세요. [Aspose 구매](https://purchase.aspose.com/temporary-license/).

### 기본 초기화

프로젝트에 Aspose.Imaging을 포함시킨 후 다음과 같이 초기화합니다.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```

## 구현 가이드

우리는 기능에 따라 구현을 여러 개의 논리적 섹션으로 나눌 것입니다.

### CCITTFAX3 압축을 사용하여 TiffOptions 만들기

#### 개요
만들기 `TiffOptions` TIFF 형식의 흑백 이미지를 처리할 때는 CCITTFAX3 압축으로 구성된 인스턴스가 필수적입니다. 이 기능은 저장 공간을 최적화하고 이미지 품질을 효과적으로 유지합니다.

**단계:**

1. **CCITTFAX3로 TiffOptions 초기화**
    ```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```

2. **출력 파일 소스 설정**
    ```java
    // "YOUR_OUTPUT_DIRECTORY"를 실제 디렉토리 경로로 바꾸세요.
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```

### 새 TiffImage 인스턴스 만들기

#### 개요
인스턴스 생성 `TiffImage` 치수를 지정하고 이전에 구성된 것을 활용하는 것이 포함됩니다. `TiffOptions`.

**단계:**

1. **차원 선언**
    ```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```

2. **TiffImage 인스턴스 생성**
    ```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```

### 디렉토리에서 이미지 로드 및 크기 조정

#### 개요
이미지 로딩에는 디렉토리에서 파일을 읽고, 확장자로 필터링하고, TIFF 크기에 맞게 크기를 조정하는 작업이 포함됩니다.

**단계:**

1. **JPG 파일 필터링 및 로드**
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

2. **이미지 크기 조정**
    ```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```

### 다중 페이지 TIFF 이미지에 프레임 추가

#### 개요
여러 페이지로 구성된 TIFF 파일을 제작하려면 프레임을 추가하는 것이 중요합니다. 각 프레임은 개별 이미지에 해당합니다.

**단계:**

1. **이미지 반복 및 프레임 생성**
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

### 다중 페이지 TIFF 이미지 저장

#### 개요
마지막으로, 리소스를 저장하고 닫으면 모든 변경 사항이 유지됩니다.

**단계:**

1. **변경 사항 저장**
    ```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```

## 실제 응용 프로그램

CCITTFAX3 압축을 사용하여 다중 페이지 TIFF 파일을 만드는 것은 다음과 같은 여러 시나리오에서 유용할 수 있습니다.

- **문서 보관**: 스캔한 문서를 효율적으로 저장하고 보관합니다.
- **의료 영상**: 영상의학과에서 고품질의 압축 이미지를 유지합니다.
- **인쇄 서비스**: 여러 개의 이미지 페이지가 필요한 대형 인쇄 작업을 준비합니다.

## 성능 고려 사항

최적의 성능을 보장하려면:
- 처리 시간을 줄이는 동시에 품질을 유지하려면 적절한 크기 조정 방법을 사용하세요.
- 사용 후 리소스를 즉시 닫아 메모리를 효과적으로 관리합니다.
- 파일 I/O 작업을 최적화하고 대규모 데이터 세트에 대한 비동기 처리를 고려합니다.

## 결론

이 튜토리얼에서는 Aspose.Imaging을 사용하여 Java에서 CCITTFAX3 압축을 사용하여 다중 페이지 TIFF 파일을 만드는 방법을 배웠습니다. 이러한 단계를 이해하면 다양한 애플리케이션의 이미지 데이터를 효율적으로 관리할 수 있습니다. 기술을 더욱 향상시키려면 Aspose.Imaging 라이브러리의 추가 기능을 살펴보고 프로젝트에 통합해 보세요.

## FAQ 섹션

1. **CCITTFAX3 압축이란 무엇인가요?**
   - 이는 흑백 이미지에 맞게 특별히 고안된 압축 방식으로, 문서 스캐닝에 자주 사용됩니다.

2. **대용량 이미지 데이터 세트를 효율적으로 처리하려면 어떻게 해야 하나요?**
   - 비동기 처리를 구현하고 메모리 사용량을 최적화하여 리소스를 효과적으로 관리합니다.

3. **Aspose.Imaging을 다른 시스템과 통합할 수 있나요?**
   - 네, 다양한 파일 형식과 시스템과 원활하게 통합할 수 있는 API를 제공합니다.

4. **Aspose.Imaging의 라이선싱 옵션은 무엇입니까?**
   - 옵션으로는 무료 체험판, 장기 테스트를 위한 임시 라이선스, 전체 라이선스 구매 등이 있습니다.

5. **TIFF 파일을 사용할 때 발생하는 일반적인 문제는 어떻게 해결합니까?**
   - Aspose를 참조하세요 [선적 서류 비치](https://reference.aspose.com/imaging/java/) 문제 해결 팁을 위한 지원 포럼도 있습니다.

## 자원

- **선적 서류 비치**https://reference.aspose.com/imaging/java/
- **다운로드**: https://releases.aspose.com/imaging/java/
- **구입**: https://purchase.aspose.com/buy
- **무료 체험**: https://releases.aspose.com/imaging/java/
- **임시 면허**: https://purchase.aspose.com/temporary-license/
- **지원하다**: https://forum.aspose.com/c/imaging/14

이제 지식을 갖추었으니, Java 프로젝트에서 이러한 기술을 구현하고 탐색해보세요!

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}