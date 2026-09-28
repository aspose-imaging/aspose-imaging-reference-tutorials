---
date: '2026-09-28'
description: Lär dig hur du använder ccittfax3 compression java för att skapa flersidiga
  TIFF‑filer med Aspose.Imaging. Skanna, arkivera och minska filstorleken effektivt
  för dokumentarbetsflöden.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Upptäck steg‑för‑steg hur du använder ccittfax3 compression java med
  Aspose.Imaging för att bygga effektiva flersidiga TIFF‑filer för skanning och arkivering.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: Hur man skapar flersidig TIFF med ccittfax3 compression java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: Hur man skapar flersidig TIFF med ccittfax3 compression java
url: /sv/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mästra skapandet av flersidiga TIFF-filer med ccittfax3 compression java med Aspose.Imaging

## Introduktion

If you need to archive large volumes of scanned documents while keeping file sizes low, **ccittfax3 compression java** is the go‑to solution. This tutorial shows you how to generate multi‑page TIFF files with CCITTFAX3 compression in Java using Aspose.Imaging. You’ll learn why this compression works so well for monochrome scans, how to configure the library, and how to add each page as a frame.

**What you’ll learn**
- How to add Aspose.Imaging to a Java project.
- How to configure `TiffOptions` for CCITTFAX3 compression.
- How to create a `TiffImage`, resize source images, and add them as frames.
- How to save the final multi‑page TIFF efficiently.

Let’s walk through the complete implementation.

## Snabba svar
- **Vad är den största fördelen med CCITTFAX3-komprimering?** Upp till 80 % minskning av filstorleken för svart‑vita skanningar.  
- **Vilket bibliotek erbjuder inbyggt stöd?** Aspose.Imaging för Java, version 25.5+.  
- **Behöver jag en licens för utveckling?** En gratis provlicens fungerar för alla funktioner; en betald licens krävs för produktion.  
- **Kan jag bearbeta hundratals sidor?** Ja—Aspose.Imaging strömmar sidor, så minnesanvändningen förblir låg.  
- **Är koden kompatibel med Java 11 och senare?** Absolut; API:et riktar sig mot Java 8+.

## Vad är ccittfax3 compression java?
`CCITTFAX3` är en förlustfri, monokrom komprimeringsalgoritm designad för fax‑ och skannade dokumentbilder. Den kodar varje pixel som en enda bit, vilket ger högkvalitativt resultat samtidigt som filstorleken minskar dramatiskt—ofta med 70‑80 % jämfört med okomprimerad TIFF. Detta gör den idealisk för arkivering av svart‑vita dokument där noggrannhet måste bevaras.

## Varför använda Aspose.Imaging för denna uppgift?
Aspose.Imaging stödjer **100+** in‑ och utdataformat, inklusive PDF, PNG, JPEG och TIFF. Dess strömningsarkitektur kan hantera **flerhundratusentals‑sidiga** TIFF‑filer utan att ladda hela dokumentet i minnet, vilket gör den idealisk för storskaliga arkiveringsprojekt.

## Förutsättningar

- **Java Development Kit (JDK)** 8 eller nyare installerat.
- **IDE** såsom IntelliJ IDEA eller Eclipse.
- **Maven** eller **Gradle** för beroendehantering.
- Grundläggande Java‑kunskaper (klasser, objekt, samlingar).

## Konfigurera Aspose.Imaging för Java

