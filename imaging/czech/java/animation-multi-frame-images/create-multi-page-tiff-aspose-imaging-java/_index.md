---
date: '2026-11-16'
description: Naučte se, jak vytvořit multi page tiff s Aspose.Imaging for Java. Převádějte
  obrázky do tiff, kombinujte snímky a optimalizujte úložiště v jednom průvodci.
keywords:
- create multi page tiff
- convert images to tiff
- aspose imaging java
- java image processing tutorial
- multi-page tiff generation
lastmod: '2026-11-16'
og_description: Vytvořte multi page tiff pomocí Aspose.Imaging for Java. Tento krok‑za‑krokem
  průvodce ukazuje, jak převést obrázky do tiff, přidat snímky a optimalizovat úložiště.
og_image_alt: 'Developer guide: create multi page tiff using Aspose.Imaging for Java'
og_title: Vytvořte multi page tiff s Aspose.Imaging for Java
schemas:
- author: Aspose
  dateModified: '2026-11-16'
  description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  headline: How to create multi page tiff using Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  name: How to create multi page tiff using Aspose.Imaging for Java
  steps:
  - name: load an image
    text: '`Image.load` reads the image file into memory and returns an `Image` object
      that you can manipulate. Ensure the file path is correct to avoid `FileNotFoundException`.'
  - name: resize the image
    text: '`ResizeType.NearestNeighbourResample` preserves hard edges and pixel data,
      which is ideal when you need a faithful representation of scanned documents.'
  - name: set up TIFF options
    text: '`TiffOptions` defines the compression, bits per pixel, and other TIFF‑specific
      settings. The `source` property points to the file where the multi‑page TIFF
      will be saved.'
  - name: initialize the TIFF image
    text: '`TiffImage.create` creates an empty TIFF container with the width and height
      derived from the first resized image. This container will later hold each frame
      you add.'
  - name: load additional images
    text: The loop iterates over every file ending with `.img` (or any supported raster
      format) in the target directory, loads each image, and calls `savePixels` to
      copy pixel data into a new frame of the TIFF.
  - name: save your work
    text: '`image.save` writes the complete multi‑page TIFF to the output path you
      specified in `TiffOptions`. Verify that the directory is writable to avoid `IOException`.'
  type: HowTo
- questions:
  - answer: Absolutely. Load any supported raster format (PNG, JPEG, BMP, etc.) and
      add each as a frame using the same workflow.
    question: Can I convert PNG or JPEG files to a multi‑page TIFF with this approach?
  - answer: Yes. Call `tiffOptions.setCompression(TiffCompression.Lzw)` before creating
      the image to reduce file size while preserving quality.
    question: Is it possible to set compression (e.g., LZW) for the output TIFF?
  - answer: Use `frame.getMetadata().addProperty("Author", "Your Name")` after creating
      the frame and before saving.
    question: How do I add metadata (author, description) to each TIFF frame?
  - answer: It does. Load the file with `Image.load("existing.tiff")` and iterate
      through `((TiffImage)image).getFrames()` to access each page.
    question: Does Aspose.Imaging support reading existing multi‑page TIFFs?
  - answer: Process pages in batches, call `System.gc()` periodically, and use the
      try‑with‑resources pattern to release native memory promptly.
    question: What if I need to process thousands of pages?
  type: FAQPage
tags:
- create multi page tiff
- Aspose.Imaging
- Java image processing
- TIFF conversion
title: Jak vytvořit multi page tiff pomocí Aspose.Imaging for Java
url: /cs/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak vytvořit vícestránkový tiff pomocí Aspose.Imaging pro Java

## Úvod

Vytvoření **multi page tiff** je běžnou potřebou, když potřebujete archivovat několik souvisejících obrázků v jednom kompaktním souboru. Ať už budujete systém pro správu dokumentů, pipeline pro medicínské zobrazování nebo nástroj pro dávkové zpracování, Aspose.Imaging pro Java vám poskytuje plnou kontrolu nad tvorbou TIFF, kompresí a manipulací s rámci. V tomto průvodci se naučíte, jak načíst, změnit velikost a sloučit více obrázků do jednoho vícestránkového TIFF, přičemž udržíte nízkou spotřebu paměti a vysoký výkon.

