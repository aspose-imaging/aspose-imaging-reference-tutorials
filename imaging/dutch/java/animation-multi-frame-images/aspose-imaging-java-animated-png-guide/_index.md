---
date: '2026-11-04'
description: Leer hoe u een geanimeerde PNG in Java maakt met een Aspose Imaging-licentie,
  voeg de Maven-afhankelijkheid toe, converteer TIFF naar APNG en sla de afbeelding
  op.
keywords:
- aspose imaging license
- convert tiff to apng
- tiff to png conversion
- add maven dependency java
- control animation speed java
lastmod: '2026-11-04'
og_description: Leer hoe u een geanimeerde PNG in Java maakt met een Aspose Imaging-licentie,
  voeg de Maven-afhankelijkheid toe, converteer TIFF naar APNG en beheer de animatiesnelheid.
og_image_alt: Guide showing how to generate animated PNGs in Java with Aspose Imaging
og_title: Maak een geanimeerde PNG in Java met een Aspose Imaging-licentie
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to create animated PNG in Java with an Aspose Imaging license,
    add the Maven dependency, convert TIFF to APNG and save the image.
  headline: Create animated PNG in Java using an Aspose Imaging license
  type: TechArticle
- description: Learn how to create animated PNG in Java with an Aspose Imaging license,
    add the Maven dependency, convert TIFF to APNG and save the image.
  name: Create animated PNG in Java using an Aspose Imaging license
  steps:
  - name: '**Web development** – Animated banners, icons, or loading spinners that
      work across browsers without needing GIF support.'
    text: '**Web development** – Animated banners, icons, or loading spinners that
      work across browsers without needing GIF support.'
  - name: '**Desktop applications** – Enrich Swing or JavaFX UI components with subtle
      motion cues.'
    text: '**Desktop applications** – Enrich Swing or JavaFX UI components with subtle
      motion cues.'
  - name: '**Data visualization** – Animate chart transitions or step‑by‑step walkthroughs
      for reports.'
    text: '**Data visualization** – Animate chart transitions or step‑by‑step walkthroughs
      for reports.'
  type: HowTo
