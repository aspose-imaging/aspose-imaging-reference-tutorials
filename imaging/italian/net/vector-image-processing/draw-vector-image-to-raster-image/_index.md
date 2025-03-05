---
title: Disegna un'immagine vettoriale in un'immagine raster in Aspose.Imaging per .NET
linktitle: Disegna un'immagine vettoriale in un'immagine raster in Aspose.Imaging per .NET
second_title: Aspose.Imaging API di elaborazione delle immagini .NET
description: Scopri come convertire immagini vettoriali in immagini raster in .NET utilizzando Aspose.Imaging. Una guida passo passo per un'elaborazione efficiente delle immagini.
type: docs
weight: 13
url: /it/net/vector-image-processing/draw-vector-image-to-raster-image/
---

Stai cercando di convertire immagini vettoriali in immagini raster senza sforzo nelle tue applicazioni .NET? Aspose.Imaging per .NET fornisce una soluzione efficiente per questo compito. In questa guida passo passo, ti guideremo attraverso il processo di disegno di immagini vettoriali in immagini raster utilizzando Aspose.Imaging per .NET. 

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di disporre dei seguenti prerequisiti:

### 1. Aspose.Imaging per .NET

 Dovresti avere Aspose.Imaging per .NET installato. Se non ce l'hai, puoi scaricarlo dal sito web all'indirizzo[Scarica Aspose.Imaging per .NET](https://releases.aspose.com/imaging/net/).

### 2. Ambiente di sviluppo .NET

Assicurati di avere un ambiente di sviluppo .NET configurato sul tuo computer. È possibile utilizzare Visual Studio o qualsiasi altro strumento di sviluppo .NET.

Ora, suddividiamo il processo di disegno di immagini vettoriali in immagini raster in passaggi semplici e facili da seguire:

## Passaggio 1: inizializza il tuo progetto

Inizia creando un nuovo progetto .NET nel tuo ambiente di sviluppo. Assicurati di avere Aspose.Imaging per .NET integrato nel tuo progetto.

## Passaggio 2: carica l'immagine vettoriale

In questo passaggio carichiamo l'immagine vettoriale (in formato SVG) che desideri convertire in immagine raster.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## Passaggio 3: rasterizza l'immagine vettoriale

Ora dobbiamo rasterizzare l'immagine SVG nel formato PNG. È qui che avviene la conversione da vettoriale a raster.

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## Passaggio 4: caricare l'immagine raster

Dopo la rasterizzazione, carica l'immagine PNG dallo stream per ulteriori disegni.

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## Passaggio 5: disegna l'immagine raster

Ora possiamo disegnare l'immagine raster sull'immagine SVG esistente.

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## Passaggio 6: salva il risultato

Infine, salva l'immagine del risultato. Ora hai un'immagine raster che include la tua immagine vettoriale.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## Conclusione

In questo tutorial, abbiamo dimostrato come convertire immagini vettoriali in immagini raster utilizzando Aspose.Imaging per .NET. Con questi semplici passaggi puoi integrare facilmente questa funzionalità nelle tue applicazioni .NET.

### Domande frequenti

### Cos'è Aspose.Imaging per .NET?
Aspose.Imaging per .NET è una libreria .NET che fornisce potenti funzionalità di elaborazione delle immagini, inclusa la possibilità di lavorare con vari formati di immagine, convertire immagini ed eseguire attività avanzate di manipolazione delle immagini.

### Dove posso trovare la documentazione per Aspose.Imaging per .NET?
 È possibile trovare la documentazione per Aspose.Imaging per .NET[Qui](https://reference.aspose.com/imaging/net/).

### È disponibile una versione di prova gratuita?
 Sì, puoi accedere a una prova gratuita di Aspose.Imaging per .NET[Qui](https://releases.aspose.com/).

### Come posso ottenere una licenza temporanea per Aspose.Imaging per .NET?
 Se hai bisogno di una licenza temporanea, puoi ottenerne una[Qui](https://purchase.aspose.com/temporary-license/).

### Dove posso ottenere supporto per Aspose.Imaging per .NET?
 Per qualsiasi supporto o domanda, puoi visitare il[Forum Aspose.Imaging](https://forum.aspose.com/).
