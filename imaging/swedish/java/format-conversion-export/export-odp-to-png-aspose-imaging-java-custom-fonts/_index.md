---
date: '2026-06-28'
description: Lär dig hur du konverterar ODP till PNG med Aspose.Imaging för Java,
  ställer in anpassade teckensnitt och inaktiverar systemteckensnitt för korrekt rendering.
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
title: Hur man konverterar ODP till PNG med Aspose.Imaging för Java – Anpassade teckensnitt
  & exportguide
url: /sv/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Hur man konverterar ODP till PNG med Aspose.Imaging för Java – Anpassade typsnitt & Exportguide

I moderna Java‑applikationer är konvertering av OpenDocument Presentation (ODP)‑filer till högkvalitativa PNG‑bilder ett vanligt krav—särskilt när du behöver bevara varumärket genom anpassade typsnitt. Denna handledning visar **hur man konverterar ODP** till PNG med Aspose.Imaging för Java, guidar dig genom att ange en anpassad typsnittsmapp, inaktivera system‑fallback‑typsnitt och finjustera rasteriseringsalternativ för optimal prestanda.

**Vad du kommer att lära dig**
- Hur man anger en anpassad typsnittskatalog för ODP‑konvertering.  
- Hur man inaktiverar systemets alternativa typsnitt så att endast dina valda teckensnitt används.  
- Hur man exporterar en ODP‑fil till PNG med exakta dimensioner och typsnittsinställningar.  
- Tips för att förbättra hastighet och minnesanvändning vid bearbetning av stora presentationer.

## Snabba svar
- **Kan jag använda Maven för att lägga till Aspose.Imaging?** Ja, lägg till Maven‑beroendet och kör `mvn install`.  
- **Behöver jag en licens för produktion?** En giltig Aspose.Imaging‑licens krävs för obegränsad användning.  
- **Kommer mina anpassade typsnitt att respekteras?** Ange typsnittsmappen och inaktivera systemalternativ för att verkställa dem.  
- **Vilka bildformat stöds?** Aspose.Imaging stöder över 120 raster‑ och vektorformat, inklusive PNG, JPEG, TIFF och WebP.  
- **Är API‑et trådsäkert?** Ja, de flesta Aspose.Imaging‑klasser är säkra för samtidig användning när du skapar separata instanser per tråd.

## Vad är “how to convert odp”?
*“How to convert odp”* avser processen att omvandla en OpenDocument Presentation‑fil till ett annat format—vanligtvis PNG—medan layout, typsnitt och visuell trohet bevaras. Aspose.Imaging för Java erbjuder ett en‑metod‑arbetsflöde som hanterar denna konvertering utan att kräva externa verktyg, vilket låter utvecklare integrera konverteringen direkt i sina applikationer med minimal kod.

## Varför använda Aspose.Imaging för Java?
Aspose.Imaging stöder **120+ utdataformat** och kan rasterisera flersidiga ODP‑filer utan att ladda hela dokumentet i minnet, vilket minskar maximal RAM‑användning med upp till 70 % för stora presentationer. Biblioteket erbjuder också inbyggd typsnittshantering, vilket eliminerar behovet av tredjepartsrenderingsmotorer.

## Förutsättningar
- **Bibliotek**: Aspose.Imaging för Java ≥ 25.5.  
- **JDK**: Version 8 eller nyare.  
- **IDE**: IntelliJ IDEA, Eclipse eller någon Java‑kompatibel editor.  
- **Grundläggande kunskap**: Java I/O, objekt‑orienterad programmering och bildkoncept.

## Installationsinstruktioner

