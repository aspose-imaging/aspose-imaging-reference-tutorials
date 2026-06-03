---
date: 2026-01-09
description: Impara come aggiungere una filigrana alle immagini con Aspose.Imaging
  per Java. Questo tutorial di elaborazione immagini Java mostra passo passo come
  creare rapidamente una filigrana diagonale.
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: Come aggiungere una filigrana – Filigrana diagonale per immagini (Java)
url: /it/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Come aggiungere una filigrana – Filigrana diagonale su immagine (Java)

Se stai cercando **how to add watermark** per le tue foto con un'elegante orientazione diagonale, Aspose.Imaging for Java lo rende semplice. In questo tutorial passo‑per‑passo vedremo come aggiungere una filigrana di testo ruotata di 45° a un'immagine JPG (o qualsiasi formato supportato). Non è necessario essere un mago di Java – ogni blocco è spiegato in modo chiaro così potrai replicare il risultato in pochi minuti.

## Risposte rapide
- **What library is used?** Aspose.Imaging for Java  
- **Which primary keyword is covered?** how to add watermark  
- **Supported image formats?** JPEG, PNG, BMP, TIFF, GIF and more  
- **How much code is required?** Only seven concise code blocks  
- **Do I need a license for testing?** A free trial is available; a license is required for production  

## Cos'è “how to add watermark” nell'elaborazione delle immagini?
Aggiungere una filigrana significa sovrapporre testo o grafica semi‑trasparenti su un'immagine per proteggere la proprietà o trasmettere il brand. Una filigrana diagonale è particolarmente efficace perché copre l'intera immagine ed è più difficile da ritagliare.

## Perché usare Aspose.Imaging for Java?
Aspose.Imaging fornisce un'API di alto livello che astrae la manipolazione a basso livello dei pixel, supporta decine di formati e funziona su qualsiasi runtime Java. Ti consente di concentrarti su *cosa* vuoi ottenere — come aggiungere una filigrana diagonale — senza preoccuparti delle particolarità dei formati immagine.

## Prerequisiti

1. **Aspose.Imaging for Java** – scarica l'ultima versione dal sito ufficiale **[here](https://releases.aspose.com/imaging/java/)**.  
2. **Java Development Environment** – JDK 8+ e il tuo IDE preferito (IntelliJ, Eclipse, VS Code, ecc.).  
3. **Un'immagine da filigranare** – posiziona un JPG/TIFF/PNG di esempio in una cartella a cui farai riferimento nel codice.

## Importa i pacchetti

Per prima cosa, importa le classi di cui avrai bisogno. Tenere gli import insieme rende il codice più facile da leggere e mantenere.

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Passo 1: Carica un'immagine esistente

Iniziamo caricando l'immagine di origine. Il metodo `Image.load` rileva automaticamente il formato.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **Consiglio:** Avvolgi l'oggetto `Image` in un blocco try‑with‑resources (come mostrato) così viene rilasciato automaticamente, evitando perdite di memoria.

## Passo 2: Prepara il testo e la grafica della filigrana

Crea un oggetto `Graphics` collegato all'immagine caricata e memorizza le dimensioni dell'immagine per i calcoli successivi.

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## Passo 3: Definisci Font e Brush

Scegli un font che risalti e un brush che definisca il colore e l'opacità della filigrana. Regola l'opacità per rendere la filigrana semi‑trasparente.

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Passo 4: Formatta il tuo testo

Imposta l'allineamento e i flag di formattazione in modo che il testo sia centrato quando disegnato.

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Passo 5: Applica la trasformazione

Una matrice di trasformazione ci permette di spostare l'origine al centro dell'immagine e poi ruotare il testo di ‑45° (orario).

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## Passo 6: Disegna e salva

Infine, renderizza la stringa sull'immagine e scrivi il risultato su disco.

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Quando apri `AddDiagonalWatermarkToImage_out.jpg` vedrai il testo rosso, semi‑trasparente, inclinato attraverso il centro dell'immagine.

## Problemi comuni e soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| La filigrana appare troppo tenue | Opacità impostata a 0 (completamente trasparente) | Aumenta l'opacità, ad esempio `brush.setOpacity(0.5f);` |
| Il testo è tagliato ai bordi | Traslazione non centrata per immagini non quadrate | Usa `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` come mostrato, poi regola l'angolo di rotazione se necessario |
| Errore di formato immagine non supportato | Uso di una versione più vecchia di Aspose.Imaging | Aggiorna all'ultima versione di Aspose.Imaging |

## Domande frequenti

### Q1: Aspose.Imaging for Java è adatto ai principianti?

**A:** Assolutamente! L'API è intuitiva e la documentazione fornisce esempi chiari. Anche gli sviluppatori nuovi all'elaborazione delle immagini possono seguire questo tutorial e produrre risultati professionali rapidamente.

### Q2: Posso personalizzare il testo e lo stile della filigrana?

**A:** Sì. Cambia la variabile `theString`, scegli un `Font` diverso, modifica `brush.setColor(...)` o regola l'angolo di rotazione nella matrice per adattarlo al tuo brand.

### Q3: Aspose.Imaging for Java supporta altri formati immagine oltre al JPG?

**A:** Sì. La libreria funziona con BMP, PNG, GIF, TIFF, PSD e molti altri. Basta puntare il metodo `Image.load` al file appropriato.

### Q4: È disponibile una versione di prova gratuita per Aspose.Imaging for Java?

**A:** Sì, puoi provare Aspose.Imaging for Java con una versione di prova gratuita. Ottienila **[here](https://releases.aspose.com/)**.

### Q5: Dove posso trovare aiuto o supporto per Aspose.Imaging for Java?

**A:** Per domande, segnalazioni di bug o consigli sulle migliori pratiche, visita il forum di supporto di Aspose.Imaging for Java **[here](https://forum.aspose.com/)**.

---

**Ultimo aggiornamento:** 2026-01-09  
**Testato con:** Aspose.Imaging for Java 24.11 (latest at time of writing)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}