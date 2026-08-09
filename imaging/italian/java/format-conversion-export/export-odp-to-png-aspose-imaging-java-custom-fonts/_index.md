---
date: '2026-06-28'
description: Scopri come convertire ODP in PNG usando Aspose.Imaging for Java, impostare
  font personalizzati e disabilitare i font di sistema per una resa accurata.
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: Come convertire ODP in PNG con Aspose.Imaging for Java – Guida a font personalizzati
  e esportazione
url: /it/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Come Convertire ODP in PNG con Aspose.Imaging per Java – Font Personalizzati & Guida all'Esportazione

Nelle moderne applicazioni Java, convertire i file OpenDocument Presentation (ODP) in immagini PNG ad alta qualità è una esigenza comune—soprattutto quando è necessario preservare l'identità del brand tramite font personalizzati. Questa guida mostra **come convertire ODP** in PNG usando Aspose.Imaging per Java, ti accompagna nella configurazione di una cartella di font personalizzati, nella disabilitazione dei font di fallback di sistema e nella messa a punto delle opzioni di rasterizzazione per prestazioni ottimali.

**Cosa Imparerai**
- Come impostare una directory di font personalizzati per la conversione ODP.  
- Come disabilitare i font alternativi di sistema in modo che vengano usati solo i tipi di carattere scelti.  
- Come esportare un file ODP in PNG con dimensioni precise e impostazioni dei font.  
- Suggerimenti per migliorare velocità e utilizzo della memoria durante l'elaborazione di presentazioni di grandi dimensioni.

## Risposte Rapide
- **Posso usare Maven per aggiungere Aspose.Imaging?** Sì, aggiungi la dipendenza Maven ed esegui `mvn install`.  
- **Ho bisogno di una licenza per la produzione?** È necessaria una licenza valida di Aspose.Imaging per un utilizzo illimitato.  
- **I miei font personalizzati saranno rispettati?** Imposta la cartella dei font e disabilita le alternative di sistema per farli rispettare.  
- **Quali formati immagine sono supportati?** Aspose.Imaging supporta oltre 120 formati raster e vettoriali, inclusi PNG, JPEG, TIFF e WebP.  
- **L'API è thread‑safe?** Sì, la maggior parte delle classi di Aspose.Imaging è sicura per l'uso concorrente quando crei istanze separate per thread.

## Che cos'è “how to convert odp”?
*“How to convert odp”* si riferisce al processo di trasformazione di un file OpenDocument Presentation in un altro formato—spesso PNG—preservando layout, font e fedeltà visiva. Aspose.Imaging per Java fornisce un flusso di lavoro a singolo metodo che gestisce questa conversione senza richiedere strumenti esterni, consentendo agli sviluppatori di integrare la conversione direttamente nelle loro applicazioni con codice minimo.

## Perché Usare Aspose.Imaging per Java?
Aspose.Imaging supporta **oltre 120 formati di output** e può rasterizzare file ODP multi‑pagina senza caricare l'intero documento in memoria, riducendo l'utilizzo di RAM di picco fino al 70 % su presentazioni di grandi dimensioni. La libreria offre anche una gestione dei font integrata, eliminando la necessità di motori di rendering di terze parti.

## Prerequisiti
- **Librerie**: Aspose.Imaging per Java ≥ 25.5.  
- **JDK**: Versione 8 o successiva.  
- **IDE**: IntelliJ IDEA, Eclipse o qualsiasi editor compatibile con Java.  
- **Conoscenze di base**: Java I/O, programmazione orientata agli oggetti e concetti di immagine.

## Istruzioni di Installazione

### Maven
Aggiungi la seguente dipendenza al tuo `pom.xml` ed esegui `mvn clean install`:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
Includi la libreria nel tuo file `build.gradle` e aggiorna il progetto:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Download Diretto
Scarica l'ultimo JAR da [Rilasci di Aspose.Imaging per Java](https://releases.aspose.com/imaging/java/).

## Passaggi per Ottenere la Licenza
Per sbloccare tutte le funzionalità, applica una licenza temporanea o permanente:

