---
title: DICOM-tömörítés az Aspose.Imaging-ben .NET-hez
linktitle: DICOM-tömörítés az Aspose.Imaging-ben .NET-hez
second_title: Aspose.Imaging .NET Image Processing API
description: Ismerje meg, hogyan hajthat végre DICOM-tömörítést az Aspose.Imaging for .NET használatával. Kövesse ezt a lépésenkénti útmutatót, hogy hatékonyan tárolja és továbbítsa az orvosi képeket, kiváló diagnosztikai minőségben.
type: docs
weight: 17
url: /hu/net/dicom-image-processing/dicom-compression/
---
Az orvosi képalkotás világában a DICOM (Digital Imaging and Communications in Medicine) szabvány kiemelkedően fontos az orvosi képek tárolására és megosztására. Az Aspose.Imaging for .NET egy nagy teljesítményű .NET-könyvtár, amely átfogó támogatást nyújt a DICOM-képekkel való munkavégzéshez. Ez az oktatóanyag végigvezeti a DICOM-tömörítés folyamatán az Aspose.Imaging for .NET használatával. Lebontjuk az egyes lépéseket, és részletesen elmagyarázzuk a folyamatot.

## Előfeltételek

Mielőtt belemerülnénk a DICOM-tömörítésbe az Aspose.Imaging for .NET segítségével, meg kell győződnie arról, hogy a következő előfeltételeket teljesíti:

1. Vizuális Stúdió

Győződjön meg arról, hogy a Visual Studio telepítve van a rendszeren. Ha nem, akkor letöltheti a webhelyről.

2. Aspose.Imaging for .NET

Rendelkeznie kell az Aspose.Imaging for .NET könyvtárral. Ezt a könyvtárat az alábbi linkek segítségével szerezheti be:

- [Az Aspose.Imaging letöltése .NET-hez](https://releases.aspose.com/imaging/net/)
- [Vásároljon Aspose.Imaging for.NET-hez](https://purchase.aspose.com/buy)
- [Szerezzen ingyenes próbaverziót](https://releases.aspose.com/)
- [Ideiglenes jogosítvány](https://purchase.aspose.com/temporary-license/)

Ha megvannak ezek az előfeltételek, ugorjunk bele a DICOM-tömörítés Aspose.Imaging for .NET segítségével lépésenkénti útmutatójába.

## Névterek importálása

Mielőtt folytatnánk, importálnunk kell a szükséges névtereket, hogy elérjük a szükséges osztályokat és metódusokat. Nyissa meg a Visual Studio projektet, és a C# fájl tetején adja hozzá a következőket:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

Most készen állunk a DICOM tömörítési folyamat megkezdésére.

## 1. lépés: Töltse be az eredeti képet

 Kezdjük azzal, hogy betöltjük az eredeti képet, amelyet DICOM formátumba szeretnénk konvertálni. Ügyeljen arra, hogy cserélje ki`"Your Document Directory"` a képkönyvtár tényleges elérési útjával.

```csharp
string dataDir = "Your Document Directory";
string inputFile = Path.Combine(dataDir, "original.jpg");

using (var inputImage = Image.Load(inputFile))
{
    // Ide kerül a DICOM-tömörítéshez szükséges kód.
}
```

## 2. lépés: Végezze el a tömörítetlen DICOM-tömörítést

Ebben a lépésben tömörítetlen DICOM-tömörítést hajtunk végre. Íme a kód hozzá:

```csharp
string output1 = Path.Combine(dataDir, "original_Uncompressed.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.None }
};

inputImage.Save(output1, options);
```

## 3. lépés: Hajtsa végre a JPEG DICOM tömörítést

Most pedig folytassuk a DICOM-tömörítést JPEG formátum használatával:

```csharp
string output2 = Path.Combine(dataDir, "original_JPEG.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Jpeg }
};

inputImage.Save(output2, options);
```

## 4. lépés: Hajtsa végre a JPEG2000 DICOM tömörítést

Ebben a lépésben DICOM-tömörítést hajtunk végre a JPEG2000 formátum használatával. Íme, hogyan kell csinálni:

```csharp
string output3 = Path.Combine(dataDir, "original_JPEG2000.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression
    {
        Type = CompressionType.Jpeg2000,
        Jpeg2000 = new Jpeg2000Options
        {
            Codec = Jpeg2000Codec.Jp2,
            Irreversible = false
        }
    }
};

inputImage.Save(output3, options);
```

## 5. lépés: Hajtsa végre az RLE DICOM tömörítést

Végül végezzünk DICOM-tömörítést az RLE (Run-Length Encoding) formátum használatával:

```csharp
string output4 = Path.Combine(dataDir, "original_RLE.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Rle }
};

inputImage.Save(output4, options);
```

## Következtetés

 Ebben a lépésenkénti útmutatóban megtanultuk, hogyan végezzünk DICOM-tömörítést az Aspose.Imaging for .NET használatával. Ez a könyvtár hatékony eszközkészletet biztosít az orvosi képekkel való munkavégzéshez, és lehetőségeit tovább fedezheti fel a[dokumentáció](https://reference.aspose.com/imaging/net/).

## GYIK

### 1. kérdés: Mi az a DICOM-tömörítés?

1. válasz: A DICOM-tömörítés az orvosi képek méretének csökkentését jelenti, miközben megőrzi azok diagnosztikai minőségét. Elengedhetetlen az orvosi adatok hatékony tárolásához és továbbításához.

### 2. kérdés: Miért érdemes az Aspose.Imaging for .NET-et használni DICOM-tömörítéshez?

2. válasz: Az Aspose.Imaging for .NET robusztus szolgáltatáskészletet és felhasználóbarát API-t kínál a DICOM-képekkel való munkához, így kiváló választás az orvosi képalkotó alkalmazásokhoz.

### 3. kérdés: Alkalmazhatok-e más képfeldolgozási műveleteket a DICOM-tömörítéssel az Aspose.Imaging for .NET használatával?

3. válasz: Igen, az Aspose.Imaging for .NET a képfeldolgozási lehetőségek széles skáláját kínálja, amelyek kombinálhatók a DICOM-tömörítéssel, hogy megfeleljenek a speciális követelményeknek.

### 4. kérdés: Hol kaphatok támogatást, vagy hol tehetek fel kérdéseket az Aspose.Imaging for .NET-hez kapcsolódóan?

 A4: Meglátogathatja a[Aspose.Képalkotó fórumok](https://forum.aspose.com/) támogatást kapni, kérdéseket feltenni, és kapcsolatba lépni az Aspose.Imaging közösséggel.

### 5. kérdés: Elérhető az Aspose.Imaging .NET-hez készült próbaverziója tesztelésre?

 V5: Igen, beszerezheti a[ingyenes próba licenc](https://releases.aspose.com/) hogy vásárlás előtt tesztelje az Aspose.Imaging for .NET-et.