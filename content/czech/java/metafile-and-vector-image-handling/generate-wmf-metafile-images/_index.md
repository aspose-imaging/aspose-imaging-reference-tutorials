---
title: Vytváření WMF obrázků pomocí Aspose.Imaging pro Java
linktitle: Vytvářejte obrázky metasouborů WMF
second_title: Aspose.Imaging Java Image Processing API
description: Naučte se vytvářet obrázky metasouborů WMF v Javě pomocí Aspose.Imaging. Postupujte podle tohoto podrobného průvodce pro výkonné možnosti generování obrázků.
type: docs
weight: 10
url: /cs/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/
---
Chcete vytvořit obrázky WMF (Windows Metafile) pomocí svých aplikací Java? Aspose.Imaging for Java je výkonný nástroj, který vám umožňuje snadno vytvářet obrázky WMF. V tomto podrobném průvodci vás provedeme procesem použití Aspose.Imaging pro Java k vytvoření obrázků metasouborů WMF. 

## Předpoklady

Než začnete, ujistěte se, že máte splněny následující předpoklady:

- Vývojové prostředí Java nastavené na vašem počítači.
-  Nainstalovaná knihovna Aspose.Imaging for Java. Můžete si jej stáhnout z[webová stránka](https://releases.aspose.com/imaging/java/).
- Základní znalost programování v Javě.

## Importujte balíčky

Nejprve naimportujte potřebné balíčky pro vaši aplikaci Java, abyste mohli používat Aspose.Imaging for Java:

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

 Chcete-li začít vytvářet obrázek WMF, musíte vytvořit plátno, na kterém můžete kreslit tvary. The`WmfRecorderGraphics2D` class vám poskytuje toto plátno. Zde je návod, jak můžete vytvořit jeho instanci:

```java
// Cesta k adresáři dokumentů.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

V kódu výše specifikujeme rozměry plátna (100x100) a rozlišení (96 DPI).

## Krok 2: Nastavte barvu pozadí

 Dále definujte barvu pozadí pro vaše plátno. Můžete použít`setBackgroundColor` způsob nastavení barvy pozadí:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

V tomto příkladu nastavíme barvu pozadí na bílý kouř.

## Krok 3: Definujte pero a štětec

Chcete-li kreslit tvary na plátno, musíte definovat pero a štětec. Pero se používá pro kreslení obrysů a štětec se používá pro vyplňování tvarů. Zde je návod, jak vytvořit pero a pevný štětec:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

V tomto kódu vytvoříme modré pero a žlutozelený pevný štětec.

## Krok 4: Vyplňte a nakreslete tvary

Nyní vyplníme a nakreslíme na plátno některé základní tvary. Začneme polygonem:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Zde vyplníme a nakreslíme polygon pomocí určeného pera a štětce. Souřadnice a tvary můžete upravit podle potřeby.

## Krok 5: Použijte HatchBrush

 Chcete-li ke svým tvarům přidat textury, můžete použít a`HatchBrush`. Například:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

V tomto kódu vytvoříme křížový štětec s bílou a stříbrnou barvou.

## Krok 6: Vyplňte a nakreslete elipsu

Vyplníme a nakreslíme elipsu na plátno:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

Polohu a velikost elipsy můžete upravit podle potřeby.

## Krok 7: Nakreslete Arc a Cubic Bezier

Kreslení složitějších tvarů je také možné. Zde je návod, jak nakreslit oblouk a kubickou Bezierovu křivku:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

Ve výše uvedeném kódu nejprve nakreslíme oblouk tečkovanou čárou a poté nakreslíme kubickou Bezierovu křivku plným červeným perem.

## Krok 8: Přidejte obrázky

Do metasouboru WMF můžete také přidat obrázky. Jak na to:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

V tomto kroku načteme obrázek a umístíme jej na plátno na zadané souřadnice (50, 50).

## Krok 9: Kreslení čar a koláče

Chcete-li přidat čáry a tvary koláče, můžete postupovat podle těchto příkladů:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Zde nakreslíme čáru a vyplníme/nakreslíme tvar koláče pomocí určeného pera a štětce.

## Krok 10: Nakreslete křivku a text

Přidání textu a křivek je jednoduché:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

Podle potřeby můžete upravit písmo, text a body křivky.

## Krok 11: Uložte obrázek WMF

Jakmile vytvoříte obrázek WMF, je čas jej uložit:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Tento kód uloží obrázek WMF do určeného adresáře.

A je to! Úspěšně jste vygenerovali obrázek metasouboru WMF pomocí Aspose.Imaging for Java.

## Závěr

tomto tutoriálu jsme prozkoumali, jak vytvořit obrázky metasouborů WMF pomocí Aspose.Imaging pro Java. Pokryli jsme nezbytné předpoklady, importovali balíčky a poskytli podrobné pokyny pro kreslení různých tvarů, přidávání textur, vkládání obrázků a ukládání finálního obrázku. Aspose.Imaging for Java nabízí výkonnou sadu nástrojů pro manipulaci a vytváření obrázků, díky čemuž je cenným zdrojem pro vaše Java aplikace.

## FAQ

### Q1: Co je formát obrázku WMF?

A1: WMF je zkratka pro Windows Metafile, což je vektorový grafický formát používaný k ukládání obrázků, kreseb a dalších grafických dat. Běžně se používá v aplikacích Windows a lze jej snadno škálovat bez ztráty kvality.

### Q2: Kde si mohu stáhnout Aspose.Imaging pro Java?

 A2: Aspose.Imaging pro Java si můžete stáhnout z[webová stránka](https://releases.aspose.com/imaging/java/).

### Otázka 3: Potřebuji pokročilé znalosti programování, abych mohl používat Aspose.Imaging pro Java?

Odpověď 3: I když jsou vyžadovány základní znalosti programování v jazyce Java, Aspose.Imaging for Java poskytuje uživatelsky přívětivé rozhraní API, které zjednodušuje manipulaci s obrázky a úkoly vytváření.

### Q4: Mohu používat Aspose.Imaging pro Java pro komerční účely?

 Odpověď 4: Ano, Aspose.Imaging for Java nabízí komerční licence pro podniky a vývojáře. Licenci si můžete zakoupit od[tady](https://purchase.aspose.com/buy).

### Otázka 5: Kde mohu získat podporu nebo se ptát na Aspose.Imaging for Java?

 A5: Můžete najít podporu a zapojit se do komunity Aspose na[Aspose.Imaging fóra](https://forum.aspose.com/).