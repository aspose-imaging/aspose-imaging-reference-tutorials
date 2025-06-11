---
"description": "Naučte se, jak vytvářet obrazy metasouborů WMF v Javě pomocí Aspose.Imaging. Postupujte podle tohoto podrobného návodu a získejte výkonné funkce pro generování obrázků."
"linktitle": "Generování obrazů metasouborů WMF"
"second_title": "API pro zpracování obrazu v Javě Aspose.Imaging"
"title": "Vytváření obrázků WMF pomocí Aspose.Imaging pro Javu"
"url": "/cs/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/"
"weight": 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Vytváření obrázků WMF pomocí Aspose.Imaging pro Javu

Chcete vytvářet obrazy WMF (Windows Metafile) pomocí vašich Java aplikací? Aspose.Imaging for Java je výkonný nástroj, který vám umožňuje snadno generovat obrazy WMF. V tomto podrobném návodu vás provedeme procesem použití Aspose.Imaging for Java k vytváření obrazů metasouborů WMF. 

## Předpoklady

Než začnete, ujistěte se, že máte splněny následující předpoklady:

- Vývojové prostředí Java nastavené na vašem počítači.
- Je nainstalována knihovna Aspose.Imaging pro Javu. Můžete si ji stáhnout z [webové stránky](https://releases.aspose.com/imaging/java/).
- Základní znalost programování v Javě.

## Importovat balíčky

Nejprve importujte potřebné balíčky pro vaši Java aplikaci, aby mohla používat Aspose.Imaging pro Javu:

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

## Krok 1: Vytvořte plátno

Chcete-li začít vytvářet obrázek WMF, musíte si vytvořit plátno, na kterém můžete kreslit tvary. `WmfRecorderGraphics2D` třída vám poskytuje toto plátno. Zde je návod, jak vytvořit jeho instanci:

```java
// Cesta k adresáři s dokumenty.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

Ve výše uvedeném kódu zadáváme rozměry plátna (100x100) a rozlišení (96 DPI).

## Krok 2: Nastavení barvy pozadí

Dále definujte barvu pozadí pro plátno. Můžete použít `setBackgroundColor` metoda pro nastavení barvy pozadí:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

V tomto příkladu jsme nastavili barvu pozadí na bílý kouř.

## Krok 3: Definujte pero a štětec

Pro kreslení tvarů na plátně je potřeba definovat pero a štětec. Pero se používá pro kreslení obrysů a štětec pro vyplňování tvarů. Zde je návod, jak vytvořit pero a plný štětec:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

V tomto kódu vytvoříme modré pero a žlutozelený plný štětec.

## Krok 4: Vyplňte a nakreslete tvary

Nyní si na plátno vyplníme a nakreslíme několik základních tvarů. Začneme s polygonem:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Zde vyplníme a nakreslíme polygon pomocí zadaného pera a štětce. Souřadnice a tvary můžete upravit dle potřeby.

## Krok 5: Použití šrafovacího štětce

Chcete-li přidat textury k tvarům, můžete použít `HatchBrush`Například:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

V tomto kódu vytvoříme šrafovaný štětec s bílou a stříbrnou barvou.

## Krok 6: Vyplnění a nakreslení elipsy

Vyplňme a nakreslíme elipsu na plátno:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

Polohu a velikost elipsy můžete upravit dle potřeby.

## Krok 7: Nakreslete oblouk a kubickou Bézierovu rovnici

Kreslení složitějších tvarů je také možné. Zde je návod, jak nakreslit oblouk a kubickou Bézierovu křivku:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

Ve výše uvedeném kódu nejprve nakreslíme oblouk tečkovanou čarou a poté nakreslíme kubickou Bézierovu křivku plným červeným perem.

## Krok 8: Přidání obrázků

Do metasouboru WMF můžete také přidat obrázky. Postupujte takto:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

tomto kroku načteme obrázek a umístíme ho na plátno na zadané souřadnice (50, 50).

## Krok 9: Kreslení čar a koláčů

Chcete-li přidat čáry a tvary koláčů, můžete postupovat podle těchto příkladů:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Zde nakreslíme čáru a vyplníme/nakreslíme tvar koláče pomocí zadaného pera a štětce.

## Krok 10: Nakreslete křivku a text

Přidání textu a křivek je jednoduché:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

Písmo, text a body křivky můžete podle potřeby upravit.

## Krok 11: Uložení obrazu WMF

Jakmile si vytvoříte obrázek WMF, je čas ho uložit:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Tento kód uloží obraz WMF do zadaného adresáře.

To je vše! Úspěšně jste vygenerovali metasoubor WMF pomocí Aspose.Imaging pro Javu.

## Závěr

tomto tutoriálu jsme prozkoumali, jak vytvářet obrazy metasouborů WMF pomocí Aspose.Imaging pro Javu. Probrali jsme nezbytné předpoklady, importovali balíčky a poskytli podrobné pokyny pro kreslení různých tvarů, přidávání textur, vkládání obrázků a ukládání finálního obrázku. Aspose.Imaging pro Javu nabízí výkonnou sadu nástrojů pro manipulaci s obrázky a jejich tvorbu, což z něj činí cenný zdroj pro vaše Java aplikace.

## Často kladené otázky

### Otázka 1: Co je formát obrázku WMF?

A1: WMF je zkratka pro Windows Metafile, což je formát vektorové grafiky používaný pro ukládání obrázků, kreseb a dalších grafických dat. Běžně se používá v aplikacích systému Windows a lze jej snadno škálovat bez ztráty kvality.

### Q2: Kde si mohu stáhnout Aspose.Imaging pro Javu?

A2: Aspose.Imaging pro Javu si můžete stáhnout z [webové stránky](https://releases.aspose.com/imaging/java/).

### Q3: Potřebuji pokročilé programátorské dovednosti k používání Aspose.Imaging pro Javu?

A3: I když jsou vyžadovány základní znalosti programování v Javě, Aspose.Imaging pro Javu poskytuje uživatelsky přívětivé API, které zjednodušuje manipulaci s obrázky a jejich vytváření.

### Q4: Mohu používat Aspose.Imaging pro Javu pro komerční účely?

A4: Ano, Aspose.Imaging pro Javu nabízí komerční licence pro firmy a vývojáře. Licenci si můžete zakoupit od [zde](https://purchase.aspose.com/buy).

### Q5: Kde mohu získat podporu nebo se zeptat na otázky ohledně Aspose.Imaging pro Javu?

A5: Podporu a spolupráci s komunitou Aspose můžete najít na [Fóra Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}