---
date: 2026-01-12
description: Leer hoe u het contrast in DICOM‑afbeeldingen kunt aanpassen – een stapsgewijze
  handleiding over het aanpassen van contrast met Aspose.Imaging voor Java en het
  converteren van DICOM naar BMP.
linktitle: DICOM Image Contrast Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: Hoe het contrast aanpassen in DICOM-afbeeldingen met Aspose.Imaging voor Java
url: /nl/java/image-processing-and-enhancement/dicom-image-contrast-adjustment/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Hoe het contrast aanpassen in DICOM-afbeeldingen met Aspose.Imaging voor Java

In moderne medische beeldvorming kan **hoe je het contrast aanpast** het verschil maken tussen een duidelijke diagnose en een gemist detail. Deze tutorial leidt je door de exacte stappen om het contrast in DICOM‑bestanden aan te passen met Aspose.Imaging voor Java, en laat zien hoe je die DICOM‑afbeeldingen naar BMP kunt converteren voor eenvoudig bekijken of verdere verwerking. Aan het einde heb je een kant‑klaar code‑fragment dat je in elk Java‑project kunt gebruiken.

## Snelle antwoorden
- **Wat doet contrastaanpassing?** Het vergroot het bereik tussen donkere en heldere pixels, waardoor structuren beter opvallen.
- **Welke bibliotheek is vereist?** Aspose.Imaging voor Java.
- **Kan ik exporteren naar BMP?** Ja – je kunt DICOM naar BMP converteren na het aanpassen van het contrast.
- **Heb ik een licentie nodig voor productie?** Een commerciële licentie is vereist voor niet‑evaluatiegebruik.
- **Welke Java‑versie wordt ondersteund?** Java 8 en nieuwer.

## Wat is contrastaanpassing en waarom is het belangrijk?
Contrastaanpassing verbetert het visuele onderscheid tussen anatomische kenmerken, waardoor radiologen afwijkingen sneller kunnen opmerken. In een DICOM‑workflow zorgt het aanpassen van het contrast vóór conversie ervoor dat de BMP‑output de diagnostische kwaliteit behoudt die nodig is voor rapportage of archivering.

## Voorwaarden

Voordat je in de code duikt, controleer dat je het volgende hebt:

1. **Aspose.Imaging voor Java** – download het van de officiële site [hier](https://releases.aspose.com/imaging/java/).  
2. **Java‑ontwikkelomgeving** – JDK 8+ en je favoriete IDE (IntelliJ, Eclipse, VS Code, enz.).  
3. **Een DICOM‑afbeelding** – elk .dcm‑bestand dat je wilt verbeteren; voorbeeldbestanden zijn online beschikbaar of je kunt je eigen klinische data gebruiken.

## Import pakketten

Deze imports geven je toegang tot de DICOM‑verwerking en BMP‑opslaafuncties.

```java
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
```

## Hoe het contrast aanpassen in DICOM‑afbeeldingen

Hieronder vind je de volledige, stap‑voor‑stap workflow. Elke stap wordt in eenvoudige taal uitgelegd zodat je kunt volgen, zelfs als je nieuw bent met Aspose.Imaging.

### Stap 1: Specificeer de bestands‑paden

Stel de locatie van de invoer‑DICOM en het gewenste uitvoer‑BMP‑pad in. Vervang de tijdelijke aanduiding door de daadwerkelijke map op je computer.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingContrast_out.bmp";
```

### Stap 2: Laad de DICOM‑afbeelding

We openen het DICOM‑bestand met een `FileInputStream`. Het `try‑with‑resources`‑blok zorgt ervoor dat de stream automatisch wordt gesloten.

```java
File file = new File(inputFile);

try (FileInputStream fis = new FileInputStream(file)) {
    try (DicomImage image = (DicomImage) Image.load(fis)) {
        // All further processing happens inside this block
    }
} catch (IOException ex) {
    Logger.println(ex.getMessage());
    ex.printStackTrace();
}
```

### Stap 3: Pas het contrast aan

In het binnenste `try`‑blok roep je `adjustContrast` aan. De waarde kan variëren van **‑100** (verlagen) tot **+100** (verhogen). In dit voorbeeld verhogen we het contrast met 50 eenheden.

```java
image.adjustContrast(50);
```

### Stap 4: Converteer DICOM naar BMP en sla de afbeelding op

Nadat we het contrast hebben aangepast, maken we een `BmpOptions`‑instantie aan en slaan we het resultaat op als een BMP‑bestand. Deze stap **converteert DICOM naar BMP**, waardoor je een breed ondersteund rasterformaat krijgt.

```java
image.save(outputFile, new BmpOptions());
```

## Veelvoorkomende problemen & tips

- **Ongeldig DICOM‑bestand** – Zorg ervoor dat het .dcm‑bestand niet gecomprimeerd is met een niet‑ondersteunde transfersyntax. Aspose.Imaging ondersteunt de meeste standaard DICOM‑coderingen.
- **Contrastwaarde buiten bereik** – Waarden buiten ±100 worden begrensd; kies een getal dat past bij het histogram van de afbeelding.
- **Geheugengebruik** – Grote DICOM‑series kunnen veel RAM verbruiken. Verwerk één slice per keer als je een `OutOfMemoryError` tegenkomt.

## Conclusie

Je hebt nu geleerd **hoe je contrast aanpast** in DICOM‑afbeeldingen met Aspose.Imaging voor Java en hoe je **DICOM naar BMP converteert** voor downstream‑taken. Deze workflow is snel, betrouwbaar en kan worden geïntegreerd in grotere medische‑beeld‑pijplijnen, of je nu een PACS‑viewer, een onderzoekstool of een geautomatiseerd rapportagesysteem bouwt.

Aspose.Imaging voor Java abstraheert de low‑level DICOM‑verwerking, zodat je je kunt concentreren op de klinische waarde van je afbeeldingen.

## Veelgestelde vragen

**Q: Wat is DICOM en waarom is het de standaard in medische beeldvorming?**  
A: DICOM (Digital Imaging and Communications in Medicine) is het universele formaat voor het opslaan, verzenden en delen van medische beelden, waardoor interoperabiliteit tussen apparaten en instellingen wordt gegarandeerd.

**Q: Kan ik helderheid aanpassen samen met contrast?**  
A: Ja, de methode `adjustBrightness(int value)` werkt op dezelfde manier en kan vóór het opslaan worden gekoppeld.

**Q: Ondersteunt Aspose.Imaging andere uitvoerformaten naast BMP?**  
A: Zeker – je kunt exporteren naar PNG, JPEG, TIFF en nog veel meer door de bijbehorende `*Options`‑klasse te gebruiken.

**Q: Is een commerciële licentie vereist voor productiegebruik?**  
A: Ja. Je kunt een licentie kopen [hier](https://purchase.aspose.com/buy) of een tijdelijke evaluatielicentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

**Q: Waar kan ik meer hulp en voorbeelden vinden?**  
A: Het Aspose.Imaging voor Java community‑forum biedt uitgebreide documentatie en voorbeeldcode: [Aspose.Imaging for Java forum](https://forum.aspose.com/).

**Laatst bijgewerkt:** 2026-01-12  
**Getest met:** Aspose.Imaging voor Java 24.11  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}