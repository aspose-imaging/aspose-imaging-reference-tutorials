---
"date": "2025-06-03"
"description": "Padroneggia la conversione da SVG a PDF con Aspose.Imaging .NET, preservando la qualità dei font. Scopri come impostare le directory, incorporare i font e altro ancora."
"title": "Conversione efficiente da SVG a PDF utilizzando la gestione dei font e le tecniche di Aspose.Imaging .NET"
"url": "/it/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Conversione efficiente da SVG a PDF utilizzando Aspose.Imaging .NET

## Introduzione

Convertire la grafica vettoriale in formati versatili come il PDF è fondamentale per la condivisione e la stampa di documenti nell'era digitale odierna. Mantenere l'integrità dei font durante questa conversione può essere impegnativo. Questo tutorial illustra come convertire SVG in PDF senza problemi, preservando la qualità dei font utilizzando Aspose.Imaging per .NET.

**Cosa imparerai:**
- Impostazione delle directory ed esportazione dei file SVG come PDF.
- Tecniche per incorporare o esportare font nei file SVG.
- Implementazione di un gestore di callback personalizzato per la gestione dei font SVG durante il processo di salvataggio.

Con queste competenze, puoi garantire che i tuoi documenti abbiano un aspetto professionale e coerente su diverse piattaforme. Iniziamo configurando il nostro ambiente!

## Prerequisiti

Prima di immergerti nel codice, assicurati di avere quanto segue:

### Librerie richieste
- **Aspose.Imaging per .NET**: Essenziale per gestire le conversioni delle immagini.
- **Spazio dei nomi System.IO**: Per operazioni su file e directory.

### Configurazione dell'ambiente
Assicurati di avere un ambiente di sviluppo compatibile come Visual Studio o qualsiasi IDE che supporti progetti .NET. La familiarità con la programmazione C# di base è utile.

## Impostazione di Aspose.Imaging per .NET

Per utilizzare Aspose.Imaging nel tuo progetto, segui questi passaggi di installazione:

**Utilizzo della CLI .NET:**
```bash
dotnet add package Aspose.Imaging
```

**Utilizzo del Gestore Pacchetti:**
```powershell
Install-Package Aspose.Imaging
```

**Tramite l'interfaccia utente del gestore pacchetti NuGet:**
Cerca "Aspose.Imaging" e installa la versione più recente.

### Acquisizione della licenza
- **Prova gratuita**: Inizia con una prova gratuita per testare le funzionalità.
- **Licenza temporanea**: Ottieni una licenza temporanea per una valutazione estesa.
- **Acquistare**: Valuta l'acquisto se Aspose.Imaging soddisfa le tue esigenze.

#### Inizializzazione e configurazione
Per utilizzare Aspose.Imaging, aggiungilo come dipendenza al tuo progetto. Ecco una configurazione di base:

```csharp
using Aspose.Imaging;
```

Assicurare il `Aspose.Imaging` namespace è incluso all'inizio del file per accedere alle sue classi e ai suoi metodi.

## Guida all'implementazione

Questa sezione suddivide ciascuna funzionalità in passaggi gestibili.

### Impostazione della directory ed esportazione SVG in PDF

#### Panoramica
Converti un file SVG in un PDF assicurandoti che i percorsi delle directory siano impostati correttamente per l'output.

**Passaggio 1: assicurarsi che la directory di output esista**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*Spiegazione*: Questo frammento di codice controlla se la directory di output esiste e, se necessario, la crea.

**Passaggio 2: carica SVG ed esporta in PDF**
```csharp
public void ReadAndExportToPdf(string inputFileName)
{
    string inputFile = Path.Combine(SourceFolder, inputFileName);
    string outFile = Path.Combine(OutFolder, inputFileName + ".pdf");
    
    using (Image image = Image.Load(inputFile))
    {
        image.Save(outFile,
            new PdfOptions { VectorRasterizationOptions = new SvgRasterizationOptions { PageSize = image.Size } });
    }
}
```
*Spiegazione*: IL `PdfOptions` consentono di configurare la rasterizzazione del contenuto SVG, assicurando che le dimensioni della pagina corrispondano alle dimensioni dell'immagine originale.

### Salvataggio SVG con opzioni di incorporamento dei caratteri

#### Panoramica
Salva un file SVG controllando le impostazioni di incorporamento dei font per mantenere la fedeltà dei font.

