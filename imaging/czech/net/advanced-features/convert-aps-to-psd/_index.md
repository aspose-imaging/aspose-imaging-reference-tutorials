---
title: Převeďte APS na PSD pomocí Aspose.Imaging pro .NET
linktitle: Převeďte APS na PSD v Aspose.Imaging pro .NET
second_title: Aspose.Imaging .NET Image Processing API
description: Převeďte APS na PSD pomocí Aspose.Imaging pro .NET. Zachovat vlastnosti vektoru během převodu.
type: docs
weight: 11
url: /cs/net/advanced-features/convert-aps-to-psd/
---
Chcete bez námahy převést soubory APS do formátu PSD při zachování vektorových vlastností? Aspose.Imaging pro .NET je zde pro zjednodušení vašeho úkolu. V tomto podrobném průvodci vám ukážeme, jak této konverze dosáhnout. 

## Předpoklady

Než se pustíme do procesu, ujistěte se, že máte splněny následující předpoklady:

1.  Knihovna Aspose.Imaging pro .NET: Musíte si stáhnout a nainstalovat knihovnu Aspose.Imaging pro .NET. Můžete jej získat z[stránka ke stažení](https://releases.aspose.com/imaging/net/).

2. Váš adresář dokumentů: Ujistěte se, že máte připravenou cestu k adresáři dokumentů. Zde se nachází soubor APS.

3. Základní znalost C#: Pro implementaci procesu převodu je nezbytná znalost programovacího jazyka C#.

## Importovat jmenné prostory

Začněme importem potřebných jmenných prostorů pro práci s Aspose.Imaging pro .NET. Ujistěte se, že jste do projektu přidali odkaz na knihovnu Aspose.Imaging.

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Vectorization;
```

## Krok 1: Načtěte soubor APS

Začněte načtením souboru APS, který chcete převést na PSD. Zadáte také cestu k adresáři dokumentů, kde je umístěn soubor APS.

```csharp
string dataDir = "Your Document Directory";
string inputFileName = dataDir + "SimpleShapes.cdr";

using (Image image = Image.Load(inputFileName))
{
    // Váš kód je zde
}
```

## Krok 2: Nakonfigurujte možnosti převodu

V tomto kroku je potřeba nastavit možnosti převodu pro export souboru APS do formátu PSD. Aspose.Imaging poskytuje různé možnosti pro převod vektorových obrázků.

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

## Krok 3: Uložte soubor PSD

Nyní je čas uložit převedený soubor PSD do požadovaného umístění.

```csharp
image.Save(dataDir + "result.psd", imageOptions);
```

## Krok 4: Vyčistěte

Po dokončení převodu můžete chtít odstranit dočasný soubor PSD, který byl vytvořen během procesu.

```csharp
File.Delete(dataDir + "result.psd");
```

## Závěr

Převod APS do formátu PSD pomocí Aspose.Imaging pro .NET je přímočarý a efektivní. Tato výkonná knihovna umožňuje zachovat vektorové vlastnosti během převodu, což z ní činí cenný nástroj pro grafické designéry i vývojáře.

## FAQ

### Q1: Je Aspose.Imaging for .NET bezplatná knihovna?

 A1: Aspose.Imaging for .NET je komerční knihovna. Možnosti licencování můžete prozkoumat na[nákupní stránku](https://purchase.aspose.com/buy).

### Q2: Mohu vyzkoušet Aspose.Imaging pro .NET před jeho zakoupením?

 A2: Ano, můžete získat bezplatnou zkušební verzi Aspose.Imaging pro .NET z[zkušební stránka](https://releases.aspose.com/imaging/net/).

### Q3: Jaké formáty vektorových obrázků jsou podporovány pro převod do PSD?

Odpověď 3: Aspose.Imaging for .NET podporuje převod formátů vektorových obrázků, jako jsou CDR, EMF, EPS, ODG, SVG a WMF, do formátu PSD.

### Q4: Existují nějaká omezení složitosti tvarů během převodu?

A4: V současné době Aspose.Imaging podporuje export nepříliš složitých tvarů bez texturových štětců nebo otevřených tvarů s tahem. To však může být v nadcházejících verzích vylepšeno.

### Q5: Kde mohu získat podporu nebo klást otázky týkající se Aspose.Imaging pro .NET?

 A5: Pokud máte nějaké dotazy nebo potřebujete podporu, můžete navštívit stránku[Aspose.Imaging fóra](https://forum.aspose.com/)pro pomoc.
