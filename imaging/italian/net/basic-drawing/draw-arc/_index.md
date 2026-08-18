---
date: 2026-02-09
description: Scopri come disegnare un arco usando Aspose.Imaging per .NET, inclusi
  come salvare un file BMP, impostare le dimensioni dell'immagine e impostare lo sfondo
  della grafica. Guida passo‑passo per generare immagini BMP.
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Come disegnare un arco con Aspose.Imaging per .NET
url: /it/net/basic-drawing/draw-arc/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Come disegnare un arco con Aspose.Imaging per .NET

Nel mondo dell'elaborazione delle immagini, **come disegnare un arco** è un compito comune che può aggiungere un tocco visivo a qualsiasi grafica. Con Aspose.Imaging per .NET puoi generare immagini BMP, impostare le dimensioni dell'immagine e disegnare un arco con una penna in poche righe di C#. Alla fine di questo tutorial saprai esattamente come disegnare un arco, impostare lo sfondo della grafica e salvare il file BMP risultante senza sforzo.

## Risposte rapide
- **Cosa produce il codice?** Un'immagine BMP di 100 × 100 pixel con sfondo giallo e un arco nero.  
- **Quale libreria viene utilizzata?** Aspose.Imaging per .NET.  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per lo sviluppo; è necessaria una licenza commerciale per la produzione.  
- **Posso modificare le dimensioni dell'immagine?** Sì – modifica i parametri di larghezza e altezza nella chiamata `Image.Create`.  
- **Il formato di output è fisso?** L'esempio salva un file BMP, ma può essere usato qualsiasi formato supportato da Aspose.Imaging.

## Che cosa è “come disegnare un arco” in Aspose.Imaging?
Disegnare un arco significa renderizzare un segmento di linea curva definito da un rettangolo di delimitazione, un angolo di partenza e un angolo di sweep. Aspose.Imaging fornisce il metodo `Graphics.DrawArc`, che consente di **disegnare un arco con la penna** e controllare ogni aspetto visivo.

## Perché usare Aspose.Imaging per questo compito?
- **Controllo completo** su dimensioni dell'immagine, profondità di colore e formato file.  
- **Nessuna dipendenza esterna** – tutto gira su .NET puro.  
- **Alte prestazioni** per generare grandi quantità di grafica sul lato server.  

## Prerequisiti

Prima di immergerci nel codice, assicurati di avere quanto segue:

1. **Aspose.Imaging per .NET** – scaricalo dal sito ufficiale [qui](https://releases.aspose.com/imaging/net/).  
2. **Un ambiente di sviluppo .NET** (Visual Studio, VS Code o qualsiasi compilatore C#).  

Ora che abbiamo i prerequisiti pronti, iniziamo a disegnare!

## Importazione dei namespace necessari

Per lavorare con Aspose.Imaging è necessario importare i namespace pertinenti:

### Passo 1: Importare i namespace

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

Queste istruzioni `using` ti danno accesso alle classi per la creazione di immagini, la gestione della grafica e le operazioni di I/O su file.

## Come disegnare un arco con Aspose.Imaging per .NET

Divideremo il processo in tre passaggi chiari: creare l'immagine, preparare la superficie grafica e infine disegnare l'arco.

### Passo 1: Configurare l'immagine (impostare le dimensioni dell'immagine e generare un'immagine BMP)

```csharp
// Specify the directory where you want to save the image
string dataDir = "Your Document Directory";

// Create an instance of FileStream to save the image
using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
{
    // Create an instance of BmpOptions and set its properties
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;

    // Set the source for BmpOptions and create an instance of Image
    saveOptions.Source = new StreamSource(stream);
    using (Image image = Image.Create(saveOptions, 100, 100))
    {
```

Qui **impostiamo le dimensioni dell'immagine** a 100 × 100 pixel e configuriamo le opzioni BMP. Il `FileStream` garantisce che **salviamo il file BMP** nella posizione desiderata.

### Passo 2: Inizializzare Graphics e impostare lo sfondo della grafica

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

L'oggetto `Graphics` ci permette di dipingere sull'immagine. Chiamando `Clear(Color.Yellow)` **impostiamo lo sfondo della grafica** su un giallo brillante, facendo risaltare l'arco.

### Passo 3: Definire i parametri dell'arco e disegnare l'arco con la penna

```csharp
        // Define the parameters for the arc
        int width = 100;
        int height = 200;
        int startAngle = 45;
        int sweepAngle = 270;

        // Draw the arc
        graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);

        // Save the changes
        image.Save();
    }
    stream.Close();
}
```

- `width` e `height` definiscono il rettangolo di delimitazione, impostando effettivamente **le dimensioni dell'immagine** per l'arco.  
- L'oggetto `Pen` è ciò che consente di **disegnare un arco con la penna** in nero.  
- Dopo il disegno, `image.Save()` scrive il **file BMP** su disco.

## Problemi comuni e suggerimenti

- **Arco non visibile?** Assicurati che il colore della penna contrasti con lo sfondo (es. nero su giallo).  
- **Dimensioni errate?** Ricorda che il rettangolo di delimitazione dell'arco può essere più grande dell'immagine; regola `width`/`height` o le dimensioni dell'immagine di conseguenza.  
- **Suggerimento di prestazioni:** Riutilizza una singola istanza di `Graphics` se devi disegnare più forme sulla stessa immagine.

## FAQ

### Q1: Dove posso trovare la documentazione per Aspose.Imaging per .NET?

A1: Puoi consultare la documentazione [qui](https://reference.aspose.com/imaging/net/) per informazioni complete su Aspose.Imaging per .NET.

### Q2: Come posso scaricare Aspose.Imaging per .NET?

A2: Puoi scaricare Aspose.Imaging per .NET dal sito web [qui](https://releases.aspose.com/imaging/net/).

### Q3: È disponibile una versione di prova gratuita per Aspose.Imaging per .NET?

A3: Sì, puoi ottenere una versione di prova gratuita [qui](https://releases.aspose.com/) per provare Aspose.Imaging per .NET.

### Q4: Ho bisogno di una licenza temporanea per Aspose.Imaging per .NET?

A4: Se ti serve una licenza temporanea, puoi ottenerla [qui](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso trovare supporto o fare domande su Aspose.Imaging per .NET?

A5: Puoi visitare il forum di Aspose.Imaging per supporto e discussioni [qui](https://forum.aspose.com/).

---

**Last Updated:** 2026-02-09  
**Tested With:** Aspose.Imaging 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}