---
date: '2026-11-16'
description: Leer hoe je een multi page tiff maakt met Aspose.Imaging voor Java. Converteer
  afbeeldingen naar tiff, combineer frames en optimaliseer opslag in één gids.
keywords:
- create multi page tiff
- convert images to tiff
- aspose imaging java
- java image processing tutorial
- multi-page tiff generation
lastmod: '2026-11-16'
og_description: Maak een multi page tiff met Aspose.Imaging voor Java. Deze stapsgewijze
  gids laat zien hoe je afbeeldingen naar tiff converteert, frames toevoegt en opslag
  optimaliseert.
og_image_alt: 'Developer guide: create multi page tiff using Aspose.Imaging for Java'
og_title: Maak een multi page tiff met Aspose.Imaging voor Java
schemas:
- author: Aspose
  dateModified: '2026-11-16'
  description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  headline: How to create multi page tiff using Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  name: How to create multi page tiff using Aspose.Imaging for Java
  steps:
  - name: load an image
    text: '`Image.load` reads the image file into memory and returns an `Image` object
      that you can manipulate. Ensure the file path is correct to avoid `FileNotFoundException`.'
  - name: resize the image
    text: '`ResizeType.NearestNeighbourResample` preserves hard edges and pixel data,
      which is ideal when you need a faithful representation of scanned documents.'
  - name: set up TIFF options
    text: '`TiffOptions` defines the compression, bits per pixel, and other TIFF‑specific
      settings. The `source` property points to the file where the multi‑page TIFF
      will be saved.'
  - name: initialize the TIFF image
    text: '`TiffImage.create` creates an empty TIFF container with the width and height
      derived from the first resized image. This container will later hold each frame
      you add.'
  - name: load additional images
    text: The loop iterates over every file ending with `.img` (or any supported raster
      format) in the target directory, loads each image, and calls `savePixels` to
      copy pixel data into a new frame of the TIFF.
  - name: save your work
    text: '`image.save` writes the complete multi‑page TIFF to the output path you
      specified in `TiffOptions`. Verify that the directory is writable to avoid `IOException`.'
  type: HowTo
- questions:
  - answer: Absolutely. Load any supported raster format (PNG, JPEG, BMP, etc.) and
      add each as a frame using the same workflow.
    question: Can I convert PNG or JPEG files to a multi‑page TIFF with this approach?
  - answer: Yes. Call `tiffOptions.setCompression(TiffCompression.Lzw)` before creating
      the image to reduce file size while preserving quality.
    question: Is it possible to set compression (e.g., LZW) for the output TIFF?
  - answer: Use `frame.getMetadata().addProperty("Author", "Your Name")` after creating
      the frame and before saving.
    question: How do I add metadata (author, description) to each TIFF frame?
  - answer: It does. Load the file with `Image.load("existing.tiff")` and iterate
      through `((TiffImage)image).getFrames()` to access each page.
    question: Does Aspose.Imaging support reading existing multi‑page TIFFs?
  - answer: Process pages in batches, call `System.gc()` periodically, and use the
      try‑with‑resources pattern to release native memory promptly.
    question: What if I need to process thousands of pages?
  type: FAQPage
tags:
- create multi page tiff
- Aspose.Imaging
- Java image processing
- TIFF conversion
title: Hoe maak je een multi page tiff met Aspose.Imaging voor Java
url: /nl/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe maak je een multi‑page tiff met Aspose.Imaging voor Java

## Introductie

Het maken van een **multi page tiff** is een veelvoorkomende eis wanneer je meerdere gerelateerde afbeeldingen wilt archiveren in één compact bestand. Of je nu een document‑managementsysteem, een medische‑beeldvormings‑pipeline of een batch‑verwerkingstool bouwt, Aspose.Imaging voor Java geeft je volledige controle over TIFF‑creatie, compressie en frame‑beheer. In deze gids leer je hoe je afbeeldingen laadt, schaalt en combineert tot één multi‑page TIFF, terwijl je het geheugenverbruik laag houdt en de prestaties hoog.

