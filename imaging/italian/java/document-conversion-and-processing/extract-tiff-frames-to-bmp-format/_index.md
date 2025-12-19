---
date: 2025-12-19
description: Scopri come convertire i file TIFF in BMP in Java con Aspose.Imaging.
  Questo tutorial passo‑passo di elaborazione immagini in Java mostra la conversione
  di immagini Java per file TIFF multi‑pagina.
linktitle: Extract TIFF Frames to BMP Format
second_title: Aspose.Imaging Java Image Processing API
title: Come convertire TIFF in BMP usando Aspose.Imaging per Java
url: /it/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# converti tiff in bmp con Aspose.Imaging per Java

Se hai bisogno di **convertire tiff in bmp** all'interno di un'applicazione Java, sei nel posto giusto. Che tu stia gestendo un TIFF a pagina singola o un documento multi‑pagina, Aspose.Imaging per Java rende il processo semplice e affidabile. In questo tutorial vedremo come estrarre ogni frame da un file TIFF e salvarlo come immagine BMP individuale—perfetto per scenari di conversione di immagini java.

## Risposte rapide
- **Quale libreria gestisce la conversione?** Aspose.Imaging for Java  
- **Può elaborare TIFF multi‑pagina?** Sì – ogni frame viene salvato come BMP separato  
- **È necessaria una licenza per la produzione?** È richiesta una licenza Aspose valida per uso commerciale  
- **Quale versione di Java è supportata?** Java 8 o superiore  
- **Quanto tempo impiega il codice ad eseguire?** Tipicamente pochi secondi per immagini di dimensioni standard  

## Prerequisiti

Prima di iniziare, assicurati di avere i seguenti prerequisiti pronti:

1. **Java Development Environment** – un JDK funzionante (8 o più recente) e un IDE o strumento di build a tua scelta.  
2. **Aspose.Imaging for Java** – scarica l'ultimo JAR dal sito web [here](https://releases.aspose.com/imaging/java/).  
3. **Sample TIFF Image** – un file TIFF (a pagina singola o multi‑pagina) posizionato nella directory di lavoro del tuo progetto.

## Importa pacchetti

Per avviare il processo, è necessario importare i pacchetti necessari per la tua applicazione Java:

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## Guida passo‑passo per convertire tiff in bmp

### Passo 1: Carica l'immagine TIFF e inizializza il contatore dei frame

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // Create an instance of int to keep track of frames in TiffImage
    int frameCounter = 0;
```

### Passo 2: Itera sui frame TIFF

```java
    // Iterate over the TiffFrames in TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

### Passo 3: Carica i pixel di TiffFrame in un array di colori

```java
        // Load Pixels of TiffFrame into an array of Colors
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

### Passo 4: Crea le opzioni BMP e imposta i bit per pixel

```java
        // Create an instance of bmpCreateOptions
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

### Passo 5: Salva l'immagine BMP

```java
            // Set the Source of bmpCreateOptions as FileCreateSource by specifying the location where output will be saved
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // Create a new bmpImage
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // Save the bmpImage with pixels from TiffFrame
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## Perché usare Aspose.Imaging per Java?

- **Supporto multi‑pagina robusto** – Gestisce qualsiasi numero di frame TIFF senza codice aggiuntivo.  
- **Implementazione pure Java** – Nessuna dipendenza nativa, rendendola ideale per distribuzioni cross‑platform.  
- **Output BMP di alta qualità** – Puoi controllare i bit‑per‑pixel, la compressione e la profondità di colore.  
- **Toolkit completo per la conversione di immagini java** – Funziona con JPEG, PNG, GIF e molti altri formati.

## Problemi comuni e risoluzione

| Sintomo | Causa probabile | Risoluzione |
|---------|-----------------|-------------|
| `OutOfMemoryError` durante il caricamento di TIFF di grandi dimensioni | L'intera immagine è caricata in memoria | Elabora i frame uno‑per‑uno come mostrato, oppure aumenta la dimensione dell'heap JVM (`-Xmx`) |
| Il file BMP è corrotto | Valore `BitsPerPixel` errato | Usa 24 o 32 per BMP a colori veri |
| Nessun file di output creato | Percorso della directory di output errato | Verifica che `Your Document Directory` punti a una cartella esistente |

## Domande frequenti

### Q1: Cos'è Aspose.Imaging per Java?

A1: Aspose.Imaging per Java è una libreria Java che fornisce ampie capacità di elaborazione delle immagini, consentendo di lavorare con vari formati di immagine ed eseguire operazioni come conversione, modifica e manipolazione.

### Q2: Posso usare Aspose.Imaging per Java con diversi formati di immagine?

A2: Sì, Aspose.Imaging per Java supporta un'ampia gamma di formati di immagine, inclusi TIFF, BMP, JPEG, PNG e molti altri, rendendolo uno strumento versatile per attività legate alle immagini.

### Q3: Dove posso trovare la documentazione per Aspose.Imaging per Java?

A3: Puoi trovare la documentazione dettagliata per Aspose.Imaging per Java [here](https://reference.aspose.com/imaging/java/).

### Q4: È disponibile una versione di prova gratuita per Aspose.Imaging per Java?

A4: Sì, puoi provare Aspose.Imaging per Java con una versione di prova gratuita disponibile [here](https://releases.aspose.com/).

### Q5: Come posso ottenere supporto per Aspose.Imaging per Java?

A5: Per qualsiasi domanda, problema o supporto relativo a Aspose.Imaging per Java, puoi visitare il forum di supporto [here](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2025-12-19  
**Testato con:** Aspose.Imaging for Java 24.12 (latest)  
**Autore:** Aspose