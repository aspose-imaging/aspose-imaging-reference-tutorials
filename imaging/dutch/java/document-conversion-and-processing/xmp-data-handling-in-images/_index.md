---
date: 2026-05-18
description: Leer hoe u de Java-afbeeldingsverwerkingsbibliotheek Aspose.Imaging kunt
  gebruiken om XMP-metadata in afbeeldingen in te sluiten en op te halen, met stapsgewijze
  code.
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: XMP-gegevensverwerking in afbeeldingen
schemas:
- author: Aspose
  dateModified: '2026-05-18'
  description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  headline: 'Java Image Processing Library: XMP with Aspose.Imaging'
  type: TechArticle
- description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  name: 'Java Image Processing Library: XMP with Aspose.Imaging'
  steps:
  - name: Specify Image Size and Tiff Options
    text: First, define the directory where your image will be stored and create a
      `Rectangle` to specify the size of the image. In this example, we use a TIFF
      image with certain options. `TiffOptions` configures format‑specific settings
      for the TIFF image.
  - name: Create a New Image
    text: Now, create a new image with the specified options. This image will be used
      to store the XMP metadata. `TiffImage` represents a TIFF image object, and `TiffFrame`
      defines an individual frame within it.
  - name: Create XMP Header and Trailer
    text: Create instances of XMP‑Header and XMP‑Trailer for your XMP metadata. These
      headers and trailers help define the metadata structure. `XmpHeaderPi` and `XmpTrailerPi`
      represent the XMP packet’s opening and closing sections.
  - name: Create XMP Meta Information
    text: Now, create an instance of XMP meta to set different attributes. You can
      add information like the author and description. `XmpMeta` holds the core metadata
      fields such as author and description.
  - name: Create XMP Packet Wrapper
    text: '`XmpPacketWrapper` is the container that holds the XMP header, trailer,
      and meta information in a single packet. It ensures the packet conforms to the
      XMP specification. `XmpPacketWrapper` packages the header, meta, and trailer
      into a single XMP packet.'
  - name: Add Photoshop Package
    text: To store Photoshop‑specific information, create a Photoshop package and
      set its attributes, such as city, country, and color mode. Then, add this package
      to the XMP metadata. `PhotoshopPackage` stores Photoshop‑specific metadata like
      city, country, and color mode.
  - name: Add Dublin Core Package
    text: For more general information, like author, title, and additional values,
      create a DublinCore package and set its attributes. Add this package to the
      XMP metadata as well. `DublinCorePackage` contains standard Dublin Core fields
      such as title, creator, and keywords.
  - name: Update XMP Metadata in the Image
    text: Update the XMP metadata into the image using the `setXmpData` method. This
      call writes the XMP packet into the image’s metadata section. `setXmpData` writes
      the XMP packet into the image’s metadata section.
  - name: Save the Image
    text: You can now save the image with the embedded XMP metadata on the disk or
      in a memory stream.
  - name: Load the Image and Retrieve XMP Metadata
    text: To retrieve the XMP metadata from the image, load the image from the memory
      stream or disk and access the XMP data via the `getXmpData` method. `getXmpData`
      reads the embedded XMP packet from the image. Congratulations! You've successfully
      learned how to handle XMP data in images using Aspose.Imagin
  type: HowTo
