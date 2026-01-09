---
date: 2026-01-09
description: Dowiedz się, jak dodać znak wodny do obrazów przy użyciu Aspose.Imaging
  dla Javy. Ten samouczek przetwarzania obrazów w Javie pokazuje krok po kroku, jak
  szybko stworzyć ukośny znak wodny.
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: Jak dodać znak wodny – Przekątne znakowanie obrazu (Java)
url: /pl/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Jak dodać znak wodny – Przerywany znak wodny po przekątnej (Java)

Jeśli chcesz **dodać znak wodny** do swoich zdjęć w stylowej położeniu po przekątnej, Aspose.Imaging for Java robi to bezproblemowo. W tym samouczku krok po kroku pokażemy, jak dodać tekstowy znak wodny obrócony o 45 stopni do obrazu JPG (lub dowolnego obsługiwanego). Nie musisz być mistrzem Javy – każdy fragment jest wyjaśniony prostym językiem, dzięki czemu możesz odtworzyć wynik w kilka minut.

## Szybkie odpowiedzi
- **Jakiej biblioteki użyto?** Aspose.Imaging for Java  
- **Jakie główne słowo kluczowe jest omówione?** how to add watermark  
- **Obsługiwane formaty obrazów?** JPEG, PNG, BMP, TIFF, GIF i inne  
- **Ile kodu jest potrzebne?** Tylko siedem zwięzłych bloków kodu  
- **Czy potrzebna jest licencja do testów?** Dostępna jest bezpłatna wersja próbna; licencja jest wymagana w środowisku produkcyjnym  

## Co oznacza „how to add watermark” w przetwarzaniu obrazów?
Dodanie znaku wodnego oznacza nałożenie półprzezroczystego tekstu lub grafiki na obraz w celu ochrony własności lub przekazania marki. Znak wodny po przekątnej jest szczególnie skuteczny, ponieważ rozciąga się na całym obrazie i trudniej go wyciąć.

## Dlaczego warto używać Aspose.Imaging for Java?
Aspose.Imaging udostępnia wysokopoziomowe API, które ukrywa niskopoziomową manipulację pikselami, obsługuje dziesiątki formatów i działa na dowolnym środowisku Java. Pozwala skupić się na *tym*, co chcesz osiągnąć — np. dodaniu znaku wodnego po przekątnej — bez martwienia się o specyficzne cechy formatów obrazów.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz następujące elementy:

1. **Aspose.Imaging for Java** – pobierz najnowszą wersję ze strony oficjalnej **[tutaj](https://releases.aspose.com/imaging/java/)**.  
2. **Środowisko programistyczne Java** – JDK 8+ oraz ulubione IDE (IntelliJ, Eclipse, VS Code itp.).  
3. **Obraz do oznaczenia znakiem wodnym** – umieść przykładowy plik JPG/TIFF/PNG w folderze, do którego odwołasz się w kodzie.

## Importowanie pakietów

Najpierw zaimportuj potrzebne klasy. Trzymanie importów razem ułatwia czytanie i utrzymanie kodu.

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Krok 1: Załaduj istniejący obraz

Zaczynamy od załadowania obrazu źródłowego. Metoda `Image.load` automatycznie wykrywa format.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **Wskazówka:** Umieść obiekt `Image` w bloku try‑with‑resources (jak pokazano), aby został automatycznie zwolniony, zapobiegając wyciekom pamięci.

## Krok 2: Przygotuj tekst i grafikę znaku wodnego

Utwórz obiekt `Graphics` powiązany z załadowanym obrazem i zapisz rozmiar obrazu do późniejszych obliczeń.

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## Krok 3: Zdefiniuj czcionkę i pędzel

Wybierz czcionkę, która się wyróżnia, oraz pędzel definiujący kolor i przezroczystość znaku wodnego. Dostosuj przezroczystość, aby znak wodny był półprzezroczysty.

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Krok 4: Sformatuj tekst

Ustaw wyrównanie i flagi formatowania, aby tekst był wyśrodkowany podczas rysowania.

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Krok 5: Zastosuj transformację

Macierz transformacji pozwala przenieść początek do środka obrazu, a następnie obrócić tekst o ‑45° (zgodnie z ruchem wskazówek zegara).

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## Krok 6: Rysowanie i zapisywanie

Na koniec renderuj ciąg znaków na obrazie i zapisz wynik na dysku.

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Po otwarciu `AddDiagonalWatermarkToImage_out.jpg` zobaczysz czerwony, półprzezroczysty tekst nachylony przez środek obrazu.

## Typowe problemy i rozwiązania

| Problem | Powód | Rozwiązanie |
|---------|-------|-------------|
| Znak wodny jest zbyt słaby | Ustawiono przezroczystość na 0 (całkowicie przezroczysty) | Zwiększ przezroczystość, np. `brush.setOpacity(0.5f);` |
| Tekst jest obcięty na krawędziach | Translacja nie jest wyśrodkowana dla obrazów nie‑kwadratowych | Użyj `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` jak pokazano, a następnie w razie potrzeby dostosuj kąt obrotu |
| Błąd nieobsługiwanego formatu obrazu | Używanie starszej wersji Aspose.Imaging | Zaktualizuj do najnowszej wersji Aspose.Imaging |

## Najczęściej zadawane pytania

### P1: Czy Aspose.Imaging for Java jest odpowiedni dla początkujących?

**A:** Zdecydowanie! API jest intuicyjne, a dokumentacja zawiera przejrzyste przykłady. Nawet programiści nowi w przetwarzaniu obrazów mogą podążać za tym samouczkiem i szybko uzyskać profesjonalne wyniki.

### P2: Czy mogę dostosować tekst i styl znaku wodnego?

**A:** Tak. Zmień zmienną `theString`, wybierz inną `Font`, zmodyfikuj `brush.setColor(...)` lub dostosuj kąt obrotu w macierzy, aby pasował do Twojej marki.

### P3: Czy Aspose.Imaging for Java obsługuje inne formaty obrazów poza JPG?

**A:** Tak. Biblioteka działa z BMP, PNG, GIF, TIFF, PSD i wieloma innymi. Wystarczy przekazać metodzie `Image.load` odpowiedni plik.

### P4: Czy dostępna jest bezpłatna wersja próbna Aspose.Imaging for Java?

**A:** Tak, możesz wypróbować Aspose.Imaging for Java w wersji próbnej. Pobierz ją **[tutaj](https://releases.aspose.com/)**.

### P5: Gdzie mogę znaleźć pomoc lub wsparcie dla Aspose.Imaging for Java?

**A:** W przypadku pytań, zgłoszeń błędów lub porad dotyczących najlepszych praktyk, odwiedź forum wsparcia Aspose.Imaging for Java **[tutaj](https://forum.aspose.com/)**.

---

**Ostatnia aktualizacja:** 2026-01-09  
**Testowano z:** Aspose.Imaging for Java 24.11 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}