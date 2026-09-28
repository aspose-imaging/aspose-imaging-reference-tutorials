---
date: '2026-09-28'
description: Naučte se, jak použít ccittfax3 compression java k vytvoření multi-page
  TIFF souborů s Aspose.Imaging. Efektivně scan, archive a reduce file size pro document
  workflows.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Objevte krok za krokem, jak použít ccittfax3 compression java s Aspose.Imaging
  k vytvoření efektivních multi-page TIFF souborů pro scanning a archiving.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: Jak vytvořit multi-page TIFF s ccittfax3 compression java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: Jak vytvořit multi-page TIFF s ccittfax3 compression java
url: /cs/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ovládání tvorby vícestránkových TIFF souborů s kompresí ccittfax3 v Javě pomocí Aspose.Imaging

## Úvod

Pokud potřebujete archivovat velké objemy naskenovaných dokumentů a zároveň udržet velikost souborů nízkou, **ccittfax3 compression java** je řešením. Tento tutoriál vám ukáže, jak v Javě pomocí Aspose.Imaging generovat vícestránkové TIFF soubory s kompresí CCITTFAX3. Naučíte se, proč tato komprese funguje tak dobře pro monochromatické skeny, jak nakonfigurovat knihovnu a jak přidat každou stránku jako rámec.

**Co se naučíte**
- Jak přidat Aspose.Imaging do Java projektu.
- Jak nakonfigurovat `TiffOptions` pro kompresi CCITTFAX3.
- Jak vytvořit `TiffImage`, změnit velikost zdrojových obrázků a přidat je jako rámce.
- Jak efektivně uložit finální vícestránkový TIFF.

Pojďme projít kompletní implementaci.

## Rychlé odpovědi
- **Jaký je hlavní přínos komprese CCITTFAX3?** Až 80 % snížení velikosti souboru pro černobílé skeny.  
- **Která knihovna poskytuje vestavěnou podporu?** Aspose.Imaging pro Java, verze 25.5+.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební licence funguje pro všechny funkce; placená licence je vyžadována pro produkci.  
- **Mohu zpracovat stovky stránek?** Ano—Aspose.Imaging streamuje stránky, takže využití paměti zůstává nízké.  
- **Je kód kompatibilní s Java 11 a novějšími?** Absolutně; API cílí na Java 8+.

## Co je ccittfax3 compression java?
`CCITTFAX3` je bezztrátový, monochromatický kompresní algoritmus určený pro fax a skenované dokumenty. Kóduje každý pixel jako jeden bit, poskytuje vysoce kvalitní výstup a zároveň dramaticky zmenšuje velikost souboru—často o 70‑80 % oproti nekomprimovanému TIFF. To ho činí ideálním pro archivaci černobílých dokumentů, kde je nutná zachovat věrnost.

## Proč použít Aspose.Imaging pro tento úkol?
Aspose.Imaging podporuje **100+** vstupních a výstupních formátů, včetně PDF, PNG, JPEG a TIFF. Jeho streamovací architektura dokáže zpracovat **více‑stovek‑stránkových** TIFF souborů, aniž by načítala celý dokument do paměti, což je ideální pro rozsáhlé archivní projekty.

## Požadavky

- **Java Development Kit (JDK)** 8 nebo novější nainstalovaný.
- **IDE** jako IntelliJ IDEA nebo Eclipse.
- **Maven** nebo **Gradle** pro správu závislostí.
- Základní znalost Javy (třídy, objekty, kolekce).

## Nastavení Aspose.Imaging pro Java

