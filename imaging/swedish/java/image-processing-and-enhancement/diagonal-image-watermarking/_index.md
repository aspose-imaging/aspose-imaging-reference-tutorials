---
date: 2026-01-09
description: Lär dig hur du lägger till en vattenstämpel på bilder med Aspose.Imaging
  för Java. Denna Java‑bildbehandlingshandledning visar steg för steg hur du snabbt
  skapar en diagonal vattenstämpel.
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: Hur man lägger till vattenstämpel – Diagonal bildvattenmärkning (Java)
url: /sv/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Hur man lägger till vattenstämpel – Diagonal bildvattenmärkning (Java)

Om du vill **how to add watermark** till dina bilder med en stilfull diagonal orientering, gör Aspose.Imaging for Java det enkelt. I den här steg‑för‑steg‑handledningen går vi igenom hur man lägger till en 45‑grad roterad textvattenstämpel på en JPG (eller någon annan stödd) bild. Du behöver inte vara ett Java‑geni – varje block förklaras på enkel svenska så att du kan reproducera resultatet på några minuter.

## Snabba svar
- **Vilket bibliotek används?** Aspose.Imaging for Java  
- **Vilket primärt nyckelord täcks?** how to add watermark  
- **Stödda bildformat?** JPEG, PNG, BMP, TIFF, GIF och mer  
- **Hur mycket kod krävs?** Endast sju koncisa kodblock  
- **Behöver jag en licens för testning?** En gratis provversion finns tillgänglig; en licens krävs för produktion  

## Vad betyder “how to add watermark” i bildbehandling?
Att lägga till en vattenstämpel innebär att överlagra halvgenomskinlig text eller grafik på en bild för att skydda äganderätt eller förmedla varumärke. En diagonal vattenstämpel är särskilt effektiv eftersom den sträcker sig över hela bilden och är svårare att beskära bort.

## Varför använda Aspose.Imaging for Java?
Aspose.Imaging erbjuder ett hög‑nivå API som abstraherar låg‑nivå pixelmanipulation, stödjer dussintals format och fungerar på alla Java‑miljöer. Det låter dig fokusera på *vad* du vill uppnå—som att lägga till en diagonal vattenstämpel—utan att oroa dig för bildformatets egenheter.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1. **Aspose.Imaging for Java** – ladda ner den senaste versionen från den officiella sidan **[here](https://releases.aspose.com/imaging/java/)**.  
2. **Java Development Environment** – JDK 8+ och din favorit‑IDE (IntelliJ, Eclipse, VS Code, etc.).  
3. **En bild att vattenmärka** – placera ett exempel‑JPG/TIFF/PNG i en mapp som du kommer referera till i koden.

## Importera paket

Först, importera de klasser du behöver. Att hålla importerna samlade gör koden lättare att läsa och underhålla.

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Steg 1: Ladda en befintlig bild

Vi börjar med att ladda källbilden. Metoden `Image.load` upptäcker automatiskt formatet.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **Proffstips:** Wrappa `Image`‑objektet i ett try‑with‑resources‑block (som visas) så att det frigörs automatiskt, vilket förhindrar minnesläckor.

## Steg 2: Förbered vattenstämpeltext och grafik

Skapa ett `Graphics`‑objekt kopplat till den laddade bilden och spara bildens storlek för senare beräkningar.

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## Steg 3: Definiera teckensnitt och pensel

Välj ett teckensnitt som sticker ut och en pensel som definierar vattenstämpelns färg och opacitet. Justera opaciteten för att göra vattenstämpeln halvgenomskinlig.

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Steg 4: Formatera din text

Ställ in justering och formateringsflaggor så att texten centreras när den ritas.

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Steg 5: Tillämpa transformation

En transformationsmatris låter oss flytta origo till bildens centrum och sedan rotera texten med ‑45° (medurs).

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## Steg 6: Rita och spara

Till sist, rendera strängen på bilden och skriv resultatet till disk.

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

När du öppnar `AddDiagonalWatermarkToImage_out.jpg` kommer du att se den röda, halvgenomskinliga texten lutad över bildens centrum.

## Vanliga problem & lösningar

| Problem | Orsak | Lösning |
|---------|-------|---------|
| Vattenstämpeln är för svag | Opaciteten är satt till 0 (helt genomskinlig) | Öka opaciteten, t.ex. `brush.setOpacity(0.5f);` |
| Texten klipps av i kanterna | Översättningen är inte centrerad för icke‑kvadratiska bilder | Använd `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` som visas, justera sedan rotationsvinkeln vid behov |
| Fel: ej stödd bildformat | Använder en äldre version av Aspose.Imaging | Uppdatera till den senaste Aspose.Imaging‑utgåvan |

## Vanliga frågor

### Q1: Är Aspose.Imaging for Java lämplig för nybörjare?

**A:** Absolut! API:et är intuitivt och dokumentationen ger tydliga exempel. Även utvecklare som är nya inom bildbehandling kan följa den här handledningen och snabbt producera professionella resultat.

### Q2: Kan jag anpassa vattenstämpelns text och stil?

**A:** Ja. Ändra variabeln `theString`, välj ett annat `Font`, modifiera `brush.setColor(...)`, eller justera rotationsvinkeln i matrisen för att passa ditt varumärke.

### Q3: Stöder Aspose.Imaging for Java andra bildformat förutom JPG?

**A:** Ja. Biblioteket fungerar med BMP, PNG, GIF, TIFF, PSD och många fler. Peka bara `Image.load`‑metoden på rätt fil.

### Q4: Finns det en gratis provversion av Aspose.Imaging for Java?

**A:** Ja, du kan prova Aspose.Imaging for Java med en gratis provversion. Skaffa den **[here](https://releases.aspose.com/)**.

### Q5: Var kan jag hitta hjälp eller support för Aspose.Imaging for Java?

**A:** För frågor, felrapporter eller bästa praxis‑råd, besök Aspose.Imaging for Java‑supportforumet **[here](https://forum.aspose.com/)**.

---

**Senast uppdaterad:** 2026-01-09  
**Testat med:** Aspose.Imaging for Java 24.11 (latest at time of writing)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}