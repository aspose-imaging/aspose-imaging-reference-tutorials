---
title: Een rasterafbeelding tekenen op SVG in Aspose.Imaging voor .NET
linktitle: Teken een rasterafbeelding op SVG in Aspose.Imaging voor .NET
second_title: Aspose.Imaging .NET-API voor beeldverwerking
description: Leer hoe u rasterafbeeldingen tekent op SVG met Aspose.Imaging voor .NET. Verbeter uw .NET-applicaties met dynamische afbeeldingen.
type: docs
weight: 11
url: /nl/net/vector-image-processing/draw-raster-image-on-svg/
---

In de wereld van .NET-programmeren staat Aspose.Imaging als een betrouwbare en veelzijdige bibliotheek voor het afhandelen van verschillende beeldgerelateerde taken. Een fascinerende mogelijkheid die het biedt, is de mogelijkheid om een rasterafbeelding op een SVG-canvas te tekenen. In deze stapsgewijze handleiding leiden we u door het proces van het tekenen van een rasterafbeelding op een SVG met behulp van Aspose.Imaging voor .NET.

## Vereisten

Voordat we ingaan op de details, zorg ervoor dat u aan de volgende vereisten voldoet:

-  Aspose.Imaging voor .NET: U moet de bibliotheek geïnstalleerd hebben. Als dit niet het geval is, kunt u deze downloaden van de[Aspose.Imaging voor .NET-downloadpagina](https://releases.aspose.com/imaging/net/).

-  Uw documentenmap: Vervangen`"Your Document Directory"` met het daadwerkelijke pad naar uw werkmap.

Laten we het proces nu opsplitsen in eenvoudig te volgen stappen:

## Stap 1: Importeer de benodigde naamruimten

U moet de vereiste naamruimten importeren om met Aspose.Imaging te kunnen werken:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Stap 2: Laad de afbeeldingen

- Laad eerst de rasterafbeelding die u op het SVG-canvas wilt tekenen.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Laad vervolgens de SVG-canvasafbeelding op de plek waar u de rasterafbeelding wilt tekenen.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Stap 3: Tekenen op de SVG-afbeelding

Nu kunt u beginnen met tekenen op de bestaande SVG-afbeelding. Om dit te doen, moet u een exemplaar van`SvgGraphics2D`:

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

Gefeliciteerd! U hebt met succes een rasterafbeelding op een SVG-canvas getekend met Aspose.Imaging voor .NET. Dit kan ongelooflijk handig zijn voor het maken van rijke en dynamische afbeeldingen binnen uw .NET-toepassingen.

 Voor meer informatie en gedetailleerde documentatie kunt u terecht op de website[Aspose.Imaging voor .NET-documentatie](https://reference.aspose.com/imaging/net/).

## Veel Gestelde Vragen

### Wat is Aspose.Imaging voor .NET?
   Aspose.Imaging voor .NET is een krachtige bibliotheek voor beeldverwerking waarmee ontwikkelaars afbeeldingen in verschillende formaten binnen .NET-toepassingen kunnen maken, manipuleren en converteren.

### Kan ik Aspose.Imaging voor .NET gebruiken in commerciële projecten?
    Ja, u kunt Aspose.Imaging voor .NET gebruiken in zowel commerciële als niet-commerciële projecten. Licentiegegevens zijn te vinden op de[aankooppagina](https://purchase.aspose.com/buy).

### Is er een gratis proefversie beschikbaar?
    Ja, u kunt een gratis proefversie van Aspose.Imaging voor .NET krijgen[hier](https://releases.aspose.com/).

### Waar kan ik ondersteuning krijgen of vragen stellen?
    Als u vragen heeft of ondersteuning nodig heeft, kunt u terecht op de[Aspose.Imaging-forum](https://forum.aspose.com/).

### Hoe kan ik een tijdelijke licentie verkrijgen voor Aspose.Imaging voor .NET?
    U kunt een tijdelijke licentie verkrijgen via[hier](https://purchase.aspose.com/temporary-license/).


