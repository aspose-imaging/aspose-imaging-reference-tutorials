---
date: 2026-01-30
description: Dowiedz się, jak rysować tekst na obrazie, rysować kształty na obrazie
  i wypełniać kształty wzorem przy użyciu Aspose.Imaging dla .NET.
linktitle: Draw Using GraphicsPath – draw text on image, shapes and patterns
second_title: Aspose.Imaging .NET Image Processing API
title: Jak narysować tekst na obrazie przy użyciu Aspose.Imaging dla .NET
url: /pl/net/advanced-drawing/draw-using-graphicspath/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Jak rysować tekst na obrazie przy użyciu Aspose.Imaging dla .NET

W tym samouczku przeprowadzimy Cię przez **rysowanie tekstu na obrazie**, a także pokażemy, jak rysować kształty na obrazie i wypełniać je wzorem przy użyciu potężnej biblioteki Aspose.Imaging. Niezależnie od tego, czy tworzysz narzędzie raportujące, własny generator odznak, czy po prostu potrzebujesz programowo oznaczyć zdjęcia, poniższe kroki zapewnią solidne podstawy.

## Szybkie odpowiedzi
- **Co mogę rysować?** Tekst, podstawowe kształty (elipsa, prostokąt) oraz wypełnienia wzorowane.  
- **Która klasa jest centralna?** `GraphicsPath` w połączeniu z `Graphics`.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna wystarcza do rozwoju; licencja jest wymagana w środowisku produkcyjnym.  
- **Obsługiwane formaty?** BMP, PNG, JPEG, TIFF i wiele innych dzięki Aspose.Imaging.  
- **Wymagania wstępne?** Visual Studio, .NET 6+ (lub .NET Framework 4.6+), oraz Aspose.Imaging dla .NET.

## Co to jest rysowanie tekstu na obrazie przy użyciu Aspose.Imaging?
Aspose.Imaging udostępnia wysokopoziomowe API, które ukrywa niskopoziomowe wywołania GDI+. Korzystając z obiektu `Graphics` razem z `GraphicsPath`, możesz tworzyć wektorowe rysunki — tekst, kształty i wypełnienia wzorowane — i renderować je na bitmapie lub w dowolnym obsługiwanym formacie obrazu.

## Dlaczego rysować kształty na obrazie i wypełniać je wzorem?
- **Podkreślenie wizualne:** Wyróżnij obszary własnymi wzorami kreskowania.  
- **Branding:** Dodaj logotypy firmy lub znaki wodne łączące tekst i grafikę.  
- **Grafika dynamiczna:** Generuj wykresy, odznaki lub certyfikaty w locie bez zewnętrznych narzędzi projektowych.

## Wymagania wstępne

