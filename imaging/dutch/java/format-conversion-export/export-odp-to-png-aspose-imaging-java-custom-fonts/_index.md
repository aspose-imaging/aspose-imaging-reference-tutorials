---
date: '2026-06-28'
description: Leer hoe u ODP naar PNG kunt converteren met Aspose.Imaging voor Java,
  custom fonts kunt instellen en system fonts kunt uitschakelen voor nauwkeurige weergave.
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: Hoe ODP naar PNG converteren met Aspose.Imaging voor Java – Custom Fonts &
  Export Guide
url: /nl/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Hoe ODP naar PNG converteren met Aspose.Imaging voor Java – Aangepaste lettertypen & Exportgids

In moderne Java‑applicaties is het converteren van OpenDocument Presentation (ODP)-bestanden naar PNG‑afbeeldingen van hoge kwaliteit een veelvoorkomende eis—vooral wanneer u de huisstijl moet behouden met aangepaste lettertypen. Deze tutorial laat **hoe ODP** naar PNG te converteren met Aspose.Imaging voor Java, begeleidt u bij het instellen van een aangepaste lettertype‑map, het uitschakelen van systeem‑fallback‑lettertypen, en het fijn afstemmen van rasterisatie‑opties voor optimale prestaties.

**Wat u zult leren**
- Hoe een aangepaste lettertype‑directory in te stellen voor ODP‑conversie.  
- Hoe systeem‑alternatieve lettertypen uit te schakelen zodat alleen uw gekozen lettertypen worden gebruikt.  
- Hoe een ODP‑bestand naar PNG te exporteren met precieze afmetingen en lettertype‑instellingen.  
- Tips voor het verbeteren van snelheid en geheugengebruik bij het verwerken van grote presentaties.

## Snelle antwoorden
- **Kan ik Maven gebruiken om Aspose.Imaging toe te voegen?** Ja, voeg de Maven‑dependency toe en voer `mvn install` uit.  
- **Heb ik een licentie nodig voor productie?** Een geldige Aspose.Imaging‑licentie is vereist voor onbeperkt gebruik.  
- **Worden mijn aangepaste lettertypen gerespecteerd?** Stel de lettertype‑map in en schakel systeem‑alternatieven uit om ze af te dwingen.  
- **Welke afbeeldingsformaten worden ondersteund?** Aspose.Imaging ondersteunt meer dan 120 raster‑ en vectorformaten, waaronder PNG, JPEG, TIFF en WebP.  
- **Is de API thread‑safe?** Ja, de meeste Aspose.Imaging‑klassen zijn veilig voor gelijktijdig gebruik wanneer u afzonderlijke instanties per thread maakt.

## Wat is “how to convert odp”?
*“How to convert odp”* verwijst naar het proces van het omzetten van een OpenDocument Presentation‑bestand naar een ander formaat—meestal PNG—terwijl de lay-out, lettertypen en visuele getrouwheid behouden blijven. Aspose.Imaging voor Java biedt een workflow met één methode die deze conversie afhandelt zonder externe tools, waardoor ontwikkelaars de conversie direct in hun applicaties kunnen integreren met minimale code.

## Waarom Aspose.Imaging voor Java gebruiken?
Aspose.Imaging ondersteunt **meer dan 120 outputformaten** en kan multi‑page ODP‑bestanden rasteren zonder het volledige document in het geheugen te laden, waardoor het piek‑RAM‑gebruik met tot 70 % wordt verminderd bij grote presentaties. De bibliotheek biedt ook ingebouwd lettertype‑beheer, waardoor de noodzaak voor third‑party render‑engines wegvalt.

## Voorvereisten
- **Bibliotheken**: Aspose.Imaging voor Java ≥ 25.5.  
- **JDK**: Versie 8 of hoger.  
- **IDE**: IntelliJ IDEA, Eclipse, of een willekeurige Java‑compatibele editor.  
- **Basiskennis**: Java I/O, object‑georiënteerd programmeren, en beeldconcepten.

## Installatie‑instructies

