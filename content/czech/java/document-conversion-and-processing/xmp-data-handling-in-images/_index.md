---
title: Zpracování dat XMP v obrázcích pomocí Aspose.Imaging pro Java
linktitle: Zpracování dat XMP v obrázcích
second_title: Aspose.Imaging Java Image Processing API
description: Naučte se zacházet s metadaty XMP v obrázcích pomocí Aspose.Imaging for Java. Vkládáním a načítáním metadat můžete vylepšit své soubory obrázků.
type: docs
weight: 16
url: /cs/java/document-conversion-and-processing/xmp-data-handling-in-images/
---
Aspose.Imaging for Java je všestranná a výkonná knihovna pro práci s obrázky v různých formátech. Tento tutoriál vás provede procesem zpracování dat XMP (Extensible Metadata Platform) v obrázcích pomocí Aspose.Imaging for Java. XMP je standard pro vkládání metadat do obrazových souborů, což vám umožňuje ukládat cenné informace, jako je autor, popis a další.

## Předpoklady

Než začnete, ujistěte se, že máte splněny následující předpoklady:

- Vývojové prostředí Java nastavené na vašem počítači.
-  Nainstalovaná knihovna Aspose.Imaging for Java. Můžete si jej stáhnout z[Aspose.Imaging pro webové stránky Java](https://releases.aspose.com/imaging/java/).
- Základní znalost programování v Javě.

## Import balíčků

Začněte importováním potřebných balíčků do vašeho projektu Java. Na začátek kódu můžete přidat následující příkazy pro import:

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

Nyní rozeberme příklad do podrobného průvodce:

## Krok 1: Zadejte možnosti Velikost obrázku a Tiff

Nejprve definujte adresář, kde bude váš obrázek uložen, a vytvořte obdélník pro určení velikosti obrázku. V tomto příkladu používáme obrázek Tiff s určitými možnostmi.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## Krok 2: Vytvořte nový obrázek

Nyní vytvořte nový obrázek se zadanými možnostmi. Tento obrázek bude použit k uložení metadat XMP.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## Krok 3: Vytvořte XMP záhlaví a upoutávku

Vytvořte instance XMP-Header a XMP-Trailer pro vaše metadata XMP. Tato záhlaví a upoutávky pomáhají definovat strukturu metadat.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Krok 4: Vytvořte metainformace XMP

Nyní vytvořte instanci XMP meta pro nastavení různých atributů. Můžete přidat informace, jako je autor a popis.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Krok 5: Vytvořte XMP Packet Wrapper

Vytvořte instanci XmpPacketWrapper, která obsahuje záhlaví XMP, upoutávku a metainformace.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Krok 6: Přidejte balíček Photoshopu

Chcete-li uložit informace specifické pro Photoshop, vytvořte balíček Photoshopu a nastavte jeho atributy, jako je město, země a barevný režim. Poté přidejte tento balíček do metadat XMP.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## Krok 7: Přidejte balíček Dublin Core

Pro obecnější informace, jako je autor, název a další hodnoty, vytvořte balíček DublinCore a nastavte jeho atributy. Přidejte tento balíček také do metadat XMP.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## Krok 8: Aktualizujte metadata XMP v obrázku

 Aktualizujte metadata XMP do obrázku pomocí`setXmpData` metoda.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## Krok 9: Uložte obrázek

Nyní můžete uložit obrázek s vloženými metadaty XMP na disk nebo do paměťového toku.

```java
    image.save(ms);
```

## Krok 10: Načtěte obrázek a načtěte metadata XMP

Chcete-li získat metadata XMP z obrázku, načtěte obrázek z paměťového toku nebo disku a získejte přístup k datům XMP.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Použít data balíčku...
        }
    }
}
```

Gratulujeme! Úspěšně jste se naučili, jak zacházet s daty XMP v obrázcích pomocí Aspose.Imaging for Java. To vám umožňuje ukládat a získávat cenná metadata v rámci vašich obrazových souborů.

## Závěr

V tomto tutoriálu jsme prozkoumali, jak pracovat s metadaty XMP v obrázcích pomocí Aspose.Imaging for Java. Podle tohoto podrobného průvodce můžete snadno vkládat a načítat metadata do svých obrazových souborů, čímž se zvýší jejich informace a použitelnost.

## FAQ

### Q1: Co jsou metadata XMP?

A1: XMP (Extensible Metadata Platform) je standard pro vkládání metadat do různých typů souborů, včetně obrázků. Umožňuje vám ukládat informace, jako je autor, název, popis a další, v rámci samotného souboru.

### Q2: Proč jsou metadata XMP důležitá?

Odpověď 2: Metadata XMP jsou nezbytná pro organizaci a kategorizaci digitálních aktiv. Pomáhá při přiřazování vlastnictví, popisu obsahu a přidávání kontextu k souborům, jako jsou obrázky, díky čemuž jsou přístupnější a smysluplnější.

### Otázka 3: Mohu upravit metadata XMP po jejich vložení do obrázku?

Odpověď 3: Ano, metadata XMP můžete upravit po jejich vložení do obrázku. Aspose.Imaging for Java poskytuje nástroje pro úpravu a aktualizaci atributů metadat podle potřeby.

### Q4: Je Aspose.Imaging for Java bezplatný nástroj?

 A4: Aspose.Imaging for Java nabízí bezplatnou zkušební verzi, ale pro plnou funkčnost a rozšířené použití je vyžadována placená licence. Možnosti můžete prozkoumat na[Aspose.Imaging pro webové stránky Java](https://purchase.aspose.com/buy).

### Q5: Kde mohu získat pomoc a podporu pro Aspose.Imaging pro Java?

 A5: Pokud narazíte na nějaké problémy nebo máte dotazy týkající se Aspose.Imaging pro Java, můžete navštívit stránku[Aspose.Imaging fóra](https://forum.aspose.com/) za podporu a vedení komunity.



## Kompletní zdrojový kód
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Určete velikost obrázku definováním obdélníku
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// vytvořit zbrusu nový obrázek pouze pro účely vzorku
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// vytvořit instanci XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// vytvořit instanci Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// vytvořte instanci meta třídy XMP pro nastavení různých atributů
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	//vytvořte instanci XmpPacketWrapper, která obsahuje všechna metadata
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// vytvořte instanci balíku Photoshop a nastavte atributy Photoshopu
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// přidat balíček photoshop do metadat XMP
	xmpData.addPackage(photoshopPackage);
	// vytvořte instanci balíčku DublinCore a nastavte atributy dublinCore
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// přidat balíček dublinCore do metadat XMP
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// aktualizovat metadata XMP na obrázek
	image.setXmpData(xmpData);
	// Uložit obrázek na disk nebo do paměti
	image.save(ms);
	// Chcete-li číst/získat metadata, načtěte obrázek z paměti nebo z disku
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Získání metadat XMP
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Použít data balíčku...
		}
	}
}
        
```