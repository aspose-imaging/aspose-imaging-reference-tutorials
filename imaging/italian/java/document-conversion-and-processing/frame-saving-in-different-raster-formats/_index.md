---
date: 2026-04-28
description: Scopri come convertire i file TIFF in PNG e come convertire i file TIFF
  in altri formati raster utilizzando Aspose.Imaging per Java. Guida passo‑passo per
  la manipolazione delle immagini.
keywords:
- tiff to png java
- how to convert tiff
- Aspose.Imaging Java
linktitle: Salvataggio dei fotogrammi in diversi formati raster
second_title: Aspose.Imaging Java Image Processing API
title: tiff to png java – Converti TIFF in PNG e salva i fotogrammi in diversi formati
  raster
url: /it/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# tiff to png java – Converti TIFF in PNG e salva i fotogrammi in diversi formati raster

Lavorare con file TIFF multi‑pagina è uno scenario comune nelle applicazioni con grandi volumi di documenti. Se hai bisogno di **convert tiff to png**—o di estrarre fotogrammi individuali e archiviarli in altri formati raster—Aspose.Imaging for Java rende il processo semplice e performante. In questo tutorial vedremo passo dopo passo come caricare un TIFF, iterare i suoi fotogrammi e salvare ciascuno come PNG (puoi facilmente passare a BMP o GIF in seguito). Alla fine vedrai anche **how to convert tiff** in uno dei formati raster supportati con poche righe di codice.

## Risposte rapide
- **Cosa significa “convert tiff to png”?** Significa estrarre ogni pagina di un file TIFF e scriverla come immagine raster PNG.  
- **Quale libreria gestisce questo?** Aspose.Imaging for Java fornisce pieno supporto per l'estrazione dei fotogrammi TIFF e la conversione di formati raster.  
- **Ho bisogno di una licenza?** Una prova gratuita funziona per lo sviluppo; è necessaria una licenza completa per l'uso in produzione.  
- **Posso salvare in BMP o GIF invece di PNG?** Sì—basta sostituire `PngOptions` con `BmpOptions` o `GifOptions`.  
- **Quale versione di Java è richiesta?** Java 8 o superiore è consigliata.

## Cos'è “convert tiff to png”?
Convertire un TIFF in PNG comporta la decodifica del TIFF multi‑pagina, l'accesso a ciascun fotogramma e la codifica di quel fotogramma nel formato PNG, che è lossless, adatto al web e ampiamente supportato.

## Perché usare Aspose.Imaging per Java?
- **Ampio supporto di formati** – Gestisce TIFF, PNG, JPEG, BMP, GIF e molti altri.  
- **Nessuna dipendenza nativa** – Pure Java, facile da integrare in qualsiasi progetto JVM.  
- **Alte prestazioni** – Ottimizzato per immagini di grandi dimensioni e documenti multi‑pagina.  
- **API semplice** – Codice minimo necessario per eseguire conversioni complesse.

## Perché è importante
Molti sistemi legacy archiviano documenti scansionati come TIFF multi‑pagina perché il formato è adatto all'archiviazione a lungo termine. Le applicazioni web e mobile moderne, tuttavia, preferiscono PNG, BMP o GIF per una rapida visualizzazione e generazione di miniature. Convertire i fotogrammi TIFF al volo riduce i costi di archiviazione, migliora i tempi di caricamento e amplia la compatibilità tra browser e dispositivi.

## Prerequisiti

1. **Ambiente di sviluppo Java** – Assicurati che il JDK sia installato. Scaricalo dal [Oracle website](https://www.oracle.com/java/technologies/javase-downloads) se non lo hai già fatto.  
2. **Aspose.Imaging for Java Library** – Accedi al riferimento API nella [documentation](https://reference.aspose.com/imaging/java/). Ottieni la libreria dalla [download page](https://releases.aspose.com/imaging/java/). Una prova gratuita è disponibile [here](https://releases.aspose.com/), e una licenza completa può essere acquistata [here](https://purchase.aspose.com/buy).  
3. **Sample TIFF Image** – Preparati un TIFF multi‑pagina pronto per l'elaborazione.

Ora che i prerequisiti sono coperti, immergiamoci nel codice.

## Come convertire TIFF in PNG usando Aspose.Imaging per Java

### Importa i pacchetti
Prima, importa le classi necessarie di Aspose.Imaging.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

### Passo 1: Carica l'immagine TIFF
Inizializza la directory dei dati e carica il file TIFF sorgente.

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

### Passo 2: Salva i fotogrammi in diversi formati raster
Itera su ogni fotogramma e **save image as png**. Per **convert tiff to bmp** o eseguire una **tiff to gif conversion**, sostituisci semplicemente `PngOptions` con `BmpOptions` o `GifOptions`.

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **Consiglio professionale:** Mantieni il blocco `try‑with‑resources` come mostrato per garantire che il file TIFF venga correttamente rilasciato dopo l'elaborazione.

## Casi d'uso comuni
- **Archiviazione di documenti:** Converti documenti TIFF scansionati in PNG per l'anteprima web.  
- **Generazione di miniature:** Estrai il primo fotogramma di un TIFF e salvalo come una piccola miniatura PNG.  
- **Migrazione di formato:** Sposta le risorse TIFF legacy in formati moderni come BMP o GIF per la compatibilità con sistemi più vecchi.

## Risoluzione dei problemi e consigli
- **Fotogrammi mancanti:** Verifica che il TIFF sorgente contenga effettivamente più pagine; usa `multiImage.getFrames().size()` per il debug.  
- **Errori di out‑of‑memory:** Processa i TIFF di grandi dimensioni pagina per pagina come mostrato, invece di caricare l'intero file in memoria.  
- **Controllo qualità:** PNG è lossless; se ti servono file più piccoli, considera l'uso delle opzioni JPEG con impostazioni di qualità.

## Domande frequenti

**Q1: Quali sono i formati raster supportati per il salvataggio dei fotogrammi in Aspose.Imaging per Java?**  
A1: Aspose.Imaging for Java supporta un'ampia gamma di formati raster, tra cui PNG, JPEG, BMP, GIF e altri. Puoi scegliere il formato più adatto alle esigenze della tua applicazione.

**Q2: Posso eseguire altre operazioni di immagine usando Aspose.Imaging per Java?**  
A2: Sì, Aspose.Imaging for Java offre un set completo di funzionalità per la manipolazione delle immagini, inclusi ridimensionamento, ritaglio e applicazione di vari filtri ed effetti. È uno strumento versatile per tutte le tue esigenze di elaborazione delle immagini.

**Q3: Come posso ottenere una licenza completa per Aspose.Imaging per Java?**  
A: Per acquistare una licenza completa per Aspose.Imaging per Java, visita la [purchase page](https://purchase.aspose.com/buy). Troverai varie opzioni di licenza adatte al tuo progetto.

**Q4: È disponibile una prova gratuita per Aspose.Imaging per Java?**  
A: Sì, puoi accedere a una prova gratuita di Aspose.Imaging per Java dalla [releases page](https://releases.aspose.com/). Questa prova ti permette di esplorare le capacità della libreria prima di effettuare un acquisto.

**Q5: Dove posso cercare supporto o assistenza per Aspose.Imaging per Java?**  
A: Per qualsiasi domanda, problema o assistenza su Aspose.Imaging per Java, puoi visitare il [Aspose Imaging forum](https://forum.aspose.com/). La community e il team di supporto sono pronti ad aiutarti.

---

**Ultimo aggiornamento:** 2026-04-28  
**Testato con:** Aspose.Imaging for Java 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}