---
date: 2026-02-09
description: Dowiedz się, jak rysować łuk przy użyciu Aspose.Imaging dla .NET, w tym
  jak zapisać plik BMP, ustawić rozmiar obrazu i tło grafiki. Przewodnik krok po kroku
  dotyczący generowania obrazów BMP.
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Jak narysować łuk przy użyciu Aspose.Imaging dla .NET
url: /pl/net/basic-drawing/draw-arc/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Jak narysować łuk przy użyciu Aspose.Imaging dla .NET

W świecie przetwarzania obrazów, **how to draw arc** jest powszechnym zadaniem, które może dodać wizualny akcent każdej grafice. Dzięki Aspose.Imaging dla .NET możesz generować obrazy BMP, ustawiać rozmiar obrazu i rysować łuk przy użyciu pióra w kilku linijkach C#. Po zakończeniu tego samouczka dokładnie wiesz, jak narysować łuk, ustawić tło grafiki i bez wysiłku zapisać powstały plik BMP.

## Szybkie odpowiedzi
- **Co generuje kod?** Obraz BMP o wymiarach 100 × 100 pikseli z żółtym tłem i czarnym łukiem.  
- **Jakiej biblioteki użyto?** Aspose.Imaging for .NET.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę zmienić rozmiar obrazu?** Tak – zmodyfikuj parametry szerokości i wysokości w wywołaniu `Image.Create`.  
- **Czy format wyjściowy jest stały?** Przykład zapisuje plik BMP, ale można użyć dowolnego formatu obsługiwanego przez Aspose.Imaging.

## Co to jest „how to draw arc” w Aspose.Imaging?
Rysowanie łuku oznacza renderowanie zakrzywionego odcinka linii określonego prostokątem ograniczającym, kątem początkowym i kątem przebiegu. Aspose.Imaging udostępnia metodę `Graphics.DrawArc`, która pozwala **draw arc with pen** i kontrolować każdy aspekt wizualny.

## Dlaczego warto używać Aspose.Imaging do tego zadania?
- **Pełna kontrola** nad wymiarami obrazu, głębią kolorów i formatem pliku.  
- **Brak zewnętrznych zależności** – wszystko działa na czystym .NET.  
- **Wysoka wydajność** przy generowaniu dużej liczby grafik po stronie serwera.  

## Wymagania wstępne

Zanim przejdziemy do kodu, upewnij się, że masz następujące elementy:

1. **Aspose.Imaging for .NET** – pobierz go z oficjalnej strony [here](https://releases.aspose.com/imaging/net/).  
2. **Środowisko programistyczne .NET** (Visual Studio, VS Code lub dowolny kompilator C#).  

Teraz, gdy mamy gotowe wymagania wstępne, zacznijmy rysować!

## Importowanie niezbędnych przestrzeni nazw

Aby pracować z Aspose.Imaging, musisz wprowadzić odpowiednie przestrzenie nazw do zakresu:

### Krok 1: Importuj przestrzenie nazw

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

## Jak narysować łuk przy użyciu Aspose.Imaging dla .NET

Podzielimy proces na trzy przejrzyste kroki: utworzenie obrazu, przygotowanie powierzchni graficznej i ostateczne narysowanie łuku.

### Krok 1: Przygotowanie obrazu (ustaw rozmiar obrazu i wygeneruj obraz BMP)

```csharp
// Specify the directory where you want to save the image
string dataDir = "Your Document Directory";

// Create an instance of FileStream to save the image
using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
{
    // Create an instance of BmpOptions and set its properties
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;

    // Set the source for BmpOptions and create an instance of Image
    saveOptions.Source = new StreamSource(stream);
    using (Image image = Image.Create(saveOptions, 100, 100))
    {
```

Tutaj **set image size** na 100 × 100 pikseli i konfigurujemy opcje BMP. `FileStream` zapewnia, że **save BMP file** do wybranej lokalizacji.

### Krok 2: Inicjalizacja Graphics i ustawienie tła Graphics

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

`Graphics` pozwala nam malować na obrazie. Wywołując `Clear(Color.Yellow)`, **set graphics background** na jasny żółty, co sprawia, że łuk wyróżnia się.

### Krok 3: Zdefiniuj parametry łuku i narysuj łuk przy użyciu pióra

```csharp
        // Define the parameters for the arc
        int width = 100;
        int height = 200;
        int startAngle = 45;
        int sweepAngle = 270;

        // Draw the arc
        graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);

        // Save the changes
        image.Save();
    }
    stream.Close();
}
```

- `width` i `height` definiują prostokąt ograniczający, skutecznie **set image size** dla łuku.  
- Obiekt `Pen` umożliwia **draw arc with pen** w kolorze czarnym.  
- Po narysowaniu, `image.Save()` zapisuje **BMP file** na dysku.

## Typowe problemy i wskazówki

- **Łuk niewidoczny?** Upewnij się, że kolor pióra kontrastuje z tłem (np. czarny na żółtym).  
- **Nieprawidłowe wymiary?** Pamiętaj, że prostokąt ograniczający łuk może być większy niż obraz; dostosuj `width`/`height` lub rozmiar obrazu odpowiednio.  
- **Wskazówka dotycząca wydajności:** Używaj jednego obiektu `Graphics`, jeśli musisz narysować wiele kształtów na tym samym obrazie.

## FAQ

### Q1: Gdzie mogę znaleźć dokumentację Aspose.Imaging dla .NET?

A1: Dokumentację można znaleźć [here](https://reference.aspose.com/imaging/net/) – zawiera kompleksowe informacje o Aspose.Imaging dla .NET.

### Q2: Jak mogę pobrać Aspose.Imaging dla .NET?

A2: Aspose.Imaging dla .NET można pobrać ze strony [here](https://releases.aspose.com/imaging/net/).

### Q3: Czy dostępna jest darmowa wersja próbna Aspose.Imaging dla .NET?

A3: Tak, darmową wersję próbną można uzyskać [here](https://releases.aspose.com/), aby wypróbować Aspose.Imaging dla .NET.

### Q4: Czy potrzebuję tymczasowej licencji dla Aspose.Imaging dla .NET?

A4: Jeśli potrzebujesz tymczasowej licencji, możesz ją uzyskać [here](https://purchase.aspose.com/temporary-license/).

### Q5: Gdzie mogę uzyskać wsparcie lub zadać pytania dotyczące Aspose.Imaging dla .NET?

A5: Możesz odwiedzić forum Aspose.Imaging w celu uzyskania wsparcia i dyskusji [here](https://forum.aspose.com/).

---

**Ostatnia aktualizacja:** 2026-02-09  
**Testowano z:** Aspose.Imaging 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}