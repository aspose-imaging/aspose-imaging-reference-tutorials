---
date: 2026-05-18
description: Java 이미지 처리 라이브러리 Aspose.Imaging을 사용하여 이미지에 XMP 메타데이터를 삽입하고 검색하는 방법을
  step‑by‑step code와 함께 배웁니다.
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: 이미지에서 XMP 데이터 처리
schemas:
- author: Aspose
  dateModified: '2026-05-18'
  description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  headline: 'Java Image Processing Library: XMP with Aspose.Imaging'
  type: TechArticle
- description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  name: 'Java Image Processing Library: XMP with Aspose.Imaging'
  steps:
  - name: Specify Image Size and Tiff Options
    text: First, define the directory where your image will be stored and create a
      `Rectangle` to specify the size of the image. In this example, we use a TIFF
      image with certain options. `TiffOptions` configures format‑specific settings
      for the TIFF image.
  - name: Create a New Image
    text: Now, create a new image with the specified options. This image will be used
      to store the XMP metadata. `TiffImage` represents a TIFF image object, and `TiffFrame`
      defines an individual frame within it.
  - name: Create XMP Header and Trailer
    text: Create instances of XMP‑Header and XMP‑Trailer for your XMP metadata. These
      headers and trailers help define the metadata structure. `XmpHeaderPi` and `XmpTrailerPi`
      represent the XMP packet’s opening and closing sections.
  - name: Create XMP Meta Information
    text: Now, create an instance of XMP meta to set different attributes. You can
      add information like the author and description. `XmpMeta` holds the core metadata
      fields such as author and description.
  - name: Create XMP Packet Wrapper
    text: '`XmpPacketWrapper` is the container that holds the XMP header, trailer,
      and meta information in a single packet. It ensures the packet conforms to the
      XMP specification. `XmpPacketWrapper` packages the header, meta, and trailer
      into a single XMP packet.'
  - name: Add Photoshop Package
    text: To store Photoshop‑specific information, create a Photoshop package and
      set its attributes, such as city, country, and color mode. Then, add this package
      to the XMP metadata. `PhotoshopPackage` stores Photoshop‑specific metadata like
      city, country, and color mode.
  - name: Add Dublin Core Package
    text: For more general information, like author, title, and additional values,
      create a DublinCore package and set its attributes. Add this package to the
      XMP metadata as well. `DublinCorePackage` contains standard Dublin Core fields
      such as title, creator, and keywords.
  - name: Update XMP Metadata in the Image
    text: Update the XMP metadata into the image using the `setXmpData` method. This
      call writes the XMP packet into the image’s metadata section. `setXmpData` writes
      the XMP packet into the image’s metadata section.
  - name: Save the Image
    text: You can now save the image with the embedded XMP metadata on the disk or
      in a memory stream.
  - name: Load the Image and Retrieve XMP Metadata
    text: To retrieve the XMP metadata from the image, load the image from the memory
      stream or disk and access the XMP data via the `getXmpData` method. `getXmpData`
      reads the embedded XMP packet from the image. Congratulations! You've successfully
      learned how to handle XMP data in images using Aspose.Imagin
  type: HowTo
