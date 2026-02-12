---
date: 2026-02-12
description: Lär dig hur du skapar en tom bild med Aspose och hur du ritar en rektangel
  i .NET med Aspose.Imaging – en snabb guide för bildmanipulation i dina .NET‑applikationer.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Skapa en tom bild med Aspose – Rita rektanglar i .NET
url: /sv/net/basic-drawing/draw-rectangle/
weight: 14
---

 images..." translate.

Let's produce Swedish.

Will keep code block placeholders unchanged.

Tables: translate column headers and content.

Make sure to keep markdown syntax.

Proceed.

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Skapa tom bild Aspose – Rita rektanglar i .NET

Att skapa och manipulera bilder i .NET‑applikationer kan kännas skrämmande, men med Aspose.Imaging kan du **skapa en tom bild Aspose** med bara några rader kod och sedan rita former på den. I den här handledningen går vi igenom hela processen — från att skapa en tom duk till att rita rektanglar—så att du snabbt kan börja lägga till grafik i dina .NET‑projekt.

## Snabba svar
- **Vad betyder “create blank image Aspose”?** Det betyder att generera en tom bitmap med Aspose.Imaging‑API‑et.  
- **Hur ritar man en rektangel i .NET med Aspose?** Använd metoden `Graphics.DrawRectangle` efter att ha initierat ett `Graphics`‑objekt.  
- **Vilket NuGet‑paket krävs?** `Aspose.Imaging` (senaste versionen).  
- **Kan jag spara bilden som PNG, JPEG eller BMP?** Ja – ändra bara bildalternativen (t.ex. `BmpOptions`, `JpegOptions`).  
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för utvärdering; en kommersiell licens krävs för produktion.

## Vad är “create blank image Aspose”?
Att skapa en tom bild innebär att allokera en pixelförråd med definierad bredd, höjd och pixelformat. Aspose.Imaging hanterar de lågnivå‑detaljerna och ger dig en färdig att rita-duk utan att du behöver arbeta med GDI+ eller System.Drawing.

## Varför använda Aspose.Imaging för att rita rektanglar i .NET?
- **Cross‑platform** – fungerar på Windows, Linux och macOS.  
- **Inga inhemska beroenden** – ren managed kod, perfekt för servermiljöer.  
- **Rik rit‑API** – stödjer pennor, penslar, anti‑aliasing och många former.  
- **Hög prestanda** – optimerad för stora bilder och batch‑bearbetning.

## Förutsättningar

1. **Aspose.Imaging för .NET** – ladda ner det från [nedladdningssidan](https://releases.aspose.com/imaging/net/).  
2. **Utvecklingsmiljö** – Visual Studio, VS Code eller någon .NET‑kompatibel IDE.  
3. **.NET‑runtime** – .NET 6+ eller .NET Framework 4.7.2+.  

Nu när vi har allt på plats, låt oss dyka ner i koden.

## Hur skapar man en tom bild Aspose i .NET?

### Steg 1: Importera de nödvändiga namnutrymmena

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Dessa namnutrymmen ger dig åtkomst till de centrala bildklasserna, penseltyperna och bild‑sparalternativen.

### Steg 2: Skapa en tom bild (duken)

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

I detta block:

* Definierar vi utskriftsplatsen (`dataDir`).  
* Konfigurerar `BmpOptions` för att använda ett 32‑bits pixelformat.  
* Skapar en **tom bild** på 100 × 100 pixlar.  

### Steg 3: Hur ritar man en rektangel i .NET med Aspose.Imaging

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` fyller duken med en bakgrundsfärg (gul i det här exemplet).  
* `DrawRectangle` ritar två rektanglar—en med en enkel röd penna, en annan med en blå solid pensel—för visuell kontrast.

### Steg 4: Spara bilden

```csharp
image.Save();
```

Anropet `Save` skriver bitmapen till filsystemet med de alternativ som definierades tidigare.

## Vanliga problem & tips

| Problem | Orsak | Åtgärd |
|-------|--------|-----|
| **Tom bild visas svart** | Bakgrunden har inte rensats | Anropa `graphic.Clear(Color.YourColor)` innan du ritar. |
| **File not found‑undantag** | `dataDir` pekar på en icke‑existerande mapp | Säkerställ att katalogen finns eller använd `Path.Combine` med `Environment.CurrentDirectory`. |
| **Fel färger** | Använder `System.Drawing.Color` istället för `Aspose.Imaging.Color` | Importera alltid `Aspose.Imaging.Color`. |
| **Prestandafördröjning på stora bilder** | Använder standard‑`BmpOptions` med hög bit‑per‑pixel | Byt till `JpegOptions` eller `PngOptions` för komprimering. |

## Vanliga frågor (utökad)

**Q: Kan jag rita andra former än rektanglar?**  
A: Absolut. Aspose.Imaging erbjuder metoder som `DrawEllipse`, `DrawLine` och `DrawPolygon`.

**Q: Är biblioteket gratis för kommersiell användning?**  
A: Nej, Aspose.Imaging är en kommersiell produkt, men du kan utvärdera det med en gratis provversion som finns [här](https://releases.aspose.com/).

**Q: Fungerar detta både på Windows‑ och webbapplikationer?**  
A: Ja, samma kod körs i ASP.NET, Blazor och konsolprogram.

**Q: Hur ändrar jag utdataformatet till PNG?**  
A: Byt ut `BmpOptions` mot `PngOptions` och justera filändelsen därefter.

**Q: Var kan jag hitta mer detaljerad dokumentation?**  
A: Se hela API‑referensen [här](https://reference.aspose.com/imaging/net/) och gå med i communityn på [Aspose.Imaging‑forumet](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Senast uppdaterad:** 2026-02-12  
**Testad med:** Aspose.Imaging 24.12 för .NET  
**Författare:** Aspose