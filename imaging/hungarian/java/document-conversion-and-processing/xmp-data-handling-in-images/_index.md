---
title: XMP adatkezelés képekben az Aspose.Imaging for Java segítségével
linktitle: XMP adatkezelés képekben
second_title: Aspose.Imaging Java Image Processing API
description: Ismerje meg, hogyan kezelheti az XMP metaadatokat a képekben az Aspose.Imaging for Java segítségével. Metaadatok beágyazása és lekérése a képfájlok javításához.
weight: 16
url: /hu/java/document-conversion-and-processing/xmp-data-handling-in-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# XMP adatkezelés képekben az Aspose.Imaging for Java segítségével

Az Aspose.Imaging for Java egy sokoldalú és hatékony könyvtár a különféle formátumú képekkel való munkavégzéshez. Ez az oktatóanyag végigvezeti Önt a képekben lévő XMP (Extensible Metadata Platform) adatok kezelésének folyamatán az Aspose.Imaging for Java használatával. Az XMP a metaadatok képfájlokba való beágyazásának szabványa, amely lehetővé teszi olyan értékes információk tárolását, mint a szerző, leírás stb.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy a következő előfeltételeket teljesítette:

- A számítógépen beállított Java fejlesztői környezet.
-  Aspose.Imaging for Java könyvtár telepítve. Letöltheti a[Aspose.Imaging for Java webhely](https://releases.aspose.com/imaging/java/).
- Alapvető ismeretek a Java programozásról.

## Csomagok importálása

Kezdje azzal, hogy importálja a szükséges csomagokat a Java projektbe. A következő importálási utasításokat adhatja hozzá a kód elejéhez:

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

Most bontsuk le a példát egy lépésről lépésre útmutatóra:

## 1. lépés: Adja meg a képméretet és a tiff-beállításokat

Először határozza meg a könyvtárat, ahol a kép tárolni fogja, és hozzon létre egy téglalapot a kép méretének megadásához. Ebben a példában egy Tiff képet használunk bizonyos beállításokkal.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## 2. lépés: Hozzon létre egy új képet

Most hozzon létre egy új képet a megadott beállításokkal. Ez a kép az XMP metaadatok tárolására szolgál.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## 3. lépés: Hozzon létre XMP fejlécet és előzetest

Hozzon létre XMP-Header és XMP-Trailer példányokat az XMP metaadataihoz. Ezek a fejlécek és előzetesek segítenek meghatározni a metaadat-struktúrát.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## 4. lépés: Hozzon létre XMP metainformációt

Most hozzon létre egy XMP meta példányt a különböző attribútumok beállításához. Hozzáadhat információkat, például a szerzőt és a leírást.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## 5. lépés: Hozzon létre XMP Packet Wrappert

Hozzon létre egy XmpPacketWrapper példányt, amely tartalmazza az XMP fejlécet, előzetesét és metainformációit.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## 6. lépés: Photoshop-csomag hozzáadása

Photoshop-specifikus információk tárolásához hozzon létre egy Photoshop-csomagot, és állítsa be annak attribútumait, például a várost, az országot és a színmódot. Ezután adja hozzá ezt a csomagot az XMP metaadatokhoz.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## 7. lépés: Adja hozzá a Dublin Core csomagot

Általánosabb információkért, például szerző, cím és további értékekért hozzon létre egy DublinCore-csomagot, és állítsa be annak attribútumait. Adja hozzá ezt a csomagot az XMP metaadatokhoz is.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## 8. lépés: Frissítse az XMP metaadatokat a képen

 Frissítse az XMP metaadatokat a képbe a`setXmpData` módszer.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## 9. lépés: Mentse el a képet

Most már mentheti a képet a beágyazott XMP-metaadatokkal a lemezre vagy egy memóriafolyamba.

```java
    image.save(ms);
```

## 10. lépés: Töltse be a képet és kérje le az XMP metaadatokat

Az XMP-metaadatok lekéréséhez a képről töltse be a képet a memóriafolyamról vagy a lemezről, és nyissa meg az XMP-adatokat.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Csomagadatok használata...
        }
    }
}
```

Gratulálunk! Sikeresen megtanulta, hogyan kell XMP-adatokat kezelni képekben az Aspose.Imaging for Java segítségével. Ez lehetővé teszi értékes metaadatok tárolását és visszakeresését a képfájlokban.

## Következtetés

Ebben az oktatóanyagban megvizsgáltuk, hogyan dolgozhatunk XMP-metaadatokkal a képekben az Aspose.Imaging for Java segítségével. A lépésenkénti útmutató követésével könnyedén beágyazhat és visszakereshet metaadatokat képfájljaiba, javítva azok információit és használhatóságát.

## GYIK

### 1. kérdés: Mi az XMP metaadat?

1. válasz: Az XMP (Extensible Metadata Platform) egy szabvány a metaadatok különféle típusú fájlokba, köztük képekbe ágyazására. Lehetővé teszi, hogy magában a fájlban tároljon információkat, például szerzőt, címet, leírást és egyebeket.

### 2. kérdés: Miért fontosak az XMP metaadatok?

2. válasz: Az XMP metaadatok elengedhetetlenek a digitális eszközök rendszerezéséhez és kategorizálásához. Segít a tulajdonjog hozzárendelésében, a tartalom leírásában, valamint a fájlok, például a képek kontextusának meghatározásában, hozzáférhetőbbé és értelmesebbé téve azokat.

### 3. kérdés: Szerkeszthetem az XMP metaadatokat, miután beágyaztam egy képbe?

3. válasz: Igen, szerkesztheti az XMP metaadatokat, miután beágyazta őket egy képbe. Az Aspose.Imaging for Java eszközöket biztosít a metaadat-attribútumok szükség szerinti módosításához és frissítéséhez.

### 4. kérdés: Az Aspose.Imaging for Java ingyenes eszköz?

 4. válasz: Az Aspose.Imaging for Java ingyenes próbaverziót kínál, de a teljes funkcionalitás és a kiterjesztett használat érdekében fizetős licenc szükséges. A lehetőségeket a[Aspose.Imaging for Java webhely](https://purchase.aspose.com/buy).

### 5. kérdés: Hol kaphatok segítséget és támogatást az Aspose.Imaging for Java-hoz?

 5. válasz: Ha bármilyen problémába ütközik, vagy kérdései vannak az Aspose.Imaging for Java-val kapcsolatban, keresse fel a[Aspose.Képalkotó fórumok](https://forum.aspose.com/) közösségi támogatásért és útmutatásért.



## Teljes forráskód
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Adja meg a kép méretét egy téglalap megadásával
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// hozza létre a vadonatúj képet csak minta céljából
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// hozzon létre egy XMP-Header példányt
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// hozzon létre egy Xmp-TrailerPi példányt
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// hozzon létre egy XMP metaosztály példányt a különböző attribútumok beállításához
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	//hozzon létre egy XmpPacketWrapper példányt, amely tartalmazza az összes metaadatot
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// hozzon létre egy példányt a Photoshop csomagból, és állítsa be a Photoshop attribútumokat
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// Photoshop-csomag hozzáadása az XMP metaadatokhoz
	xmpData.addPackage(photoshopPackage);
	// hozzon létre egy DublinCore-csomag példányt, és állítsa be a dublinCore attribútumokat
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// dublinCore Package hozzáadása az XMP metaadatokhoz
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// frissítse az XMP metaadatokat képpé
	image.setXmpData(xmpData);
	// Mentse a képet a lemezre vagy a memóriafolyamba
	image.save(ms);
	// A metaadatok olvasásához/lekéréséhez töltse be a képet a memóriafolyamból vagy a lemezről
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Az XMP metaadatok lekérése
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Csomagadatok használata...
		}
	}
}
        
```
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
