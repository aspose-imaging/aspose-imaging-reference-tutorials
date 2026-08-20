---
date: '2026-03-20'
description: Scopri come utilizzare Aspose.Imaging per Java per comprimere le immagini
  TIFF con compressione LZW, riducendo le dimensioni del file mantenendo la qualità.
keywords:
- compress TIFF images Java
- Aspose.Imaging LZW compression
- Java image optimization
- TIFF compression in Java with Aspose
- image compression tutorial
title: Come utilizzare Aspose.Imaging per comprimere le immagini TIFF in Java (Guida
  alla compressione LZW)
url: /it/java/compression-optimization/compress-tiff-images-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Tutorial: Compressione di immagini TIFF con Aspose.Imaging Java

## Introduzione

In questo tutorial imparerai **come utilizzare Aspose.Imaging per Java** per comprimere le immagini TIFF in modo efficiente. Gestire file TIFF di grandi dimensioni può consumare rapidamente spazio di archiviazione e larghezza di banda, ma con la compressione LZW (Lempel‑Ziv‑Welch) puoi **ridurre le dimensioni del file TIFF** senza sacrificare la fedeltà dell’immagine. Ti guideremo attraverso il caricamento di un TIFF, la configurazione della **compressione TIFF LZW** e il salvataggio del risultato ottimizzato—perfetto per chiunque sia interessato alla **ottimizzazione delle immagini Java**.

**Cosa imparerai**
- Come configurare Aspose.Imaging per Java
- Caricare e processare immagini TIFF con facilità
- Configurare la compressione LZW usando `TiffOptions`
- Salvare immagini TIFF ottimizzate più piccole ma senza perdita di qualità

Procediamo con i prerequisiti così potrai iniziare a comprimere subito.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.Imaging per Java  
- **Quale algoritmo di compressione?** LZW (senza perdita)  
- **Versioni Java supportate?** Le versioni JDK più recenti (es. 11, 17)  
- **È necessaria una licenza?** Una licenza di prova o temporanea è sufficiente per i test; per la produzione è richiesta una licenza commerciale.  
- **Riduzione tipica delle dimensioni?** Fino al 30‑50 % per immagini idonee  

## Prerequisiti

Prima di implementare la compressione delle immagini nel tuo progetto Java, assicurati di avere quanto segue:

- **Libreria Aspose.Imaging per Java** – indispensabile per tutte le funzionalità di elaborazione immagini.  
- **Java Development Kit (JDK)** – una versione recente compatibile con la libreria Aspose.  
- **Conoscenze di base di Java** – familiarità con I/O di file e concetti di programmazione orientata agli oggetti sarà d’aiuto.

## Configurare Aspose.Imaging per Java

Per iniziare, aggiungi la libreria Aspose.Imaging al tuo sistema di build. Scegli il metodo che corrisponde al tuo progetto.

