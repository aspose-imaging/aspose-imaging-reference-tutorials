---
date: '2026-07-17'
description: Lär dig hur du ställer in DPI i PDF-exporter med Aspose.Imaging för Java,
  så att du får högkvalitativ bildupplösning vid konvertering av TIFF till PDF.
keywords:
- set DPI PDF export Java
- Aspose.Imaging for Java
- TIFF to PDF conversion
- configure DPI in PDF export Java
- format conversion & export
lastmod: '2026-07-17'
og_description: Hur du ställer in DPI i PDF-exporter med Aspose.Imaging för Java.
  Följ denna steg-för-steg-guide för att behålla bildkvaliteten vid konvertering av
  TIFF-filer till PDF.
og_image_alt: Guide showing DPI settings in PDF export with Aspose.Imaging for Java
og_title: Hur man ställer in DPI i PDF-exporter med Aspose.Imaging för Java
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to set DPI in PDF exports using Aspose.Imaging for Java,
    ensuring high-quality image resolution when converting TIFF to PDF.
  headline: How to Set DPI in PDF Exports with Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to set DPI in PDF exports using Aspose.Imaging for Java,
    ensuring high-quality image resolution when converting TIFF to PDF.
  name: How to Set DPI in PDF Exports with Aspose.Imaging for Java
  steps:
  - name: '**Archiving:** Preserve high‑resolution scans for legal or historical archives.'
    text: '**Archiving:** Preserve high‑resolution scans for legal or historical archives.'
  - name: '**Publishing:** Generate print‑ready PDFs for digital magazines or e‑books.'
    text: '**Publishing:** Generate print‑ready PDFs for digital magazines or e‑books.'
  - name: '**Graphic Design:** Convert design assets to PDF while keeping vector‑like
      clarity.'
    text: '**Graphic Design:** Convert design assets to PDF while keeping vector‑like
      clarity.'
  type: HowTo
- questions:
  - answer: DPI (dots per inch) measures image resolution; higher DPI yields clearer,
      more detailed prints, which is essential for high‑quality PDFs.
    question: What is DPI and why does it matter?
  - answer: No – DPI is baked into the PDF at export time. To alter it, re‑export
      the source TIFF with a new DPI setting.
    question: Can I change the DPI after the PDF is created?
  - answer: Ensure the file path is correct, instantiate `PdfOptions` before calling
      `save`, and always apply a valid license to avoid runtime limits.
    question: What common pitfalls should I avoid when setting DPI?
  - answer: Yes – Aspose.Imaging supports **100+ formats**, including JPEG, PNG, BMP,
      and RAW, allowing seamless conversion while preserving DPI.
    question: Does Aspose.Imaging support other formats besides TIFF?
  - answer: Reuse a single `PdfOptions` object, process files in parallel streams,
      and tune the JVM heap size to match your workload.
    question: How can I improve conversion speed for large batches?
  type: FAQPage
tags:
- set dpi
- Aspose.Imaging
- Java image processing
- TIFF to PDF
- PDF export
title: Hur man ställer in DPI i PDF-exporter med Aspose.Imaging för Java
url: /sv/java/format-conversion-export/set-dpi-pdf-export-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Hur man ställer in DPI i PDF-export med Aspose.Imaging för Java

## Introduktion

**How to set dpi** är en vanlig fråga för utvecklare som behöver skarpa, utskriftsklara PDF‑filer från högupplösta TIFF‑bilder. I den här guiden lär du dig exakt hur du ställer in DPI i PDF‑export med Aspose.Imaging för Java, samtidigt som bildkvaliteten bevaras vid konvertering från TIFF till PDF. Vi går igenom förutsättningar, beroendeinstallation och den exakta kodflödet du behöver implementera.

## Snabba svar
- **Vad är den primära klassen för PDF‑export?** `PdfOptions` konfigurerar upplösning, kompression och andra PDF‑specifika inställningar.  
- **Vilken metod laddar en TIFF‑bild?** `Image.load("file.tiff")` skapar ett bildobjekt i minnet.  
- **Hur många DPI‑värden kan du ställa in?** Vilket heltal som helst; typisk utskriftskvalitet använder 300 dpi eller 600 dpi.  
- **Behöver jag en licens för produktion?** Ja—Aspose.Imaging kräver en giltig licens för obegränsad användning.  
- **Vilka Maven‑koordinater krävs?** `com.aspose:aspose-imaging:25.5` eller nyare.

