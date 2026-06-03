---
date: 2026-01-09
description: Dowiedz się, jak binaryzować obraz przy użyciu Aspose.Imaging dla Javy.
  Ten przewodnik obejmuje techniki przetwarzania obrazu w Javie dotyczące konwersji
  DICOM do BMP.
linktitle: Bradley's Adaptive Threshold Binarization
second_title: Aspose.Imaging Java Image Processing API
title: Jak binaryzować obraz przy użyciu Aspose.Imaging dla Javy
url: /pl/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Jak binaryzować obraz przy użyciu Aspose.Imaging dla Javy

Obrazy odgrywają kluczową rolę w świecie cyfrowym, zarówno na stronach internetowych, w dokumentach, jak i jako część różnych aplikacji. Jeśli zastanawiasz się **jak binaryzować obraz** efektywnie, szczególnie w formatach medycznych takich jak DICOM, trafiłeś we właściwe miejsce. Binaryzacja obrazu upraszcza go, przekształcając w czarno‑białą reprezentację, co jest idealne do dalszej analizy, OCR lub optymalizacji przechowywania. W tym samouczku przeprowadzimy cały proces przy użyciu Bradley’s Adaptive Threshold Binarization z Aspose.Imaging dla Javy.

## Szybkie odpowiedzi
- **Co robi binaryzacja?** Przekształca każdy piksel w czarny lub biały na podstawie progu.
- **Która biblioteka jest najlepsza do przetwarzania obrazów w Javie?** Aspose.Imaging dla Javy oferuje solidne funkcje w wersji próbnej bez licencji.
- **Czy mogę przetwarzać pliki DICOM bezpośrednio?** Tak, Aspose.Imaging potrafi wczytać DICOM i wyeksportować BMP, PNG itp.
- **Czy potrzebna jest licencja do produkcji?** Licencja komercyjna jest wymagana do użytku nie‑próbnego.
- **Jaką wersję Javy obsługuje?** Java 8 i nowsze są w pełni kompatybilne.

## Co to jest binaryzacja obrazu?
Binaryzacja obrazu to proces przekształcania obrazu w odcieniach szarości lub kolorowego w obraz binarny, w którym każdy piksel ma wartość 0 (czarny) lub 255 (biały). Ten krok jest często pierwszym etapem w pipeline’ach przetwarzania obrazów medycznych, skanowania dokumentów i zadań komputerowego widzenia.

## Dlaczego warto używać Aspose.Imaging dla Javy?
Aspose.Imaging oferuje czysto‑Java API, które **wczytuje DICOM**, stosuje zaawansowane algorytmy takie jak **Bradley’s Adaptive Threshold** i zapisuje wynik w popularnych formatach bez potrzeby zewnętrznych bibliotek natywnych. Jest to idealne rozwiązanie dla **przetwarzania obrazów medycznych**, **konwersji DICOM do BMP** oraz innych przepływów pracy opartych na Javie.

## Wymagania wstępne

Zanim przejdziesz do kodu, upewnij się, że masz następujące elementy:

- **Środowisko programistyczne Java** – zainstalowany JDK 8 lub nowszy.
- **Aspose.Imaging dla Javy** – pobierz ze strony: [Download Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/).
- **Obraz DICOM** – dowolny przykładowy plik DICOM, który chcesz binaryzować.

Teraz, gdy wszystko jest gotowe, przejdźmy do implementacji.

## Jak binaryzować obraz – przewodnik krok po kroku

### Importowanie pakietów
Najpierw zaimportuj wymagane klasy Aspose.Imaging. Ten fragment definiuje także ścieżki wejściowe i wyjściowe.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// Load a DICOM image in an instance of DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Binarize image with Bradley's adaptive threshold.
    image.binarizeBradley(10);
    // Save the resultant image.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

### Krok 1: Definiowanie ścieżek
Ustaw lokalizacje dla swojego źródłowego pliku DICOM oraz docelowego pliku BMP. Zastąp `"Your Document Directory"` rzeczywistym folderem w swoim systemie.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

