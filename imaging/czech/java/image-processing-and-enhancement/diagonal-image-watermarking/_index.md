---
"description": "Vylepšete své obrázky diagonálním vodoznakem pomocí Aspose.Imaging pro Javu. Postupujte podle tohoto podrobného návodu a bez námahy vytvářejte úžasné obrázky s vodoznakem."
"linktitle": "Diagonální vodoznak na obrázku"
"second_title": "API pro zpracování obrazu v Javě Aspose.Imaging"
"title": "Diagonální vodoznak na obrázku s Aspose.Imaging pro Javu"
"url": "/cs/java/image-processing-and-enhancement/diagonal-image-watermarking/"
"weight": 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Diagonální vodoznak na obrázku s Aspose.Imaging pro Javu


Pokud chcete vylepšit své obrázky stylovým diagonálním vodoznakem, Aspose.Imaging pro Javu je tu, aby vám pomohl. V tomto podrobném návodu vás provedeme procesem přidání vodoznaku s textem otočeným o 45 stupňů do existujícího obrázku JPG. Nemusíte být odborníkem na Javu ani na zpracování obrázků, abyste mohli postupovat podle pokynů – každý příklad rozdělíme do několika kroků, abyste snadno dosáhli profesionálních výsledků.

## Předpoklady

Než se ponoříme do vzrušujícího světa vodoznaků v obrázcích, budete potřebovat pár věcí:

1. Aspose.Imaging pro Javu: Ujistěte se, že máte nainstalovaný Aspose.Imaging pro Javu. Odkaz ke stažení naleznete [zde](https://releases.aspose.com/imaging/java/).

2. Vývojové prostředí Java: Na počítači byste měli mít nainstalované funkční vývojové prostředí Java.

3. Obrázek pro vodoznak: Připravte si obrázek, který chcete vodoznakem použít, a uložte jej do adresáře. Pro tento tutoriál můžete použít ukázkový obrázek.

## Importovat balíčky

Nejprve importujte potřebné balíčky, abyste připravili svůj projekt Java pro vodoznaky do obrázků. Níže jsou uvedeny základní balíčky, které je třeba zahrnout:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Krok 1: Načtení existujícího obrázku

Načtěte obrázek, na který chcete vložit vodoznak. V tomto příkladu předpokládáme, že máte ve složce „ModifyingImages“ obrázek JPG s názvem „SampleTiff1.tiff“.

```java
// Cesta k adresáři s dokumenty.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Načíst existující obrázek JPG
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Zbytek kódu jde sem
}
```

## Krok 2: Příprava textu a grafiky vodoznaku

Nyní deklarujme text vodoznaku a nastavme pro něj grafiku.

```java
// Deklarujte objekt typu String s textem vodoznaku
String theString = "45 Degree Rotated Text";

// Vytvořte a inicializujte instanci třídy Graphics
Graphics graphics = new Graphics(image);

// Inicializovat objekt SizeF pro uložení velikosti obrázku
Size sz = graphics.getImage().getSize();
```

## Krok 3: Definujte písmo a štětec

Nastavte písmo a štětec pro vodoznak. Písmo, velikost a styl si můžete přizpůsobit svým preferencím.

```java
// Vytvořte instanci třídy Font a inicializujte ji s nastavením typu Font Face, Size a Style.
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Vytvořte instanci SolidBrush a nastavte její různé vlastnosti
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Krok 4: Naformátujte text

Definujte formát textu vodoznaku, včetně zarovnání a formátovacích příznaků.

```java
// Inicializujte objekt třídy StringFormat a nastavte jeho různé vlastnosti
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Krok 5: Použití transformace

Vytvořte transformační matici pro umístění a otočení textu vodoznaku. V tomto příkladu otočíme text o 45 stupňů.

```java
// Vytvořte objekt třídy Matrix pro transformaci
Matrix matrix = new Matrix();
// Nejprve posunutí, poté rotace
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Nastavte transformaci pomocí matice
graphics.setTransform(matrix);
```

## Krok 6: Nakreslete a uložte

Nyní je čas přidat text k obrázku a uložit obrázek s vodoznakem na požadované místo.

```java
// Nakreslete řetězec na obrázek
graphics.drawString(theString, font, brush, 0, 0, format);

// Uložit výstup na disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Gratulujeme! Úspěšně jste přidali diagonální vodoznak do obrázku pomocí Aspose.Imaging pro Javu.

## Závěr

tomto tutoriálu jsme se naučili, jak vylepšit obrázky diagonálním vodoznakem pomocí Aspose.Imaging pro Javu. Je to výkonný nástroj pro přidání profesionálního nádechu k vašim obrázkům. Pomocí několika jednoduchých kroků můžete vytvořit úžasné obrázky s vodoznakem, které vyčnívají z řady ostatních.

## Často kladené otázky

### Q1: Je Aspose.Imaging pro Javu vhodný pro začátečníky?

A1: Rozhodně! Aspose.Imaging pro Javu nabízí uživatelsky přívětivé rozhraní a komplexní dokumentaci. I začátečníci se mohou rychle seznámit se zpracováním obrázků.

### Q2: Mohu si přizpůsobit text a styl vodoznaku?

A2: Ano, text vodoznaku, písmo, velikost, barvu a úhel natočení si můžete snadno přizpůsobit tak, aby odpovídaly vašim preferencím a brandingu.

### Q3: Podporuje Aspose.Imaging pro Javu i jiné formáty obrázků než JPG?

A3: Ano, Aspose.Imaging pro Javu podporuje širokou škálu obrazových formátů, včetně BMP, PNG, GIF a dalších.

### Q4: Je k dispozici bezplatná zkušební verze Aspose.Imaging pro Javu?

A4: Ano, můžete si vyzkoušet Aspose.Imaging pro Javu s bezplatnou zkušební verzí. Stáhněte si ji. [zde](https://releases.aspose.com/).

### Q5: Kde najdu pomoc nebo podporu pro Aspose.Imaging pro Javu?

A5: Pokud máte jakékoli dotazy nebo potřebujete pomoc, navštivte fórum podpory Aspose.Imaging pro Javu [zde](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}