---
title: Jak nakreslit rastrový obrázek na SVG v Aspose.Imaging pro .NET
linktitle: Kreslit rastrový obrázek na SVG v Aspose.Imaging pro .NET
second_title: Aspose.Imaging .NET Image Processing API
description: Naučte se kreslit rastrové obrázky na SVG pomocí Aspose.Imaging for .NET. Vylepšete své aplikace .NET pomocí dynamických obrázků.
weight: 11
url: /cs/net/vector-image-processing/draw-raster-image-on-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak nakreslit rastrový obrázek na SVG v Aspose.Imaging pro .NET


Ve světě programování .NET je Aspose.Imaging spolehlivá a všestranná knihovna pro zpracování různých úloh souvisejících s obrázky. Jednou z fascinujících schopností, které nabízí, je schopnost kreslit rastrový obrázek na plátno SVG. V tomto podrobném průvodci vás provedeme procesem kreslení rastrového obrázku na SVG pomocí Aspose.Imaging for .NET.

## Předpoklady

Než se ponoříme do podrobností, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.Imaging for .NET: Musíte mít nainstalovanou knihovnu. Pokud ne, můžete si jej stáhnout z[Stránka ke stažení Aspose.Imaging pro .NET](https://releases.aspose.com/imaging/net/).

-  Váš adresář dokumentů: Nahradit`"Your Document Directory"` se skutečnou cestou k vašemu pracovnímu adresáři.

Nyní si tento proces rozdělíme do snadno pochopitelných kroků:

## Krok 1: Importujte potřebné jmenné prostory

Pro práci s Aspose.Imaging musíte importovat požadované jmenné prostory:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Krok 2: Načtěte obrázky

- Nejprve načtěte rastrový obrázek, který chcete nakreslit na plátno SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Dále načtěte obraz na plátně SVG, kam chcete nakreslit rastrový obrázek.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Krok 3: Kreslení na obrázek SVG

Nyní můžete začít kreslit na existující obrázek SVG. Chcete-li to provést, musíte vytvořit instanci`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Krok 4: Nakreslete rastrový obrázek

- Definujte hranice, kde chcete nakreslit rastrový obrázek, a určete zdrojovou oblast z rastrového obrázku.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Krok 5: Uložte výsledek

Po nakreslení rastrového obrázku na plátno SVG můžete výsledný obrázek uložit:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Závěr

Gratulujeme! Úspěšně jste nakreslili rastrový obrázek na plátno SVG pomocí Aspose.Imaging for .NET. To může být neuvěřitelně užitečné pro vytváření bohatých a dynamických obrázků ve vašich aplikacích .NET.

 Pro více informací a podrobnou dokumentaci navštivte[Dokumentace Aspose.Imaging pro .NET](https://reference.aspose.com/imaging/net/).

## Často kladené otázky

### Co je Aspose.Imaging pro .NET?
   Aspose.Imaging for .NET je výkonná knihovna pro zpracování obrázků, která umožňuje vývojářům vytvářet, manipulovat a převádět obrázky v různých formátech v rámci aplikací .NET.

### Mohu použít Aspose.Imaging pro .NET v komerčních projektech?
    Ano, Aspose.Imaging pro .NET můžete používat v komerčních i nekomerčních projektech. Podrobnosti o licenci naleznete na[nákupní stránku](https://purchase.aspose.com/buy).

### Je k dispozici bezplatná zkušební verze?
    Ano, můžete získat bezplatnou zkušební verzi Aspose.Imaging pro .NET od[tady](https://releases.aspose.com/).

### Kde mohu získat podporu nebo klást otázky?
    Pokud máte nějaké dotazy nebo potřebujete podporu, můžete navštívit stránku[Fórum Aspose.Imaging](https://forum.aspose.com/).

### Jak mohu získat dočasnou licenci pro Aspose.Imaging pro .NET?
    Dočasnou licenci můžete získat od[tady](https://purchase.aspose.com/temporary-license/).



{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