1. ** ** pobierz ze strony oficjalnej: [Download Aspose.Imaging for .NET](https://releases.aspose.com/imaging/net/).  
3. **Podstawowa znajomość C#** – powinieneś być zaznajomiony z klasami, przestrzeniami nazw i dyrektywą `using`.

## Importowanie przestrzeni nazw

Otwórz projekt i upewnij się, że dostępna jest przestrzeń nazw Aspose.Imaging:

```csharp
using Aspose.Imaging;
```

## Krok 1: Konfiguracja środowiska

Najpierw tworzymy pustą płaszczyznę, która będzie hostować nasze rysowanie.

```csharp
public static void Run()
{
    Console.WriteLine("Running example DrawingUsingGraphicsPath");
    string dataDir = "Your Document Directory";

    // Create an instance of BmpOptions and set its various properties
    BmpOptions ImageOptions = new BmpOptions();
    ImageOptions.BitsPerPixel = 24;

    // Create an instance of FileCreateSource and assign it to Source property
    ImageOptions.Source = new FileCreateSource(dataDir + "sample_1.bmp", false);

    // Create an instance of Image and initialize an instance of Graphics
    using (Image image = Image.Create(ImageOptions, 500, 500))
    {
        Graphics graphics = new Graphics(image);
        graphics.Clear(Color.White);
```

Tutaj konfigurowany jest obraz BMP o wymiarach 500 × 500 pikseli z białym tłem, gotowy do rysowania.

## Krok 2: Tworzenie GraphicsPath, dodawanie kształtów i tekstu

Teraz budujemy `GraphicsPath`, który zawiera zarówno kształty, **jak i tekst, który chcemy narysować na obrazie**.

```csharp
        GraphicsPath graphicspath = new GraphicsPath();
        Figure figure = new Figure();

        figure.AddShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
        figure.AddShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
        figure.AddShape(new TextShape("Aspose.Imaging", new RectangleF(170, 225, 170, 100), new Font("Arial", 20), StringFormat.GenericTypographic));

        graphicspath.AddFigures(new[] { figure });
```

- **EllipseShape** i **RectangleShape** pozwalają nam **rysować kształty na obrazie**.  
- **TextShape** to miejsce, w którym **rysujemy tekst na obrazie** – ciąg „Aspose.Imaging” zostanie wyrenderowany wewnątrz określonego prostokąta.

## Krok 3: Rysowanie ścieżki i wypełnianie wzorem kreskowania

Gdy ścieżka jest gotowa, obrysowujemy ją piórem, a następnie wypełniamy wnętrze pędzlem kreskowanym — to demonstruje **wypełnianie kształtów wzorem**.

```csharp
        graphics.DrawPath(new Pen(Color.Blue), graphicspath);

        // Create an instance of HatchBrush and set its properties
        HatchBrush hatchbrush = new HatchBrush();
        hatchbrush.BackgroundColor = Color.Brown;
        hatchbrush.ForegroundColor = Color.Blue;
        hatchbrush.HatchStyle = HatchStyle.Vertical;

        graphics.FillPath(hatchbrush, graphicspath);

        image.Save();
        Console.WriteLine("Processing completed successfully.");
    }
    Console.WriteLine("Finished example DrawingUsingGraphicsPath");
}
```

`HatchBrush` maluje pionowy niebieski wzór linii na brązowym tle, nadając kształtom charakterystyczny wygląd.

## Typowe przypadki użycia

| Scenariusz | Jak kod pomaga |
|------------|----------------|
| **Generowanie odznak** | Połącz logo firmy (elipsa), obramowanie (prostokąt) i imię pracownika (tekst) w jednym obrazie. |
| **Wykresy dynamiczne** | Rysuj kształty zależne od danych i oznaczaj je wartościami przy użyciu `TextShape`. |
| **Znakowanie wodne** | Renderuj półprzezroczysty tekst na istniejącym zdjęciu i wypełnij tło wzorem dla subtelnego brandingu. |

## Rozwiązywanie problemów i wskazówki

- **Ścieżki plików** – Upewnij się, że `dataDir` wskazuje na folder z prawami zapisu; w przeciwnym razie `FileCreateSource` zgłosi wyjątek.  
- **Kontrast kolorów** – Przy wypełnieniach wzorowanych wybieraj kolory pierwszego planu i tła zapewniające wystarczający kontrast dla czytelności.  
Image` zamiast `BmpOptions`, aby zmniejszyć zużycie pamięci.

## Najczęściej zadawane pytania

**P: Czy Aspose.Imaging dla .NET jest kompatybilny z najnowszymi frameworkami .NET?**  
O: Tak, biblioteka wspiera przekon PNG lub.Load` i wywołać `Save` z innym rozszerzeniem pliku.

**P: Gdzie znajdę bardziej szczegółową dokumentację?**  
O: Odwiedź oficjalną dokumentację pod adresem [Aspose.Imaging documentation](https://reference.aspose.com/imaging/net/).

**P: Czy dostępna jest darmowa wersja próbna?**  
O: Tak, wersję próbną możesz pobrać [tutaj](https://releases.aspose.com/).

**P: Jak zakupić licencję do użytku produkcyjnego?**  
O: Licencje można nabyć bezpośrednio w sklepie Aspose: [ten link](https://purchase.aspose.com/buy).

## Podsumowanie

Nauczyłeś się teraz, jak **rysować tekst na obrazie**, **rysować kształty na obrazie** oraz **wypełniać kształty wzorem** przy użyciu API `GraphicsPath` Aspose.Imaging. Dzięki tym elementom budulcowym możesz tworzyć bogatą, programową grafikę dla raportów, pulpitów nawigacyjnych lub dowolnych niestandardowych wyjść wizualnych w aplikacjach .NET.

Jeśli napotkasz problemy lub chcesz podzielić się swoimi projektami, zapraszamy do społeczności na [Aspose.Imaging Forum](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-01-30  
**Testowano z:** Aspose.Imaging 24.12 dla .NET  
**Autor:** Aspose