**Co se naučíte**
- Načíst a změnit velikost obrázků pomocí Aspose.Imaging.
- Konfigurovat `TiffOptions` pro vícestránkový výstup.
- Přidat rámy z několika zdrojových obrázků.
- Uložit finální TIFF s volitelnou kompresí.
- Reálné scénáře, kde se vícestránkové TIFFy uplatní.

## Rychlé odpovědi
- **Jaká je hlavní knihovna?** Aspose.Imaging for Java.  
- **Mohu převést obrázky na tiff?** Ano – tutoriál ukazuje, jak sloučit PNG, JPEG, BMP a další formáty do vícestránkového TIFF.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro hodnocení; pro produkční použití je vyžadována trvalá licence.  
- **Jaká verze Javy je vyžadována?** Java 8 nebo vyšší (JDK 8+).  
- **Je kód thread‑safe?** Příklad běží v jednom vlákně; pro souběžné scénáře spravujte objekty `Image` na vlákno.

## Jak vytvořit vícestránkový tiff?

Načtěte své zdrojové obrázky, v případě potřeby změňte jejich velikost, nakonfigurujte `TiffOptions`, přidejte každý obrázek jako rám a zavolejte `save`. Tento stručný postup vytvoří standardy splňující vícestránkový TIFF během několika řádků Java kódu a umožní vám kontrolovat kompresi a rozměry stránek.

## Co je vícestránkový TIFF?

Vícestránkový TIFF je jeden TIFF soubor, který obsahuje několik obrazových rámců, z nichž každý představuje stránku. Je široce používán pro archivaci, fax a aplikace skenování dokumentů, protože ukládá mnoho stránek bez režie samostatných souborů.

## Požadavky

- Knihovna **Aspose.Imaging for Java** (stáhněte z odkazů níže).  
- **JDK 8+** nainstalováno a nakonfigurováno ve vašem IDE (IntelliJ IDEA, Eclipse, atd.).  
- Základní znalost Javy a povědomí o práci se soubory (I/O).

## Nastavení Aspose.Imaging pro Java

Abyste mohli začít pracovat s Aspose.Imaging, musíte jej integrovat do svého projektu. Zde je návod, jak to provést pomocí populárních nástrojů pro sestavení:

**Maven:**  
Přidejte následující závislost do vašeho `pom.xml`:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle:**  
Zahrňte toto do souboru `build.gradle`:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

Případně můžete **přímo stáhnout** nejnovější JAR Aspose.Imaging pro Java z [Aspose releases](/imaging/java/).

### Získání licence

Můžete začít s bezplatnou zkušební verzí a prozkoumat funkce Aspose.Imaging. Pro delší používání zvažte získání dočasné licence nebo zakoupení plné licence:
- **Bezplatná zkušební verze:** Navštivte [Aspose Imaging Java Releases](/imaging/java/) a stáhněte si knihovnu k vyzkoušení.  
- **Dočasná licence:** Získejte ji na [Aspose Temporary License Page](/purchase/temporary-license/).  
- **Nákup:** Pro trvalé řešení přejděte na [Aspose Purchase](/purchase/buy).

## Načtení a změna velikosti obrázku

**Přehled:**  
Prvním krokem je načtení obrázku ze souborového systému a změna jeho velikosti pomocí metody nejbližšího souseda (nearest‑neighbor resample).

#### Krok 1: načíst obrázek
`Image.load` načte soubor obrázku do paměti a vrátí objekt `Image`, který můžete manipulovat. Ujistěte se, že cesta k souboru je správná, aby nedošlo k `FileNotFoundException`.  
```java
import com.aspose.imaging.Image;

String dataDir = "YOUR_DOCUMENT_DIRECTORY";
Image tempImage = Image.load(dataDir + "/Image1.png");
```

