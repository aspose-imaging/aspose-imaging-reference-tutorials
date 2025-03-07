---
title: Raszterkép rajzolása SVG-n az Aspose.Imaging for .NET-ben
linktitle: Rajzoljon raszterképet SVG-n az Aspose.Imaging for .NET programban
second_title: Aspose.Imaging .NET Image Processing API
description: Ismerje meg, hogyan rajzolhat raszteres képeket SVG-ben az Aspose.Imaging for .NET használatával. Bővítse .NET-alkalmazásait dinamikus képekkel.
weight: 11
url: /hu/net/vector-image-processing/draw-raster-image-on-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Raszterkép rajzolása SVG-n az Aspose.Imaging for .NET-ben


.NET programozás világában az Aspose.Imaging megbízható és sokoldalú könyvtár a különféle képekkel kapcsolatos feladatok kezelésére. Az egyik lenyűgöző képesség, amelyet kínál, az a képesség, hogy raszterképet rajzolhat egy SVG vászonra. Ebben a lépésenkénti útmutatóban végigvezetjük a raszterkép SVG-re való rajzolásának folyamatán az Aspose.Imaging for .NET segítségével.

## Előfeltételek

Mielőtt belemerülnénk a részletekbe, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

-  Aspose.Imaging for .NET: Telepíteni kell a könyvtárat. Ha nem, akkor letöltheti a[Aspose.Imaging for .NET letöltési oldal](https://releases.aspose.com/imaging/net/).

-  Az Ön dokumentumkönyvtára: Cserélje ki`"Your Document Directory"` a munkakönyvtár tényleges elérési útjával.

Most bontsuk le a folyamatot könnyen követhető lépésekre:

## 1. lépés: Importálja a szükséges névtereket

Az Aspose.Imaging használatához importálnia kell a szükséges névtereket:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## 2. lépés: Töltse be a képeket

- Először töltse be az SVG vászonra rajzolni kívánt raszterképet.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Ezután töltse be az SVG vászonképet oda, ahová a raszterképet meg szeretné rajzolni.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## 3. lépés: Rajzolás az SVG-képre

Most elkezdhet rajzolni a meglévő SVG-képre. Ehhez létre kell hoznia egy példányt`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## 4. lépés: Rajzolja meg a raszterképet

- Határozza meg a határokat, ahol a raszterképet meg kívánja rajzolni, és adja meg a raszterkép forrásterületét.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## 5. lépés: Mentse el az eredményt

Miután felrajzolta a raszterképet az SVG vászonra, elmentheti a kapott képet:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Következtetés

Gratulálunk! Sikeresen rajzolt egy raszterképet egy SVG vászonra az Aspose.Imaging for .NET használatával. Ez hihetetlenül hasznos lehet gazdag és dinamikus képek létrehozásához a .NET-alkalmazásokon belül.

 További információkért és részletes dokumentációért látogassa meg a[Aspose.Imaging .NET dokumentációhoz](https://reference.aspose.com/imaging/net/).

## Gyakran Ismételt Kérdések

### Mi az Aspose.Imaging for .NET?
   Az Aspose.Imaging for .NET egy hatékony képfeldolgozó könyvtár, amely lehetővé teszi a fejlesztők számára, hogy .NET-alkalmazásokon belül különféle formátumú képeket hozzanak létre, kezeljenek és konvertáljanak.

### Használhatom az Aspose.Imaging for .NET-et kereskedelmi projektekben?
    Igen, az Aspose.Imaging for .NET használható kereskedelmi és nem kereskedelmi projektekben is. Az engedélyezés részleteit a[vásárlási oldal](https://purchase.aspose.com/buy).

### Van ingyenes próbaverzió?
    Igen, letöltheti az Aspose.Imaging ingyenes próbaverzióját .NET-hez innen[itt](https://releases.aspose.com/).

### Hol kaphatok támogatást vagy tehetek fel kérdéseket?
    Ha bármilyen kérdése van, vagy segítségre van szüksége, látogasson el a[Aspose.Imaging fórum](https://forum.aspose.com/).

### Hogyan szerezhetek ideiglenes licencet az Aspose.Imaging for .NET számára?
    Ideiglenes jogosítványt kaphat[itt](https://purchase.aspose.com/temporary-license/).



{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
