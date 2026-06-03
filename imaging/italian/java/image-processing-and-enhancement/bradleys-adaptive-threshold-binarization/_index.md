---
date: 2026-01-09
description: Scopri come binarizzare un'immagine usando Aspose.Imaging per Java. Questa
  guida copre le tecniche di elaborazione delle immagini in Java per la conversione
  da DICOM a BMP.
linktitle: Bradley's Adaptive Threshold Binarization
second_title: Aspose.Imaging Java Image Processing API
title: Come binarizzare un'immagine con Aspose.Imaging per Java
url: /it/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Come binarizzare un'immagine con Aspose.Imaging per Java

Le immagini svolgono un ruolo cruciale nel mondo digitale, sia sui siti web, nei documenti o come parte di varie applicazioni. Se ti stai chiedendo **come binarizzare un'immagine** in modo efficiente, soprattutto per formati medici come DICOM, sei nel posto giusto. La binarizzazione delle immagini semplifica una foto convertendola in una rappresentazione in bianco‑e‑nero, ideale per analisi successive, OCR o ottimizzazione dello spazio di archiviazione. In questo tutorial percorreremo l’intero processo usando la binarizzazione a soglia adattiva di Bradley di Aspose.Imaging per Java.

## Risposte rapide
- **Cosa fa la binarizzazione?** Converte ogni pixel in nero o bianco in base a una soglia.
- **Quale libreria è la migliore per l'elaborazione di immagini Java?** Aspose.Imaging per Java offre funzionalità robuste con una versione di prova gratuita.
- **Posso elaborare file DICOM direttamente?** Sì, Aspose.Imaging può caricare DICOM e generare BMP, PNG, ecc.
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale per l'uso non‑di prova.
- **Quale versione di Java è supportata?** Java 8 e versioni successive sono pienamente compatibili.

## Cos'è la binarizzazione delle immagini?
La binarizzazione delle immagini è il processo di trasformare un'immagine in scala di grigi o a colori in un'immagine binaria in cui ogni pixel è 0 (nero) o 255 (bianco). Questo passaggio è spesso la prima fase nei flussi di lavoro di elaborazione di immagini mediche, scansione di documenti e compiti di visione artificiale.

## Perché usare Aspose.Imaging per Java?
Aspose.Imaging offre un'API pure‑Java che **carica DICOM**, applica algoritmi avanzati come **Bradley’s Adaptive Threshold** e salva il risultato in formati comuni senza necessità di librerie native esterne. È ideale per **l'elaborazione di immagini mediche**, **convertire DICOM in BMP** e altri flussi di lavoro basati su Java.

## Prerequisiti

Prima di immergerti nel codice, assicurati di avere quanto segue:

- **Ambiente di sviluppo Java** – JDK 8 o versioni successive installate.
- **Aspose.Imaging per Java** – Scaricalo dal sito ufficiale: [Download Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/).
- **Un'immagine DICOM** – Qualsiasi file DICOM di esempio che desideri binarizzare.

Ora che tutto è pronto, passiamo all'implementazione.

## Come binarizzare un'immagine – Guida passo‑passo

### Importare i pacchetti
Per prima cosa, importa le classi Aspose.Imaging necessarie. Questo snippet definisce anche i percorsi dei file di input e output.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// Load a DICOM image in an instance of DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Binarize image with Bradley's adaptive threshold.
    image.binarizeBradley(10);
    // Save the resultant image.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

### Passo 1: Definire i percorsi
Imposta le posizioni per il tuo file DICOM di origine e il file BMP di destinazione. Sostituisci `"Your Document Directory"` con la cartella reale sul tuo sistema.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

### Passo 2: Caricare l'immagine DICOM
Usa Aspose.Imaging per **caricare l'immagine DICOM** in un oggetto `DicomImage`. Questo oggetto ti dà pieno accesso ai dati dei pixel e ai metodi di elaborazione.

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // The image processing steps will go here.
}
```

### Passo 3: Eseguire la binarizzazione
Applica l'algoritmo di soglia adattiva di Bradley. Il parametro (`10` in questo esempio) controlla la sensibilità della soglia; puoi sperimentare con valori diversi per ottenere risultati ottimali.

```java
image.binarizeBradley(10);
```

### Passo 4: Salvare l'immagine binarizzata
Infine, esporta l'immagine elaborata. Qui usiamo il formato BMP, ma Aspose.Imaging supporta PNG, JPEG, TIFF e molti altri.

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## Problemi comuni e risoluzione

- **FileNotFoundException** – Assicurati che il percorso `dataDir` termini con una barra e che il nome del file DICOM corrisponda esattamente.
- **OutOfMemoryError** – File DICOM di grandi dimensioni potrebbero richiedere l'aumento della dimensione dell'heap JVM (`-Xmx2g` o superiore).
- **Soglia errata** – Se l'output appare troppo scuro o troppo chiaro, regola l'intero passato a `binarizeBradley()` (ad es. 5‑15).

## Domande frequenti

### Q1: Cos'è DICOM e perché è importante nell'imaging medico?
**A:** DICOM sta per Digital Imaging and Communications in Medicine. È lo standard universale per memorizzare, trasmettere e gestire immagini mediche, consentendo l'interoperabilità tra dispositivi e sistemi.

### Q2: Posso usare Aspose.Imaging per Java nei miei progetti commerciali?
**A:** Sì, Aspose.Imaging per Java offre sia versioni di prova gratuite sia licenze commerciali. Puoi esplorare le opzioni e ottenere la licenza necessaria dal [sito di Aspose](https://purchase.aspose.com/buy).

### Q3: Esistono licenze temporanee disponibili per scopi di test?
**A:** Sì, è possibile ottenere una licenza temporanea per testare e valutare Aspose.Imaging per Java. Visita [questo link](https://purchase.aspose.com/temporary-license/) per maggiori informazioni.

### Q4: Dove posso chiedere aiuto o discutere problemi relativi a Aspose.Imaging per Java?
**A:** Per supporto comunitario e discussioni, puoi visitare il [forum Aspose.Imaging](https://forum.aspose.com/). È un ottimo posto per trovare risposte alle tue domande e connetterti con altri utenti.

### Q5: Aspose.Imaging per Java è adatto all'elaborazione di immagini in altre applicazioni basate su Java?
**A:** Assolutamente sì. La libreria funziona bene in applicazioni web, software desktop, strumenti di elaborazione batch e altro, fornendo un'API coerente su tutte le piattaforme.

## Conclusione
Ora sai **come binarizzare un'immagine** usando Aspose.Imaging per Java con la soglia adattiva di Bradley. Questa tecnica è particolarmente utile per **l'elaborazione di immagini mediche**, consentendoti di convertire file DICOM in formati BMP leggeri (o altri) per analisi o archiviazione. Continua a sperimentare con soglie diverse e scopri le altre potenti funzionalità di Aspose.Imaging.

Per approfondimenti sulla manipolazione delle immagini, consulta la documentazione ufficiale: [Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/).

---

**Last Updated:** 2026-01-09  
**Tested With:** Aspose.Imaging per Java 24.12 (ultima versione al momento della stesura)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}