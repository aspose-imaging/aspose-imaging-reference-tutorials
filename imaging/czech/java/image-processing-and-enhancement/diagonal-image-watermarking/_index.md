---
date: 2026-01-09
description: Naučte se, jak přidat vodoznak do obrázků pomocí Aspose.Imaging pro Javu.
  Tento tutoriál pro zpracování obrázků v Javě ukazuje krok za krokem, jak rychle
  vytvořit diagonální vodoznak.
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: Jak přidat vodoznak – Diagonální vodoznakování obrázku (Java)
url: /cs/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Jak přidat vodoznak – Diagonální vodoznakování obrázku (Java)

Pokud hledáte **how to add watermark** do svých obrázků se stylovým diagonálním natočením, Aspose.Imaging pro Java to usnadňuje. V tomto krok‑za‑krokem tutoriálu vás provedeme přidáním textového vodoznaku otočeného o 45 stupňů do JPG (nebo jakéhokoli podporovaného) obrázku. Nemusíte být Java kouzelník – každý blok je vysvětlen jednoduchým jazykem, takže výsledek můžete replikovat během několika minut.

## Rychlé odpovědi
- **Jaká knihovna je použita?** Aspose.Imaging for Java  
- **Jaké primární klíčové slovo je pokryto?** how to add watermark  
- **Podporované formáty obrázků?** JPEG, PNG, BMP, TIFF, GIF and more  
- **Kolik kódu je potřeba?** Only seven concise code blocks  
- **Potřebuji licenci pro testování?** A free trial is available; a license is required for production  

## Co znamená “how to add watermark” ve zpracování obrazu?
Přidání vodoznaku znamená překrytí semi‑průhledného textu nebo grafiky na obrázek za účelem ochrany vlastnictví nebo předání značky. Diagonální vodoznak je zvláště účinný, protože pokrývá celý obrázek a je obtížnější jej oříznout.

## Proč použít Aspose.Imaging pro Java?
Aspose.Imaging poskytuje high‑level API, které abstrahuje nízko‑úrovňovou manipulaci s pixely, podporuje desítky formátů a funguje na jakémkoli Java runtime. Umožňuje vám soustředit se na *co* chcete dosáhnout — například přidání diagonálního vodoznaku — bez starostí o zvláštnosti formátů obrázků.

## Předpoklady

Než se pustíme dál, ujistěte se, že máte následující:

1. **Aspose.Imaging for Java** – stáhněte nejnovější verzi z oficiálního webu **[here](https://releases.aspose.com/imaging/java/)**.  
2. **Java Development Environment** – JDK 8+ a vaše oblíbené IDE (IntelliJ, Eclipse, VS Code, atd.).  
3. **An image to watermark** – umístěte ukázkový JPG/TIFF/PNG do složky, na kterou budete v kódu odkazovat.

## Import balíčků

Nejprve importujte třídy, které budete potřebovat. Udržování importů pohromadě usnadňuje čtení a údržbu kódu.

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Krok 1: Načtení existujícího obrázku

Začínáme načtením zdrojového obrázku. Metoda `Image.load` automaticky detekuje formát.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **Tip:** Zabalte objekt `Image` do bloku try‑with‑resources (jak je ukázáno), aby byl automaticky uvolněn a zabránili tak únikům paměti.

## Krok 2: Příprava textu a grafiky vodoznaku

Vytvořte objekt `Graphics` spojený s načteným obrázkem a uložte velikost obrázku pro pozdější výpočty.

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## Krok 3: Definice písma a štětce

Zvolte písmo, které vynikne, a štětec, který určuje barvu a průhlednost vodoznaku. Nastavte průhlednost tak, aby byl vodoznak semi‑transparentní.

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Krok 4: Formátování textu

Nastavte zarovnání a formátovací příznaky, aby byl text při vykreslování vycentrován.

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Krok 5: Aplikace transformace

Transformační matice nám umožňuje přesunout počátek do středu obrázku a poté otočit text o ‑45° (ve směru hodinových ručiček).

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## Krok 6: Vykreslení a uložení

Nakonec vykreslete řetězec na obrázek a výsledek zapište na disk.

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Když otevřete `AddDiagonalWatermarkToImage_out.jpg`, uvidíte červený, semi‑transparentní text nakloněný přes střed obrázku.

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|---------|--------|-----|
| Vodoznak je příliš slabý | Průhlednost nastavena na 0 (zcela průhledná) | Zvyšte průhlednost, např. `brush.setOpacity(0.5f);` |
| Text je oříznutý na okrajích | Posunutí není vycentrováno pro nečtvercové obrázky | Použijte `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` jak je ukázáno, poté případně upravte úhel rotace |
| Chyba nepodporovaného formátu obrázku | Použití starší verze Aspose.Imaging | Aktualizujte na nejnovější verzi Aspose.Imaging |

## Často kladené otázky

### Q1: Je Aspose.Imaging pro Java vhodný pro začátečníky?

**A:** Rozhodně! API je intuitivní a dokumentace poskytuje jasné příklady. I vývojáři noví v oblasti zpracování obrazu mohou tento tutoriál následovat a rychle vytvořit profesionální výsledky.

### Q2: Mohu přizpůsobit text a styl vodoznaku?

**A:** Ano. Změňte proměnnou `theString`, vyberte jiné `Font`, upravte `brush.setColor(...)` nebo změňte úhel rotace v matici podle vaší značky.

### Q3: Podporuje Aspose.Imaging pro Java další formáty obrázků kromě JPG?

**A:** Ano. Knihovna pracuje s BMP, PNG, GIF, TIFF, PSD a mnoha dalšími. Stačí nasměrovat metodu `Image.load` na příslušný soubor.

### Q4: Je k dispozici bezplatná zkušební verze Aspose.Imaging pro Java?

**A:** Ano, můžete vyzkoušet Aspose.Imaging pro Java s bezplatnou zkušební verzí. Získejte ji **[here](https://releases.aspose.com/)**.

### Q5: Kde mohu najít pomoc nebo podporu pro Aspose.Imaging pro Java?

**A:** Pro otázky, hlášení chyb nebo rady ohledně osvědčených postupů navštivte fórum podpory Aspose.Imaging pro Java **[here](https://forum.aspose.com/)**.

---

**Poslední aktualizace:** 2026-01-09  
**Testováno s:** Aspose.Imaging pro Java 24.11 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}