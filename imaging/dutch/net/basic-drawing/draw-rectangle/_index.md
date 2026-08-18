---
date: 2026-02-12
description: Leer hoe je een lege afbeelding maakt met Aspose en hoe je een rechthoek
  tekent in .NET met Aspose.Imaging – een snelle gids voor beeldmanipulatie in je
  .NET-toepassingen.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Maak een lege afbeelding met Aspose – Teken rechthoeken in .NET
url: /nl/net/basic-drawing/draw-rectangle/
weight: 14
---

NET"

**Author:** Aspose -> "**Auteur:** Aspose"

Make sure to keep bold formatting.

Now produce final content with all sections.

Check we didn't miss any markdown formatting.

Make sure code block placeholders remain as is (they are not fenced code blocks but placeholders). The instruction says preserve code blocks: there are placeholders but not actual fenced blocks. That's fine.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Maak lege afbeelding Aspose – Teken rechthoeken in .NET

Het maken en manipuleren van afbeeldingen in .NET‑toepassingen kan ontmoedigend aanvoelen, maar met Aspose.Imaging kun je **create blank image Aspose** maken in slechts een paar regels code en vervolgens vormen erop tekenen. In deze tutorial lopen we het volledige proces door — van het opzetten van een leeg canvas tot het tekenen van rechthoeken—zodat je meteen grafische elementen aan je .NET‑projecten kunt toevoegen.

## Snelle antwoorden
- **Wat betekent “create blank image Aspose”?** Het betekent het genereren van een lege bitmap met behulp van de Aspose.Imaging API.  
- **Hoe teken je een rechthoek in .NET met Aspose?** Gebruik de `Graphics.DrawRectangle`‑methode na het initialiseren van een `Graphics`‑object.  
- **Welk NuGet‑pakket is vereist?** `Aspose.Imaging` (nieuwste versie).  
- **Kan ik de afbeelding opslaan als PNG, JPEG of BMP?** Ja – wijzig gewoon de afbeeldingsopties (bijv. `BmpOptions`, `JpegOptions`).  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor evaluatie; een commerciële licentie is vereist voor productie.

## Wat is “create blank image Aspose”?
Een lege afbeelding maken betekent het toewijzen van een pixelbuffer met een gedefinieerde breedte, hoogte en pixelindeling. Aspose.Imaging behandelt de low‑level details en biedt je een kant‑klaar canvas om op te tekenen zonder dat je met GDI+ of System.Drawing hoeft te werken.

## Waarom Aspose.Imaging gebruiken voor het tekenen van rechthoeken in .NET?
- **Cross‑platform** – werkt op Windows, Linux en macOS.  
- **Geen native afhankelijkheden** – pure managed code, perfect voor serveromgevingen.  
- **Rijke teken‑API** – ondersteunt pennen, penselen, anti‑aliasing en vele vormtypen.  
- **Hoge prestaties** – geoptimaliseerd voor grote afbeeldingen en batchverwerking.

## Vereisten

1. **Aspose.Imaging for .NET** – download het van de [downloadpagina](https://releases.aspose.com/imaging/net/).  
2. **Ontwikkelomgeving** – Visual Studio, VS Code, of een andere .NET‑compatibele IDE.  
3. **.NET runtime** – .NET 6+ of .NET Framework 4.7.2+.  

Nu we alles hebben ingesteld, duiken we in de code.

## Hoe maak je een lege afbeelding Aspose in .NET?

### Stap 1: Importeer de benodigde namespaces

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Deze namespaces geven je toegang tot de kern‑imagingklassen, penseeltypes en opties voor het opslaan van afbeeldingen.

### Stap 2: Maak een lege afbeelding (het canvas)

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

In dit blok doen we:

* Definieer de uitvoerlokatie (`dataDir`).  
* Configureer `BmpOptions` om een 32‑bit pixelindeling te gebruiken.  
* Maak een **blank image** van 100 × 100 pixels.  

### Stap 3: Hoe teken je een rechthoek in .NET met Aspose.Imaging

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` vult het canvas met een achtergrondkleur (geel in dit voorbeeld).  
* `DrawRectangle` tekent twee rechthoeken—een met een eenvoudige rode pen, een andere met een blauwe effen penseel—voor visueel contrast.

### Stap 4: Sla de afbeelding op

```csharp
image.Save();
```

Het aanroepen van `Save` schrijft de bitmap naar het bestandssysteem met de eerder gedefinieerde opties.

## Veelvoorkomende problemen & tips

| Issue | Reason | Fix |
|-------|--------|-----|
| **Lege afbeelding verschijnt zwart** | Achtergrond niet gewist | Roep `graphic.Clear(Color.YourColor)` aan vóór het tekenen. |
| **File not found exception** | `dataDir` wijst naar een niet‑bestaande map | Zorg dat de map bestaat of gebruik `Path.Combine` met `Environment.CurrentDirectory`. |
| **Onjuiste kleuren** | Gebruik van `System.Drawing.Color` in plaats van `Aspose.Imaging.Color` | Importeer altijd `Aspose.Imaging.Color`. |
| **Prestatievertraging bij grote afbeeldingen** | Gebruik van standaard `BmpOptions` met veel bits per pixel | Schakel over naar `JpegOptions` of `PngOptions` voor compressie. |

## Veelgestelde vragen (Uitgebreid)

**Q: Kan ik andere vormen tekenen naast rechthoeken?**  
A: Absoluut. Aspose.Imaging biedt methoden zoals `DrawEllipse`, `DrawLine` en `DrawPolygon`.

**Q: Is de bibliotheek gratis voor commercieel gebruik?**  
A: Nee, Aspose.Imaging is een commercieel product, maar je kunt het evalueren met een gratis proefversie die beschikbaar is [hier](https://releases.aspose.com/).

**Q: Werkt dit zowel op Windows- als webapplicaties?**  
A: Ja, dezelfde code werkt in ASP.NET, Blazor en console‑apps.

**Q: Hoe wijzig ik het uitvoerformaat naar PNG?**  
A: Vervang `BmpOptions` door `PngOptions` en pas de bestandsextensie dienovereenkomstig aan.

**Q: Waar kan ik meer gedetailleerde documentatie vinden?**  
A: Toegang tot de volledige API‑referentie [hier](https://reference.aspose.com/imaging/net/) en sluit je aan bij de community op het [Aspose.Imaging‑forum](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2026-02-12  
**Getest met:** Aspose.Imaging 24.12 voor .NET  
**Auteur:** Aspose