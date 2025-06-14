---
"description": "Ulepsz swoje obrazy za pomocą diagonalnego znaku wodnego za pomocą Aspose.Imaging dla Java. Postępuj zgodnie z tym przewodnikiem krok po kroku i bez wysiłku twórz oszałamiające obrazy ze znakiem wodnym."
"linktitle": "Znakowanie wodne obrazu diagonalnego"
"second_title": "Aspose.Imaging API przetwarzania obrazu Java"
"title": "Znakowanie wodne obrazu diagonalnego za pomocą Aspose.Imaging dla Java"
"url": "/pl/java/image-processing-and-enhancement/diagonal-image-watermarking/"
"weight": 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Znakowanie wodne obrazu diagonalnego za pomocą Aspose.Imaging dla Java


Jeśli chcesz ulepszyć swoje obrazy za pomocą stylowego, ukośnego znaku wodnego, Aspose.Imaging for Java jest tutaj, aby Ci pomóc. W tym przewodniku krok po kroku przeprowadzimy Cię przez proces dodawania obróconego o 45 stopni znaku wodnego do istniejącego obrazu JPG. Nie musisz być ekspertem w Javie ani przetwarzaniu obrazów, aby to zrobić — podzielimy każdy przykład na wiele kroków, aby zapewnić Ci łatwe osiągnięcie profesjonalnych rezultatów.

## Wymagania wstępne

Zanim zanurzymy się w fascynującym świecie znaków wodnych na obrazach, będziesz potrzebować kilku rzeczy:

1. Aspose.Imaging dla Java: Upewnij się, że masz zainstalowany Aspose.Imaging dla Java. Link do pobrania znajdziesz [Tutaj](https://releases.aspose.com/imaging/java/).

2. Środowisko programistyczne Java: Na swoim komputerze powinieneś mieć zainstalowane działające środowisko programistyczne Java.

3. Obraz do znaku wodnego: Przygotuj obraz, który chcesz oznaczyć znakiem wodnym i zapisz go w katalogu. Możesz użyć przykładowego obrazu do tego samouczka.

## Importuj pakiety

Najpierw zaimportuj niezbędne pakiety, aby przygotować projekt Java do znakowania wodnego obrazu. Poniżej znajdują się niezbędne pakiety, które musisz uwzględnić:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Krok 1: Załaduj istniejący obraz

Załaduj obraz, który chcesz oznaczyć znakiem wodnym. W tym przykładzie zakładamy, że masz obraz JPG o nazwie „SampleTiff1.tiff” w katalogu „ModifyingImages”.

```java
// Ścieżka do katalogu dokumentów.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Załaduj istniejący obraz JPG
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Reszta kodu znajduje się tutaj
}
```

## Krok 2: Przygotuj tekst i grafikę znaku wodnego

Teraz zadeklarujmy tekst znaku wodnego i ustawmy jego grafikę.

```java
// Deklarowanie obiektu String z tekstem znaku wodnego
String theString = "45 Degree Rotated Text";

// Utwórz i zainicjuj instancję klasy Graphics
Graphics graphics = new Graphics(image);

// Zainicjuj obiekt SizeF, aby zapisać rozmiar obrazu
Size sz = graphics.getImage().getSize();
```

## Krok 3: Zdefiniuj czcionkę i pędzel

Ustaw czcionkę i pędzel dla swojego znaku wodnego. Możesz dostosować czcionkę, rozmiar i styl do swoich preferencji.

```java
// Utwórz instancję czcionki, zainicjuj ją za pomocą kroju, rozmiaru i stylu czcionki
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Utwórz instancję SolidBrush i ustaw jej różne właściwości
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Krok 4: Sformatuj swój tekst

Zdefiniuj format tekstu znaku wodnego, w tym wyrównanie i flagi formatowania.

```java
// Zainicjuj obiekt klasy StringFormat i ustaw jego różne właściwości
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Krok 5: Zastosuj transformację

Utwórz macierz transformacji, aby ustawić i obrócić tekst znaku wodnego. W tym przykładzie obrócimy tekst o 45 stopni.

```java
// Utwórz obiekt klasy Matrix do transformacji
Matrix matrix = new Matrix();
// Najpierw tłumaczenie, potem obrót
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Ustaw transformację za pomocą macierzy
graphics.setTransform(matrix);
```

## Krok 6: Narysuj i zapisz

Teraz pora dodać tekst do obrazu i zapisać obraz ze znakiem wodnym w wybranej lokalizacji.

```java
// Narysuj sznurek na obrazku
graphics.drawString(theString, font, brush, 0, 0, format);

// Zapisz dane wyjściowe na dysku
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Gratulacje! Udało Ci się dodać diagonalny znak wodny do swojego obrazu za pomocą Aspose.Imaging dla Java.

## Wniosek

tym samouczku nauczyliśmy się, jak ulepszyć swoje obrazy za pomocą diagonalnego znaku wodnego za pomocą Aspose.Imaging for Java. To potężne narzędzie do dodawania profesjonalnego akcentu do obrazów. Za pomocą zaledwie kilku prostych kroków możesz tworzyć oszałamiające obrazy ze znakiem wodnym, które wyróżniają się na tle innych.

## Najczęściej zadawane pytania

### P1: Czy Aspose.Imaging dla Java nadaje się dla początkujących?

A1: Oczywiście! Aspose.Imaging for Java oferuje przyjazny dla użytkownika interfejs i kompleksową dokumentację. Nawet początkujący mogą szybko rozpocząć przetwarzanie obrazu.

### P2: Czy mogę dostosować tekst i styl znaku wodnego?

A2: Tak, możesz łatwo dostosować tekst znaku wodnego, czcionkę, rozmiar, kolor i kąt obrotu, aby dopasować go do swoich preferencji i marki.

### P3: Czy Aspose.Imaging dla Java obsługuje inne formaty obrazów oprócz JPG?

A3: Tak, Aspose.Imaging for Java obsługuje szeroką gamę formatów obrazów, w tym BMP, PNG, GIF i inne.

### P4: Czy jest dostępna bezpłatna wersja próbna Aspose.Imaging for Java?

A4: Tak, możesz wypróbować Aspose.Imaging dla Java z bezpłatną wersją próbną. Pobierz [Tutaj](https://releases.aspose.com/).

### P5: Gdzie mogę znaleźć pomoc i wsparcie dla Aspose.Imaging dla Java?

A5: Jeśli masz jakieś pytania lub potrzebujesz pomocy, odwiedź forum pomocy technicznej Aspose.Imaging for Java [Tutaj](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}