- questions:
  - answer: You must set the value yourself with `setDefaultFrameTime(int ms)`; there
      is no hidden default.
    question: What is the default frame duration for APNG using Aspose.Imaging?
  - answer: Yes—load the file, modify the frame timings via `ApngOptions`, and save
      it again.
    question: Can I adjust animation speed in an existing APNG file?
  - answer: Ensure the image path is correct, allocate enough heap memory for large
      files, and use `try‑with‑resources` to release resources promptly.
    question: What are common pitfalls when loading images with Aspose.Imaging?
  - answer: Visit [Aspose's download page](https://releases.aspose.com/imaging/java/)
      to request a trial.
    question: How do I obtain a free trial license for Aspose.Imaging?
  - answer: Absolutely—you can combine it with Spring, Apache Commons, or any UI framework
      such as JavaFX.
    question: Is Aspose.Imaging compatible with other Java libraries?
  type: FAQPage
tags:
- aspose imaging
- animated png java
- tiff conversion
- maven dependency
- java image processing
title: Maak een geanimeerde PNG in Java met een Aspose Imaging-licentie
url: /nl/java/animation-multi-frame-images/aspose-imaging-java-animated-png-guide/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak een animated PNG in Java met een Aspose Imaging-licentie

## Introductie

Als je **animated PNG in Java** moet maken en een betrouwbare, productie‑klare oplossing wilt, geeft een **Aspose Imaging-licentie** je volledige toegang tot de high‑performance API van de bibliotheek. Of je nu een webportaal, een desktop‑UI of een data‑visualisatie‑dashboard bouwt, animated PNG's (APNG) voegen vloeiende beweging toe zonder de nadelen van GIF's. Deze tutorial leidt je door het toevoegen van de Maven‑dependency, het converteren van een multi‑page TIFF naar APNG, en het regelen van de frame‑timing, zodat je snel gepolijste animaties kunt leveren.

## Snelle antwoorden
- **Welke bibliotheek maakt APNG‑creatie in Java mogelijk?** Aspose.Imaging met de Aspose Imaging Maven‑dependency.  
- **Welk formaat kan worden geconverteerd naar APNG?** Multi‑page TIFF‑bestanden kunnen worden geconverteerd naar animated PNG's.  
- **Hoe regel ik de animatiesnelheid?** Stel `ApngOptions.setDefaultFrameTime(milliseconds)` in.  
- **Heb ik een licentie nodig voor productie?** Ja—een Aspose Imaging‑licentie verwijdert evaluatielimieten en ontgrendelt alle functies.  
- **Kan ik Maven of Gradle gebruiken?** Beide worden ondersteund; voeg gewoon de juiste dependency toe.

## Wat is een Aspose Imaging-licentie?

Een **Aspose Imaging-licentie** is een bestand dat de volledige, onbeperkte functionaliteit van de Aspose.Imaging voor Java‑bibliotheek ontgrendelt, waardoor evaluatiewatermerken en gebruikslimieten verdwijnen. Je laadt de licentie één keer bij het starten van de applicatie, en alle daaropvolgende API‑aanroepen verlopen zonder proefbeperkingen.

## Waarom Aspose.Imaging gebruiken voor APNG?

Aspose.Imaging verwerkt **150+ beeldformaten** (inclusief JPEG, PNG, TIFF, BMP en WebP) en kan documenten met honderden pagina's aan, terwijl het geheugenverbruik onder de 200 MB blijft op een typische 8 GB JVM. De native APNG‑encoder van de bibliotheek behoudt transparantie, volledige kleurdiepte en per‑frame timing zonder externe tools, waardoor het de snelste en meest betrouwbare optie is voor Java‑ontwikkelaars.

## Vereisten
- Java 8 of hoger geïnstalleerd.  
- Een IDE zoals IntelliJ IDEA of Eclipse.  
- Maven of Gradle voor dependency‑beheer (of het JAR‑bestand).  

## Maven‑dependency Aspose Imaging toevoegen

### Maven

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

Voor wie de voorkeur geeft aan directe downloads, kun je de nieuwste versie ophalen van [Aspose's download page](https://releases.aspose.com/imaging/java/). Je kunt ook [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) bezoeken voor release‑notities.

## Licentie‑acquisitie

Om de volledige functionaliteit te ontgrendelen zonder evaluatielimieten:

- **Gratis proefversie:** Begin met een gratis proefversie om de functionaliteit te testen.  
- **Tijdelijke licentie:** Verkrijg een tijdelijke licentie voor uitgebreide toegang tijdens ontwikkeling.  
- **Aankoop:** Voor langdurig gebruik, koop een commerciële licentie.

Initialiseer de licentie in je code:

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path/to/your/license/file.lic");
```

`License` laadt het Aspose.Imaging‑licentiebestand om alle functies te ontgrendelen.

## Hoe TIFF naar APNG converteren met Aspose.Imaging?

Laad de bron‑TIFF, configureer de APNG‑opties en sla het resultaat op. De bibliotheek extraheert elke TIFF‑pagina als een afzonderlijk frame en schrijft een standards‑conforme animated PNG. Dit proces stelt je ook in staat om de standaard frame‑timing in te stellen, compressieniveau te kiezen en eventueel frames te verkleinen vóór het opslaan, waardoor je volledige controle hebt over de uiteindelijke animatie‑kwaliteit en bestandsgrootte.

### Een afbeelding laden

`Image` is de basisklasse die een afbeeldingobject vertegenwoordigt in Aspose.Imaging.

```java
import com.aspose.imaging.Image;
```

```java
String inputFilePath = "YOUR_DOCUMENT_DIRECTORY/img4.tif";

try (Image image = Image.load(inputFilePath)) {
    // The image is now loaded and ready for manipulation.
}
```

### Standaard frame‑duur instellen voor APNG

`ApngOptions` configureert instellingen voor het opslaan van een afbeelding als een animated PNG.

```java
import com.aspose.imaging.imageoptions.ApngOptions;
```

```java
ApngOptions op = new ApngOptions();
op.setDefaultFrameTime(500); // Default frame time set to 500 milliseconds
```

### De afbeelding opslaan als APNG

Bereid het uitvoerpad voor en roep `save` aan met de geconfigureerde opties:

```java
String outputFilePath = "YOUR_OUTPUT_DIRECTORY/img4.tif.500ms.png";
```

```java
try (Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/img4.tif")) {
    ApngOptions op = new ApngOptions();
    op.setDefaultFrameTime(500); // Frame time set to 500 ms
    
    image.save(outputFilePath, op);
}
```

De regel `image.save(outputFilePath, op);` **slaat de afbeelding op als APNG**. Zorg ervoor dat het uitvoerbestand eindigt op `.png` en dat `ApngOptions` de gewenste frame‑timing weergeeft.

## Hoe afbeelding opslaan als APNG in Java?

Roep `image.save` aan met een `ApngOptions`‑instantie die de standaard frame‑tijd specificeert. Pas `setDefaultFrameTime` aan om de animatie te versnellen of te vertragen, en je kunt dezelfde aanroep hergebruiken voor andere bronformaten zoals multi‑page PDF's. Het gebruik van een try‑with‑resources‑blok zorgt ervoor dat de afbeeldingsresources direct worden vrijgegeven, waardoor geheugenlekken tijdens batchverwerking worden voorkomen.

## Praktische toepassingen
1. **Webontwikkeling** – Animated banners, iconen of laadspinners die in alle browsers werken zonder GIF‑ondersteuning.  
2. **Desktop‑applicaties** – Verrijk Swing‑ of JavaFX‑UI‑componenten met subtiele bewegingsaanwijzingen.  
3. **Data‑visualisatie** – Animeer grafiek‑overgangen of stap‑voor‑stap walkthroughs voor rapporten.

Combineer Aspose.Imaging met bibliotheken zoals Swing, JavaFX of Spring Boot om een naadloze gebruikerservaring te bieden.

## Prestatie‑overwegingen
- **Verklein verstandig:** Grotere resoluties verhogen het geheugenverbruik; verklein waar mogelijk.  
- **Vrijgeven tijdig:** Gebruik `try‑with‑resources` (zoals getoond) om native resources vrij te maken.  
- **Batchverwerking:** Hergebruik een enkele `License`‑instantie en vermijd herhaaldelijk laden van hetzelfde bronbestand bij het genereren van veel APNG's.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **OutOfMemoryError** bij het laden van grote TIFF's | Afbeelding is te groot voor de JVM-heap | Verhoog `-Xmx` of verklein vóór verwerking |
| **Lege frames** in de output‑APNG | Bron‑TIFF‑pagina's hebben verschillende afmetingen | Verklein alle pagina's naar een gemeenschappelijke grootte vóór het opslaan |
| **Licentie niet toegepast** | Pad naar licentiebestand onjuist | Controleer het pad en zorg dat het bestand leesbaar is tijdens runtime |

## Veelgestelde vragen

**V: Wat is de standaard frame‑duur voor APNG met Aspose.Imaging?**  
A: Je moet de waarde zelf instellen met `setDefaultFrameTime(int ms)`; er is geen verborgen standaardwaarde.

**V: Kan ik de animatiesnelheid aanpassen in een bestaand APNG‑bestand?**  
A: Ja—laad het bestand, wijzig de frame‑timings via `ApngOptions`, en sla het opnieuw op.

**V: Wat zijn veelvoorkomende valkuilen bij het laden van afbeeldingen met Aspose.Imaging?**  
A: Zorg dat het afbeeldingspad correct is, wijs voldoende heap‑geheugen toe voor grote bestanden, en gebruik `try‑with‑resources` om resources tijdig vrij te geven.

**V: Hoe verkrijg ik een gratis proeflicentie voor Aspose.Imaging?**  
A: Bezoek [Aspose's download page](https://releases.aspose.com/imaging/java/) om een proefversie aan te vragen.

**V: Is Aspose.Imaging compatibel met andere Java‑bibliotheken?**  
A: Absoluut—je kunt het combineren met Spring, Apache Commons of elk UI‑framework zoals JavaFX.

## Bronnen

- **Documentatie:** [Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)  
- **Download:** [Latest Release Download](https://releases.aspose.com/imaging/java/)  
- **Aankoop:** [Buy Aspose.Imaging](https://purchase.aspose.com/buy)  
- **Gratis proefversie:** [Get Started with Free Trial](https://releases.aspose.com/imaging/java/)  
- **Tijdelijke licentie:** [Acquire Temporary License](https://purchase.aspose.com/temporary-license/)  
- **Supportforum:** [Aspose Community Support](https://forum.aspose.com/c/imaging/14)

---

**Laatst bijgewerkt:** 2026-11-04  
**Getest met:** Aspose.Imaging 25.5 for Java  
**Auteur:** Aspose

## Gerelateerde tutorials

- [How to create animated gif with Aspose.Imaging Java: Frame and Loop Control](/imaging/java/animation-multi-frame-images/gif-manipulation-java-aspose-imaging-guide/)
- [How to Create Multi-Page TIFF with Aspose.Imaging for Java – A Complete Guide](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [process multi frame tiff in Java using Aspose.Imaging](/imaging/java/animation-multi-frame-images/java-aspose-imaging-multi-frame-tiff-processing/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}