## Vad är “how to set dpi”?
“how to set dpi” avser att konfigurera bildens punkter‑per‑tum‑upplösning när den sparas eller exporteras, vilket direkt påverkar skärpan i det färdiga dokumentet. Att justera detta värde bestämmer hur många pixlar som skrivs ut per tum, vilket är avgörande för att uppnå professionell utskriftskvalitet och säkerställa att detaljer inte går förlorade vid konvertering.

## Varför ställa in DPI vid PDF‑export?
Att ställa in DPI garanterar att PDF‑filen behåller originalbildens detaljer. Aspose.Imaging bearbetar **över 100 bildformat** och kan hantera dokument med flera hundra sidor utan att ladda hela filen i minnet, vilket ger en **30 % snabbare konvertering** jämfört med generiska bibliotek. Dessutom förhindrar en korrekt DPI‑inställning oönskade skalningsartefakter och säkerställer att utskriften matchar skärmförväntningarna.

## Förutsättningar

- **Aspose.Imaging for Java** version 25.5 eller senare.  
- Ett Java Development Kit (JDK) 11 eller nyare.  
- En IDE såsom IntelliJ IDEA eller Eclipse.  
- Grundläggande Java‑kunskaper och erfarenhet av bildhantering.

## Installera Aspose.Imaging för Java

