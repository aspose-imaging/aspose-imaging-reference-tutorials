---
date: 2026-05-03
description: Scopri come ritagliare un'immagine con Aspose.Imaging per Java, inclusi
  il ritaglio rettangolare e l'espansione della tela. Guida passo passo per gli sviluppatori.
keywords:
- how to crop image
- crop and expand image
- aspose imaging crop
- java image processing tutorial
- expand image canvas java
linktitle: Espansione o ritaglio dell'immagine
second_title: Aspose.Imaging Java Image Processing API
title: Come ritagliare un'immagine a rettangolo con Aspose.Imaging per Java
url: /it/java/document-conversion-and-processing/image-expansion-or-cropping/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Come ritagliare un'immagine in un rettangolo con Aspose.Imaging per Java

Nel mondo digitale di oggi, in rapida evoluzione, sapere **come ritagliare un'immagine** in modo rapido e affidabile è un requisito fondamentale per qualsiasi flusso di lavoro di immagini basato su Java. Che tu stia ritagliando foto caricate dagli utenti per un servizio web, generando miniature coerenti per un catalogo e‑commerce o preparando risorse per una campagna di marketing, Aspose.Imaging per Java offre un'API pulita e ad alte prestazioni per svolgere il lavoro. In questo tutorial vedremo come ritagliare un rettangolo da un'immagine e come espandere la tela dell'immagine—perfetto per chi desidera padroneggiare le tecniche di elaborazione immagini in Java.

## Risposte rapide
- **Qual è la libreria migliore per il ritaglio di immagini in Java?** Aspose.Imaging for Java.  
- **Posso ritagliare in un rettangolo arbitrario?** Sì – definisci qualsiasi X, Y, larghezza e altezza.  
- **Ho bisogno di una licenza per lo sviluppo?** Una versione di prova gratuita è sufficiente per i test; è necessaria una licenza per la produzione.  
- **È possibile espandere un'immagine?** Assolutamente – puoi aumentare le dimensioni della tela prima del ritaglio.  
- **Quale versione di Java è supportata?** Java 8 e successive.

## Cos'è il ritaglio di un'immagine in un rettangolo
Ritagliare un'immagine in un rettangolo significa estrarre una sotto‑sezione del bitmap originale definita da una regione rettangolare (offset X, offset Y, larghezza, altezza). Il resto dell'immagine viene scartato, lasciandoti con una nuova immagine più piccola che contiene solo l'area necessaria.

## Perché usare Aspose.Imaging per Java?
- **Nessuna dipendenza esterna** – puro Java, funziona su qualsiasi piattaforma.  
- **Ampio supporto di formati** – JPEG, PNG, BMP, TIFF e altri.  
- **Caching ad alte prestazioni** – `cacheData()` riduce il carico I/O.  
- **API semplice** – chiamate a una riga per caricare, definire un rettangolo e salvare.