**Passaggio 1: definire le directory di output e dei font**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*Spiegazione*: Assicurarsi che le directory siano impostate prima di salvare i file.

**Passaggio 2: salva SVG con opzioni di carattere personalizzate**
```csharp
public void Save(bool useEmbedded, string fileName, int expectedCountFonts)
{
    string fontStoreType = useEmbedded ? "Embedded" : "Stream";
    string inputFile = Path.Combine(SourceFolder, fileName);
    string outFileName = $"{Path.GetFileNameWithoutExtension(fileName)}_{fontStoreType}.svg";
    string outputFile = Path.Combine(OutFolder, outFileName);

    using (Image image = Image.Load(inputFile))
    {
        EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions
        {
            BackgroundColor = Color.White,
            PageWidth = image.Width,
            PageHeight = image.Height
        };

        string testingFileName = Path.GetFileNameWithoutExtension(inputFile);
        string fontFolder = Path.Combine(FontFolder, testingFileName);

        image.Save(outputFile,
            new SvgOptions
            {
                VectorRasterizationOptions = emfRasterizationOptions,
                Callback = new SvgCallbackFontTest(useEmbedded, fontFolder)
                {
                    Link = FontFolderName + "/" + testingFileName
                }
            });
    }

    if (!useEmbedded)
    {
        string[] files = Directory.GetFiles(fontFolder);
        if (files.Length != expectedCountFonts)
        {
            throw new Exception($"Expected count font files = {expectedCountFonts}, Current count font files = {files.Length}");
        }
    }
}
```
*Spiegazione*: Questo metodo consente di specificare se i font devono essere incorporati o trasmessi in streaming, influenzando il modo in cui vengono archiviati e accessibili.

### Gestore di callback dei font SVG personalizzati

#### Panoramica
Implementare un gestore personalizzato per gestire le risorse dei font durante il salvataggio SVG.

**Passaggio 1: implementare la classe SvgCallbackFontTest**
```csharp
public class SvgCallbackFontTest : SvgResourceKeeperCallback
{
    private readonly string outFolder;
    private readonly bool useEmbeddedFont;
    private int fontCounter = 0;

    public string Link { get; set; }

    public SvgCallbackFontTest(bool useEmbeddedFont, string outFolder)
    {
        this.useEmbeddedFont = useEmbeddedFont;
        this.outFolder = outFolder;
        
        if (Directory.Exists(outFolder))
        {
            Directory.Delete(this.outFolder, true);
        }
    }

    public override void OnFontResourceReady(FontStoringArgs args)
    {
        if (this.useEmbeddedFont)
        {
            args.FontStoreType = FontStoreType.Embedded;
        }
        else
        {
            args.FontStoreType = FontStoreType.Stream;
            string fontFolder = this.outFolder;

            if (!Directory.Exists(fontFolder))
            {
                Directory.CreateDirectory(fontFolder);
            }

            string fName = args.SourceFontFileName;
            if (!File.Exists(fName))
            {
                fName = $"font_{this.fontCounter++}.ttf";
            }

            string fileName = Path.Combine(fontFolder, Path.GetFileName(fName));
            
            args.DestFontStream = new FileStream(fileName, FileMode.OpenOrCreate);
            args.DisposeStream = true;
            args.FontFileUri = $".{this.Link}/{Path.GetFileName(fName)}";
        }
    }
}
```
*Spiegazione*: Questa classe gestisce le risorse dei font decidendo se incorporarle direttamente o memorizzarle separatamente. Garantisce che i font siano correttamente referenziati e salvati durante il processo di esportazione SVG.

## Applicazioni pratiche

1. **Generazione automatica di report**: Utilizza Aspose.Imaging per convertire le bozze di progettazione in PDF per una distribuzione uniforme.
2. **Editoria digitale**Garantisci un rendering dei font di alta qualità quando converti articoli con grafica incorporata da SVG a PDF.
3. **Condivisione di documenti multipiattaforma**: Mantenere l'integrità visiva dei documenti condivisi tra diversi sistemi operativi.

## Considerazioni sulle prestazioni

### Suggerimenti per ottimizzare le prestazioni
- Utilizzare pratiche efficienti di gestione dei file, ad esempio eliminando i flussi immediatamente dopo l'uso.
- Ridurre al minimo l'utilizzo della memoria cancellando gli oggetti e le directory non utilizzati una volta completata l'elaborazione.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}