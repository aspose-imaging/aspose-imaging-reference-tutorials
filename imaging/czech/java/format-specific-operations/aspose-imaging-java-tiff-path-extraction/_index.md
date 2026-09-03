---
date: '2026-09-02'
description: Naučte se, jak vytvořit ořezovou cestu a extrahovat ji z TIFF obrázků
  pomocí Aspose.Imaging pro Java. Postupujte podle podrobných kroků k efektivní konverzi
  TIFF na PSD.
keywords:
- create clipping path
- how to extract path
- how to convert tiff
- aspose imaging java
- convert tiff to psd
lastmod: '2026-09-02'
og_description: Naučte se, jak vytvořit ořezovou cestu a extrahovat ji z TIFF obrázků
  pomocí Aspose.Imaging pro Java. Postupujte podle podrobného kódu k převodu TIFF
  na PSD.
og_image_alt: Guide showing how to create clipping path in TIFF using Aspose.Imaging
  Java
og_title: Vytvořte ořezovou cestu v TIFF pomocí Aspose.Imaging pro Java
schemas:
- author: Aspose
  dateModified: '2026-09-02'
  description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  headline: Create clipping path in TIFF with Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  name: Create clipping path in TIFF with Aspose.Imaging for Java
  steps:
  - name: '**Free trial** – start with a 30‑day trial.'
    text: '**Free trial** – start with a 30‑day trial.'
  - name: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
    text: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
  - name: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
    text: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
  - name: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
    text: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
  - name: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
    text: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
  type: HowTo
- questions:
  - answer: Yes, provided you have a valid commercial license; a free trial is available
      for evaluation.
    question: Can I use Aspose.Imaging for Java in a commercial application?
  - answer: The library supports over 100 formats, including TIFF, PSD, BMP, JPEG,
      PNG, and many more.
    question: What image formats does Aspose.Imaging support?
  - answer: Verify that the source TIFF actually contains vector path resources; use
      the `hasPathResources()` check before extraction.
    question: How do I troubleshoot path extraction errors?
  - answer: Absolutely – combine the extraction code with Java’s parallel streams
      or an executor service to handle many files efficiently.
    question: Is batch processing of multiple TIFFs possible?
  - answer: Complex shapes may need manual adjustment after creation; the API handles
      standard Bezier curves and straight lines reliably.
    question: Are there limitations when creating clipping paths in TIFF?
  type: FAQPage
tags:
- create clipping path
- TIFF processing
- Aspose.Imaging
- Java image manipulation
- PSD conversion
title: Vytvořte ořezovou cestu v TIFF pomocí Aspose.Imaging pro Java
url: /cs/java/format-specific-operations/aspose-imaging-java-tiff-path-extraction/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvoření ořezové cesty v TIFF pomocí Aspose.Imaging pro Java

V tomto komplexním průvodci se naučíte **jak vytvořit ořezovou cestu** v souboru TIFF a jak extrahovat existující cesty pomocí Aspose.Imaging pro Java. Na konci budete schopni převést TIFF obrázky na plně editovatelné PSD soubory, připravené pro Photoshop nebo jakýkoli editor podporující vektory.

## Rychlé odpovědi
- **Co je ořezová cesta?** Vektorový obrys, který určuje průhledné a neprůhledné oblasti obrázku.  
- **Mohu extrahovat existující cestu z TIFF?** Ano – Aspose.Imaging může číst vložené zdroje cest a uložit je jako PSD.  
- **Jak přidám novou ořezovou cestu?** Vytvořte `PathResource`, naplňte jej vektorovými záznamy a přiřaďte jej aktivnímu snímku obrázku.  
- **Potřebuji licenci pro produkční použití?** Platná licence Aspose.Imaging je vyžadována pro komerční nasazení.  
- **Jaká verze Javy je vyžadována?** JDK 8 nebo vyšší; knihovna funguje s Java 11, 17 a novějšími.

## Co je ořezová cesta?
Ořezová cesta je vektorový obrys, který říká vykreslovacím enginům, které části obrázku zobrazit nebo skrýt. Je uložena jako zdroj cesty uvnitř souborů TIFF nebo PSD a může být upravována v Adobe Photoshopu.

## Proč převádět TIFF na PSD?
Převod TIFF na PSD umožňuje bezztrátovou úpravu vrstev, masek a ořezových cest. Aspose.Imaging podporuje **více než 50 vstupních a výstupních formátů** a může zpracovávat více‑stovkové TIFFy bez načítání celého souboru do paměti, což poskytuje vysoce výkonný hromadný převod.

