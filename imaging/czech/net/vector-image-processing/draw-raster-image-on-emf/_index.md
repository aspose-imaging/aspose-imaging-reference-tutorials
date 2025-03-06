---
title: Kreslení rastrových obrázků na EMF pomocí Aspose.Imaging pro .NET
linktitle: Kreslit rastrový obrázek na EMF v Aspose.Imaging pro .NET
second_title: Aspose.Imaging .NET Image Processing API
description: Naučte se kreslit rastrové obrázky do souborů EMF pomocí Aspose.Imaging for .NET. Vytvářejte úžasné vizuály bez námahy.
weight: 10
url: /cs/net/vector-image-processing/draw-raster-image-on-emf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kreslení rastrových obrázků na EMF pomocí Aspose.Imaging pro .NET


## Úvod

Vítejte v tomto podrobném návodu, jak nakreslit rastrový obrázek na EMF (Enhanced Metafile) pomocí Aspose.Imaging pro .NET. Aspose.Imaging je výkonná knihovna, která vám umožňuje pracovat s různými formáty obrázků ve vašich aplikacích .NET. V tomto tutoriálu vás provedeme procesem kreslení rastrového obrázku do souboru EMF. Dozvíte se, jak importovat potřebné jmenné prostory, a každý příklad rozdělíme do několika kroků, abychom proces učení usnadnili.

Začněme!

## Předpoklady

Než se pustíme do výukového programu, měli byste mít splněny následující předpoklady:

1. Visual Studio: Abyste mohli psát a spouštět kód .NET, musíte mít na svém počítači nainstalované Visual Studio.

2.  Aspose.Imaging pro .NET: Ujistěte se, že máte nainstalovaný Aspose.Imaging pro .NET. Můžete si jej stáhnout z[tady](https://releases.aspose.com/imaging/net/).

3. Rastrový obrázek: Připravte si rastrový obrázek (např. soubor PNG), který chcete nakreslit do souboru EMF.

## Importovat jmenné prostory

Ve svém projektu Visual Studio budete muset importovat potřebné obory názvů, abyste mohli pracovat s Aspose.Imaging. Přidejte do souboru kódu následující jmenné prostory:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Emf;
using Aspose.Imaging.FileFormats.Png;
using Aspose.Imaging.Graphics;
using System;
```

Nyní, když máme předpoklady a jmenné prostory, rozdělme příklad do několika kroků.

## Krok 1: Načtěte obrázek, který chcete nakreslit

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
{
    // Zde je váš kód pro krok 1
}
```

 V tomto kroku načteme rastrový obrázek, který chcete nakreslit do souboru EMF. Nahradit`"Your Document Directory"` s cestou k vašemu obrazu.

## Krok 2: Načtěte kreslicí plochu EMF

```csharp
using (EmfImage canvasImage = (EmfImage)Image.Load(dataDir + "input.emf"))
{
    // Zde je váš kód pro krok 2
}
```

 Zde načteme soubor EMF, který bude sloužit jako kreslicí plocha pro náš obrázek. Nezapomeňte vyměnit`"input.emf"` s cestou k vašemu souboru EMF.

## Krok 3: Vytvořte grafiku EMF Recorder

```csharp
EmfRecorderGraphics2D graphics = EmfRecorderGraphics2D.FromEmfImage(canvasImage);
```

 V tomto kroku vytvoříme instanci`EmfRecorderGraphics2D` z obrázku EMF. To nám umožňuje zaznamenávat kreslicí operace.

## Krok 4: Nakreslete rastrový obrázek

```csharp
graphics.DrawImage(
    imageToDraw,
    new Rectangle(67, 67, canvasImage.Width, canvasImage.Height),
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    GraphicsUnit.Pixel);
```

 V tomto kroku použijeme`DrawImage`metoda k vykreslení načteného rastrového obrázku do souboru EMF. Můžete určit zdrojový a cílový obdélník pro řízení polohy a velikosti nakresleného obrázku.

## Krok 5: Uložte výsledný obrázek

```csharp
using (EmfImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "input.DrawImage.emf");
}
```

 Nakonec výsledný EMF obrázek s nakresleným rastrovým obrázkem uložíme do souboru. Soubor bude uložen pod názvem "input.DrawImage.emf" do adresáře určeného`dataDir`.

Gratulujeme! Úspěšně jste nakreslili rastrový obrázek do souboru EMF pomocí Aspose.Imaging for .NET. Neváhejte prozkoumat a experimentovat s různými zdrojovými a cílovými obdélníky, abyste dosáhli požadovaných efektů.

## Závěr

V tomto tutoriálu jsme se naučili, jak používat Aspose.Imaging pro .NET k nakreslení rastrového obrázku do souboru EMF. Pokud budete postupovat podle podrobného průvodce, můžete tuto funkci snadno integrovat do svých aplikací .NET.

Bavte se vytvářením úžasných obrázků s Aspose.Imaging!

## Nejčastější dotazy

### 1. Mohu nakreslit více obrázků do stejného souboru EMF?

Ano, můžete nakreslit více obrázků do stejného souboru EMF opakováním procesu kreslení s různými zdrojovými a cílovými obdélníky.

### 2. Je Aspose.Imaging kompatibilní s .NET Core?

Ano, Aspose.Imaging for .NET je kompatibilní s .NET Framework i .NET Core.

### 3. Jak mohu na nakreslený obrázek aplikovat transformace, jako je rotace nebo změna měřítka?

 Transformace můžete aplikovat manipulací se zdrojovým a cílovým obdélníkem v`DrawImage` metoda.

### 4. Mohu kreslit vektorovou grafiku i do souboru EMF?

Ano, kromě rastrových obrázků můžete pomocí Aspose.Imaging for .NET kreslit vektorovou grafiku a tvary.

### 5. Kde mohu získat podporu pro Aspose.Imaging?

 Pro podporu a pomoc můžete navštívit fórum Aspose.Imaging[tady](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
