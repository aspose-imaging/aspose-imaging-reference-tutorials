---
"date": "2025-06-03"
"description": "Opanuj konwersję SVG do PDF z Aspose.Imaging .NET, zachowując jakość czcionek. Poznaj konfigurację katalogów, osadzanie czcionek i wiele więcej."
"title": "Efektywna konwersja SVG do PDF przy użyciu Aspose.Imaging .NET&#58; Zarządzanie czcionkami i techniki"
"url": "/pl/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Efektywna konwersja SVG do PDF przy użyciu Aspose.Imaging .NET

## Wstęp

Konwersja grafiki wektorowej do uniwersalnych formatów, takich jak PDF, ma kluczowe znaczenie dla udostępniania i drukowania dokumentów w dzisiejszej erze cyfrowej. Zachowanie integralności czcionek podczas tej konwersji może być trudne. Ten samouczek pokazuje bezproblemową konwersję SVG do PDF przy zachowaniu jakości czcionek za pomocą Aspose.Imaging dla .NET.

**Czego się nauczysz:**
- Konfigurowanie katalogów i eksportowanie plików SVG jako PDF.
- Techniki osadzania i eksportowania czcionek w plikach SVG.
- Implementacja niestandardowego modułu obsługi wywołań zwrotnych do zarządzania czcionkami SVG podczas procesu zapisywania.

Dzięki tym umiejętnościom możesz zapewnić, że Twoje dokumenty będą wyglądać profesjonalnie i spójnie na różnych platformach. Zacznijmy od skonfigurowania naszego środowiska!

## Wymagania wstępne

Zanim zagłębisz się w kod, upewnij się, że masz następujące elementy:

### Wymagane biblioteki
- **Aspose.Imaging dla .NET**:Niezbędne do obsługi konwersji obrazów.
- **Przestrzeń nazw System.IO**: Do operacji na plikach i katalogach.

### Konfiguracja środowiska
Upewnij się, że masz zgodne środowisko programistyczne, takie jak Visual Studio lub dowolne IDE obsługujące projekty .NET. Znajomość podstawowego programowania C# jest korzystna.

## Konfigurowanie Aspose.Imaging dla .NET

Aby użyć Aspose.Imaging w swoim projekcie, wykonaj następujące kroki instalacji:

**Korzystanie z interfejsu wiersza poleceń .NET:**
```bash
dotnet add package Aspose.Imaging
```

**Korzystanie z Menedżera pakietów:**
```powershell
Install-Package Aspose.Imaging
```

**Za pomocą interfejsu użytkownika Menedżera pakietów NuGet:**
Wyszukaj „Aspose.Imaging” i zainstaluj najnowszą wersję.

### Nabycie licencji
- **Bezpłatna wersja próbna**: Zacznij od bezpłatnego okresu próbnego, aby sprawdzić funkcje.
- **Licencja tymczasowa**:Uzyskaj tymczasową licencję na rozszerzoną ocenę.
- **Zakup**: Rozważ zakup, jeśli Aspose.Imaging spełnia Twoje potrzeby.

#### Inicjalizacja i konfiguracja
Aby użyć Aspose.Imaging, dodaj go jako zależność w swoim projekcie. Oto podstawowa konfiguracja:

```csharp
using Aspose.Imaging;
```

Zapewnij `Aspose.Imaging` przestrzeń nazw znajduje się na początku pliku i umożliwia dostęp do jego klas i metod.

## Przewodnik wdrażania

W tej sekcji każda funkcja jest rozbijana na łatwe do wykonania kroki.

### Konfiguracja katalogu i eksport SVG do PDF

#### Przegląd
Konwertuj plik SVG do PDF, upewniając się, że ścieżki katalogów wyjściowych są poprawnie skonfigurowane.

**Krok 1: Upewnij się, że katalog wyjściowy istnieje**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*Wyjaśnienie*:Ten fragment kodu sprawdza, czy katalog wyjściowy istnieje i w razie potrzeby go tworzy.

**Krok 2: Załaduj SVG i eksportuj do PDF**
```csharp
public void ReadAndExportToPdf(string inputFileName)
{
    string inputFile = Path.Combine(SourceFolder, inputFileName);
    string outFile = Path.Combine(OutFolder, inputFileName + ".pdf");
    
    using (Image image = Image.Load(inputFile))
    {
        image.Save(outFile,
            new PdfOptions { VectorRasterizationOptions = new SvgRasterizationOptions { PageSize = image.Size } });
    }
}
```
*Wyjaśnienie*:Ten `PdfOptions` umożliwiają konfigurację rasteryzacji zawartości SVG, zapewniając, że rozmiar strony odpowiada wymiarom oryginalnego obrazu.

### Zapisywanie SVG z opcjami osadzania czcionek

