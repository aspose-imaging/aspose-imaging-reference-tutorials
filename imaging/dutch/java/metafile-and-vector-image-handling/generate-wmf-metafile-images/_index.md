---
"description": "Leer hoe je WMF-metafile-afbeeldingen in Java maakt met Aspose.Imaging. Volg deze stapsgewijze handleiding voor krachtige mogelijkheden voor het genereren van afbeeldingen."
"linktitle": "Genereer WMF-metabestandafbeeldingen"
"second_title": "Aspose.Imaging Java-beeldverwerkings-API"
"title": "WMF-afbeeldingen maken met Aspose.Imaging voor Java"
"url": "/nl/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/"
"weight": 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# WMF-afbeeldingen maken met Aspose.Imaging voor Java

Wilt u WMF-afbeeldingen (Windows Metafile) maken met uw Java-applicaties? Aspose.Imaging voor Java is een krachtige tool waarmee u eenvoudig WMF-afbeeldingen kunt genereren. In deze stapsgewijze handleiding leiden we u door het proces van het gebruik van Aspose.Imaging voor Java om WMF-metafile-afbeeldingen te maken. 

## Vereisten

Voordat u begint, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

- Een Java-ontwikkelomgeving op uw computer.
- Aspose.Imaging voor Java-bibliotheek geïnstalleerd. U kunt deze downloaden van de [website](https://releases.aspose.com/imaging/java/).
- Basiskennis van Java-programmering.

## Pakketten importeren

Importeer eerst de benodigde pakketten voor uw Java-toepassing om Aspose.Imaging voor Java te gebruiken:

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

## Stap 1: Maak een canvas

Om te beginnen met het maken van je WMF-afbeelding, moet je een canvas maken waarop je vormen kunt tekenen. `WmfRecorderGraphics2D` De klasse biedt je dit canvas. Zo kun je er een exemplaar van maken:

```java
// Het pad naar de documentenmap.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

In de bovenstaande code specificeren we de canvasafmetingen (100x100) en de resolutie (96 DPI).

## Stap 2: Achtergrondkleur instellen

Bepaal vervolgens de achtergrondkleur voor je canvas. Je kunt de `setBackgroundColor` methode om de achtergrondkleur in te stellen:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

In dit voorbeeld stellen we de achtergrondkleur in op witte rook.

## Stap 3: Pen en penseel definiëren

Om vormen op het canvas te tekenen, moet je een pen en een penseel definiëren. De pen wordt gebruikt om contouren te tekenen en het penseel om vormen te vullen. Zo maak je een pen en een effen penseel:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

In deze code maken we een blauwe pen en een geelgroen effen penseel.

## Stap 4: Vormen vullen en tekenen

Laten we nu een paar basisvormen op het canvas tekenen. We beginnen met een veelhoek:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Hier vullen en tekenen we een veelhoek met de opgegeven pen en penseel. Je kunt de coördinaten en vormen naar wens aanpassen.

## Stap 5: Gebruik HatchBrush

Om texturen aan uw vormen toe te voegen, kunt u een `HatchBrush`. Bijvoorbeeld:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

In deze code maken we een kruisarceringspenseel met de kleuren wit en zilver.

## Stap 6: Ellips vullen en tekenen

Laten we een ellips op het canvas tekenen en vullen:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

U kunt de positie en de grootte van de ellips indien nodig aanpassen.

## Stap 7: Teken een boog en een kubieke Bézier

Het tekenen van complexere vormen is ook mogelijk. Zo teken je een boog en een kubieke Bézier-curve:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

In de bovenstaande code tekenen we eerst een boog met een stippellijn en vervolgens tekenen we een kubieke Bézier-curve met een effen rode pen.

## Stap 8: Afbeeldingen toevoegen

Je kunt ook afbeeldingen toevoegen aan je WMF-metabestand. Zo doe je dat:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

In deze stap laden we een afbeelding en plaatsen deze op het canvas op de opgegeven coördinaten (50, 50).

## Stap 9: Lijnen tekenen en cirkeldiagrammen maken

Om lijnen en cirkelvormen toe te voegen, kunt u deze voorbeelden volgen:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Hier tekenen we een lijn en vullen/tekenen we een taartvorm met de opgegeven pen en penseel.

## Stap 10: Polylijn en tekst tekenen

Het toevoegen van tekst en polylijnen is eenvoudig:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

U kunt het lettertype, de tekst en de polylijnpunten naar wens aanpassen.

## Stap 11: Sla de WMF-afbeelding op

Nadat u uw WMF-afbeelding hebt gemaakt, is het tijd om deze op te slaan:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Met deze code wordt de WMF-afbeelding opgeslagen in de opgegeven directory.

Dat is alles! Je hebt met succes een WMF-metabestandafbeelding gegenereerd met Aspose.Imaging voor Java.

## Conclusie

In deze tutorial hebben we onderzocht hoe je WMF-metafile-afbeeldingen kunt maken met Aspose.Imaging voor Java. We hebben de benodigde vereisten behandeld, pakketten geïmporteerd en stapsgewijze instructies gegeven voor het tekenen van verschillende vormen, het toevoegen van texturen, het invoegen van afbeeldingen en het opslaan van de uiteindelijke afbeelding. Aspose.Imaging voor Java biedt een krachtige set tools voor het bewerken en maken van afbeeldingen, waardoor het een waardevolle bron is voor je Java-applicaties.

## Veelgestelde vragen

### V1: Wat is een WMF-afbeeldingsformaat?

A1: WMF staat voor Windows Metafile, een vectorafbeeldingsformaat dat wordt gebruikt voor het opslaan van afbeeldingen, tekeningen en andere grafische gegevens. Het wordt veel gebruikt in Windows-applicaties en kan eenvoudig worden geschaald zonder kwaliteitsverlies.

### V2: Waar kan ik Aspose.Imaging voor Java downloaden?

A2: U kunt Aspose.Imaging voor Java downloaden van de [website](https://releases.aspose.com/imaging/java/).

### V3: Heb ik geavanceerde programmeervaardigheden nodig om Aspose.Imaging voor Java te gebruiken?

A3: Hoewel basiskennis van Java-programmering vereist is, biedt Aspose.Imaging voor Java een gebruiksvriendelijke API die taken voor het manipuleren en maken van afbeeldingen vereenvoudigt.

### V4: Kan ik Aspose.Imaging voor Java voor commerciële doeleinden gebruiken?

A4: Ja, Aspose.Imaging voor Java biedt commerciële licenties voor bedrijven en ontwikkelaars. U kunt een licentie aanschaffen bij [hier](https://purchase.aspose.com/buy).

### V5: Waar kan ik ondersteuning krijgen of vragen stellen over Aspose.Imaging voor Java?

A5: Je kunt ondersteuning vinden en contact leggen met de Aspose-community op de [Aspose.Imaging forums](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}