#### Krok 2: změnit velikost obrázku
`ResizeType.NearestNeighbourResample` zachovává ostré hrany a pixelová data, což je ideální, když potřebujete věrnou reprezentaci skenovaných dokumentů.  
```java
int width = tempImage.getWidth();
int height = tempImage.getHeight();
tempImage.resize(width, height, ResizeType.NearestNeighbourResample);
```

## Vytvoření TIFF možností a zdroje

**Přehled:**  
Poté nastavíme potřebné možnosti pro vytvoření nového vícestránkového TIFF souboru. To zahrnuje specifikaci očekávaného formátu a konfiguraci zdroje.

#### Krok 1: nastavit TIFF možnosti
`TiffOptions` definuje kompresi, počet bitů na pixel a další nastavení specifické pro TIFF. Vlastnost `source` ukazuje na soubor, do kterého bude vícestránkový TIFF uložen.  
```java
import com.aspose.imaging.fileformats.tiff.TiffOptions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.sources.FileCreateSource;

TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setSource(new FileCreateSource("YOUR_DOCUMENT_DIRECTORY/MultiPage.tiff", false));
```

## Vytvoření a inicializace vícestránkového TIFF obrázku

**Přehled:**  
Nyní vytvoříme instanci vícestránkového TIFF obrázku s určenými rozměry.

#### Krok 1: inicializovat TIFF obrázek
`TiffImage.create` vytvoří prázdný TIFF kontejner se šířkou a výškou odvozenou z prvního změněného obrázku. Tento kontejner později bude obsahovat každý přidaný rám.  
```java
import com.aspose.imaging.fileformats.tiff.TiffImage;

TiffImage tiffImage = (TiffImage) Image.create(tiffOptions, width, height);
```

## Zpracování více obrázků a přidávání rámů do TIFF

**Přehled:**  
Tato sekce zahrnuje přidání více obrázků jako rámů do vašeho vícestránkového TIFF souboru.

#### Krok 1: načíst další obrázky
Cykly procházejí každý soubor končící na `.img` (nebo jakýkoli podporovaný rastrový formát) v cílovém adresáři, načtou každý obrázek a zavolají `savePixels` pro zkopírování pixelových dat do nového rámu TIFF.  
```java
import java.io.File;
import java.io.FilenameFilter;
import com.aspose.imaging.fileformats.tiff.TiffFrame;

File di = new File(dataDir);
String[] files = di.list(new FilenameFilter() {
    @Override
    public boolean accept(File dir, String name) {
        return name.endsWith(".img");
    }
});

if (files != null) {
    int index = 0;
    for (String file : files) {
        try (Image inputImage = Image.load(dataDir + "/" + file)) {
            if (index > 0) {
                TiffFrame newframe = new TiffFrame(tiffOptions, width, height);
                tiffImage.addFrame(newframe);
            }
            TiffFrame frame = tiffImage.getFrames()[index];
            frame.savePixels(frame.getBounds(), ((RasterImage) inputImage).loadPixels(inputImage.getBounds()));
            index += 1;
        }
    }
}
```

## Uložení vícestránkového TIFF obrázku

**Přehled:**  
Nakonec uložte svůj vícestránkový TIFF soubor, aby se zachovaly všechny změny provedené během zpracování.

#### Krok 1: uložit práci
`image.save` zapíše kompletní vícestránkový TIFF na výstupní cestu, kterou jste zadali v `TiffOptions`. Ověřte, že adresář je zapisovatelný, aby nedošlo k `IOException`.  
```java
import com.aspose.imaging.examples.Utils;

tiffImage.save("YOUR_OUTPUT_DIRECTORY/output.tiff");
```

## Praktické aplikace

Porozumění tomu, jak **převádět obrázky na tiff** pomocí Aspose.Imaging pro Java, může být užitečné v několika reálných scénářích:
1. **Archivní projekty:** Uložit stovky skenovaných stránek do jednoho souboru, snížit nepořádek v souborovém systému a zjednodušit zálohovací strategie.
2. **Lékařské zobrazování:** Kombinovat řezy CT, MRI nebo rentgenové snímky do jednoho vícestránkového TIFF pro snadný přenos mezi systémy.
3. **Správa dokumentů:** Uchovávat verzované PDF, skenované smlouvy nebo faktury společně, což umožňuje rychlejší vyhledávání a tisk.

