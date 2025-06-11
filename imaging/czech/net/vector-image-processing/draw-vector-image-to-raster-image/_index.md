---
"description": "Naučte se, jak převádět vektorové obrázky na rastrové v .NET pomocí Aspose.Imaging. Podrobný návod pro efektivní zpracování obrazu."
"linktitle": "Převod vektorového obrázku do rastrového v Aspose.Imaging pro .NET"
"second_title": "Rozhraní API pro zpracování obrazu Aspose.Imaging .NET"
"title": "Převod vektorového obrázku do rastrového v Aspose.Imaging pro .NET"
"url": "/cs/net/vector-image-processing/draw-vector-image-to-raster-image/"
"weight": 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Převod vektorového obrázku do rastrového v Aspose.Imaging pro .NET


Hledáte způsob, jak snadno převést vektorové obrázky na rastrové ve vašich .NET aplikacích? Aspose.Imaging for .NET nabízí efektivní řešení pro tento úkol. V tomto podrobném návodu vás provedeme procesem kreslení vektorových obrázků do rastrových obrázků pomocí Aspose.Imaging for .NET. 

## Předpoklady

Než se pustíme do tutoriálu, ujistěte se, že máte splněny následující předpoklady:

### 1. Aspose.Imaging pro .NET

Měli byste mít nainstalovaný Aspose.Imaging pro .NET. Pokud ho nemáte, můžete si ho stáhnout z webových stránek na adrese [Stáhnout Aspose.Imaging pro .NET](https://releases.aspose.com/imaging/net/).

### 2. Vývojové prostředí .NET

Ujistěte se, že máte v počítači nainstalované vývojové prostředí .NET. Můžete použít Visual Studio nebo jakýkoli jiný vývojový nástroj pro .NET.

Nyní si rozeberme proces kreslení vektorových obrázků do rastrových obrázků do jednoduchých a snadno sledovatelných kroků:

## Krok 1: Inicializace projektu

Začněte vytvořením nového projektu .NET ve vašem vývojovém prostředí. Ujistěte se, že máte do projektu integrovaný Aspose.Imaging for .NET.

## Krok 2: Načtení vektorového obrázku

V tomto kroku načteme vektorový obrázek (ve formátu SVG), který chcete převést na rastrový obrázek.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## Krok 3: Rastrování vektorového obrázku

Nyní musíme rastrovat SVG obrázek do formátu PNG. Zde probíhá převod z vektorového do rastrového formátu.

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## Krok 4: Načtení rastrového obrázku

Po rastrování načtěte obrázek PNG ze streamu pro další kreslení.

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## Krok 5: Nakreslete rastrový obrázek

Nyní můžeme nakreslit rastrový obrázek na existující SVG obrázek.

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## Krok 6: Uložení výsledku

Nakonec uložte výsledný obrázek. Nyní máte rastrový obrázek, který obsahuje váš vektorový obrázek.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## Závěr

tomto tutoriálu jsme si ukázali, jak převést vektorové obrázky na rastrové pomocí Aspose.Imaging pro .NET. Pomocí těchto jednoduchých kroků můžete tuto funkci snadno integrovat do vašich .NET aplikací.

### Často kladené otázky

### Co je Aspose.Imaging pro .NET?
Aspose.Imaging pro .NET je knihovna pro .NET, která poskytuje výkonné funkce pro zpracování obrazu, včetně možnosti pracovat s různými obrazovými formáty, převádět obrázky a provádět pokročilé úlohy manipulace s obrázky.

### Kde najdu dokumentaci k Aspose.Imaging pro .NET?
Dokumentaci k Aspose.Imaging pro .NET naleznete [zde](https://reference.aspose.com/imaging/net/).

### Je k dispozici bezplatná zkušební verze?
Ano, máte přístup k bezplatné zkušební verzi Aspose.Imaging pro .NET. [zde](https://releases.aspose.com/).

### Jak získám dočasnou licenci pro Aspose.Imaging pro .NET?
Pokud potřebujete dočasný řidičský průkaz, můžete si ho pořídit [zde](https://purchase.aspose.com/temporary-license/).

### Kde mohu získat podporu pro Aspose.Imaging pro .NET?
případě jakékoli podpory nebo dotazů můžete navštívit [Fórum Aspose.Imaging](https://forum.aspose.com/).


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}