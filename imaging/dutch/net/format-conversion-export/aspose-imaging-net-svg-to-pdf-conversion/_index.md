---
"date": "2025-06-03"
"description": "Beheers de SVG-naar-PDF-conversie met Aspose.Imaging .NET, met behoud van de lettertypekwaliteit. Leer hoe u mappen kunt instellen, lettertypen kunt insluiten en meer."
"title": "Efficiënte SVG naar PDF-conversie met Aspose.Imaging .NET-lettertypebeheer en -technieken"
"url": "/nl/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Efficiënte SVG naar PDF-conversie met Aspose.Imaging .NET

## Invoering

Het converteren van vectorafbeeldingen naar veelzijdige formaten zoals PDF is cruciaal voor het delen en afdrukken van documenten in het huidige digitale tijdperk. Het behouden van de lettertype-integriteit tijdens deze conversie kan een uitdaging zijn. Deze tutorial demonstreert naadloze SVG-naar-PDF-conversie met behoud van de lettertypekwaliteit met behulp van Aspose.Imaging voor .NET.

**Wat je leert:**
- Mappen instellen en SVG-bestanden exporteren als PDF's.
- Technieken voor het insluiten of exporteren van lettertypen in SVG-bestanden.
- Implementeren van een aangepaste callback-handler voor het beheren van SVG-lettertypen tijdens het opslagproces.

Met deze vaardigheden kunt u ervoor zorgen dat uw documenten er professioneel en consistent uitzien op verschillende platforms. Laten we beginnen met het instellen van onze omgeving!

## Vereisten

Voordat u de code induikt, moet u ervoor zorgen dat u het volgende hebt:

### Vereiste bibliotheken
- **Aspose.Imaging voor .NET**:Onmisbaar voor het verwerken van beeldconversies.
- **System.IO-naamruimte**: Voor bestands- en directorybewerkingen.

### Omgevingsinstelling
Zorg ervoor dat je een compatibele ontwikkelomgeving hebt, zoals Visual Studio of een IDE die .NET-projecten ondersteunt. Kennis van basis C#-programmering is een pré.

## Aspose.Imaging instellen voor .NET

Om Aspose.Imaging in uw project te gebruiken, volgt u deze installatiestappen:

**Met behulp van .NET CLI:**
```bash
dotnet add package Aspose.Imaging
```

**Pakketbeheer gebruiken:**
```powershell
Install-Package Aspose.Imaging
```

**Via de NuGet Package Manager-gebruikersinterface:**
Zoek naar "Aspose.Imaging" en installeer de nieuwste versie.

### Licentieverwerving
- **Gratis proefperiode**: Begin met een gratis proefperiode om de functies uit te proberen.
- **Tijdelijke licentie**: Vraag een tijdelijke vergunning aan voor uitgebreide evaluatie.
- **Aankoop**: Overweeg de aankoop als Aspose.Imaging aan uw behoeften voldoet.

#### Initialisatie en installatie
Om Aspose.Imaging te gebruiken, voegt u het toe als afhankelijkheid in uw project. Hier is een basisconfiguratie:

```csharp
using Aspose.Imaging;
```

Zorg ervoor dat de `Aspose.Imaging` De naamruimte wordt bovenaan uw bestand opgenomen om toegang te krijgen tot de klassen en methoden.

## Implementatiegids

In dit gedeelte wordt elke functie opgesplitst in beheersbare stappen.

### Directory-instellingen en SVG-export naar PDF

#### Overzicht
Converteer een SVG-bestand naar een PDF en zorg ervoor dat de directorypaden correct zijn ingesteld voor de uitvoer.

**Stap 1: Zorg ervoor dat de uitvoermap bestaat**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*Uitleg*:Dit codefragment controleert of de uitvoermap bestaat en maakt deze indien nodig aan.

**Stap 2: SVG laden en exporteren naar PDF**
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
*Uitleg*: De `PdfOptions` Hiermee kunt u de rastering van SVG-inhoud configureren, zodat de paginagrootte overeenkomt met de originele afmetingen van de afbeelding.

### SVG opslaan met opties voor het insluiten van lettertypen

#### Overzicht
Sla een SVG-bestand op en beheer de instellingen voor het insluiten van het lettertype om de lettertypegetrouwheid te behouden.

**Stap 1: Definieer uitvoer- en lettertypemappen**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*Uitleg*: Zorg ervoor dat de mappen zijn ingesteld voordat u bestanden opslaat.

**Stap 2: SVG opslaan met aangepaste lettertype-opties**
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
*Uitleg*:Met deze methode kunt u opgeven of lettertypen moeten worden ingesloten of gestreamd. Dit beïnvloedt de manier waarop ze worden opgeslagen en geopend.

### Aangepaste SVG-lettertype-callbackhandler

#### Overzicht
Implementeer een aangepaste handler om lettertypebronnen te beheren tijdens het opslaan van SVG.

**Stap 1: Implementeer de SVGCallbackFontTest-klasse**
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
*Uitleg*: Deze klasse beheert lettertypebronnen door te bepalen of ze direct moeten worden ingesloten of apart moeten worden opgeslagen. Dit zorgt ervoor dat lettertypen correct worden gerefereerd en opgeslagen tijdens het SVG-exportproces.

## Praktische toepassingen

1. **Geautomatiseerde rapportgeneratie**: Gebruik Aspose.Imaging om ontwerpschetsen om te zetten in PDF's voor consistente distributie.
2. **Digitaal publiceren**Zorg voor een hoogwaardige lettertypeweergave bij het converteren van artikelen met ingesloten afbeeldingen van SVG naar PDF.
3. **Documenten delen op meerdere platforms**: Behoud de visuele integriteit van documenten die tussen verschillende besturingssystemen worden gedeeld.

## Prestatieoverwegingen

### Tips voor het optimaliseren van prestaties
- Ga efficiënt om met bestanden, bijvoorbeeld door streams direct na gebruik weg te gooien.
- Minimaliseer het geheugengebruik door ongebruikte objecten en mappen te wissen zodra de verwerking is voltooid.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}