---
"description": "Tanuld meg, hogyan rajzolhatsz raszteres képeket SVG-re az Aspose.Imaging for .NET használatával. Fejleszd .NET alkalmazásaidat dinamikus képekkel."
"linktitle": "Raszteres kép rajzolása SVG-re Aspose.Imaging for .NET-ben"
"second_title": "Aspose.Imaging .NET képfeldolgozó API"
"title": "Hogyan rajzoljunk raszteres képet SVG-re az Aspose.Imaging for .NET programban?"
"url": "/hu/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan rajzoljunk raszteres képet SVG-re az Aspose.Imaging for .NET programban?


A .NET programozás világában az Aspose.Imaging megbízható és sokoldalú könyvtárként működik a képekkel kapcsolatos különféle feladatok kezelésében. Az egyik lenyűgöző képessége, hogy raszteres képet rajzolhat SVG-vászonra. Ebben a lépésről lépésre bemutatjuk, hogyan rajzolhat raszteres képet SVG-re az Aspose.Imaging for .NET használatával.

## Előfeltételek

Mielőtt belemerülnénk a részletekbe, győződjünk meg arról, hogy a következő előfeltételek teljesülnek:

- Aspose.Imaging .NET-hez: Telepítenie kell a könyvtárat. Ha nem, letöltheti innen: [Aspose.Imaging .NET letöltési oldal](https://releases.aspose.com/imaging/net/).

- Dokumentumkönyvtár: Csere `"Your Document Directory"` a munkakönyvtár tényleges elérési útjával.

Most pedig bontsuk le a folyamatot könnyen követhető lépésekre:

## 1. lépés: A szükséges névterek importálása

Importálnia kell a szükséges névtereket az Aspose.Imaging használatához:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## 2. lépés: Képek betöltése

- Először töltsd be a raszteres képet, amelyet az SVG vászonra szeretnél rajzolni.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Ezután töltse be az SVG vászonképet oda, ahová a raszteres képet szeretné rajzolni.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## 3. lépés: Rajzolás az SVG képre

Most elkezdhet rajzolni a meglévő SVG képre. Ehhez létre kell hoznia egy példányt a következőből: `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## 4. lépés: Rajzolja meg a raszteres képet

- Határozza meg a raszterkép rajzolási határait, és adja meg a raszterkép forrásterületét.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## 5. lépés: Mentse el az eredményt

Miután megrajzolta a raszteres képet az SVG vászonra, elmentheti a kapott képet:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Következtetés

Gratulálunk! Sikeresen rajzoltál egy raszteres képet egy SVG vászonra az Aspose.Imaging for .NET segítségével. Ez hihetetlenül hasznos lehet gazdag és dinamikus képek létrehozásához a .NET alkalmazásaidban.

További információkért és részletes dokumentációért látogassa meg a [Aspose.Imaging .NET dokumentációhoz](https://reference.aspose.com/imaging/net/).

## Gyakran Ismételt Kérdések

### Mi az Aspose.Imaging .NET-hez?
   Az Aspose.Imaging for .NET egy hatékony képfeldolgozó könyvtár, amely lehetővé teszi a fejlesztők számára, hogy különböző formátumú képeket hozzanak létre, manipuláljanak és konvertáljanak .NET alkalmazásokon belül.

### Használhatom az Aspose.Imaging for .NET-et kereskedelmi projektekben?
   Igen, az Aspose.Imaging for .NET használható mind kereskedelmi, mind nem kereskedelmi projektekben. A licencelési részletek a következő címen találhatók: [vásárlási oldal](https://purchase.aspose.com/buy).

### Van ingyenes próbaverzió?
   Igen, ingyenes próbaverziót kaphatsz az Aspose.Imaging for .NET-ből innen: [itt](https://releases.aspose.com/).

### Hol kérhetek támogatást vagy tehetek fel kérdéseket?
   Ha bármilyen kérdése van, vagy segítségre van szüksége, látogasson el a következő oldalra: [Aspose.Imaging fórum](https://forum.aspose.com/).

### Hogyan szerezhetek ideiglenes licencet az Aspose.Imaging for .NET-hez?
   Ideiglenes jogosítványt igényelhetsz [itt](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}