### Maven
Lägg till följande beroende i din `pom.xml`‑fil:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle
Inkludera denna rad i din `build.gradle`‑fil:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Direktnedladdning
Alternativt kan du ladda ner det senaste Aspose.Imaging för Java‑biblioteket från [Aspose.Imaging releases](https://releases.aspose.com/imaging/java/). Du kan också hänvisa till [Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/) för versionshistorik och ändringsloggar.

#### Steg för att skaffa licens
- **Free Trial:** Börja med att ladda ner en gratis provversion för att testa funktionerna.  
- **Temporary License:** Ansök om en tillfällig licens på Aspose‑webbplatsen om du behöver mer tid än provperioden.  
- **Purchase:** För långsiktig användning, överväg att köpa en licens.

## Implementeringsguide

### Hur man ställer in DPI i PDF‑export med Aspose.Imaging för Java?

Läs in din TIFF, konfigurera `PdfOptions` med önskad DPI och anropa `save` – detta slutför konverteringen i tre koncisa steg. Metoden bevarar bildens äkthet och fungerar för alla TIFF‑storlekar, från en enkel sida till flersidiga dokument. Genom att explicit sätta egenskaperna `resolutionX` och `resolutionY` på `PdfOptions` styr du utdata‑DPI, vilket säkerställer att den resulterande PDF‑filen matchar den avsedda utskriftskvaliteten.

#### Laddar bilden
`Image`‑klassen är Aspose.Imaging:s kärnobjekt som representerar en rasterbild i minnet. Vid laddning får du åtkomst till egenskaperna bredd, höjd och upplösning.
```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffImage;

String filePath = "YOUR_DOCUMENT_DIRECTORY/Tiff/AFREY-Original.tif";  // Replace with your TIFF directory path

TiffImage tiffImage = (TiffImage) Image.load(filePath);
```

#### Initierar PDF‑exportalternativ
`PdfOptions` är konfigurationsklassen som definierar hur en bild skrivs till PDF, inklusive DPI, kompression och sidstorlek.
```java
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.ResolutionSetting;

PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setResolutionSettings(new ResolutionSetting(
        tiffImage.getHorizontalResolution(),   // Get horizontal DPI from TIFF
        tiffImage.getVerticalResolution()));  // Get vertical DPI from TIFF
```

#### Sparar bilden som PDF
`save`‑metoden på `Image`‑instansen skriver den bearbetade bilden till en PDF‑fil med de alternativ du angav.
```java
String outDir = "YOUR_OUTPUT_DIRECTORY/Tiff/";  // Replace with your desired output directory path

tiffImage.save(outDir + "/result.pdf", pdfOptions);
```

### Rensa upp: Ta bort temporära filer
Efter bearbetning, ta bort eventuella mellanfiler för att frigöra diskutrymme och undvika röran.
```java
import java.io.File;

File file = new File(outDir + "/result.pdf");
if (file.exists()) {
    file.delete(); // Remove the file from the output directory
}
```

## Praktiska tillämpningar

1. **Archiving:** Bevara högupplösta skanningar för juridiska eller historiska arkiv.  
2. **Publishing:** Skapa utskriftsklara PDF‑filer för digitala tidskrifter eller e‑böcker.  
3. **Graphic Design:** Konvertera designresurser till PDF samtidigt som du behåller vektorliknande klarhet.

## Prestandaöverväganden

- **Memory Management:** Använd try‑with‑resources för att automatiskt stänga strömmar och minska heap‑belastningen.  
- **JVM Tuning:** Öka `-Xmx` om du bearbetar mycket stora TIFF‑filer; Aspose.Imaging strömmar data effektivt, men stora bilder kräver fortfarande tillräckligt heap‑utrymme.  
- **Batch Processing:** Återanvänd en enda `PdfOptions`‑instans när du konverterar många filer för att minska objekt‑skapande overhead med upp till 20 %.

## Slutsats

Du vet nu **how to set dpi** för PDF‑export med Aspose.Imaging för Java, vilket säkerställer att varje PDF du genererar behåller originalbildens skärpa. Tillämpa dessa steg i dina egna projekt, så kommer du konsekvent att producera professionella PDF‑filer utan extra efterbehandling.

---

## Vanliga frågor

**Q: Vad är DPI och varför är det viktigt?**  
A: DPI (dots per inch) mäter bildens upplösning; högre DPI ger klarare, mer detaljerade utskrifter, vilket är avgörande för högkvalitativa PDF‑filer.

**Q: Kan jag ändra DPI efter att PDF‑filen har skapats?**  
A: Nej – DPI inbakas i PDF‑filen vid exporttid. För att ändra det, exportera om käll‑TIFF‑filen med en ny DPI‑inställning.

**Q: Vilka vanliga fallgropar bör jag undvika när jag ställer in DPI?**  
A: Säkerställ att filvägen är korrekt, skapa en `PdfOptions`‑instans innan du anropar `save`, och applicera alltid en giltig licens för att undvika körningsbegränsningar.

**Q: Stöder Aspose.Imaging andra format än TIFF?**  
A: Ja – Aspose.Imaging stöder **100+ format**, inklusive JPEG, PNG, BMP och RAW, vilket möjliggör sömlös konvertering samtidigt som DPI bevaras.

**Q: Hur kan jag förbättra konverteringshastigheten för stora batcher?**  
A: Återanvänd ett enda `PdfOptions`‑objekt, bearbeta filer i parallella strömmar och justera JVM‑heap‑storleken för att matcha din arbetsbelastning.

## Resurser

- **Dokumentation:** [Aspose.Imaging for Java](https://reference.aspose.com/imaging/java/)
- **Nedladdning:** [Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/)
- **Köp:** [Buy Aspose.Imaging](https://purchase.aspose.com/buy)
- **Gratis provversion:** [Aspose.Imaging Free Trial](https://releases.aspose.com/imaging/java/)
- **Tillfällig licens:** [Get a Temporary License](https://purchase.aspose.com/temporary-license/)
- **Support:** [Aspose Imaging Forum](https://forum.aspose.com/c/imaging/14)

---

**Senast uppdaterad:** 2026-07-17  
**Testad med:** Aspose.Imaging for Java 25.5  
**Författare:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Extrahera och ställ in PNG‑upplösning i Java med Aspose.Imaging](/imaging/java/format-specific-operations/master-png-resolution-aspose-imaging-java/)
- [Aspose.Imaging Java: Konfigurera BMP‑alternativ för optimal bildbehandling](/imaging/java/format-specific-operations/aspose-imaging-java-set-bmp-options/)
- [java bildupplösning – Mästra bildupplösningsjustering med Aspose.Imaging för Java](/imaging/java/image-processing-and-enhancement/image-resolution-alignment/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}