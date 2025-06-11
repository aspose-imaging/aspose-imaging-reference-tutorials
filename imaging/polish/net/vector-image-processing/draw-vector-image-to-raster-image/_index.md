---
"description": "Dowiedz się, jak konwertować obrazy wektorowe na obrazy rastrowe w .NET przy użyciu Aspose.Imaging. Przewodnik krok po kroku dotyczący wydajnego przetwarzania obrazów."
"linktitle": "Narysuj obraz wektorowy do obrazu rastrowego w Aspose.Imaging dla .NET"
"second_title": "Aspose.Imaging .NET Interfejs API przetwarzania obrazu"
"title": "Narysuj obraz wektorowy do obrazu rastrowego w Aspose.Imaging dla .NET"
"url": "/pl/net/vector-image-processing/draw-vector-image-to-raster-image/"
"weight": 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Narysuj obraz wektorowy do obrazu rastrowego w Aspose.Imaging dla .NET


Czy chcesz bez wysiłku konwertować obrazy wektorowe na obrazy rastrowe w swoich aplikacjach .NET? Aspose.Imaging dla .NET zapewnia wydajne rozwiązanie tego zadania. W tym przewodniku krok po kroku przeprowadzimy Cię przez proces rysowania obrazów wektorowych na obrazy rastrowe przy użyciu Aspose.Imaging dla .NET. 

## Wymagania wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełnione są następujące wymagania wstępne:

### 1. Aspose.Imaging dla .NET

Powinieneś mieć zainstalowany Aspose.Imaging dla .NET. Jeśli go nie masz, możesz go pobrać ze strony internetowej pod adresem [Pobierz Aspose.Imaging dla .NET](https://releases.aspose.com/imaging/net/).

### 2. Środowisko programistyczne .NET

Upewnij się, że masz środowisko programistyczne .NET skonfigurowane na swoim komputerze. Możesz użyć Visual Studio lub dowolnego innego narzędzia programistycznego .NET.

Teraz omówimy proces przekształcania obrazów wektorowych w obrazy rastrowe w prostych, łatwych do wykonania krokach:

## Krok 1: Zainicjuj swój projekt

Zacznij od utworzenia nowego projektu .NET w swoim środowisku programistycznym. Upewnij się, że masz Aspose.Imaging for .NET zintegrowany ze swoim projektem.

## Krok 2: Załaduj obraz wektorowy

W tym kroku ładujemy obraz wektorowy (w formacie SVG), który chcesz przekonwertować na obraz rastrowy.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## Krok 3: Rasteryzacja obrazu wektorowego

Teraz musimy zrasteryzować obraz SVG do formatu PNG. To tutaj następuje konwersja z wektora do rastra.

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## Krok 4: Załaduj obraz rastrowy

Po rasteryzacji załaduj obraz PNG ze strumienia w celu dalszego rysowania.

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## Krok 5: Narysuj obraz rastrowy

Teraz możemy narysować obraz rastrowy na istniejącym obrazie SVG.

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## Krok 6: Zapisz wynik

Na koniec zapisz obraz wynikowy. Teraz masz obraz rastrowy, który zawiera Twój obraz wektorowy.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## Wniosek

tym samouczku pokazaliśmy, jak konwertować obrazy wektorowe na obrazy rastrowe za pomocą Aspose.Imaging dla .NET. Dzięki tym prostym krokom możesz bez wysiłku zintegrować tę funkcjonalność ze swoimi aplikacjami .NET.

### Często zadawane pytania

### Czym jest Aspose.Imaging dla .NET?
Aspose.Imaging for .NET to biblioteka .NET oferująca zaawansowane funkcje przetwarzania obrazów, w tym możliwość pracy z różnymi formatami obrazów, konwersji obrazów i wykonywania zaawansowanych zadań związanych z manipulacją obrazami.

### Gdzie mogę znaleźć dokumentację Aspose.Imaging dla .NET?
Dokumentację Aspose.Imaging dla .NET można znaleźć tutaj [Tutaj](https://reference.aspose.com/imaging/net/).

### Czy jest dostępna bezpłatna wersja próbna?
Tak, możesz uzyskać dostęp do bezpłatnej wersji próbnej Aspose.Imaging dla .NET [Tutaj](https://releases.aspose.com/).

### Jak uzyskać tymczasową licencję na Aspose.Imaging dla .NET?
Jeśli potrzebujesz tymczasowej licencji, możesz ją uzyskać [Tutaj](https://purchase.aspose.com/temporary-license/).

### Gdzie mogę uzyskać pomoc dotyczącą Aspose.Imaging dla .NET?
przypadku pytań lub potrzeby uzyskania wsparcia możesz odwiedzić stronę [Forum Aspose.Imaging](https://forum.aspose.com/).


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}