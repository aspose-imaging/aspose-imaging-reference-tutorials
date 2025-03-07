---
title: Jak narysować obraz rastrowy w formacie SVG w Aspose.Imaging dla .NET
linktitle: Narysuj obraz rastrowy na SVG w Aspose.Imaging dla .NET
second_title: Aspose.Imaging .NET API przetwarzania obrazu
description: Dowiedz się, jak rysować obrazy rastrowe w formacie SVG przy użyciu Aspose.Imaging dla .NET. Ulepsz swoje aplikacje .NET za pomocą dynamicznych obrazów.
weight: 11
url: /pl/net/vector-image-processing/draw-raster-image-on-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak narysować obraz rastrowy w formacie SVG w Aspose.Imaging dla .NET


świecie programowania .NET Aspose.Imaging jest niezawodną i wszechstronną biblioteką do obsługi różnych zadań związanych z obrazami. Jedną z fascynujących możliwości, jakie oferuje, jest możliwość rysowania obrazu rastrowego na płótnie SVG. W tym przewodniku krok po kroku przeprowadzimy Cię przez proces rysowania obrazu rastrowego na pliku SVG przy użyciu Aspose.Imaging dla .NET.

## Warunki wstępne

Zanim zagłębimy się w szczegóły, upewnij się, że spełnione są następujące wymagania wstępne:

-  Aspose.Imaging dla .NET: Musisz mieć zainstalowaną bibliotekę. Jeśli nie, możesz pobrać go ze strony[Strona pobierania Aspose.Imaging dla platformy .NET](https://releases.aspose.com/imaging/net/).

-  Twój katalog dokumentów: Zamień`"Your Document Directory"` z rzeczywistą ścieżką do katalogu roboczego.

Podzielmy teraz proces na łatwe do wykonania kroki:

## Krok 1: Zaimportuj niezbędne przestrzenie nazw

Aby pracować z Aspose.Imaging, musisz zaimportować wymagane przestrzenie nazw:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Krok 2: Załaduj obrazy

- Najpierw załaduj obraz rastrowy, który chcesz narysować na płótnie SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Następnie załaduj obraz płótna SVG w miejscu, w którym chcesz narysować obraz rastrowy.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Krok 3: Rysowanie na obrazie SVG

Teraz możesz zacząć rysować na istniejącym obrazie SVG. Aby to zrobić, musisz utworzyć instancję`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Krok 4: Narysuj obraz rastrowy

- Zdefiniuj granice miejsca, w którym chcesz narysować obraz rastrowy, i określ obszar źródłowy z obrazu rastrowego.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Krok 5: Zapisz wynik

Po narysowaniu obrazu rastrowego na płótnie SVG możesz zapisać powstały obraz:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Wniosek

Gratulacje! Pomyślnie narysowałeś obraz rastrowy na płótnie SVG przy użyciu Aspose.Imaging dla .NET. Może to być niezwykle przydatne do tworzenia bogatych i dynamicznych obrazów w aplikacjach .NET.

 Więcej informacji i szczegółową dokumentację można znaleźć na stronie[Dokumentacja Aspose.Imaging dla .NET](https://reference.aspose.com/imaging/net/).

## Często Zadawane Pytania

### Co to jest Aspose.Imaging dla .NET?
   Aspose.Imaging dla .NET to potężna biblioteka do przetwarzania obrazów, która umożliwia programistom tworzenie, manipulowanie i konwertowanie obrazów w różnych formatach w aplikacjach .NET.

### Czy mogę używać Aspose.Imaging for .NET w projektach komercyjnych?
    Tak, możesz używać Aspose.Imaging dla .NET zarówno w projektach komercyjnych, jak i niekomercyjnych. Szczegóły licencji można znaleźć na stronie[strona zakupu](https://purchase.aspose.com/buy).

### Czy dostępny jest bezpłatny okres próbny?
    Tak, możesz uzyskać bezpłatną wersję próbną Aspose.Imaging dla .NET od[Tutaj](https://releases.aspose.com/).

### Gdzie mogę uzyskać wsparcie lub zadać pytania?
    Jeśli masz jakieś pytania lub potrzebujesz wsparcia, możesz odwiedzić stronę[Forum Aspose.Imaging](https://forum.aspose.com/).

### Jak mogę uzyskać tymczasową licencję na Aspose.Imaging dla .NET?
    Możesz uzyskać tymczasową licencję od[Tutaj](https://purchase.aspose.com/temporary-license/).



{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
