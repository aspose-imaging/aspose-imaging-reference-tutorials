---
date: 2025-12-30
description: Naučte se, jak převést WMF na SVG a uložit soubor SVG v Javě pomocí Aspose.Imaging
  pro Javu. Postupujte podle našeho krok za krokem průvodce pro efektivní konverzi
  formátů obrázků.
linktitle: Convert WMF Metafiles to Scalable Vector Graphics
second_title: Aspose.Imaging Java Image Processing API
title: Převést WMF na SVG – Převést WMF metafily na škálovatelnou vektorovou grafiku
url: /cs/java/image-conversion-and-optimization/convert-wmf-metafiles-to-scalable-vector-graphics/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Převod WMF na SVG – Převod WMF metafilek na škálovatelnou vektorovou grafiku

## Úvod

Vítejte v našem podrobném průvodci, jak **převést wmf na svg** pomocí Aspose.Imaging pro Java. Ať už jste zkušený vývojář nebo začínáte, tento tutoriál vám poskytne vše, co potřebujete k rychlému a spolehlivému provedení převodu.

## Rychlé odpovědi
- **Co dělá konverze?** Převádí grafiku Windows Metafile (WMF) na škálovatelný SVG markup.
- **Jaká knihovna je vyžadována?** Aspose.Imaging pro Javu (ke stažení z oficiálního webu).
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.
- **Mohu přizpůsobit velikost výstupu?** Ano – možnosti rastrování nastavit nastavit šířku a výšku stránek.
- **Stačí Java 8?** Ano, knihovna podporuje Java8 a novější verze.

## Co je to „převést wmf na svg“?
Převod WMF na SVG znamená převzít vektorový Windows Metafile a přepsat jej do formátu Scalable Vector Graphics, což je XML‑založený formát, který se vyskytuje bez ztráty kvality a funguje napříč prohlížečem i zařízeními.

## Proč pro tuto konverzi používat Aspose.Imaging?
- **High fidelity** – zachovává vektorová data a vizuální kvalitu.
- **Žádné externí závislosti** – čistá Java, žádné nativní binární soubory.
- **Fi‑grained control** – možnosti rasterizace vám umožní definovat rozměry, DPI a další parametry.
- **Cross‑platform** – funguje na Windows, Linuxu a macOS.

## Předpoklady

Než se do procesu převodu spustíme, pustíme se, že máte splněny následující předpoklady:

1. **Java Development Environment** – Java8 nebo novější nainstalovaná na vašem počítači.
2. **Aspose.Imaging Library** – Potřebujete knihovnu Aspose.Imaging pro Java. Můžete si ji stáhnout [zde](https://releases.aspose.com/imaging/java/).
3. **An IDE** – Eclipse, IntelliJ IDEA nebo NetBeans jsou vhodné pro tento tutoriál.

Nyní projdeme skutečné kroky.

## Jak převést WMF na SVG pomocí Aspose.Imaging

### Krok 1: Importujte balíčky

Ve vaší Java kódujte importujte potřebné balíčky Aspose.Imaging pro práci se soubory WMF a SVG. Přidejte následující import na začátek vašeho souboru Java:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.SvgOptions;
import com.aspose.imaging.imageoptions.WmfRasterizationOptions;
```

### Krok 2: Načtěte obrázek WMF

Dále načtěte WMF obrázek, který chcete převést. Nahraďte zástupnou cestu skutečnou polohou vašeho WMF souboru:

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Create an instance of Image class by loading an existing WMF file.
try (Image image = Image.load(dataDir + "input.wmf")) {
    // Your code goes here...
}
```

### Krok 3: Nastavte možnosti rastrování

Vytvořte instanci `WmfRasterizationOptions`, která určuje výstupní rozměry. Tento krok vám umožní kontrolovat šířku a výšku stránky výsledného SVG:

```java
final WmfRasterizationOptions options = new WmfRasterizationOptions();
options.setPageWidth(image.getWidth()); // Set the page width
options.setPageHeight(image.getHeight()); // Set the page height
```

### Krok 4: Uložte jako SVG

Nakonec uložte WMF obrázek jako SVG soubor. Tento příkaz používá `SvgOptions` spolu s rasterizačními nastaveními, která jste definovali dříve. Název souboru odráží operaci **save svg file java**:

```java
image.save("Your Document Directory" + "ConvertWMFMetaFileToSVG_out.svg", new SvgOptions() {{ setVectorRasterizationOptions(options); }});
```

To je vše! Úspěšně jste **převáděli wmf na svg** a uložili SVG soubor pomocí Javy.

## Běžné problémy a řešení

- **File not found** – Ověřte, že `dataDir` ukazuje na příslušnou složku a že soubor `input.wmf` existuje.
- **Blank SVG output** – naleznete se, že nastavení rasterizace odpovídá rozměrům zdrojového obrázku; nesoulad může vést k prázdnému výstupu.
- **Výjimka licence** – Zkušební licence funguje pro hodnocení, ale pro produkční použití budete potřebovat zakoupenou licenci.

## Často kladené otázky

**Otázka: Je Aspose.Imaging pro Java zdarma?**
A: Ne, Aspose.Imaging je komerční knihovna. Bezplatnou zkušební verzi získáte [zde](https://releases.aspose.com/), nebo si můžete zakoupit licenci [zde](https://purchase.aspose.com/buy).

**Otázka: Mohu použít Aspose.Imaging pro Javu ve svých komerčních projektech?**
A: Ano, můžete používat Aspose.Imaging pro Java v komerčních projektech po získání platné licence.

**Otázka: Jaké další obrazové formáty mohu převést pomocí Aspose.Imaging for Java?**
A: Aspos.Imaging podporuje širokých formátů, včetně BMP, JPEG, PNG, TIFF a dalších.

**Otázka: Existuje komunitní fórum pro podporu Aspose.Imaging?**
A: Ano, komunitní fórum pro podporu a diskuze najdete na [Aspose.Imaging Forum](https://forum.aspose.com/).

**Otázka: Jaká verze Java je kompatibilní s Aspose.Imaging for Java?**
A: Aspose.Imaging pro Java je kompatibilní s Java8 a novějšími verzemi.

## Závěr

V tomto tutoriálu jsme prošli kompletním procesem **převodu wmf na svg** pomocí Aspose.Imaging pro Java. Se správným nastavením a několika řádky kódu můžete bez problémů transformovat WMF metafily na škálovatelnou SVG grafiku, připravenou pro moderní webové a UI aplikace.

Pro více informací vyzkoušejte oficiální referenční API na [dokumentaci Aspose.Imaging pro Java](https://reference.aspose.com/imaging/java/).

---

**Poslední aktualizace:** 2025-12-30
**Testováno s:** Aspose.Imaging pro Java 24.11
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}