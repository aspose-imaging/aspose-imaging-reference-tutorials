---
"description": "Dowiedz się, jak rysować obrazy rastrowe w formacie SVG za pomocą Aspose.Imaging dla platformy .NET. Ulepsz swoje aplikacje .NET za pomocą dynamicznych obrazów."
"linktitle": "Rysowanie obrazu rastrowego w formacie SVG w Aspose.Imaging dla platformy .NET"
"second_title": "Aspose.Imaging .NET Interfejs API przetwarzania obrazu"
"title": "Jak narysować obraz rastrowy w formacie SVG w Aspose.Imaging dla platformy .NET"
"url": "/pl/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Jak narysować obraz rastrowy w formacie SVG w Aspose.Imaging dla platformy .NET


W świecie programowania .NET Aspose.Imaging jest niezawodną i wszechstronną biblioteką do obsługi różnych zadań związanych z obrazami. Jedną z fascynujących możliwości, jakie oferuje, jest możliwość rysowania obrazu rastrowego na płótnie SVG. W tym przewodniku krok po kroku przeprowadzimy Cię przez proces rysowania obrazu rastrowego na SVG przy użyciu Aspose.Imaging dla .NET.

## Wymagania wstępne

Zanim przejdziemy do szczegółów, upewnij się, że spełnione są następujące wymagania wstępne:

- Aspose.Imaging dla .NET: Musisz mieć zainstalowaną bibliotekę. Jeśli nie, możesz ją pobrać z [Strona pobierania Aspose.Imaging dla .NET](https://releases.aspose.com/imaging/net/).

- Twój katalog dokumentów: Zamień `"Your Document Directory"` z rzeczywistą ścieżką do Twojego katalogu roboczego.

Teraz podzielimy ten proces na łatwe do wykonania kroki:

## Krok 1: Importuj niezbędne przestrzenie nazw

Aby pracować z Aspose.Imaging, należy zaimportować wymagane przestrzenie nazw:

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

- Następnie załaduj obraz SVG Canvas w miejscu, w którym chcesz narysować obraz rastrowy.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Krok 3: Rysowanie na obrazie SVG

Teraz możesz zacząć rysować na istniejącym obrazie SVG. Aby to zrobić, musisz utworzyć wystąpienie `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Krok 4: Narysuj obraz rastrowy

- Zdefiniuj granice, w których chcesz narysować obraz rastrowy i określ region źródłowy z obrazu rastrowego.

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

Gratulacje! Udało Ci się narysować obraz rastrowy na płótnie SVG przy użyciu Aspose.Imaging dla .NET. Może to być niezwykle przydatne do tworzenia bogatych i dynamicznych obrazów w aplikacjach .NET.

Aby uzyskać więcej informacji i szczegółową dokumentację, odwiedź stronę [Dokumentacja Aspose.Imaging dla .NET](https://reference.aspose.com/imaging/net/).

## Często zadawane pytania

### Czym jest Aspose.Imaging dla .NET?
   Aspose.Imaging for .NET to zaawansowana biblioteka do przetwarzania obrazów umożliwiająca programistom tworzenie, przetwarzanie i konwertowanie obrazów w różnych formatach w aplikacjach .NET.

### Czy mogę używać Aspose.Imaging dla .NET w projektach komercyjnych?
   Tak, możesz używać Aspose.Imaging dla .NET zarówno w projektach komercyjnych, jak i niekomercyjnych. Szczegóły dotyczące licencjonowania można znaleźć na stronie [strona zakupu](https://purchase.aspose.com/buy).

### Czy jest dostępna bezpłatna wersja próbna?
   Tak, możesz otrzymać bezpłatną wersję próbną Aspose.Imaging dla .NET od [Tutaj](https://releases.aspose.com/).

### Gdzie mogę uzyskać pomoc lub zadać pytania?
   Jeśli masz jakieś pytania lub potrzebujesz wsparcia, możesz odwiedzić stronę [Forum Aspose.Imaging](https://forum.aspose.com/).

### W jaki sposób mogę uzyskać tymczasową licencję na Aspose.Imaging dla platformy .NET?
   Możesz uzyskać tymczasową licencję od [Tutaj](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}