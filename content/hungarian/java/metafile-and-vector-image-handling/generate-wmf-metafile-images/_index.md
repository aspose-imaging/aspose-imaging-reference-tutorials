---
title: WMF képek létrehozása az Aspose.Imaging for Java segítségével
linktitle: WMF metafile képeket generál
second_title: Aspose.Imaging Java Image Processing API
description: Ismerje meg, hogyan hozhat létre WMF metafájl képeket Java nyelven az Aspose.Imaging segítségével. Kövesse ezt a lépésről lépésre szóló útmutatót a hatékony képgenerálási lehetőségekhez.
type: docs
weight: 10
url: /hu/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/
---
WMF (Windows Metafile) képeket szeretne létrehozni Java alkalmazásaival? Az Aspose.Imaging for Java egy hatékony eszköz, amellyel könnyedén hozhat létre WMF-képeket. Ebben a lépésenkénti útmutatóban végigvezetjük az Aspose.Imaging for Java használatán WMF metafájlképek létrehozásához. 

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy a következő előfeltételeket teljesítette:

- A számítógépen beállított Java fejlesztői környezet.
-  Aspose.Imaging for Java könyvtár telepítve. Letöltheti a[weboldal](https://releases.aspose.com/imaging/java/).
- Java programozási alapismeretek.

## Csomagok importálása

Először is importálja a Java-alkalmazáshoz szükséges csomagokat az Aspose.Imaging for Java használatához:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.color.*;
import com.aspose.imaging.coreexceptions.ImageLoadException;
import com.aspose.imaging.imageoptions.WmfOptions;
import com.aspose.imaging.internal.system.drawing.*;
import com.aspose.imaging.internal.system.drawing.imaging.*;
import com.aspose.imaging.pen.*;
import com.aspose.imaging.system.drawing.*;
```

## 1. lépés: Hozzon létre egy vásznat

 A WMF-kép létrehozásához létre kell hoznia egy vásznat, ahol formákat rajzolhat. A`WmfRecorderGraphics2D` osztály biztosítja Önnek ezt a vásznat. Így hozhat létre példányt belőle:

```java
// A dokumentumok könyvtárának elérési útja.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

A fenti kódban megadjuk a vászon méreteit (100x100) és a felbontást (96 DPI).

## 2. lépés: Állítsa be a háttérszínt

 Ezután határozza meg a vászon háttérszínét. Használhatja a`setBackgroundColor` a háttérszín beállításának módja:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

Ebben a példában a háttérszínt fehér füstre állítottuk.

## 3. lépés: A toll és az ecset meghatározása

Ha alakzatokat szeretne rajzolni a vászonra, meg kell határoznia egy tollat és egy ecsetet. A tollal körvonalakat rajzolunk, az ecsettel formákat töltünk ki. Így hozhat létre tollat és tömör ecsetet:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

Ebben a kódban egy kék tollat és egy sárga-zöld tömör ecsetet hozunk létre.

## 4. lépés: Töltse ki és rajzoljon alakzatokat

Most töltsünk ki és rajzoljunk néhány alapvető formát a vászonra. Kezdjük egy sokszöggel:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Itt kitöltünk és rajzolunk egy sokszöget a megadott tollal és ecsettel. Igény szerint módosíthatja a koordinátákat és az alakzatokat.

## 5. lépés: Használja a HatchBrush-t

 Ha textúrákat szeretne hozzáadni az alakzatokhoz, használhatja a`HatchBrush`. Például:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

Ebben a kódban fehér és ezüst színekkel keresztezett ecsetet hozunk létre.

## 6. lépés: Töltse ki és rajzolja meg az ellipszist

Töltsünk ki és rajzoljunk ellipszist a vászonra:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

Igény szerint módosíthatja az ellipszis helyzetét és méretét.

## 7. lépés: Rajzolja meg az ívet és a Cubic Bezier-t

Bonyolultabb formák rajzolása is lehetséges. Így rajzolhatunk egy ívet és egy köbös Bezier-görbét:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

A fenti kódban először egy ívet rajzolunk pontozott vonal stílussal, majd egy köbös Bezier-görbét rajzolunk egy piros tollal.

## 8. lépés: Képek hozzáadása

A WMF metafájlhoz képeket is hozzáadhat. Íme, hogyan kell csinálni:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

Ebben a lépésben betöltünk egy képet és a vászonra helyezzük a megadott koordinátákon (50, 50).

## 9. lépés: Rajzolj vonalakat és kört

Vonalak és tortaformák hozzáadásához kövesse az alábbi példákat:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Itt húzunk egy vonalat és kitöltünk/rajzolunk egy pite formát a megadott tollal és ecsettel.

## 10. lépés: Rajzoljon vonalláncot és szöveget

Szöveg és vonalláncok hozzáadása egyszerű:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

Szükség szerint testreszabhatja a betűtípust, a szöveget és a vonalláncpontokat.

## 11. lépés: Mentse el a WMF-képet

Miután létrehozta a WMF-képet, ideje elmenteni:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Ez a kód elmenti a WMF-képet a megadott könyvtárba.

Ez az! Sikeresen generált egy WMF metafájl képet az Aspose.Imaging for Java segítségével.

## Következtetés

Ebben az oktatóanyagban megvizsgáltuk, hogyan hozhatók létre WMF metafájlképek az Aspose.Imaging for Java használatával. Kitértünk a szükséges előfeltételekre, importáltunk csomagokat, lépésről lépésre adtunk utasításokat a különböző formák rajzolásához, textúrák hozzáadásához, képek beillesztéséhez és a végleges kép elmentéséhez. Az Aspose.Imaging for Java hatékony eszközkészletet kínál a képkezeléshez és -létrehozáshoz, így értékes erőforrássá válik Java-alkalmazásai számára.

## GYIK

### 1. kérdés: Mi az a WMF képformátum?

V1: A WMF a Windows Metafile rövidítése, amely egy vektorgrafikus formátum, amelyet képek, rajzok és egyéb grafikus adatok tárolására használnak. Általában Windows alkalmazásokban használják, és minőségromlás nélkül könnyen méretezhető.

### 2. kérdés: Honnan tölthetem le az Aspose.Imaging for Java programot?

 2. válasz: Letöltheti az Aspose.Imaging for Java webhelyet[weboldal](https://releases.aspose.com/imaging/java/).

### 3. kérdés: Szükségem van fejlett programozási ismeretekre az Aspose.Imaging for Java használatához?

3. válasz: Bár alapvető Java programozási ismeretekre van szükség, az Aspose.Imaging for Java felhasználóbarát API-t biztosít, amely leegyszerűsíti a képkezelési és -készítési feladatokat.

### 4. kérdés: Használhatom az Aspose.Imaging for Java programot kereskedelmi célokra?

 4. válasz: Igen, az Aspose.Imaging for Java kereskedelmi licenceket kínál vállalkozások és fejlesztők számára. Engedélyt vásárolhat innen[itt](https://purchase.aspose.com/buy).

### 5. kérdés: Hol kaphatok támogatást, vagy hol tehetek fel kérdéseket az Aspose.Imaging for Java-val kapcsolatban?

 5. válasz: Támogatást találhat és kapcsolatba léphet az Aspose közösséggel a webhelyen[Aspose.Képalkotó fórumok](https://forum.aspose.com/).