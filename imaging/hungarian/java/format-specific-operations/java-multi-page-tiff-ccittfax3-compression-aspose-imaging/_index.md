---
date: '2026-09-28'
description: Ismerje meg, hogyan használhatja a ccittfax3 compression java-t a többoldalas
  TIFF fájlok létrehozásához az Aspose.Imaging segítségével. Hatékonyan szkenneljen,
  archiváljon és csökkentse a fájlméretet a dokumentumfolyamatok során.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Fedezze fel lépésről‑lépésre, hogyan használja a ccittfax3 compression
  java-t az Aspose.Imaging‑kel a hatékony többoldalas TIFF fájlok létrehozásához szkenneléshez
  és archiváláshoz.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: Hogyan készítsünk többoldalas TIFF-et ccittfax3 compression java segítségével
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
title: Hogyan készítsünk többoldalas TIFF-et ccittfax3 compression java segítségével
url: /hu/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# A többoldalas TIFF létrehozásának elsajátítása ccittfax3 tömörítéssel Java-ban az Aspose.Imaging használatával

## Bevezetés

Ha nagy mennyiségű beolvasott dokumentumot kell archiválnia, miközben alacsony fájlméretet tart fenn, a **ccittfax3 compression java** a megfelelő megoldás. Ez az útmutató megmutatja, hogyan generálhat többoldalas TIFF fájlokat CCITTFAX3 tömörítéssel Java-ban az Aspose.Imaging használatával. Megtanulja, miért működik ez a tömörítés olyan jól a monokróm beolvasásoknál, hogyan konfigurálja a könyvtárat, és hogyan adja hozzá az egyes oldalakat keretként.

**Amit megtanul**
- Hogyan adja hozzá az Aspose.Imaging-et egy Java projekthez.
- Hogyan konfigurálja a `TiffOptions`-t a CCITTFAX3 tömörítéshez.
- Hogyan hozza létre a `TiffImage`-et, méretezze át a forrásképeket, és adja hozzá őket keretként.
- Hogyan mentse el hatékonyan a végleges többoldalas TIFF-et.

Lépjünk végig a teljes megvalósításon.

## Gyors válaszok
- **Mi a CCITTFAX3 tömörítés fő előnye?** Akár 80 % fájlméret-csökkenés fekete‑fehér beolvasásoknál.  
- **Melyik könyvtár biztosít beépített támogatást?** Aspose.Imaging for Java, 25.5+ verzió.  
- **Szükségem van licencre a fejlesztéshez?** Az ingyenes próbaverzió licenc minden funkciót támogat; a termeléshez fizetett licenc szükséges.  
- **Feldolgozhatok több száz oldalt?** Igen—az Aspose.Imaging adatfolyamként kezeli az oldalakat, így a memóriahasználat alacsony marad.  
- **A kód kompatibilis a Java 11‑el és újabb verziókkal?** Természetesen; az API a Java 8+ verziókat célozza.

## Mi az a ccittfax3 compression java?
`CCITTFAX3` egy veszteségmentes, monokróm tömörítési algoritmus, amely fax és beolvasott dokumentum képekhez készült. Minden pixelt egyetlen bitként kódol, magas minőségű kimenetet biztosítva, miközben drámaian csökkenti a fájlméretet—gyakran 70‑80 %-kal az eredeti, tömörítetlen TIFF-hez képest. Ez ideálissá teszi a fekete‑fehér dokumentumok archiválásához, ahol a hűség megőrzése fontos.

## Miért használjuk az Aspose.Imaging-et ehhez a feladathoz?
Aspose.Imaging több mint **100** bemeneti és kimeneti formátumot támogat, beleértve a PDF, PNG, JPEG és TIFF formátumokat. Streaming architektúrája képes **több száz oldalas** TIFF fájlok kezelésére anélkül, hogy az egész dokumentumot a memóriába töltené, így ideális nagy léptékű archiválási projektekhez.

## Előkövetelmények

