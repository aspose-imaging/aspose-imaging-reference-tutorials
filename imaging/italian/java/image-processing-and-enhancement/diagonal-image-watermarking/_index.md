---
title: Filigrana immagine diagonale con Aspose.Imaging per Java
linktitle: Filigrana immagine diagonale
second_title: Aspose.Imaging API Java di elaborazione delle immagini
description: Migliora le tue immagini con una filigrana diagonale utilizzando Aspose.Imaging per Java. Segui questa guida passo passo e crea splendide immagini con filigrana senza sforzo.
weight: 14
url: /it/java/image-processing-and-enhancement/diagonal-image-watermarking/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Filigrana immagine diagonale con Aspose.Imaging per Java


Se stai cercando di migliorare le tue immagini con un'elegante filigrana diagonale, Aspose.Imaging per Java è qui per aiutarti. In questa guida passo passo ti guideremo attraverso il processo di aggiunta di una filigrana di testo ruotata di 45 gradi a un'immagine JPG esistente. Non è necessario essere un esperto di Java o di elaborazione delle immagini per seguire: suddivideremo ogni esempio in più passaggi per assicurarti di poter ottenere facilmente risultati professionali.

## Prerequisiti

Prima di immergerci nell'entusiasmante mondo della filigrana delle immagini, avrai bisogno di alcune cose:

1.  Aspose.Imaging per Java: assicurati di avere Aspose.Imaging per Java installato. È possibile trovare il collegamento per il download[Qui](https://releases.aspose.com/imaging/java/).

2. Ambiente di sviluppo Java: dovresti avere un ambiente di sviluppo Java funzionante configurato sul tuo computer.

3. Un'immagine da filigranare: prepara l'immagine a cui vuoi applicare la filigrana e memorizzala in una directory. È possibile utilizzare un'immagine di esempio per questo tutorial.

## Importa pacchetti

Innanzitutto, importa i pacchetti necessari per preparare il tuo progetto Java per la filigrana delle immagini. Di seguito sono riportati i pacchetti essenziali che è necessario includere:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Passaggio 1: carica un'immagine esistente

Carica l'immagine a cui desideri applicare la filigrana. In questo esempio, presupponiamo che tu abbia un'immagine JPG denominata "SampleTiff1.tiff" nella directory "ModifyingImages".

```java
// Il percorso della directory dei documenti.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Carica un'immagine JPG esistente
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Il resto del codice va qui
}
```

## Passaggio 2: preparare il testo e la grafica della filigrana

Ora dichiariamo il testo della filigrana e impostiamo la grafica per la filigrana.

```java
// Dichiarare un oggetto String con testo filigrana
String theString = "45 Degree Rotated Text";

// Crea e inizializza un'istanza della classe Graphics
Graphics graphics = new Graphics(image);

// Inizializza un oggetto di SizeF per memorizzare la dimensione dell'immagine
Size sz = graphics.getImage().getSize();
```

## Passaggio 3: Definisci carattere e pennello

Imposta il carattere e il pennello per la filigrana. Puoi personalizzare il carattere, la dimensione e lo stile in base alle tue preferenze.

```java
// Crea un'istanza di Font, inizializzala con Font Face, Size e Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Crea un'istanza di SolidBrush e imposta le sue varie proprietà
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Passaggio 4: formatta il testo

Definisci il formato del testo della filigrana, inclusi l'allineamento e i contrassegni di formato.

```java
// Inizializza un oggetto della classe StringFormat e imposta le sue varie proprietà
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Passaggio 5: applicare la trasformazione

Crea una matrice di trasformazione per posizionare e ruotare il testo della filigrana. In questo esempio, ruoteremo il testo di 45 gradi.

```java
// Crea un oggetto della classe Matrix per la trasformazione
Matrix matrix = new Matrix();
//Prima una traslazione poi una rotazione
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Imposta la trasformazione tramite Matrix
graphics.setTransform(matrix);
```

## Passaggio 6: disegna e salva

Ora è il momento di aggiungere il testo all'immagine e salvare l'immagine con filigrana nella posizione desiderata.

```java
// Disegna la stringa su Immagine
graphics.drawString(theString, font, brush, 0, 0, format);

// Salva l'output su disco
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Congratulazioni! Hai aggiunto con successo una filigrana diagonale alla tua immagine utilizzando Aspose.Imaging per Java.

## Conclusione

In questo tutorial, abbiamo imparato come migliorare le tue immagini con una filigrana diagonale utilizzando Aspose.Imaging per Java. È uno strumento potente per aggiungere un tocco professionale alle tue immagini. Con pochi semplici passaggi, puoi creare splendide immagini con filigrana che si distinguono dal resto.

## Domande frequenti

### Q1: Aspose.Imaging per Java è adatto ai principianti?

R1: Assolutamente! Aspose.Imaging per Java offre un'interfaccia intuitiva e una documentazione completa. Anche i principianti possono iniziare rapidamente con l'elaborazione delle immagini.

### Q2: Posso personalizzare il testo e lo stile della filigrana?

R2: Sì, puoi personalizzare facilmente il testo, il carattere, la dimensione, il colore e l'angolo di rotazione della filigrana in base alle tue preferenze e al tuo marchio.

### Q3: Aspose.Imaging per Java supporta altri formati di immagine oltre a JPG?

R3: Sì, Aspose.Imaging per Java supporta un'ampia gamma di formati di immagine, inclusi BMP, PNG, GIF e altri.

### Q4: È disponibile una prova gratuita per Aspose.Imaging per Java?

 R4: Sì, puoi provare Aspose.Imaging per Java con una prova gratuita. Prendilo[Qui](https://releases.aspose.com/).

### Q5: Dove posso trovare aiuto o supporto per Aspose.Imaging per Java?

 R5: Se hai domande o hai bisogno di assistenza, visita il forum di supporto Aspose.Imaging per Java[Qui](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
