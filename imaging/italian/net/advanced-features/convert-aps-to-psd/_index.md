---
title: Converti APS in PSD con Aspose.Imaging per .NET
linktitle: Converti APS in PSD in Aspose.Imaging per .NET
second_title: Aspose.Imaging API di elaborazione delle immagini .NET
description: Converti APS in PSD con Aspose.Imaging per .NET. Conserva le proprietà del vettore durante la conversione.
weight: 11
url: /it/net/advanced-features/convert-aps-to-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti APS in PSD con Aspose.Imaging per .NET

Stai cercando di convertire facilmente i file APS in formato PSD preservando le proprietà vettoriali? Aspose.Imaging per .NET è qui per semplificare il tuo compito. In questa guida passo passo ti mostreremo come ottenere questa conversione. 

## Prerequisiti

Prima di approfondire il processo, assicurati di disporre dei seguenti prerequisiti:

1.  Libreria Aspose.Imaging per .NET: è necessario scaricare e installare la libreria Aspose.Imaging per .NET. Puoi ottenerlo da[pagina di download](https://releases.aspose.com/imaging/net/).

2. La tua directory dei documenti: assicurati di avere pronto il percorso della directory dei documenti. Qui è dove si trova il file APS.

3. Conoscenza di base di C#: la familiarità con il linguaggio di programmazione C# è essenziale per implementare il processo di conversione.

## Importa spazi dei nomi

Iniziamo importando gli spazi dei nomi necessari per lavorare con Aspose.Imaging per .NET. Assicurati di aver aggiunto il riferimento alla libreria Aspose.Imaging nel tuo progetto.

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Vectorization;
```

## Passaggio 1: carica il file APS

Inizia caricando il file APS che desideri convertire in PSD. Specificarai inoltre il percorso della directory del documento in cui si trova il file APS.

```csharp
string dataDir = "Your Document Directory";
string inputFileName = dataDir + "SimpleShapes.cdr";

using (Image image = Image.Load(inputFileName))
{
    // Il tuo codice va qui
}
```

## Passaggio 2: configura le opzioni di conversione

In questo passaggio, devi impostare le opzioni di conversione per esportare il file APS nel formato PSD. Aspose.Imaging fornisce varie opzioni per la conversione di immagini vettoriali.

```csharp
PsdOptions imageOptions = new PsdOptions()
{
    VectorRasterizationOptions = new VectorRasterizationOptions(),
    VectorizationOptions = new PsdVectorizationOptions()
    {
        VectorDataCompositionMode = VectorDataCompositionMode.SeparateLayers
    }
};

imageOptions.VectorRasterizationOptions.PageWidth = image.Width;
imageOptions.VectorRasterizationOptions.PageHeight = image.Height;
```

## Passaggio 3: salva il file PSD

Ora è il momento di salvare il file PSD convertito nella posizione desiderata.

```csharp
image.Save(dataDir + "result.psd", imageOptions);
```

## Passaggio 4: pulizia

Una volta completata la conversione, potresti voler eliminare il file PSD temporaneo creato durante il processo.

```csharp
File.Delete(dataDir + "result.psd");
```

## Conclusione

La conversione del formato APS in PSD con Aspose.Imaging per .NET è semplice ed efficiente. Questa potente libreria ti consente di mantenere le proprietà del vettore durante la conversione, rendendola uno strumento prezioso sia per i grafici che per gli sviluppatori.

## Domande frequenti

### Q1: Aspose.Imaging per .NET è una libreria gratuita?

 A1: Aspose.Imaging per .NET è una libreria commerciale. Puoi esplorare le opzioni di licenza su[pagina di acquisto](https://purchase.aspose.com/buy).

### Q2: Posso provare Aspose.Imaging for .NET prima di acquistarlo?

 R2: Sì, puoi ottenere una prova gratuita di Aspose.Imaging per .NET da[pagina di prova](https://releases.aspose.com/imaging/net/).

### Q3: Quali formati di immagini vettoriali sono supportati per la conversione in PSD?

A3: Aspose.Imaging per .NET supporta la conversione di formati di immagini vettoriali come CDR, EMF, EPS, ODG, SVG e WMF nel formato PSD.

### Q4: Esistono limitazioni alla complessità delle forme durante la conversione?

R4: Attualmente Aspose.Imaging supporta l'esportazione di forme non molto complesse senza pennelli texture o forme aperte con tratto. Tuttavia, questo potrebbe essere migliorato nelle prossime versioni.

### Q5: Dove posso ottenere supporto o porre domande relative ad Aspose.Imaging per .NET?

 R5: Se hai domande o hai bisogno di supporto, puoi visitare il[Forum Aspose.Imaging](https://forum.aspose.com/)per assistenza.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
