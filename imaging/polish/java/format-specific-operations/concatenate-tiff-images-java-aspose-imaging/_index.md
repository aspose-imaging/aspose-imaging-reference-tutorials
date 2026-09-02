---
date: '2026-09-02'
description: Dowiedz się, jak scalać wiele plików tiff w Javie przy użyciu Aspose.Imaging.
  Ten przewodnik pokazuje także, jak łączyć pliki tiff oraz dodać zależność Maven
  Aspose Imaging.
keywords:
- combine multiple tiff files
- how to concatenate tiff
- maven aspose imaging dependency
lastmod: '2026-09-02'
og_description: Dowiedz się, jak scalać wiele plików tiff w Javie przy użyciu Aspose.Imaging.
  Ten przewodnik krok po kroku wyjaśnia także, jak łączyć pliki tiff oraz dodać zależność
  Maven Aspose Imaging.
og_image_alt: Guide showing Java code to combine multiple TIFF files using Aspose.Imaging
og_title: Scalanie wielu plików tiff przy użyciu Aspose.Imaging dla Java
schemas:
- author: Aspose
  dateModified: '2026-09-02'
  description: Learn how to combine multiple tiff files in Java using Aspose.Imaging.
    This guide also shows how to concatenate tiff and add the Maven Aspose Imaging
    dependency.
  headline: Combine multiple tiff files with Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to combine multiple tiff files in Java using Aspose.Imaging.
    This guide also shows how to concatenate tiff and add the Maven Aspose Imaging
    dependency.
  name: Combine multiple tiff files with Aspose.Imaging for Java
  steps:
  - name: import required classes
    text: '`TiffOptions` defines the output format and compression settings for a
      TIFF file. `TiffImage` represents a multi‑frame TIFF that you can add frames
      to. `Image.load` loads an image from a file path into an Aspose.Imaging object.'
  - name: define paths and configure options
    text: First, create a `TiffOptions` instance and set the desired compression.
      Then, instantiate a `TiffImage` with those options.
  - name: load, concatenate, and save
    text: 'Loop through each source file, open it with `Image.load`, extract its frames,
      and add them to the output image via `addFrame`. Finally, save the combined
      image using `save`. **Key configuration options explained** - `BitsPerSample`:
      controls the bit depth of each channel (typically 8 for standard TI'
  type: HowTo
- questions:
  - answer: Yes, it supports over 70 formats including JPEG, PNG, BMP, GIF, and WebP,
      allowing seamless conversion between them.
    question: Does Aspose.Imaging support other image formats besides TIFF?
  - answer: The library is platform‑independent; just ensure the JDK and Maven are
      installed on the server.
    question: Can I run this code on a Linux server?
  - answer: Purchase a license from the Aspose store; then place the license file
      in your project and load it with `License license = new License(); license.setLicense("Aspose.Imaging.lic");`.
    question: How do I obtain a permanent license for production?
  type: FAQPage
tags:
- combine tiff
- Aspose.Imaging
- Java image processing
- TIFF concatenation
title: Scalanie wielu plików tiff przy użyciu Aspose.Imaging dla Java
url: /pl/java/format-specific-operations/concatenate-tiff-images-java-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Scalanie wielu plików TIFF przy użyciu Aspose.Imaging dla Javy

## Wprowadzenie
Jeśli potrzebujesz **scalić wiele plików TIFF** w jeden dokument wieloklatkowy, zachowując każdy klatkę w niezmienionej formie, trafiłeś we właściwe miejsce. Ten samouczek przeprowadzi Cię przez cały proces z Aspose.Imaging dla Javy, obejmując wszystko od konfiguracji Maven po wskazówki dotyczące wydajności. Po zakończeniu będziesz w stanie szybko i niezawodnie łączyć obrazy TIFF w dowolnej aplikacji Java.

## Szybkie odpowiedzi
- **Jaką bibliotekę używać do łączenia TIFF?** Aspose.Imaging dla Javy.  
- **Ile linii kodu jest potrzebnych?** Około 20 linii dla podstawowej implementacji.  
- **Jakie narzędzie budowania jest zalecane?** Maven, używając `maven aspose imaging dependency`.  
- **Czy można przetwarzać duże, wielogigabajtowe pliki TIFF?** Tak – Aspose.Imaging strumieniuje dane bez ładowania całego pliku do pamięci.  
- **Czy wymagana jest licencja do produkcji?** Pełna licencja usuwa ograniczenia wersji próbnej i odblokowuje wszystkie funkcje.

## Co to jest Aspose.Imaging?
`Aspose.Imaging` to biblioteka Java, która zapewnia programowy dostęp do ponad 70 formatów obrazu, w tym TIFF, JPEG, PNG i BMP. Umożliwia odczyt, edycję, konwersję i łączenie obrazów bez polegania na natywnych bibliotekach systemu operacyjnego. Biblioteka jest regularnie aktualizowana; najnowsze wersje znajdziesz na stronie [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

## Dlaczego scalać wiele plików TIFF?
Scalanie klatek TIFF zmniejsza nakład zarządzania plikami, poprawia efektywność archiwizacji i umożliwia operacje wsadowe, takie jak OCR czy ekstrakcja metadanych. Aspose.Imaging może połączyć do 10 000 klatek w jednym pliku, utrzymując zużycie pamięci poniżej 200 MB, dzięki architekturze strumieniowej.

## Wymagania wstępne
- **Java Development Kit (JDK):** wersja 8 lub nowsza.  
- **IDE:** IntelliJ IDEA, Eclipse lub dowolny edytor, którego używasz.  
- **Podstawowa znajomość Javy:** powinieneś być zaznajomiony z Mavenem i standardową składnią Javy.

## Konfiguracja Aspose.Imaging dla Javy
Aby rozpocząć korzystanie z Aspose.Imaging dla Javy, musisz dodać ją do swojego projektu. Oto metody dodania tej potężnej biblioteki:

**Maven**  
Dodaj następującą zależność do swojego `pom.xml`:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle**  
Umieść tę linię w swoim `build.gradle`:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

**Bezpośrednie pobranie**  
Alternatywnie pobierz najnowszą wersję z [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/). Szczegółowe instrukcje użycia dostępne są w oficjalnej [Documentation](https://reference.aspose.com/imaging/java/).

### Kroki uzyskania licencji
- **Bezpłatna wersja próbna:** Rozpocznij od wersji próbnej, aby przetestować funkcje Aspose.Imaging. Zobacz stronę [Free Trial](https://releases.aspose.com/imaging/java/).  
- **Licencja tymczasowa:** Uzyskaj tymczasową licencję na rozszerzone testy bez ograniczeń poprzez stronę [Temporary License](https://purchase.aspose.com/temporary-license/).  
- **Zakup:** Do użytku produkcyjnego rozważ zakup licencji na stronie [Purchase License](https://purchase.aspose.com/buy).

## Jak dodać zależność Maven Aspose Imaging?
Dodaj artefakt Aspose.Imaging Maven do swojego `pom.xml`. Ta pojedyncza zależność pobiera wszystkie niezbędne biblioteki i utrzymuje projekt aktualny. Po zapisaniu pliku uruchom `mvn clean install`, aby pobrać pakiet. Biblioteka jest gotowa do użycia w Twoim kodzie.

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>23.12</version>
</dependency>
```

## Jak scalić pliki TIFF?
Wczytaj każdy źródłowy plik TIFF, przeiteruj jego klatki i dołącz je do nowego obiektu `TiffImage`. Poniższe kroki pokazują dokładny przebieg i utrzymują niskie zużycie pamięci nawet przy bardzo dużych plikach źródłowych.

### Implementacja krok po kroku

#### Krok 1: import wymaganych klas
`TiffOptions` definiuje format wyjściowy i ustawienia kompresji dla pliku TIFF. `TiffImage` reprezentuje wieloklatkowy TIFF, do którego możesz dodawać klatki. `Image.load` wczytuje obraz z podanej ścieżki pliku do obiektu Aspose.Imaging.  
```java
import com.aspose.imaging.Image;
import com.aspose.imaging.ImageOptionsBase;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.enums.TiffCompression;
import com.aspose.imaging.fileformats.tiff.enums.TiffPhotometric;
import com.aspose.imaging.fileformats.tiff.enums.TiffOrientation;
import com.aspose.imaging.fileformats.tiff.enums.TiffPlanarConfiguration;
import com.aspose.imaging.fileformats.tiff.enums.TiffResolutionUnit;
import com.aspose.imaging.fileformats.tiff.enums.TiffSampleFormat;
import com.aspose.imaging.fileformats.tiff.enums.TiffTags;
import com.aspose.imaging.fileformats.tiff.tiffoptions.TiffOptions;
```

#### Krok 2: określenie ścieżek i konfiguracja opcji
Najpierw utwórz instancję `TiffOptions` i ustaw żądaną kompresję. Następnie zainicjuj `TiffImage` z tymi opcjami.  
```java
String[] sourceFiles = { "page1.tif", "page2.tif", "page3.tif" };
String outputFile = "combined.tif";

TiffOptions tiffOptions = new TiffOptions(TiffCompression.LZW);
tiffOptions.setPhotometric(TiffPhotometric.RGB);
tiffOptions.setOrientation(TiffOrientation.TOP_LEFT);
tiffOptions.setPlanarConfiguration(TiffPlanarConfiguration.CHUNKY);
tiffOptions.setResolutionUnit(TiffResolutionUnit.INCH);
tiffOptions.setXResolution(300);
tiffOptions.setYResolution(300);
```

#### Krok 3: wczytanie, scalenie i zapis
Iteruj przez każdy plik źródłowy, otwórz go za pomocą `Image.load`, wyodrębnij jego klatki i dodaj je do obrazu wyjściowego metodą `addFrame`. Na koniec zapisz połączony obraz przy użyciu `save`.  
```java
try (TiffImage outputImage = (TiffImage) Image.create(tiffOptions, 0, 0)) {
    for (String filePath : sourceFiles) {
        try (Image srcImage = Image.load(filePath)) {
            for (int i = 0; i < srcImage.getFrames().size(); i++) {
                outputImage.addFrame(srcImage.getFrames().get(i).clone());
            }
        }
    }
    outputImage.save(outputFile);
}
```

**Wyjaśnienie kluczowych opcji konfiguracyjnych**
- `BitsPerSample`: kontroluje głębię bitową każdego kanału (zwykle 8 dla standardowych TIFF).  
- `Orientation`: zapewnia prawidłowe wyświetlanie obrazu we wszystkich przeglądarkach.  
- `Photometric`: określa sposób interpretacji danych pikseli (RGB, CMYK itp.).  
- `Compression`: LZW zapewnia bezstratną kompresję przy dobrym zmniejszeniu rozmiaru.

## Wskazówki rozwiązywania problemów
- Sprawdź, czy wszystkie ścieżki plików są poprawne i czy aplikacja ma uprawnienia do odczytu.  
- Jeśli napotkasz `OutOfMemoryError`, zwiększ rozmiar sterty JVM (`-Xmx2g`) lub przetwarzaj pliki w mniejszych partiach.  
- Upewnij się, że wersja zależności Maven odpowiada wersji biblioteki w czasie wykonywania, aby uniknąć `NoClassDefFoundError`.

## Praktyczne zastosowania
1. **Obrazowanie medyczne:** Scalaj kolejne skany w jeden zgodny z DICOM TIFF, aby ułatwić przeglądanie.  
2. **Archiwizacja:** Połącz zeskanowane strony historycznych dokumentów w jeden wielostronicowy TIFF do długoterminowej konserwacji.  
3. **Badania naukowe:** Agreguj klatki mikroskopii poklatkowej w jeden plik do analizy wsadowej.

## Rozważania dotyczące wydajności
- **Zarządzanie pamięcią:** Aspose.Imaging strumieniuje dane obrazu, więc możesz obsługiwać pliki większe niż dostępna pamięć RAM.  
- **Przetwarzanie wsadowe:** Grupuj pliki w logiczne partie (np. 100 klatek na partię), aby utrzymać przewidywalny czas przetwarzania.  
- **Wykonanie asynchroniczne:** Owiń logikę scalania w `CompletableFuture`, aby interfejs użytkownika pozostawał responsywny w aplikacjach desktopowych.

## Podsumowanie
Masz teraz kompletną, gotową do produkcji metodę **scalania wielu plików TIFF** przy użyciu Aspose.Imaging dla Javy. Eksperymentuj z różnymi typami kompresji, odkrywaj dodatkowe funkcje przetwarzania obrazu i integruj ten przepływ pracy w większych systemach zarządzania dokumentami.

## Sekcja FAQ

1. **Jakie są wymagania wstępne do używania Aspose.Imaging Java?**  
   Potrzebujesz JDK 8+ oraz podstawowej znajomości Javy; zalecane jest IDE obsługujące Maven.

2. **Czy mogę używać Aspose.Imaging bez licencji?**  
   Tak, dostępna jest wersja próbna, ale nakłada ona ograniczenia, takie jak znaki wodne i limit liczby stron.

3. **Jak efektywnie obsługiwać duże pliki TIFF?**  
   Skorzystaj z API strumieniowego biblioteki, zwiększ stertę JVM w razie potrzeby i przetwarzaj pliki w partiach.

4. **Czy można dostosować typ kompresji w obrazach TIFF?**  
   Oczywiście – ustaw `TiffOptions.setCompression` na `LZW`, `CCITT4`, `Deflate` lub `None` według potrzeb.

5. **Jakie typowe problemy pojawiają się przy scalaniu klatek TIFF?**  
   Nieprawidłowe ścieżki plików, niezgodne wymiary obrazów lub nieobsługiwane przestrzenie kolorów mogą powodować błędy; zawsze weryfikuj pliki źródłowe przed łączeniem.

**Dodatkowe Q&A**

**P: Czy Aspose.Imaging obsługuje inne formaty obrazów poza TIFF?**  
O: Tak, obsługuje ponad 70 formatów, w tym JPEG, PNG, BMP, GIF i WebP, umożliwiając płynną konwersję między nimi.

**P: Czy mogę uruchomić ten kod na serwerze Linux?**  
O: Biblioteka jest niezależna od platformy; wystarczy, że na serwerze będą zainstalowane JDK i Maven.

**P: Jak uzyskać stałą licencję do produkcji?**  
O: Kup licencję w sklepie Aspose; następnie umieść plik licencji w projekcie i załaduj go przy pomocy `License license = new License(); license.setLicense("Aspose.Imaging.lic");`.

**Wsparcie**  
Jeśli potrzebujesz dalszej pomocy, odwiedź [Support Forum](https://forum.aspose.com/c/imaging/14).

**Ostatnia aktualizacja:** 2026-09-02  
**Testowane z:** Aspose.Imaging 23.12 dla Javy  
**Autor:** Aspose  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```
```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path/to/Aspose.Total.Java.lic");
```
```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.TiffOptions;
```
```java
String dataDir = "YOUR_DOCUMENT_DIRECTORY";
List<String> files = Arrays.asList(dataDir + "TestDemo.tiff", dataDir + "sample.tiff");

TiffOptions createOptions = new TiffOptions(TiffExpectedFormat.Default);
createOptions.setBitsPerSample(new int[]{1});
createOptions.setOrientation(TiffOrientations.TopLeft);
createOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
createOptions.setCompression(TiffCompressions.CcittFax3);
createOptions.setFillOrder(TiffFillOrders.Lsb2Msb);
```
```java
List<TiffImage> images = new ArrayList<>();
TiffImage output = null;
try {
    for (String file : files) {
        TiffImage input = (TiffImage) Image.load(file);
        images.add(input);

        for (TiffFrame frame : input.getFrames()) {
            if (output == null) {
                output = new TiffImage(TiffFrame.copyFrame(frame));
            } else {
                output.addFrame(TiffFrame.copyFrame(frame));
            }
        }
    }

    if (output != null) {
        String outputPath = "YOUR_OUTPUT_DIRECTORY" + "/ConcatenateTiffImagesHavingSeveralFrames_out.tif";
        output.save(outputPath, createOptions);
    }
} finally {
    for (TiffImage image : images) {
        image.close();
    }
}
```

## Powiązane samouczki

- [How to Create Multi-Page TIFF with Aspose.Imaging for Java – A Complete Guide](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Load TIFF Images in Java with Aspose.Imaging: Complete Guide](/imaging/java/image-loading-saving/load-tiff-image-aspose-imaging-java-guide/)
- [How to Combine Images Using Aspose.Imaging in Java: A Complete Guide](/imaging/java/image-creation-drawing/combine-images-aspose-imaging-java-tutorial/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}