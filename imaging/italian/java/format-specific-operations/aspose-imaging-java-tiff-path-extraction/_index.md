---
date: '2026-09-02'
description: Scopri come creare un percorso di ritaglio ed estrarlo dalle immagini
  TIFF usando Aspose.Imaging for Java. Segui le istruzioni passo‑passo per convertire
  TIFF in PSD in modo efficiente.
keywords:
- create clipping path
- how to extract path
- how to convert tiff
- aspose imaging java
- convert tiff to psd
lastmod: '2026-09-02'
og_description: Scopri come creare un percorso di ritaglio ed estrarlo dalle immagini
  TIFF usando Aspose.Imaging for Java. Segui il codice passo‑passo per convertire
  TIFF in PSD.
og_image_alt: Guide showing how to create clipping path in TIFF using Aspose.Imaging
  Java
og_title: Crea percorso di ritaglio in TIFF con Aspose.Imaging for Java
schemas:
- author: Aspose
  dateModified: '2026-09-02'
  description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  headline: Create clipping path in TIFF with Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  name: Create clipping path in TIFF with Aspose.Imaging for Java
  steps:
  - name: '**Free trial** – start with a 30‑day trial.'
    text: '**Free trial** – start with a 30‑day trial.'
  - name: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
    text: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
  - name: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
    text: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
  - name: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
    text: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
  - name: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
    text: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
  type: HowTo
- questions:
  - answer: Yes, provided you have a valid commercial license; a free trial is available
      for evaluation.
    question: Can I use Aspose.Imaging for Java in a commercial application?
  - answer: The library supports over 100 formats, including TIFF, PSD, BMP, JPEG,
      PNG, and many more.
    question: What image formats does Aspose.Imaging support?
  - answer: Verify that the source TIFF actually contains vector path resources; use
      the `hasPathResources()` check before extraction.
    question: How do I troubleshoot path extraction errors?
  - answer: Absolutely – combine the extraction code with Java’s parallel streams
      or an executor service to handle many files efficiently.
    question: Is batch processing of multiple TIFFs possible?
  - answer: Complex shapes may need manual adjustment after creation; the API handles
      standard Bezier curves and straight lines reliably.
    question: Are there limitations when creating clipping paths in TIFF?
  type: FAQPage
tags:
- create clipping path
- TIFF processing
- Aspose.Imaging
- Java image manipulation
- PSD conversion
title: Crea percorso di ritaglio in TIFF con Aspose.Imaging for Java
url: /it/java/format-specific-operations/aspose-imaging-java-tiff-path-extraction/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crea percorso di ritaglio in TIFF con Aspose.Imaging per Java

In questa guida completa imparerai **come creare un percorso di ritaglio** in un file TIFF e come estrarre percorsi esistenti usando Aspose.Imaging per Java. Alla fine, sarai in grado di convertire immagini TIFF in file PSD completamente modificabili, pronti per Photoshop o qualsiasi editor vettoriale.

## Risposte rapide
- **Che cos'è un percorso di ritaglio?** Un contorno vettoriale che definisce le regioni trasparenti e opache di un'immagine.  
- **Posso estrarre un percorso esistente da un TIFF?** Sì – Aspose.Imaging può leggere le risorse di percorso incorporate e salvarle come PSD.  
- **Come aggiungo un nuovo percorso di ritaglio?** Crea un `PathResource`, popolalo con record vettoriali e assegnalo al frame attivo dell'immagine.  
- **È necessaria una licenza per l'uso in produzione?** È richiesta una licenza valida di Aspose.Imaging per le distribuzioni commerciali.  
- **Quale versione di Java è necessaria?** JDK 8 o superiore; la libreria funziona con Java 11, 17 e versioni successive.

## Che cos'è un percorso di ritaglio?
Un percorso di ritaglio è un contorno basato su vettori che indica ai motori di rendering quali parti di un'immagine mostrare o nascondere. È memorizzato come risorsa di percorso all'interno di file TIFF o PSD e può essere modificato in Adobe Photoshop.

## Perché convertire TIFF in PSD?
Convertire TIFF in PSD consente una modifica senza perdita di livelli, maschere e percorsi di ritaglio. Aspose.Imaging supporta **oltre 50 formati di input e output** e può elaborare TIFF con centinaia di pagine senza caricare l'intero file in memoria, garantendo alte prestazioni nella conversione batch.

