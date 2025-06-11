---
"description": "Převeďte APS do PSD pomocí Aspose.Imaging pro .NET. Zachovávejte vlastnosti vektoru během převodu."
"linktitle": "Převod APS do PSD v Aspose.Imaging pro .NET"
"second_title": "Rozhraní API pro zpracování obrazu Aspose.Imaging .NET"
"title": "Převod APS do PSD pomocí Aspose.Imaging pro .NET"
"url": "/cs/net/advanced-features/convert-aps-to-psd/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Převod APS do PSD pomocí Aspose.Imaging pro .NET

Hledáte způsob, jak snadno převést soubory APS do formátu PSD a zároveň zachovat vektorové vlastnosti? Aspose.Imaging pro .NET vám tento úkol zjednoduší. V tomto podrobném návodu vám ukážeme, jak tohoto převodu dosáhnout. 

## Předpoklady

Než se do procesu pustíme, ujistěte se, že máte splněny následující předpoklady:

1. Knihovna Aspose.Imaging pro .NET: Je třeba si stáhnout a nainstalovat knihovnu Aspose.Imaging pro .NET. Můžete ji získat z [stránka ke stažení](https://releases.aspose.com/imaging/net/).

2. Adresář s dokumenty: Ujistěte se, že máte připravenou cestu k adresáři s dokumenty. Zde se nachází soubor APS.

3. Základní znalost jazyka C#: Znalost programovacího jazyka C# je nezbytná pro implementaci procesu konverze.

## Importovat jmenné prostory

Začněme importem potřebných jmenných prostorů pro práci s Aspose.Imaging pro .NET. Ujistěte se, že jste do projektu přidali odkaz na knihovnu Aspose.Imaging.

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Vectorization;
```

## Krok 1: Načtěte soubor APS

Začněte načtením souboru APS, který chcete převést do formátu PSD. Také zadejte cestu k adresáři dokumentu, kde se soubor APS nachází.

```csharp
string dataDir = "Your Document Directory";
string inputFileName = dataDir + "SimpleShapes.cdr";

using (Image image = Image.Load(inputFileName))
{
    // Váš kód patří sem
}
```

## Krok 2: Konfigurace možností převodu

V tomto kroku je třeba nastavit možnosti převodu pro export souboru APS do formátu PSD. Aspose.Imaging nabízí různé možnosti pro převod vektorových obrázků.

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

Nyní je čas uložit převedený soubor PSD na požadované místo.

```csharp
image.Save(dataDir + "result.psd", imageOptions);
```

## Krok 4: Úklid

Po dokončení převodu můžete chtít odstranit dočasný soubor PSD, který byl během procesu vytvořen.

```csharp
File.Delete(dataDir + "result.psd");
```

## Závěr

Převod APS do formátu PSD pomocí Aspose.Imaging pro .NET je jednoduchý a efektivní. Tato výkonná knihovna umožňuje zachovat vlastnosti vektoru během převodu, což z ní činí cenný nástroj pro grafické designéry i vývojáře.

## Často kladené otázky

### Q1: Je Aspose.Imaging pro .NET bezplatná knihovna?

A1: Aspose.Imaging pro .NET je komerční knihovna. Možnosti licencování si můžete prohlédnout na [stránka nákupu](https://purchase.aspose.com/buy).

### Q2: Mohu si vyzkoušet Aspose.Imaging pro .NET před zakoupením?

A2: Ano, můžete získat bezplatnou zkušební verzi Aspose.Imaging pro .NET z [zkušební stránka](https://releases.aspose.com/imaging/net/).

### Q3: Jaké formáty vektorových obrázků jsou podporovány pro převod do PSD?

A3: Aspose.Imaging pro .NET podporuje převod vektorových obrazových formátů, jako jsou CDR, EMF, EPS, ODG, SVG a WMF, do formátu PSD.

### Q4: Existují nějaká omezení složitosti tvarů během převodu?

A4: Aspose.Imaging v současné době podporuje export nepříliš složitých tvarů bez texturních štětců nebo otevřených tvarů s tahem. Toto by se však mohlo v nadcházejících verzích vylepšit.

### Q5: Kde mohu získat podporu nebo se zeptat na otázky týkající se Aspose.Imaging pro .NET?

A5: Pokud máte jakékoli dotazy nebo potřebujete podporu, můžete navštívit [Fóra Aspose.Imaging](https://forum.aspose.com/) o pomoc.


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}