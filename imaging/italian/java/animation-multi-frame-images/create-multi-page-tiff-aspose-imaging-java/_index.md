---
date: '2026-11-16'
description: Scopri come creare un multi page tiff con Aspose.Imaging per Java. Converti
  le immagini in tiff, combina i fotogrammi e ottimizza lo spazio di archiviazione
  in una guida completa.
keywords:
- create multi page tiff
- convert images to tiff
- aspose imaging java
- java image processing tutorial
- multi-page tiff generation
lastmod: '2026-11-16'
og_description: Crea un multi page tiff utilizzando Aspose.Imaging per Java. Questa
  guida passo‑passo mostra come convertire le immagini in tiff, aggiungere fotogrammi
  e ottimizzare lo spazio di archiviazione.
og_image_alt: 'Developer guide: create multi page tiff using Aspose.Imaging for Java'
og_title: Crea un multi page tiff con Aspose.Imaging per Java
schemas:
- author: Aspose
  dateModified: '2026-11-16'
  description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  headline: How to create multi page tiff using Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  name: How to create multi page tiff using Aspose.Imaging for Java
  steps:
  - name: load an image
    text: '`Image.load` reads the image file into memory and returns an `Image` object
      that you can manipulate. Ensure the file path is correct to avoid `FileNotFoundException`.'
  - name: resize the image
    text: '`ResizeType.NearestNeighbourResample` preserves hard edges and pixel data,
      which is ideal when you need a faithful representation of scanned documents.'
  - name: set up TIFF options
    text: '`TiffOptions` defines the compression, bits per pixel, and other TIFF‑specific
      settings. The `source` property points to the file where the multi‑page TIFF
      will be saved.'
  - name: initialize the TIFF image
    text: '`TiffImage.create` creates an empty TIFF container with the width and height
      derived from the first resized image. This container will later hold each frame
      you add.'
  - name: load additional images
    text: The loop iterates over every file ending with `.img` (or any supported raster
      format) in the target directory, loads each image, and calls `savePixels` to
      copy pixel data into a new frame of the TIFF.
  - name: save your work
    text: '`image.save` writes the complete multi‑page TIFF to the output path you
      specified in `TiffOptions`. Verify that the directory is writable to avoid `IOException`.'
  type: HowTo
- questions:
  - answer: Absolutely. Load any supported raster format (PNG, JPEG, BMP, etc.) and
      add each as a frame using the same workflow.
    question: Can I convert PNG or JPEG files to a multi‑page TIFF with this approach?
  - answer: Yes. Call `tiffOptions.setCompression(TiffCompression.Lzw)` before creating
      the image to reduce file size while preserving quality.
    question: Is it possible to set compression (e.g., LZW) for the output TIFF?
  - answer: Use `frame.getMetadata().addProperty("Author", "Your Name")` after creating
      the frame and before saving.
    question: How do I add metadata (author, description) to each TIFF frame?
  - answer: It does. Load the file with `Image.load("existing.tiff")` and iterate
      through `((TiffImage)image).getFrames()` to access each page.
    question: Does Aspose.Imaging support reading existing multi‑page TIFFs?
  - answer: Process pages in batches, call `System.gc()` periodically, and use the
      try‑with‑resources pattern to release native memory promptly.
    question: What if I need to process thousands of pages?
  type: FAQPage
tags:
- create multi page tiff
- Aspose.Imaging
- Java image processing
- TIFF conversion
title: Come creare un multi page tiff usando Aspose.Imaging per Java
url: /it/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come creare un TIFF multipagina usando Aspose.Imaging per Java

## Introduzione

Creare un **TIFF multipagina** è una necessità comune quando devi archiviare diverse immagini correlate in un unico file compatto. Che tu stia costruendo un sistema di gestione documentale, una pipeline di imaging medico o uno strumento di elaborazione batch, Aspose.Imaging per Java ti offre il pieno controllo sulla creazione del TIFF, sulla compressione e sulla gestione dei frame. In questa guida imparerai a caricare, ridimensionare e combinare più immagini in un unico TIFF multipagina, mantenendo basso l'uso della memoria e alte le prestazioni.

