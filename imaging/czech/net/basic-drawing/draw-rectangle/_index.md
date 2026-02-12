---
date: 2026-02-12
description: Naučte se, jak vytvořit prázdný obrázek pomocí Aspose a jak nakreslit
  obdélník v .NET s Aspose.Imaging – rychlý průvodce manipulací s obrázky ve vašich
  .NET aplikacích.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Vytvořit prázdný obrázek pomocí Aspose – kreslení obdélníků v .NET
url: /cs/net/basic-drawing/draw-rectangle/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Vytvořit prázdný obrázek Aspose – kreslení obdélníků v .NET

Vytváření a manipulace s obrázky v .NET aplikacích může působit odstrašujícím dojmem, ale s Aspose.Imaging můžete **create blank image Aspose** během několika řádků kódu a poté na něm kreslit tvary. V tomto tutoriálu projdeme celý proces — od nastavení prázdného plátna po kreslení obdélníků — abyste mohli okamžitě začít přidávat grafiku do svých .NET projektů.

## Rychlé odpovědi
- **Co znamená “create blank image Aspose”?** Znamená to generování prázdného bitmapu pomocí API Aspose.Imaging.  
- **Jak nakreslit obdélník v .NET s Aspose?** Použijte metodu `Graphics.DrawRectangle` po inicializaci objektu `Graphics`.  
- **Který NuGet balíček je vyžadován?** `Aspose.Imaging` (nejnovější verze).  
- **Mohu uložit obrázek jako PNG, JPEG nebo BMP?** Ano – stačí změnit možnosti obrázku (např. `BmpOptions`, `JpegOptions`).  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro hodnocení; pro produkci je vyžadována komerční licence.

## Co je “create blank image Aspose”?
Vytvoření prázdného obrázku znamená alokaci pixelového bufferu s definovanou šířkou, výškou a formátem pixelů. Aspose.Imaging se stará o nízkoúrovňové detaily a poskytuje vám připravené plátno k kreslení bez nutnosti pracovat s GDI+ nebo System.Drawing.

## Proč použít Aspose.Imaging pro kreslení obdélníků v .NET?
- **Cross‑platform** – funguje na Windows, Linuxu i macOS.  
- **Bez nativních závislostí** – čistý spravovaný kód, ideální pro serverová prostředí.  
- **Bohaté kreslicí API** – podporuje pera, štětce, anti‑aliasing a mnoho typů tvarů.  
- **Vysoký výkon** – optimalizováno pro velké obrázky a dávkové zpracování.

## Požadavky

1. **Aspose.Imaging pro .NET** – stáhněte jej ze [stránky ke stažení](https://releases.aspose.com/imaging/net/).  
2. **Vývojové prostředí** – Visual Studio, VS Code nebo jakékoli .NET‑kompatibilní IDE.  
3. **.NET runtime** – .NET 6+ nebo .NET Framework 4.7.2+.

Nyní, když máme vše připravené, ponořme se do kódu.

## Jak vytvořit prázdný obrázek Aspose v .NET?

### Krok 1: Importujte požadované jmenné prostory

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Tyto jmenné prostory vám poskytují přístup k základním třídám pro zpracování obrazu, typům štětců a možnostem ukládání obrázků.

### Krok 2: Vytvořte prázdný obrázek (plátno)

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

V tomto bloku:

* Definujeme výstupní umístění (`dataDir`).  
* Nakonfigurujeme `BmpOptions` pro použití 32‑bitového formátu pixelů.  
* Vytvoříme **blank image** o rozměrech 100 × 100 pixelů.

### Krok 3: Jak nakreslit obdélník v .NET s Aspose.Imaging

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` vyplní plátno barvou pozadí (v tomto příkladu žlutá).  
* `DrawRectangle` nakreslí dva obdélníky — jeden s jednoduchým červeným perem, druhý s modrým plným štětcem — pro vizuální kontrast.

### Krok 4: Uložte obrázek

```csharp
image.Save();
```

Volání `Save` zapíše bitmapu do souborového systému pomocí dříve definovaných možností.

## Časté problémy a tipy

| Problém | Důvod | Řešení |
|---------|-------|--------|
| **Prázdný obrázek se zobrazuje černě** | Pozadí nebylo vymazáno | Zavolejte `graphic.Clear(Color.YourColor)` před kreslením. |
| **Výjimka souboru nenalezen** | `dataDir` ukazuje na neexistující složku | Ujistěte se, že složka existuje, nebo použijte `Path.Combine` s `Environment.CurrentDirectory`. |
| **Nesprávné barvy** | Použití `System.Drawing.Color` místo `Aspose.Imaging.Color` | Vždy importujte `Aspose.Imaging.Color`. |
| **Zpoždění výkonu u velkých obrázků** | Použití výchozích `BmpOptions` s vysokým počtem bitů na pixel | Přepněte na `JpegOptions` nebo `PngOptions` pro kompresi. |

## Často kladené otázky (rozšířené)

**Q: Mohu kreslit i jiné tvary než obdélníky?**  
A: Rozhodně. Aspose.Imaging poskytuje metody jako `DrawEllipse`, `DrawLine` a `DrawPolygon`.

**Q: Je knihovna zdarma pro komerční použití?**  
A: Ne, Aspose.Imaging je komerční produkt, ale můžete ji vyzkoušet pomocí bezplatné zkušební verze dostupné [zde](https://releases.aspose.com/).

**Q: Funguje to jak na Windows, tak na webových aplikacích?**  
A: Ano, stejný kód běží v ASP.NET, Blazor a konzolových aplikacích.

**Q: Jak změním výstupní formát na PNG?**  
A: Nahraďte `BmpOptions` za `PngOptions` a podle toho upravte příponu souboru.

**Q: Kde najdu podrobnější dokumentaci?**  
A: Přístup k úplné referenci API získáte [zde](https://reference.aspose.com/imaging/net/) a můžete se připojit ke komunitě na [fóru Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-02-12  
**Testováno s:** Aspose.Imaging 24.12 for .NET  
**Autor:** Aspose