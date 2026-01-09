---
date: 2026-01-09
description: Leer hoe u een watermerk aan afbeeldingen kunt toevoegen met Aspose.Imaging
  voor Java. Deze Java‑afbeeldingsverwerkingstutorial laat stap‑voor‑stap zien hoe
  u snel een diagonaal watermerk kunt maken.
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: Hoe een watermerk toe te voegen – Diagonale afbeelding watermerken (Java)
url: /nl/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een Watermerk Toevoegen – Diagonale Afbeeldingswatermerken (Java)

Als je wilt weten **hoe je een watermerk toevoegt** aan je afbeeldingen met een stijlvolle diagonale oriëntatie, maakt Aspose.Imaging voor Java het moeiteloos. In deze stap‑voor‑stap‑handleiding lopen we door het toevoegen van een 45‑graden geroteerd tekstwatermerk aan een JPG (of een ander ondersteund) beeld. Je hoeft geen Java‑goeroe te zijn – elk blok wordt in eenvoudige taal uitgelegd zodat je het resultaat binnen enkele minuten kunt reproduceren.

## Snelle Antwoorden
- **Welke bibliotheek wordt gebruikt?** Aspose.Imaging voor Java  
- **Welk primair trefwoord wordt behandeld?** how to add watermark  
- **Ondersteunde afbeeldingsformaten?** JPEG, PNG, BMP, TIFF, GIF en meer  
- **Hoeveel code is nodig?** Slechts zeven beknopte code‑blokken  
- **Heb ik een licentie nodig voor testen?** Een gratis proefversie is beschikbaar; een licentie is vereist voor productie  

## Wat betekent “how to add watermark” in beeldverwerking?
Een watermerk toevoegen betekent semi‑transparante tekst of grafische elementen over een afbeelding leggen om eigendom te beschermen of branding over te brengen. Een diagonale watermerk is bijzonder effectief omdat het de hele afbeelding bestrijkt en moeilijker bij te snijden is.

## Waarom Aspose.Imaging voor Java gebruiken?
Aspose.Imaging biedt een high‑level API die low‑level pixelmanipulatie abstracteert, tientallen formaten ondersteunt en werkt op elke Java‑runtime. Het laat je focussen op *wat* je wilt bereiken — zoals het toevoegen van een diagonale watermerk — zonder je zorgen te maken over eigenaardigheden van afbeeldingsformaten.

## Vereisten

Voordat we beginnen, zorg dat je het volgende hebt:

1. **Aspose.Imaging voor Java** – download de nieuwste versie van de officiële site **[hier](https://releases.aspose.com/imaging/java/)**.  
2. **Java‑ontwikkelomgeving** – JDK 8+ en je favoriete IDE (IntelliJ, Eclipse, VS Code, enz.).  
3. **Een afbeelding om te watermerken** – plaats een voorbeeld‑JPG/TIFF/PNG in een map die je in de code gaat refereren.

## Pakketten Importeren

Importeer eerst de klassen die je nodig hebt. Het samenhouden van imports maakt de code makkelijker leesbaar en onderhoudbaar.

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Stap 1: Een Bestaande Afbeelding Laden

We beginnen met het laden van de bronafbeelding. De methode `Image.load` detecteert automatisch het formaat.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **Pro tip:** Plaats het `Image`‑object in een try‑with‑resources‑blok (zoals getoond) zodat het automatisch wordt vrijgegeven, waardoor geheugenlekken worden voorkomen.

## Stap 2: Watermerktekst en Grafische Objecten Voorbereiden

Maak een `Graphics`‑object gekoppeld aan de geladen afbeelding en sla de afbeeldingsgrootte op voor latere berekeningen.

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## Stap 3: Lettertype en Penseel Definiëren

Kies een lettertype dat opvalt en een penseel dat de kleur en opacity van het watermerk bepaalt. Pas de opacity aan om het watermerk semi‑transparant te maken.

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Stap 4: Tekst Formatteren

Stel uitlijnings‑ en formatteringsvlaggen in zodat de tekst gecentreerd wordt wanneer deze wordt getekend.

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Stap 5: Transformatie Toepassen

Een transformatie‑matrix laat ons de oorsprong naar het midden van de afbeelding verplaatsen en vervolgens de tekst met ‑45° (met de klok mee) roteren.

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## Stap 6: Tekst Tekenen en Opslaan

Render tenslotte de string op de afbeelding en schrijf het resultaat naar schijf.

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Wanneer je `AddDiagonalWatermarkToImage_out.jpg` opent, zie je de rode, semi‑transparante tekst schuin over het midden van de afbeelding.

## Veelvoorkomende Problemen & Oplossingen

| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| Watermerk is te zwak | Opacity ingesteld op 0 (volledig transparant) | Verhoog de opacity, bijv. `brush.setOpacity(0.5f);` |
| Tekst wordt afgesneden aan de randen | Translatie niet gecentreerd voor niet‑vierkante afbeeldingen | Gebruik `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` zoals getoond, en pas de rotatiehoek indien nodig |
| Fout: niet‑ondersteund afbeeldingsformaat | Een oudere versie van Aspose.Imaging wordt gebruikt | Update naar de nieuwste Aspose.Imaging‑release |

## Veelgestelde Vragen

### Q1: Is Aspose.Imaging voor Java geschikt voor beginners?

**A:** Absoluut! De API is intuïtief en de documentatie biedt duidelijke voorbeelden. Zelfs ontwikkelaars die nieuw zijn in beeldverwerking kunnen deze handleiding volgen en snel professionele resultaten behalen.

### Q2: Kan ik de watermerktekst en stijl aanpassen?

**A:** Ja. Wijzig de variabele `theString`, kies een ander `Font`, wijzig `brush.setColor(...)`, of pas de rotatiehoek in de matrix aan om bij je branding te passen.

### Q3: Ondersteunt Aspose.Imaging voor Java andere afbeeldingsformaten naast JPG?

**A:** Ja. De bibliotheek werkt met BMP, PNG, GIF, TIFF, PSD en nog veel meer. Verwijs de `Image.load`‑methode gewoon naar het juiste bestand.

### Q4: Is er een gratis proefversie beschikbaar voor Aspose.Imaging voor Java?

**A:** Ja, je kunt Aspose.Imaging voor Java uitproberen met een gratis proefversie. Haal het **[hier](https://releases.aspose.com/)**.

### Q5: Waar kan ik hulp of ondersteuning vinden voor Aspose.Imaging voor Java?

**A:** Voor vragen, bug‑rapporten of best‑practice‑advies, bezoek het Aspose.Imaging voor Java support‑forum **[hier](https://forum.aspose.com/)**.

---

**Laatst bijgewerkt:** 2026-01-09  
**Getest met:** Aspose.Imaging voor Java 24.11 (latest op het moment van schrijven)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}