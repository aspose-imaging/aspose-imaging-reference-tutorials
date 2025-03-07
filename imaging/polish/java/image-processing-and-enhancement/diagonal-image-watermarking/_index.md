---
title: Znak wodny obrazu diagonalnego za pomocą Aspose.Imaging dla języka Java
linktitle: Znak wodny obrazu ukośnego
second_title: Aspose.Imaging API przetwarzania obrazu Java
description: Ulepsz swoje obrazy za pomocą ukośnego znaku wodnego za pomocą Aspose.Imaging dla Java. Postępuj zgodnie z tym przewodnikiem krok po kroku i bez wysiłku twórz wspaniałe obrazy ze znakiem wodnym.
weight: 14
url: /pl/java/image-processing-and-enhancement/diagonal-image-watermarking/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Znak wodny obrazu diagonalnego za pomocą Aspose.Imaging dla języka Java


Jeśli chcesz ulepszyć swoje obrazy za pomocą stylowego, ukośnego znaku wodnego, Aspose.Imaging for Java jest tutaj, aby Ci pomóc. W tym przewodniku krok po kroku przeprowadzimy Cię przez proces dodawania tekstowego znaku wodnego obróconego o 45 stopni do istniejącego obrazu JPG. Aby śledzić dalej, nie musisz być ekspertem w dziedzinie języka Java ani przetwarzania obrazów — podzielimy każdy przykład na wiele kroków, aby zapewnić łatwe osiągnięcie profesjonalnych wyników.

## Warunki wstępne

Zanim zagłębimy się w ekscytujący świat znaków wodnych obrazów, będziesz potrzebować kilku rzeczy:

1.  Aspose.Imaging dla Java: Upewnij się, że masz zainstalowany Aspose.Imaging dla Java. Możesz znaleźć link do pobrania[Tutaj](https://releases.aspose.com/imaging/java/).

2. Środowisko programistyczne Java: Na komputerze powinno być skonfigurowane działające środowisko programistyczne Java.

3. Obraz do znaku wodnego: Przygotuj obraz, do którego chcesz dodać znak wodny, i zapisz go w katalogu. W tym samouczku możesz użyć przykładowego obrazu.

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

Załaduj obraz, do którego chcesz dodać znak wodny. W tym przykładzie zakładamy, że masz obraz JPG o nazwie „SampleTiff1.tiff” w katalogu „ModifyingImages”.

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

Teraz zadeklarujmy tekst znaku wodnego i skonfigurujmy grafikę znaku wodnego.

```java
// Zadeklaruj obiekt String z tekstem znaku wodnego
String theString = "45 Degree Rotated Text";

// Utwórz i zainicjuj instancję klasy Graphics
Graphics graphics = new Graphics(image);

// Zainicjuj obiekt SizeF, aby zapisać rozmiar obrazu
Size sz = graphics.getImage().getSize();
```

## Krok 3: Zdefiniuj czcionkę i pędzel

Ustaw czcionkę i pędzel dla swojego znaku wodnego. Możesz dostosować czcionkę, rozmiar i styl, aby dopasować je do swoich preferencji.

```java
// Utwórz instancję czcionki, zainicjuj ją za pomocą kroju czcionki, rozmiaru i stylu
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Utwórz instancję SolidBrush i ustaw jej różne właściwości
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Krok 4: Sformatuj swój tekst

Zdefiniuj format tekstu znaku wodnego, w tym wyrównanie i flagi formatu.

```java
// Zainicjuj obiekt klasy StringFormat i ustaw jego różne właściwości
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Krok 5: Zastosuj transformację

Utwórz macierz transformacji, aby ustawić położenie i obrócić tekst znaku wodnego. W tym przykładzie obrócimy tekst o 45 stopni.

```java
// Utwórz obiekt klasy Matrix do transformacji
Matrix matrix = new Matrix();
//Najpierw tłumaczenie, potem rotacja
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Ustaw transformację poprzez macierz
graphics.setTransform(matrix);
```

## Krok 6: Narysuj i zapisz

Teraz nadszedł czas, aby dodać tekst do obrazu i zapisać obraz ze znakiem wodnym w wybranej lokalizacji.

```java
// Narysuj sznurek na obrazku
graphics.drawString(theString, font, brush, 0, 0, format);

// Zapisz dane wyjściowe na dysku
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Gratulacje! Pomyślnie dodałeś ukośny znak wodny do swojego obrazu za pomocą Aspose.Imaging for Java.

## Wniosek

W tym samouczku nauczyliśmy się, jak ulepszyć obrazy za pomocą ukośnego znaku wodnego przy użyciu Aspose.Imaging dla Java. To potężne narzędzie do dodawania profesjonalnego charakteru do zdjęć. W kilku prostych krokach możesz stworzyć wspaniałe obrazy ze znakiem wodnym, które wyróżniają się na tle innych.

## Często zadawane pytania

### P1: Czy Aspose.Imaging dla Java jest odpowiedni dla początkujących?

A1: Absolutnie! Aspose.Imaging for Java oferuje przyjazny dla użytkownika interfejs i obszerną dokumentację. Nawet początkujący mogą szybko rozpocząć przetwarzanie obrazu.

### P2: Czy mogę dostosować tekst i styl znaku wodnego?

Odpowiedź 2: Tak, możesz łatwo dostosować tekst znaku wodnego, czcionkę, rozmiar, kolor i kąt obrotu, aby dopasować je do swoich preferencji i marki.

### P3: Czy Aspose.Imaging for Java obsługuje inne formaty obrazów oprócz JPG?

O3: Tak, Aspose.Imaging for Java obsługuje szeroką gamę formatów obrazów, w tym BMP, PNG, GIF i inne.

### P4: Czy dostępna jest bezpłatna wersja próbna Aspose.Imaging for Java?

 O4: Tak, możesz wypróbować Aspose.Imaging for Java w ramach bezpłatnej wersji próbnej. Zdobyć[Tutaj](https://releases.aspose.com/).

### P5: Gdzie mogę znaleźć pomoc lub wsparcie dla Aspose.Imaging dla Java?

 O5: Jeśli masz jakieś pytania lub potrzebujesz pomocy, odwiedź forum wsparcia Aspose.Imaging for Java[Tutaj](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
