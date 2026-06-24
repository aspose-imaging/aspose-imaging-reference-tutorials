---
date: 2026-05-18
description: Naučte se, jak používat Java knihovnu pro zpracování obrazu Aspose.Imaging
  k vložení a načtení XMP metadat v obrázcích, s krok za krokem kódem.
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: Zpracování XMP dat v obrázcích
schemas:
- author: Aspose
  dateModified: '2026-05-18'
  description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  headline: 'Java Image Processing Library: XMP with Aspose.Imaging'
  type: TechArticle
- description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  name: 'Java Image Processing Library: XMP with Aspose.Imaging'
  steps:
  - name: Specify Image Size and Tiff Options
    text: First, define the directory where your image will be stored and create a
      `Rectangle` to specify the size of the image. In this example, we use a TIFF
      image with certain options. `TiffOptions` configures format‑specific settings
      for the TIFF image.
  - name: Create a New Image
    text: Now, create a new image with the specified options. This image will be used
      to store the XMP metadata. `TiffImage` represents a TIFF image object, and `TiffFrame`
      defines an individual frame within it.
  - name: Create XMP Header and Trailer
    text: Create instances of XMP‑Header and XMP‑Trailer for your XMP metadata. These
      headers and trailers help define the metadata structure. `XmpHeaderPi` and `XmpTrailerPi`
      represent the XMP packet’s opening and closing sections.
  - name: Create XMP Meta Information
    text: Now, create an instance of XMP meta to set different attributes. You can
      add information like the author and description. `XmpMeta` holds the core metadata
      fields such as author and description.
  - name: Create XMP Packet Wrapper
    text: '`XmpPacketWrapper` is the container that holds the XMP header, trailer,
      and meta information in a single packet. It ensures the packet conforms to the
      XMP specification. `XmpPacketWrapper` packages the header, meta, and trailer
      into a single XMP packet.'
  - name: Add Photoshop Package
    text: To store Photoshop‑specific information, create a Photoshop package and
      set its attributes, such as city, country, and color mode. Then, add this package
      to the XMP metadata. `PhotoshopPackage` stores Photoshop‑specific metadata like
      city, country, and color mode.
  - name: Add Dublin Core Package
    text: For more general information, like author, title, and additional values,
      create a DublinCore package and set its attributes. Add this package to the
      XMP metadata as well. `DublinCorePackage` contains standard Dublin Core fields
      such as title, creator, and keywords.
  - name: Update XMP Metadata in the Image
    text: Update the XMP metadata into the image using the `setXmpData` method. This
      call writes the XMP packet into the image’s metadata section. `setXmpData` writes
      the XMP packet into the image’s metadata section.
  - name: Save the Image
    text: You can now save the image with the embedded XMP metadata on the disk or
      in a memory stream.
  - name: Load the Image and Retrieve XMP Metadata
    text: To retrieve the XMP metadata from the image, load the image from the memory
      stream or disk and access the XMP data via the `getXmpData` method. `getXmpData`
      reads the embedded XMP packet from the image. Congratulations! You've successfully
      learned how to handle XMP data in images using Aspose.Imagin
  type: HowTo
