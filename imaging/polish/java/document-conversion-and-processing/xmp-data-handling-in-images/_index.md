---
title: Obsługa danych XMP w obrazach za pomocą Aspose.Imaging dla Java
linktitle: Obsługa danych XMP w obrazach
second_title: Aspose.Imaging API przetwarzania obrazu Java
description: Dowiedz się, jak obsługiwać metadane XMP w obrazach przy użyciu Aspose.Imaging dla Java. Osadzaj i pobieraj metadane, aby ulepszyć swoje pliki obrazów.
weight: 16
url: /pl/java/document-conversion-and-processing/xmp-data-handling-in-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obsługa danych XMP w obrazach za pomocą Aspose.Imaging dla Java

Aspose.Imaging dla Java to wszechstronna i wydajna biblioteka do pracy z obrazami w różnych formatach. Ten samouczek poprowadzi Cię przez proces obsługi danych XMP (Extensible Metadata Platform) w obrazach przy użyciu Aspose.Imaging for Java. XMP to standard osadzania metadanych w plikach obrazów, umożliwiający przechowywanie cennych informacji, takich jak autor, opis i inne.

## Warunki wstępne

Zanim zaczniesz, upewnij się, że spełnione są następujące wymagania wstępne:

- Środowisko programistyczne Java skonfigurowane na Twoim komputerze.
-  Zainstalowana biblioteka Aspose.Imaging for Java. Można go pobrać z[Aspose.Imaging dla witryny Java](https://releases.aspose.com/imaging/java/).
- Podstawowa znajomość programowania w języku Java.

## Importowanie pakietów

Zacznij od zaimportowania niezbędnych pakietów do projektu Java. Na początku kodu możesz dodać następujące instrukcje importu:

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

Podzielmy teraz przykład na przewodnik krok po kroku:

## Krok 1: Określ rozmiar obrazu i opcje Tiff

Najpierw zdefiniuj katalog, w którym będzie przechowywany obraz, i utwórz prostokąt, aby określić rozmiar obrazu. W tym przykładzie używamy obrazu Tiff z pewnymi opcjami.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## Krok 2: Utwórz nowy obraz

Teraz utwórz nowy obraz z określonymi opcjami. Ten obraz będzie używany do przechowywania metadanych XMP.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## Krok 3: Utwórz nagłówek i zwiastun XMP

Utwórz instancje XMP-Header i XMP-Trailer dla swoich metadanych XMP. Te nagłówki i końcówki pomagają zdefiniować strukturę metadanych.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Krok 4: Utwórz metainformacje XMP

Teraz utwórz instancję meta XMP, aby ustawić różne atrybuty. Możesz dodać informacje takie jak autor i opis.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Krok 5: Utwórz opakowanie pakietów XMP

Utwórz instancję XmpPacketWrapper zawierającą nagłówek, zwiastun i metainformacje XMP.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Krok 6: Dodaj pakiet Photoshop

Aby przechowywać informacje specyficzne dla programu Photoshop, utwórz pakiet programu Photoshop i ustaw jego atrybuty, takie jak miasto, kraj i tryb kolorów. Następnie dodaj ten pakiet do metadanych XMP.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## Krok 7: Dodaj pakiet Dublin Core

Aby uzyskać bardziej ogólne informacje, takie jak autor, tytuł i dodatkowe wartości, utwórz pakiet DublinCore i ustaw jego atrybuty. Dodaj także ten pakiet do metadanych XMP.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## Krok 8: Zaktualizuj metadane XMP w obrazie

 Zaktualizuj metadane XMP do obrazu za pomocą pliku`setXmpData` metoda.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## Krok 9: Zapisz obraz

Możesz teraz zapisać obraz z osadzonymi metadanymi XMP na dysku lub w strumieniu pamięci.

```java
    image.save(ms);
```

## Krok 10: Załaduj obraz i pobierz metadane XMP

Aby pobrać metadane XMP z obrazu, załaduj obraz ze strumienia pamięci lub dysku i uzyskaj dostęp do danych XMP.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Użyj danych pakietu...
        }
    }
}
```

Gratulacje! Pomyślnie nauczyłeś się obsługiwać dane XMP w obrazach przy użyciu Aspose.Imaging for Java. Umożliwia to przechowywanie i odzyskiwanie cennych metadanych w plikach obrazów.

## Wniosek

W tym samouczku omówiliśmy, jak pracować z metadanymi XMP w obrazach przy użyciu Aspose.Imaging for Java. Postępując zgodnie ze szczegółowym przewodnikiem, możesz łatwo osadzać i pobierać metadane w plikach obrazów, zwiększając ich zawartość informacyjną i użyteczność.

## Często zadawane pytania

### P1: Co to są metadane XMP?

O1: XMP (Extensible Metadata Platform) to standard osadzania metadanych w różnych typach plików, w tym w obrazach. Umożliwia przechowywanie informacji, takich jak autor, tytuł, opis i inne, w samym pliku.

### P2: Dlaczego metadane XMP są ważne?

Odpowiedź 2: Metadane XMP są niezbędne do organizowania i kategoryzowania zasobów cyfrowych. Pomaga w przypisywaniu własności, opisywaniu treści i dodawaniu kontekstu do plików, takich jak obrazy, czyniąc je bardziej dostępnymi i znaczącymi.

### P3: Czy mogę edytować metadane XMP po osadzeniu ich w obrazie?

O3: Tak, możesz edytować metadane XMP po osadzeniu ich w obrazie. Aspose.Imaging for Java zapewnia narzędzia do modyfikowania i aktualizowania atrybutów metadanych w razie potrzeby.

### P4: Czy Aspose.Imaging dla Java jest narzędziem darmowym?

 O4: Aspose.Imaging dla Java oferuje bezpłatną wersję próbną, ale do pełnej funkcjonalności i rozszerzonego użytkowania wymagana jest płatna licencja. Możesz zapoznać się z opcjami na stronie[Aspose.Imaging dla witryny Java](https://purchase.aspose.com/buy).

### P5: Gdzie mogę uzyskać pomoc i wsparcie dla Aspose.Imaging for Java?

 O5: Jeśli napotkasz jakiekolwiek problemy lub masz pytania związane z Aspose.Imaging for Java, możesz odwiedzić stronę[Fora Aspose.Imaging](https://forum.aspose.com/) o wsparcie i wskazówki społeczności.



## Kompletny kod źródłowy
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Określ rozmiar obrazu, definiując prostokąt
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// utwórz zupełnie nowy obraz tylko do celów przykładowych
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// utwórz instancję nagłówka XMP
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// utwórz instancję Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// utwórz instancję metaklasy XMP, aby ustawić różne atrybuty
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	//utwórz instancję XmpPacketWrapper zawierającą wszystkie metadane
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// utwórz instancję pakietu Photoshop i ustaw atrybuty Photoshopa
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// dodaj pakiet Photoshopa do metadanych XMP
	xmpData.addPackage(photoshopPackage);
	// utwórz instancję pakietu DublinCore i ustaw atrybuty dublinCore
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// dodaj pakiet dublinCore do metadanych XMP
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// zaktualizuj metadane XMP do obrazu
	image.setXmpData(xmpData);
	// Zapisz obraz na dysku lub w strumieniu pamięci
	image.save(ms);
	// Załaduj obraz ze strumienia pamięci lub z dysku, aby odczytać/pobrać metadane
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Pobieranie metadanych XMP
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Użyj danych pakietu...
		}
	}
}
        
```
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
