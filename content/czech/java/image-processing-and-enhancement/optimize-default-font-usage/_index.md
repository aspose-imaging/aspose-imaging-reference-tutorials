---
title: Optimalizace výchozího použití písma pomocí Aspose.Imaging pro Java
linktitle: Optimalizovat výchozí použití písma
second_title: Aspose.Imaging Java Image Processing API
description: Zjistěte, jak optimalizovat použití výchozího písma pomocí Aspose.Imaging for Java. Zlepšete své zpracování dokumentů pomocí podrobných pokynů.
type: docs
weight: 10
url: /cs/java/image-processing-and-enhancement/optimize-default-font-usage/
---
Ve světě zpracování dokumentů a manipulace s obrázky vyniká Aspose.Imaging for Java jako výkonný nástroj. Tato všestranná knihovna Java umožňuje vývojářům snadno vytvářet, upravovat a převádět obrázky. Jedním z klíčových aspektů optimalizace zpracování dokumentů je zlepšení používání písem. V tomto podrobném průvodci prozkoumáme, jak optimalizovat výchozí použití písem pomocí Aspose.Imaging pro Java. Každý příklad rozdělíme do několika kroků, abychom zajistili, že procesu důkladně porozumíte.

## Předpoklady

Než se pustíme do procesu optimalizace, ujistěte se, že máte splněny následující předpoklady:

- Vývojové prostředí Java nainstalované ve vašem systému.
-  Aspose.Imaging pro knihovnu Java. Můžete si jej stáhnout z[webová stránka](https://releases.aspose.com/imaging/java/).
- Základní znalost programování v Javě.

## Importujte balíčky

Chcete-li začít s optimalizací výchozího použití písem, musíte importovat potřebné balíčky z Aspose.Imaging for Java. Zde jsou kroky, jak to udělat:

Importujte knihovnu Aspose.Imaging

Nejprve zahrňte do svého projektu Java knihovnu Aspose.Imaging přidáním následujícího příkazu importu:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fonts.FontSettings;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.odg.OdgRasterizationOptions;
```

Nyní, když jsme importovali požadované balíčky, rozdělme proces optimalizace do několika kroků.

## Krok 1: Nastavte adresář dokumentů

 Před optimalizací použití písem musíte nastavit adresář dokumentů. Nahradit`"Your Document Directory" + "otg/"` se skutečnou cestou k vašemu adresáři dokumentů. Například:

```java
String dataDir = "C:/Documents/";
String outDir = Utils.getOutDir("DefaultFontUsageImprove");
```

## Krok 2: Nakonfigurujte nastavení písma

Chcete-li zlepšit výchozí použití písma, nakonfigurujte nastavení písma následovně:

```java
FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
FontSettings.setGetSystemAlternativeFont(false);
```

## Krok 3: Export do PNG s výchozím písmem

Nyní exportujeme dokument do obrázku PNG pomocí zadaného výchozího písma. Zde máme dva příklady, jeden používá „Arial“ a druhý používá „Courier New“ jako výchozí písmo.

```java
exportToPng(Path.combine(dataDir, "missing-font2.odg"), "Arial", Path.combine(outDir, "arial.png"));
exportToPng(
    Path.combine(dataDir, "missing-font2.odg"),
    "Courier New",
    Path.combine(outDir, "courier.png"));
```

## Krok 4: Funkce Export do PNG

 Tady je`exportToPng` funkce pro provedení skutečného exportu do PNG se zadaným výchozím písmem:

```java
private static void exportToPng(String filePath, String defaultFontName, String outfileName)
{
    FontSettings.setDefaultFontName(defaultFontName);
    try (Image document = Image.load(filePath))
    {
        PngOptions saveOptions = new PngOptions();
        final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
        rasterizationOptions.setPageWidth(1000);
        rasterizationOptions.setPageHeight(1000);
        saveOptions.setVectorRasterizationOptions(rasterizationOptions);
        document.save(outfileName, saveOptions);
    }
    Utils.deleteFile(outfileName);
}
```

Tato funkce nastaví výchozí písmo, načte dokument, konfiguruje možnosti exportu a uloží výstupní obrázek PNG.

## Závěr

Optimalizace výchozího použití písma při zpracování dokumentů může výrazně zvýšit kvalitu vašeho výstupu. Aspose.Imaging for Java tento proces zjednodušuje, umožňuje vám specifikovat písmo a efektivně exportovat dokumenty. Pokud budete postupovat podle podrobného průvodce popsaného v tomto článku, můžete snadno zlepšit používání písma.

## FAQ

### Q1: Co je Aspose.Imaging pro Java?

Odpověď 1: Aspose.Imaging for Java je knihovna Java, která poskytuje širokou škálu funkcí pro práci s obrázky a dokumenty, včetně vytváření, převodu a manipulace s obrázky.

### Q2: Jak mohu získat Aspose.Imaging pro Java?

 A2: Aspose.Imaging for Java si můžete stáhnout z webové stránky na adrese[tento odkaz](https://releases.aspose.com/imaging/java/).

### Q3: Existují nějaké možnosti licencování pro Aspose.Imaging pro Java?

 A3: Ano, můžete si zakoupit licence pro Aspose.Imaging pro Java z[nákupní stránku](https://purchase.aspose.com/buy).

### Q4: Je k dispozici bezplatná zkušební verze?

A4: Ano, můžete si zdarma vyzkoušet Aspose.Imaging pro Javu stažením zkušební verze z[tady](https://releases.aspose.com/).

### Q5: Kde mohu získat podporu pro Aspose.Imaging pro Java?

 Odpověď 5: Pokud potřebujete pomoc nebo máte dotazy, můžete navštívit fórum podpory Aspose.Imaging for Java na adrese[https://forum.aspose.com/](https://forum.aspose.com/).