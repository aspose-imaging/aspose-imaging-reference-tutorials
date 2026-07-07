---
date: 2026-05-03
description: Scopri come convertire un TIFF multipagina in formato BMP in Java usando
  Aspose.Imaging. Segui questa guida passo‑passo su come convertire il TIFF in modo
  efficiente.
keywords:
- convert multi page tiff
- how to convert tiff
- Aspose.Imaging Java
- TIFF to BMP conversion
- image processing Java
linktitle: Estrai i fotogrammi TIFF in formato BMP
second_title: Aspose.Imaging Java Image Processing API
title: Converti TIFF multipagina in BMP usando Aspose.Imaging per Java
url: /it/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Converti TIFF multipagina in BMP usando Aspose.Imaging per Java

Se hai bisogno di **convertire file tiff multipagina** in immagini BMP individuali mentre lavori in un ambiente Java, sei nel posto giusto. In questo tutorial illustreremo i passaggi esatti per estrarre ogni fotogramma TIFF e salvarlo come file BMP usando la potente libreria Aspose.Imaging per Java. Alla fine, comprenderai non solo *come convertire i file tiff* programmaticamente, ma anche perché questo approccio è affidabile per attività di elaborazione batch di immagini.

## Risposte rapide
- **Qual è la libreria migliore per la conversione da TIFF a BMP?** Aspose.Imaging for Java  
- **Quante righe di codice sono necessarie?** Circa 30 righe suddivise in cinque passaggi logici  
- **È necessaria una licenza per la produzione?** Sì, è richiesta una licenza commerciale (disponibile una prova gratuita)  
- **Può gestire grandi TIFF multipagina?** Sì, l'API trasmette i fotogrammi in modo efficiente  
- **Quale versione di Java è supportata?** Java 8 e successive  

## Cos'è “convertire TIFF multipagina”?
Convertire un TIFF multipagina significa prendere ogni pagina (o fotogramma) memorizzata all'interno di un singolo contenitore TIFF ed esportarla come file immagine indipendente—qui, BMP. Questo è utile per l'archiviazione di documenti, l'imaging medico o qualsiasi flusso di lavoro che richieda immagini raster per ulteriori elaborazioni.

## Perché usare Aspose.Imaging per Java?
- **Supporto completo dei formati** – Gestisce TIFF, BMP, JPEG, PNG e molti altri.  
- **Nessuna dipendenza esterna** – Pure Java, nessuna libreria nativa.  
- **Alte prestazioni** – L'accesso in streaming ai fotogrammi riduce l'uso della memoria.  
- **API ricca** – Offre un controllo dettagliato sui dati dei pixel, sulla profondità di colore e sui metadati.

## Prerequisiti

1. **Java Development Environment** – JDK 8+ e il tuo IDE preferito.  
2. **Aspose.Imaging for Java** – Scarica l'ultimo JAR dal sito ufficiale **[here](https://releases.aspose.com/imaging/java/)**.  
3. **Sample multi‑page TIFF** – Posiziona un file TIFF (ad es., `sample.tiff`) in una directory nota che il tuo codice può leggere.

## Importa pacchetti

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## Come convertire TIFF multipagina in BMP con Aspose.Imaging

### Passo 1: Carica l'immagine TIFF e inizializza il contatore dei fotogrammi

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // Create an instance of int to keep track of frames in TiffImage
    int frameCounter = 0;
```

### Passo 2: Itera sui fotogrammi TIFF

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

## Problemi comuni e consigli

- **Uso della memoria:** Quando si gestiscono file TIFF molto grandi, considera di elaborare i fotogrammi uno alla volta (come mostrato) invece di caricare l'intera immagine in memoria.  
- **Denominazione dei file:** La chiamata `String.format` genera un nome file unico per ogni fotogramma (`...out0.bmp`, `...out1.bmp`, ecc.). Regola il modello se ti serve una convenzione di denominazione diversa.  
- **Profondità di bit:** BMP supporta varie profondità di bit; 24‑bit (vero colore) funziona nella maggior parte degli scenari. Cambia `setBitsPerPixel` se ti serve un output in scala di grigi a 8‑bit.

## FAQ

### Q1: Cos'è Aspose.Imaging per Java?

A1: Aspose.Imaging per Java è una libreria Java che offre ampie capacità di elaborazione delle immagini, consentendo di lavorare con vari formati di immagine ed eseguire operazioni come conversione, modifica e manipolazione.

### Q2: Posso usare Aspose.Imaging per Java con diversi formati di immagine?

A2: Sì, Aspose.Imaging per Java supporta un'ampia gamma di formati immagine, inclusi TIFF, BMP, JPEG, PNG e molti altri, rendendolo uno strumento versatile per attività legate alle immagini.

### Q3: Dove posso trovare la documentazione per Aspose.Imaging per Java?

A3: Puoi trovare la documentazione dettagliata per Aspose.Imaging per Java **[here](https://reference.aspose.com/imaging/java/)**.

### Q4: È disponibile una prova gratuita per Aspose.Imaging per Java?

A4: Sì, puoi esplorare Aspose.Imaging per Java con una prova gratuita disponibile **[here](https://releases.aspose.com/)**.

### Q5: Come posso ottenere supporto per Aspose.Imaging per Java?

A5: Per qualsiasi domanda, problema o supporto relativo a Aspose.Imaging per Java, puoi visitare il forum di supporto **[here](https://forum.aspose.com/)**.

## Domande frequenti

**Q: Posso convertire un TIFF multipagina in altri formati (ad es., PNG) usando lo stesso approccio?**  
A: Assolutamente. Sostituisci `BmpOptions` con la classe di opzioni appropriata (ad es., `PngOptions`) e regola l'estensione del file nel percorso `FileCreateSource`.

**Q: Aspose.Imaging gestisce TIFF compressi (LZW, CCITT)?**  
A: Sì, la libreria decomprime in modo trasparente gli schemi di compressione TIFF supportati durante l'estrazione dei fotogrammi.

**Q: È possibile preservare i metadati EXIF durante la conversione in BMP?**  
A: BMP non supporta i metadati EXIF. Se hai bisogno di conservare i metadati, considera di convertire in un formato che li supporta (ad es., PNG) o copia manualmente i metadati dopo la conversione.

**Q: Come posso elaborare in batch più file TIFF in una cartella?**  
A: Avvolgi il codice sopra in un ciclo che itera sugli oggetti `File` in una directory, aggiornando `dataDir` e il nome file di origine per ogni file.

**Q: Quale licenza è necessaria per il deployment commerciale?**  
A: È richiesta una licenza a pagamento di Aspose.Imaging per Java per l'uso in produzione. È possibile utilizzare una licenza di prova temporanea durante lo sviluppo.

---

**Ultimo aggiornamento:** 2026-05-03  
**Testato con:** Aspose.Imaging for Java 24.12 (latest at time of writing)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}