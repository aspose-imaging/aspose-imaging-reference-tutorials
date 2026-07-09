---
date: 2026-01-12
description: Dowiedz się, jak dostosować kontrast w obrazach DICOM – krok po kroku
  przewodnik, jak regulować kontrast przy użyciu Aspose.Imaging dla Javy i konwertować
  DICOM na BMP.
linktitle: DICOM Image Contrast Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: Jak dostosować kontrast w obrazach DICOM przy użyciu Aspose.Imaging dla Javy
url: /pl/java/image-processing-and-enhancement/dicom-image-contrast-adjustment/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Jak dostosować kontrast w obrazach DICOM przy użyciu Aspose.Imaging for Java

We współczesnej diagnostyce obrazowej **jak dostosować kontrast** może decydować o jasnej diagnozie lub przeoczeniu szczegółu. Ten samouczek przeprowadzi Cię krok po kroku przez proces regulacji kontrastu w plikach DICOM przy użyciu Aspose.Imaging for Java oraz pokaże, jak przekonwertować te obrazy DICOM do formatu BMP w celu łatwego podglądu lub dalszego przetwarzania. Po zakończeniu będziesz mieć gotowy fragment kodu, który możesz wstawić do dowolnego projektu Javy.

## Szybkie odpowiedzi
- **Co robi regulacja kontrastu?** Rozszerza zakres pomiędzy ciemnymi a jasnymi pikselami, uwydatniając struktury.
- **Jakiej biblioteki potrzebuję?** Aspose.Imaging for Java.
- **Czy mogę wyeksportować do BMP?** Tak – po regulacji kontrastu możesz przekonwertować DICOM na BMP.
- **Czy potrzebna jest licencja do produkcji?** Licencja komercyjna jest wymagana przy użyciu nie‑ewaluacyjnym.
- **Jaką wersję Javy obsługuje?** Java 8 i nowsze.

## Co to jest regulacja kontrastu i dlaczego jest ważna?
Regulacja kontrastu zwiększa wizualną różnicę pomiędzy cechami anatomicznymi, pomagając radiologom szybciej dostrzegać nieprawidłowości. W przepływie pracy z DICOM regulacja kontrastu przed konwersją zapewnia, że wyjściowy plik BMP zachowuje jakość diagnostyczną niezbędną do raportowania lub archiwizacji.

## Wymagania wstępne

Zanim przejdziesz do kodu, upewnij się, że masz:

1. **Aspose.Imaging for Java** – pobierz ją ze strony [tutaj](https://releases.aspose.com/imaging/java/).  
2. **Środowisko programistyczne Javy** – JDK 8+ oraz ulubione IDE (IntelliJ, Eclipse, VS Code itp.).  
3. **Obraz DICOM** – dowolny plik .dcm, który chcesz ulepszyć; przykładowe pliki są dostępne w internecie lub możesz użyć własnych danych klinicznych.

## Importowanie pakietów

Te importy dają dostęp do obsługi DICOM oraz funkcji zapisu BMP.

```java
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
```

## Jak dostosować kontrast w obrazach DICOM

Poniżej znajduje się kompletny, krok‑po‑kroku przepływ pracy. Każdy krok jest wyjaśniony prostym językiem, abyś mógł podążać za instrukcją nawet będąc nowicjuszem w Aspose.Imaging.

### Krok 1: Określ ścieżki plików

Ustaw lokalizację wejściowego pliku DICOM oraz żądaną ścieżkę wyjściowego pliku BMP. Zastąp placeholder rzeczywistą ścieżką na swoim komputerze.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingContrast_out.bmp";
```

### Krok 2: Załaduj obraz DICOM

Otwieramy plik DICOM przy użyciu `FileInputStream`. Blok `try‑with‑resources` zapewnia automatyczne zamknięcie strumienia.

```java
File file = new File(inputFile);

try (FileInputStream fis = new FileInputStream(file)) {
    try (DicomImage image = (DicomImage) Image.load(fis)) {
        // All further processing happens inside this block
    }
} catch (IOException ex) {
    Logger.println(ex.getMessage());
    ex.printStackTrace();
}
```

### Krok 3: Dostosuj kontrast

Wewnątrz wewnętrznego bloku `try` wywołujemy `adjustContrast`. Wartość może wynosić od **‑100** (zmniejszenie) do **+100** (zwiększenie). W tym przykładzie podnosimy kontrast o 50 jednostek.

```java
image.adjustContrast(50);
```

### Krok 4: Konwertuj DICOM na BMP i zapisz obraz

Po zmianie kontrastu tworzymy instancję `BmpOptions` i zapisujemy wynik jako plik BMP. Ten krok **konwertuje DICOM na BMP**, dając Ci szeroko wspierany format rastrowy.

```java
image.save(outputFile, new BmpOptions());
```

## Typowe problemy i wskazówki

- **Nieprawidłowy plik DICOM** – Upewnij się, że plik .dcm nie jest skompresowany przy użyciu nieobsługiwanej składni transferu. Aspose.Imaging obsługuje większość standardowych kodowań DICOM.  
- **Wartość kontrastu poza zakresem** – Wartości poza ±100 są przycinane; wybierz liczbę odpowiednią dla histogramu obrazu.  
- **Zużycie pamięci** – Duże serie DICOM mogą pochłaniać znaczną ilość RAM. Przetwarzaj pojedyncze przekroje, jeśli napotkasz `OutOfMemoryError`.

## Podsumowanie

Teraz wiesz **jak dostosować kontrast** w obrazach DICOM przy użyciu Aspose.Imaging for Java oraz **jak przekonwertować DICOM na BMP** do dalszych zadań. Ten przepływ pracy jest szybki, niezawodny i może być zintegrowany z większymi pipeline’ami obrazowania medycznego, niezależnie od tego, czy tworzysz przeglądarkę PACS, narzędzie badawcze czy zautomatyzowany system raportowania.

Aspose.Imaging for Java abstrahuje niskopoziomową obsługę DICOM, pozwalając skupić się na wartości klinicznej Twoich obrazów.

## Najczęściej zadawane pytania

**Q: Co to jest DICOM i dlaczego jest standardem w obrazowaniu medycznym?**  
A: DICOM (Digital Imaging and Communications in Medicine) to uniwersalny format do przechowywania, przesyłania i udostępniania obrazów medycznych, zapewniający interoperacyjność między urządzeniami i placówkami.

**Q: Czy mogę jednocześnie regulować jasność wraz z kontrastem?**  
A: Tak, metoda `adjustBrightness(int value)` działa podobnie i może być wywołana przed zapisem.

**Q: Czy Aspose.Imaging obsługuje inne formaty wyjściowe poza BMP?**  
A: Oczywiście – możesz eksportować do PNG, JPEG, TIFF i wielu innych, używając odpowiedniej klasy `*Options`.

**Q: Czy wymagana jest licencja komercyjna do użytku produkcyjnego?**  
A: Tak. Licencję możesz zakupić [tutaj](https://purchase.aspose.com/buy) lub uzyskać tymczasową licencję ewaluacyjną [tutaj](https://purchase.aspose.com/temporary-license/).

**Q: Gdzie mogę znaleźć więcej pomocy i przykładów?**  
A: Forum społeczności Aspose.Imaging for Java oferuje obszerną dokumentację i przykładowy kod: [Aspose.Imaging for Java forum](https://forum.aspose.com/).

---

**Ostatnia aktualizacja:** 2026-01-12  
**Testowano z:** Aspose.Imaging for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}