**Cosa imparerai**
- Caricare e ridimensionare le immagini con Aspose.Imaging.
- Configurare `TiffOptions` per l'output multipagina.
- Aggiungere frame da diverse immagini di origine.
- Salvare il TIFF finale con compressione opzionale.
- Scenari reali in cui i TIFF multipagina si distinguono.

## Risposte rapide
- **Qual è la libreria principale?** Aspose.Imaging per Java.  
- **Posso convertire le immagini in TIFF?** Sì – il tutorial mostra come combinare PNG, JPEG, BMP e altri formati in un TIFF multipagina.  
- **Ho bisogno di una licenza?** Una prova gratuita è sufficiente per la valutazione; è necessaria una licenza permanente per l'uso in produzione.  
- **Quale versione di Java è richiesta?** Java 8 o superiore (JDK 8+).  
- **Il codice è thread‑safe?** L'esempio viene eseguito su un singolo thread; per scenari concorrenti, gestire gli oggetti `Image` per thread.

## Come creare un TIFF multipagina?

Carica le immagini di origine, ridimensionali se necessario, configura `TiffOptions`, aggiungi ogni immagine come frame e chiama `save`. Questo flusso conciso crea un TIFF multipagina conforme agli standard in poche righe di codice Java, consentendoti di controllare compressione e dimensioni delle pagine.

## Cos'è un TIFF multipagina?

Un TIFF multipagina è un singolo file TIFF che contiene diversi frame immagine, ciascuno rappresentante una pagina. È ampiamente usato per archiviazione, fax e applicazioni di scansione documenti perché consente di memorizzare molte pagine senza l'overhead di file separati.

## Prerequisiti

- Libreria **Aspose.Imaging per Java** (scarica dai link sotto).  
- **JDK 8+** installato e configurato nel tuo IDE (IntelliJ IDEA, Eclipse, ecc.).  
- Conoscenza di base di Java e familiarità con I/O di file.

## Configurare Aspose.Imaging per Java

Per iniziare a lavorare con Aspose.Imaging, devi integrarlo nel tuo progetto. Ecco come farlo con i più popolari strumenti di build:

**Maven:**  
Aggiungi la seguente dipendenza al tuo `pom.xml`:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle:**  
Includi questo nel tuo file `build.gradle`:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

In alternativa, puoi **scaricare direttamente** l'ultimo JAR di Aspose.Imaging per Java da [Aspose releases](/imaging/java/).

### Acquisizione della licenza

Puoi iniziare con una prova gratuita per esplorare le funzionalità di Aspose.Imaging. Per un uso prolungato, considera di richiedere una licenza temporanea o di acquistare una licenza completa:
- **Prova gratuita:** Visita [Aspose Imaging Java Releases](/imaging/java/) per scaricare e provare la libreria.  
- **Licenza temporanea:** Ottienila da [Aspose Temporary License Page](/purchase/temporary-license/).  
- **Acquisto:** Per una soluzione permanente, vai a [Aspose Purchase](/purchase/buy).

## Caricamento e ridimensionamento di un'immagine

**Panoramica:**  
Il primo passo consiste nel caricare un'immagine dal file system e ridimensionarla usando il metodo di ricampionamento nearest‑neighbor.

#### Passo 1: caricare un'immagine
`Image.load` legge il file immagine in memoria e restituisce un oggetto `Image` che puoi manipolare. Assicurati che il percorso del file sia corretto per evitare `FileNotFoundException`.  
```java
import com.aspose.imaging.Image;

String dataDir = "YOUR_DOCUMENT_DIRECTORY";
Image tempImage = Image.load(dataDir + "/Image1.png");
```

