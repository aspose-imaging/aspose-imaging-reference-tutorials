---
"date": "2025-06-03"
"description": "Zvládněte převod SVG do PDF pomocí Aspose.Imaging .NET se zachováním kvality písma. Naučte se nastavení adresářů, vkládání písem a další."
"title": "Efektivní převod SVG do PDF pomocí správy písem a technik v .NET v Aspose.Imaging"
"url": "/cs/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Efektivní převod SVG do PDF pomocí Aspose.Imaging .NET

## Zavedení

Převod vektorové grafiky do univerzálních formátů, jako je PDF, je v dnešní digitální době klíčový pro sdílení a tisk dokumentů. Zachování integrity písma během této konverze může být náročné. Tento tutoriál demonstruje bezproblémovou konverzi SVG do PDF se zachováním kvality písma pomocí Aspose.Imaging pro .NET.

**Co se naučíte:**
- Nastavení adresářů a export souborů SVG do formátu PDF.
- Techniky pro vkládání nebo export písem v souborech SVG.
- Implementace vlastního obslužného programu zpětného volání pro správu SVG fontů během procesu ukládání.

těmito dovednostmi si můžete zajistit, aby vaše dokumenty vypadaly profesionálně a konzistentně napříč různými platformami. Začněme nastavením našeho prostředí!

## Předpoklady

Než se ponoříte do kódu, ujistěte se, že máte následující:

### Požadované knihovny
- **Aspose.Imaging pro .NET**Nezbytné pro zpracování konverzí obrázků.
- **Jmenný prostor System.IO**Pro operace se soubory a adresáři.

### Nastavení prostředí
Ujistěte se, že máte kompatibilní vývojové prostředí, jako je Visual Studio nebo jakékoli IDE podporující projekty .NET. Znalost základů programování v C# je výhodou.

## Nastavení Aspose.Imaging pro .NET

Chcete-li ve svém projektu použít Aspose.Imaging, postupujte podle těchto kroků instalace:

**Použití .NET CLI:**
```bash
dotnet add package Aspose.Imaging
```

**Používání Správce balíčků:**
```powershell
Install-Package Aspose.Imaging
```

**Prostřednictvím uživatelského rozhraní Správce balíčků NuGet:**
Vyhledejte „Aspose.Imaging“ a nainstalujte nejnovější verzi.

### Získání licence
- **Bezplatná zkušební verze**Začněte s bezplatnou zkušební verzí a otestujte si funkce.
- **Dočasná licence**Získejte dočasnou licenci pro rozšířené vyhodnocení.
- **Nákup**Pokud Aspose.Imaging splňuje vaše potřeby, zvažte nákup.

#### Inicializace a nastavení
Chcete-li použít Aspose.Imaging, přidejte jej jako závislost do svého projektu. Zde je základní nastavení:

```csharp
using Aspose.Imaging;
```

Zajistěte, aby `Aspose.Imaging` jmenný prostor je zahrnut na začátku souboru pro přístup k jeho třídám a metodám.

## Průvodce implementací

Tato část rozděluje každou funkci na zvládnutelné kroky.

### Nastavení adresáře a export SVG do PDF

#### Přehled
Převeďte soubor SVG do PDF a zároveň zajistěte, aby byly cesty k adresářům správně nastaveny pro výstup.

**Krok 1: Zajistěte existenci výstupního adresáře**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*Vysvětlení*Tento úryvek kódu kontroluje, zda výstupní adresář existuje, a v případě potřeby jej vytvoří.

**Krok 2: Načtení SVG a export do PDF**
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
*Vysvětlení*: Ten `PdfOptions` umožňují konfiguraci rastrování SVG obsahu a zajištění toho, aby velikost stránky odpovídala původním rozměrům obrázku.

### Ukládání SVG s možnostmi vkládání písem

#### Přehled
Uložte soubor SVG a zároveň upravte nastavení vkládání písem, abyste zachovali věrnost písma.

**Krok 1: Definování výstupních a fontových adresářů**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*Vysvětlení*Před uložením souborů se ujistěte, že jsou nastaveny adresáře.

**Krok 2: Uložení SVG s vlastními možnostmi písma**
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
*Vysvětlení*Tato metoda umožňuje určit, zda mají být písma vložena nebo streamována, což ovlivňuje způsob jejich ukládání a přístupu k nim.

### Obslužná rutina zpětného volání vlastního písma SVG

#### Přehled
Implementujte vlastní obslužnou rutinu pro správu zdrojů písma během ukládání SVG.

**Krok 1: Implementace třídy SvgCallbackFontTest**
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
*Vysvětlení*Tato třída zpracovává zdroje písem tím, že rozhoduje, zda je vložit přímo, nebo je uložit samostatně. Zajišťuje, aby se na písma správně odkazovalo a ukládalo během procesu exportu SVG.

## Praktické aplikace

1. **Automatizované generování reportů**: Pro konzistentní distribuci použijte Aspose.Imaging k převodu návrhů do PDF.
2. **Digitální publikování**Zajistěte vysoce kvalitní vykreslování písma při převodu článků s vloženou grafikou z formátu SVG do formátu PDF.
3. **Sdílení dokumentů napříč platformami**Zachovat vizuální integritu dokumentů sdílených mezi různými operačními systémy.

## Úvahy o výkonu

### Tipy pro optimalizaci výkonu
- Používejte efektivní postupy pro práci se soubory, například likvidujte streamy ihned po použití.
- Minimalizujte využití paměti vymazáním nepoužívaných objektů a adresářů po dokončení zpracování.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}