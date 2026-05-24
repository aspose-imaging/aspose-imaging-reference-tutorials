---
date: 2026-01-04
description: Scopri come suddividere i fotogrammi TIFF multipagina usando Aspose.Imaging
  per Java. Questa guida passo‑passo copre i prerequisiti, un esempio di codice e
  le FAQ per gli sviluppatori.
linktitle: TIFF Image Frame Splitting
second_title: Aspose.Imaging Java Image Processing API
title: Dividi i fotogrammi TIFF multi-pagina con Aspose.Imaging per Java
url: /it/java/image-conversion-and-optimization/tiff-image-frame-splitting/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Dividi i fotogrammi TIFF multi‑pagina con Aspose.Imaging per Java

## Introduzione

In questo tutorial imparerai **come dividere i fotogrammi TIFF multi‑pagina** usando Aspose.Imaging per Java. Che tu stia creando un **tutorial di elaborazione immagini Java**, estraendo pagine individuali da un documento scansionato, o semplicemente abbia bisogno di **estrarre fotogrammi da file TIFF**, questa guida ti accompagna passo dopo passo. Inizieremo con i requisiti, importeremo i pacchetti necessari e poi approfondiremo un esempio completo e funzionante che mostra esattamente come dividere i file TIFF multi‑pagina nei tuoi progetti Java.

## Risposte rapide
- **Qual è l'obiettivo principale?** Dividere i fotogrammi TIFF multi‑pagina in file TIFF separati.  
- **Quale libreria viene utilizzata?** Aspose.Imaging per Java.  
- **È necessaria una licenza?** È disponibile una versione di prova; per la produzione è richiesta una licenza commerciale.  
- **Quale versione di Java è necessaria?** JDK 8 o superiore.  
- **Quante righe di codice?** Meno di 30 righe per la logica di divisione principale.

## Prerequisiti

Prima di intraprendere il nostro percorso con Aspose.Imaging per Java, assicurati di avere quanto segue:

### Ambiente di sviluppo Java
Un JDK recente (8 o successivo) installato sulla tua macchina. Puoi scaricarlo dal sito di Oracle se non lo possiedi già.

### Aspose.Imaging per Java
La libreria Aspose.Imaging per Java. Puoi ottenerla dalla pagina della [documentazione di Aspose.Imaging per Java](https://reference.aspose.com/imaging/java/).

### Immagine TIFF di esempio
Un file TIFF multi‑pagina su cui sperimentare. Usa la tua immagine o scaricane una per i test.

## Importa i pacchetti

Ora che i prerequisiti sono pronti, importa le classi necessarie nel tuo progetto Java.

### Passo 1: Scarica il JAR di Aspose.Imaging

Visita la [pagina di download di Aspose.Imaging per Java](https://releases.aspose.com/imaging/java/) per ottenere l'ultima versione del JAR.

### Passo 2: Aggiungi il JAR al tuo progetto

Aggiungi il JAR scaricato al percorso di compilazione del tuo progetto (IDE → Struttura progetto → Librerie).

### Passo 3: Importa le classi richieste

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.imageoptions.TiffOptions;
```

## Come dividere i fotogrammi TIFF multi‑pagina

Di seguito trovi il codice completo, passo dopo passo, che dimostra **come dividere i file TIFF** in pagine individuali.

### Passo 1: Inizializza il progetto
Assicurati che il tuo progetto includa il JAR di Aspose.Imaging e gli import mostrati sopra.

### Passo 2: Carica l'immagine TIFF
```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Create an instance of TiffImage and load the file from disc
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

Sostituisci `"Your Document Directory"` con la cartella reale che contiene il tuo file TIFF e `"SampleTiff1.tiff"` con il nome del file da elaborare.

### Passo 3: Dividi e salva i fotogrammi
```java
    // Initialize a variable to keep track of the frames in the image
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.tiff", new TiffOptions(TiffExpectedFormat.TiffJpegRgb));
        i++;
    }
}
```

Questo ciclo **estrae i fotogrammi da TIFF** e salva ciascuno come un file TIFF separato (`0_out.tiff`, `1_out.tiff`, …). Modifica lo schema di denominazione o il formato di output secondo le esigenze del tuo flusso di lavoro **java split tiff files**.

## Problemi comuni e suggerimenti

- **Errori di percorso file:** Usa percorsi assoluti o verifica che la directory di lavoro sia impostata correttamente.  
- **Consumo di memoria:** I TIFF multi‑pagina di grandi dimensioni possono richiedere molta memoria; considera di elaborare un fotogramma alla volta come mostrato.  
- **Formato di output:** `TiffOptions` ti permette di scegliere il tipo di compressione; `TiffJpegRgb` funziona bene nella maggior parte dei casi.

## Conclusione

Aspose.Imaging per Java rende semplice **dividere i file TIFF multi‑pagina**, trasformando un documento complesso a più fotogrammi in immagini individuali e gestibili. Con i prerequisiti e gli snippet di codice sopra, ora disponi di una solida base per qualsiasi **tutorial di elaborazione immagini Java** che coinvolga la manipolazione di TIFF. Sentiti libero di sperimentare con diversi `TiffOptions` o di integrare questa logica in pipeline di elaborazione batch più ampie.

## Domande frequenti

**D1: Dove posso scaricare Aspose.Imaging per Java?**  
R1: Puoi scaricare Aspose.Imaging per Java dalla [pagina di download](https://releases.aspose.com/imaging/java/).

**D2: Aspose.Imaging per Java è gratuito?**  
R2: Aspose.Imaging per Java è una libreria commerciale. Puoi consultare i prezzi e le opzioni di licenza nella [pagina di acquisto](https://purchase.aspose.com/buy).

**D3: Posso provare Aspose.Imaging per Java prima di acquistarlo?**  
R3: Sì, è disponibile una versione di prova gratuita di Aspose.Imaging per Java dalla [pagina di download della prova](https://releases.aspose.com/).

**D4: Dove posso trovare supporto e discussioni della community relative a Aspose.Imaging per Java?**  
R4: Puoi visitare il [forum di Aspose.Imaging per Java](https://forum.aspose.com/) per supporto e discussioni.

**D5: Aspose.Imaging per Java supporta altri formati immagine oltre a TIFF?**  
R5: Sì, Aspose.Imaging per Java supporta una vasta gamma di formati immagine, tra cui JPEG, PNG, BMP e molti altri.

---

**Ultimo aggiornamento:** 2026-01-04  
**Testato con:** Aspose.Imaging per Java 24.12 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}