#### Passo 2: ridimensionare l'immagine
`ResizeType.NearestNeighbourResample` preserva i bordi netti e i dati dei pixel, ideale quando è necessaria una rappresentazione fedele dei documenti scansionati.  
```java
int width = tempImage.getWidth();
int height = tempImage.getHeight();
tempImage.resize(width, height, ResizeType.NearestNeighbourResample);
```

## Creazione delle opzioni TIFF e della sorgente

**Panoramica:**  
Successivamente, impostiamo le opzioni necessarie per creare un nuovo file TIFF multipagina. Questo comporta la specifica del formato previsto e della configurazione della sorgente.

#### Passo 1: impostare le opzioni TIFF
`TiffOptions` definisce la compressione, i bit per pixel e altre impostazioni specifiche del TIFF. La proprietà `source` indica il file dove verrà salvato il TIFF multipagina.  
```java
import com.aspose.imaging.fileformats.tiff.TiffOptions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.sources.FileCreateSource;

TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setSource(new FileCreateSource("YOUR_DOCUMENT_DIRECTORY/MultiPage.tiff", false));
```

## Creazione e inizializzazione di un'immagine TIFF multipagina

**Panoramica:**  
Ora, creiamo un'istanza di un'immagine TIFF multipagina con le dimensioni specificate.

#### Passo 1: inizializzare l'immagine TIFF
`TiffImage.create` crea un contenitore TIFF vuoto con larghezza e altezza derivati dalla prima immagine ridimensionata. Questo contenitore conterrà in seguito ogni frame aggiunto.  
```java
import com.aspose.imaging.fileformats.tiff.TiffImage;

TiffImage tiffImage = (TiffImage) Image.create(tiffOptions, width, height);
```

## Elaborazione di più immagini e aggiunta di frame al TIFF

**Panoramica:**  
Questa sezione prevede l'aggiunta di più immagini come frame nel tuo file TIFF multipagina.

#### Passo 1: caricare immagini aggiuntive
Il ciclo itera su ogni file che termina con `.img` (o qualsiasi formato raster supportato) nella directory di destinazione, carica ogni immagine e chiama `savePixels` per copiare i dati dei pixel in un nuovo frame del TIFF.  
```java
import java.io.File;
import java.io.FilenameFilter;
import com.aspose.imaging.fileformats.tiff.TiffFrame;

File di = new File(dataDir);
String[] files = di.list(new FilenameFilter() {
    @Override
    public boolean accept(File dir, String name) {
        return name.endsWith(".img");
    }
});

if (files != null) {
    int index = 0;
    for (String file : files) {
        try (Image inputImage = Image.load(dataDir + "/" + file)) {
            if (index > 0) {
                TiffFrame newframe = new TiffFrame(tiffOptions, width, height);
                tiffImage.addFrame(newframe);
            }
            TiffFrame frame = tiffImage.getFrames()[index];
            frame.savePixels(frame.getBounds(), ((RasterImage) inputImage).loadPixels(inputImage.getBounds()));
            index += 1;
        }
    }
}
```

## Salvataggio dell'immagine TIFF multipagina

**Panoramica:**  
Infine, salva il tuo file TIFF multipagina per preservare tutte le modifiche apportate durante l'elaborazione.

#### Passo 1: salvare il lavoro
`image.save` scrive il TIFF multipagina completo nel percorso di output specificato in `TiffOptions`. Verifica che la directory sia scrivibile per evitare `IOException`.  
```java
import com.aspose.imaging.examples.Utils;

tiffImage.save("YOUR_OUTPUT_DIRECTORY/output.tiff");
```

## Applicazioni pratiche

Comprendere come **convertire le immagini in TIFF** usando Aspose.Imaging per Java può essere utile in diversi scenari reali:

