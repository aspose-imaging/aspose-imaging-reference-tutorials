---
"description": "Lär dig hur du ritar rasterbilder på SVG med Aspose.Imaging för .NET. Förbättra dina .NET-applikationer med dynamiska bilder."
"linktitle": "Rita rasterbild på SVG i Aspose.Imaging för .NET"
"second_title": "Aspose.Imaging .NET bildbehandlings-API"
"title": "Hur man ritar en rasterbild på SVG i Aspose.Imaging för .NET"
"url": "/sv/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Hur man ritar en rasterbild på SVG i Aspose.Imaging för .NET


I .NET-programmeringens värld står Aspose.Imaging som ett pålitligt och mångsidigt bibliotek för att hantera olika bildrelaterade uppgifter. En fascinerande funktion som det erbjuder är möjligheten att rita en rasterbild på en SVG-duk. I den här steg-för-steg-guiden guidar vi dig genom processen att rita en rasterbild på en SVG med Aspose.Imaging för .NET.

## Förkunskapskrav

Innan vi går in på detaljerna, se till att du har följande förutsättningar på plats:

- Aspose.Imaging för .NET: Du måste ha biblioteket installerat. Om inte kan du ladda ner det från [Nedladdningssida för Aspose.Imaging för .NET](https://releases.aspose.com/imaging/net/).

- Din dokumentkatalog: Ersätt `"Your Document Directory"` med den faktiska sökvägen till din arbetskatalog.

Nu ska vi dela upp processen i enkla steg:

## Steg 1: Importera nödvändiga namnrymder

Du måste importera de namnrymder som krävs för att fungera med Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Steg 2: Ladda bilderna

- Ladda först rasterbilden som du vill rita på SVG-arbetsytan.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Ladda sedan SVG-arbetsytans bild där du vill rita rasterbilden.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Steg 3: Rita på SVG-bilden

Nu kan du börja rita på den befintliga SVG-bilden. För att göra detta måste du skapa en instans av `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Steg 4: Rita rasterbilden

- Definiera gränserna för där du vill rita rasterbilden och ange källregionen från rasterbilden.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Steg 5: Spara resultatet

Efter att du har ritat rasterbilden på SVG-arbetsytan kan du spara den resulterande bilden:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Slutsats

Grattis! Du har lyckats rita en rasterbild på en SVG-duk med Aspose.Imaging för .NET. Detta kan vara otroligt användbart för att skapa rika och dynamiska bilder i dina .NET-applikationer.

För mer information och detaljerad dokumentation, besök [Aspose.Imaging för .NET-dokumentation](https://reference.aspose.com/imaging/net/).

## Vanliga frågor

### Vad är Aspose.Imaging för .NET?
   Aspose.Imaging för .NET är ett kraftfullt bildbehandlingsbibliotek som låter utvecklare skapa, manipulera och konvertera bilder i olika format inom .NET-applikationer.

### Kan jag använda Aspose.Imaging för .NET i kommersiella projekt?
   Ja, du kan använda Aspose.Imaging för .NET i både kommersiella och icke-kommersiella projekt. Licensinformation finns på [köpsida](https://purchase.aspose.com/buy).

### Finns det en gratis provperiod tillgänglig?
   Ja, du kan få en gratis provperiod av Aspose.Imaging för .NET från [här](https://releases.aspose.com/).

### Var kan jag få stöd eller ställa frågor?
   Om du har några frågor eller behöver stöd kan du besöka [Aspose.Imaging-forum](https://forum.aspose.com/).

### Hur kan jag få en tillfällig licens för Aspose.Imaging för .NET?
   Du kan få en tillfällig licens från [här](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}