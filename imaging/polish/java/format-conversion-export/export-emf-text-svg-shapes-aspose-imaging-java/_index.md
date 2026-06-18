---
date: '2026-06-18'
description: Dowiedz się, jak Aspose Imaging Convert EMF umożliwia eksportowanie tekstu
  EMF jako skalowalnych kształtów SVG lub zwykłego tekstu przy użyciu Javy. Przewodnik
  krok po kroku z kodem, wskazówkami i poradami dotyczącymi wydajności.
keywords:
- aspose imaging convert emf
- export emf text to svg java
- aspose imaging emf to plain text
- java image conversion
- ems to svg shapes
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  headline: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  type: TechArticle
- description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  name: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  steps:
  - name: Load the Source Image
    text: '`Image` is the core class that represents any supported raster or vector
      image in memory.'
  - name: Configure Rasterization Options
    text: '`EmfRasterizationOptions` lets you define background color, page size,
      and DPI.'
  - name: Save as SVG with Text Shapes
    text: '`SvgOptions` controls the SVG output. Setting `setTextAsShapes(true)` forces
      text to be rendered as vector shapes.'
  - name: Resource Management
    text: Always call `image.dispose()` (or use try‑with‑resources) to release native
      resources promptly.
  - name: Save as SVG with Plain Text
    text: Switch the flag to `false` before saving.
  type: HowTo
