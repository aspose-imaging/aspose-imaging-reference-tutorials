---
title: Hur man ritar en rasterbild på SVG i Aspose.Imaging för .NET
linktitle: Rita rasterbild på SVG i Aspose.Imaging för .NET
second_title: Aspose.Imaging .NET Image Processing API
description: Lär dig hur du ritar rasterbilder på SVG med Aspose.Imaging för .NET. Förbättra dina .NET-applikationer med dynamiska bilder.
type: docs
weight: 11
url: /sv/net/vector-image-processing/draw-raster-image-on-svg/
---

I en värld av .NET-programmering står Aspose.Imaging som ett pålitligt och mångsidigt bibliotek för att hantera olika bildrelaterade uppgifter. En fascinerande funktion som den erbjuder är möjligheten att rita en rasterbild på en SVG-duk. I den här steg-för-steg-guiden går vi igenom processen att rita en rasterbild på en SVG med Aspose.Imaging för .NET.

## Förutsättningar

Innan vi dyker in i detaljerna, se till att du har följande förutsättningar på plats:

-  Aspose.Imaging för .NET: Du måste ha biblioteket installerat. Om inte kan du ladda ner den från[Aspose.Imaging för .NET nedladdningssida](https://releases.aspose.com/imaging/net/).

-  Din dokumentkatalog: Ersätt`"Your Document Directory"` med den faktiska sökvägen till din arbetskatalog.

Låt oss nu dela upp processen i enkla steg:

## Steg 1: Importera nödvändiga namnområden

Du måste importera de nödvändiga namnrymden för att arbeta med Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Steg 2: Ladda bilderna

- Ladda först in rasterbilden som du vill rita på SVG-duken.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Ladda sedan SVG-canvasbilden där du vill rita rasterbilden.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Steg 3: Rita på SVG-bilden

 Nu kan du börja rita på den befintliga SVG-bilden. För att göra detta måste du skapa en instans av`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Steg 4: Rita rasterbilden

- Definiera gränserna där du vill rita rasterbilden och ange källregionen från rasterbilden.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Steg 5: Spara resultatet

Efter att ha ritat rasterbilden på SVG-duken kan du spara den resulterande bilden:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Slutsats

Grattis! Du har framgångsrikt ritat en rasterbild på en SVG-duk med Aspose.Imaging för .NET. Detta kan vara otroligt användbart för att skapa rika och dynamiska bilder i dina .NET-applikationer.

 För mer information och detaljerad dokumentation, besök[Aspose.Imaging för .NET-dokumentation](https://reference.aspose.com/imaging/net/).

## Vanliga frågor

### Vad är Aspose.Imaging för .NET?
   Aspose.Imaging for .NET är ett kraftfullt bildbehandlingsbibliotek som låter utvecklare skapa, manipulera och konvertera bilder i olika format inom .NET-applikationer.

### Kan jag använda Aspose.Imaging för .NET i kommersiella projekt?
    Ja, du kan använda Aspose.Imaging för .NET i både kommersiella och icke-kommersiella projekt. Licensinformation finns på[köpsidan](https://purchase.aspose.com/buy).

### Finns det en gratis provperiod?
    Ja, du kan få en gratis provversion av Aspose.Imaging för .NET från[här](https://releases.aspose.com/).

### Var kan jag få support eller ställa frågor?
    Om du har några frågor eller behöver support kan du besöka[Aspose.Imaging forum](https://forum.aspose.com/).

### Hur kan jag få en tillfällig licens för Aspose.Imaging för .NET?
    Du kan få en tillfällig licens från[här](https://purchase.aspose.com/temporary-license/).