## Prerequisiti
- **Ambiente di sviluppo Java** – JDK 8+ installato e configurato.  
- **Aspose.Imaging per Java** – scarica dal [sito web](https://releases.aspose.com/imaging/java/).  
- **Conoscenza di base di Java** – familiarità con classi, try‑with‑resources e percorsi di file.  
- **Immagine da utilizzare** – qualsiasi JPEG/PNG che desideri ritagliare o espandere.

## Importazione dei pacchetti
Per prima cosa, indica al codice la cartella che contiene le tue immagini sorgente. Questo snippet rimane invariato rispetto al tutorial originale.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

Sostituisci `"Your Document Directory"` con il percorso assoluto sul tuo computer.

## Passo 1: Caricare l'immagine
Caricare l'immagine è la base per qualsiasi manipolazione. Chiamiamo anche `cacheData()` per mantenere il bitmap in memoria per operazioni successive più veloci.

```java
try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
{
    rasterImage.cacheData();
}
```

> **Consiglio professionale:** Usa un blocco `try‑with‑resources` (come mostrato) per garantire che l'immagine venga chiusa automaticamente, evitando perdite di memoria.

## Passo 2: Definire l'area per il ritaglio
Qui creiamo un `Rectangle` che rappresenta l'esatta area che vuoi conservare. Il rettangolo può iniziare al di fuori dei limiti originali – Aspose.Imaging espanderà automaticamente la tela (utile per lo scenario **expand image canvas java**).

```java
// Create an instance of Rectangle class and define X, Y, Width, and Height of the rectangle
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

- **X / Y** – valori negativi spostano il rettangolo a sinistra/alto, facendo espandere la tela.  
- **Larghezza / Altezza** – dimensione dell'area ritagliata.

## Passo 3: Salvare l'immagine ritagliata (o espansa)
Infine, scrivi il risultato su disco. Il metodo `save` accetta il percorso di destinazione, le opzioni di formato immagine e il rettangolo definito.

```java
rasterImage.save("Your Document Directory" + "Grayscaling_out.jpg", new JpegOptions(), destRect);
```

Il file di output `Grayscaling_out.jpg` ora contiene il risultato del **crop image to rectangle**. Se il rettangolo si estendeva oltre l'immagine originale, l'area extra viene riempita con uno sfondo predefinito (trasparente per PNG, nero per JPEG).

## Come ritagliare un'immagine con Aspose.Imaging per Java
Questa sezione riepiloga i passaggi fondamentali in una checklist concisa così da poterli consultare rapidamente durante la codifica:

1. **Imposta la directory dei dati** – punta alla cartella contenente le immagini sorgente.  
2. **Carica l'immagine** con `Image.load()` e chiama `cacheData()`.  
3. **Crea un `Rectangle`** che definisce l'area di ritaglio (o l'espansione della tela).  
4. **Salva** la nuova immagine usando `rasterImage.save()` e passa il rettangolo.

## Ritagliare ed Espandere l'Immagine – Casi d'Uso Reali
| Scenario | Perché è importante |
|----------|----------------------|
| **Generazione di miniature** | Estrai rapidamente una regione centrale per dimensioni coerenti. |
| **Ritaglio dell'immagine del profilo utente** | Imponi un'area avatar quadrata o rettangolare. |
| **Espansione della tela prima di aggiungere filigrane** | Aggiungi spazio attorno all'immagine senza distorcere l'originale. |
| **Elaborazione batch di documenti scansionati** | Ritaglia i margini in un'unica passata. |

## Risoluzione dei problemi e consigli
- **Immagine non si carica?** Verifica il percorso del file e assicurati che il formato dell'immagine sia supportato.  
- **Bordi neri inattesi dopo l'espansione?** Imposta un colore di sfondo in `JpegOptions` o usa PNG per la trasparenza.  
- **Problemi di prestazioni con immagini grandi?** Aumenta la dimensione dell'heap Java (`-Xmx`) o elabora le immagini in batch più piccoli.  
- **Errore comune:** Dimenticare di chiamare `cacheData()` può causare I/O più lento nelle operazioni successive.

## Domande Frequenti

**D: Quali formati di immagine supporta Aspose.Imaging per Java?**  
R: JPEG, PNG, BMP, TIFF, GIF, ICO, PSD e molti altri. Consulta la documentazione ufficiale per l'elenco completo.

**D: Posso eseguire altre manipolazioni di immagine con Aspose.Imaging per Java?**  
R: Assolutamente! Ridimensionamento, rotazione, filtraggio e conversione di formato sono tutti disponibili.

**D: Aspose.Imaging per Java è adatto per applicazioni web?**  
R: Sì. La libreria è thread‑safe e funziona bene in contenitori servlet e servizi Spring Boot.

**D: Come posso ottenere supporto per Aspose.Imaging per Java?**  
R: Visita il [forum](https://forum.aspose.com/) per assistenza della community, o apri un ticket di supporto con una licenza valida.

**D: È disponibile una versione di prova gratuita per Aspose.Imaging per Java?**  
R: Sì, puoi esplorare la libreria con una prova gratuita. Scaricala da [qui](https://releases.aspose.com/).

## Conclusione
Ora sai **come ritagliare un'immagine** in un rettangolo e persino **espandere la tela dell'immagine** usando la potente API di Aspose.Imaging. Padroneggiando questi fondamenti potrai costruire pipeline di elaborazione immagini robuste, migliorare la reattività dell'interfaccia utente e fornire contenuti visivi di alta qualità in qualsiasi applicazione Java.

---

**Last Updated:** 2026-05-03  
**Testato con:** Aspose.Imaging for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}