- questions:
  - answer: XMP is an XML‑based standard for embedding descriptive information directly
      inside files, enabling consistent metadata across applications.
    question: What is XMP metadata?
  - answer: It lets you tag images with author, copyright, keywords, and custom data,
      improving searchability and asset management without external databases.
    question: Why is XMP metadata important?
  - answer: Yes, Aspose.Imaging for Java provides methods to modify existing XMP packets
      and write them back to the file.
    question: Can I edit XMP metadata after embedding it in an image?
  - answer: A free trial is available for evaluation, but a paid license is required
      for production use. You can explore options on the [Aspose.Imaging for Java
      website](https://purchase.aspose.com/buy).
    question: Is Aspose.Imaging for Java a free tool?
  - answer: Visit the [Aspose.Imaging forums](https://forum.aspose.com/) for community
      assistance, or contact Aspose support directly for paid‑license customers.
    question: Where can I get help and support for Aspose.Imaging for Java?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: 'Java knihovna pro zpracování obrazu: XMP s Aspose.Imaging'
url: /cs/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Zpracování dat XMP v obrázcích pomocí Aspose.Imaging pro Java

Aspose.Imaging je **java image processing library**, která vám umožní pracovat s desítkami rastrových a vektorových formátů. V tomto tutoriálu se naučíte, jak pomocí Aspose.Imaging pro Java vložit a načíst data XMP (Extensible Metadata Platform) do obrázků. Na konci budete schopni uložit autora, popis a vlastní metadata přímo do souborů obrázků, což je učiní prohledávatelnými a samopopisnými.

## Rychlé odpovědi
- **What is XMP?** XMP je standardizovaný formát založený na XML pro vkládání metadat do souborů, jako jsou obrázky, PDF a videa.  
- **Which library handles XMP in Java?** Aspose.Imaging pro Java poskytuje kompletní API pro čtení a zápis XMP paketů.  
- **Do I need a license?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **How many image formats are supported?** Více než 150 formátů, včetně TIFF, JPEG, PNG, PSD a RAW.  
- **Can I process large images?** Ano – knihovna dokáže zpracovat soubory až do 2 GB, aniž by načetla celý obrázek do paměti.

## Co jsou metadata XMP?
Metadata XMP je standard založený na XML, který vkládá popisné informace přímo do digitálních souborů. Umožňuje jednotné ukládání autora, autorských práv, klíčových slov a vlastních dat napříč aplikacemi. Protože je založen na XML, lze XMP rozšířit o vlastní jmenné prostory, což vývojářům umožňuje přidávat proprietární pole a zároveň zůstávat kompatibilní s nástroji, které rozumí základnímu schématu. To činí XMP ideálním pro dlouhodobou správu aktiv a interoperabilitu mezi aplikacemi.

## Proč použít Java knihovnu pro zpracování obrázků pro XMP?
Aspose.Imaging pro Java podporuje **150+ image formats** a dokáže zpracovávat soubory o velikosti několika gigabajtů ve streamovacím režimu, čímž snižuje spotřebu paměti až o 80 % ve srovnání s naivním načítáním. API také zaručuje, že XMP pakety zůstávají v souladu se standardy, což zajišťuje kompatibilitu s Adobe Photoshop, Lightroom a dalšími nástroji.

## Předpoklady

- Na vašem počítači je nastavené vývojové prostředí Java.  
- Knihovna Aspose.Imaging pro Java nainstalována. Můžete si ji stáhnout z [Aspose.Imaging for Java website](https://releases.aspose.com/imaging/java/).  
- Základní znalost programování v Javě.

## Importování balíčků

Začněte importováním potřebných balíčků do vašeho Java projektu. Můžete přidat následující importy na začátek vašeho kódu:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.xmp.XmpPackage;
import com.aspose.imaging.xmp.XmpPacketWrapper;
import com.aspose.imaging.xmp.XmpMeta;
import com.aspose.imaging.xmp.photoshop.ColorMode;
import com.aspose.imaging.xmp.photoshop.PhotoshopPackage;
import com.aspose.imaging.xmp.dc.DublinCorePackage;
import com.aspose.imaging.xmp.header.XmpHeaderPi;
import com.aspose.imaging.xmp.trailer.XmpTrailerPi;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Nyní rozdělíme příklad do krok‑za‑krokem průvodce:

## Jak vložit metadata XMP pomocí Java knihovny pro zpracování obrázků?

Načtěte svůj obrázek, vytvořte XMP paket, připojte paket k obrázku a uložte – vše v několika stručných řádcích. Metoda `setXmpData` z Aspose.Imaging zapisuje paket přímo do souboru, aniž by vyžadovala samostatný soubor s metadaty. Proces funguje jak s obrázky založenými na souborech, tak s těmi založenými na streamu, což jej činí vhodným pro webové služby a dávkové úlohy.

### Krok 1: Určete velikost obrázku a možnosti TIFF

Nejprve definujte adresář, kde bude váš obrázek uložen, a vytvořte `Rectangle` pro určení velikosti obrázku. V tomto příkladu používáme TIFF obrázek s určitými možnostmi. `TiffOptions` konfiguruje nastavení specifická pro formát TIFF.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### Krok 2: Vytvořte nový obrázek

Nyní vytvořte nový obrázek s určenými možnostmi. Tento obrázek bude použit k uložení XMP metadat. `TiffImage` představuje objekt TIFF obrázku a `TiffFrame` definuje jednotlivý rámec v něm.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### Krok 3: Vytvořte XMP hlavičku a patu

Vytvořte instance XMP‑Header a XMP‑Trailer pro vaše XMP metadata. Tyto hlavičky a paty pomáhají definovat strukturu metadat. `XmpHeaderPi` a `XmpTrailerPi` představují úvodní a závěrné sekce XMP paketu.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### Krok 4: Vytvořte XMP meta informace

Nyní vytvořte instanci XMP meta pro nastavení různých atributů. Můžete přidat informace jako autor a popis. `XmpMeta` obsahuje základní pole metadat, jako je autor a popis.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### Krok 5: Vytvořte XMP Packet Wrapper

`XmpPacketWrapper` je kontejner, který v jednom paketu drží XMP hlavičku, patu a meta informace. Zajišťuje, že paket odpovídá specifikaci XMP. `XmpPacketWrapper` balí hlavičku, meta a patu do jednoho XMP paketu.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### Krok 6: Přidejte Photoshop balíček

Pro uložení specifických informací Photoshopu vytvořte Photoshop balíček a nastavte jeho atributy, jako je město, země a režim barev. Poté tento balíček přidejte do XMP metadat. `PhotoshopPackage` ukládá specifická metadata Photoshopu, jako je město, země a režim barev.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### Krok 7: Přidejte Dublin Core balíček

Pro obecnější informace, jako je autor, název a další hodnoty, vytvořte DublinCore balíček a nastavte jeho atributy. Tento balíček také přidejte do XMP metadat. `DublinCorePackage` obsahuje standardní pole Dublin Core, jako je název, tvůrce a klíčová slova.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### Krok 8: Aktualizujte XMP metadata v obrázku

Aktualizujte XMP metadata v obrázku pomocí metody `setXmpData`. Toto volání zapíše XMP paket do sekce metadat obrázku. `setXmpData` zapisuje XMP paket do sekce metadat obrázku.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### Krok 9: Uložte obrázek

Nyní můžete uložit obrázek s vloženými XMP metadaty na disk nebo do paměťového streamu.

```java
    image.save(ms);
```

### Krok 10: Načtěte obrázek a načtěte XMP metadata

Pro načtení XMP metadat z obrázku načtěte obrázek z paměťového streamu nebo disku a přistupte k XMP datům pomocí metody `getXmpData`. `getXmpData` čte vložený XMP paket z obrázku.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

Gratulujeme! Úspěšně jste se naučili, jak zpracovávat data XMP v obrázcích pomocí Aspose.Imaging pro Java. To vám umožní ukládat a načítat cenná metadata ve vašich souborech obrázků.

## Časté problémy a řešení

- **Metadata not appearing in Photoshop:** Ujistěte se, že XMP paket odpovídá správnému XML schématu; Aspose.Imaging jej automaticky validuje, ale vlastní jmenné prostory mohou vyžadovat registraci.  
- **Large TIFF files cause OutOfMemoryError:** Použijte `TiffOptions` s `Compression` nastaveným na `LZW` a povolte streamování (`loadOptions.setBufferSize`), aby se spotřeba paměti udržela nízká.  
- **Unexpected character encoding:** XMP očekává UTF‑8; vždy předávejte řetězce pomocí `StandardCharsets.UTF_8`, aby nedošlo k poškození dat.

## Často kladené otázky

**Q: Co jsou XMP metadata?**  
A: XMP je standard založený na XML pro vkládání popisných informací přímo do souborů, což umožňuje jednotná metadata napříč aplikacemi.

**Q: Proč jsou XMP metadata důležitá?**  
A: Umožňují označit obrázky autorem, autorskými právy, klíčovými slovy a vlastními daty, což zlepšuje vyhledatelnost a správu aktiv bez externích databází.

**Q: Mohu upravit XMP metadata po jejich vložení do obrázku?**  
A: Ano, Aspose.Imaging pro Java poskytuje metody pro úpravu existujících XMP paketů a jejich zápis zpět do souboru.

**Q: Je Aspose.Imaging pro Java zdarma?**  
A: K dispozici je bezplatná zkušební verze pro vyhodnocení, ale pro produkční použití je vyžadována placená licence. Možnosti můžete prozkoumat na [Aspose.Imaging for Java website](https://purchase.aspose.com/buy).

**Q: Kde mohu získat pomoc a podporu pro Aspose.Imaging pro Java?**  
A: Navštivte [Aspose.Imaging forums](https://forum.aspose.com/) pro komunitní pomoc, nebo kontaktujte přímo podporu Aspose pro zákazníky s placenou licencí.

## Závěr

V tomto tutoriálu jsme prozkoumali, jak pracovat s XMP metadaty v obrázcích pomocí Aspose.Imaging pro Java, přední **java image processing library**. Dodržením krok‑za‑krokem průvodce můžete snadno vkládat, aktualizovat a načítat XMP data, čímž obohatíte své digitální aktiva o vyhledávatelná metadata v souladu se standardy.

---

**Last Updated:** 2026-05-18  
**Tested With:** Aspose.Imaging for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Mistrovství v Java zpracování obrázků: Úprava EXIF dat pomocí Aspose.Imaging](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [Java zpracování obrázků s Aspose.Imaging: Načítání, vylepšování a ukládání obrázků](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [Pokročilé Java zpracování obrázků s knihovnou Aspose.Imaging](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Specify the size of image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// create the brand new image just for sample purposes
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// create an instance of XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// create an instance of Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// create an instance of XMP meta class to set different attributes
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// create an instance of XmpPacketWrapper that contains all metadata
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// create an instance of Photoshop package and set photoshop attributes
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// add photoshop package into XMP metadata
	xmpData.addPackage(photoshopPackage);
	// create an instance of DublinCore package and set dublinCore attributes
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// add dublinCore Package into XMP metadata
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// update XMP metadata into image
	image.setXmpData(xmpData);
	// Save image on the disk or in memory stream
	image.save(ms);
	// Load the image from memory stream or from disk to read/get the metadata
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Getting the XMP metadata
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Use package data ...
		}
	}
}
        
```