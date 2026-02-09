---
date: 2026-02-09
description: Leer hoe je een boog tekent met Aspose.Imaging voor .NET, inclusief hoe
  je een BMP‑bestand opslaat, de afbeeldingsgrootte instelt en de grafische achtergrond
  bepaalt. Stapsgewijze handleiding voor het genereren van BMP‑afbeeldingen.
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Hoe een boog te tekenen met Aspose.Imaging voor .NET
url: /nl/net/basic-drawing/draw-arc/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een boog te tekenen met Aspose.Imaging voor .NET

In de wereld van beeldverwerking is **how to draw arc** een veelvoorkomende taak die visuele flair aan elke afbeelding kan toevoegen. Met Aspose.Imaging voor .NET kun je BMP-afbeeldingen genereren, de afbeeldingsgrootte instellen en een boog tekenen met een pen in slechts een paar regels C#. Aan het einde van deze tutorial weet je precies hoe je een boog tekent, de achtergrond van de graphics instelt en het resulterende BMP‑bestand moeiteloos opslaat.

## Snelle antwoorden
- **What does the code produce?** Een 100 × 100 pixel BMP‑afbeelding met een gele achtergrond en een zwarte boog.  
- **Which library is used?** Aspose.Imaging voor .NET.  
- **Do I need a license?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Can I change the image size?** Ja – wijzig de breedte‑ en hoogte‑parameters in de `Image.Create`‑aanroep.  
- **Is the output format fixed?** Het voorbeeld slaat een BMP‑bestand op, maar elk formaat dat door Aspose.Imaging wordt ondersteund kan worden gebruikt.

## Wat is “how to draw arc” in Aspose.Imaging?
Een boog tekenen betekent het renderen van een gebogen lijnsegment dat wordt gedefinieerd door een begrenzende rechthoek, een starthoek en een sweep‑hoek. Aspose.Imaging biedt de `Graphics.DrawArc`‑methode, waarmee je **draw arc with pen** kunt uitvoeren en elk visueel aspect kunt beheersen.

## Waarom Aspose.Imaging voor deze taak gebruiken?
- **Full control** over afbeeldingsafmetingen, kleurdiepte en bestandsformaat.  
- **No external dependencies** – alles draait op pure .NET.  
- **High performance** voor het genereren van grote aantallen graphics aan de serverzijde.  

## Vereisten

Voordat we in de code duiken, zorg ervoor dat je het volgende hebt:

1. **Aspose.Imaging for .NET** – download het van de officiële site [here](https://releases.aspose.com/imaging/net/).  
2. **A .NET development environment** (Visual Studio, VS Code, of een C#‑compiler).  

Nu we onze vereisten klaar hebben, laten we beginnen met tekenen!

## Benodigde namespaces importeren

Om met Aspose.Imaging te werken moet je de relevante namespaces in scope brengen:

### Stap 1: De namespaces importeren

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

Deze `using`‑statements geven je toegang tot klassen voor het maken van afbeeldingen, graphics‑verwerking en bestands‑I/O.

## Hoe een boog te tekenen met Aspose.Imaging voor .NET

We splitsen het proces op in drie duidelijke stappen: de afbeelding maken, het graphics‑oppervlak voorbereiden en tenslotte de boog tekenen.

### Stap 1: De afbeelding instellen (afbeeldingsgrootte instellen & BMP‑afbeelding genereren)

```csharp
// Specify the directory where you want to save the image
string dataDir = "Your Document Directory";

// Create an instance of FileStream to save the image
using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
{
    // Create an instance of BmpOptions and set its properties
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;

    // Set the source for BmpOptions and create an instance of Image
    saveOptions.Source = new StreamSource(stream);
    using (Image image = Image.Create(saveOptions, 100, 100))
    {
```

Hier **set image size** we naar 100 × 100 pixels en configureren we de BMP‑opties. De `FileStream` zorgt ervoor dat we **save BMP file** naar de gewenste locatie.

### Stap 2: Graphics initialiseren en de graphics‑achtergrond instellen

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

Het `Graphics`‑object laat ons op de afbeelding tekenen. Door `Clear(Color.Yellow)` aan te roepen, **set graphics background** we naar een felgele kleur, waardoor de boog opvalt.

### Stap 3: Boog‑parameters definiëren en boog tekenen met pen

```csharp
        // Define the parameters for the arc
        int width = 100;
        int height = 200;
        int startAngle = 45;
        int sweepAngle = 270;

        // Draw the arc
        graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);

        // Save the changes
        image.Save();
    }
    stream.Close();
}
```

- `width` en `height` definiëren de begrenzende rechthoek, waardoor effectief **set image size** voor de boog wordt bepaald.  
- Het `Pen`‑object is wat ons in staat stelt **draw arc with pen** in het zwart uit te voeren.  
- Na het tekenen schrijft `image.Save()` het **BMP file** naar de schijf.

## Veelvoorkomende problemen & tips

- **Arc not visible?** Zorg ervoor dat de penkleur contrasteert met de achtergrond (bijv. zwart op geel).  
- **Incorrect dimensions?** Onthoud dat de begrenzende rechthoek van de boog groter kan zijn dan de afbeelding; pas `width`/`height` of de afbeeldingsgrootte dienovereenkomstig aan.  
- **Performance tip:** Hergebruik een enkele `Graphics`‑instantie als je meerdere vormen op dezelfde afbeelding moet tekenen.

## Veelgestelde vragen

### Q1: Waar kan ik de documentatie voor Aspose.Imaging voor .NET vinden?

A1: Je kunt de documentatie raadplegen [here](https://reference.aspose.com/imaging/net/) voor uitgebreide informatie over Aspose.Imaging voor .NET.

### Q2: Hoe kan ik Aspose.Imaging voor .NET downloaden?

A2: Je kunt Aspose.Imaging voor .NET downloaden van de website [here](https://releases.aspose.com/imaging/net/).

### Q3: Is er een gratis proefversie beschikbaar voor Aspose.Imaging voor .NET?

A3: Ja, je kunt een gratis proefversie krijgen [here](https://releases.aspose.com/) om Aspose.Imaging voor .NET uit te proberen.

### Q4: Heb ik een tijdelijke licentie nodig voor Aspose.Imaging voor .NET?

A4: Als je een tijdelijke licentie nodig hebt, kun je er een verkrijgen [here](https://purchase.aspose.com/temporary-license/).

### Q5: Waar kan ik ondersteuning zoeken of vragen stellen over Aspose.Imaging voor .NET?

A5: Je kunt het Aspose.Imaging‑forum bezoeken voor ondersteuning en discussies [here](https://forum.aspose.com/).

---

**Laatst bijgewerkt:** 2026-02-09  
**Getest met:** Aspose.Imaging 24.11 for .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}