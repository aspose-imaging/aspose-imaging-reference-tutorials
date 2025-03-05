---
title: Java용 Aspose.Imaging을 사용하여 ODG를 PNG 및 PDF로 변환
linktitle: ODG 파일 형식 지원
second_title: Aspose.Imaging Java 이미지 처리 API
description: Java용 Aspose.Imaging을 사용하여 ODG 파일을 PNG 및 PDF로 변환하는 방법을 알아보세요. 효율적인 변환을 위해 단계별 가이드를 따르세요.
type: docs
weight: 12
url: /ko/java/metafile-and-vector-image-handling/odg-file-format-support/
---
문서 변환 분야에서 Aspose.Imaging for Java는 ODG(OpenDocument Graphics) 파일을 PNG 및 PDF 형식으로 쉽게 변환할 수 있는 강력한 도구로 돋보입니다. 이 튜토리얼은 Aspose.Imaging for Java를 사용하는 프로세스를 단계별로 안내합니다. 개발자이든 ODG 파일을 변환하려는 사람이든 이 문서는 목표를 달성하는 데 도움이 될 것입니다.

## 전제 조건

변환 프로세스를 시작하기 전에 다음 전제 조건이 충족되었는지 확인해야 합니다.

### 1. 자바 개발 환경

 시스템에 Java 개발 환경이 설정되어 있는지 확인하십시오. 최신 JDK(Java Development Kit)를 다운로드하여 설치할 수 있습니다.[오라클 웹사이트](https://www.oracle.com/java/technologies/javase-downloads).

### 2. Java용 Aspose.Imaging

 Java용 Aspose.Imaging을 다운로드하여 설치해야 합니다. 최신 버전은 다음에서 찾을 수 있습니다.[Aspose.Imaging for Java 다운로드 페이지](https://releases.aspose.com/imaging/java/).

### 3. ODG 파일

물론 변환하려는 ODG 파일이 필요합니다. 시스템의 디렉토리에 이러한 파일이 있는지 확인하십시오.

## 패키지 가져오기

이제 전제조건이 준비되었으므로 Java 프로젝트에 필요한 패키지를 가져오는 것부터 시작해 보겠습니다. 이 패키지를 사용하면 Aspose.Imaging for Java를 효과적으로 사용할 수 있습니다.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.SizeF;
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
```

이제 쉽게 따라할 수 있도록 변환 프로세스를 간단한 단계로 나누어 보겠습니다. 각 단계마다 제목과 설명이 제공됩니다.

## 1단계: 데이터 디렉터리 정의

 ODG 파일이 있는 디렉터리를 지정하여 시작하세요. 교체하셔야 합니다`"Your Document Directory"` 디렉터리의 실제 경로를 사용합니다.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

## 2단계: ODG 파일 지정

변환하려는 ODG 파일 이름 배열을 만듭니다. 예제 파일 이름을 ODG 파일 이름으로 바꿉니다.

```java
String[] files = new String[] {"example.odg", "example1.odg"};
```

## 3단계: 래스터화 옵션 구성

ODG 파일의 래스터화 옵션을 설정합니다. 이러한 옵션은 페이지 크기와 벡터 래스터화 설정을 결정합니다.

```java
final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
```

## 4단계: ODG 파일 반복

이제 각 ODG 파일을 반복하여 로드하고 PNG 및 PDF 형식으로 변환합니다.

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

축하해요! Java용 Aspose.Imaging을 사용하여 ODG 파일을 PNG 및 PDF 형식으로 성공적으로 변환했습니다.

## 결론

Aspose.Imaging for Java는 ODG 파일을 PNG 및 PDF와 같이 보다 널리 지원되는 이미지 형식으로 변환하는 프로세스를 단순화합니다. 이 튜토리얼에 설명된 단계를 따르면 Java 프로젝트에서 이러한 변환을 효율적으로 수행할 수 있습니다.

## FAQ

### Q1: Aspose.Imaging for Java는 무료 도구입니까?

 A1: 아니요, Aspose.Imaging for Java는 상업용 라이브러리이며 가격 정보는 다음에서 확인할 수 있습니다.[구매 페이지](https://purchase.aspose.com/buy).

### Q2: 구매하기 전에 Java용 Aspose.Imaging을 사용해 볼 수 있나요?

 A2: 예, 다음에서 무료 평가판을 다운로드할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Java용 Aspose.Imaging에 대한 지원을 어떻게 받을 수 있나요?

 답변 3: 다음 웹사이트에서 도움을 구하고 질문할 수 있습니다.[Aspose.이미징 포럼](https://forum.aspose.com/).

### Q4: Aspose.Imaging for Java가 처리할 수 있는 다른 파일 형식은 무엇입니까?

 A4: Aspose.Imaging for Java는 BMP, JPEG, TIFF, PDF 등을 포함한 광범위한 이미지 및 문서 형식을 지원합니다. 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/imaging/java/) 포괄적인 목록을 보려면

### Q5: 상업용 프로젝트에서 Java용 Aspose.Imaging을 사용할 수 있나요?

A5: 예, 적절한 라이선스를 구매한 후 상업용 프로젝트에서 Aspose.Imaging for Java를 사용할 수 있습니다.