1. **Prova gratuita** – Nessuna licenza richiesta, funzionalità limitate.  
2. **Licenza temporanea** – Richiedila sul [sito Aspose](https://purchase.aspose.com/temporary-license/).  
3. **Acquisto** – Acquista un abbonamento o una licenza perpetua dalla [pagina di acquisto di Aspose](https://purchase.aspose.com/buy).

Inizializza la libreria con il tuo file di licenza:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## Come impostare una directory di font personalizzati per la conversione ODP?
`FontSettings` è una classe che gestisce le risorse dei font per Aspose.Imaging. Carica i tuoi font personalizzati prima di avviare qualsiasi elaborazione di immagini. Questo garantisce che ogni diapositiva utilizzi esattamente i tipi di carattere forniti.

Imposta il percorso della cartella dei font usando `FontSettings` di Aspose.Imaging:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Ancora di definizione*: `FontSettings.setFontsFolder` indica ad Aspose.Imaging dove cercare i font TrueType e OpenType nel file system.

## Come disabilitare i font alternativi di sistema durante la conversione ODP?
Disabilitare le alternative di sistema costringe il motore di rendering a ignorare i font installati sul sistema operativo, garantendo che vengano usati solo i font forniti da te. Questo elimina sostituzioni di font inattese che possono alterare l'aspetto visivo delle tue diapositive.

Disabilita le alternative di sistema con la seguente chiamata:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Ancora di definizione*: `FontSettings.setGetSystemAlternativeFont(false)` costringe il motore a usare solo i font presenti nella cartella definita, eliminando sostituzioni inattese.

## Come esportare un file ODP in PNG con un font specificato?
`RasterizationOptions` definisce come le pagine vettoriali vengono rasterizzate in immagini bitmap. Combinando la configurazione dei font con le impostazioni di rasterizzazione, puoi controllare DPI, colore di sfondo e dimensione della pagina per ogni PNG esportato.

Implementa il metodo di esportazione come mostrato di seguito:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*Ancora di definizione*: La classe `RasterizationOptions` controlla DPI, dimensione della pagina e colore di sfondo per i file PNG generati.

### Problemi Comuni & Soluzioni
- **File di font mancanti** – Verifica che ogni `.ttf` o `.otf` referenziato nell'ODP sia presente nella cartella impostata.  
- **Percorsi file errati** – Usa percorsi assoluti o risolvi i percorsi relativi rispetto a `System.getProperty("user.dir")`.  
- **Permessi insufficienti** – Assicurati che il processo Java possa leggere la directory dei font e scrivere nella cartella di output.

## Applicazioni Pratiche
1. **Diapositive coerenti con il brand** – Esporta le presentazioni come PNG per la pubblicazione web preservando i font aziendali.  
2. **Generazione automatica di report** – Converti ogni diapositiva in un'immagine da includere in report PDF o newsletter email.  
3. **Creazione di archivi legacy** – Archivia il contenuto ODP come PNG per garantire l'accessibilità futura senza necessità di visualizzatori ODP.

## Considerazioni sulle Prestazioni
- Usa l'ultima versione di Aspose.Imaging per beneficiare dei miglioramenti della rasterizzazione multithread (fino a 2× più veloce su CPU a 8 core).  
- Avvolgi l'elaborazione delle immagini in un blocco try‑with‑resources per garantire la corretta liberazione tempestiva delle risorse native.  
- Regola `RasterizationOptions` (ad esempio, DPI più basso) quando elabori migliaia di diapositive per bilanciare qualità e utilizzo della memoria.

## Domande Frequenti

**D: Qual è la versione minima di Java richiesta?**  
R: Aspose.Imaging per Java funziona con JDK 8 e versioni successive; JDK 11 è consigliato per il supporto a lungo termine.

**D: Posso convertire solo diapositive selezionate?**  
R: Sì, imposta `rasterizationOptions.setPageNumber(specificSlideIndex)` prima di chiamare `save`.

**D: Come gestisco i file ODP protetti da password?**  
R: Carica il file con `LoadOptions` che include la password, quindi procedi con le stesse impostazioni dei font.

**D: La disabilitazione dei font di sistema influisce sulle prestazioni?**  
R: Migliora marginalmente la velocità poiché il motore salta la ricerca dei font di sistema, soprattutto su macchine con grandi collezioni di font.

**D: Dove posso trovare altri esempi di codice?**  
R: Esplora la [documentazione ufficiale di Aspose.Imaging](https://reference.aspose.com/imaging/java/) per scenari aggiuntivi come conversione batch e trasformazioni di immagini.

## Risorse Aggiuntive
- [Rilasci di Aspose.Imaging per Java](https://releases.aspose.com/imaging/java/)  
- [Rilasci di Aspose.Imaging](https://releases.aspose.com/imaging/java/)  
- [Inizia la tua prova gratuita](https://releases.aspose.com/imaging/java/)  
- [Documentazione di Aspose.Imaging](https://reference.aspose.com/imaging/java/)  
- [Forum di Aspose.Imaging](https://forum.aspose.com/c/imaging/14)  
- [Acquista licenze Aspose](https://purchase.aspose.com/buy)  
- [Richiedi una licenza temporanea](https://purchase.aspose.com/temporary-license/)  

---

**Ultimo aggiornamento:** 2026-06-28  
**Testato con:** Aspose.Imaging per Java 25.5  
**Autore:** Aspose

## Tutorial Correlati

- [Converti ODG in PNG con Aspose.Imaging per Java: Guida Completa](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Conversione Efficiente di Immagini in Java con Aspose.Imaging: Guida Completa](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}