#### Przegląd
Zapisz plik SVG, kontrolując ustawienia osadzania czcionek w celu zachowania ich wierności.

**Krok 1: Zdefiniuj katalogi wyjściowe i czcionek**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*Wyjaśnienie*: Przed zapisaniem plików upewnij się, że katalogi są skonfigurowane.

**Krok 2: Zapisz SVG z niestandardowymi opcjami czcionki**
```csharp
public void Save(bool useEmbedded, string fileName, int expectedCountFonts)
{
    string fontStoreType = useEmbedded ? "Embedded" : "Stream";
    string inputFile = Path.Combine(SourceFolder, fileName);
    string outFileName = $"{Path.GetFileNameWithoutExtension(fileName)}_{fontStoreType}.svg";
    string outputFile = Path.Combine(OutFolder, outFileName);

    using (Image image = Image.Load(inputFile))
    {
        EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions
        {
            BackgroundColor = Color.White,
            PageWidth = image.Width,
            PageHeight = image.Height
        };

        string testingFileName = Path.GetFileNameWithoutExtension(inputFile);
        string fontFolder = Path.Combine(FontFolder, testingFileName);

        image.Save(outputFile,
            new SvgOptions
            {
                VectorRasterizationOptions = emfRasterizationOptions,
                Callback = new SvgCallbackFontTest(useEmbedded, fontFolder)
                {
                    Link = FontFolderName + "/" + testingFileName
                }
            });
    }

    if (!useEmbedded)
    {
        string[] files = Directory.GetFiles(fontFolder);
        if (files.Length != expectedCountFonts)
        {
            throw new Exception($"Expected count font files = {expectedCountFonts}, Current count font files = {files.Length}");
        }
    }
}
```
*Wyjaśnienie*:Metoda ta umożliwia określenie, czy czcionki mają być osadzone czy przesyłane strumieniowo, co ma wpływ na sposób ich przechowywania i dostępu do nich.

### Niestandardowy program obsługi wywołań zwrotnych czcionek SVG

#### Przegląd
Zaimplementuj niestandardowy moduł obsługi zasobów czcionek podczas zapisywania pliku SVG.

**Krok 1: Implementacja klasy SvgCallbackFontTest**
```csharp
public class SvgCallbackFontTest : SvgResourceKeeperCallback
{
    private readonly string outFolder;
    private readonly bool useEmbeddedFont;
    private int fontCounter = 0;

    public string Link { get; set; }

    public SvgCallbackFontTest(bool useEmbeddedFont, string outFolder)
    {
        this.useEmbeddedFont = useEmbeddedFont;
        this.outFolder = outFolder;
        
        if (Directory.Exists(outFolder))
        {
            Directory.Delete(this.outFolder, true);
        }
    }

    public override void OnFontResourceReady(FontStoringArgs args)
    {
        if (this.useEmbeddedFont)
        {
            args.FontStoreType = FontStoreType.Embedded;
        }
        else
        {
            args.FontStoreType = FontStoreType.Stream;
            string fontFolder = this.outFolder;

            if (!Directory.Exists(fontFolder))
            {
                Directory.CreateDirectory(fontFolder);
            }

            string fName = args.SourceFontFileName;
            if (!File.Exists(fName))
            {
                fName = $"font_{this.fontCounter++}.ttf";
            }

            string fileName = Path.Combine(fontFolder, Path.GetFileName(fName));
            
            args.DestFontStream = new FileStream(fileName, FileMode.OpenOrCreate);
            args.DisposeStream = true;
            args.FontFileUri = $".{this.Link}/{Path.GetFileName(fName)}";
        }
    }
}
```
*Wyjaśnienie*: Ta klasa obsługuje zasoby czcionek, decydując, czy osadzić je bezpośrednio, czy przechowywać osobno. Zapewnia, że czcionki są poprawnie odwoływane i zapisywane podczas procesu eksportu SVG.

## Zastosowania praktyczne

1. **Automatyczne generowanie raportów**: Użyj Aspose.Imaging do konwersji projektów do plików PDF w celu zapewnienia spójnej dystrybucji.
2. **Publikacje cyfrowe**:Zapewnij wysoką jakość renderowania czcionek podczas konwersji artykułów z osadzoną grafiką z formatu SVG do formatu PDF.
3. **Udostępnianie dokumentów między platformami**:Zachowaj integralność wizualną dokumentów współdzielonych między różnymi systemami operacyjnymi.

## Rozważania dotyczące wydajności

### Wskazówki dotyczące optymalizacji wydajności
- Stosuj efektywne praktyki zarządzania plikami, np. usuwaj strumienie niezwłocznie po wykorzystaniu.
- Zminimalizuj użycie pamięci poprzez usunięcie nieużywanych obiektów i katalogów po zakończeniu przetwarzania.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}