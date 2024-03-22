---
title: Binaryzacja obrazu za pomocą Aspose.Imaging dla Java
linktitle: Adaptacyjna binaryzacja progowa Bradleya
second_title: Aspose.Imaging API przetwarzania obrazu Java
description: Naucz się binaryzacji obrazów za pomocą Aspose.Imaging dla Java. Z łatwością przekształcaj obrazy DICOM. Zapoznaj się z przewodnikiem krok po kroku z przykładami kodu.
type: docs
weight: 27
url: /pl/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
---
Obrazy odgrywają kluczową rolę w cyfrowym świecie, czy to na stronach internetowych, w dokumentach, czy jako część różnych aplikacji. Przetwarzanie obrazu jest w tych dziedzinach istotnym zadaniem, a jedną z podstawowych operacji jest binaryzacja obrazu. Binaryzacja upraszcza obraz, konwertując go do postaci binarnej, co ułatwia przetwarzanie komputerom. Aspose.Imaging dla Java to potężne narzędzie, które zapewnia szeroką gamę funkcji manipulacji obrazami. W tym samouczku przyjrzymy się, jak przeprowadzić binaryzację obrazu przy użyciu adaptacyjnej binaryzacji progowej Bradleya firmy Aspose.Imaging. 

## Warunki wstępne

Zanim zagłębisz się w świat binaryzacji obrazów z Aspose.Imaging for Java, upewnij się, że masz wszystko, czego potrzebujesz:

### Środowisko programistyczne Java

Powinieneś mieć skonfigurowane środowisko programistyczne Java w swoim systemie. Jeśli jeszcze tego nie zrobiłeś, możesz pobrać i zainstalować zestaw Java Development Kit (JDK) z witryny internetowej Oracle.

### Aspose.Imaging dla Java

Aby skorzystać z tego samouczka, musisz mieć zainstalowany program Aspose.Imaging for Java. Można go pobrać ze strony internetowej Aspose, korzystając z następującego łącza:[Pobierz Aspose.Imaging dla Java](https://releases.aspose.com/imaging/java/).

### Obraz DICOM

Będziesz potrzebował obrazu DICOM, który chcesz binaryzować. Jeśli go nie masz, możesz znaleźć próbki obrazów DICOM w Internecie lub możesz użyć własnych obrazów DICOM.

Teraz, gdy masz już wymagania wstępne, przejdźmy do następnego kroku.

## Importuj pakiety

W tej sekcji zaimportujemy niezbędne pakiety z Aspose.Imaging dla Java. Pakiety te zawierają klasy i metody potrzebne do przeprowadzenia adaptacyjnej binaryzacji progów Bradleya na obrazie DICOM.

```java
// Ścieżka do katalogu dokumentów.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// Załaduj obraz DICOM do instancji DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Binaryzuj obraz za pomocą progu adaptacyjnego Bradleya.
    image.binarizeBradley(10);
    // Zapisz wynikowy obraz.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

## Krok 1: Zdefiniuj ścieżki

 Najpierw zdefiniuj ścieżki wejściowego obrazu DICOM i wyjściowego obrazu binarnego. Zastępować`"Your Document Directory"` z rzeczywistą ścieżką do katalogu.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

## Krok 2: Załaduj obraz DICOM

Użyj Aspose.Imaging, aby załadować obraz DICOM określony przez`inputFile` . Ta operacja tworzy instancję klasy`DicomImage` klasa.

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Tutaj znajdziesz kroki przetwarzania obrazu.
}
```

## Krok 3: Wykonaj binaryzację

 Wykonaj adaptacyjną binaryzację progową Bradleya na załadowanym obrazie DICOM. W tym przykładzie próg wynoszący`10` jest stosowany.

```java
image.binarizeBradley(10);
```

## Krok 4: Zapisz binarny obraz

Zapisz wynikowy obraz binarny w określonym pliku wyjściowym, używając formatu BMP.

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## Wniosek

Gratulacje! Pomyślnie nauczyłeś się, jak przeprowadzać binaryzację obrazu za pomocą Aspose.Imaging dla Java, korzystając z adaptacyjnej binaryzacji progowej Bradleya. To potężne narzędzie pozwala zwiększyć możliwości przetwarzania obrazu, co czyni go cennym narzędziem w różnych zastosowaniach.

 Pamiętaj, aby zapoznać się z obszerną dokumentacją Aspose.Imaging, aby uzyskać więcej możliwości przetwarzania obrazu:[Aspose.Imaging dla dokumentacji Java](https://reference.aspose.com/imaging/java/).

## Często zadawane pytania

### P1: Co to jest DICOM i dlaczego jest ważny w obrazowaniu medycznym?

Odpowiedź 1: DICOM oznacza cyfrowe obrazowanie i komunikację w medycynie i jest to standardowy format obrazów medycznych i powiązanych informacji. Odgrywa kluczową rolę w przechowywaniu, wymianie i interpretacji obrazów medycznych, co czyni go niezbędnym dla pracowników służby zdrowia i systemów obrazowania medycznego.

### P2: Czy mogę używać Aspose.Imaging for Java w moich projektach komercyjnych?

 Odpowiedź 2: Tak, Aspose.Imaging for Java oferuje zarówno bezpłatne wersje próbne, jak i licencje komercyjne. Możesz zapoznać się z dostępnymi opcjami i uzyskać niezbędne licencje od firmy[stronie Aspose](https://purchase.aspose.com/buy).

### P3: Czy dostępne są jakieś licencje tymczasowe do celów testowych?

 O3: Tak, możesz uzyskać tymczasową licencję na testowanie i ocenę Aspose.Imaging dla Java. Odwiedzać[ten link](https://purchase.aspose.com/temporary-license/) po więcej informacji.

### P4: Gdzie mogę szukać pomocy lub omówić problemy związane z Aspose.Imaging for Java?

 Odpowiedź 4: Aby uzyskać wsparcie i dyskusje społeczności, możesz odwiedzić stronę[Forum Aspose.Imaging](https://forum.aspose.com/). To świetne miejsce, aby znaleźć odpowiedzi na swoje pytania i nawiązać kontakt z innymi użytkownikami.

### P5: Czy Aspose.Imaging for Java nadaje się do przetwarzania obrazów w innych aplikacjach opartych na Javie?

O5: Tak, Aspose.Imaging for Java jest wszechstronny i może być używany w różnych aplikacjach opartych na Javie, w tym w aplikacjach internetowych, oprogramowaniu komputerowym i nie tylko.