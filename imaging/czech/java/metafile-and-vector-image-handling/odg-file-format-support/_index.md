---
title: Převeďte ODG na PNG a PDF pomocí Aspose.Imaging pro Java
linktitle: Podpora formátu souborů ODG
second_title: Aspose.Imaging Java Image Processing API
description: Naučte se převádět soubory ODG do PNG a PDF pomocí Aspose.Imaging for Java. Postupujte podle našeho podrobného průvodce pro efektivní převod.
weight: 12
url: /cs/java/metafile-and-vector-image-handling/odg-file-format-support/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převeďte ODG na PNG a PDF pomocí Aspose.Imaging pro Java

Ve světě převodu dokumentů vyniká Aspose.Imaging for Java jako výkonný nástroj, který umožňuje snadno převádět soubory ODG (OpenDocument Graphics) do formátů PNG a PDF. Tento tutoriál vás provede procesem krok za krokem pomocí Aspose.Imaging pro Java. Ať už jste vývojář nebo jen někdo, kdo chce převést soubory ODG, tento článek vám pomůže dosáhnout vašeho cíle.

## Předpoklady

Než se pustíme do procesu převodu, musíte se ujistit, že máte splněny následující předpoklady:

### 1. Vývojové prostředí Java

 Ujistěte se, že máte ve svém systému nastavené vývojové prostředí Java. Nejnovější sadu Java Development Kit (JDK) si můžete stáhnout a nainstalovat z webu[Web společnosti Oracle](https://www.oracle.com/java/technologies/javase-downloads).

### 2. Aspose.Imaging pro Java

 Budete si muset stáhnout a nainstalovat Aspose.Imaging for Java. Nejnovější verzi najdete na[Stránka ke stažení Aspose.Imaging pro Java](https://releases.aspose.com/imaging/java/).

### 3. Soubory ODG

Samozřejmě budete potřebovat soubory ODG, které chcete převést. Ujistěte se, že máte tyto soubory dostupné v adresáři ve vašem systému.

## Importujte balíčky

Nyní, když máte připravené předpoklady, začněme s importem potřebných balíčků do vašeho projektu Java. Tyto balíčky vám umožní efektivně pracovat s Aspose.Imaging for Java.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.SizeF;
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
```

Nyní rozdělíme proces převodu do jednoduchých kroků, aby bylo snadné jej sledovat. U každého kroku poskytneme nadpis a vysvětlení.

## Krok 1: Definujte svůj datový adresář

 Začněte zadáním adresáře, kde jsou umístěny vaše soubory ODG. Budete muset vyměnit`"Your Document Directory"` se skutečnou cestou k vašemu adresáři.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

## Krok 2: Zadejte soubory ODG

Vytvořte pole názvů souborů ODG, které chcete převést. Nahraďte vzorové názvy souborů názvy vašich souborů ODG.

```java
String[] files = new String[] {"example.odg", "example1.odg"};
```

## Krok 3: Nakonfigurujte možnosti rastrování

Nastavte možnosti rasterizace pro soubory ODG. Tyto možnosti určí velikost stránky a nastavení vektorového rastrování.

```java
final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
```

## Krok 4: Procházení souborů ODG

Nyní iterujte každý soubor ODG, načtěte jej a převeďte do formátu PNG i PDF.

```java
for (String file : files) {
    String fileName = dataDir + file;
    try (Image image = Image.load(fileName)) {
        rasterizationOptions.setPageSize(new SizeF(image.getWidth(), image.getHeight()));

        // Převést do PNG
        String outFileName = "Your Document Directory" + file.replace(".odg", ".png");
        image.save(outFileName, new PngOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});

        // Převést do PDF
        outFileName = "Your Document Directory" + file.replace(".odg", ".pdf");
        image.save(outFileName, new PdfOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});
    }
}
```

Gratulujeme! Úspěšně jste převedli své soubory ODG do formátu PNG i PDF pomocí Aspose.Imaging for Java.

## Závěr

Aspose.Imaging for Java zjednodušuje proces převodu souborů ODG do více podporovaných obrazových formátů, jako jsou PNG a PDF. Podle kroků uvedených v tomto kurzu můžete efektivně provádět tyto převody ve svých projektech Java.

## FAQ

### Q1: Je Aspose.Imaging for Java bezplatný nástroj?

 A1: Ne, Aspose.Imaging for Java je komerční knihovna a informace o cenách najdete na[nákupní stránku](https://purchase.aspose.com/buy).

### Q2: Mohu vyzkoušet Aspose.Imaging pro Java před nákupem?

 A2: Ano, můžete si stáhnout bezplatnou zkušební verzi z[tady](https://releases.aspose.com/).

### Q3: Jak mohu získat podporu pro Aspose.Imaging pro Java?

 A3: Můžete vyhledat pomoc a klást otázky na[Fórum Aspose.Imaging](https://forum.aspose.com/).

### Q4: Jaké další formáty souborů může Aspose.Imaging for Java zpracovat?

 A4: Aspose.Imaging for Java podporuje širokou škálu formátů obrázků a dokumentů, včetně BMP, JPEG, TIFF, PDF a dalších. Odkazovat na[dokumentace](https://reference.aspose.com/imaging/java/) pro úplný seznam.

### Q5: Mohu použít Aspose.Imaging pro Java ve svých komerčních projektech?

A5: Ano, Aspose.Imaging pro Java můžete používat v komerčních projektech po zakoupení příslušné licence.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
