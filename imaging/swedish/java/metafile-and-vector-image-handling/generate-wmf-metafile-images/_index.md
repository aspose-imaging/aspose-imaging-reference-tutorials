---
"description": "Lär dig hur du skapar WMF-metafilbilder i Java med Aspose.Imaging. Följ den här steg-för-steg-guiden för kraftfulla bildgenereringsfunktioner."
"linktitle": "Generera WMF-metafilbilder"
"second_title": "Aspose.Imaging Java-bildbehandlings-API"
"title": "Skapa WMF-bilder med Aspose.Imaging för Java"
"url": "/sv/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/"
"weight": 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Skapa WMF-bilder med Aspose.Imaging för Java

Vill du skapa WMF-bilder (Windows Metafile) med dina Java-program? Aspose.Imaging för Java är ett kraftfullt verktyg som låter dig enkelt generera WMF-bilder. I den här steg-för-steg-guiden guidar vi dig genom processen att använda Aspose.Imaging för Java för att skapa WMF-metafilbilder. 

## Förkunskapskrav

Innan du börjar, se till att du har följande förutsättningar på plats:

- En Java-utvecklingsmiljö konfigurerad på din dator.
- Aspose.Imaging för Java-biblioteket är installerat. Du kan ladda ner det från [webbplats](https://releases.aspose.com/imaging/java/).
- Grundläggande kunskaper i Java-programmering.

## Importera paket

Importera först de paket som behövs för att din Java-applikation ska kunna använda Aspose.Imaging för Java:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.color.*;
import com.aspose.imaging.coreexceptions.ImageLoadException;
import com.aspose.imaging.imageoptions.WmfOptions;
import com.aspose.imaging.internal.system.drawing.*;
import com.aspose.imaging.internal.system.drawing.imaging.*;
import com.aspose.imaging.pen.*;
import com.aspose.imaging.system.drawing.*;
```

## Steg 1: Skapa en arbetsyta

För att börja skapa din WMF-bild måste du skapa en arbetsyta där du kan rita former. `WmfRecorderGraphics2D` klassen ger dig den här arbetsytan. Så här skapar du en instans av den:

```java
// Sökvägen till dokumentkatalogen.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

I koden ovan anger vi arbetsytans dimensioner (100x100) och upplösningen (96 DPI).

## Steg 2: Ställ in bakgrundsfärg

Definiera sedan bakgrundsfärgen för din arbetsyta. Du kan använda `setBackgroundColor` metod för att ställa in bakgrundsfärgen:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

I det här exemplet ställer vi in bakgrundsfärgen till vit rök.

## Steg 3: Definiera penna och pensel

För att rita former på arbetsytan måste du definiera en penna och en pensel. Pennan används för att rita konturer och penseln används för att fylla former. Så här skapar du en penna och en heldragen pensel:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

I den här koden skapar vi en blå penna och en gulgrön heldragen pensel.

## Steg 4: Fyll och rita former

Nu ska vi fylla och rita några grundläggande former på arbetsytan. Vi börjar med en polygon:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Här fyller och ritar vi en polygon med den angivna pennan och penseln. Du kan justera koordinaterna och formerna efter behov.

## Steg 5: Använd HatchBrush

För att lägga till texturer till dina former kan du använda en `HatchBrush`Till exempel:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

I den här koden skapar vi en korsstreckpensel med vita och silverfärger.

## Steg 6: Fyll och rita ellipsen

Låt oss fylla och rita en ellips på duken:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

Du kan justera ellipsens position och storlek efter behov.

## Steg 7: Rita båge och kubisk bezier

Det är också möjligt att rita mer komplexa former. Så här ritar du en båge och en kubisk Bezier-kurva:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

I koden ovan ritar vi först en båge med en prickad linjestil, och sedan ritar vi en kubisk Bezier-kurva med en heldragen röd penna.

## Steg 8: Lägg till bilder

Du kan också lägga till bilder i din WMF-metafil. Så här gör du:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

det här steget laddar vi en bild och placerar den på arbetsytan vid de angivna koordinaterna (50, 50).

## Steg 9: Rita linjer och cirkeldiagram

För att lägga till linjer och cirkelformer kan du följa dessa exempel:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Här ritar vi en linje och fyller/rita en pajform med den angivna pennan och penseln.

## Steg 10: Rita polylinje och text

Det är enkelt att lägga till text och polylinjer:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

Du kan anpassa teckensnitt, text och polylinjepunkter efter behov.

## Steg 11: Spara WMF-avbildningen

När du har skapat din WMF-avbildning är det dags att spara den:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Den här koden sparar WMF-avbildningen i den angivna katalogen.

Det var allt! Du har lyckats generera en WMF-metafilbild med Aspose.Imaging för Java.

## Slutsats

den här handledningen har vi utforskat hur man skapar WMF-metafilbilder med Aspose.Imaging för Java. Vi har gått igenom de nödvändiga förutsättningarna, importerat paket och tillhandahållit steg-för-steg-instruktioner för att rita olika former, lägga till texturer, infoga bilder och spara den slutliga bilden. Aspose.Imaging för Java erbjuder en kraftfull uppsättning verktyg för bildmanipulation och skapande, vilket gör det till en värdefull resurs för dina Java-applikationer.

## Vanliga frågor

### F1: Vad är ett WMF-bildformat?

A1: WMF står för Windows Metafile, vilket är ett vektorgrafikformat som används för att lagra bilder, teckningar och annan grafisk data. Det används ofta i Windows-program och kan enkelt skalas utan kvalitetsförlust.

### F2: Var kan jag ladda ner Aspose.Imaging för Java?

A2: Du kan ladda ner Aspose.Imaging för Java från [webbplats](https://releases.aspose.com/imaging/java/).

### F3: Behöver jag avancerade programmeringskunskaper för att använda Aspose.Imaging för Java?

A3: Grundläggande kunskaper i Java-programmering krävs, men Aspose.Imaging för Java erbjuder ett användarvänligt API som förenklar bildmanipulation och skapande.

### F4: Kan jag använda Aspose.Imaging för Java för kommersiella ändamål?

A4: Ja, Aspose.Imaging för Java erbjuder kommersiella licenser för företag och utvecklare. Du kan köpa en licens från [här](https://purchase.aspose.com/buy).

### F5: Var kan jag få support eller ställa frågor om Aspose.Imaging för Java?

A5: Du kan hitta stöd och interagera med Aspose-communityn på [Aspose.Imaging-forum](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}