---
date: '2026-02-09'
description: Scopri come convertire JPEG in TIFF e creare immagini TIFF multi‑frame
  con Aspose.Imaging per .NET. Include l'installazione, la configurazione di TiffOptions,
  il caricamento delle immagini da una cartella e la gestione dei frame.
keywords:
- create multi-frame tiff images
- Aspose.Imaging for .NET tutorial
- configure TiffOptions in .NET
title: Come convertire JPEG in TIFF e creare immagini TIFF multi-frame con Aspose.Imaging
  per .NET
url: /it/net/animation-multi-frame-images/create-multi-frame-tiff-images-aspose-imaging-dotnet/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Come Convertire JPEG in TIFF e Creare Immagini TIFF Multi-Frame con Aspose.Imaging per .NET

## Introduzione

Stai cercando di padroneggiare l'arte di **convertire JPEG in TIFF** e allo stesso tempo creare file TIFF multi‑frame usando Aspose.Imaging per .NET? Questo tutorial completo ti guiderà nella configurazione dell'ambiente, nella configurazione di `TiffOptions`, nel ridimensionamento dei file JPEG e nell'aggiunta di frame a un'immagine TIFF—tutto con facilità. Che tu stia gestendo archivi di documenti o integrando imaging di alta qualità in applicazioni software, questa guida è pensata per migliorare il tuo flusso di lavoro.

**Ciò che imparerai:**
- Come configurare Aspose.Imaging per .NET
- Configurare `TiffOptions` per immagini in bianco‑nero usando la compressione CCITT Fax Group 3
- Caricare e ridimensionare file JPEG da una directory
- Aggiungere frame a un'immagine TIFF
- Salvare immagini TIFF multi‑frame

Iniziamo con i prerequisiti per cominciare.

## Risposte Rapide
- **Cosa significa “convertire JPEG in TIFF”?** Significa prendere un'immagine raster JPEG e salvarla nel formato TIFF, spesso con compressione personalizzata o più frame.  
- **Quale libreria gestisce meglio questo in .NET?** Aspose.Imaging per .NET fornisce un'API ricca per conversione, ridimensionamento e creazione multi‑frame.  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per la valutazione; una licenza permanente rimuove tutte le limitazioni di valutazione.  
- **Posso caricare le immagini da una directory automaticamente?** Sì – il tutorial mostra come enumerare i file JPEG e processarli uno per uno.  
- **Il codice è compatibile con .NET 6+?** Assolutamente – il campione utilizza le API .NET Core/5+ che funzionano su .NET 6 e versioni successive.

## Cos'è “convertire JPEG in TIFF”?
Convertire JPEG in TIFF comporta la decodifica di un file JPEG, l'eventuale trasformazione (ad esempio ridimensionamento o cambio di profondità di colore) e quindi la codifica del risultato come file TIFF. TIFF supporta più frame, compressione senza perdita e metadati che JPEG non possiede, rendendolo ideale per scenari di archiviazione e multi‑pagina.

## Perché usare Aspose.Imaging per questa conversione?
- **Controllo totale** su compressione, interpretazione fotometrica e formato pixel.  
- **Supporto multi‑frame** – è possibile raggruppare diverse pagine JPEG in un unico documento TIFF.  
- **Cross‑platform** – funziona su Windows, Linux e macOS con .NET Core/5+.  
- **Nessuna dipendenza esterna** – codice gestito puro, senza DLL native.

## Prerequisiti

Prima di immergerti nella creazione di immagini TIFF con Aspose.Imaging, assicurati di avere quanto segue:

### Librerie e Dipendenze Richieste
- **Aspose.Imaging per .NET**: Installa questa libreria tramite NuGet o il tuo gestore di pacchetti preferito.
  
### Requisiti di Configurazione dell'Ambiente
- Un ambiente di sviluppo che supporti C# e .NET Core/5+  
  
### Prerequisiti di Conoscenza
- Comprensione di base dei concetti di programmazione C#  
- Familiarità con la gestione di file immagine in .NET  

## Configurare Aspose.Imaging per .NET

