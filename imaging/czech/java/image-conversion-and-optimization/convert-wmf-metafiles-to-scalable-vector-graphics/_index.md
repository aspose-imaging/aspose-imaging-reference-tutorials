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

## Introduction

Vítejte v našem podrobném průvodci, jak **převést wmf na svg** pomocí Aspose.Imaging pro Java. Ať už jste zkušený vývojář nebo teprve začínáte, tento tutoriál vám poskytne vše, co potřebujete k rychlému a spolehlivému provedení převodu.

## Quick Answers
- **What does the conversion do?** Převádí grafiku Windows Metafile (WMF) na škálovatelný SVG markup.  
- **Which library is required?** Aspose.Imaging for Java (ke stažení z oficiálního webu).  
- **Do I need a license?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Can I customize the output size?** Ano – možnosti rasterizace umožňují nastavit šířku a výšku stránky.  
- **Is Java 8 sufficient?** Ano, knihovna podporuje Java 8 a novější verze.

## What is “convert wmf to svg”?
Převod WMF na SVG znamená převzít vektorový Windows Metafile a přepsat jej do formátu Scalable Vector Graphics, což je XML‑založený formát, který se škáluje bez ztráty kvality a funguje napříč prohlížeči i zařízeními.

## Why use Aspose.Imaging for this conversion?
- **High fidelity** – zachovává vektorová data a vizuální kvalitu.  
- **No external dependencies** – čistě Java, žádné nativní binární soubory.  
- **Fine‑grained control** – možnosti rasterizace vám umožní definovat rozměry, DPI a další parametry.  
- **Cross‑platform** – funguje na Windows, Linuxu i macOS.

## Prerequisites

Než se pustíme do procesu převodu, ujistěte se, že máte splněny následující předpoklady:

1. **Java Development Environment** – Java 8 nebo novější nainstalovaná na vašem počítači.  
2. **Aspose.Imaging Library** – Budete potřebovat knihovnu Aspose.Imaging pro Java. Můžete si ji stáhnout [zde](https://releases.aspose.com/imaging/java/).  
3. **An IDE** – Eclipse, IntelliJ IDEA nebo NetBeans jsou vhodné pro tento tutoriál.

Nyní projděme skutečné kroky.

## How to convert WMF to SVG using Aspose.Imaging

### Step 1: Import Packages

Ve vašem Java kódu importujte potřebné balíčky Aspose.Imaging pro práci se soubory WMF a SVG. Přidejte následující importy na začátek vašeho Java souboru:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.SvgOptions;
import com.aspose.imaging.imageoptions.WmfRasterizationOptions;
```

### Step 2: Load the WMF Image

Dále načtěte WMF obrázek, který chcete převést. Nahraďte zástupnou cestu skutečnou polohou vašeho WMF souboru:

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Create an instance of Image class by loading an existing WMF file.
try (Image image = Image.load(dataDir + "input.wmf")) {
    // Your code goes here...
}
```

### Step 3: Set Rasterization Options

Vytvořte instanci `WmfRasterizationOptions`, která určuje výstupní rozměry. Tento krok vám umožní kontrolovat šířku a výšku stránky výsledného SVG:

```java
final WmfRasterizationOptions options = new WmfRasterizationOptions();
options.setPageWidth(image.getWidth()); // Set the page width
options.setPageHeight(image.getHeight()); // Set the page height
```

### Step 4: Save as SVG

Nakonec uložte WMF obrázek jako SVG soubor. Tento příkaz používá `SvgOptions` spolu s rasterizačními nastaveními, která jste definovali dříve. Název souboru odráží operaci **save svg file java**:

```java
image.save("Your Document Directory" + "ConvertWMFMetaFileToSVG_out.svg", new SvgOptions() {{ setVectorRasterizationOptions(options); }});
```

To je vše! Úspěšně jste **převáděli wmf na svg** a uložili SVG soubor pomocí Javy.

## Common Issues and Solutions

- **File not found** – Ověřte, že `dataDir` ukazuje na správnou složku a že soubor `input.wmf` existuje.  
- **Blank SVG output** – Ujistěte se, že nastavení rasterizace odpovídá rozměrům zdrojového obrázku; nesoulad může vést k prázdnému výstupu.  
- **License exception** – Zkušební licence funguje pro hodnocení, ale pro produkční použití budete potřebovat zakoupenou licenci.

## Frequently Asked Questions

**Q: Is Aspose.Imaging for Java free?**  
A: Ne, Aspose.Imaging je komerční knihovna. Bezplatnou zkušební verzi získáte [zde](https://releases.aspose.com/), nebo můžete zakoupit licenci [zde](https://purchase.aspose.com/buy).

**Q: Can I use Aspose.Imaging for Java in my commercial projects?**  
A: Ano, můžete používat Aspose.Imaging pro Java v komerčních projektech po získání platné licence.

**Q: What other image formats can I convert with Aspose.Imaging for Java?**  
A: Aspose.Imaging podporuje širokou škálu formátů, včetně BMP, JPEG, PNG, TIFF a dalších.

**Q: Is there a community forum for Aspose.Imaging support?**  
A: Ano, komunitní fórum pro podporu a diskuze najdete na [Aspose.Imaging Forum](https://forum.aspose.com/).

**Q: What version of Java is compatible with Aspose.Imaging for Java?**  
A: Aspose.Imaging pro Java je kompatibilní s Java 8 a novějšími verzemi.

## Conclusion

V tomto tutoriálu jsme prošli kompletním procesem **převodu wmf na svg** pomocí Aspose.Imaging pro Java. Se správným nastavením a několika řádky kódu můžete bez problémů transformovat WMF metafily na škálovatelnou SVG grafiku, připravenou pro moderní webové a UI aplikace.

Pro více informací prozkoumejte oficiální referenci API na [Aspose.Imaging for Java documentation](https://reference.aspose.com/imaging/java/).

---

**Last Updated:** 2025-12-30  
**Tested With:** Aspose.Imaging for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}