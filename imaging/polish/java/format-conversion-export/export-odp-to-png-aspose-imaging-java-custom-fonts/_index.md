---
date: '2026-06-28'
description: Dowiedz się, jak przekonwertować ODP na PNG przy użyciu Aspose.Imaging
  for Java, ustawić czcionki niestandardowe i wyłączyć czcionki systemowe, aby uzyskać
  dokładne renderowanie.
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
title: Jak przekonwertować ODP na PNG przy użyciu Aspose.Imaging for Java – Przewodnik
  po czcionkach niestandardowych i eksporcie
url: /pl/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Jak przekonwertować ODP na PNG przy użyciu Aspose.Imaging dla Javy – Niestandardowe czcionki i przewodnik eksportu

W nowoczesnych aplikacjach Java konwersja plików OpenDocument Presentation (ODP) na obrazy PNG wysokiej jakości jest powszechnym wymogiem — szczególnie gdy trzeba zachować identyfikację wizualną dzięki niestandardowym czcionkom. Ten samouczek pokazuje **jak przekonwertować ODP** na PNG przy użyciu Aspose.Imaging dla Javy, prowadzi przez ustawienie własnego folderu czcionek, wyłączenie czcionek zapasowych systemu oraz precyzyjne dostosowanie opcji rasteryzacji w celu uzyskania optymalnej wydajności.

**Czego się nauczysz**
- Jak ustawić własny katalog czcionek dla konwersji ODP.  
- Jak wyłączyć systemowe czcionki alternatywne, aby używane były wyłącznie wybrane fonty.  
- Jak wyeksportować plik ODP do PNG z dokładnymi wymiarami i ustawieniami czcionek.  
- Wskazówki dotyczące przyspieszenia i zmniejszenia zużycia pamięci przy przetwarzaniu dużych prezentacji.

## Szybkie odpowiedzi
- **Czy mogę użyć Maven do dodania Aspose.Imaging?** Tak, dodaj zależność Maven i uruchom `mvn install`.  
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest ważna licencja Aspose.Imaging, aby uzyskać nieograniczone użycie.  
- **Czy moje niestandardowe czcionki będą respektowane?** Ustaw folder czcionek i wyłącz systemowe alternatywy, aby je wymusić.  
- **Jakie formaty obrazu są obsługiwane?** Aspose.Imaging obsługuje ponad 120 formatów rastrowych i wektorowych, w tym PNG, JPEG, TIFF i WebP.  
- **Czy API jest wątkowo‑bezpieczne?** Tak, większość klas Aspose.Imaging jest bezpieczna przy równoczesnym użyciu, pod warunkiem tworzenia oddzielnych instancji dla każdego wątku.

## Co oznacza „how to convert odp”?
*„How to convert odp”* odnosi się do procesu przekształcania pliku OpenDocument Presentation w inny format — najczęściej PNG — przy zachowaniu układu, czcionek i wierności wizualnej. Aspose.Imaging dla Javy zapewnia jednofunkcyjną metodę, która obsługuje tę konwersję bez konieczności używania zewnętrznych narzędzi, umożliwiając deweloperom integrację konwersji bezpośrednio w aplikacjach przy minimalnym kodzie.

## Dlaczego warto używać Aspose.Imaging dla Javy?
Aspose.Imaging obsługuje **ponad 120 formatów wyjściowych** i może rasteryzować wielostronicowe pliki ODP bez ładowania całego dokumentu do pamięci, zmniejszając szczytowe zużycie RAM nawet o 70 % przy dużych prezentacjach. Biblioteka oferuje także wbudowane zarządzanie czcionkami, eliminując potrzebę używania zewnętrznych silników renderujących.

## Wymagania wstępne
- **Biblioteki**: Aspose.Imaging dla Javy ≥ 25.5.  
- **JDK**: wersja 8 lub nowsza.  
- **IDE**: IntelliJ IDEA, Eclipse lub dowolny edytor kompatybilny z Javą.  
- **Podstawowa wiedza**: Java I/O, programowanie obiektowe oraz pojęcia związane z obrazami.

## Instrukcje instalacji