## Prerequisiti
- **Java Development Kit (JDK)** 8 o più recente installato.  
- Libreria **Aspose.Imaging per Java** (aggiungi tramite Maven, Gradle o download diretto).  
- Familiarità di base con i concetti di programmazione Java.

## Come configurare Aspose.Imaging per Java
Prima di aggiungere codice, assicurati che la libreria sia correttamente referenziata nel tuo sistema di build e che disponi di un file di licenza valido. Questo garantisce che l'API funzioni senza restrizioni di valutazione e che tutte le funzionalità, inclusa la manipolazione dei percorsi, siano disponibili.

### Maven
Aggiungi la seguente dipendenza al tuo file `pom.xml`:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle
Inserisci questa riga nel tuo file `build.gradle`:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Download diretto
Scarica l'ultima versione da [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

#### Acquisizione della licenza
1. **Prova gratuita** – inizia con una prova di 30 giorni.  
2. **Licenza temporanea** – ottieni una dalla [pagina della licenza temporanea](https://purchase.aspose.com/temporary-license/).  
3. **Acquisto** – acquista una licenza completa su [sito di Aspose](https://purchase.aspose.com/buy).

Una volta installato e licenziato, inizializza Aspose.Imaging nel tuo progetto:
```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path_to_license_file");
```

## Come estrarre il percorso di ritaglio da un TIFF?
L'estrazione di un percorso di ritaglio prevede il caricamento del TIFF, l'individuazione di eventuali risorse di percorso incorporate e la scrittura di tali risorse in un nuovo file PSD. Il processo legge i dati vettoriali direttamente dall'immagine sorgente, preservando la precisione e evitando conversioni raster.

Carica il TIFF, itera attraverso le sue risorse di percorso e salva il risultato come PSD. Questa operazione legge i dati vettoriali incorporati e li scrive in un nuovo file in un unico passaggio.
```java
String filePath = "YOUR_DOCUMENT_DIRECTORY/SupportExtractingPathsFromTiff/Sample.tif";
try (TiffImage image = (TiffImage) com.aspose.imaging.Image.load(filePath)) {
    // Proceed with extraction steps...
}
```

Itera attraverso le risorse di percorso nel frame attivo e raccoglile:
```java
for (PathResource path : image.getActiveFrame().getPathResources()) {
    System.out.println(path.getName());  // Output the name of each path resource found.
}
```

Salva l'immagine con i percorsi estratti in un nuovo file PSD:
```java
String outFilePath = "YOUR_OUTPUT_DIRECTORY/SampleWithPaths.psd";
image.save(outFilePath);
```

## Come creare un percorso di ritaglio in TIFF?
Creare un percorso di ritaglio richiede la costruzione di un `PathResource` che descriva il contorno vettoriale desiderato, il suo collegamento al frame attivo del TIFF e quindi il salvataggio dell'immagine (o di una copia) come PSD affinché il percorso venga conservato. Questo approccio consente di aggiungere programmaticamente maschere vettoriali a file raster.

`PathResource` rappresenta un percorso vettoriale memorizzato all'interno di un file immagine.  
Inizializza un nuovo `PathResource` con gli attributi richiesti:
```java
final PathResource pathResource = new PathResource();
pathResource.setBlockId((short) 2000); // Set Block ID per Photoshop specs
pathResource.setName("My Clipping Path"); // Name your clipping path for easy identification

// Create and add vector path records using the provided coordinates.
pathResource.setRecords(createRecords(0.2f, 0.2f, 0.8f, 0.2f, 0.8f, 0.8f, 0.2f, 0.8f));
```

Assegna la risorsa di percorso creata al frame attivo dell'immagine:
```java
List<PathResource> list = new LinkedList<>();
list.add(pathResource);
image.getActiveFrame().setPathResources(list);
```

Salva il TIFF modificato come PSD che ora contiene il percorso di ritaglio:
```java
String outFilePath2 = "YOUR_OUTPUT_DIRECTORY/ImageWithPath.psd";
image.save(outFilePath2);
```

## Metodi di supporto

### Creare record
Genera record di percorso vettoriale usando nodi Bezier e record di lunghezza:
```java
private static List<VectorPathRecord> createRecords(float ... coordinates) {
    List<VectorPathRecord> records = createBezierRecords(coordinates); 
    LengthRecord lr = new LengthRecord();
    lr.setOpen(false);
    lr.setRecordCount(records.size());
    
    records.add(0, lr);
    return records;
}
```

### Creare record Bezier
Converti array di coordinate in record di percorso vettoriale Bezier:
```java
private static List<VectorPathRecord> createBezierRecords(float[] coordinates) {
    final List<VectorPathRecord> list = new LinkedList<>();
    
    for (int index = 0; index < coordinates.length - 1; index += 2) {
        PointF point = new PointF(coordinates[index], coordinates[index + 1]);
        list.add(createBezierRecord(point));
    }
    
    return list;
}
```

### Creare record Bezier singolo
Definisci un singolo record di percorso vettoriale Bezier knot:
```java
private static VectorPathRecord createBezierRecord(PointF point) {
    BezierKnotRecord it = new BezierKnotRecord();
    it.setPathPoints(new PointF[] { point, point, point });
    return it;
}
```

## Applicazioni pratiche
1. **Flussi di lavoro di graphic design** – Converti TIFF in PSD per modificare livelli e maschere in Photoshop.  
2. **Pipeline di immagini automatizzate** – Elabora in batch migliaia di TIFF, estraendo o aggiungendo percorsi al volo.  
3. **Visualizzazioni basate sui dati** – Usa percorsi vettoriali per generare grafici o schemi precisi da sorgenti raster.

## Considerazioni sulle prestazioni
- **Gestione della memoria** – Usa try‑with‑resources per garantire che gli oggetti immagine vengano rilasciati prontamente.  
- **Elaborazione batch** – Parallelizza le conversioni con `ForkJoinPool` di Java per insiemi di immagini di grandi dimensioni.  
- **Gestione della risoluzione** – Regola DPI solo quando necessario per mantenere basso il tempo di elaborazione preservando la qualità.

## Conclusione
Ora sai **come creare un percorso di ritaglio** nei file TIFF e come estrarre percorsi esistenti usando Aspose.Imaging per Java. Queste tecniche ti permettono di integrare una sofisticata manipolazione delle immagini in qualsiasi flusso di lavoro basato su Java, dalle utility desktop alle pipeline di elaborazione di livello enterprise.

### Prossimi passi
- Sperimenta con forme vettoriali e attributi di percorso diversi.  
- Esplora ulteriori funzionalità di Aspose.Imaging come watermarking, conversione di formati e gestione dei metadati.

## Domande frequenti

**D: Posso usare Aspose.Imaging per Java in un'applicazione commerciale?**  
R: Sì, a condizione di possedere una licenza commerciale valida; è disponibile una prova gratuita per la valutazione.

**D: Quali formati di immagine supporta Aspose.Imaging?**  
R: La libreria supporta oltre 100 formati, inclusi TIFF, PSD, BMP, JPEG, PNG e molti altri.

**D: Come risolvere gli errori di estrazione del percorso?**  
R: Verifica che il TIFF di origine contenga effettivamente risorse di percorso vettoriale; utilizza il controllo `hasPathResources()` prima dell'estrazione.

**D: È possibile elaborare in batch più TIFF?**  
R: Assolutamente – combina il codice di estrazione con gli stream paralleli di Java o un executor service per gestire efficientemente molti file.

**D: Ci sono limitazioni nella creazione di percorsi di ritaglio in TIFF?**  
R: Forme complesse potrebbero richiedere aggiustamenti manuali dopo la creazione; l'API gestisce in modo affidabile curve Bezier standard e linee rette.

---

**Ultimo aggiornamento:** 2026-09-02  
**Testato con:** Aspose.Imaging per Java 24.12  
**Autore:** Aspose  

## Risorse

- [Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)
- [Download Aspose.Imaging per Java](https://releases.aspose.com/imaging/java/)
- [Acquista licenza](https://purchase.aspose.com/buy)
- [Prova gratuita](https://releases.aspose.com/imaging/java/)
- [Licenza temporanea](https://purchase.aspose.com/temporary-license/)
- [Forum di supporto Aspose](https://forum.aspose.com/c/imaging/14)

## Tutorial correlati

- [Converti immagine in PSD con Aspose.Imaging per Java – Guida passo‑passo](/imaging/java/format-conversion-export/convert-images-to-psd-using-aspose-imaging-java-guide/)
- [Come convertire TIFF in GraphicsPath con Aspose.Imaging Java](/imaging/java/advanced-drawing-graphics/aspose-imaging-java-tiff-graphicspath-conversion/)
- [Caricamento e salvataggio efficienti di immagini TIFF in Java con Aspose.Imaging](/imaging/java/image-loading-saving/aspose-imaging-java-tiff-image-saving/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}