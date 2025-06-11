---
"description": "Scopri come disegnare immagini raster su SVG usando Aspose.Imaging per .NET. Migliora le tue applicazioni .NET con immagini dinamiche."
"linktitle": "Disegna un'immagine raster su SVG in Aspose.Imaging per .NET"
"second_title": "API di elaborazione delle immagini .NET Aspose.Imaging"
"title": "Come disegnare un'immagine raster su SVG in Aspose.Imaging per .NET"
"url": "/it/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Come disegnare un'immagine raster su SVG in Aspose.Imaging per .NET


Nel mondo della programmazione .NET, Aspose.Imaging si distingue per la sua versatilità e affidabilità, consentendo di gestire diverse attività legate alle immagini. Una delle funzionalità più interessanti è la possibilità di disegnare un'immagine raster su un'area di lavoro SVG. In questa guida passo passo, vi guideremo attraverso il processo di disegno di un'immagine raster su un'area di lavoro SVG utilizzando Aspose.Imaging per .NET.

## Prerequisiti

Prima di entrare nei dettagli, assicurati di avere i seguenti prerequisiti:

- Aspose.Imaging per .NET: è necessario che la libreria sia installata. In caso contrario, è possibile scaricarla da [Pagina di download di Aspose.Imaging per .NET](https://releases.aspose.com/imaging/net/).

- La tua directory dei documenti: Sostituisci `"Your Document Directory"` con il percorso effettivo verso la directory di lavoro.

Ora scomponiamo il processo in semplici passaggi:

## Passaggio 1: importare gli spazi dei nomi necessari

Per lavorare con Aspose.Imaging è necessario importare gli spazi dei nomi richiesti:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Passaggio 2: caricare le immagini

- Per prima cosa, carica l'immagine raster che vuoi disegnare sulla tela SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Successivamente, carica l'immagine canvas SVG nel punto in cui vuoi disegnare l'immagine raster.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Passaggio 3: disegno sull'immagine SVG

Ora puoi iniziare a disegnare sull'immagine SVG esistente. Per farlo, devi creare un'istanza di `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Passaggio 4: disegnare l'immagine raster

- Definisci i limiti in cui desideri disegnare l'immagine raster e specifica la regione sorgente dell'immagine raster.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Passaggio 5: salva il risultato

Dopo aver disegnato l'immagine raster sulla tela SVG, puoi salvare l'immagine risultante:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Conclusione

Congratulazioni! Hai disegnato con successo un'immagine raster su un canvas SVG utilizzando Aspose.Imaging per .NET. Questo può essere incredibilmente utile per creare immagini ricche e dinamiche nelle tue applicazioni .NET.

Per maggiori informazioni e documentazione dettagliata, visitare il sito [Documentazione di Aspose.Imaging per .NET](https://reference.aspose.com/imaging/net/).

## Domande frequenti

### Che cos'è Aspose.Imaging per .NET?
   Aspose.Imaging per .NET è una potente libreria di elaborazione delle immagini che consente agli sviluppatori di creare, manipolare e convertire immagini in vari formati all'interno delle applicazioni .NET.

### Posso utilizzare Aspose.Imaging per .NET in progetti commerciali?
   Sì, puoi utilizzare Aspose.Imaging per .NET sia in progetti commerciali che non commerciali. I dettagli sulle licenze sono disponibili su [pagina di acquisto](https://purchase.aspose.com/buy).

### È disponibile una prova gratuita?
   Sì, puoi ottenere una prova gratuita di Aspose.Imaging per .NET da [Qui](https://releases.aspose.com/).

### Dove posso ottenere supporto o porre domande?
   Se hai domande o hai bisogno di supporto, puoi visitare il [Forum di Aspose.Imaging](https://forum.aspose.com/).

### Come posso ottenere una licenza temporanea per Aspose.Imaging per .NET?
   Puoi ottenere una licenza temporanea da [Qui](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}