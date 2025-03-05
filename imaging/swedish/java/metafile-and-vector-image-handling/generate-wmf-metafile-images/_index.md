---
title: Skapa WMF-bilder med Aspose.Imaging för Java
linktitle: Generera WMF-metafilbilder
second_title: Aspose.Imaging Java Image Processing API
description: Lär dig hur du skapar WMF-metafilbilder i Java med Aspose.Imaging. Följ denna steg-för-steg-guide för kraftfulla bildgenereringsmöjligheter.
type: docs
weight: 10
url: /sv/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/
---
Vill du skapa WMF-bilder (Windows Metafile) med dina Java-applikationer? Aspose.Imaging för Java är ett kraftfullt verktyg som låter dig skapa WMF-bilder med lätthet. I den här steg-för-steg-guiden går vi igenom processen att använda Aspose.Imaging för Java för att skapa WMF-metafilbilder. 

## Förutsättningar

Innan du börjar, se till att du har följande förutsättningar på plats:

- En Java-utvecklingsmiljö konfigurerad på din dator.
-  Aspose.Imaging för Java-biblioteket installerat. Du kan ladda ner den från[hemsida](https://releases.aspose.com/imaging/java/).
- Grundläggande kunskaper i Java-programmering.

## Importera paket

Importera först de nödvändiga paketen för din Java-applikation för att använda Aspose.Imaging för Java:

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

## Steg 1: Skapa en Canvas

 För att börja skapa din WMF-bild måste du skapa en duk där du kan rita former. De`WmfRecorderGraphics2D` klass förser dig med denna duk. Så här skapar du en instans av det:

```java
// Sökvägen till dokumentkatalogen.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

I koden ovan anger vi canvasmåtten (100x100) och upplösningen (96 DPI).

## Steg 2: Ställ in bakgrundsfärg

 Därefter definierar du bakgrundsfärgen för din duk. Du kan använda`setBackgroundColor` metod för att ställa in bakgrundsfärgen:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

I det här exemplet ställer vi in bakgrundsfärgen till vit rök.

## Steg 3: Definiera penna och pensel

För att rita former på duken måste du definiera en penna och en pensel. Pennan används för att rita konturer, och penseln används för att fylla former. Så här skapar du en penna och en solid pensel:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

I den här koden skapar vi en blå penna och en gulgrön fast pensel.

## Steg 4: Fyll och rita former

Låt oss nu fylla och rita några grundläggande former på duken. Vi börjar med en polygon:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Här fyller och ritar vi en polygon med den angivna pennan och penseln. Du kan justera koordinaterna och formerna efter behov.

## Steg 5: Använd HatchBrush

 För att lägga till texturer till dina former kan du använda en`HatchBrush`. Till exempel:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

I den här koden skapar vi en crosshatch-pensel med vita och silverfärger.

## Steg 6: Fyll och rita ellips

Låt oss fylla och rita en ellips på duken:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

Du kan justera ellipsens position och storlek efter behov.

## Steg 7: Rita båge och Cubic Bezier

Att rita mer komplexa former är också möjligt. Så här ritar du en båge och en kubisk Bezier-kurva:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

I koden ovan ritar vi först en båge med en prickad linjestil, och sedan ritar vi en kubisk Bezier-kurva med en solid röd penna.

## Steg 8: Lägg till bilder

Du kan också lägga till bilder till din WMF-metafil. Så här gör du:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

I det här steget laddar vi en bild och placerar den på duken med de angivna koordinaterna (50, 50).

## Steg 9: Rita linjer och paj

För att lägga till linjer och pajformer kan du följa dessa exempel:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Här ritar vi en linje och fyller/ritar en pajform med den angivna pennan och penseln.

## Steg 10: Rita polylinje och text

Att lägga till text och polylinjer är enkelt:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

Du kan anpassa teckensnitt, text och polylinjepunkter efter behov.

## Steg 11: Spara WMF-bilden

När du har skapat din WMF-bild är det dags att spara den:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Denna kod kommer att spara WMF-bilden i den angivna katalogen.

Det är allt! Du har framgångsrikt skapat en WMF-metafilbild med Aspose.Imaging för Java.

## Slutsats

den här handledningen har vi utforskat hur man skapar WMF-metafilbilder med Aspose.Imaging för Java. Vi täckte de nödvändiga förutsättningarna, importerade paket och gav steg-för-steg-instruktioner för att rita olika former, lägga till texturer, infoga bilder och spara den slutliga bilden. Aspose.Imaging för Java erbjuder en kraftfull uppsättning verktyg för bildmanipulering och skapande, vilket gör det till en värdefull resurs för dina Java-applikationer.

## FAQ's

### F1: Vad är ett WMF-bildformat?

S1: WMF står för Windows Metafile, vilket är ett vektorgrafikformat som används för att lagra bilder, ritningar och annan grafisk data. Det används ofta i Windows-applikationer och kan enkelt skalas utan kvalitetsförlust.

### F2: Var kan jag ladda ner Aspose.Imaging för Java?

 S2: Du kan ladda ner Aspose.Imaging för Java från[hemsida](https://releases.aspose.com/imaging/java/).

### F3: Behöver jag avancerade programmeringskunskaper för att använda Aspose.Imaging för Java?

S3: Även om grundläggande Java-programmeringskunskaper krävs, tillhandahåller Aspose.Imaging för Java ett användarvänligt API som förenklar bildmanipulering och skapande uppgifter.

### F4: Kan jag använda Aspose.Imaging för Java för kommersiella ändamål?

 S4: Ja, Aspose.Imaging för Java erbjuder kommersiella licenser för företag och utvecklare. Du kan köpa en licens från[här](https://purchase.aspose.com/buy).

### F5: Var kan jag få support eller ställa frågor om Aspose.Imaging för Java?

 S5: Du kan hitta stöd och engagera dig i Aspose-gemenskapen på[Aspose.Imaging forum](https://forum.aspose.com/).