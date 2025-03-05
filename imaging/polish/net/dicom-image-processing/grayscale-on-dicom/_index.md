---
title: Obrazy DICOM w skali szarości z Aspose.Imaging dla .NET
linktitle: Skala szarości w formacie DICOM w Aspose.Imaging dla .NET
second_title: Aspose.Imaging .NET API przetwarzania obrazu
description: Dowiedz się, jak przeprowadzić skalowanie szarości na obrazach DICOM za pomocą Aspose.Imaging dla .NET, potężnej biblioteki do przetwarzania obrazów.
type: docs
weight: 24
url: /pl/net/dicom-image-processing/grayscale-on-dicom/
---
Jeśli pracujesz z danymi obrazowania medycznego w formacie DICOM i musisz wykonać transformacje w skali szarości, Aspose.Imaging dla .NET oferuje potężne rozwiązanie. W tym samouczku krok po kroku przeprowadzimy Cię przez proces skalowania szarości obrazu DICOM przy użyciu Aspose.Imaging. Biblioteka ta jest wszechstronnym narzędziem umożliwiającym pracę z różnymi formatami obrazów, w tym DICOM, w środowisku .NET. Zacznijmy!

## Warunki wstępne

Zanim zaczniesz, upewnij się, że spełnione są następujące wymagania wstępne:

1.  Aspose.Imaging dla .NET: Powinieneś mieć zainstalowaną tę bibliotekę. Można go pobrać z[Strona pobierania Aspose.Imaging dla platformy .NET](https://releases.aspose.com/imaging/net/).

2. Obraz DICOM: Powinieneś mieć obraz DICOM, który chcesz przekształcić w skalę szarości. Jeśli go nie masz, możesz znaleźć przykładowe obrazy DICOM do celów testowych.

## Importuj przestrzenie nazw

Najpierw zaimportujmy niezbędne przestrzenie nazw do pracy z Aspose.Imaging:

```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

Teraz, gdy masz już wstępne wymagania i zaimportowane przestrzenie nazw, możemy krok po kroku przystąpić do procesu skalowania szarości.

## Krok 1: Zainicjuj obraz DICOM

 Zaczynamy od inicjalizacji obrazu DICOM. W tym przykładzie zakładamy, że plik DICOM nosi nazwę „file.dcm” i znajduje się w katalogu określonym przez`dataDir`.

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
```

## Krok 2: Transformacja w skali szarości

 Następnym krokiem jest przekształcenie załadowanego obrazu DICOM na jego reprezentację w skali szarości za pomocą`Grayscale()` metoda. Ta metoda automatycznie konwertuje obraz do skali szarości.

```csharp
{
    // Przekształć obraz w jego reprezentację w skali szarości
    image.Grayscale();
}
```

## Krok 3: Zapisz obraz w skali szarości

 Po przeskalowaniu obrazu w skali szarości możesz zapisać wynikowy obraz. W tym przykładzie zapisujemy go w formacie BMP za pomocą pliku`BmpOptions()`.

```csharp
image.Save(dataDir + "GrayscalingOnDICOM_out.bmp", new BmpOptions());
```

## Wniosek

tym samouczku nauczyliśmy się, jak wykonywać skalowanie szarości na obrazie DICOM przy użyciu Aspose.Imaging dla .NET. Biblioteka ta upraszcza proces pracy z danymi obrazowania medycznego i umożliwia łatwe wykonywanie różnych transformacji. Niezależnie od tego, czy pracujesz nad badaniami medycznymi, czy aplikacjami związanymi z opieką zdrowotną, Aspose.Imaging może być cennym narzędziem w zestawie narzędzi programistycznych .NET.

## Często zadawane pytania

### P1: Co to jest DICOM?

A1: DICOM oznacza cyfrowe obrazowanie i komunikację w medycynie. Jest to standard obsługi, przechowywania, drukowania i przesyłania obrazów medycznych.

### P2: Czy Aspose.Imaging nadaje się do niemedycznego przetwarzania obrazów?

Odpowiedź 2: Tak, Aspose.Imaging to wszechstronna biblioteka, która obsługuje szeroką gamę formatów obrazów do różnych zastosowań poza obrazowaniem medycznym.

### P3: Gdzie mogę znaleźć więcej dokumentacji?

 A3: Możesz odwołać się do[Dokumentacja Aspose.Imaging dla .NET](https://reference.aspose.com/imaging/net/) szczegółowe informacje i przykłady.

### P4: Czy dostępny jest bezpłatny okres próbny?

 A4: Tak, możesz uzyskać dostęp do[bezpłatna wersja próbna Aspose.Imaging](https://releases.aspose.com/) aby ocenić jego możliwości.

### P5: Jak mogę uzyskać pomoc dotyczącą Aspose.Imaging?

 A5: Jeśli masz jakieś pytania lub potrzebujesz pomocy, możesz odwiedzić stronę[Forum Aspose.Imaging](https://forum.aspose.com/) aby zwrócić się o pomoc do społeczności lub skontaktować się z jej zespołem wsparcia.