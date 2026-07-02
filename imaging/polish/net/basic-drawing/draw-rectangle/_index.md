---
date: 2026-02-12
description: Dowiedz się, jak utworzyć pusty obraz w Aspose i jak narysować prostokąt
  w .NET za pomocą Aspose.Imaging – szybki przewodnik po manipulacji obrazami w Twoich
  aplikacjach .NET.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Utwórz pusty obraz Aspose – rysuj prostokąty w .NET
url: /pl/net/basic-drawing/draw-rectangle/
weight: 14
---

:** Aspose => "**Autor:** Aspose"

Now produce final content with all translations.

Check we kept all code block placeholders unchanged.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz pusty obraz Aspose – Rysowanie prostokątów w .NET

Tworzenie i manipulowanie obrazami w aplikacjach .NET może wydawać się trudne, ale dzięki Aspose.Imaging możesz **create blank image Aspose** w kilku linijkach kodu i następnie rysować na nim kształty. W tym samouczku przeprowadzimy Cię przez cały proces — od przygotowania pustego płótna po rysowanie prostokątów — abyś mógł od razu dodawać grafikę do swoich projektów .NET.

## Szybkie odpowiedzi
- **What does “create blank image Aspose” mean?** Oznacza to generowanie pustego bitmapa przy użyciu API Aspose.Imaging.  
- **How to draw rectangle .net with Aspose?** Użyj metody `Graphics.DrawRectangle` po zainicjowaniu obiektu `Graphics`.  
- **Which NuGet package is required?** `Aspose.Imaging` (najnowsza wersja).  
- **Can I save the image as PNG, JPEG, or BMP?** Tak – wystarczy zmienić opcje obrazu (np. `BmpOptions`, `JpegOptions`).  
- **Do I need a license for development?** Darmowa wersja próbna działa w celach ewaluacji; licencja komercyjna jest wymagana w produkcji.

## Co to jest „create blank image Aspose”?

Utworzenie pustego obrazu oznacza przydzielenie bufora pikseli o określonej szerokości, wysokości i formacie pikseli. Aspose.Imaging zajmuje się szczegółami niskiego poziomu, zapewniając gotowe do rysowania płótno bez konieczności pracy z GDI+ lub System.Drawing.

## Dlaczego warto używać Aspose.Imaging do rysowania prostokątów w .NET?

- **Cross‑platform** – działa na Windows, Linux i macOS.  
- **No native dependencies** – czysty kod zarządzany, idealny dla środowisk serwerowych.  
- **Rich drawing API** – obsługuje pióra, pędzle, antyaliasing i wiele typów kształtów.  
- **High performance** – zoptymalizowane pod kątem dużych obrazów i przetwarzania wsadowego.

## Wymagania wstępne

1. **Aspose.Imaging for .NET** – pobierz go ze [strony pobierania](https://releases.aspose.com/imaging/net/).  
2. **Development Environment** – Visual Studio, VS Code lub dowolne IDE zgodne z .NET.  
3. **.NET runtime** – .NET 6+ lub .NET Framework 4.7.2+.  

Teraz, gdy wszystko jest gotowe, przejdźmy do kodu.

## Jak utworzyć pusty obraz Aspose w .NET?

### Krok 1: Importuj wymagane przestrzenie nazw

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Te przestrzenie nazw zapewniają dostęp do podstawowych klas obrazowania, typów pędzli oraz opcji zapisu obrazu.

### Krok 2: Utwórz pusty obraz (płótno)

```csharp
string dataDir = "Your Document Directory";  // Set the path to your document directory
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Your drawing code will go here
        image.Save();
    }
}
```

W tym bloku:

* Definiujemy lokalizację wyjściową (`dataDir`).  
* Konfigurujemy `BmpOptions`, aby używał 32‑bitowego formatu pikseli.  
* Tworzymy **blank image** o wymiarach 100 × 100 pikseli.

### Krok 3: Jak narysować prostokąt .net przy użyciu Aspose.Imaging

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` wypełnia płótno kolorem tła (żółtym w tym przykładzie).  
* `DrawRectangle` rysuje dwa prostokąty — jeden prostym czerwonym piórem, drugi niebieskim, jednolitym pędzlem — dla kontrastu wizualnego.

### Krok 4: Zapisz obraz

```csharp
image.Save();
```

Wywołanie `Save` zapisuje bitmapę w systemie plików przy użyciu wcześniej zdefiniowanych opcji.

## Typowe problemy i wskazówki

| Issue | Reason | Fix |
|-------|--------|-----|
| **Blank image appears black** | Tło nie zostało wyczyszczone | Wywołaj `graphic.Clear(Color.YourColor)` przed rysowaniem. |
| **File not found exception** | `dataDir` wskazuje na nieistniejący folder | Upewnij się, że katalog istnieje lub użyj `Path.Combine` z `Environment.CurrentDirectory`. |
| **Incorrect colors** | Używanie `System.Drawing.Color` zamiast `Aspose.Imaging.Color` | Zawsze importuj `Aspose.Imaging.Color`. |
| **Performance lag on large images** | Używanie domyślnego `BmpOptions` z wysoką liczbą bitów na piksel | Przejdź na `JpegOptions` lub `PngOptions` w celu kompresji. |

## Najczęściej zadawane pytania (rozszerzone)

**Q: Czy mogę rysować inne kształty oprócz prostokątów?**  
A: Zdecydowanie. Aspose.Imaging udostępnia metody takie jak `DrawEllipse`, `DrawLine` i `DrawPolygon`.

**Q: Czy biblioteka jest darmowa do użytku komercyjnego?**  
A: Nie, Aspose.Imaging jest produktem komercyjnym, ale możesz go ocenić korzystając z darmowej wersji próbnej dostępnej [tutaj](https://releases.aspose.com/).

**Q: Czy to działa zarówno na Windows, jak i w aplikacjach internetowych?**  
A: Tak, ten sam kod działa w ASP.NET, Blazor oraz aplikacjach konsolowych.

**Q: Jak zmienić format wyjściowy na PNG?**  
A: Zastąp `BmpOptions` przez `PngOptions` i odpowiednio zmień rozszerzenie pliku.

**Q: Gdzie mogę znaleźć bardziej szczegółową dokumentację?**  
A: Uzyskaj dostęp do pełnej referencji API [tutaj](https://reference.aspose.com/imaging/net/) i dołącz do społeczności na [forum Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-02-12  
**Testowano z:** Aspose.Imaging 24.12 for .NET  
**Autor:** Aspose