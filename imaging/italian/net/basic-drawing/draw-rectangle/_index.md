---
date: 2026-02-12
description: Scopri come creare un'immagine vuota con Aspose e come disegnare un rettangolo
  in .NET con Aspose.Imaging – una guida rapida per la manipolazione delle immagini
  nelle tue applicazioni .NET.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Crea immagine vuota Aspose – Disegna rettangoli in .NET
url: /it/net/basic-drawing/draw-rectangle/
weight: 14
---

 keep code block placeholders unchanged.

Also ensure markdown tables keep pipe formatting.

Now craft final answer.{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Crea Immagine Vuota Aspose – Disegna Rettangoli in .NET

Creare e manipolare immagini nelle applicazioni .NET può sembrare impegnativo, ma con Aspose.Imaging è possibile **creare un'immagine vuota Aspose** in poche righe di codice e poi disegnare forme su di essa. In questo tutorial percorreremo l'intero processo — dalla configurazione di una tela vuota al disegno dei rettangoli—così potrai iniziare ad aggiungere grafiche ai tuoi progetti .NET subito.

## Risposte Rapide
- **Cosa significa “create blank image Aspose”?** Significa generare un bitmap vuoto usando l'API Aspose.Imaging.  
- **Come disegnare un rettangolo .net con Aspose?** Usa il metodo `Graphics.DrawRectangle` dopo aver inizializzato un oggetto `Graphics`.  
- **Quale pacchetto NuGet è necessario?** `Aspose.Imaging` (ultima versione).  
- **Posso salvare l'immagine come PNG, JPEG o BMP?** Sì – basta cambiare le opzioni dell'immagine (ad es., `BmpOptions`, `JpegOptions`).  
- **È necessaria una licenza per lo sviluppo?** Una prova gratuita è sufficiente per la valutazione; è necessaria una licenza commerciale per la produzione.

## Cos'è “create blank image Aspose”?
Creare un'immagine vuota significa allocare un buffer di pixel con larghezza, altezza e formato pixel definiti. Aspose.Imaging gestisce i dettagli a basso livello, fornendoti una tela pronta per il disegno senza dover gestire GDI+ o System.Drawing.

## Perché usare Aspose.Imaging per disegnare rettangoli in .NET?
- **Cross‑platform** – funziona su Windows, Linux e macOS.  
- **Nessuna dipendenza nativa** – codice gestito puro, perfetto per ambienti server.  
- **API di disegno ricca** – supporta penne, pennelli, anti‑aliasing e molti tipi di forme.  
- **Alte prestazioni** – ottimizzato per immagini di grandi dimensioni e elaborazione batch.

## Prerequisiti

1. **Aspose.Imaging per .NET** – scaricalo dalla [pagina di download](https://releases.aspose.com/imaging/net/).  
2. **Ambiente di sviluppo** – Visual Studio, VS Code o qualsiasi IDE compatibile con .NET.  
3. **Runtime .NET** – .NET 6+ o .NET Framework 4.7.2+.  

Ora che abbiamo tutto configurato, immergiamoci nel codice.

## Come creare un'immagine vuota Aspose in .NET?

### Passo 1: Importa gli spazi dei nomi richiesti

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Questi spazi dei nomi ti danno accesso alle classi di imaging di base, ai tipi di pennello e alle opzioni di salvataggio dell'immagine.

### Passo 2: Crea un'immagine vuota (la tela)

```csharp
string dataDir = "Your Document Directory";  // Set the path to your document directory
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Your drawing code will go here
        image.Save();
    }
}
```

In questo blocco facciamo:
* Definiamo la posizione di output (`dataDir`).  
* Configuriamo `BmpOptions` per usare un formato pixel a 32‑bit.  
* Creiamo un'**immagine vuota** di 100 × 100 pixel.  

### Passo 3: Come disegnare un rettangolo .net con Aspose.Imaging

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` riempie la tela con un colore di sfondo (giallo in questo esempio).  
* `DrawRectangle` disegna due rettangoli — uno con una penna rossa semplice, un altro con un pennello solido blu — per contrasto visivo.

### Passo 4: Salva l'immagine

```csharp
image.Save();
```

Chiamare `Save` scrive il bitmap nel file system usando le opzioni definite in precedenza.

## Problemi Comuni & Suggerimenti

| Problema | Motivo | Correzione |
|----------|--------|------------|
| **L'immagine vuota appare nera** | Sfondo non cancellato | Chiama `graphic.Clear(Color.YourColor)` prima di disegnare. |
| **Eccezione file non trovato** | `dataDir` punta a una cartella inesistente | Assicurati che la directory esista o usa `Path.Combine` con `Environment.CurrentDirectory`. |
| **Colori errati** | Uso di `System.Drawing.Color` invece di `Aspose.Imaging.Color` | Importa sempre `Aspose.Imaging.Color`. |
| **Ritardo di prestazioni su immagini grandi** | Uso delle `BmpOptions` predefinite con alto bit-per-pixel | Passa a `JpegOptions` o `PngOptions` per la compressione. |

## Domande Frequenti (Estese)

**D: Posso disegnare altre forme oltre ai rettangoli?**  
**R:** Assolutamente. Aspose.Imaging fornisce metodi come `DrawEllipse`, `DrawLine` e `DrawPolygon`.

**D: La libreria è gratuita per uso commerciale?**  
**R:** No, Aspose.Imaging è un prodotto commerciale, ma è possibile valutarlo con una prova gratuita disponibile [qui](https://releases.aspose.com/).

**D: Funziona sia su Windows che su applicazioni web?**  
**R:** Sì, lo stesso codice funziona in ASP.NET, Blazor e applicazioni console.

**D: Come cambio il formato di output in PNG?**  
**R:** Sostituisci `BmpOptions` con `PngOptions` e regola l'estensione del file di conseguenza.

**D: Dove posso trovare una documentazione più dettagliata?**  
**R:** Accedi al riferimento completo dell'API [qui](https://reference.aspose.com/imaging/net/) e unisciti alla community sul [forum Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2026-02-12  
**Testato con:** Aspose.Imaging 24.12 per .NET  
**Autore:** Aspose