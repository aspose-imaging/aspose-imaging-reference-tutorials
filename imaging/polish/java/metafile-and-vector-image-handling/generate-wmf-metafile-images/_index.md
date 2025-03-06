---
title: Tworzenie obrazów WMF za pomocą Aspose.Imaging dla Java
linktitle: Generuj obrazy metaplików WMF
second_title: Aspose.Imaging API przetwarzania obrazu Java
description: Dowiedz się, jak tworzyć obrazy metaplików WMF w Javie przy użyciu Aspose.Imaging. Postępuj zgodnie z tym przewodnikiem krok po kroku, aby uzyskać zaawansowane możliwości generowania obrazów.
weight: 10
url: /pl/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tworzenie obrazów WMF za pomocą Aspose.Imaging dla Java

Czy chcesz tworzyć obrazy WMF (metaplik systemu Windows) za pomocą aplikacji Java? Aspose.Imaging for Java to potężne narzędzie, które pozwala z łatwością generować obrazy WMF. W tym przewodniku krok po kroku przeprowadzimy Cię przez proces używania Aspose.Imaging for Java do tworzenia obrazów metaplików WMF. 

## Warunki wstępne

Zanim zaczniesz, upewnij się, że spełnione są następujące wymagania wstępne:

- Środowisko programistyczne Java skonfigurowane na Twoim komputerze.
-  Zainstalowana biblioteka Aspose.Imaging for Java. Można go pobrać z[strona internetowa](https://releases.aspose.com/imaging/java/).
- Podstawowa znajomość programowania w języku Java.

## Importuj pakiety

Najpierw zaimportuj niezbędne pakiety dla aplikacji Java, aby móc korzystać z Aspose.Imaging for Java:

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

 Aby rozpocząć tworzenie obrazu WMF, musisz utworzyć płótno, na którym będziesz mógł rysować kształty. The`WmfRecorderGraphics2D` class udostępnia Ci to płótno. Oto jak możesz utworzyć jego instancję:

```java
// Ścieżka do katalogu dokumentów.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

W powyższym kodzie podajemy wymiary płótna (100x100) oraz rozdzielczość (96 DPI).

## Krok 2: Ustaw kolor tła

 Następnie zdefiniuj kolor tła płótna. Możesz skorzystać z`setBackgroundColor` metoda ustawienia koloru tła:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

W tym przykładzie ustawiliśmy kolor tła na biały dym.

## Krok 3: Zdefiniuj pióro i pędzel

Aby rysować kształty na płótnie, należy zdefiniować pióro i pędzel. Pióro służy do rysowania konturów, a pędzel do wypełniania kształtów. Oto jak możesz stworzyć pióro i solidny pędzel:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

W tym kodzie tworzymy niebieski długopis i żółto-zielony, solidny pędzel.

## Krok 4: Wypełniaj i rysuj kształty

Teraz wypełnijmy i narysujmy kilka podstawowych kształtów na płótnie. Zaczniemy od wielokąta:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Tutaj wypełniamy i rysujemy wielokąt za pomocą określonego pióra i pędzla. W razie potrzeby możesz dostosować współrzędne i kształty.

## Krok 5: Użyj HatchBrush

 Aby dodać tekstury do swoich kształtów, możesz użyć a`HatchBrush`. Na przykład:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

W tym kodzie tworzymy pędzel z kreskowaniem w kolorach białym i srebrnym.

## Krok 6: Wypełnij i narysuj elipsę

Wypełnijmy i narysujmy elipsę na płótnie:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

W razie potrzeby możesz dostosować położenie i rozmiar elipsy.

## Krok 7: Narysuj łuk i sześcienny Bezier

Możliwe jest również rysowanie bardziej skomplikowanych kształtów. Oto jak narysować łuk i sześcienną krzywą Beziera:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

W powyższym kodzie najpierw rysujemy łuk linią przerywaną, a następnie rysujemy sześcienną krzywą Beziera za pomocą stałego, czerwonego pisaka.

## Krok 8: Dodaj obrazy

Możesz także dodawać obrazy do metapliku WMF. Oto jak to zrobić:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

W tym kroku ładujemy obraz i umieszczamy go na płótnie pod określonymi współrzędnymi (50, 50).

## Krok 9: Narysuj linie i ciasto

Aby dodać linie i kształty koła, możesz skorzystać z poniższych przykładów:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Tutaj rysujemy linię i wypełniamy/rysujemy kształt koła za pomocą określonego pióra i pędzla.

## Krok 10: Narysuj polilinię i tekst

Dodawanie tekstu i polilinii jest proste:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

W razie potrzeby możesz dostosować czcionkę, tekst i punkty polilinii.

## Krok 11: Zapisz obraz WMF

Po utworzeniu obrazu WMF czas go zapisać:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Ten kod zapisze obraz WMF w określonym katalogu.

Otóż to! Pomyślnie wygenerowałeś obraz metapliku WMF przy użyciu Aspose.Imaging for Java.

## Wniosek

tym samouczku omówiliśmy, jak tworzyć obrazy metaplików WMF przy użyciu Aspose.Imaging dla Java. Omówiliśmy niezbędne wymagania wstępne, zaimportowaliśmy pakiety i udostępniliśmy instrukcje krok po kroku dotyczące rysowania różnych kształtów, dodawania tekstur, wstawiania obrazów i zapisywania końcowego obrazu. Aspose.Imaging for Java oferuje potężny zestaw narzędzi do manipulacji i tworzenia obrazów, co czyni go cennym zasobem dla aplikacji Java.

## Często zadawane pytania

### P1: Co to jest format obrazu WMF?

O1: WMF oznacza Windows Metafile, który jest formatem grafiki wektorowej używanym do przechowywania obrazów, rysunków i innych danych graficznych. Jest powszechnie używany w aplikacjach Windows i można go łatwo skalować bez utraty jakości.

### P2: Gdzie mogę pobrać Aspose.Imaging dla Java?

 O2: Możesz pobrać Aspose.Imaging dla Java z[strona internetowa](https://releases.aspose.com/imaging/java/).

### P3: Czy potrzebuję zaawansowanych umiejętności programowania, aby korzystać z Aspose.Imaging for Java?

Odpowiedź 3: Chociaż wymagana jest podstawowa znajomość programowania w języku Java, Aspose.Imaging for Java zapewnia przyjazny dla użytkownika interfejs API, który upraszcza zadania manipulowania i tworzenia obrazów.

### P4: Czy mogę używać Aspose.Imaging for Java do celów komercyjnych?

 O4: Tak, Aspose.Imaging for Java oferuje licencje komercyjne dla firm i programistów. Możesz kupić licencję od[Tutaj](https://purchase.aspose.com/buy).

### P5: Gdzie mogę uzyskać pomoc lub zadać pytania dotyczące Aspose.Imaging for Java?

 Odpowiedź 5: Możesz znaleźć wsparcie i nawiązać kontakt ze społecznością Aspose na stronie[Fora Aspose.Imaging](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
