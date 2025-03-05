---
title: XMP-gegevensverwerking in afbeeldingen met Aspose.Imaging voor Java
linktitle: XMP-gegevensverwerking in afbeeldingen
second_title: Aspose.Imaging Java-beeldverwerkings-API
description: Leer hoe u met XMP-metagegevens in afbeeldingen omgaat met Aspose.Imaging voor Java. Metagegevens insluiten en ophalen om uw afbeeldingsbestanden te verbeteren.
type: docs
weight: 16
url: /nl/java/document-conversion-and-processing/xmp-data-handling-in-images/
---
Aspose.Imaging for Java is een veelzijdige en krachtige bibliotheek voor het werken met afbeeldingen in verschillende formaten. Deze tutorial begeleidt u bij het verwerken van XMP-gegevens (Extensible Metadata Platform) in afbeeldingen met behulp van Aspose.Imaging voor Java. XMP is een standaard voor het insluiten van metagegevens in afbeeldingsbestanden, waardoor u waardevolle informatie zoals auteur, beschrijving en meer kunt opslaan.

## Vereisten

Voordat u begint, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

- Een Java-ontwikkelomgeving die op uw computer is geïnstalleerd.
-  Aspose.Imaging voor Java-bibliotheek geïnstalleerd. Je kunt het downloaden van de[Aspose.Imaging voor Java-website](https://releases.aspose.com/imaging/java/).
- Een basiskennis van Java-programmeren.

## Pakketten importeren

Begin met het importeren van de benodigde pakketten in uw Java-project. U kunt de volgende importinstructies aan het begin van uw code toevoegen:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.xmp.XmpPackage;
import com.aspose.imaging.xmp.XmpPacketWrapper;
import com.aspose.imaging.xmp.XmpMeta;
import com.aspose.imaging.xmp.photoshop.ColorMode;
import com.aspose.imaging.xmp.photoshop.PhotoshopPackage;
import com.aspose.imaging.xmp.dc.DublinCorePackage;
import com.aspose.imaging.xmp.header.XmpHeaderPi;
import com.aspose.imaging.xmp.trailer.XmpTrailerPi;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Laten we het voorbeeld nu opsplitsen in een stapsgewijze handleiding:

## Stap 1: Geef de afbeeldingsgrootte en TIFF-opties op

Definieer eerst de map waar uw afbeelding zal worden opgeslagen en maak een rechthoek om de grootte van de afbeelding aan te geven. In dit voorbeeld gebruiken we een Tiff-afbeelding met bepaalde opties.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## Stap 2: Maak een nieuwe afbeelding

Maak nu een nieuwe afbeelding met de opgegeven opties. Deze afbeelding wordt gebruikt om de XMP-metagegevens op te slaan.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## Stap 3: Maak een XMP-header en trailer

Creëer exemplaren van XMP-Header en XMP-Trailer voor uw XMP-metagegevens. Deze headers en trailers helpen bij het definiëren van de metadatastructuur.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Stap 4: Maak XMP-meta-informatie aan

Maak nu een exemplaar van XMP-meta om verschillende kenmerken in te stellen. U kunt informatie toevoegen, zoals de auteur en een beschrijving.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Stap 5: Maak een XMP-pakketverpakking

Maak een exemplaar van XmpPacketWrapper dat de XMP-header, trailer en meta-informatie bevat.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Stap 6: Voeg Photoshop-pakket toe

Als u Photoshop-specifieke informatie wilt opslaan, maakt u een Photoshop-pakket en stelt u de bijbehorende kenmerken in, zoals stad, land en kleurmodus. Voeg dit pakket vervolgens toe aan de XMP-metagegevens.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## Stap 7: Voeg het Dublin Core-pakket toe

Voor meer algemene informatie, zoals auteur, titel en aanvullende waarden, maakt u een DublinCore-pakket en stelt u de kenmerken ervan in. Voeg dit pakket ook toe aan de XMP-metagegevens.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## Stap 8: Update XMP-metagegevens in de afbeelding

 Werk de XMP-metagegevens bij naar de afbeelding met behulp van de`setXmpData` methode.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## Stap 9: Sla de afbeelding op

U kunt de afbeelding nu met de ingebouwde XMP-metagegevens op de schijf of in een geheugenstream opslaan.

```java
    image.save(ms);
```

## Stap 10: Laad de afbeelding en haal XMP-metagegevens op

Om de XMP-metagegevens uit de afbeelding op te halen, laadt u de afbeelding uit de geheugenstroom of schijf en krijgt u toegang tot de XMP-gegevens.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Pakketgegevens gebruiken...
        }
    }
}
```

Gefeliciteerd! U hebt met succes geleerd hoe u XMP-gegevens in afbeeldingen kunt verwerken met behulp van Aspose.Imaging voor Java. Hierdoor kunt u waardevolle metadata in uw afbeeldingsbestanden opslaan en ophalen.

## Conclusie

In deze zelfstudie hebben we onderzocht hoe u met XMP-metagegevens in afbeeldingen kunt werken met behulp van Aspose.Imaging voor Java. Door de stapsgewijze handleiding te volgen, kunt u eenvoudig metagegevens in uw afbeeldingsbestanden insluiten en ophalen, waardoor de informatie en bruikbaarheid ervan worden verbeterd.

## Veelgestelde vragen

### Vraag 1: Wat zijn XMP-metagegevens?

A1: XMP (Extensible Metadata Platform) is een standaard voor het insluiten van metadata in verschillende soorten bestanden, inclusief afbeeldingen. Hiermee kunt u informatie zoals auteur, titel, beschrijving en meer in het bestand zelf opslaan.

### Vraag 2: Waarom zijn XMP-metadata belangrijk?

A2: XMP-metadata zijn essentieel voor het organiseren en categoriseren van digitale assets. Het helpt bij het toekennen van eigendom, het beschrijven van inhoud en het toevoegen van context aan bestanden zoals afbeeldingen, waardoor ze toegankelijker en betekenisvoller worden.

### V3: Kan ik XMP-metagegevens bewerken nadat ik deze in een afbeelding heb ingesloten?

A3: Ja, u kunt XMP-metagegevens bewerken nadat u deze in een afbeelding hebt ingesloten. Aspose.Imaging voor Java biedt tools voor het indien nodig wijzigen en bijwerken van metadata-attributen.

### V4: Is Aspose.Imaging voor Java een gratis tool?

 A4: Aspose.Imaging voor Java biedt een gratis proefversie, maar voor volledige functionaliteit en uitgebreid gebruik is een betaalde licentie vereist. Op de website kunt u de mogelijkheden verkennen[Aspose.Imaging voor Java-website](https://purchase.aspose.com/buy).

### V5: Waar kan ik hulp en ondersteuning krijgen voor Aspose.Imaging voor Java?

 A5: Als u problemen ondervindt of vragen heeft met betrekking tot Aspose.Imaging voor Java, kunt u terecht op de[Aspose.Imaging-forums](https://forum.aspose.com/) voor gemeenschapsondersteuning en begeleiding.



## Volledige broncode
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Geef de grootte van de afbeelding op door een rechthoek te definiëren
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// maak de gloednieuwe afbeelding alleen voor voorbeelddoeleinden
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// maak een exemplaar van XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// maak een exemplaar van Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// maak een exemplaar van de XMP-metaklasse om verschillende attributen in te stellen
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	//maak een exemplaar van XmpPacketWrapper dat alle metagegevens bevat
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// maak een exemplaar van het Photoshop-pakket en stel Photoshop-kenmerken in
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// voeg een Photoshop-pakket toe aan XMP-metagegevens
	xmpData.addPackage(photoshopPackage);
	// maak een exemplaar van het DublinCore-pakket en stel dublinCore-kenmerken in
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// voeg dublinCore-pakket toe aan XMP-metadata
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// update XMP-metagegevens naar afbeelding
	image.setXmpData(xmpData);
	// Sla de afbeelding op de schijf of in de geheugenstroom op
	image.save(ms);
	// Laad de afbeelding vanuit de geheugenstream of vanaf schijf om de metagegevens te lezen/op te halen
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// De XMP-metagegevens ophalen
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Pakketgegevens gebruiken...
		}
	}
}
        
```