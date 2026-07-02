---
date: '2026-01-30'
description: Leer hoe je PNG's met tekst maakt, strings uitlijnt en links-, gecentreerde
  of rechts uitgelijnde tekst tekent in .NET met Aspose.Imaging.
keywords:
- Aspose.Imaging for .NET
- string alignment in .NET
- drawing strings in C#
title: Maak PNG met tekst en rangschik strings met Aspose.Imaging
url: /nl/net/advanced-drawing-graphics/aspose-imaging-net-string-alignment-guide/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# PNG maken met Tekst en Strings Uitlijnen met Aspose.Imaging

## Inleiding

Als je **PNG met tekst wilt maken** en de uitlijning wilt regelen—links, gecentreerd of rechts—dan biedt deze gids alles wat je nodig hebt. In moderne .NET‑toepassingen is het tekenen van tekst op afbeeldingen een veelvoorkomende eis voor rapportgeneratie, dynamische graphics en geautomatiseerde document‑ het proces van het gebruik van **Aspose.Imaging voor .NET** om strings te tekenen, de string‑grootte te meten en ze nauwkeurig op een PNG‑canvas te positioneren.

### Wat je zult leren
- Hoe- Technieken om **tekst te centreren op afbeelding** en links uitgelijnde tekst te tekenen
- Prestatie‑tips voor het verwerken van grote batches afbeeldingen

Nu je weet wat we gaan bereiken, laten we de omgeving gereedmaken.

## Snelle Antwoorden
- **Wat betekent “PNG met tekst maken”?** Een PNG‑afbeelding genereren die gerenderde tekst bevat.
- **Welke biedt ingebouwde uitlijningsondersteuning.
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een betaalde licentie is vereist voor productie.
- **Kan ik tekst centreren op afbeelding?** Ja—gebruik `StringAlignment.Center` in de `StringFormat`.
- **Is het meten van string‑grootte noodzakelijk?** Absoluut; het zorgt ervoor dat tekst past en correct wordt uitgelijnd.

## Wat betekent “PNG met tekst maken”?
Een PNG met tekst maken betekent dat je programmatisch een PNG‑afbeeldingsbestand genereert en één of meer strings erop rendert. Dit is nuttig voor dynamische graphics, watermerken of aangepaste rapport‑koppen.

## Waarom Aspose.Imaging voor .NET gebruiken?
Aspose.Imaging biedt een rijke API die low‑level GDI+ details abstraheert, cross‑platform ondersteuning levert en geavanceerde functies bevat zoals precieze string‑meting en uitlijning zonder extra afhankelijkheden.

## Vereisten
- **Aspose.Imaging voor .NET** (nieuwste versie via NuGet)
- **.NET Core 3.0** of later (inclusief .NET 6/7)
- Basiskennis vanI/O. Volg deze stappen om het in je project te integreren:

### Installatie‑informatie
#### Met de .NET CLI
```bash
dotnet add package Aspose.Imaging
```

#### Met Package Manager
```powershell
Install-Package Aspose.Imaging
```

#### Met de NuGet Package Manager UI
Navigeer naar de NuGet Package Manager in je IDE, zoek naar "Aspose.Imaging" en installeer de nieuwste versie.