- questions:
  - answer: XMP is an XML‑based standard for embedding descriptive information directly
      inside files, enabling consistent metadata across applications.
    question: What is XMP metadata?
  - answer: It lets you tag images with author, copyright, keywords, and custom data,
      improving searchability and asset management without external databases.
    question: Why is XMP metadata important?
  - answer: Yes, Aspose.Imaging for Java provides methods to modify existing XMP packets
      and write them back to the file.
    question: Can I edit XMP metadata after embedding it in an image?
  - answer: A free trial is available for evaluation, but a paid license is required
      for production use. You can explore options on the [Aspose.Imaging for Java
      website](https://purchase.aspose.com/buy).
    question: Is Aspose.Imaging for Java a free tool?
  - answer: Visit the [Aspose.Imaging forums](https://forum.aspose.com/) for community
      assistance, or contact Aspose support directly for paid‑license customers.
    question: Where can I get help and support for Aspose.Imaging for Java?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: 'Java 이미지 처리 라이브러리: XMP with Aspose.Imaging'
url: /ko/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java를 사용한 이미지의 XMP 데이터 처리

Aspose.Imaging은 **java image processing library**로 수십 가지 래스터 및 벡터 형식을 다룰 수 있습니다. 이 튜토리얼에서는 Aspose.Imaging for Java를 사용하여 이미지에 XMP(Extensible Metadata Platform) 데이터를 삽입하고 검색하는 방법을 배웁니다. 끝까지 진행하면 저자, 설명 및 사용자 정의 메타데이터를 이미지 파일에 직접 저장하여 검색 가능하고 자체 설명이 가능하게 됩니다.

## 빠른 답변
- **What is XMP?** XMP는 이미지, PDF, 비디오와 같은 파일에 메타데이터를 삽입하기 위한 표준화된 XML 기반 포맷입니다.  
- **Which library handles XMP in Java?** Aspose.Imaging for Java는 XMP 패킷을 읽고 쓰기 위한 완전한 API를 제공합니다.  
- **Do I need a license?** 무료 체험판은 개발에 사용할 수 있으며, 상용 환경에서는 상업 라이선스가 필요합니다.  
- **How many image formats are supported?** TIFF, JPEG, PNG, PSD, RAW 등을 포함해 150개 이상의 포맷을 지원합니다.  
- **Can I process large images?** 예 – 라이브러리는 전체 이미지를 메모리에 로드하지 않고도 최대 2 GB 파일을 처리할 수 있습니다.

## XMP 메타데이터란?
XMP 메타데이터는 디지털 파일에 직접 서술 정보를 삽입하기 위한 XML 기반 표준입니다. 저자, 저작권, 키워드 및 사용자 정의 데이터를 일관되게 저장할 수 있게 해줍니다. XML이기 때문에 사용자 정의 네임스페이스를 통해 고유 필드를 추가할 수 있으며, 핵심 스키마를 이해하는 도구와도 호환됩니다. 이러한 특성 덕분에 XMP는 장기 자산 관리와 애플리케이션 간 상호 운용성에 이상적입니다.

## 왜 Java 이미지 처리 라이브러리를 사용해 XMP를 다루나요?
Aspose.Imaging for Java는 **150+ image formats**를 지원하고 스트리밍 방식으로 멀티 기가바이트 파일을 처리하여 메모리 사용량을 최대 80 % 절감합니다. 또한 API는 XMP 패킷이 표준을 준수하도록 보장하므로 Adobe Photoshop, Lightroom 등과의 호환성을 유지합니다.

## 전제 조건

시작하기 전에 다음이 준비되어 있어야 합니다:

- 컴퓨터에 Java 개발 환경이 설정되어 있어야 합니다.  
- Aspose.Imaging for Java 라이브러리를 설치합니다. [Aspose.Imaging for Java website](https://releases.aspose.com/imaging/java/)에서 다운로드할 수 있습니다.  
- Java 프로그래밍에 대한 기본적인 이해가 필요합니다.

## 패키지 가져오기

프로젝트에 필요한 패키지를 가져옵니다. 코드 시작 부분에 다음 import 문을 추가하십시오:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.xmp.XmpPackage;
import com.aspose.imaging.xmp.XmpPacketWrapper;
import com.aspose.imaging.xmp.XmpMeta;
import com.aspose.imaging.xmp.photoshop.ColorMode;
import com.aspose.imaging.xmp.photoshop.PhotoshopPackage;
import com.aspose.imaging.xmp.dc.DublinCorePackage;
import com.aspose.imaging.xmp.header.XmpHeaderPi;
import com.aspose.imaging.xmp.trailer.XmpTrailerPi;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

이제 예제를 단계별 가이드로 나누어 보겠습니다:

## Java 이미지 처리 라이브러리를 사용해 XMP 메타데이터를 삽입하는 방법

이미지를 로드하고, XMP 패킷을 생성한 뒤, 이미지에 첨부하고 저장합니다 – 몇 줄의 간결한 코드로 가능합니다. Aspose.Imaging의 `setXmpData` 메서드는 별도의 메타데이터 파일 없이 바로 파일에 패킷을 기록합니다. 이 과정은 파일 기반 이미지와 스트림 기반 이미지 모두에 적용되어 웹 서비스와 배치 작업에 적합합니다.

### 단계 1: 이미지 크기 및 Tiff 옵션 지정

먼저 이미지가 저장될 디렉터리를 정의하고 `Rectangle`을 만들어 이미지 크기를 지정합니다. 여기서는 특정 옵션을 가진 TIFF 이미지를 사용합니다. `TiffOptions`는 TIFF 이미지에 대한 형식별 설정을 구성합니다.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### 단계 2: 새 이미지 생성

지정한 옵션으로 새 이미지를 생성합니다. 이 이미지는 XMP 메타데이터를 저장하는 데 사용됩니다. `TiffImage`는 TIFF 이미지 객체를 나타내며, `TiffFrame`은 그 안의 개별 프레임을 정의합니다.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### 단계 3: XMP 헤더 및 트레일러 생성

XMP 메타데이터를 위한 XMP‑Header와 XMP‑Trailer 인스턴스를 생성합니다. 이 헤더와 트레일러는 메타데이터 구조를 정의하는 데 도움을 줍니다. `XmpHeaderPi`와 `XmpTrailerPi`는 XMP 패킷의 시작 및 종료 섹션을 나타냅니다.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### 단계 4: XMP 메타 정보 생성

이제 XMP 메타 인스턴스를 만들어 다양한 속성을 설정합니다. 저자와 설명 같은 정보를 추가할 수 있습니다. `XmpMeta`는 저자, 설명 등 핵심 메타데이터 필드를 보유합니다.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### 단계 5: XMP 패킷 래퍼 생성

`XmpPacketWrapper`는 XMP 헤더, 트레일러 및 메타 정보를 하나의 패킷에 담는 컨테이너입니다. 패킷이 XMP 사양을 준수하도록 보장합니다. `XmpPacketWrapper`는 헤더, 메타, 트레일러를 단일 XMP 패킷으로 패키징합니다.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### 단계 6: Photoshop 패키지 추가

Photoshop‑specific 정보를 저장하기 위해 Photoshop 패키지를 생성하고 도시, 국가, 색상 모드와 같은 속성을 설정합니다. 그런 다음 이 패키지를 XMP 메타데이터에 추가합니다. `PhotoshopPackage`는 도시, 국가, 색상 모드 등 Photoshop 전용 메타데이터를 저장합니다.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### 단계 7: Dublin Core 패키지 추가

저자, 제목 및 추가 값과 같은 일반 정보를 위해 DublinCore 패키지를 생성하고 속성을 설정합니다. 이 패키지도 XMP 메타데이터에 추가합니다. `DublinCorePackage`는 제목, 작성자, 키워드 등 표준 Dublin Core 필드를 포함합니다.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### 단계 8: 이미지에 XMP 메타데이터 업데이트

`setXmpData` 메서드를 사용해 이미지에 XMP 메타데이터를 업데이트합니다. 이 호출은 XMP 패킷을 이미지 메타데이터 섹션에 기록합니다. `setXmpData`는 XMP 패킷을 이미지 메타데이터 섹션에 기록합니다.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### 단계 9: 이미지 저장

이제 이미지에 삽입된 XMP 메타데이터를 디스크나 메모리 스트림에 저장할 수 있습니다.

```java
    image.save(ms);
```

### 단계 10: 이미지 로드 및 XMP 메타데이터 검색

메모리 스트림이나 디스크에서 이미지를 로드하고 `getXmpData` 메서드를 통해 XMP 메타데이터를 가져옵니다. `getXmpData`는 이미지에 삽입된 XMP 패킷을 읽어옵니다.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

축하합니다! Aspose.Imaging for Java를 사용해 이미지에서 XMP 데이터를 처리하는 방법을 성공적으로 배웠습니다. 이제 이미지 파일 내에 귀중한 메타데이터를 저장하고 검색할 수 있습니다.

## 일반적인 문제 및 해결책

- **Metadata not appearing in Photoshop:** XMP 패킷이 올바른 XML 스키마를 따르는지 확인하세요; Aspose.Imaging이 자동으로 검증하지만, 사용자 정의 네임스페이스는 등록이 필요할 수 있습니다.  
- **Large TIFF files cause OutOfMemoryError:** `Compression`을 `LZW`로 설정한 `TiffOptions`를 사용하고 스트리밍(`loadOptions.setBufferSize`)을 활성화하여 메모리 사용량을 낮추세요.  
- **Unexpected character encoding:** XMP는 UTF‑8을 기대합니다; 문자열은 항상 `StandardCharsets.UTF_8`을 사용해 전달하여 깨진 데이터를 방지하세요.

## 자주 묻는 질문

**Q: What is XMP metadata?**  
A: XMP는 파일 내부에 직접 서술 정보를 삽입하기 위한 XML 기반 표준으로, 애플리케이션 간 일관된 메타데이터를 가능하게 합니다.

**Q: Why is XMP metadata important?**  
A: 이미지에 저자, 저작권, 키워드 및 사용자 정의 데이터를 태그함으로써 외부 데이터베이스 없이도 검색 가능성과 자산 관리 효율성을 높여줍니다.

**Q: Can I edit XMP metadata after embedding it in an image?**  
A: 예, Aspose.Imaging for Java는 기존 XMP 패킷을 수정하고 파일에 다시 기록하는 메서드를 제공합니다.

**Q: Is Aspose.Imaging for Java a free tool?**  
A: 평가용 무료 체험판을 제공하지만, 상용 환경에서는 유료 라이선스가 필요합니다. 옵션은 [Aspose.Imaging for Java website](https://purchase.aspose.com/buy)에서 확인할 수 있습니다.

**Q: Where can I get help and support for Aspose.Imaging for Java?**  
A: 커뮤니티 지원은 [Aspose.Imaging forums](https://forum.aspose.com/)에서 받을 수 있으며, 유료 라이선스 고객은 Aspose 지원팀에 직접 문의할 수 있습니다.

## 결론

이 튜토리얼에서는 선도적인 **java image processing library**인 Aspose.Imaging for Java를 사용해 이미지에서 XMP 메타데이터를 다루는 방법을 살펴보았습니다. 단계별 가이드를 따라 하면 XMP 데이터를 손쉽게 삽입, 업데이트 및 검색하여 디지털 자산에 검색 가능하고 표준을 준수하는 메타데이터를 부여할 수 있습니다.

---

**마지막 업데이트:** 2026-05-18  
**테스트 환경:** Aspose.Imaging for Java 24.12  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [마스터 Java 이미지 처리: Aspose.Imaging으로 EXIF 데이터 수정](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [Aspose.Imaging을 사용한 Java 이미지 처리: 로드, 향상 및 이미지 저장](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [Aspose.Imaging 라이브러리를 활용한 고급 Java 이미지 처리](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Specify the size of image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// create the brand new image just for sample purposes
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// create an instance of XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// create an instance of Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// create an instance of XMP meta class to set different attributes
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// create an instance of XmpPacketWrapper that contains all metadata
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// create an instance of Photoshop package and set photoshop attributes
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// add photoshop package into XMP metadata
	xmpData.addPackage(photoshopPackage);
	// create an instance of DublinCore package and set dublinCore attributes
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// add dublinCore Package into XMP metadata
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// update XMP metadata into image
	image.setXmpData(xmpData);
	// Save image on the disk or in memory stream
	image.save(ms);
	// Load the image from memory stream or from disk to read/get the metadata
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Getting the XMP metadata
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Use package data ...
		}
	}
}
        
```