Možnosti integrace zahrnují propojení této funkčnosti s cloudovými úložišti jako AWS S3 nebo Azure Blob Storage, což umožňuje automatizované archivní pipeline.

## Úvahy o výkonu

V práci s knihovnami pro zpracování obrázků v Javě:
- **Změňte velikost před přidáním rámů** – snižuje paměťovou stopu až o 60 % u vysoce rozlišených skenů.
- **Používejte streaming API** – Aspose.Imaging může zpracovávat obrázky po částech, což pomáhá při práci s TIFFy s více než 500 stránkami.
- **Okamžitě uvolňujte objekty Image** – obalte použití do `try (Image img = Image.load(...)) { … }`, aby se automaticky uvolnily nativní zdroje.

## Proč používat Aspose.Imaging pro Java?

Aspose.Imaging podporuje **50+** vstupních a výstupních formátů, včetně PNG, JPEG, BMP, GIF a TIFF, a dokáže zpracovávat více než stovky stránek TIFF souborů bez načítání celého dokumentu do paměti. Benchmarky ukazují 30 % snížení využití CPU ve srovnání s nativním Java ImageIO při zpracování velkých dávek.

## Často kladené otázky

**Q: Můžu převést soubory PNG nebo JPEG na vícestránkový TIFF tímto postupem?**  
A: Rozhodně. Načtěte jakýkoli podporovaný rastrový formát (PNG, JPEG, BMP, atd.) a přidejte každý jako rám pomocí stejného pracovního postupu.

**Q: Je možné nastavit kompresi (např. LZW) pro výstupní TIFF?**  
A: Ano. Zavolejte `tiffOptions.setCompression(TiffCompression.Lzw)` před vytvořením obrázku, aby se snížila velikost souboru při zachování kvality.

**Q: Jak přidat metadata (autor, popis) ke každému rámu TIFF?**  
A: Použijte `frame.getMetadata().addProperty("Author", "Your Name")` po vytvoření rámu a před uložením.

**Q: Podporuje Aspose.Imaging čtení existujících vícestránkových TIFF?**  
A: Ano. Načtěte soubor pomocí `Image.load("existing.tiff")` a iterujte přes `((TiffImage)image).getFrames()` pro přístup k jednotlivým stránkám.

**Q: Co když potřebuji zpracovat tisíce stránek?**  
A: Zpracovávejte stránky po dávkách, periodicky volajte `System.gc()` a používejte vzor try‑with‑resources pro rychlé uvolnění nativní paměti.

## Zdroje

- [Dokumentace Aspose.Imaging pro Java](/reference/imaging/java/)
- [Stáhnout nejnovější verzi](/imaging/java/)
- [Možnosti nákupu licence](/purchase/buy)
- [Aspose Nákup](/purchase/buy)
- [Začít s bezplatnou zkušební verzí](/imaging/java/)
- [Informace o dočasné licenci](/purchase/temporary-license/)
- [Komunitní podpora a fóra](/forum/imaging/14)

Využitím těchto zdrojů můžete prohloubit své porozumění Aspose.Imaging pro Java a efektivně jej aplikovat ve svých projektech. Šťastné programování!

---

**Last Updated:** 2026-11-16  
**Tested With:** Aspose.Imaging for Java 25.5  
**Author:** Aspose

```java
// Example: load and save a TIFF
Image img = Image.load("input.png");
img.save("output.tiff");
```

## Související tutoriály

- [Převod více‑rámcového TIFF na JPEG pomocí Aspose.Imaging pro Java – Kompletní průvodce](/imaging/java/image-loading-saving/convert-multi-frame-tiff-to-jpeg-aspose-imaging-java/)
- [Rozdělení rámů vícestránkového TIFF pomocí Aspose.Imaging pro Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)
- [aspose imaging java – Převod TIFF na BMP rámy](/imaging/java/animation-multi-frame-images/extract-tiff-frames-to-bmp-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}