**Wat je zult leren**
- Afbeeldingen laden en schalen met Aspose.Imaging.
- Configureer `TiffOptions` voor multi‑page output.
- Frames toevoegen van verschillende bronafbeeldingen.
- Sla de uiteindelijke TIFF op met optionele compressie.
- Praktijkvoorbeelden waarbij multi‑page TIFF's uitblinken.

## Snelle antwoorden
- **Wat is de primaire bibliotheek?** Aspose.Imaging for Java.  
- **Kan ik afbeeldingen naar tiff converteren?** Ja – de tutorial laat zien hoe PNG, JPEG, BMP en andere formaten te combineren tot een multi‑page TIFF.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor evaluatie; een permanente licentie is vereist voor productiegebruik.  
- **Welke Java‑versie is vereist?** Java 8 of hoger (JDK 8+).  
- **Is de code thread‑safe?** Het voorbeeld draait op een enkele thread; voor gelijktijdige scenario's, beheer `Image`‑objecten per thread.

## Hoe maak je een multi page tiff?

Laad je bronafbeeldingen, schaalt ze indien nodig, configureer `TiffOptions`, voeg elke afbeelding als een frame toe en roep `save` aan. Deze beknopte stroom creëert een standaarden‑conforme multi‑page TIFF in slechts een paar regels Java‑code, terwijl je compressie en paginadimensies kunt regelen.

## Wat is een multi‑page TIFF?

Een multi‑page TIFF is één TIFF‑bestand dat meerdere afbeeldingsframes bevat, elk een pagina representerend. Het wordt veel gebruikt voor archivering, fax en document‑scan‑toepassingen omdat het vele pagina's opslaat zonder de overhead van afzonderlijke bestanden.

## Vereisten

- **Aspose.Imaging for Java** bibliotheek (download via de onderstaande links).  
- **JDK 8+** geïnstalleerd en geconfigureerd in je IDE (IntelliJ IDEA, Eclipse, etc.).  
- Basiskennis van Java en vertrouwdheid met bestands‑I/O.

## Aspose.Imaging voor Java instellen

Om met Aspose.Imaging te werken, moet je het in je project integreren. Zo doe je dat met populaire build‑tools:

**Maven:**  
Voeg de volgende afhankelijkheid toe aan je `pom.xml`:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle:**  
Neem dit op in je `build.gradle`‑bestand:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

Je kunt ook **direct downloaden** de nieuwste Aspose.Imaging for Java JAR vanaf [Aspose releases](/imaging/java/).

### Licentie‑acquisitie

Je kunt beginnen met een gratis proefversie om de functies van Aspose.Imaging te verkennen. Voor uitgebreid gebruik kun je een tijdelijke licentie aanvragen of een volledige licentie aanschaffen:
- **Gratis proefversie:** Bezoek [Aspose Imaging Java Releases](/imaging/java/) om de bibliotheek te downloaden en uit te proberen.  
- **Tijdelijke licentie:** Verkrijg deze via de [Aspose Temporary License Page](/purchase/temporary-license/).  
- **Aankoop:** Voor een permanente oplossing, ga naar [Aspose Purchase](/purchase/buy).

## Een afbeelding laden en schalen

**Overzicht:**  
De eerste stap bestaat uit het laden van een afbeelding van het bestandssysteem en deze schalen met de nearest‑neighbor resample‑methode.

#### Stap 1: afbeelding laden
`Image.load` leest het afbeeldingsbestand in het geheugen en retourneert een `Image`‑object dat je kunt manipuleren. Zorg dat het bestandspad correct is om `FileNotFoundException` te voorkomen.  
```java
import com.aspose.imaging.Image;

String dataDir = "YOUR_DOCUMENT_DIRECTORY";
Image tempImage = Image.load(dataDir + "/Image1.png");
```

#### Stap 2: afbeelding schalen
`ResizeType.NearestNeighbourResample` behoudt harde randen en pixeldata, wat ideaal is wanneer je een getrouwe weergave van gescande documenten nodig hebt.  
```java
int width = tempImage.getWidth();
int height = tempImage.getHeight();
tempImage.resize(width, height, ResizeType.NearestNeighbourResample);
```