- **Java Development Kit (JDK)** 8 vagy újabb telepítve.
- **IDE** mint IntelliJ IDEA vagy Eclipse.
- **Maven** vagy **Gradle** a függőségkezeléshez.
- Alap Java ismeretek (osztályok, objektumok, gyűjtemények).

## Az Aspose.Imaging beállítása Java-hoz

Adja hozzá a könyvtárat a build fájlhoz.

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

### Közvetlen letöltés

A legújabb JAR fájlt letöltheti a [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) oldalról.

### Licenc beszerzése

Egy ingyenes próbaverzió licenc elérhető a [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/) oldalról. Termeléshez vásároljon állandó licencet vagy kérjen ideiglenes licencet a [Aspose Purchase](https://purchase.aspose.com/temporary-license/) oldalon.

A részletes API használathoz tekintse meg az Aspose.Imaging for Java [documentation](https://reference.aspose.com/imaging/java/) dokumentációt.

### Alap inicializálás

A függőség hozzáadása után inicializálja a könyvtárat az alább látható módon.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## Hogyan konfiguráljuk a ccittfax3 compression java-t egy többoldalas TIFF-hez?

`TiffOptions` egy osztály, amely meghatározza a TIFF fájl kimeneti formátumát és tömörítési beállításait. Töltse be a `TiffOptions` objektumot a `CCITTGroup3FaxCompression` enum-mal, majd állítsa be a kimeneti fájl forrását. Ez a kéts lépéses konfiguráció előkészíti az íróprogramot a monokróm tömörítéshez, és biztosítja, hogy a később hozzáadott minden oldal a CCITTFAX3 algoritmussal legyen kódolva, ami jelentős méretcsökkenést eredményez a képminőség megőrzése mellett.

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

## Hogyan hozzunk létre egy TiffImage példányt Java-ban?

`TiffImage` egy többoldalas TIFF dokumentumot reprezentál a memóriában, és módszereket biztosít a keretek manipulálásához. Először határozza meg a szélességet és magasságot, amelyet az összes oldal megoszt. Ezután hozza létre a `TiffImage`-et a korábban létrehozott `TiffOptions` használatával. A `TiffImage` objektum egy tárolóként működik az egyes keretek számára, lehetővé téve oldalak hozzáadását, eltávolítását vagy átrendezését a végleges fájl mentése előtt.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## Hogyan töltsük be és méretezzük át a forrásképeket egy mappából?

Szűrje a célkönyvtárat JPEG fájlokra, olvassa be minden képet, és méretezze át, hogy illeszkedjen a TIFF vászonhoz. A keretek hozzáadása előtt végzett átméretezés csökkenti a memóriahasználatot és felgyorsítja a mentési műveletet. Az egyes forrásképek a szükséges méretre és pixelformátumra konvertálásával biztosítható a konzisztens oldalelrendezés, és elkerülhetők a futásidejű hibák, amikor a keretek a TIFF dokumentumhoz kerülnek.

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

## Hogyan adjuk hozzá minden képet keretként a többoldalas TIFF-hez?

`TiffFrame` egy objektum, amely egyetlen oldalképet és a hozzá tartozó metaadatokat tárolja egy TIFF-ben. Iteráljon a átméretezett képeken, hozzon létre egy új `TiffFrame`-et, és fűzze hozzá a `TiffImage`-hez. Minden keret külön oldalként jelenik meg a végső dokumentumban, és a könyvtár automatikusan kezeli a szükséges metaadat-frissítéseket, mint például az oldalszám és az eltolások, biztosítva a megfelelő többoldalas TIFF struktúrát.

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

## Hogyan mentse el a végleges többoldalas TIFF fájlt?

Hívja meg a `save` metódust a `TiffImage` példányon, megadva a kívánt kimeneti útvonalat. A könyvtár automatikusan minden keretet CCITTFAX3 tömörítéssel ír ki, hatékonyan adatfolyamként menti a lemezre, és bezárja az esetleges alatta lévő erőforrásokat. A mentési művelet befejezése után a kapott fájl tartalmazza az összes oldalt a megadott tömörítéssel, készen áll a terjesztésre vagy archiválásra.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## Gyakorlati alkalmazások

- **Dokumentum archiválás:** Beolvasott szerződések, számlák vagy jogi feljegyzések tárolása minimális tárolási költséggel.  
- **Orvosi képalkotás:** Radiológiai felvételek tömörítése a diagnosztikai részletek megőrzése mellett.  
- **Nyomtatási termelés:** Többoldalas nyomtatási feladatok generálása, amelyeket a nyomtatók közvetlenül felhasználhatnak.

## Teljesítmény szempontok

- Használjon `ResizeOptions`-t, amely megőrzi az oldalarányt a torzulás elkerülése érdekében.  
- Zárja be minden `Image` objektumot a keret hozzáadása után, hogy felszabadítsa a natív memóriát.  
- Nagyon nagy kötegek esetén dolgozza fel a fájlokat párhuzamos adatfolyamokban, és írja a TIFF szegmenseket aszinkron módon.

## Gyakori buktatók és hibaelhárítás

- **Helytelen pixel formátum:** A CCITTFAX3 csak 1‑bit (fekete‑fehér) képekkel működik. Színes képeket konvertáljon szürkeárnyalatosra a méretezés előtt.  
- **Memória szivárgások:** Mindig hívja meg a `dispose()`-t az ideiglenes `Image` objektumokon; ellenkező esetben a natív pufferek továbbra is lefoglalva maradnak.  
- **A fájlméret nem csökken:** Győződjön meg arról, hogy a `TiffOptions` tömörítési tulajdonsága be van állítva; különben az alapértelmezett (nincs tömörítés) kerül alkalmazásra.

## Gyakran ismételt kérdések

**K: Használhatom ezt a megközelítést színes képekkel?**  
V: A CCITTFAX3 csak monokróm adatokra korlátozódik; színes esetben használjon JPEG vagy LZW tömörítést.

**K: Támogatja az Aspose.Imaging a streaminget hatalmas TIFF-ekhez?**  
V: Igen— a könyvtár minden keretet közvetlenül az output adatfolyamra ír, így a memóriahasználat alacsony marad még több ezer oldal esetén is.

**K: Hogyan alkalmazhatok programozottan ideiglenes licencet?**  
V: Töltse be a `.lic` fájlt a `License license = new License(); license.setLicense("Aspose.Total.Java.lic");` kóddal.

**K: Van mód a TIFF előnézetére mentés előtt?**  
V: Minden `TiffFrame`-et renderelhet egy `BufferedImage`-re, és megjelenítheti egy Swing komponensben.

**K: Mely Java verziók támogatottak hivatalosan?**  
V: Az Aspose.Imaging a Java 8-tól a Java 21-ig, beleértve az LTS kiadásokat, támogatja.

## Összegzés

Most már rendelkezik egy teljes, termelésre kész munkafolyamattal a többoldalas TIFF fájlok létrehozásához **ccittfax3 compression java** használatával az Aspose.Imaging segítségével. A fenti lépések követésével hatékonyan archiválhat hatalmas dokumentumgyűjteményeket, miközben alacsony tárolási költségeket és magas képminőséget tart fenn. Fedezze fel az Aspose.Imaging további funkcióit—például OCR, metaadat-kezelés és formátumkonverzió—hogy tovább fejlessze a dokumentumfeldolgozó csővezetékét.

---

**Utolsó frissítés:** 2026-09-28  
**Tesztelt verzió:** Aspose.Imaging 25.5 for Java  
**Szerző:** Aspose

## Kapcsolódó útmutatók

- [Hogyan hozzunk létre többoldalas TIFF-et az Aspose.Imaging for Java segítségével – Teljes útmutató](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Hogyan csökkentsük a képfájl méretét LZW tömörítéssel Java-ban](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Többoldalas TIFF keretek szétválasztása az Aspose.Imaging for Java segítségével](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}