### Maven
Voeg de volgende dependency toe aan uw `pom.xml` en voer `mvn clean install` uit:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
Neem de bibliotheek op in uw `build.gradle`‑bestand en vernieuw het project:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Directe download
Download de nieuwste JAR van [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

## Stappen voor licentie‑acquisitie
Om de volledige functionaliteit te ontgrendelen, past u een tijdelijke of permanente licentie toe:

1. **Gratis proefversie** – Geen licentie vereist, beperkte functies.  
2. **Tijdelijke licentie** – Vraag er een aan op de [Aspose website](https://purchase.aspose.com/temporary-license/).  
3. **Aankoop** – Koop een abonnement of permanente licentie via de [Aspose purchase page](https://purchase.aspose.com/buy).

Initialiseer de bibliotheek met uw licentiebestand:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## Hoe een aangepaste lettertype‑directory instellen voor ODP‑conversie?
`FontSettings` is een klasse die lettertype‑bronnen beheert voor Aspose.Imaging. Laad uw aangepaste lettertypen voordat enige beeldverwerking begint. Dit zorgt ervoor dat elke dia de exacte lettertypen gebruikt die u levert.

Stel het pad van de lettertype‑map in met behulp van Aspose.Imaging’s `FontSettings`:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Definitie‑anker*: `FontSettings.setFontsFolder` vertelt Aspose.Imaging waar op het bestandssysteem naar TrueType‑ en OpenType‑lettertypen gezocht moet worden.

## Hoe systeem‑alternatieve lettertypen uitschakelen tijdens ODP‑conversie?
Het uitschakelen van systeem‑alternatieven dwingt de render‑engine om lettertypen die op het besturingssysteem geïnstalleerd zijn te negeren, waardoor gegarandeerd alleen de door u geleverde lettertypen worden gebruikt. Dit elimineert onverwachte lettertype‑vervangingen die het visuele uiterlijk van uw dia’s kunnen veranderen.

Schakel systeem‑alternatieven uit met de volgende aanroep:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Definitie‑anker*: `FontSettings.setGetSystemAlternativeFont(false)` dwingt de engine om alleen de lettertypen te gebruiken die zich in de door u gedefinieerde map bevinden, waardoor onverwachte vervangingen worden geëlimineerd.

## Hoe een ODP‑bestand exporteren naar PNG met een opgegeven lettertype?
`RasterizationOptions` definieert hoe vectorpagina’s worden gerasterd naar bitmap‑afbeeldingen. Door lettertype‑configuratie te combineren met rasterisatie‑instellingen, kunt u DPI, achtergrondkleur en paginagrootte voor elke geëxporteerde PNG regelen.

Implementeer de export‑methode zoals hieronder weergegeven:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*Definitie‑anker*: De `RasterizationOptions`‑klasse regelt DPI, paginagrootte en achtergrondkleur voor de gegenereerde PNG‑bestanden.

### Veelvoorkomende valkuilen & oplossingen
- **Ontbrekende lettertype‑bestanden** – Controleer of elk `.ttf`‑ of `.otf`‑bestand dat in de ODP wordt verwezen, aanwezig is in de map die u hebt ingesteld.  
- **Onjuiste bestands‑paden** – Gebruik absolute paden of los relatieve paden op ten opzichte van `System.getProperty("user.dir")`.  
- **Onvoldoende rechten** – Zorg ervoor dat het Java‑proces de lettertype‑map kan lezen en naar de uitvoermap kan schrijven.

## Praktische toepassingen
1. **Merk‑consistente dia‑sets** – Exporteer presentaties als PNG‑bestanden voor webpublicatie terwijl u de bedrijfslettertypen behoudt.  
2. **Geautomatiseerde rapportgeneratie** – Converteer elke dia naar een afbeelding voor opname in PDF‑rapporten of e‑mail‑nieuwsbrieven.  
3. **Legacy‑archiefcreatie** – Sla ODP‑inhoud op als PNG‑bestanden om toekomstige toegankelijkheid te garanderen zonder ODP‑viewers.

## Prestatie‑overwegingen
- Gebruik de nieuwste versie van Aspose.Imaging om te profiteren van multi‑threaded rasterisatie‑verbeteringen (tot 2× sneller op 8‑core CPU’s).  
- Omhul beeldverwerking in een try‑with‑resources‑blok om tijdige vrijgave van native resources te garanderen.  
- Pas `RasterizationOptions` aan (bijv. lagere DPI) bij het verwerken van duizenden dia’s om kwaliteit en geheugengebruik in balans te houden.

## Veelgestelde vragen

**Q: Wat is de minimale Java‑versie die vereist is?**  
A: Aspose.Imaging voor Java werkt met JDK 8 en hoger; JDK 11 wordt aanbevolen voor langdurige ondersteuning.

**Q: Kan ik alleen geselecteerde dia’s converteren?**  
A: Ja, stel `rasterizationOptions.setPageNumber(specificSlideIndex)` in vóór het aanroepen van `save`.

**Q: Hoe ga ik om met wachtwoord‑beveiligde ODP‑bestanden?**  
A: Laad het bestand met `LoadOptions` dat het wachtwoord bevat, en ga vervolgens verder met dezelfde lettertype‑instellingen.

**Q: Heeft het uitschakelen van systeem‑lettertypen invloed op de prestaties?**  
A: Het verbetert de snelheid marginalement omdat de engine de zoekopdracht naar systeem‑lettertypen overslaat, vooral merkbaar op machines met grote lettertype‑collecties.

**Q: Waar kan ik meer code‑voorbeelden vinden?**  
A: Bekijk de officiële [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/) voor extra scenario’s zoals batch‑conversie en beeldtransformaties.

## Aanvullende bronnen
- [Aspose.Imaging voor Java releases](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging releases](https://releases.aspose.com/imaging/java/)  
- [Start uw gratis proefversie](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging documentatie](https://reference.aspose.com/imaging/java/)  
- [Aspose.Imaging forum](https://forum.aspose.com/c/imaging/14)  
- [Aspose licenties kopen](https://purchase.aspose.com/buy)  
- [Vraag een tijdelijke licentie aan](https://purchase.aspose.com/temporary-license/)  

---

**Last Updated:** 2026-06-28  
**Tested With:** Aspose.Imaging for Java 25.5  
**Author:** Aspose

## Gerelateerde tutorials

- [ODG naar PNG converteren met Aspose.Imaging voor Java: Een volledige gids](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Efficiënte beeldconversie in Java met Aspose.Imaging: Een volledige gids](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}