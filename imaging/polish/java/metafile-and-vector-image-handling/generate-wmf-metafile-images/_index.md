---
"description": "Dowiedz się, jak tworzyć obrazy metaplików WMF w Javie przy użyciu Aspose.Imaging. Postępuj zgodnie z tym przewodnikiem krok po kroku, aby uzyskać potężne możliwości generowania obrazów."
"linktitle": "Generuj obrazy metapliku WMF"
"second_title": "Aspose.Imaging API przetwarzania obrazu Java"
"title": "Tworzenie obrazów WMF za pomocą Aspose.Imaging dla Java"
"url": "/pl/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/"
"weight": 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Tworzenie obrazów WMF za pomocą Aspose.Imaging dla Java

Czy chcesz tworzyć obrazy WMF (Windows Metafile) za pomocą aplikacji Java? Aspose.Imaging for Java to potężne narzędzie, które pozwala na łatwe generowanie obrazów WMF. W tym przewodniku krok po kroku przeprowadzimy Cię przez proces używania Aspose.Imaging for Java do tworzenia obrazów metaplików WMF. 

## Wymagania wstępne

Zanim zaczniesz, upewnij się, że spełnione są następujące wymagania wstępne:

- Środowisko programistyczne Java skonfigurowane na Twoim komputerze.
- Biblioteka Aspose.Imaging for Java została zainstalowana. Możesz ją pobrać ze strony [strona internetowa](https://releases.aspose.com/imaging/java/).
- Podstawowa znajomość programowania w Javie.

## Importuj pakiety

Najpierw zaimportuj niezbędne pakiety, aby Twoja aplikacja Java mogła korzystać z Aspose.Imaging dla Java:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.color.*;
import com.aspose.imaging.coreexceptions.ImageLoadException;
import com.aspose.imaging.imageoptions.WmfOptions;
import com.aspose.imaging.internal.system.drawing.*;
import com.aspose.imaging.internal.system.drawing.imaging.*;
import com.aspose.imaging.pen.*;
import com.aspose.imaging.system.drawing.*;
```

## Krok 1: Utwórz płótno

Aby rozpocząć tworzenie obrazu WMF, musisz utworzyć płótno, na którym możesz rysować kształty. `WmfRecorderGraphics2D` Klasa dostarcza ci tego płótna. Oto jak możesz utworzyć jego instancję:

```java
// Ścieżka do katalogu dokumentów.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

W powyższym kodzie określamy wymiary płótna (100x100) i rozdzielczość (96 DPI).

## Krok 2: Ustaw kolor tła

Następnie zdefiniuj kolor tła dla swojego płótna. Możesz użyć `setBackgroundColor` metoda ustawiania koloru tła:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

W tym przykładzie ustawiliśmy kolor tła na biały dym.

## Krok 3: Zdefiniuj pióro i pędzel

Aby rysować kształty na płótnie, musisz zdefiniować pióro i pędzel. Pióro służy do rysowania konturów, a pędzel do wypełniania kształtów. Oto jak możesz utworzyć pióro i pędzel pełny:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

W tym kodzie tworzymy niebieski długopis i żółtozielony pędzel.

## Krok 4: Wypełnij i narysuj kształty

Teraz wypełnijmy i narysujmy kilka podstawowych kształtów na płótnie. Zaczniemy od wielokąta:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Tutaj wypełniamy i rysujemy wielokąt za pomocą określonego pióra i pędzla. Możesz dostosować współrzędne i kształty według potrzeb.

## Krok 5: Użyj HatchBrush

Aby dodać tekstury do swoich kształtów, możesz użyć `HatchBrush`. Na przykład:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

W tym kodzie tworzymy pędzel w kształcie kratki, używając kolorów białego i srebrnego.

## Krok 6: Wypełnij i narysuj elipsę

Wypełnijmy i narysujmy elipsę na płótnie:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

Możesz dostosować położenie i rozmiar elipsy według potrzeb.

## Krok 7: Narysuj łuk i sześcienny Bezier

Rysowanie bardziej złożonych kształtów jest również możliwe. Oto jak narysować łuk i krzywą Beziera sześcienną:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

W powyższym kodzie najpierw rysujemy łuk linią przerywaną, a następnie rysujemy krzywą Béziera sześcienną za pomocą jednolitego, czerwonego długopisu.

## Krok 8: Dodaj obrazy

Możesz również dodać obrazy do swojego metapliku WMF. Oto jak to zrobić:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

tym kroku ładujemy obraz i umieszczamy go na płótnie w określonych współrzędnych (50, 50).

## Krok 9: Narysuj linie i wykres kołowy

Aby dodać linie i kształty koła, możesz skorzystać z poniższych przykładów:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Tutaj rysujemy linię i wypełniamy/rysujemy kształt koła przy użyciu określonego pióra i pędzla.

## Krok 10: Narysuj linię łamaną i tekst

Dodawanie tekstu i linii łamanych jest proste:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

Możesz dostosować czcionkę, tekst i punkty linii łamanej według swoich potrzeb.

## Krok 11: Zapisz obraz WMF

Po utworzeniu obrazu WMF czas go zapisać:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Ten kod zapisze obraz WMF w określonym katalogu.

To wszystko! Udało Ci się wygenerować obraz metapliku WMF przy użyciu Aspose.Imaging dla Java.

## Wniosek

tym samouczku zbadaliśmy, jak tworzyć obrazy metaplików WMF przy użyciu Aspose.Imaging for Java. Omówiliśmy niezbędne wymagania wstępne, zaimportowaliśmy pakiety i podaliśmy instrukcje krok po kroku dotyczące rysowania różnych kształtów, dodawania tekstur, wstawiania obrazów i zapisywania ostatecznego obrazu. Aspose.Imaging for Java oferuje potężny zestaw narzędzi do manipulacji obrazami i ich tworzenia, co czyni go cennym zasobem dla Twoich aplikacji Java.

## Najczęściej zadawane pytania

### P1: Czym jest format obrazu WMF?

A1: WMF to skrót od Windows Metafile, czyli formatu grafiki wektorowej używanego do przechowywania obrazów, rysunków i innych danych graficznych. Jest powszechnie używany w aplikacjach Windows i można go łatwo skalować bez utraty jakości.

### P2: Gdzie mogę pobrać Aspose.Imaging dla Java?

A2: Aspose.Imaging dla Javy można pobrać ze strony [strona internetowa](https://releases.aspose.com/imaging/java/).

### P3: Czy do korzystania z Aspose.Imaging dla Java potrzebne są zaawansowane umiejętności programistyczne?

A3: Chociaż wymagana jest podstawowa znajomość programowania w Javie, Aspose.Imaging for Java udostępnia przyjazny dla użytkownika interfejs API, który upraszcza zadania związane z manipulacją obrazami i ich tworzeniem.

### P4: Czy mogę używać Aspose.Imaging for Java w celach komercyjnych?

A4: Tak, Aspose.Imaging for Java oferuje komercyjne licencje dla firm i deweloperów. Licencję można kupić od [Tutaj](https://purchase.aspose.com/buy).

### P5: Gdzie mogę uzyskać pomoc lub zadać pytania dotyczące Aspose.Imaging dla Java?

A5: Wsparcie i współpracę ze społecznością Aspose można znaleźć na stronie [Fora Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}