Per iniziare, devi installare Aspose.Imaging. Ecco come:

**.NET CLI**
```shell
dotnet add package Aspose.Imaging
```

**Package Manager**
```powershell
Install-Package Aspose.Imaging
```

**NuGet Package Manager UI**  
Cerca "Aspose.Imaging" e installa l'ultima versione.

### Passaggi per Ottenere la Licenza
- **Prova Gratuita**: Accedi a una versione a funzionalità limitata per testare le caratteristiche.  
- **Licenza Temporanea**: Ottienila per una prova estesa senza limitazioni di valutazione. Visita [Temporary License](https://purchase.aspose.com/temporary-license/).  
- **Acquisto**: Per accesso completo, considera l'acquisto di una licenza su [Purchase Aspose.Imaging](https://purchase.aspose.com/buy).

### Inizializzazione e Configurazione di Base

```csharp
// Initialize the library with your license
Aspose.Imaging.License license = new Aspose.Imaging.License();
license.SetLicense("Path to your license file");
```

## Come Convertire JPEG in TIFF e Aggiungere Più Frame

Dividiamo l'implementazione in sezioni gestibili.

### Creare e Configurare TiffOptions per l'Immagine TIFF

#### Panoramica
Creare un oggetto `TiffOptions` ti consente di definire impostazioni come compressione e interpretazione fotometrica, essenziali per personalizzare i file TIFF.

#### Implementazione Passo‑per‑Passo

**1. Importare gli Spazi dei Nomi Necessari**  
Assicurati di includere questi namespace nel tuo file:

```csharp
using Aspose.Imaging.FileFormats.Tiff;
using Aspose.Imaging.FileFormats.Tiff.Enums;
using Aspose.Imaging.ImageOptions;
```

**2. Configurare TiffOptions**  
Imposta l'oggetto `TiffOptions` con configurazioni specifiche per un'immagine in bianco‑nero usando la compressione CCITT Fax Group 3.

```csharp
// Create TiffOptions with default settings
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);

// Set bits per sample to 1 (black and white)
outputSettings.BitsPerSample = new ushort[] { 1 };

// Use CCITT Fax Group 3 compression
outputSettings.Compression = TiffCompressions.CcittFax3;

// Define photometric interpretation as MinIsWhite
outputSettings.Photometric = TiffPhotometrics.MinIsWhite;

// Set source to an empty stream for creating new TIFF from scratch
outputSettings.Source = new Aspose.Imaging.Sources.StreamSource(new System.IO.MemoryStream());
```

### Creare e Configurare TiffImage con Dimensioni Specifiche

#### Panoramica
Creare un `TiffImage` comporta l'impostazione di dimensioni personalizzate, fondamentale quando si definisce la grandezza di ogni frame TIFF.

**1. Definire le Dimensioni dell'Immagine**

```csharp
int newWidth = 500; // Width for each TIFF frame
int newHeight = 500; // Height for each TIFF frame
string path = "@YOUR_OUTPUT_DIRECTORY\\AddFramesToTIFFImage_out.tif";
```

**2. Creare un'Istanza di TiffImage**  
Inizializza il `TiffImage` con le dimensioni specificate e le impostazioni di output.

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    // Logic to add frames will be added here.
}
```

### Caricare File JPEG da una Directory e Ridimensionarli

#### Panoramica
Caricare immagini JPEG, ridimensionarle e prepararle per l'inclusione in un file TIFF è semplificato con Aspose.Imaging.

**1. Caricare le Immagini JPEG**

```csharp
string dataDir = "@YOUR_DOCUMENT_DIRECTORY"; // Directory containing input images

foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
{
    using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
    {
        // Resize image to match TIFF frame dimensions
        ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
        
        // Additional logic for handling multiple frames will be added here.
    }
}
```

> **Suggerimento professionale:** La frase **load images from directory** è esattamente ciò che il ciclo sopra fa – enumera ogni file JPEG nella cartella di destinazione.

### Aggiungere un Frame a TiffImage e Salvarlo

#### Panoramica
Aggiungere frame a un'immagine TIFF comporta copiare i pixel JPEG ridimensionati in ciascun frame e salvare il TIFF multi‑frame completo.

**1. Inizializzare l'Istanza di TiffImage**

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    int index = 0; // Frame index tracker
    
    foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
    {
        using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
        {
            ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
            
            TiffFrame frame = tiffImage.ActiveFrame;
            if (index > 0)
            {
                // Create a new frame for each subsequent image
                frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            }
            
            // Copy pixels from the resized JPEG into the TIFF frame
            frame.SavePixels(frame.Bounds, ri.LoadPixels(ri.Bounds));
            if (index > 0)
            {
                tiffImage.AddFrame(frame); // Add to TIFF image only after the first frame
            }
            index++;
        }
    }
    
    tiffImage.Save(path); // Save the final TIFF with all frames
}
```

## Applicazioni Pratiche

Ecco alcuni casi d'uso reali per la creazione di immagini TIFF multi‑frame:

1. **Archiviazione Documenti** – Conserva documenti scannerizzati in un unico file TIFF per garantire integrità dei dati e facilità di accesso.  
2. **Imaging Medico** – Usa formati TIFF di alta qualità e compressi per memorizzare scansioni come MRI e CT.  
3. **Design Grafico** – Combina più livelli di design in un unico file per una gestione efficiente nei software grafici.  
4. **Fotografia** – Archivia album fotografici multi‑pagina come file singoli per una condivisione e conservazione semplificate.  
5. **Controllo Qualità Industriale** – Registra dati di ispezione dettagliati su più frame in un'immagine TIFF.

## Considerazioni sulle Prestazioni

### Suggerimenti per Ottimizzare le Prestazioni
- **Gestione della Memoria** – Elimina prontamente gli oggetti immagine (`using` statements) per liberare risorse.  
- **Elaborazione a Lotti** – Processa le immagini in batch se lavori con grandi dataset per mantenere prevedibile l'uso della memoria.  
- **Compressione Efficiente** – Scegli impostazioni di compressione che bilancino qualità e velocità per il tuo scenario.

## Domande Frequenti

**D: Posso convertire JPEG in TIFF senza perdere qualità?**  
R: Sì. Utilizzando opzioni di compressione senza perdita (ad esempio LZW o CCITT Fax) e preservando i dati pixel originali, la conversione può essere senza perdita.

**D: È necessario ridimensionare le immagini prima di aggiungerle come frame?**  
R: Tutti i frame in un TIFF devono condividere le stesse dimensioni, quindi è necessario ridimensionare ogni JPEG alla larghezza e altezza target.

**D: Quanti frame può contenere un file TIFF?**  
R: Praticamente illimitati; il limite è determinato dalla dimensione del file e dalla memoria disponibile.

**D: Il TIFF generato è compatibile con i visualizzatori comuni?**  
R: L'esempio utilizza la compressione standard CCITT Fax Group 3, ampiamente supportata dalla maggior parte dei visualizzatori e editor TIFF.

**D: E se volessi aggiungere una compressione diversa per immagini a colori?**  
R: Sostituisci `TiffCompressions.CcittFax3` con `TiffCompressions.Lzw` o `TiffCompressions.Jpeg` e regola `BitsPerSample` di conseguenza.

## Conclusione

Questo tutorial ha coperto i passaggi essenziali per **convertire JPEG in TIFF** e creare immagini TIFF multi‑frame usando Aspose.Imaging per .NET. Dalla configurazione di `TiffOptions` all'aggiunta di frame, ora disponi di una solida base per integrare imaging di alta qualità nelle tue applicazioni.

**Passi Successivi**  
- Sperimenta con altri tipi di compressione e profondità di colore.  
- Esplora funzionalità aggiuntive di Aspose.Imaging come la gestione dei metadati o la conversione PDF.  
- Consulta la [documentazione ufficiale](https://reference.aspose.com/imaging/net/) per approfondimenti più dettagliati.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo Aggiornamento:** 2026-02-09  
**Testato Con:** Aspose.Imaging per .NET (ultima versione stabile)  
**Autore:** Aspose