- questions:
  - answer: XMP is an XML‑based standard for embedding descriptive information directly
      inside files, enabling consistent metadata across applications.
    question: What is XMP metadata?
  - answer: It lets you tag images with author, copyright, keywords, and custom data,
      improving searchability and asset management without external databases.
    question: Why is XMP metadata important?
  - answer: Yes, Aspose.Imaging for Java provides methods to modify existing XMP packets
      and write them back to the file.
    question: Can I edit XMP metadata after embedding it in an image?
  - answer: A free trial is available for evaluation, but a paid license is required
      for production use. You can explore options on the [Aspose.Imaging for Java
      website](https://purchase.aspose.com/buy).
    question: Is Aspose.Imaging for Java a free tool?
  - answer: Visit the [Aspose.Imaging forums](https://forum.aspose.com/) for community
      assistance, or contact Aspose support directly for paid‑license customers.
    question: Where can I get help and support for Aspose.Imaging for Java?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: 'Java-afbeeldingsverwerkingsbibliotheek: XMP met Aspose.Imaging'
url: /nl/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# XMP-gegevensverwerking in afbeeldingen met Aspose.Imaging voor Java

Aspose.Imaging is een **java image processing library** die je laat werken met tientallen raster- en vectorformaten. In deze tutorial leer je hoe je XMP (Extensible Metadata Platform)-gegevens in afbeeldingen kunt insluiten en ophalen met Aspose.Imaging voor Java. Aan het einde kun je auteur, beschrijving en aangepaste metadata direct in je afbeeldingsbestanden opslaan, waardoor ze doorzoekbaar en zelfbeschrijvend zijn.

## Snelle antwoorden
- **Wat is XMP?** XMP is een gestandaardiseerd XML‑gebaseerd formaat voor het insluiten van metadata in bestanden zoals afbeeldingen, PDF's en video’s.  
- **Welke bibliotheek verwerkt XMP in Java?** Aspose.Imaging for Java biedt een volledige API voor het lezen en schrijven van XMP‑pakketten.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Hoeveel afbeeldingsformaten worden ondersteund?** Meer dan 150 formaten, waaronder TIFF, JPEG, PNG, PSD en RAW.  
- **Kan ik grote afbeeldingen verwerken?** Ja – de bibliotheek kan bestanden tot 2 GB aan zonder de volledige afbeelding in het geheugen te laden.

## Wat is XMP-metadata?
XMP-metadata is een XML‑gebaseerde standaard die beschrijvende informatie direct in digitale bestanden insluit. Het maakt consistente opslag van auteur, auteursrecht, trefwoorden en aangepaste gegevens mogelijk over verschillende toepassingen heen. Omdat het XML is, kan XMP worden uitgebreid met aangepaste namespaces, waardoor ontwikkelaars propriëtaire velden kunnen toevoegen terwijl ze compatibel blijven met tools die het kernschema begrijpen. Dit maakt XMP ideaal voor langdurig asset‑beheer en interoperabiliteit tussen toepassingen.

## Waarom een Java image processing library gebruiken voor XMP?
Aspose.Imaging voor Java ondersteunt **150+ image formats** en kan multi‑gigabyte bestanden verwerken in een streaming‑modus, waardoor het geheugenverbruik tot 80 % wordt verminderd vergeleken met naïef laden. De API garandeert ook dat XMP‑pakketten aan de normen voldoen, waardoor compatibiliteit met Adobe Photoshop, Lightroom en andere tools wordt verzekerd.

## Voorvereisten

Zorg ervoor dat je de volgende voorvereisten hebt voordat je begint:

- Een Java‑ontwikkelomgeving geïnstalleerd op je computer.  
- Aspose.Imaging voor Java bibliotheek geïnstalleerd. Je kunt deze downloaden van de [Aspose.Imaging for Java website](https://releases.aspose.com/imaging/java/).  
- Een basisbegrip van Java‑programmeren.

## Pakketten importeren

Begin met het importeren van de benodigde pakketten in je Java‑project. Je kunt de volgende import‑statements aan het begin van je code toevoegen:

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

Laten we nu het voorbeeld stap voor stap ontleden:

## Hoe XMP-metadata insluiten met een Java image processing library?

Laad je afbeelding, maak een XMP‑pakket, voeg het pakket toe aan de afbeelding en sla op – alles in een paar beknopte regels. De `setXmpData`‑methode van Aspose.Imaging schrijft het pakket direct in het bestand zonder een apart metadata‑bestand nodig te hebben. Het proces werkt zowel met bestands‑ als stream‑gebaseerde afbeeldingen, waardoor het geschikt is voor webservices en batch‑taken.

### Stap 1: Afbeeldingsgrootte en Tiff‑opties opgeven

Definieer eerst de map waarin je afbeelding wordt opgeslagen en maak een `Rectangle` om de grootte van de afbeelding op te geven. In dit voorbeeld gebruiken we een TIFF‑afbeelding met bepaalde opties. `TiffOptions` configureert formatspecifieke instellingen voor de TIFF‑afbeelding.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### Stap 2: Een nieuwe afbeelding maken

Maak nu een nieuwe afbeelding met de opgegeven opties. Deze afbeelding wordt gebruikt om de XMP‑metadata op te slaan. `TiffImage` vertegenwoordigt een TIFF‑afbeeldingsobject en `TiffFrame` definieert een individueel frame daarin.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### Stap 3: XMP‑header en -trailer maken

Maak instanties van XMP‑Header en XMP‑Trailer voor je XMP‑metadata. Deze headers en trailers helpen de metadata‑structuur te definiëren. `XmpHeaderPi` en `XmpTrailerPi` vertegenwoordigen respectievelijk de opening- en sluitingssecties van het XMP‑pakket.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### Stap 4: XMP‑meta‑informatie maken

Maak nu een instantie van XMP‑meta om verschillende attributen in te stellen. Je kunt informatie toevoegen zoals auteur en beschrijving. `XmpMeta` bevat de kernmetadata‑velden zoals auteur en beschrijving.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### Stap 5: XMP‑pakketwrapper maken

`XmpPacketWrapper` is de container die de XMP‑header, trailer en meta‑informatie in één pakket bevat. Het zorgt ervoor dat het pakket voldoet aan de XMP‑specificatie. `XmpPacketWrapper` verpakt de header, meta en trailer in één XMP‑pakket.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### Stap 6: Photoshop‑pakket toevoegen

Om Photoshop‑specifieke informatie op te slaan, maak je een Photoshop‑pakket en stel je de attributen in, zoals stad, land en kleermodus. Voeg vervolgens dit pakket toe aan de XMP‑metadata. `PhotoshopPackage` slaat Photoshop‑specifieke metadata op zoals stad, land en kleermodus.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### Stap 7: Dublin Core‑pakket toevoegen

Voor meer algemene informatie, zoals auteur, titel en extra waarden, maak je een DublinCore‑pakket en stel je de attributen in. Voeg dit pakket ook toe aan de XMP‑metadata. `DublinCorePackage` bevat standaard Dublin Core‑velden zoals titel, maker en trefwoorden.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### Stap 8: XMP‑metadata bijwerken in de afbeelding

Werk de XMP‑metadata bij in de afbeelding met de `setXmpData`‑methode. Deze oproep schrijft het XMP‑pakket naar de metadata‑sectie van de afbeelding. `setXmpData` schrijft het XMP‑pakket naar de metadata‑sectie van de afbeelding.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### Stap 9: De afbeelding opslaan

Je kunt nu de afbeelding met de ingesloten XMP‑metadata opslaan op de schijf of in een geheugen‑stream.

```java
    image.save(ms);
```

### Stap 10: De afbeelding laden en XMP‑metadata ophalen

Om de XMP‑metadata uit de afbeelding op te halen, laad je de afbeelding vanuit de geheugen‑stream of van de schijf en krijg je toegang tot de XMP‑gegevens via de `getXmpData`‑methode. `getXmpData` leest het ingesloten XMP‑pakket uit de afbeelding.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

Gefeliciteerd! Je hebt met succes geleerd hoe je XMP‑gegevens in afbeeldingen kunt verwerken met Aspose.Imaging voor Java. Hiermee kun je waardevolle metadata opslaan en ophalen binnen je afbeeldingsbestanden.

## Veelvoorkomende problemen en oplossingen

- **Metadata verschijnt niet in Photoshop:** Zorg ervoor dat het XMP‑pakket het juiste XML‑schema volgt; Aspose.Imaging valideert het automatisch, maar aangepaste namespaces moeten mogelijk worden geregistreerd.  
- **Grote TIFF‑bestanden veroorzaken OutOfMemoryError:** Gebruik `TiffOptions` met `Compression` ingesteld op `LZW` en schakel streaming in (`loadOptions.setBufferSize`) om het geheugenverbruik laag te houden.  
- **Onverwachte tekenencoding:** XMP verwacht UTF‑8; geef altijd strings door met `StandardCharsets.UTF_8` om vervormde gegevens te voorkomen.

## Veelgestelde vragen

**Q: Wat is XMP-metadata?**  
A: XMP is een XML‑gebaseerde standaard voor het insluiten van beschrijvende informatie direct in bestanden, waardoor consistente metadata over toepassingen heen mogelijk is.

**Q: Waarom is XMP-metadata belangrijk?**  
A: Het stelt je in staat afbeeldingen te taggen met auteur, auteursrecht, trefwoorden en aangepaste gegevens, waardoor de doorzoekbaarheid en asset‑beheer verbeteren zonder externe databases.

**Q: Kan ik XMP-metadata bewerken nadat ik het in een afbeelding heb ingesloten?**  
A: Ja, Aspose.Imaging voor Java biedt methoden om bestaande XMP‑pakketten te wijzigen en terug naar het bestand te schrijven.

**Q: Is Aspose.Imaging voor Java een gratis tool?**  
A: Een gratis proefversie is beschikbaar voor evaluatie, maar een betaalde licentie is vereist voor productiegebruik. Je kunt de opties verkennen op de [Aspose.Imaging for Java website](https://purchase.aspose.com/buy).

**Q: Waar kan ik hulp en ondersteuning krijgen voor Aspose.Imaging voor Java?**  
A: Bezoek de [Aspose.Imaging forums](https://forum.aspose.com/) voor community‑ondersteuning, of neem rechtstreeks contact op met de Aspose‑ondersteuning voor klanten met een betaalde licentie.

## Conclusie

In deze tutorial hebben we onderzocht hoe je met XMP‑metadata in afbeeldingen kunt werken met Aspose.Imaging voor Java, een toonaangevende **java image processing library**. Door de stap‑voor‑stap‑gids te volgen, kun je eenvoudig XMP‑gegevens insluiten, bijwerken en ophalen, waardoor je digitale assets worden verrijkt met doorzoekbare, aan de normen‑conforme metadata.

---

**Laatst bijgewerkt:** 2026-05-18  
**Getest met:** Aspose.Imaging for Java 24.12  
**Auteur:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Gerelateerde tutorials

- [Beheers Java Image Processing: EXIF-gegevens wijzigen met Aspose.Imaging](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [Java Image Processing met Aspose.Imaging: afbeeldingen laden, verbeteren en opslaan](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [Geavanceerde Java Image Processing met Aspose.Imaging Library](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Specify the size of image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// create the brand new image just for sample purposes
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// create an instance of XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// create an instance of Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// create an instance of XMP meta class to set different attributes
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// create an instance of XmpPacketWrapper that contains all metadata
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// create an instance of Photoshop package and set photoshop attributes
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// add photoshop package into XMP metadata
	xmpData.addPackage(photoshopPackage);
	// create an instance of DublinCore package and set dublinCore attributes
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// add dublinCore Package into XMP metadata
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// update XMP metadata into image
	image.setXmpData(xmpData);
	// Save image on the disk or in memory stream
	image.save(ms);
	// Load the image from memory stream or from disk to read/get the metadata
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Getting the XMP metadata
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Use package data ...
		}
	}
}
        
```