### Stappen voor Licentie‑verwerving
1. **Gratis proefversie**: Begin met een gratis proefversie door de bibliotheek te downloaden van [Aspose's website](https://releases.aspose.com/imaging/net/).
2. **Tijdelijke licentie**: Verkrijg een tijdelijke licentie als je de volledige functionaliteit zonder beperkingen wilt verkennen.
3. **Aankoop**: Overweeg een licentie aan te schaffen voor productiegebruik.

### Basisinitialisatie en Setup
```csharp
using Aspose.Imaging;
```

Nu onze setup compleet is, duiken we in de implementatie.

## Implementatie‑gids
Deze sectie leidt je stap voor stap door het **maken van PNG met tekst** en het correct uitlijnen ervan.

### Hoe PNG met Tekst Maken en Strings Uitlijnen
#### Overzicht
De onderstaande code toont hoe je links‑uitgelijnde, gecentreerde en rechts‑uitgelijnde tekst op een PNG‑afbeelding tekent. Het laat ook zien hoe je **string‑grootte meet C#** om elke regel precies te positioneren.

#### Stapsgewijze Instructies
##### Stap 1: Bestands‑paden, Uitlijningen, Lettertypen en Groottes Definiëren
We beginnen met het declareren van de output‑map, de uitlijningsopties die we zullen doorlopen, en een collectie van lettertypen en groottes om te demonstreren.
```csharp
string baseFolder = "YOUR_DOCUMENT_DIRECTORY";
string[] alignments = new[] { "Left", "Center", "Right" };
string[] fontNames = new[] { "Arial", "Times New Roman", "Bookman Old Style", "Calibri", "Comic Sans MS",
    "Courier New", "Microsoft Sans Serif", "Tahoma", "Verdana", "Proxima Nova Rg" };
float[] fontSizes = new[] { 10f, 22f, 50f, 100f };
```

##### Stap 2: Output‑bestand Maken en Afbeeldingsopties Configureren
Voor elke uitlijning genereren we een aparte PNG‑file. Het `PngOptions`‑object vertelt Aspose.Imaging hoe de afbeelding moet worden weggeschreven.
```csharp
string fileName = "output_" + align + ".png";
string outputFileName = Path.Combine(baseFolder, fileName);

using (FileStream stream = new FileStream(outputFileName, FileMode.Create))
{
    Aspose.Imaging.ImageOptions.PngOptions pngOptions = new Aspose.Imaging.ImageOptions.PngOptions();
    pngOptions.Source = new Aspose.Imaging.Sources.StreamSource(stream);
}
```

##### Stap 3: Graphics Initialiseren, Achtergrond Wissen en Penselen Voorbereiden
We maken het afbeeldingscanvas, wissen het naar wit, en stellen een zwarte pen voor tekst en een rode pen voor hulplijnen in.
```csharp
using (Aspose.Imaging.Image image = Aspose.Imaging.Image.Create(pngOptions, width, height))
{
    Aspose.Imaging.Graphics graphics = new Aspose.Imaging.Graphics(image);
    graphics.Clear(Aspose.Imaging.Color.White);

    SolidBrush brush = new SolidBrush(Color.Black);
    Pen pen = new Pen(Color.Red, 1);
}
```

##### Stap 4: Strings Tekenen met de Gewenste Uitlijning
Hier koppelen we onze tekst‑uitlijningskeuze aan `StringAlignment`, maken we een `StringFormat` aan en renderen we elke regel. Dit demonstreert ook **hoe je tekst tekent** links, gecentreerd of rechts uitgelijnd.
```csharp
StringAlignment alignment = align switch
{
    "Left" => StringAlignment.Near,
    "Center" => StringAlignment.Center,
    "Right" => StringAlignment.Far,
    _ => StringAlignment.Near,
};

StringFormat stringFormat = new StringFormat(StringFormatFlags.ExactAlignment) { Alignment = alignment };

foreach (var fontName in fontNames)
{
    foreach (var fontSize in fontSizes)
    {
        Font font = new Font(fontName, fontSize);
        string text = $"This is font: {fontName}, size:{fontSize}";
        SizeF textSize = graphics.MeasureString(text, font, SizeF.Empty, null); // **measure string size C#**

        graphics.DrawString(text, font, brush, new RectangleF(x, y, w, textSize.Height), stringFormat);
        y += textSize.Height;
    }

    graphics.DrawLine(pen, new Point((int)x, (int)y), new Point((int)(x + w), (int)y));
}

graphics.DrawLine(pen, new Point(lineX, 0), new Point(lineX, (int)y));
```

##### Stap 5: Afbeelding Opslaan en Opruimen
Tot slot schrijven we de PNG naar schijf en verwijderen we eventueel het tijdelijke stream‑bestand.
```csharp
image.Save();
File.Delete(outputFileName);
```

### Probleemoplossingstips
- **Afbeelding wordt niet opgeslagen** – Controleer of de output‑directory bestaat en of je schrijfrechten hebt.
- **Verkeerde uitlijning** – Controleer de `StringAlignment`‑mapping; `StringAlignment.Near` tekent links‑uitgelijnde tekst.
- **Onverwachte lettertype‑rendering** – Zorg ervoor dat de gekozen lettertypen op de host‑machine geïnstalleerd zijn.

## Praktische Toepassingen
1. **Rapportgeneratie** – Voeg automatisch links‑uitgelijnde koppen, gecentreerde titels en rechts‑uitgelijnde voetteksten toe.
2. **Dynamische Bannercreatie** – Genereer marketing‑banners waarbij tekst precies gecentreerd moet zijn.
3. **Documentautomatisering** – Plaats uitgelijnde tekst in afbeelding‑gebaseerde sjablonen voor facturen of certificaten.

## Prestatie‑overwegingen
- **Afbeeldingen verstandig schalen** – Kies de kleinste afmetingen die nog aan de kwaliteitsvereisten voldoen.
- **Objecten vrijgeven** – Gebruik `using`‑statements (zoals getoond) om onbeheerste resources snel vrij te geven.
- **Batch‑verwerking** – Bij het maken van veel PNG’s, hergebruik `PngOptions` en wijzig alleen het tekenoppervlak.

## Conclusie
Je weet nu hoe je **PNG met tekst maakt**, string‑dimensies meet en de inhoud precies uitlijnt waar je het nodig hebt. Door gebruik te maken van de robuuste API van Aspose.Imaging kun je geavanceerde tekst‑rendering toevoegen aan elke .NET‑applicatie.

### Volgende Stappen
- Experimenteer met extra teken‑features zoals schaduwen of contouren.
- Combineer tekst‑rendering met afbeeldingsfilters voor rijkere graphics.
- Integreer deze routine in een grotere document‑generatie‑pipeline.

## FAQ‑sectie
1. **Wat is Aspose.Imaging voor .NET?**  
   - Een krachtige bibliotheek voor het verwerken van afbeeldingen, inclusief het tekenen van tekst met verschillende uitlijningen.
2. **Hoe stel ik Aspose.Imaging voor .NET in?**  
   - Installeer via NuGet Package Manager of CLI zoals beschreven in de setup‑sectie.

**Q: Kan ik deze code gebruiken om tekst te centreren op afbeelding?**  
A: Ja—stel de uitlijning in op `StringAlignment.Center` zoals gedemonstreerd in Stap 4.

**Q: Hoe meet ik string‑grootte in C#?**  
A: Gebruik `graphics.MeasureString`, dat een `SizeF` retourneert die de gerenderde afmetingen weergeeft.

**Q: Wat als ik alleen links‑uitgelijnde tekst wil tekenen?**  
A: Gebruik `StringAlignment.Near` (of `StringAlignment.Far` voor rechts) bij het construeren van de `StringFormat`.

**Q: Ondersteunt Aspose.Imaging andere afbeeldingsformaten?**  
A: Absoluut; je kunt JPEG BMP, TIFF en meer maken door de `ImageOptions`‑klasse te vervangen.

**Q: Is een licentie vereist voor productie?**  
A: Ja—schaf een licentie aan om het evaluatiewatermerk te verwijderen en volledige functionaliteit te ontgrendelen.

---

**Laatst bijgewerkt:** 2026-01-30  
**Getest met:** Aspose.Imaging 24.12 voor .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}