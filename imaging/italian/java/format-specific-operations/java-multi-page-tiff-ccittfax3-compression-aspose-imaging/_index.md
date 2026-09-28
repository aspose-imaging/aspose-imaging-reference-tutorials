---
date: '2026-09-28'
description: Scopri come utilizzare la compressione ccittfax3 java per creare file
  TIFF multipagina con Aspose.Imaging. Scansiona, archivia e riduci efficientemente
  le dimensioni dei file per i flussi di lavoro dei documenti.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Scopri passo a passo come utilizzare la compressione ccittfax3 java
  con Aspose.Imaging per creare file TIFF multipagina efficienti per la scansione
  e l'archiviazione.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: Come creare un TIFF multipagina con compressione ccittfax3 java
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
title: Come creare un TIFF multipagina con compressione ccittfax3 java
url: /it/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Padroneggiare la creazione di TIFF multi-pagina con compressione ccittfax3 java usando Aspose.Imaging

## Introduzione

Se hai bisogno di archiviare grandi volumi di documenti scansionati mantenendo le dimensioni dei file ridotte, **ccittfax3 compression java** è la soluzione ideale. Questo tutorial ti mostra come generare file TIFF multi‑pagina con compressione CCITTFAX3 in Java usando Aspose.Imaging. Imparerai perché questa compressione funziona così bene per le scansioni monocromatiche, come configurare la libreria e come aggiungere ogni pagina come frame.

**Cosa imparerai**
- Come aggiungere Aspose.Imaging a un progetto Java.
- Come configurare `TiffOptions` per la compressione CCITTFAX3.
- Come creare un `TiffImage`, ridimensionare le immagini di origine e aggiungerle come frame.
- Come salvare efficientemente il TIFF multi‑pagina finale.

Procediamo passo passo attraverso l'implementazione completa.

## Risposte rapide
- **Qual è il principale vantaggio della compressione CCITTFAX3?** Fino all'80 % di riduzione della dimensione del file per scansioni in bianco‑nero.  
- **Quale libreria fornisce supporto integrato?** Aspose.Imaging per Java, versione 25.5+.  
- **Ho bisogno di una licenza per lo sviluppo?** Una licenza di prova gratuita funziona per tutte le funzionalità; è necessaria una licenza a pagamento per la produzione.  
- **Posso elaborare centinaia di pagine?** Sì—Aspose.Imaging trasmette le pagine, quindi l'uso della memoria rimane basso.  
- **Il codice è compatibile con Java 11 e versioni successive?** Assolutamente; l'API è destinata a Java 8+.

## Cos'è la compressione ccittfax3 java?
`CCITTFAX3` è un algoritmo di compressione lossless e monocromatico progettato per fax e immagini di documenti scansionati. Codifica ogni pixel come un singolo bit, fornendo output ad alta qualità riducendo drasticamente le dimensioni del file—spesso del 70‑80 % rispetto a un TIFF non compresso. Questo lo rende ideale per l'archiviazione di documenti in bianco‑nero dove è necessario preservare la fedeltà.

## Perché usare Aspose.Imaging per questo compito?
Aspose.Imaging supporta **oltre 100** formati di input e output, inclusi PDF, PNG, JPEG e TIFF. La sua architettura di streaming può gestire file TIFF **con centinaia di pagine** senza caricare l'intero documento in memoria, rendendolo ideale per progetti di archiviazione su larga scala.

## Prerequisiti

- **Java Development Kit (JDK)** 8 o versioni successive installato.
- **IDE** come IntelliJ IDEA o Eclipse.
- **Maven** o **Gradle** per la gestione delle dipendenze.
- Conoscenze di base di Java (classi, oggetti, collezioni).

## Configurare Aspose.Imaging per Java

Aggiungi la libreria al tuo file di build.

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

### Download diretto

Puoi anche scaricare l'ultimo JAR da [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### Acquisizione della licenza

Una licenza di prova gratuita è disponibile su [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/). Per l'uso in produzione, acquista una licenza permanente o richiedi una temporanea su [Aspose Purchase](https://purchase.aspose.com/temporary-license/).

Per un utilizzo dettagliato dell'API, consulta la [documentazione](https://reference.aspose.com/imaging/java/) di Aspose.Imaging per Java.

### Inizializzazione di base

Dopo aver aggiunto la dipendenza, inizializza la libreria come mostrato di seguito.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## Come configurare la compressione ccittfax3 java per un TIFF multi‑pagina?

`TiffOptions` è una classe che definisce il formato di output e le impostazioni di compressione per un file TIFF. Carica l'oggetto `TiffOptions` con l'enumerazione `CCITTGroup3FaxCompression`, quindi imposta la sorgente del file di output. Questa configurazione a due passaggi prepara lo scrittore per la compressione monocromatica e garantisce che ogni pagina aggiunta successivamente venga codificata usando l'algoritmo CCITTFAX3, ottenendo una riduzione significativa delle dimensioni mantenendo la qualità dell'immagine.

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

## Come creare un'istanza di TiffImage in Java?