Přidejte knihovnu do vašeho build souboru.

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```  

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

### Přímé stažení

Můžete také stáhnout nejnovější JAR z [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### Získání licence

Bezplatná zkušební licence je k dispozici na [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/). Pro produkční použití zakupte trvalou licenci nebo požádejte o dočasnou na [Aspose Purchase](https://purchase.aspose.com/temporary-license/).

Pro podrobný popis API viz Aspose.Imaging pro Java [documentation](https://reference.aspose.com/imaging/java/).

### Základní inicializace

Po přidání závislosti inicializujte knihovnu, jak je ukázáno níže.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## Jak nakonfigurovat ccittfax3 compression java pro vícestránkový TIFF?

`TiffOptions` je třída, která definuje výstupní formát a nastavení komprese pro TIFF soubor. Načtěte objekt `TiffOptions` s výčtem `CCITTGroup3FaxCompression` a poté nastavte zdroj výstupního souboru. Toto dvoustupňové nastavení připraví zapisovač na monochromatickou kompresi a zajistí, že každá později přidaná stránka bude kódována algoritmem CCITTFAX3, což vede k výraznému snížení velikosti při zachování kvality obrazu.

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## Jak vytvořit instanci TiffImage v Javě?

`TiffImage` představuje vícestránkový TIFF dokument v paměti a poskytuje metody pro manipulaci s jeho rámci. Nejprve definujte šířku a výšku, které budou sdílet všechny stránky. Poté vytvořte instanci `TiffImage` pomocí dříve vytvořených `TiffOptions`. Objekt `TiffImage` funguje jako kontejner pro jednotlivé rámce, umožňuje přidávat, odstraňovat nebo měnit pořadí stránek před uložením finálního souboru.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## Jak načíst a změnit velikost zdrojových obrázků ze složky?

Filtrujte cílový adresář na JPEG soubory, načtěte každý obrázek a změňte jeho velikost tak, aby odpovídal plátnu TIFF. Změna velikosti před přidáním rámců snižuje spotřebu paměti a urychluje operaci ukládání. Převodem každého zdrojového obrázku na požadované rozměry a formát pixelů zajistíte konzistentní rozvržení stránek a vyhnete se chybám za běhu při připojování rámců k TIFF dokumentu.

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## Jak přidat každý obrázek jako rámec do vícestránkového TIFF?

`TiffFrame` je objekt, který v TIFF uchovává obrázek jedné stránky a související metadata. Procházejte změněné obrázky, vytvořte nový `TiffFrame` a připojte jej k `TiffImage`. Každý rámec se stane samostatnou stránkou ve finálním dokumentu a knihovna automaticky spravuje potřebné aktualizace metadat, jako je počet stránek a offsety, což zajišťuje platnou strukturu vícestránkového TIFF.

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## Jak uložit finální vícestránkový TIFF soubor?

Zavolejte metodu `save` na instanci `TiffImage` a předáte požadovanou výstupní cestu. Knihovna automaticky zapíše všechny rámce s kompresí CCITTFAX3, efektivně streamuje data na disk a uzavře všechny podkladové zdroje. Po dokončení operace ukládání obsahuje výsledný soubor všechny stránky s určenou kompresí, připravený k distribuci nebo archivaci.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## Praktické aplikace

- **Archivace dokumentů:** Ukládejte naskenované smlouvy, faktury nebo právní záznamy s minimálním úložným zatížením.  
- **Lékařské zobrazování:** Komprimujte radiologické snímky při zachování diagnostických detailů.  
- **Tisková produkce:** Generujte vícestránkové tiskové úlohy, které tiskárny mohou přímo zpracovat.

## Úvahy o výkonu

- Používejte `ResizeOptions`, které zachovávají poměr stran, aby nedošlo k deformaci.  
- Po přidání rámce zavřete každý objekt `Image`, aby se uvolnila nativní paměť.  
- Pro velmi velké dávky zpracovávejte soubory v paralelních streamech a zapisujte každý segment TIFF asynchronně.

## Časté úskalí a řešení problémů

- **Nesprávný formát pixelů:** CCITTFAX3 funguje pouze s 1‑bitovými (černobílými) obrázky. Před změnou velikosti převádějte barevné obrázky na odstíny šedi.  
- **Úniky paměti:** Vždy zavolejte `dispose()` na dočasných objektech `Image`; jinak zůstávají nativní buffery alokovány.  
- **Velikost souboru se nesnížila:** Ujistěte se, že je nastavená vlastnost komprese v `TiffOptions`; jinak se použije výchozí (žádná komprese).

## Často kladené otázky

**Q: Mohu tento přístup použít s barevnými obrázky?**  
A: CCITTFAX3 je omezen na monochromatická data; pro barvu použijte místo toho kompresi JPEG nebo LZW.

**Q: Podporuje Aspose.Imaging streamování pro obrovské TIFFy?**  
A: Ano—knihovna zapisuje každý rámec přímo do výstupního streamu, což udržuje nízké využití paměti i při tisících stránkách.

**Q: Jak aplikovat dočasnou licenci programově?**  
A: Načtěte soubor `.lic` pomocí `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.

**Q: Existuje způsob, jak si před uložením prohlédnout TIFF?**  
A: Můžete vykreslit každý `TiffFrame` do `BufferedImage` a zobrazit jej v komponentě Swing.

**Q: Které verze Javy jsou oficiálně podporovány?**  
A: Aspose.Imaging podporuje Java 8 až Java 21, včetně LTS verzí.

## Závěr

Nyní máte kompletní, připravený workflow pro tvorbu vícestránkových TIFF souborů s **ccittfax3 compression java** pomocí Aspose.Imaging. Dodržením výše uvedených kroků můžete efektivně archivovat obrovské kolekce dokumentů při nízkých nákladech na úložiště a vysoké kvalitě obrazu. Prozkoumejte další funkce Aspose.Imaging—jako OCR, práci s metadaty a konverzi formátů—abyste dále vylepšili svůj proces zpracování dokumentů.

---

**Poslední aktualizace:** 2026-09-28  
**Testováno s:** Aspose.Imaging 25.5 for Java  
**Autor:** Aspose

## Související tutoriály

- [Jak vytvořit vícestránkový TIFF s Aspose.Imaging pro Java – Kompletní průvodce](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Jak snížit velikost souboru obrázku pomocí LZW komprese v Javě](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Rozdělení vícestránkových TIFF rámců s Aspose.Imaging pro Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}