### Krok 2: Wczytanie obrazu DICOM
Użyj Aspose.Imaging, aby **wczytać obraz DICOM** do obiektu `DicomImage`. Obiekt ten daje pełny dostęp do danych pikseli i metod przetwarzania.

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // The image processing steps will go here.
}
```

### Krok 3: Wykonanie binaryzacji
Zastosuj algorytm Bradley’s Adaptive Threshold. Parametr (`10` w tym przykładzie) kontroluje czułość progu; możesz eksperymentować z różnymi wartościami, aby uzyskać optymalne wyniki.

```java
image.binarizeBradley(10);
```

### Krok 4: Zapis binaryzowanego obrazu
Na koniec wyeksportuj przetworzony obraz. Tutaj używamy formatu BMP, ale Aspose.Imaging obsługuje PNG, JPEG, TIFF i wiele innych.

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## Typowe problemy i rozwiązywanie

- **FileNotFoundException** – Upewnij się, że ścieżka `dataDir` kończy się ukośnikiem i nazwa pliku DICOM jest dokładnie taka sama.
- **OutOfMemoryError** – Duże pliki DICOM mogą wymagać zwiększenia rozmiaru sterty JVM (`-Xmx2g` lub więcej).
- **Nieprawidłowy próg** – Jeśli wynik jest zbyt ciemny lub zbyt jasny, dostosuj liczbę przekazywaną do `binarizeBradley()` (np. 5‑15).

## Najczęściej zadawane pytania

### Q1: Co to jest DICOM i dlaczego jest ważny w obrazowaniu medycznym?
**A:** DICOM oznacza Digital Imaging and Communications in Medicine. To uniwersalny standard przechowywania, transmisji i obsługi obrazów medycznych, umożliwiający interoperacyjność między urządzeniami i systemami.

### Q2: Czy mogę używać Aspose.Imaging dla Javy w projektach komercyjnych?
**A:** Tak, Aspose.Imaging dla Javy oferuje zarówno darmowe wersje próbne, jak i licencje komercyjne. Opcje możesz poznać i nabyć na [stronie Aspose](https://purchase.aspose.com/buy).

### Q3: Czy dostępne są tymczasowe licencje do testów?
**A:** Tak, możesz uzyskać tymczasową licencję do testowania i oceny Aspose.Imaging dla Javy. Odwiedź [ten link](https://purchase.aspose.com/temporary-license/) po więcej informacji.

### Q4: Gdzie mogę uzyskać pomoc lub dyskutować o problemach związanych z Aspose.Imaging dla Javy?
**A:** Wsparcie społeczności i dyskusje znajdziesz na [forum Aspose.Imaging](https://forum.aspose.com/). To świetne miejsce, aby znaleźć odpowiedzi i połączyć się z innymi użytkownikami.

### Q5: Czy Aspose.Imaging dla Javy nadaje się do przetwarzania obrazów w innych aplikacjach opartych na Javie?
**A:** Absolutnie. Biblioteka sprawdza się w aplikacjach webowych, oprogramowaniu desktopowym, narzędziach batch‑processing i nie tylko, zapewniając spójne API na różnych platformach.

## Podsumowanie
Właśnie nauczyłeś się **jak binaryzować obraz** przy użyciu Aspose.Imaging dla Javy z algorytmem Bradley’s Adaptive Threshold. Technika ta jest szczególnie cenna w **przetwarzaniu obrazów medycznych**, pozwalając konwertować pliki DICOM na lekkie formaty BMP (lub inne) do analizy lub przechowywania. Eksperymentuj z różnymi progami i odkrywaj bogaty zestaw funkcji Aspose.Imaging.

Po głębsze zanurzenie się w manipulację obrazami, zajrzyj do oficjalnej dokumentacji: [Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/).

---

**Ostatnia aktualizacja:** 2026-01-09  
**Testowano z:** Aspose.Imaging dla Javy 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}