### Maven
Dodaj następującą zależność do swojego `pom.xml` i uruchom `mvn clean install`:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
Umieść bibliotekę w pliku `build.gradle` i odśwież projekt:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Bezpośrednie pobranie
Pobierz najnowszy JAR z [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

## Kroki uzyskania licencji
Aby odblokować pełną funkcjonalność, zastosuj tymczasową lub stałą licencję:

1. **Bezpłatna wersja próbna** – Licencja nie jest wymagana, ograniczone funkcje.  
2. **Licencja tymczasowa** – Zamów ją na [stronie Aspose](https://purchase.aspose.com/temporary-license/).  
3. **Zakup** – Kup subskrypcję lub licencję wieczystą na [stronie zakupu Aspose](https://purchase.aspose.com/buy).

Zainicjalizuj bibliotekę przy użyciu pliku licencji:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## Jak ustawić własny katalog czcionek dla konwersji ODP?
`FontSettings` to klasa zarządzająca zasobami czcionek dla Aspose.Imaging. Załaduj własne czcionki przed rozpoczęciem jakiegokolwiek przetwarzania obrazu. Dzięki temu każdy slajd użyje dokładnie tych fontów, które dostarczysz.

Ustaw ścieżkę folderu czcionek przy pomocy `FontSettings` Aspose.Imaging:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Definicja*: `FontSettings.setFontsFolder` informuje Aspose.Imaging, gdzie szukać czcionek TrueType i OpenType w systemie plików.

## Jak wyłączyć systemowe czcionki alternatywne podczas konwersji ODP?
Wyłączenie alternatywnych czcionek systemowych zmusza silnik renderujący do ignorowania czcionek zainstalowanych w systemie operacyjnym, gwarantując, że używane będą wyłącznie czcionki dostarczone przez Ciebie. Eliminuje to nieoczekiwane podstawienia czcionek, które mogą zmienić wygląd slajdów.

Wyłącz systemowe alternatywy za pomocą następującego wywołania:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Definicja*: `FontSettings.setGetSystemAlternativeFont(false)` wymusza użycie wyłącznie czcionek znajdujących się w określonym folderze, eliminując nieprzewidziane podstawienia.

## Jak wyeksportować plik ODP do PNG z określoną czcionką?
`RasterizationOptions` definiuje, w jaki sposób strony wektorowe są rasteryzowane do obrazów bitmapowych. Łącząc konfigurację czcionek z ustawieniami rasteryzacji, możesz kontrolować DPI, kolor tła i rozmiar strony dla każdego eksportowanego pliku PNG.

Zaimplementuj metodę eksportu zgodnie z poniższym przykładem:

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

*Definicja*: Klasa `RasterizationOptions` kontroluje DPI, rozmiar strony oraz kolor tła generowanych plików PNG.

### Typowe pułapki i rozwiązania
- **Brakujące pliki czcionek** – Upewnij się, że każdy plik `.ttf` lub `.otf` odwoływany w ODP znajduje się w ustawionym folderze.  
- **Nieprawidłowe ścieżki** – Używaj ścieżek bezwzględnych lub rozwiązuj ścieżki względne względem `System.getProperty("user.dir")`.  
- **Niewystarczające uprawnienia** – Zapewnij, że proces Java ma prawo odczytu folderu czcionek i zapisu w folderze wyjściowym.

## Praktyczne zastosowania
1. **Prezentacje zgodne z marką** – Eksportuj prezentacje jako PNG do publikacji w sieci, zachowując firmowe czcionki.  
2. **Automatyczne generowanie raportów** – Konwertuj każdy slajd na obraz w celu wstawienia go do raportów PDF lub newsletterów e‑mailowych.  
3. **Tworzenie archiwów legacy** – Przechowuj zawartość ODP jako PNG, aby zapewnić przyszłą dostępność bez konieczności posiadania przeglądarek ODP.

## Rozważania dotyczące wydajności
- Korzystaj z najnowszej wersji Aspose.Imaging, aby wykorzystać ulepszenia rasteryzacji wielowątkowej (do 2× szybsze na procesorach 8‑rdzeniowych).  
- Owiń przetwarzanie obrazu w blok `try‑with‑resources`, aby zapewnić terminowe zwolnienie zasobów natywnych.  
- Dostosuj `RasterizationOptions` (np. obniż DPI) przy przetwarzaniu tysięcy slajdów, aby zrównoważyć jakość i zużycie pamięci.

## Najczęściej zadawane pytania

**P: Jaka jest minimalna wymagana wersja Javy?**  
O: Aspose.Imaging dla Javy działa z JDK 8 i nowszymi; zalecany jest JDK 11 dla długoterminowego wsparcia.

**P: Czy mogę konwertować tylko wybrane slajdy?**  
O: Tak, ustaw `rasterizationOptions.setPageNumber(specificSlideIndex)` przed wywołaniem `save`.

**P: Jak obsłużyć pliki ODP zabezpieczone hasłem?**  
O: Załaduj plik przy użyciu `LoadOptions` zawierającego hasło, a następnie kontynuuj z tymi samymi ustawieniami czcionek.

**P: Czy wyłączenie czcionek systemowych wpływa na wydajność?**  
O: Nieznacznie przyspiesza działanie, ponieważ silnik pomija wyszukiwanie czcionek systemowych, co jest szczególnie widoczne na maszynach z dużą kolekcją fontów.

**P: Gdzie mogę znaleźć więcej przykładów kodu?**  
O: Przeglądaj oficjalną [dokumentację Aspose.Imaging](https://reference.aspose.com/imaging/java/) po dodatkowe scenariusze, takie jak konwersja wsadowa i przekształcenia obrazów.

## Dodatkowe zasoby
- [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/)  
- [Start Your Free Trial](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)  
- [Aspose.Imaging Forum](https://forum.aspose.com/c/imaging/14)  
- [Buy Aspose Licensing](https://purchase.aspose.com/buy)  
- [Apply for a Temporary License](https://purchase.aspose.com/temporary-license/)  

---

**Ostatnia aktualizacja:** 2026-06-28  
**Testowano z:** Aspose.Imaging dla Javy 25.5  
**Autor:** Aspose

## Powiązane samouczki

- [Convert ODG to PNG with Aspose.Imaging for Java: A Complete Guide](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Efficient Image Conversion in Java with Aspose.Imaging: A Complete Guide](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}