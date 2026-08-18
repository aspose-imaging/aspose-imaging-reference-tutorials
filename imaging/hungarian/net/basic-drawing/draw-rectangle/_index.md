---
date: 2026-02-12
description: Tanulja meg, hogyan hozhat létre üres képet az Aspose segítségével, és
  hogyan rajzolhat téglalapot .NET-ben az Aspose.Imaging használatával – egy gyors
  útmutató a képmódosításhoz .NET alkalmazásaiban.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Üres kép létrehozása Aspose – Téglalapok rajzolása .NET-ben
url: /hu/net/basic-drawing/draw-rectangle/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Üres kép létrehozása Aspose – Téglalapok rajzolása .NET-ben

## Gyors válaszok
- **Mit jelent a „create blank image Aspose”?** Ez azt jelenti, hogy egy üres bitmapet generálunk az Aspose.Imaging API segítségével.  
- **Hogyan rajzoljunk téglalapot .net-ben az Aspose segítségével?** Használja a `Graphics.DrawRectangle` metódust a `Graphics` objektum inicializálása után.  
- **Melyik NuGet csomagra van szükség?** `Aspose.Imaging` (latest version).  
- **Menthetem a képet PNG, JPEG vagy BMP formátumban?** Igen – csak módosítsa a képbeállításokat (pl. `BmpOptions`, `JpegOptions`).  
- **Szükségem van licencre a fejlesztéshez?** Az ingyenes próba verzió elegendő értékeléshez; a termeléshez kereskedelmi licenc szükséges.

## Mi a „create blank image Aspose”?
A blank kép létrehozása azt jelenti, hogy egy pixelpuffer lefoglalása meghatározott szélességgel, magassággal és pixelformátummal. Az Aspose.Imaging kezeli az alacsony szintű részleteket, így egy rajzolásra kész vásznat kapunk anélkül, hogy a GDI+ vagy a System.Drawing használatával kellene foglalkozni.

## Miért használjuk az Aspose.Imaging-et téglalapok rajzolásához .NET-ben?
- **Cross‑platform** – működik Windows, Linux és macOS rendszereken.  
- **Nincs natív függőség** – tisztán kezelt kód, tökéletes szerverkörnyezetekhez.  
- **Gazdag rajzoló API** – támogatja a tollakat, ecseteket, anti‑aliasingot és számos alakzattípust.  
- **Magas teljesítmény** – optimalizált nagy képekhez és kötegelt feldolgozáshoz.

## Előfeltételek

1. **Aspose.Imaging for .NET** – töltse le a [letöltési oldalról](https://releases.aspose.com/imaging/net/).  
2. **Fejlesztői környezet** – Visual Studio, VS Code vagy bármely .NET‑kompatibilis IDE.  
3. **.NET runtime** – .NET 6+ vagy .NET Framework 4.7.2+.  

Most, hogy minden készen áll, merüljünk el a kódban.

## Hogyan hozzunk létre egy üres képet Aspose-ban .NET-ben?

### 1. lépés: A szükséges névterek importálása

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Ezek a névterek hozzáférést biztosítanak a fő képalkotó osztályokhoz, ecsettípusokhoz és a kép mentési beállításokhoz.

### 2. lépés: Üres kép létrehozása (a vászon)

```csharp
string dataDir = "Your Document Directory";  // Set the path to your document directory
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Your drawing code will go here
        image.Save();
    }
}
```

Ebben a blokkban:
* Meghatározzuk a kimeneti helyet (`dataDir`).  
* Beállítjuk a `BmpOptions`-t 32‑bit pixelformátum használatára.  
* Létrehozunk egy **üres kép** 100 × 100 pixel méretben.

### 3. lépés: Hogyan rajzoljunk téglalapot .net-ben az Aspose.Imaging segítségével

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` kitölti a vásznat egy háttérszínnel (ebben a példában sárga).  
* `DrawRectangle` két téglalapot rajzol – egy egyszerű piros tollal, egy másikat kék szilárd ecsettel – a vizuális kontraszt érdekében.

### 4. lépés: Kép mentése

```csharp
image.Save();
```

A `Save` hívás a bitmapet a fájlrendszerbe írja a korábban definiált beállítások használatával.

## Gyakori problémák és tippek

| Probléma | Ok | Megoldás |
|----------|----|----------|
| **Az üres kép fekete** | A háttér nincs törölve | Hívja a `graphic.Clear(Color.YourColor)` metódust a rajzolás előtt. |
| **Fájl nem található kivétel** | `dataDir` egy nem létező mappára mutat | Győződjön meg arról, hogy a könyvtár létezik, vagy használja a `Path.Combine`-t az `Environment.CurrentDirectory`-val. |
| **Helytelen színek** | `System.Drawing.Color` használata `Aspose.Imaging.Color` helyett | Mindig importálja a `Aspose.Imaging.Color`-t. |
| **Teljesítménycsökkenés nagy képeknél** | Alapértelmezett `BmpOptions` használata magas bitmélységgel | Váltson `JpegOptions` vagy `PngOptions`-ra a tömörítéshez. |

## Gyakran Ismételt Kérdések (Bővített)

**Q: Rajzolhatok más alakzatokat is a téglalapok mellett?**  
A: Természetesen. Az Aspose.Imaging olyan metódusokat kínál, mint a `DrawEllipse`, `DrawLine` és `DrawPolygon`.

**Q: Ingyenes a könyvtár kereskedelmi felhasználásra?**  
A: Nem, az Aspose.Imaging egy kereskedelmi termék, de ingyenes próba verzióval értékelhető, amely [itt](https://releases.aspose.com/) érhető el.

**Q: Működik ez Windows és webalkalmazások esetén egyaránt?**  
A: Igen, ugyanaz a kód fut ASP.NET, Blazor és konzolos alkalmazásokban.

**Q: Hogyan változtassam meg a kimeneti formátumot PNG-re?**  
A: Cserélje le a `BmpOptions`-t `PngOptions`-ra, és ennek megfelelően módosítsa a fájl kiterjesztését.

**Q: Hol találok részletesebb dokumentációt?**  
A: A teljes API referenciához férjen hozzá [itt](https://reference.aspose.com/imaging/net/), és csatlakozzon a közösséghez a [Aspose.Imaging fórumon](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Legutóbb frissítve:** 2026-02-12  
**Tesztelve ezzel:** Aspose.Imaging 24.12 for .NET  
**Szerző:** Aspose