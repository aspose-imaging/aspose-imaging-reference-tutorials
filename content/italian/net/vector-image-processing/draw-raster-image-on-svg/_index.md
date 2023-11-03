---
title: Come disegnare un'immagine raster su SVG in Aspose.Imaging per .NET
linktitle: Disegna un'immagine raster su SVG in Aspose.Imaging per .NET
second_title: Aspose.Imaging API di elaborazione delle immagini .NET
description: Scopri come disegnare immagini raster su SVG utilizzando Aspose.Imaging per .NET. Migliora le tue applicazioni .NET con immagini dinamiche.
type: docs
weight: 11
url: /it/net/vector-image-processing/draw-raster-image-on-svg/
---

Nel mondo della programmazione .NET, Aspose.Imaging rappresenta una libreria affidabile e versatile per la gestione di varie attività relative alle immagini. Una funzionalità affascinante che offre è la possibilità di disegnare un'immagine raster su una tela SVG. In questa guida passo passo ti guideremo attraverso il processo di disegno di un'immagine raster su un SVG utilizzando Aspose.Imaging per .NET.

## Prerequisiti

Prima di immergerci nei dettagli, assicurati di avere i seguenti prerequisiti:

-  Aspose.Imaging per .NET: è necessario avere la libreria installata. In caso contrario, puoi scaricarlo da[Pagina di download di Aspose.Imaging per .NET](https://releases.aspose.com/imaging/net/).

-  La tua directory dei documenti: sostituisci`"Your Document Directory"` con il percorso effettivo della directory di lavoro.

Ora suddividiamo il processo in passaggi facili da seguire:

## Passaggio 1: importa gli spazi dei nomi necessari

È necessario importare gli spazi dei nomi richiesti per lavorare con Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Passaggio 2: caricare le immagini

- Innanzitutto, carica l'immagine raster che desideri disegnare sulla tela SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Successivamente, carica l'immagine canvas SVG nel punto in cui desideri disegnare l'immagine raster.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Passaggio 3: disegnare sull'immagine SVG

Ora puoi iniziare a disegnare sull'immagine SVG esistente. Per fare ciò, è necessario creare un'istanza di`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Passaggio 4: disegna l'immagine raster

- Definire i limiti in cui si desidera disegnare l'immagine raster e specificare la regione di origine dall'immagine raster.

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

Congratulazioni! Hai disegnato con successo un'immagine raster su una tela SVG utilizzando Aspose.Imaging per .NET. Questo può essere incredibilmente utile per creare immagini ricche e dinamiche all'interno delle tue applicazioni .NET.

 Per ulteriori informazioni e documentazione dettagliata, visitare il[Aspose.Imaging per la documentazione .NET](https://reference.aspose.com/imaging/net/).

## Domande frequenti

### Cos'è Aspose.Imaging per .NET?
   Aspose.Imaging per .NET è una potente libreria di elaborazione delle immagini che consente agli sviluppatori di creare, manipolare e convertire immagini in vari formati all'interno delle applicazioni .NET.

### Posso utilizzare Aspose.Imaging for .NET in progetti commerciali?
    Sì, puoi utilizzare Aspose.Imaging for .NET sia in progetti commerciali che non commerciali. I dettagli della licenza possono essere trovati su[pagina di acquisto](https://purchase.aspose.com/buy).

### È disponibile una prova gratuita?
    Sì, puoi ottenere una prova gratuita di Aspose.Imaging per .NET da[Qui](https://releases.aspose.com/).

### Dove posso ottenere supporto o porre domande?
    Se hai domande o hai bisogno di supporto, puoi visitare il[Forum Aspose.Imaging](https://forum.aspose.com/).

### Come posso ottenere una licenza temporanea per Aspose.Imaging for .NET?
    Puoi ottenere una licenza temporanea da[Qui](https://purchase.aspose.com/temporary-license/).


