---
"description": "Aspose.Imaging for Java를 사용하여 ODG 파일을 PNG 및 PDF로 변환하는 방법을 알아보세요. 효율적인 변환을 위한 단계별 가이드를 따라해 보세요."
"linktitle": "ODG 파일 형식 지원"
"second_title": "Aspose.Imaging Java 이미지 처리 API"
"title": "Aspose.Imaging for Java를 사용하여 ODG를 PNG 및 PDF로 변환"
"url": "/ko/java/metafile-and-vector-image-handling/odg-file-format-support/"
"weight": 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java를 사용하여 ODG를 PNG 및 PDF로 변환

문서 변환 분야에서 Aspose.Imaging for Java는 ODG(OpenDocument Graphics) 파일을 PNG 및 PDF 형식으로 쉽게 변환할 수 있는 강력한 도구로 두각을 나타냅니다. 이 튜토리얼에서는 Aspose.Imaging for Java를 사용하여 변환 과정을 단계별로 안내합니다. 개발자든 ODG 파일 변환을 원하는 사람이든 이 글이 목표를 달성하는 데 도움이 될 것입니다.

## 필수 조건

변환 과정을 시작하기 전에 다음과 같은 전제 조건이 충족되었는지 확인해야 합니다.

### 1. 자바 개발 환경

시스템에 Java 개발 환경이 설정되어 있는지 확인하세요. 최신 Java Development Kit(JDK)은 다음에서 다운로드하여 설치할 수 있습니다. [오라클 웹사이트](https://www.oracle.com/java/technologies/javase-downloads).

### 2. 자바용 Aspose.Imaging

Aspose.Imaging for Java를 다운로드하여 설치해야 합니다. 최신 버전은 다음에서 찾을 수 있습니다. [Aspose.Imaging for Java 다운로드 페이지](https://releases.aspose.com/imaging/java/).

### 3. ODG 파일

물론, 변환하려는 ODG 파일이 필요합니다. 시스템 디렉터리에 해당 파일이 있는지 확인하세요.

## 패키지 가져오기

이제 필수 구성 요소를 갖추었으니, Java 프로젝트에 필요한 패키지를 가져오는 것부터 시작해 보겠습니다. 이 패키지를 사용하면 Aspose.Imaging for Java를 효과적으로 사용할 수 있습니다.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.SizeF;
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
```

이제 변환 과정을 쉽게 따라갈 수 있도록 간단한 단계로 나누어 설명하겠습니다. 각 단계마다 제목과 설명을 첨부하겠습니다.

## 1단계: 데이터 디렉터리 정의

먼저 ODG 파일이 있는 디렉토리를 지정하세요. `"Your Document Directory"` 디렉토리의 실제 경로를 사용합니다.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

## 2단계: ODG 파일 지정

변환할 ODG 파일 이름 배열을 만드세요. 예시 파일 이름을 실제 ODG 파일 이름으로 바꾸세요.

```java
String[] files = new String[] {"example.odg", "example1.odg"};
```

## 3단계: 래스터화 옵션 구성

ODG 파일의 래스터화 옵션을 설정합니다. 이 옵션에 따라 페이지 크기와 벡터 래스터화 설정이 결정됩니다.

```java
final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
```

## 4단계: ODG 파일 반복

이제 각 ODG 파일을 반복해서 살펴보고 로드한 다음 PNG와 PDF 형식으로 변환합니다.

```java
for (String file : files) {
    String fileName = dataDir + file;
    try (Image image = Image.load(fileName)) {
        rasterizationOptions.setPageSize(new SizeF(image.getWidth(), image.getHeight()));

        // PNG로 변환
        String outFileName = "Your Document Directory" + file.replace(".odg", ".png");
        image.save(outFileName, new PngOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});

        // PDF로 변환
        outFileName = "Your Document Directory" + file.replace(".odg", ".pdf");
        image.save(outFileName, new PdfOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});
    }
}
```

축하합니다! Aspose.Imaging for Java를 사용하여 ODG 파일을 PNG와 PDF 형식으로 성공적으로 변환했습니다.

## 결론

Aspose.Imaging for Java는 ODG 파일을 PNG 및 PDF와 같이 더 널리 지원되는 이미지 형식으로 변환하는 과정을 간소화합니다. 이 튜토리얼에 설명된 단계를 따르면 Java 프로젝트에서 이러한 변환을 효율적으로 수행할 수 있습니다.

## 자주 묻는 질문

### 질문 1: Aspose.Imaging for Java는 무료 도구인가요?

A1: 아니요, Aspose.Imaging for Java는 상용 라이브러리이며 가격 정보는 다음에서 찾을 수 있습니다. [구매 페이지](https://purchase.aspose.com/buy).

### 질문 2: 구매하기 전에 Aspose.Imaging for Java를 사용해 볼 수 있나요?

A2: 네, 무료 체험판을 다운로드할 수 있습니다. [여기](https://releases.aspose.com/).

### 질문 3: Java용 Aspose.Imaging에 대한 지원은 어떻게 받을 수 있나요?

A3: 도움을 요청하고 질문을 할 수 있습니다. [Aspose.Imaging 포럼](https://forum.aspose.com/).

### 질문 4: Aspose.Imaging for Java에서는 어떤 다른 파일 형식을 처리할 수 있나요?

A4: Aspose.Imaging for Java는 BMP, JPEG, TIFF, PDF 등 다양한 이미지 및 문서 형식을 지원합니다. [선적 서류 비치](https://reference.aspose.com/imaging/java/) 포괄적인 목록을 보려면 여기를 클릭하세요.

### Q5: 상업 프로젝트에서 Aspose.Imaging for Java를 사용할 수 있나요?

A5: 네, 적절한 라이선스를 구매한 후에는 Aspose.Imaging for Java를 상업 프로젝트에서 사용할 수 있습니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}