### Utilizzo di Maven
Aggiungi la seguente dipendenza al tuo `pom.xml`:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Utilizzo di Gradle
Inserisci questa riga nel tuo file `build.gradle`:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Download diretto
In alternativa, scarica l’ultima versione da [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

#### Acquisizione della licenza
Puoi ottenere una licenza di prova gratuita o richiedere una licenza temporanea per valutare completamente le capacità di Aspose.Imaging prima dell’acquisto.

## Come utilizzare Aspose.Imaging per la compressione TIFF in Java

Ora analizziamo l’implementazione passo dopo passo. Ogni blocco di codice è rimasto invariato rispetto al tutorial originale, ma aggiungeremo un contesto più chiaro attorno ad essi.

### Caricamento di un’immagine TIFF

**Perché è importante:** Caricare correttamente l’immagine crea un oggetto `Image` valido su cui tutte le operazioni successive agiranno.

#### Passo 1: Importare la classe Image
```java
import com.aspose.imaging.Image;
```

#### Passo 2: Caricare l’immagine dal disco
```java
String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "/sample.tiff";
Image image = Image.load(dataDir);
```

### Creare TiffOptions per la compressione dell’immagine

**Perché è importante:** `TiffOptions` ti consente di definire esattamente come il TIFF di output deve essere codificato, inclusa l’impostazione **tiff compression LZW**.

#### Passo 1: Importare gli enum e la classe delle opzioni richiesti
```java
import com.aspose.imaging.fileformats.tiff.enums.TiffCompressions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.imaging.imageoptions.TiffOptions;
```

#### Passo 2: Configurare le opzioni di compressione
```java
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);
outputSettings.setBitsPerSample(new int[] { 4 });
outputSettings.setCompression(TiffCompressions.Lzw);
outputSettings.setPhotometric(TiffPhotometrics.Palette);
```

### Impostare una palette in scala di grigi (opzionale ma utile)

Applicare una palette in scala di grigi a 4 bit può ridurre ulteriormente **le dimensioni del file TIFF**, soprattutto per scansioni monocromatiche.

#### Passo 1: Importare l’aiutante per la palette
```java
import com.aspose.imaging.ColorPaletteHelper;
```

#### Passo 2: Assegnare la palette in scala di grigi
```java
outputSettings.setPalette(ColorPaletteHelper.create4BitGrayscale(false));
```

### Salvataggio dell’immagine TIFF compressa

**Perché è importante:** La chiamata `save` scrive l’immagine su disco usando tutte le opzioni configurate, producendo un file più piccolo e compresso con LZW.

#### Passo 1: Definire il percorso di output
```java
String outputDir = "YOUR_OUTPUT_DIRECTORY" + "/SampleTiff_out.tiff";
```

#### Passo 2: Salvare con le impostazioni di compressione
```java
image.save(outputDir, outputSettings);
```

## Applicazioni pratiche

Ecco alcuni scenari reali in cui **come comprimere immagini tiff** con LZW può fare la differenza:

1. **Archiviazione di documenti** – Conserva PDF o TIFF scansionati in modo più efficiente.  
2. **Imaging medico** – Mantieni i dettagli diagnostici preservando dimensioni di file gestibili.  
3. **Archivi fotografici** – Conserva master ad alta risoluzione senza gonfiare lo spazio di archiviazione.  
4. **Applicazioni web** – Servi immagini più piccole per caricamenti di pagina più rapidi e costi di larghezza di banda inferiori.

## Considerazioni sulle prestazioni

Quando lavori con immagini di grandi dimensioni, tieni presenti questi consigli per mantenere prestazioni ottimali:

- **Gestione della memoria:** Rilascia prontamente gli oggetti `Image` di grandi dimensioni (`image.dispose()`) se elabori molti file in un ciclo.  
- **Ottimizzazione della profondità di bit:** Regola `BitsPerSample` al valore più basso accettabile per il tuo caso d’uso.  
- **Elaborazione batch:** Per operazioni su larga scala, considera il multithreading ma monitora l’utilizzo dell’heap JVM.

## Problemi comuni e soluzioni

| Sintomo | Probabile causa | Soluzione |
|---------|-----------------|-----------|
| OutOfMemoryError durante il caricamento di TIFF enormi | L’immagine viene caricata interamente in memoria | Usa `Image.load(dataDir, new LoadOptions { BufferSize = … })` o elabora a tasselli. |
| Il file salvato è più grande dell’originale | `BitsPerSample` errato o palette non corrispondente | Verifica che `setBitsPerSample` corrisponda alla profondità colore dell’immagine sorgente. |
| La palette in scala di grigi appare errata | Palette non applicata prima del salvataggio | Assicurati che `outputSettings.setPalette(...)` sia chiamato **prima** di `image.save`. |

## Domande frequenti

**D: Cos’è la compressione LZW?**  
R: La compressione Lempel‑Ziv‑Welch (LZW) è un algoritmo senza perdita che riduce le dimensioni del file senza perdere dati dell’immagine.

**D: Posso usare Aspose.Imaging per Java in progetti commerciali?**  
R: Sì, è possibile acquistare una licenza per utilizzo commerciale. Visita [Aspose Purchase](https://purchase.aspose.com/buy) per i dettagli.

**D: La libreria è compatibile con tutte le versioni JDK?**  
R: Supporta la maggior parte delle versioni JDK recenti. Consulta la documentazione ufficiale per la compatibilità esatta.

**D: Come gestire immagini di grandi dimensioni senza esaurire la memoria?**  
R: Implementa pratiche di gestione della memoria efficienti, come il rilascio tempestivo degli oggetti `Image` e l’elaborazione delle immagini in blocchi più piccoli quando possibile.

**D: Quali altri formati di file supporta Aspose.Imaging?**  
R: La libreria gestisce BMP, JPEG, PNG, GIF e molti altri. Esplora l’elenco completo sul loro [sito di documentazione](https://reference.aspose.com/imaging/java/).

## Risorse

- **Documentazione:** [Aspose.Imaging Java Reference](https://reference.aspose.com/imaging/java/)  
- **Download:** [Latest Releases](https://releases.aspose.com/imaging/java/)  
- **Acquisto:** [Buy Now](https://purchase.aspose.com/buy)  
- **Prova gratuita:** [Start Here](https://releases.aspose.com/imaging/java/)  
- **Licenza temporanea:** [Request Here](https://purchase.aspose.com/temporary-license/)  
- **Supporto:** Per ulteriore assistenza, visita il [Forum Aspose](https://forum.aspose.com/c/imaging/14)

---  

**Ultimo aggiornamento:** 2026-03-20  
**Testato con:** Aspose.Imaging 25.5 per Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}