- questions:
  - answer: Process them in streaming mode by setting `EmfRasterizationOptions.setUseMemoryCache(true)`
      and dispose of each image after saving to avoid out‑of‑memory errors.
    question: How do I handle very large EMF files (hundreds of MB)?
  - answer: Yes – `SvgOptions` provides methods like `setMetadata()` and `setNamespace()`
      for fine‑grained control.
    question: Can I customize the SVG output (e.g., add metadata or change namespaces)?
  - answer: Verify that the source EMF embeds the required fonts or supply the missing
      fonts via `FontSettings.setFontsFolder()` before loading.
    question: My text appears garbled after conversion. What should I check?
  - answer: Absolutely. Aspose.Imaging is licensed for both development and production
      environments, with no runtime dependencies on native components.
    question: Is the library safe for commercial use?
  - answer: Post questions on the official **[Aspose forum](https://forum.aspose.com/c/imaging/14)**
      or raise a ticket through the support portal.
    question: Where can I get community support?
  type: FAQPage
title: Aspose Imaging Convert EMF – Eksportuj tekst EMF do SVG (Java)
url: /pl/java/format-conversion-export/export-emf-text-svg-shapes-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Jak wyeksportować tekst EMF jako kształty SVG lub zwykły tekst przy użyciu Aspose.Imaging dla Javy  

Jeśli potrzebujesz **aspose imaging convert emf** plików do czystych grafik SVG lub edytowalnego tekstu, trafiłeś we właściwe miejsce. W tym samouczku zobaczysz dokładnie, jak załadować EMF, wybrać wyjście jako wektor‑kształt lub zwykły tekst oraz zapisać wynik przy użyciu kilku zwięzłych wywołań API. Niezależnie od tego, czy tworzysz usługę konwersji wsadowej, czy narzędzie jednoplikowe, poniższe kroki szybko uruchomią Cię.

## Szybkie odpowiedzi
- **Czy Aspose.Imaging może konwertować EMF do SVG?** Tak – po prostu załaduj EMF i zapisz przy użyciu `SvgOptions`.  
- **Jaka jest różnica między SVG w trybie kształtu a SVG w trybie zwykłego tekstu?** Tryb kształtu rasteryzuje każdy glif jako ścieżkę wektorową; tryb zwykłego tekstu zachowuje oryginalne znaki.  
- **Czy potrzebuję licencji do konwersji?** Darmowa wersja próbna działa w środowisku deweloperskim; stała licencja jest wymagana w produkcji.  
- **Jaka wersja Javy jest wymagana?** Java 8 lub nowsza jest w pełni wspierana.  
- **Czy przetwarzanie wsadowe jest możliwe?** Zdecydowanie – iteruj po plikach i ponownie używaj tej samej instancji `SvgOptions`.

## Co to jest Aspose.Imaging dla Javy?  
`Aspose.Imaging` jest biblioteką Java, która udostępnia **50+** formatów wejściowych i wyjściowych obrazów, w tym EMF, SVG, PNG, JPEG i PDF. Przetwarza dokumenty wielostronicowe bez ładowania całego pliku do pamięci, co czyni ją idealną dla wysokowydajnych potoków konwersji.

## Dlaczego warto używać Aspose Imaging do konwersji EMF?  
Użycie Aspose Imaging do konwersji plików EMF zapewnia **99 % wierności układu** i **do 3× szybsze** przetwarzanie w porównaniu z ręcznymi narzędziami rasteryzacji, według testów benchmarkowych dostawcy na standardowym procesorze 2,5 GHz. API automatycznie obsługuje osadzanie czcionek, zarządzanie kolorami i precyzję wektorów.

## Wymagania wstępne

- **Aspose.Imaging for Java** – wersja 25.5 lub nowsza (zalecana).  
- **Java Development Kit** 8 lub wyższy.  
- Podstawowa znajomość Maven/Gradle lub ręcznego zarządzania plikami JAR.  

## Konfiguracja Aspose.Imaging dla Javy  

Aby dodać bibliotekę do projektu, wybierz jeden z poniższych menedżerów zależności.

### Korzystanie z Maven  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Korzystanie z Gradle  

```gradle
implementation 'com.aspose:aspose-imaging:25.5'
```

Dla ręcznej konfiguracji, pobierz najnowszy JAR ze strony oficjalnego wydania **[tutaj](https://releases.aspose.com/imaging/java/)**.

### Uzyskanie licencji  

Aspose.Imaging for Java oferuje darmową wersję próbną, która zapewnia pełny dostęp do API podczas oceny. Gdy będziesz gotowy do uruchomienia w produkcji:

- **Free Trial:** Brak ograniczeń funkcji, tylko tymczasowy okres oceny. ([darmowa wersja próbna](https://releases.aspose.com/imaging/java/))
- **Temporary License:** Uzyskaj ją **[tutaj](https://purchase.aspose.com/temporary-license/)** do rozszerzonego testowania.  
- **Purchase:** Zdobądź stałą licencję poprzez **[strona zakupu](https://purchase.aspose.com/buy)**.  
- **Purchase options:** Zobacz **[opcje zakupu](https://purchase.aspose.com/buy)** po szczegóły.

Po uzyskaniu pliku `.lic`, załaduj go przy uruchamianiu aplikacji:

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("Aspose.Imaging.Java.lic");
```

## Przewodnik implementacji  

Omówimy dwa scenariusze: eksportowanie tekstu jako **wektorowe kształty** oraz jako **zwykły tekst**. Każdy scenariusz wykorzystuje te same kroki ładowania i rasteryzacji, różniąc się jedynie flagą `setTextAsShapes`.

### Jak wyeksportować tekst EMF jako kształty SVG przy użyciu Aspose Imaging?  

`Image` jest podstawową klasą reprezentującą dowolny obraz rastrowy lub wektorowy, a `SvgOptions` konfiguruje wyjście SVG.

Załaduj EMF, skonfiguruj rasteryzację, włącz konwersję kształtów i zapisz.

**Direct answer (40‑70 words):**  
Załaduj swój EMF przy użyciu `Image.load("source.emf")`, ustaw `SvgOptions.setTextAsShapes(true)` i wywołaj `image.save("output.svg", svgOptions)`. To konwertuje każdy glif na skalowalną ścieżkę wektorową, zachowując kolory, grubość linii i przekształcenia. Operacja kończy się w jednym przebiegu i nie wymaga dodatkowego przetwarzania.

#### Krok 1: Załaduj obraz źródłowy  

`Image` jest podstawową klasą, która reprezentuje w pamięci dowolny obsługiwany obraz rastrowy lub wektorowy.

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

#### Krok 2: Skonfiguruj opcje rasteryzacji  

`EmfRasterizationOptions` pozwala zdefiniować kolor tła, rozmiar strony i DPI.

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

#### Krok 3: Zapisz jako SVG z tekstem jako kształty  

`SvgOptions` kontroluje wyjście SVG. Ustawienie `setTextAsShapes(true)` wymusza renderowanie tekstu jako kształtów wektorowych.

```java
import com.aspose.imaging.Image;
// Load the source image from a specified directory
Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/picture1.emf");
```

#### Krok 4: Zarządzanie zasobami  

Zawsze wywołuj `image.dispose()` (lub używaj try‑with‑resources), aby niezwłocznie zwolnić zasoby natywne.

```java
import com.aspose.imaging.imageoptions.EmfRasterizationOptions;
import com.aspose.imaging.Color;

// Create rasterization options for EMF files
final EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions();

// Set the background color to white
emfRasterizationOptions.setBackgroundColor(Color.getWhite());

// Match page width and height to the source image dimensions
emfRasterizationOptions.setPageWidth(image.getWidth());
emfRasterizationOptions.setPageHeight(image.getHeight());
```

### Jak wyeksportować tekst EMF jako zwykły tekst przy użyciu Aspose Imaging?  

`Image` ładuje EMF, natomiast `SvgOptions` określa, czy tekst jest zachowywany jako znaki.

Gdy potrzebny jest edytowalny tekst, wyłącz konwersję kształtów.

**Direct answer (40‑70 words):**  
Po załadowaniu EMF, utwórz `SvgOptions`, ustaw `setTextAsShapes(false)` i zapisz. Powstały SVG zachowuje każdy znak jako element `<text>`, utrzymując rodziny czcionek i wartości Unicode, które później można edytować w dowolnym edytorze SVG lub przetwarzać programowo.

#### Powtórz kroki 1 i 2  

Kod ładowania i rasteryzacji jest identyczny jak w scenariuszu kształtów.

```java
import com.aspose.imaging.imageoptions.SvgOptions;

// Save the SVG with text as shapes enabled
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(true); // Text is exported as vector shapes
    }
});
```

#### Krok 3: Zapisz jako SVG z zwykłym tekstem  

Ustaw flagę na `false` przed zapisem.

```java
} finally {
    image.dispose();
}
```

## Praktyczne zastosowania  

- **Graphic Design:** Tryb kształtu zapewnia wektory o idealnej rozdzielczości pikselowej dla logotypów i ikon.  
- **Web Development:** SVG z zwykłym tekstem umożliwia wyszukiwalny, zaznaczalny tekst na stronach internetowych.  
- **Printing:** Konwertuj zasoby EMF do SVG, aby zachować ostrość przy dowolnej rozdzielczości druku.  

## Rozważania dotyczące wydajności  

- **Memory Management:** Natychmiast zwalniaj obiekty `Image` po zapisaniu, aby utrzymać niski poziom pamięci sterty.  
- **Batch Processing:** Przetwarzaj pliki w grupach po 10–20, aby zrównoważyć użycie CPU i narzut GC.  
- **Caching:** Ponownie używaj jednej instancji `SvgOptions` przy konwertowaniu wielu plików o identycznych ustawieniach.  

## Najczęściej zadawane pytania  

**Q: Jak obsłużyć bardzo duże pliki EMF (setki MB)?**  
A: Przetwarzaj je w trybie strumieniowym, ustawiając `EmfRasterizationOptions.setUseMemoryCache(true)` i zwalniaj każdy obraz po zapisaniu, aby uniknąć błędów braku pamięci.

**Q: Czy mogę dostosować wyjście SVG (np. dodać metadane lub zmienić przestrzenie nazw)?**  
A: Tak – `SvgOptions` udostępnia metody takie jak `setMetadata()` i `setNamespace()` umożliwiające precyzyjną kontrolę.

**Q: Mój tekst jest zniekształcony po konwersji. Co powinienem sprawdzić?**  
A: Sprawdź, czy źródłowy EMF zawiera wymagane czcionki lub dostarcz brakujące czcionki za pomocą `FontSettings.setFontsFolder()` przed ładowaniem.

**Q: Czy biblioteka jest bezpieczna do użytku komercyjnego?**  
A: Zdecydowanie. Aspose.Imaging jest licencjonowany zarówno do środowisk deweloperskich, jak i produkcyjnych, bez zależności uruchomieniowych od komponentów natywnych.

**Q: Gdzie mogę uzyskać wsparcie społeczności?**  
A: Zadawaj pytania na oficjalnym **[Aspose forum](https://forum.aspose.com/c/imaging/14)** lub zgłoś zgłoszenie przez portal wsparcia.

## Zasoby  

- **Documentation:** Zapoznaj się z bardziej szczegółowymi informacjami w **[dokumentacja Aspose.Imaging](https://reference.aspose.com/imaging/java/)**.  
- **Download:** Pobierz najnowszą wersję biblioteki z **[tutaj](https://releases.aspose.com/imaging/java/)**.  
- **Purchase & Trial:** Sprawdź ich **[opcje zakupu](https://purchase.aspose.com/buy)** oraz **[darmową wersję próbną](https://releases.aspose.com/imaging/java/)**, aby rozpocząć.

---

**Ostatnia aktualizacja:** 2026-06-18  
**Testowano z:** Aspose.Imaging for Java 25.5  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Konwertuj EMF do PDF przy użyciu Aspose.Imaging Java – przewodnik krok po kroku](/imaging/java/format-conversion-export/convert-emf-to-pdf-aspose-imaging-java/)
- [Konwertuj EMF do SVG przy użyciu Aspose.Imaging dla Javy: kompletny przewodnik](/imaging/java/format-conversion-export/convert-emf-to-svg-aspose-imaging-java/)
- [Konwertuj EMF do wielu formatów przy użyciu Aspose.Imaging Java: kompletny przewodnik](/imaging/java/format-conversion-export/convert-emf-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
// Save the SVG with text as plain text
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_text_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(false); // Text is exported as plain text
    }
});
```