---
title: Narysuj obraz wektorowy na obraz rastrowy w Aspose.Imaging dla .NET
linktitle: Narysuj obraz wektorowy na obraz rastrowy w Aspose.Imaging dla .NET
second_title: Aspose.Imaging .NET API przetwarzania obrazu
description: Dowiedz się, jak konwertować obrazy wektorowe na obrazy rastrowe w .NET przy użyciu Aspose.Imaging. Przewodnik krok po kroku dotyczący wydajnego przetwarzania obrazu.
weight: 13
url: /pl/net/vector-image-processing/draw-vector-image-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Narysuj obraz wektorowy na obraz rastrowy w Aspose.Imaging dla .NET


Czy chcesz bez wysiłku konwertować obrazy wektorowe na obrazy rastrowe w aplikacjach .NET? Aspose.Imaging dla .NET zapewnia wydajne rozwiązanie tego zadania. W tym przewodniku krok po kroku przeprowadzimy Cię przez proces rysowania obrazów wektorowych do obrazów rastrowych przy użyciu Aspose.Imaging dla .NET. 

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

### 1. Aspose.Imaging dla .NET

 Powinieneś mieć zainstalowany Aspose.Imaging dla .NET. Jeśli go nie masz, możesz go pobrać ze strony internetowej pod adresem[Pobierz Aspose.Imaging dla .NET](https://releases.aspose.com/imaging/net/).

### 2. Środowisko programistyczne .NET

Upewnij się, że na komputerze jest skonfigurowane środowisko programistyczne .NET. Możesz użyć programu Visual Studio lub dowolnego innego narzędzia programistycznego .NET.

Podzielmy teraz proces rysowania obrazów wektorowych na obrazy rastrowe na proste, łatwe do wykonania kroki:

## Krok 1: Zainicjuj swój projekt

Zacznij od utworzenia nowego projektu .NET w swoim środowisku programistycznym. Upewnij się, że masz zintegrowany program Aspose.Imaging for .NET ze swoim projektem.

## Krok 2: Załaduj obraz wektorowy

Na tym etapie ładujemy obraz wektorowy (w formacie SVG), który chcesz przekonwertować na obraz rastrowy.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## Krok 3: Rasteryzacja obrazu wektorowego

Teraz musimy zrasteryzować obraz SVG do formatu PNG. W tym miejscu następuje konwersja z wektora na raster.

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

Na koniec zapisz obraz wynikowy. Masz teraz obraz rastrowy zawierający obraz wektorowy.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## Wniosek

W tym samouczku pokazaliśmy, jak konwertować obrazy wektorowe na obrazy rastrowe za pomocą Aspose.Imaging dla .NET. Dzięki tym prostym krokom możesz bez wysiłku zintegrować tę funkcjonalność z aplikacjami .NET.

### Często Zadawane Pytania

### Co to jest Aspose.Imaging dla .NET?
Aspose.Imaging dla .NET to biblioteka .NET zapewniająca zaawansowane funkcje przetwarzania obrazów, w tym możliwość pracy z różnymi formatami obrazów, konwertowania obrazów i wykonywania zaawansowanych zadań manipulacji obrazami.

### Gdzie mogę znaleźć dokumentację Aspose.Imaging dla .NET?
 Możesz znaleźć dokumentację Aspose.Imaging dla .NET[Tutaj](https://reference.aspose.com/imaging/net/).

### Czy dostępna jest bezpłatna wersja próbna?
 Tak, możesz uzyskać dostęp do bezpłatnej wersji próbnej Aspose.Imaging dla .NET[Tutaj](https://releases.aspose.com/).

### Jak uzyskać tymczasową licencję na Aspose.Imaging dla .NET?
 Jeśli potrzebujesz licencji tymczasowej, możesz ją uzyskać[Tutaj](https://purchase.aspose.com/temporary-license/).

### Gdzie mogę uzyskać pomoc dotyczącą Aspose.Imaging dla .NET?
 Aby uzyskać pomoc lub zadać pytania, możesz odwiedzić stronę[Forum Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