Add the library to your build file.

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```  

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

### Direktnedladdning

You can also download the latest JAR from [Aspose.Imaging för Java releases](https://releases.aspose.com/imaging/java/).

### Licensanskaffning

A free trial license is available from [Asposes gratis provlicenssida](https://releases.aspose.com/imaging/java/). For production use, purchase a permanent license or request a temporary one at [Aspose Köp](https://purchase.aspose.com/temporary-license/).

For detailed API usage, see the Aspose.Imaging for Java [dokumentation](https://reference.aspose.com/imaging/java/).

### Grundläggande initiering

After adding the dependency, initialise the library as shown below.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## Hur man konfigurerar ccittfax3 compression java för en flersidig TIFF?

`TiffOptions` är en klass som definierar utdataformatet och komprimeringsinställningarna för en TIFF‑fil. Ladda `TiffOptions`‑objektet med `CCITTGroup3FaxCompression`‑enum, och sätt sedan källan för utdatafilen. Denna tvåstegs‑konfiguration förbereder skrivaren för monokrom komprimering och säkerställer att varje sida som läggs till senare kodas med CCITTFAX3‑algoritmen, vilket ger en betydande storleksreduktion samtidigt som bildkvaliteten bevaras.

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## Hur man skapar en TiffImage‑instans i Java?

`TiffImage` representerar ett flersidigt TIFF‑dokument i minnet och tillhandahåller metoder för att manipulera dess ramar. Definiera först bredden och höjden som alla sidor ska dela. Instansiera sedan `TiffImage` med de tidigare skapade `TiffOptions`. `TiffImage`‑objektet fungerar som en behållare för de enskilda ramarna, så att du kan lägga till, ta bort eller omordna sidor innan du sparar den slutliga filen.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## Hur man laddar och ändrar storlek på källbilder från en mapp?

Filtrera målkatalogen efter JPEG‑filer, läs varje bild och ändra storlek så att den matchar TIFF‑canvasen. Att ändra storlek innan ramar läggs till minskar minnesförbrukningen och påskyndar sparningsoperationen. Genom att konvertera varje källbild till de erforderliga dimensionerna och pixelformatet säkerställer du en konsekvent sidlayout och undviker körningsfel när ramarna läggs till TIFF‑dokumentet.

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## Hur man lägger till varje bild som en ram i den flersidiga TIFF‑filen?

`TiffFrame` är ett objekt som innehåller en enskild sidbild och dess associerade metadata inom en TIFF. Iterera över de storleksändrade bilderna, skapa en ny `TiffFrame` och lägg till den i `TiffImage`. Varje ram blir en separat sida i det slutliga dokumentet, och biblioteket hanterar automatiskt nödvändiga metadatauppdateringar, såsom sidantal och offset, vilket säkerställer en giltig flersidig TIFF‑struktur.

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## Hur man sparar den slutliga flersidiga TIFF‑filen?

Anropa `save`‑metoden på `TiffImage`‑instansen och ange den önskade utdata‑sökvägen. Biblioteket skriver automatiskt alla ramar med CCITTFAX3‑komprimering, strömmar data till disken effektivt och stänger eventuella underliggande resurser. När sparningsoperationen är klar innehåller den resulterande filen alla sidor med den angivna komprimeringen, redo för distribution eller arkivering.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## Praktiska tillämpningar

- **Dokumentarkivering:** Lagra skannade kontrakt, fakturor eller juridiska handlingar med minimal lagringskostnad.  
- **Medicinsk bildbehandling:** Komprimera radiologiska skanningar samtidigt som diagnostisk detalj bevaras.  
- **Tryckproduktion:** Generera flersidiga utskriftsjobb som skrivare kan använda direkt.

## Prestandaöverväganden

- Använd `ResizeOptions` som bevarar bildförhållandet för att undvika förvrängning.  
- Stäng varje `Image`‑objekt efter att dess ram har lagts till för att frigöra inbyggt minne.  
- För mycket stora batcher, bearbeta filer i parallella strömmar och skriv varje TIFF‑segment asynkront.

## Vanliga fallgropar och felsökning

- **Fel pixelformat:** CCITTFAX3 fungerar endast med 1‑bit (svart‑vita) bilder. Konvertera färgbilder till gråskala innan storleksändring.  
- **Minnesläckor:** Anropa alltid `dispose()` på temporära `Image`‑objekt; annars förblir inbyggda buffertar allokerade.  
- **Filstorlek minskas inte:** Säkerställ att `TiffOptions`‑komprimeringsegenskapen är satt; annars används standard (ingen komprimering).

## Vanliga frågor

**Q: Kan jag använda detta tillvägagångssätt med färgbilder?**  
A: CCITTFAX3 är begränsad till monokroma data; för färg använd JPEG eller LZW‑komprimering istället.

**Q: Stöder Aspose.Imaging strömning för enorma TIFF‑filer?**  
A: Ja—biblioteket skriver varje ram direkt till utdata‑strömmen, vilket håller minnesanvändningen låg även för tusentals sidor.

**Q: Hur applicerar jag en tillfällig licens programmässigt?**  
A: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.

**Q: Finns det ett sätt att förhandsgranska TIFF‑filen innan sparning?**  
A: Du kan rendera varje `TiffFrame` till en `BufferedImage` och visa den i en Swing‑komponent.

**Q: Vilka Java‑versioner stöds officiellt?**  
A: Aspose.Imaging stödjer Java 8 till Java 21, inklusive LTS‑utgåvor.

## Slutsats

Du har nu ett komplett, produktionsklart arbetsflöde för att skapa flersidiga TIFF‑filer med **ccittfax3 compression java** med Aspose.Imaging. Genom att följa stegen ovan kan du effektivt arkivera enorma dokumentsamlingar samtidigt som lagringskostnaderna hålls låga och bildkvaliteten hög. Utforska ytterligare Aspose.Imaging‑funktioner—såsom OCR, metadatahantering och formatkonvertering—för att ytterligare förbättra din dokumentbehandlingspipeline.

---

**Senast uppdaterad:** 2026-09-28  
**Testat med:** Aspose.Imaging 25.5 för Java  
**Författare:** Aspose

## Relaterade handledningar

- [Hur man skapar flersidig TIFF med Aspose.Imaging för Java – En komplett guide](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Hur man minskar bildfilens storlek med LZW‑komprimering i Java](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Dela upp flersidiga TIFF‑ramar med Aspose.Imaging för Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}