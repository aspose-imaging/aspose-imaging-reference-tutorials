---
title: Java용 Aspose.Imaging을 사용하여 기본 글꼴 사용 최적화
linktitle: 기본 글꼴 사용 최적화
second_title: Aspose.Imaging Java 이미지 처리 API
description: Aspose.Imaging for Java를 사용하여 기본 글꼴 사용을 최적화하는 방법을 알아보세요. 단계별 지침을 통해 문서 처리를 개선하세요.
type: docs
weight: 10
url: /ko/java/image-processing-and-enhancement/optimize-default-font-usage/
---
문서 처리 및 이미지 조작 분야에서 Aspose.Imaging for Java는 강력한 도구로 돋보입니다. 이 다목적 Java 라이브러리를 사용하면 개발자가 이미지를 쉽게 생성, 편집 및 변환할 수 있습니다. 문서 처리 최적화의 주요 측면 중 하나는 글꼴 사용을 개선하는 것입니다. 이 단계별 가이드에서는 Aspose.Imaging for Java를 사용하여 기본 글꼴 사용을 최적화하는 방법을 살펴보겠습니다. 프로세스를 철저하게 이해할 수 있도록 각 예를 여러 단계로 나누어 보겠습니다.

## 전제 조건

최적화 프로세스를 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- 시스템에 설치된 Java 개발 환경.
-  Aspose.Imaging for Java 라이브러리. 다음에서 다운로드할 수 있습니다.[웹사이트](https://releases.aspose.com/imaging/java/).
- Java 프로그래밍에 대한 기본 지식.

## 패키지 가져오기

기본 글꼴 사용 최적화를 시작하려면 Aspose.Imaging for Java에서 필요한 패키지를 가져와야 합니다. 이를 수행하는 단계는 다음과 같습니다.

Aspose.Imaging 라이브러리 가져오기

먼저 다음 가져오기 문을 추가하여 Java 프로젝트에 Aspose.Imaging 라이브러리를 포함합니다.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fonts.FontSettings;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.odg.OdgRasterizationOptions;
```

이제 필요한 패키지를 가져왔으므로 최적화 프로세스를 여러 단계로 나누어 보겠습니다.

## 1단계: 문서 디렉터리 설정

 글꼴 사용을 최적화하기 전에 문서 디렉터리를 설정해야 합니다. 바꾸다`"Your Document Directory" + "otg/"` 문서 디렉토리의 실제 경로를 사용하십시오. 예를 들어:

```java
String dataDir = "C:/Documents/";
String outDir = Utils.getOutDir("DefaultFontUsageImprove");
```

## 2단계: 글꼴 설정 구성

기본 글꼴 사용을 개선하려면 다음과 같이 글꼴 설정을 구성하십시오.

```java
FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
FontSettings.setGetSystemAlternativeFont(false);
```

## 3단계: 기본 글꼴을 사용하여 PNG로 내보내기

이제 지정된 기본 글꼴을 사용하여 문서를 PNG 이미지로 내보내겠습니다. 여기에는 두 가지 예가 있습니다. 하나는 "Arial"을 사용하고 다른 하나는 "Courier New"를 기본 글꼴로 사용합니다.

```java
exportToPng(Path.combine(dataDir, "missing-font2.odg"), "Arial", Path.combine(outDir, "arial.png"));
exportToPng(
    Path.combine(dataDir, "missing-font2.odg"),
    "Courier New",
    Path.combine(outDir, "courier.png"));
```

## 4단계: PNG 기능으로 내보내기

 여기에`exportToPng` 지정된 기본 글꼴을 사용하여 PNG로 실제 내보내기를 수행하는 함수:

```java
private static void exportToPng(String filePath, String defaultFontName, String outfileName)
{
    FontSettings.setDefaultFontName(defaultFontName);
    try (Image document = Image.load(filePath))
    {
        PngOptions saveOptions = new PngOptions();
        final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
        rasterizationOptions.setPageWidth(1000);
        rasterizationOptions.setPageHeight(1000);
        saveOptions.setVectorRasterizationOptions(rasterizationOptions);
        document.save(outfileName, saveOptions);
    }
    Utils.deleteFile(outfileName);
}
```

이 기능은 기본 글꼴을 설정하고, 문서를 로드하고, 내보내기 옵션을 구성하고, 출력 PNG 이미지를 저장합니다.

## 결론

문서 처리 시 기본 글꼴 사용을 최적화하면 출력 품질을 크게 향상시킬 수 있습니다. Aspose.Imaging for Java는 이 프로세스를 단순화하여 글꼴을 지정하고 문서를 효율적으로 내보낼 수 있도록 해줍니다. 이 문서에 설명된 단계별 가이드를 따르면 글꼴 사용을 쉽게 개선할 수 있습니다.

## FAQ

### Q1: Java용 Aspose.Imaging이 무엇인가요?

A1: Aspose.Imaging for Java는 이미지 생성, 변환, 조작을 포함하여 이미지와 문서 작업을 위한 광범위한 기능을 제공하는 Java 라이브러리입니다.

### Q2: Java용 Aspose.Imaging을 어떻게 구할 수 있나요?

 A2: 다음 웹사이트에서 Java용 Aspose.Imaging을 다운로드할 수 있습니다.[이 링크](https://releases.aspose.com/imaging/java/).

### Q3: Aspose.Imaging for Java에 대한 라이선스 옵션이 있습니까?

 A3: 네, Aspose.Imaging for Java 라이선스를 다음 사이트에서 구매할 수 있습니다.[구매 페이지](https://purchase.aspose.com/buy).

### Q4: 무료 평가판이 제공됩니까?

A4: 예, 다음에서 평가판을 다운로드하여 Java용 Aspose.Imaging을 무료로 사용해 볼 수 있습니다.[여기](https://releases.aspose.com/).

### Q5: Java용 Aspose.Imaging에 대한 지원은 어디서 받을 수 있나요?

 A5: 도움이 필요하거나 질문이 있는 경우 Aspose.Imaging for Java 지원 포럼을 방문하세요.[https://forum.aspose.com/](https://forum.aspose.com/).