---
"description": "Leer hoe u rasterafbeeldingen op SVG tekent met Aspose.Imaging voor .NET. Verbeter uw .NET-toepassingen met dynamische afbeeldingen."
"linktitle": "Rasterafbeelding tekenen op SVG in Aspose.Imaging voor .NET"
"second_title": "Aspose.Imaging .NET-beeldverwerkings-API"
"title": "Een rasterafbeelding tekenen op SVG in Aspose.Imaging voor .NET"
"url": "/nl/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Een rasterafbeelding tekenen op SVG in Aspose.Imaging voor .NET


In de wereld van .NET-programmering staat Aspose.Imaging bekend als een betrouwbare en veelzijdige bibliotheek voor het verwerken van diverse beeldgerelateerde taken. Een fascinerende mogelijkheid is de mogelijkheid om een rasterafbeelding op een SVG-canvas te tekenen. In deze stapsgewijze handleiding leiden we je door het proces van het tekenen van een rasterafbeelding op een SVG met Aspose.Imaging voor .NET.

## Vereisten

Voordat we in de details duiken, moet u ervoor zorgen dat u aan de volgende voorwaarden voldoet:

- Aspose.Imaging voor .NET: U moet de bibliotheek geïnstalleerd hebben. Zo niet, dan kunt u deze downloaden van de [Aspose.Imaging voor .NET downloadpagina](https://releases.aspose.com/imaging/net/).

- Uw documentenmap: vervangen `"Your Document Directory"` met het werkelijke pad naar uw werkdirectory.

Laten we het proces nu opsplitsen in eenvoudig te volgen stappen:

## Stap 1: Importeer de benodigde naamruimten

U moet de vereiste naamruimten importeren om met Aspose.Imaging te kunnen werken:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Stap 2: Afbeeldingen laden

- Laad eerst de rasterafbeelding die u wilt tekenen op het SVG-canvas.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Laad vervolgens de SVG-canvasafbeelding op de plek waar u de rasterafbeelding wilt tekenen.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Stap 3: Tekenen op de SVG-afbeelding

Nu kunt u beginnen met tekenen op de bestaande SVG-afbeelding. Hiervoor moet u een instantie van `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Stap 4: Teken de rasterafbeelding

- Definieer de grenzen waar u de rasterafbeelding wilt tekenen en geef het brongebied van de rasterafbeelding op.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Stap 5: Sla het resultaat op

Nadat u de rasterafbeelding op het SVG-canvas hebt getekend, kunt u de resulterende afbeelding opslaan:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Conclusie

Gefeliciteerd! Je hebt met succes een rasterafbeelding op een SVG-canvas getekend met Aspose.Imaging voor .NET. Dit kan ontzettend handig zijn voor het maken van rijke en dynamische afbeeldingen in je .NET-applicaties.

Voor meer informatie en gedetailleerde documentatie, bezoek de [Aspose.Imaging voor .NET-documentatie](https://reference.aspose.com/imaging/net/).

## Veelgestelde vragen

### Wat is Aspose.Imaging voor .NET?
   Aspose.Imaging voor .NET is een krachtige beeldverwerkingsbibliotheek waarmee ontwikkelaars afbeeldingen in verschillende formaten in .NET-toepassingen kunnen maken, bewerken en converteren.

### Kan ik Aspose.Imaging voor .NET gebruiken in commerciële projecten?
   Ja, u kunt Aspose.Imaging voor .NET gebruiken in zowel commerciële als niet-commerciële projecten. Licentiegegevens vindt u op de [aankooppagina](https://purchase.aspose.com/buy).

### Is er een gratis proefperiode beschikbaar?
   Ja, u kunt een gratis proefversie van Aspose.Imaging voor .NET krijgen van [hier](https://releases.aspose.com/).

### Waar kan ik ondersteuning krijgen of vragen stellen?
   Als u vragen heeft of ondersteuning nodig heeft, kunt u terecht op de [Aspose.Imaging forum](https://forum.aspose.com/).

### Hoe kan ik een tijdelijke licentie voor Aspose.Imaging voor .NET verkrijgen?
   U kunt een tijdelijke vergunning krijgen van [hier](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}