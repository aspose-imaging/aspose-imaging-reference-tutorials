---
title: Kreslit vektorový obrázek na rastrový obrázek v Aspose.Imaging pro .NET
linktitle: Kreslit vektorový obrázek na rastrový obrázek v Aspose.Imaging pro .NET
second_title: Aspose.Imaging .NET Image Processing API
description: Naučte se převádět vektorové obrázky na rastrové obrázky v .NET pomocí Aspose.Imaging. Návod krok za krokem pro efektivní zpracování obrazu.
type: docs
weight: 13
url: /cs/net/vector-image-processing/draw-vector-image-to-raster-image/
---

Hledáte převést vektorové obrázky na rastrové obrázky bez námahy ve svých aplikacích .NET? Aspose.Imaging for .NET poskytuje efektivní řešení pro tento úkol. V tomto podrobném průvodci vás provedeme procesem kreslení vektorových obrázků na rastrové obrázky pomocí Aspose.Imaging for .NET. 

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

### 1. Aspose.Imaging pro .NET

 Měli byste mít nainstalovaný Aspose.Imaging for .NET. Pokud jej nemáte, můžete si jej stáhnout z webových stránek na adrese[Stáhněte si Aspose.Imaging pro .NET](https://releases.aspose.com/imaging/net/).

### 2. Vývojové prostředí .NET

Ujistěte se, že máte na svém počítači nastavené vývojové prostředí .NET. Můžete použít Visual Studio nebo jakýkoli jiný vývojový nástroj .NET.

Nyní si rozdělme proces kreslení vektorových obrázků na rastrové obrázky do jednoduchých, snadno pochopitelných kroků:

## Krok 1: Inicializujte svůj projekt

Začněte vytvořením nového projektu .NET ve vašem vývojovém prostředí. Ujistěte se, že máte Aspose.Imaging for .NET integrovaný do vašeho projektu.

## Krok 2: Načtěte vektorový obrázek

tomto kroku načteme vektorový obrázek (ve formátu SVG), který chcete převést na rastrový obrázek.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## Krok 3: Rastrujte vektorový obrázek

Nyní potřebujeme rastrovat obrázek SVG do formátu PNG. Zde dochází ke konverzi z vektoru na rastr.

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## Krok 4: Načtěte rastrový obrázek

Po rastrování načtěte obrázek PNG ze streamu pro další kreslení.

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## Krok 5: Nakreslete rastrový obrázek

Nyní můžeme nakreslit rastrový obrázek na existující obrázek SVG.

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## Krok 6: Uložte výsledek

Nakonec výsledný obrázek uložte. Nyní máte rastrový obrázek, který obsahuje váš vektorový obrázek.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## Závěr

V tomto tutoriálu jsme si ukázali, jak převést vektorové obrázky na rastrové obrázky pomocí Aspose.Imaging for .NET. Pomocí těchto jednoduchých kroků můžete tuto funkci bez námahy integrovat do svých aplikací .NET.

### Často kladené otázky

### Co je Aspose.Imaging pro .NET?
Aspose.Imaging for .NET je knihovna .NET, která poskytuje výkonné funkce pro zpracování obrázků, včetně schopnosti pracovat s různými formáty obrázků, převádět obrázky a provádět pokročilé úlohy manipulace s obrázky.

### Kde najdu dokumentaci k Aspose.Imaging pro .NET?
 Můžete najít dokumentaci k Aspose.Imaging pro .NET[tady](https://reference.aspose.com/imaging/net/).

### Je k dispozici bezplatná zkušební verze?
 Ano, máte přístup k bezplatné zkušební verzi Aspose.Imaging pro .NET[tady](https://releases.aspose.com/).

### Jak získám dočasnou licenci pro Aspose.Imaging pro .NET?
 Pokud potřebujete dočasnou licenci, můžete si ji pořídit[tady](https://purchase.aspose.com/temporary-license/).

### Kde mohu získat podporu pro Aspose.Imaging pro .NET?
 V případě jakékoli podpory nebo dotazů můžete navštívit stránku[Fórum Aspose.Imaging](https://forum.aspose.com/).