### Maven
Lägg till följande beroende i din `pom.xml` och kör `mvn clean install`:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
Inkludera biblioteket i din `build.gradle`‑fil och uppdatera projektet:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Direktnedladdning
Download the latest JAR from [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

## Steg för att skaffa licens
För att låsa upp full funktionalitet, ansök om en tillfällig eller permanent licens:

1. **Gratis prov** – Ingen licens krävs, begränsade funktioner.  
2. **Tillfällig licens** – Begär en på [Aspose webbplats](https://purchase.aspose.com/temporary-license/).  
3. **Köp** – Köp ett abonnemang eller en evig licens från [Aspose köpsida](https://purchase.aspose.com/buy).

Initiera biblioteket med din licensfil:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## Hur man anger en anpassad typsnittskatalog för ODP‑konvertering?
`FontSettings` är en klass som hanterar typsnittresurser för Aspose.Imaging. Ladda dina anpassade typsnitt innan någon bildbehandling påbörjas. Detta säkerställer att varje bildspel använder exakt de teckensnitt du tillhandahåller.

Ange sökvägen till typsnittsmappen med Aspose.Imaging’s `FontSettings`:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Definition ankare*: `FontSettings.setFontsFolder` talar om för Aspose.Imaging var den ska leta efter TrueType‑ och OpenType‑typsnitt i filsystemet.

## Hur man inaktiverar systemets alternativa typsnitt under ODP‑konvertering?
Inaktivering av systemalternativ tvingar renderingsmotorn att ignorera typsnitt som är installerade på operativsystemet, vilket garanterar att endast de typsnitt du tillhandahåller används. Detta eliminerar oväntade typsnittssubstitutioner som kan förändra bildspelets visuella utseende.

Inaktivera systemalternativ med följande anrop:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Definition ankare*: `FontSettings.setGetSystemAlternativeFont(false)` tvingar motorn att endast använda typsnitten som finns i den mapp du definierat, vilket eliminerar oväntade substitutioner.

## Hur man exporterar en ODP‑fil till PNG med ett specificerat typsnitt?
`RasterizationOptions` definierar hur vektorsidor rasteriseras till bitmap‑bilder. Genom att kombinera typsnittskonfiguration med rasteriseringsinställningar kan du kontrollera DPI, bakgrundsfärg och sidstorlek för varje exporterad PNG.

Implementera exportmetoden som visas nedan:

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

*Definition ankare*: `RasterizationOptions`‑klassen styr DPI, sidstorlek och bakgrundsfärg för de genererade PNG‑filerna.

### Vanliga fallgropar & lösningar
- **Saknade typsnittsfiler** – Verifiera att varje `.ttf` eller `.otf` som refereras i ODP‑filen finns i den mapp du angivit.  
- **Felaktiga filsökvägar** – Använd absoluta sökvägar eller lös relativa sökvägar mot `System.getProperty("user.dir")`.  
- **Otillräckliga behörigheter** – Säkerställ att Java‑processen kan läsa typsnittsmappen och skriva till utmatningsmappen.

## Praktiska tillämpningar
1. **Varumärkeskonsekventa bildspel** – Exportera presentationer som PNG för webbpublicering samtidigt som företags­typsnitt bevaras.  
2. **Automatiserad rapportgenerering** – Konvertera varje bild till en bild för inkludering i PDF‑rapporter eller e‑postnyhetsbrev.  
3. **Skapande av äldre arkiv** – Spara ODP‑innehåll som PNG för att garantera framtida åtkomst utan att behöva ODP‑visare.

## Prestandaöverväganden
- Använd den senaste versionen av Aspose.Imaging för att dra nytta av förbättringar i flerkärnig rasterisering (upp till 2× snabbare på 8‑kärniga CPU:er).  
- Omslut bildbehandling i ett try‑with‑resources‑block för att garantera tidsenlig frigöring av inhemska resurser.  
- Justera `RasterizationOptions` (t.ex. lägre DPI) när du bearbetar tusentals bildspel för att balansera kvalitet och minnesanvändning.

## Vanliga frågor

**Q: Vad är den minsta Java‑versionen som krävs?**  
A: Aspose.Imaging för Java fungerar med JDK 8 och nyare; JDK 11 rekommenderas för långsiktig support.

**Q: Kan jag konvertera endast utvalda bildspel?**  
A: Ja, ange `rasterizationOptions.setPageNumber(specificSlideIndex)` innan du anropar `save`.

**Q: Hur hanterar jag lösenordsskyddade ODP‑filer?**  
A: Läs in filen med `LoadOptions` som inkluderar lösenordet, fortsätt sedan med samma typsnittinställningar.

**Q: Påverkar inaktivering av systemtypsnitt prestandan?**  
A: Det förbättrar hastigheten marginellt eftersom motorn hoppar över uppslagning av systemtypsnitt, särskilt märkbart på maskiner med stora typsnittssamlingar.

**Q: Var kan jag hitta fler kodexempel?**  
A: Utforska den officiella [Aspose.Imaging‑dokumentationen](https://reference.aspose.com/imaging/java/) för ytterligare scenarier såsom batch‑konvertering och bildtransformationer.

## Ytterligare resurser
- [Aspose.Imaging för Java‑utgåvor](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging‑utgåvor](https://releases.aspose.com/imaging/java/)  
- [Starta din gratis provperiod](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging‑dokumentation](https://reference.aspose.com/imaging/java/)  
- [Aspose.Imaging‑forum](https://forum.aspose.com/c/imaging/14)  
- [Köp Aspose‑licens](https://purchase.aspose.com/buy)  
- [Ansök om en tillfällig licens](https://purchase.aspose.com/temporary-license/)  

---

**Senast uppdaterad:** 2026-06-28  
**Testat med:** Aspose.Imaging för Java 25.5  
**Författare:** Aspose

## Relaterade handledningar

- [Konvertera ODG till PNG med Aspose.Imaging för Java: En komplett guide](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Effektiv bildkonvertering i Java med Aspose.Imaging: En komplett guide](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}