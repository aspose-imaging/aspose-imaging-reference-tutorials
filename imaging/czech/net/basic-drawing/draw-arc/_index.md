---
date: 2026-02-09
description: Naučte se, jak pomocí Aspose.Imaging pro .NET kreslit oblouk, včetně
  toho, jak uložit soubor BMP, nastavit velikost obrázku a nastavit pozadí grafiky.
  Krok za krokem průvodce tvorbou BMP obrázků.
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Jak nakreslit oblouk pomocí Aspose.Imaging pro .NET
url: /cs/net/basic-drawing/draw-arc/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Jak nakreslit oblouk pomocí Aspose.Imaging pro .NET

Ve světě zpracování obrazu je **how to draw arc** běžný úkol, který může dodat vizuální šmrnc jakémukoli grafickému prvku. S Aspose.Imaging pro .NET můžete generovat BMP obrázky, nastavit velikost obrázku a nakreslit oblouk pomocí pera během několika řádků C#. Na konci tohoto tutoriálu budete přesně vědět, jak nakreslit oblouk, nastavit pozadí grafiky a snadno uložit výsledný BMP soubor.

## Rychlé odpovědi
- **What does the code produce?** 100 × 100 pixel BMP obrázek se žlutým pozadím a černým obloukem.  
- **Which library is used?** Aspose.Imaging pro .NET.  
- **Do I need a license?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Can I change the image size?** Ano – upravte parametry šířky a výšky ve volání `Image.Create`.  
- **Is the output format fixed?** Příklad ukládá BMP soubor, ale lze použít libovolný formát podporovaný Aspose.Imaging.

## Co je “how to draw arc” v Aspose.Imaging?
Nakreslení oblouku znamená vykreslení zakřiveného úseku definovaného ohraničujícím obdélníkem, počátečním úhlem a úhlem úseku. Aspose.Imaging poskytuje metodu `Graphics.DrawArc`, která vám umožní **draw arc with pen** a ovládat každý vizuální aspekt.

## Proč použít Aspose.Imaging pro tento úkol?
- **Full control** nad rozměry obrázku, barevnou hloubkou a formátem souboru.  
- **No external dependencies** – vše běží na čistém .NET.  
- **High performance** pro generování velkého množství grafiky na serverové straně.  

## Požadavky

Než se ponoříme do kódu, ujistěte se, že máte následující:

1. **Aspose.Imaging for .NET** – stáhněte jej z oficiálního webu [zde](https://releases.aspose.com/imaging/net/).  
2. **A .NET development environment** (Visual Studio, VS Code nebo jakýkoli C# kompilátor).  

Nyní, když máme požadavky připravené, pojďme začít kreslit!

## Importování potřebných jmenných prostorů

Pro práci s Aspose.Imaging musíte do rozsahu přinést příslušné jmenné prostory:

### Krok 1: Importujte jmenné prostory

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

Tyto `using` příkazy vám poskytují přístup ke třídám pro tvorbu obrázků, práci s grafikou a souborovým I/O.

## Jak nakreslit oblouk pomocí Aspose.Imaging pro .NET

Rozdělíme proces do tří jasných kroků: vytvořit obrázek, připravit grafický povrch a nakonec nakreslit oblouk.

### Krok 1: Nastavení obrázku (nastavit velikost obrázku a vygenerovat BMP obrázek)

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

Zde **set image size** na 100 × 100 pixelů a nakonfigurujeme BMP možnosti. `FileStream` zajišťuje, že **save BMP file** do požadovaného umístění.

### Krok 2: Inicializace Graphics a nastavení pozadí grafiky

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

`Graphics` objekt nám umožňuje kreslit na obrázek. Voláním `Clear(Color.Yellow)` **set graphics background** na jasně žlutou, což způsobí, že oblouk bude výrazný.

### Krok 3: Definování parametrů oblouku a nakreslení oblouku pomocí pera

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

- `width` a `height` definují ohraničující obdélník, což v podstatě **set image size** pro oblouk.  
- Objekt `Pen` je to, co nám umožňuje **draw arc with pen** černě.  
- Po nakreslení `image.Save()` zapíše **BMP file** na disk.

## Časté problémy a tipy

- **Arc not visible?** Ujistěte se, že barva pera kontrastuje s pozadím (např. černá na žluté).  
- **Incorrect dimensions?** Pamatujte, že ohraničující obdélník oblouku může být větší než obrázek; podle toho upravte `width`/`height` nebo velikost obrázku.  
- **Performance tip:** Znovu použijte jedinou instanci `Graphics`, pokud potřebujete nakreslit více tvarů na stejný obrázek.

## Často kladené otázky

### Q1: Kde najdu dokumentaci pro Aspose.Imaging pro .NET?

A1: Dokumentaci můžete najít [zde](https://reference.aspose.com/imaging/net/) pro komplexní informace o Aspose.Imaging pro .NET.

### Q2: Jak si mohu stáhnout Aspose.Imaging pro .NET?

A2: Aspose.Imaging pro .NET si můžete stáhnout z webu [zde](https://releases.aspose.com/imaging/net/).

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.Imaging pro .NET?

A3: Ano, bezplatnou zkušební verzi získáte [zde](https://releases.aspose.com/) a můžete vyzkoušet Aspose.Imaging pro .NET.

### Q4: Potřebuji dočasnou licenci pro Aspose.Imaging pro .NET?

A4: Pokud potřebujete dočasnou licenci, můžete ji získat [zde](https://purchase.aspose.com/temporary-license/).

### Q5: Kde mohu získat podporu nebo klást otázky ohledně Aspose.Imaging pro .NET?

A5: Fórum Aspose.Imaging můžete navštívit pro podporu a diskuze [zde](https://forum.aspose.com/).

---

**Poslední aktualizace:** 2026-02-09  
**Testováno s:** Aspose.Imaging 24.11 pro .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}