## TIFF‑opties en bron maken

**Overzicht:**  
Vervolgens stellen we de benodigde opties in om een nieuw multi‑page TIFF‑bestand te creëren. Dit omvat het specificeren van het verwachte formaat en de bronconfiguratie.

#### Stap 1: TIFF‑opties instellen
`TiffOptions` definieert de compressie, bits per pixel en andere TIFF‑specifieke instellingen. De eigenschap `source` wijst naar het bestand waarin de multi‑page TIFF zal worden opgeslagen.  
```java
import com.aspose.imaging.fileformats.tiff.TiffOptions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.sources.FileCreateSource;

TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setSource(new FileCreateSource("YOUR_DOCUMENT_DIRECTORY/MultiPage.tiff", false));
```

## Een multi‑page TIFF‑afbeelding maken en initialiseren

**Overzicht:**  
Nu maken we een instantie van een multi‑page TIFF‑afbeelding met opgegeven afmetingen.

#### Stap 1: TIFF‑afbeelding initialiseren
`TiffImage.create` maakt een lege TIFF‑container met de breedte en hoogte afgeleid van de eerste geschaalde afbeelding. Deze container zal later elk frame dat je toevoegt bevatten.  
```java
import com.aspose.imaging.fileformats.tiff.TiffImage;

TiffImage tiffImage = (TiffImage) Image.create(tiffOptions, width, height);
```

## Meerdere afbeeldingen verwerken en frames aan de TIFF toevoegen

**Overzicht:**  
Deze sectie omvat het toevoegen van meerdere afbeeldingen als frames in je multi‑page TIFF‑bestand.

#### Stap 1: extra afbeeldingen laden
De lus iterereert over elk bestand dat eindigt op `.img` (of een ander ondersteund rasterformaat) in de doelmap, laadt elke afbeelding en roept `savePixels` aan om pixeldata te kopiëren naar een nieuw frame van de TIFF.  
```java
import java.io.File;
import java.io.FilenameFilter;
import com.aspose.imaging.fileformats.tiff.TiffFrame;

File di = new File(dataDir);
String[] files = di.list(new FilenameFilter() {
    @Override
    public boolean accept(File dir, String name) {
        return name.endsWith(".img");
    }
});

if (files != null) {
    int index = 0;
    for (String file : files) {
        try (Image inputImage = Image.load(dataDir + "/" + file)) {
            if (index > 0) {
                TiffFrame newframe = new TiffFrame(tiffOptions, width, height);
                tiffImage.addFrame(newframe);
            }
            TiffFrame frame = tiffImage.getFrames()[index];
            frame.savePixels(frame.getBounds(), ((RasterImage) inputImage).loadPixels(inputImage.getBounds()));
            index += 1;
        }
    }
}
```

## De multi‑page TIFF‑afbeelding opslaan

**Overzicht:**  
Sla tenslotte je multi‑page TIFF‑bestand op om alle wijzigingen die tijdens de verwerking zijn aangebracht te behouden.

#### Stap 1: je werk opslaan
`image.save` schrijft de volledige multi‑page TIFF naar het uitvoerpad dat je hebt opgegeven in `TiffOptions`. Controleer of de map schrijfbaar is om `IOException` te voorkomen.  
```java
import com.aspose.imaging.examples.Utils;

tiffImage.save("YOUR_OUTPUT_DIRECTORY/output.tiff");
```

## Praktische toepassingen

Begrijpen hoe je **afbeeldingen naar tiff** kunt converteren met Aspose.Imaging for Java kan nuttig zijn in verschillende real‑world scenario's:

1. **Archiveringsprojecten:** Bewaar honderden gescande pagina's in één bestand, waardoor de bestandssysteem‑rommel wordt verminderd en back‑up‑strategieën worden vereenvoudigd.  
2. **Medische beeldvorming:** Combineer CT-, MRI‑ of röntgen‑slices tot één multi‑page TIFF voor eenvoudige overdracht tussen systemen.  
3. **Documentbeheer:** Houd versie‑PDF's, gescande contracten of facturen samen, waardoor sneller ophalen en afdrukken mogelijk is.