## Požadavky
- **Java Development Kit (JDK)** 8 nebo novější nainstalovaný.
- **Aspose.Imaging for Java** knihovna (přidejte přes Maven, Gradle nebo přímé stažení).  
- Základní znalost konceptů programování v Javě.

## Jak nastavit Aspose.Imaging pro Java
Před přidáním jakéhokoli kódu se ujistěte, že je knihovna správně odkazována ve vašem build systému a že máte platný licenční soubor. To zajišťuje, že API funguje bez omezení hodnocení a že jsou k dispozici všechny funkce, včetně manipulace s cestami.

### Maven
Přidejte následující závislost do souboru `pom.xml`:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle
Include this line in your `build.gradle` file:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Přímé stažení
Stáhněte nejnovější verzi z [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

#### Získání licence
1. **Free trial** – začněte s 30‑denní zkušební verzí.  
2. **Temporary license** – získejte ji na [temporary license page](https://purchase.aspose.com/temporary-license/).  
3. **Purchase** – zakupte plnou licenci na [Aspose's website](https://purchase.aspose.com/buy).

Jakmile je nainstalováno a licencováno, inicializujte Aspose.Imaging ve svém projektu:
```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path_to_license_file");
```

## Jak extrahovat ořezovou cestu z TIFF?
Extrahování ořezové cesty zahrnuje načtení TIFF, nalezení všech vložených zdrojů cest a zápis těchto zdrojů do nového PSD souboru. Proces čte vektorová data přímo ze zdrojového obrázku, zachovává přesnost a vyhýbá se rasterové konverzi.

Load the TIFF, iterate through its path resources, and save the result as a PSD. This operation reads the embedded vector data and writes it to a new file in a single pass.
```java
String filePath = "YOUR_DOCUMENT_DIRECTORY/SupportExtractingPathsFromTiff/Sample.tif";
try (TiffImage image = (TiffImage) com.aspose.imaging.Image.load(filePath)) {
    // Proceed with extraction steps...
}
```

Iterate through the path resources in the active frame and collect them:
```java
for (PathResource path : image.getActiveFrame().getPathResources()) {
    System.out.println(path.getName());  // Output the name of each path resource found.
}
```

Save the image with the extracted paths to a new PSD file:
```java
String outFilePath = "YOUR_OUTPUT_DIRECTORY/SampleWithPaths.psd";
image.save(outFilePath);
```

## Jak vytvořit ořezovou cestu v TIFF?
Vytvoření ořezové cesty vyžaduje konstrukci `PathResource`, který popisuje požadovaný vektorový obrys, jeho připojení k aktivnímu snímku TIFF a následné uložení obrázku (nebo kopie) jako PSD, aby cesta byla zachována. Tento přístup vám umožní programově přidávat vektorové masky k rastrovým souborům.

PathResource represents a vector path stored inside an image file.  
Initialize a new `PathResource` with the required attributes:
```java
final PathResource pathResource = new PathResource();
pathResource.setBlockId((short) 2000); // Set Block ID per Photoshop specs
pathResource.setName("My Clipping Path"); // Name your clipping path for easy identification

// Create and add vector path records using the provided coordinates.
pathResource.setRecords(createRecords(0.2f, 0.2f, 0.8f, 0.2f, 0.8f, 0.8f, 0.2f, 0.8f));
```

Assign the created path resource to the image’s active frame:
```java
List<PathResource> list = new LinkedList<>();
list.add(pathResource);
image.getActiveFrame().setPathResources(list);
```

Save the modified TIFF as a PSD that now contains the clipping path:
```java
String outFilePath2 = "YOUR_OUTPUT_DIRECTORY/ImageWithPath.psd";
image.save(outFilePath2);
```

## Pomocné metody

### Vytvořit záznamy
Generate vector path records using Bezier knots and length records:
```java
private static List<VectorPathRecord> createRecords(float ... coordinates) {
    List<VectorPathRecord> records = createBezierRecords(coordinates); 
    LengthRecord lr = new LengthRecord();
    lr.setOpen(false);
    lr.setRecordCount(records.size());
    
    records.add(0, lr);
    return records;
}
```

### Vytvořit Bezier záznamy
Convert coordinate arrays into Bezier vector path records:
```java
private static List<VectorPathRecord> createBezierRecords(float[] coordinates) {
    final List<VectorPathRecord> list = new LinkedList<>();
    
    for (int index = 0; index < coordinates.length - 1; index += 2) {
        PointF point = new PointF(coordinates[index], coordinates[index + 1]);
        list.add(createBezierRecord(point));
    }
    
    return list;
}
```

### Vytvořit Bezier záznam
Define a single Bezier knot vector path record:
```java
private static VectorPathRecord createBezierRecord(PointF point) {
    BezierKnotRecord it = new BezierKnotRecord();
    it.setPathPoints(new PointF[] { point, point, point });
    return it;
}
```

## Praktické aplikace
1. **Graphic design workflows** – Převod TIFF na PSD pro úpravu vrstev a masek v Photoshopu.  
2. **Automated image pipelines** – Hromadně zpracovávejte tisíce TIFFů, extrahujte nebo přidávejte cesty za běhu.  
3. **Data‑driven visualizations** – Použijte vektorové cesty k vytvoření přesných grafů nebo schémat z rastrových zdrojů.

## Úvahy o výkonu
- **Memory management** – Použijte try‑with‑resources k zajištění rychlého uvolnění objektů obrázku.  
- **Batch processing** – Paralelizujte převody pomocí Java `ForkJoinPool` pro velké sady obrázků.  
- **Resolution handling** – Upravit DPI pouze v případě potřeby, aby byl čas zpracování nízký a zachována kvalita.

## Závěr
Nyní víte, jak **vytvořit ořezovou cestu** v TIFF souborech a extrahovat existující cesty pomocí Aspose.Imaging pro Java. Tyto techniky vám umožní integrovat pokročilou manipulaci s obrázky do jakéhokoli Java‑založeného pracovního postupu, od desktopových nástrojů po podnikovou úroveň zpracování.

### Další kroky
- Experimentujte s různými vektorovými tvary a atributy cesty.  
- Prozkoumejte další funkce Aspose.Imaging, jako je vodoznakování, konverze formátů a správa metadat.

## Často kladené otázky

**Q: Mohu použít Aspose.Imaging pro Java v komerční aplikaci?**  
A: Ano, pokud máte platnou komerční licenci; k hodnocení je k dispozici bezplatná zkušební verze.

**Q: Jaké formáty obrázků Aspose.Imaging podporuje?**  
A: Knihovna podporuje více než 100 formátů, včetně TIFF, PSD, BMP, JPEG, PNG a mnoha dalších.

**Q: Jak řešit chyby při extrakci cesty?**  
A: Ověřte, že zdrojový TIFF skutečně obsahuje vektorové zdroje cest; před extrakcí použijte kontrolu `hasPathResources()`.

**Q: Je hromadné zpracování více TIFFů možné?**  
A: Rozhodně – kombinujte kód pro extrakci s Java paralelními streamy nebo executor službou pro efektivní zpracování mnoha souborů.

**Q: Existují omezení při vytváření ořezových cest v TIFF?**  
A: Složitější tvary mohou vyžadovat ruční úpravu po vytvoření; API spolehlivě zvládá standardní Bezierovy křivky a přímé linie.

---

**Poslední aktualizace:** 2026-09-02  
**Testováno s:** Aspose.Imaging for Java 24.12  
**Autor:** Aspose  

## Zdroje

- [Dokumentace Aspose.Imaging](https://reference.aspose.com/imaging/java/)
- [Stáhnout Aspose.Imaging pro Java](https://releases.aspose.com/imaging/java/)
- [Koupit licenci](https://purchase.aspose.com/buy)
- [Bezplatná zkušební verze](https://releases.aspose.com/imaging/java/)
- [Dočasná licence](https://purchase.aspose.com/temporary-license/)
- [Fórum podpory Aspose](https://forum.aspose.com/c/imaging/14)

## Související tutoriály

- [Převod obrázku na PSD pomocí Aspose.Imaging pro Java – krok za krokem průvodce](/imaging/java/format-conversion-export/convert-images-to-psd-using-aspose-imaging-java-guide/)
- [Jak převést TIFF na GraphicsPath pomocí Aspose.Imaging Java](/imaging/java/advanced-drawing-graphics/aspose-imaging-java-tiff-graphicspath-conversion/)
- [Efektivní načítání a ukládání TIFF obrázků v Javě s Aspose.Imaging](/imaging/java/image-loading-saving/aspose-imaging-java-tiff-image-saving/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}