1. **Progetti di archiviazione:** Conserva centinaia di pagine scansionate in un unico file, riducendo il disordine del filesystem e semplificando le strategie di backup.  
2. **Imaging medico:** Combina fette di TC, RM o raggi X in un unico TIFF multipagina per facilitare il trasferimento tra sistemi.  
3. **Gestione documenti:** Mantieni PDF versionati, contratti scansionati o fatture insieme, consentendo un recupero e una stampa più rapidi.

Le possibilità di integrazione includono il collegamento di questa funzionalità a soluzioni di storage cloud come AWS S3 o Azure Blob Storage, abilitando pipeline di archiviazione automatizzate.

## Considerazioni sulle prestazioni

Quando si lavora con librerie di elaborazione immagini in Java:

- **Ridimensiona prima di aggiungere i frame** – riduce l'uso di memoria fino al 60 % per scansioni ad alta risoluzione.  
- **Usa le API di streaming** – Aspose.Imaging può elaborare le immagini a blocchi, utile quando si gestiscono TIFF con più di 500 pagine.  
- **Rilascia rapidamente gli oggetti Image** – avvolgi l'uso in `try (Image img = Image.load(...)) { … }` per liberare automaticamente le risorse native.

## Perché usare Aspose.Imaging per Java?

Aspose.Imaging supporta **50+** formati di input e output, inclusi PNG, JPEG, BMP, GIF e TIFF, e può elaborare file TIFF con centinaia di pagine senza caricare l'intero documento in memoria. I benchmark mostrano una riduzione del 30 % dell'uso CPU rispetto a Java ImageIO nativo quando si gestiscono grandi lotti.

## Domande frequenti

**D: Posso convertire file PNG o JPEG in un TIFF multipagina con questo approccio?**  
R: Assolutamente. Carica qualsiasi formato raster supportato (PNG, JPEG, BMP, ecc.) e aggiungi ciascuno come frame usando lo stesso flusso di lavoro.

**D: È possibile impostare la compressione (ad es., LZW) per il TIFF di output?**  
R: Sì. Chiama `tiffOptions.setCompression(TiffCompression.Lzw)` prima di creare l'immagine per ridurre le dimensioni del file mantenendo la qualità.

**D: Come aggiungere metadati (autore, descrizione) a ciascun frame del TIFF?**  
R: Usa `frame.getMetadata().addProperty("Author", "Your Name")` dopo aver creato il frame e prima del salvataggio.

**D: Aspose.Imaging supporta la lettura di TIFF multipagina esistenti?**  
R: Sì. Carica il file con `Image.load("existing.tiff")` e itera attraverso `((TiffImage)image).getFrames()` per accedere a ogni pagina.

**D: Cosa fare se devo elaborare migliaia di pagine?**  
R: Elabora le pagine in batch, chiama `System.gc()` periodicamente e utilizza il pattern try‑with‑resources per rilasciare la memoria nativa tempestivamente.

## Risorse

- [Documentazione Aspose.Imaging per Java](/reference/imaging/java/)
- [Scarica l'ultima versione](/imaging/java/)
- [Opzioni di licenza acquisto](/purchase/buy)
- [Acquisto Aspose](/purchase/buy)
- [Inizia con una prova gratuita](/imaging/java/)
- [Informazioni sulla licenza temporanea](/purchase/temporary-license/)
- [Supporto e forum della community](/forum/imaging/14)

**Last Updated:** 2026-11-16  
**Tested With:** Aspose.Imaging for Java 25.5  
**Author:** Aspose

```java
// Example: load and save a TIFF
Image img = Image.load("input.png");
img.save("output.tiff");
```

## Tutorial correlati

- [Converti TIFF multi-frame in JPEG con Aspose.Imaging per Java - Guida completa](/imaging/java/image-loading-saving/convert-multi-frame-tiff-to-jpeg-aspose-imaging-java/)
- [Dividi i frame TIFF multipagina con Aspose.Imaging per Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)
- [aspose imaging java – Converti TIFF in frame BMP](/imaging/java/animation-multi-frame-images/extract-tiff-frames-to-bmp-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}