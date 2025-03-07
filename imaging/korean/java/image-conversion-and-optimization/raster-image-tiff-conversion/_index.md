---
title: Aspose.Imaging을 사용하여 Java에서 래스터 이미지를 TIFF로 변환
linktitle: 래스터 이미지 TIFF 변환
second_title: Aspose.Imaging Java 이미지 처리 API
description: Aspose.Imaging for Java를 사용하여 Java에서 래스터 이미지를 TIFF 형식으로 변환하는 방법을 알아보세요. 이미지 조작에 대한 포괄적인 가이드입니다.
weight: 20
url: /ko/java/image-conversion-and-optimization/raster-image-tiff-conversion/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging을 사용하여 Java에서 래스터 이미지를 TIFF로 변환

Java 애플리케이션에서 래스터 이미지를 조작하고 변환하려는 경우 Aspose.Imaging for Java가 완벽한 도구입니다. 이 단계별 튜토리얼은 Aspose.Imaging for Java를 사용하여 래스터 이미지를 TIFF 형식으로 변환하는 과정을 안내합니다. 세부 사항을 살펴보기 전에 시작하는 데 필요한 것이 무엇인지 살펴보겠습니다.

## 전제 조건

래스터 이미지를 TIFF로 변환하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

### 1. 자바 개발 환경

시스템에 JDK(Java Development Kit)가 설치되어 있는지 확인하십시오. 오라클 홈페이지에서 다운로드하실 수 있습니다.

### 2. Java용 Aspose.Imaging

 다양한 이미지 형식 작업에 필요한 API를 제공하는 Aspose.Imaging for Java를 구해야 합니다. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/imaging/java/).

### 3. 기본 Java 지식

이 튜토리얼에서는 사용자가 Java 프로그래밍에 대한 기본 지식을 가지고 있다고 가정합니다. 클래스, 개체, 메서드 호출과 같은 개념에 익숙해야 합니다.

## 패키지 가져오기

시작하려면 필요한 Aspose.Imaging for Java 패키지를 Java 프로그램으로 가져와야 합니다. 그렇게 하는 방법은 다음과 같습니다.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.imageoptions.TiffExpectedFormat;
import com.aspose.imaging.imageoptions.TiffPhotometrics;
import com.aspose.imaging.imageoptions.TiffRational;
import com.aspose.imaging.imageoptions.TiffResolutionUnits;
import com.aspose.imaging.imageoptions.TiffPlanarConfigs;
import com.aspose.imaging.imageoptions.TiffCompressions;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

## 1단계: 환경 설정

 첫 번째 단계는 환경을 설정하는 것입니다. 프로젝트용 디렉토리를 생성하고 TIFF로 변환하려는 래스터 이미지를 그 안에 배치하세요. 교체할 수 있습니다`"Your Document Directory"` 프로젝트 디렉터리의 실제 경로를 사용하세요.

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
```

## 2단계: TiffOptions 생성

이제`TiffOptions` TIFF 형식에 대한 다양한 속성을 설정합니다. 요구 사항에 따라 이러한 옵션을 사용자 정의할 수 있습니다.

```java
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
options.setBitsPerSample(new int[] { 8, 8, 8 });
options.setPhotometric(TiffPhotometrics.Rgb);
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));
options.setResolutionUnit(TiffResolutionUnits.Inch);
options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);
options.setCompression(TiffCompressions.AdobeDeflate);
```

## 3단계: 이미지 로드

 인스턴스로 변환하려는 기존 이미지를 로드합니다.`RasterImage`. 이미지 파일의 경로를 지정해야 합니다.

```java
try (RasterImage image = (RasterImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

## 4단계: TiffImage 생성 및 저장

 새로 만들기`TiffImage` ~로부터`RasterImage` 인스턴스를 전달하는 동안 결과 이미지를 저장합니다.`TiffOptions`. 변환된 TIFF 이미지를 저장할 경로를 지정할 수도 있습니다.

```java
    try (TiffImage tiffImage = new TiffImage(new TiffFrame(image))) {
        tiffImage.save("Your Document Directory" + "SavingRasterImage_out.tiff", options);
    }
}
```

그게 다야! Java용 Aspose.Imaging을 사용하여 래스터 이미지를 TIFF 형식으로 성공적으로 변환했습니다.

## 결론

이 튜토리얼에서는 Aspose.Imaging for Java를 사용하여 래스터 이미지를 TIFF 형식으로 변환하는 방법을 배웠습니다. 이 강력한 라이브러리를 사용하면 이미지를 쉽게 조작하고 변환할 수 있습니다. 이미지 처리, 문서 변환 또는 이미지와 관련된 기타 애플리케이션 작업을 하든 Aspose.Imaging for Java는 툴킷에 포함된 귀중한 도구입니다.

 이제 Aspose.Imaging for Java를 최대한 활용하여 Java 애플리케이션의 이미지 작업을 수행할 수 있습니다. 더 많은 기능과 가능성에 대한 설명서를 살펴보십시오.[Java 문서용 Aspose.Imaging](https://reference.aspose.com/imaging/java/).

## FAQ

### Q1: Aspose.Imaging for Java는 어떤 이미지 형식을 지원합니까?
Aspose.Imaging for Java는 JPEG, PNG, TIFF, BMP, GIF 등 다양한 이미지 형식을 지원합니다. 지원되는 형식의 전체 목록은 설명서를 확인하세요.

### Q2: Aspose.Imaging for Java를 사용하여 이미지 편집 작업을 수행할 수 있나요?

A2: 예, Aspose.Imaging for Java를 사용하면 크기 조정, 자르기, 회전 등과 같은 다양한 이미지 편집 작업을 수행할 수 있습니다.

### Q3: Aspose.Imaging for Java의 임시 라이선스를 어떻게 얻을 수 있나요?

 A3: 다음 사이트를 방문하시면 임시면허증을 받으실 수 있습니다.[임시 면허를 양도하다](https://purchase.aspose.com/temporary-license/).

### Q4: Aspose.Imaging for Java에 대한 무료 평가판이 있습니까?

 A4: 예, 다음에서 Aspose.Imaging for Java의 무료 평가판에 액세스할 수 있습니다.[Aspose.Imaging 무료 평가판](https://releases.aspose.com/).

### Q5: Aspose.Imaging for Java에 대한 지원을 받거나 질문을 할 수 있는 곳은 어디입니까?

 A5: Aspose.Imaging 커뮤니티에 가입하고 다음에서 지원을 받을 수 있습니다.[Aspose.이미징 포럼](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