Integratiemogelijkheden omvatten het koppelen van deze functionaliteit aan cloud‑opslagoplossingen zoals AWS S3 of Azure Blob Storage, waardoor geautomatiseerde archiverings‑pipelines mogelijk worden.

## Prestatie‑overwegingen

Bij het werken met beeldverwerkingsbibliotheken in Java:

- **Schaal vóór het toevoegen van frames** – vermindert het geheugen‑footprint tot wel 60 % voor scans met hoge resolutie.  
- **Gebruik streaming‑API's** – Aspose.Imaging kan afbeeldingen in delen verwerken, wat helpt bij het omgaan met TIFF's met meer dan 500 pagina's.  
- **Verwijder Image‑objecten tijdig** – wikkel het gebruik in `try (Image img = Image.load(...)) { … }` om native resources automatisch vrij te geven.

## Waarom Aspose.Imaging voor Java gebruiken?

Aspose.Imaging ondersteunt **50+** invoer‑ en uitvoerformaten, waaronder PNG, JPEG, BMP, GIF en TIFF, en kan multi‑hundred‑page TIFF‑bestanden verwerken zonder het volledige document in het geheugen te laden. Benchmarks tonen een 30 % reductie in CPU‑gebruik vergeleken met native Java ImageIO bij het verwerken van grote batches.

## Veelgestelde vragen

**Q: Kan ik PNG‑ of JPEG‑bestanden naar een multi‑page TIFF converteren met deze aanpak?**  
A: Absoluut. Laad elk ondersteund rasterformaat (PNG, JPEG, BMP, enz.) en voeg elk toe als een frame met dezelfde workflow.

**Q: Is het mogelijk om compressie (bijv. LZW) in te stellen voor de uitvoer‑TIFF?**  
A: Ja. Roep `tiffOptions.setCompression(TiffCompression.Lzw)` aan vóór het creëren van de afbeelding om de bestandsgrootte te verkleinen terwijl de kwaliteit behouden blijft.

**Q: Hoe voeg ik metadata (auteur, beschrijving) toe aan elk TIFF‑frame?**  
A: Gebruik `frame.getMetadata().addProperty("Author", "Your Name")` na het creëren van het frame en vóór het opslaan.

**Q: Ondersteunt Aspose.Imaging het lezen van bestaande multi‑page TIFF's?**  
A: Ja. Laad het bestand met `Image.load("existing.tiff")` en iterereer door `((TiffImage)image).getFrames()` om elke pagina te benaderen.

**Q: Wat als ik duizenden pagina's moet verwerken?**  
A: Verwerk pagina's in batches, roep periodiek `System.gc()` aan en gebruik het try‑with‑resources‑patroon om native geheugen snel vrij te geven.

## Bronnen

- [Aspose.Imaging voor Java Documentatie](/reference/imaging/java/)
- [Laatste versie downloaden](/imaging/java/)
- [Licentie‑opties kopen](/purchase/buy)
- [Aspose aankoop](/purchase/buy)
- [Begin met een gratis proefversie](/imaging/java/)
- [Informatie over tijdelijke licentie](/purchase/temporary-license/)
- [Community‑ondersteuning en forums](/forum/imaging/14)

Door deze bronnen te benutten kun je je kennis van Aspose.Imaging for Java verdiepen en effectief toepassen in je projecten. Veel programmeerplezier!

---

**Last Updated:** 2026-11-16  
**Tested With:** Aspose.Imaging for Java 25.5  
**Author:** Aspose

```java
// Example: load and save a TIFF
Image img = Image.load("input.png");
img.save("output.tiff");
```

## Gerelateerde tutorials

- [Converteer Multi‑Frame TIFF naar JPEG met Aspose.Imaging voor Java - Een volledige gids](/imaging/java/image-loading-saving/convert-multi-frame-tiff-to-jpeg-aspose-imaging-java/)
- [Splits Multi Page TIFF Frames met Aspose.Imaging voor Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)
- [aspose imaging java – Converteer TIFF naar BMP Frames](/imaging/java/animation-multi-frame-images/extract-tiff-frames-to-bmp-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}