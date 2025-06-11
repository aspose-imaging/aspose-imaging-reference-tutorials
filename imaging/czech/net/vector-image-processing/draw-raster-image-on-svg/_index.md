---
"description": "Naučte se kreslit rastrové obrázky v SVG pomocí Aspose.Imaging pro .NET. Vylepšete své .NET aplikace dynamickými obrázky."
"linktitle": "Kreslení rastrového obrázku na SVG v Aspose.Imaging pro .NET"
"second_title": "Rozhraní API pro zpracování obrazu Aspose.Imaging .NET"
"title": "Jak nakreslit rastrový obrázek na SVG v Aspose.Imaging pro .NET"
"url": "/cs/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Jak nakreslit rastrový obrázek na SVG v Aspose.Imaging pro .NET


Ve světě programování v .NET je Aspose.Imaging spolehlivou a všestrannou knihovnou pro zpracování různých úloh souvisejících s obrázky. Jednou z fascinujících funkcí, které nabízí, je možnost kreslení rastrového obrázku na SVG plátno. V tomto podrobném návodu vás provedeme procesem kreslení rastrového obrázku na SVG pomocí Aspose.Imaging pro .NET.

## Předpoklady

Než se ponoříme do detailů, ujistěte se, že máte splněny následující předpoklady:

- Aspose.Imaging pro .NET: Musíte mít knihovnu nainstalovanou. Pokud ne, můžete si ji stáhnout z [Stránka pro stažení Aspose.Imaging pro .NET](https://releases.aspose.com/imaging/net/).

- Váš adresář dokumentů: Nahradit `"Your Document Directory"` se skutečnou cestou k vašemu pracovnímu adresáři.

Nyní si celý proces rozdělme na snadno sledovatelné kroky:

## Krok 1: Importujte potřebné jmenné prostory

Pro práci s Aspose.Imaging je třeba importovat požadované jmenné prostory:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Krok 2: Načtení obrázků

- Nejprve si načtěte rastrový obrázek, který chcete nakreslit na plátno SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Dále načtěte obrázek SVG plátna na místo, kam chcete rastrový obrázek umístit.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Krok 3: Kreslení na SVG obrázku

Nyní můžete začít kreslit na existující SVG obrázek. K tomu je potřeba vytvořit instanci třídy `SvgGraphics2D`:

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

## Krok 5: Uložení výsledku

Po nakreslení rastrového obrázku na plátno SVG můžete výsledný obrázek uložit:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Závěr

Gratulujeme! Úspěšně jste nakreslili rastrový obrázek na SVG plátno pomocí Aspose.Imaging pro .NET. To může být neuvěřitelně užitečné pro vytváření bohatých a dynamických obrázků ve vašich .NET aplikacích.

Pro více informací a podrobnou dokumentaci navštivte [Dokumentace k Aspose.Imaging pro .NET](https://reference.aspose.com/imaging/net/).

## Často kladené otázky

### Co je Aspose.Imaging pro .NET?
   Aspose.Imaging pro .NET je výkonná knihovna pro zpracování obrazu, která umožňuje vývojářům vytvářet, manipulovat a převádět obrázky v různých formátech v rámci .NET aplikací.

### Mohu použít Aspose.Imaging pro .NET v komerčních projektech?
   Ano, Aspose.Imaging pro .NET můžete používat v komerčních i nekomerčních projektech. Podrobnosti o licencování naleznete na [stránka nákupu](https://purchase.aspose.com/buy).

### Je k dispozici bezplatná zkušební verze?
   Ano, můžete získat bezplatnou zkušební verzi Aspose.Imaging pro .NET od [zde](https://releases.aspose.com/).

### Kde mohu získat podporu nebo se zeptat?
   Pokud máte jakékoli dotazy nebo potřebujete podporu, můžete navštívit [Fórum Aspose.Imaging](https://forum.aspose.com/).

### Jak mohu získat dočasnou licenci pro Aspose.Imaging pro .NET?
   Dočasné povolení můžete získat od [zde](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}