---
"description": "Naučte se, jak pracovat s metadaty XMP v obrázcích pomocí Aspose.Imaging pro Javu. Vkládejte a načítejte metadata pro vylepšení obrazových souborů."
"linktitle": "Zpracování dat XMP v obrazech"
"second_title": "API pro zpracování obrazu v Javě Aspose.Imaging"
"title": "Zpracování dat XMP v obrazech pomocí Aspose.Imaging pro Javu"
"url": "/cs/java/document-conversion-and-processing/xmp-data-handling-in-images/"
"weight": 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Zpracování dat XMP v obrazech pomocí Aspose.Imaging pro Javu

Aspose.Imaging pro Javu je všestranná a výkonná knihovna pro práci s obrázky v různých formátech. Tento tutoriál vás provede procesem zpracování dat XMP (Extensible Metadata Platform) v obrázcích pomocí knihovny Aspose.Imaging pro Javu. XMP je standard pro vkládání metadat do obrazových souborů, který umožňuje ukládat cenné informace, jako je autor, popis a další.

## Předpoklady

Než začnete, ujistěte se, že máte splněny následující předpoklady:

- Vývojové prostředí Java nastavené na vašem počítači.
- Je nainstalována knihovna Aspose.Imaging pro Javu. Můžete si ji stáhnout z [Web Aspose.Imaging pro Javu](https://releases.aspose.com/imaging/java/).
- Základní znalost programování v Javě.

## Import balíčků

Začněte importem potřebných balíčků do vašeho projektu Java. Na začátek kódu můžete přidat následující příkazy importu:

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

Nyní si tento příklad rozdělme do podrobného návodu:

## Krok 1: Zadejte velikost obrázku a možnosti formátu TIFF

Nejprve definujte adresář, kam bude váš obrázek uložen, a vytvořte obdélník, který určí velikost obrázku. V tomto příkladu používáme obrázek Tiff s určitými možnostmi.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## Krok 2: Vytvořte nový obrázek

Nyní vytvořte nový obraz se zadanými možnostmi. Tento obraz bude použit k uložení metadat XMP.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## Krok 3: Vytvořte hlavičku a upoutávku XMP

Vytvořte instance XMP-Header a XMP-Trailer pro vaše metadata XMP. Tyto hlavičky a trailery pomáhají definovat strukturu metadat.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Krok 4: Vytvoření meta informací XMP

Nyní vytvořte instanci XMP meta pro nastavení různých atributů. Můžete přidat informace, jako je autor a popis.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Krok 5: Vytvoření obalovacího modulu XMP paketů

Vytvořte instanci třídy XmpPacketWrapper, která obsahuje hlavičku, upoutávku a meta informace XMP.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Krok 6: Přidání balíčku Photoshopu

Chcete-li ukládat informace specifické pro Photoshop, vytvořte balíček Photoshopu a nastavte jeho atributy, jako je město, země a barevný režim. Poté tento balíček přidejte do metadat XMP.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## Krok 7: Přidání balíčku Dublin Core

Pro obecnější informace, jako je autor, název a další hodnoty, vytvořte balíček DublinCore a nastavte jeho atributy. Tento balíček také přidejte do metadat XMP.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## Krok 8: Aktualizace metadat XMP v obrazu

Aktualizujte metadata XMP do obrazu pomocí `setXmpData` metoda.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## Krok 9: Uložení obrázku

Nyní můžete uložit obraz s vloženými metadaty XMP na disk nebo do paměťového streamu.

```java
    image.save(ms);
```

## Krok 10: Načtení obrazu a načtení metadat XMP

Chcete-li načíst metadata XMP z obrazu, načtěte obraz z paměťového proudu nebo disku a zpřístupněte data XMP.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Použít data balíčku ...
        }
    }
}
```

Gratulujeme! Úspěšně jste se naučili, jak zpracovávat XMP data v obrázcích pomocí Aspose.Imaging pro Javu. To vám umožní ukládat a načítat cenná metadata v obrazových souborech.

## Závěr

V tomto tutoriálu jsme prozkoumali, jak pracovat s metadaty XMP v obrázcích pomocí Aspose.Imaging pro Javu. Podle podrobného návodu můžete snadno vkládat a načítat metadata v obrazových souborech, čímž vylepšíte jejich informační obsah a použitelnost.

## Často kladené otázky

### Q1: Co jsou metadata XMP?

A1: XMP (Extensible Metadata Platform) je standard pro vkládání metadat do různých typů souborů, včetně obrázků. Umožňuje ukládat informace, jako je autor, název, popis a další, přímo do souboru.

### Otázka 2: Proč jsou metadata XMP důležitá?

A2: Metadata XMP jsou nezbytná pro organizaci a kategorizaci digitálních aktiv. Pomáhají s přiřazováním vlastnictví, popisem obsahu a přidáváním kontextu k souborům, jako jsou obrázky, čímž je činí přístupnějšími a smysluplnějšími.

### Q3: Mohu upravovat metadata XMP po jejich vložení do obrázku?

A3: Ano, metadata XMP můžete upravovat po vložení do obrázku. Aspose.Imaging pro Javu poskytuje nástroje pro úpravu a aktualizaci atributů metadat podle potřeby.

### Q4: Je Aspose.Imaging pro Javu bezplatný nástroj?

A4: Aspose.Imaging pro Javu nabízí bezplatnou zkušební verzi, ale pro plnou funkčnost a rozšířené používání je vyžadována placená licence. Možnosti si můžete prohlédnout na [Web Aspose.Imaging pro Javu](https://purchase.aspose.com/buy).

### Q5: Kde mohu získat pomoc a podporu pro Aspose.Imaging pro Javu?

A5: Pokud narazíte na jakékoli problémy nebo máte otázky týkající se Aspose.Imaging pro Javu, můžete navštívit [Fóra Aspose.Imaging](https://forum.aspose.com/) pro podporu a vedení komunity.



## Kompletní zdrojový kód
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Určete velikost obrázku definováním obdélníku
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// vytvořte zcela nový obrázek pouze pro vzorové účely
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// vytvořit instanci XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// vytvořit instanci Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// vytvořit instanci metatřídy XMP pro nastavení různých atributů
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// vytvořit instanci XmpPacketWrapper, která obsahuje všechna metadata
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// vytvořit instanci balíčku Photoshop a nastavit atributy Photoshopu
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// přidat balíček Photoshopu do metadat XMP
	xmpData.addPackage(photoshopPackage);
	// vytvořit instanci balíčku DublinCore a nastavit atributy dublinCore
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// přidat balíček dublinCore do metadat XMP
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// aktualizovat metadata XMP do obrazu
	image.setXmpData(xmpData);
	// Uložení obrazu na disk nebo do paměťového proudu
	image.save(ms);
	// Načtěte obraz z paměťového proudu nebo z disku pro čtení/získání metadat.
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Získání metadat XMP
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Použít data balíčku ...
		}
	}
}
        
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}