`TiffImage` rappresenta un documento TIFF multi‑pagina in memoria e fornisce metodi per manipolare i suoi frame. Prima, definisci la larghezza e l'altezza che tutte le pagine condivideranno. Poi istanzia `TiffImage` usando i `TiffOptions` creati in precedenza. L'oggetto `TiffImage` funge da contenitore per i singoli frame, permettendoti di aggiungere, rimuovere o riordinare le pagine prima di salvare il file finale.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## Come caricare e ridimensionare le immagini di origine da una cartella?

Filtra la directory di destinazione per i file JPEG, leggi ogni immagine e ridimensionala per corrispondere al canvas TIFF. Ridimensionare prima di aggiungere i frame riduce il consumo di memoria e velocizza l'operazione di salvataggio. Convertendo ogni immagine di origine alle dimensioni e al formato pixel richiesti, garantisci un layout di pagina coerente ed eviti errori di runtime quando i frame vengono aggiunti al documento TIFF.

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

## Come aggiungere ogni immagine come frame al TIFF multi‑pagina?

`TiffFrame` è un oggetto che contiene l'immagine di una singola pagina e i relativi metadati all'interno di un TIFF. Itera sulle immagini ridimensionate, crea un nuovo `TiffFrame` e aggiungilo al `TiffImage`. Ogni frame diventa una pagina separata nel documento finale, e la libreria gestisce automaticamente gli aggiornamenti dei metadati necessari, come il conteggio delle pagine e gli offset, garantendo una struttura TIFF multi‑pagina valida.

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

## Come salvare il file TIFF multi‑pagina finale?

Chiama il metodo `save` sull'istanza `TiffImage`, passando il percorso di output desiderato. La libreria scrive automaticamente tutti i frame usando la compressione CCITTFAX3, trasmette i dati su disco in modo efficiente e chiude le risorse sottostanti. Dopo il completamento dell'operazione di salvataggio, il file risultante contiene tutte le pagine con la compressione specificata, pronto per la distribuzione o l'archiviazione.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## Applicazioni pratiche

- **Archiviazione di documenti:** Conserva contratti, fatture o registri legali scansionati con un minimo ingombro di archiviazione.  
- **Imaging medico:** Comprimi le scansioni radiologiche mantenendo i dettagli diagnostici.  
- **Produzione di stampa:** Genera lavori di stampa multi‑pagina che le stampanti possono consumare direttamente.

## Considerazioni sulle prestazioni

- Usa `ResizeOptions` che preservano il rapporto d'aspetto per evitare distorsioni.  
- Chiudi ogni oggetto `Image` dopo aver aggiunto il suo frame per liberare la memoria nativa.  
- Per batch molto grandi, elabora i file in stream paralleli e scrivi ogni segmento TIFF in modo asincrono.

## Problemi comuni e risoluzione

- **Formato pixel errato:** CCITTFAX3 funziona solo con immagini a 1‑bit (bianco‑nero). Converti le immagini a colori in scala di grigi prima del ridimensionamento.  
- **Perdite di memoria:** Chiama sempre `dispose()` sugli oggetti `Image` temporanei; altrimenti i buffer nativi rimangono allocati.  
- **Dimensione del file non ridotta:** Assicurati che la proprietà di compressione di `TiffOptions` sia impostata; altrimenti viene usata l'impostazione predefinita (nessuna compressione).

## Domande frequenti

**Q: Posso usare questo approccio con immagini a colori?**  
A: CCITTFAX3 è limitato ai dati monocromatici; per il colore usa la compressione JPEG o LZW.

**Q: Aspose.Imaging supporta lo streaming per TIFF enormi?**  
A: Sì—la libreria scrive ogni frame direttamente sullo stream di output, mantenendo basso l'uso della memoria anche per migliaia di pagine.

**Q: Come applicare una licenza temporanea programmaticamente?**  
A: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.

**Q: Esiste un modo per visualizzare l'anteprima del TIFF prima di salvarlo?**  
A: Puoi renderizzare ogni `TiffFrame` in un `BufferedImage` e visualizzarlo in un componente Swing.

**Q: Quali versioni di Java sono ufficialmente supportate?**  
A: Aspose.Imaging supporta Java 8 fino a Java 21, incluse le versioni LTS.

## Conclusione

Ora disponi di un flusso di lavoro completo e pronto per la produzione per creare file TIFF multi‑pagina con **ccittfax3 compression java** usando Aspose.Imaging. Seguendo i passaggi sopra, puoi archiviare in modo efficiente enormi collezioni di documenti mantenendo bassi i costi di archiviazione e alta la qualità delle immagini. Esplora ulteriori funzionalità di Aspose.Imaging—come OCR, gestione dei metadati e conversione di formato—per migliorare ulteriormente la tua pipeline di elaborazione dei documenti.

---

**Ultimo aggiornamento:** 2026-09-28  
**Testato con:** Aspose.Imaging 25.5 per Java  
**Autore:** Aspose

## Tutorial correlati

- [Come creare TIFF multi-pagina con Aspose.Imaging per Java – Guida completa](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Come ridurre le dimensioni dei file immagine con compressione LZW in Java](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Dividi i frame TIFF multi-pagina con Aspose.Imaging per Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}