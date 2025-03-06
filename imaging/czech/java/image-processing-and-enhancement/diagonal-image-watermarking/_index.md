---
title: Diagonální obrazový vodoznak s Aspose.Imaging pro Java
linktitle: Diagonální obrázek vodoznak
second_title: Aspose.Imaging Java Image Processing API
description: Vylepšete své obrázky pomocí diagonálního vodoznaku pomocí Aspose.Imaging pro Java. Postupujte podle tohoto podrobného průvodce a bez námahy vytvořte úžasné obrázky s vodoznakem.
weight: 14
url: /cs/java/image-processing-and-enhancement/diagonal-image-watermarking/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Diagonální obrazový vodoznak s Aspose.Imaging pro Java


Pokud chcete vylepšit své obrázky stylovým diagonálním vodoznakem, Aspose.Imaging pro Java vám pomůže. V tomto podrobném průvodci vás provedeme procesem přidání textového vodoznaku otočeného o 45 stupňů do existujícího obrázku JPG. Abyste mohli pokračovat, nemusíte být odborníkem na Javu nebo zpracování obrázků – každý příklad rozdělíme do několika kroků, abyste mohli snadno dosáhnout profesionálních výsledků.

## Předpoklady

Než se ponoříme do vzrušujícího světa obrazového vodoznaku, budete potřebovat několik věcí:

1.  Aspose.Imaging for Java: Ujistěte se, že máte nainstalovaný Aspose.Imaging for Java. Odkaz ke stažení najdete[tady](https://releases.aspose.com/imaging/java/).

2. Vývojové prostředí Java: Na svém počítači byste měli mít nastavené funkční vývojové prostředí Java.

3. Obrázek k vodoznaku: Připravte obrázek, který chcete označit vodoznakem, a uložte jej do adresáře. Pro tento tutoriál můžete použít ukázkový obrázek.

## Importujte balíčky

Nejprve naimportujte potřebné balíčky, aby byl váš projekt Java připraven na vodoznak obrázku. Níže jsou uvedeny základní balíčky, které musíte zahrnout:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Krok 1: Načtěte existující obrázek

Vložte obrázek, který chcete přidat vodoznak. V tomto příkladu předpokládáme, že máte ve svém adresáři "ModifyingImages" obrázek JPG s názvem "SampleTiff1.tiff".

```java
// Cesta k adresáři dokumentů.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Načtěte existující obrázek JPG
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Zbytek kódu je zde
}
```

## Krok 2: Připravte text a grafiku vodoznaku

Nyní deklarujeme text vodoznaku a nastavíme grafiku vodoznaku.

```java
// Deklarujte objekt typu String textem vodoznaku
String theString = "45 Degree Rotated Text";

// Vytvořte a inicializujte instanci třídy Graphics
Graphics graphics = new Graphics(image);

// Inicializujte objekt SizeF pro uložení velikosti obrázku
Size sz = graphics.getImage().getSize();
```

## Krok 3: Definujte písmo a štětec

Nastavte písmo a štětec pro vodoznak. Písmo, velikost a styl si můžete přizpůsobit svým preferencím.

```java
// Vytvořte instanci Písma, inicializujte ji pomocí Řez písma, Velikost a Styl
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Vytvořte instanci SolidBrush a nastavte jeho různé vlastnosti
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Krok 4: Formátujte svůj text

Definujte formát pro text vodoznaku, včetně zarovnání a příznaků formátu.

```java
// Inicializujte objekt třídy StringFormat a nastavte jeho různé vlastnosti
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Krok 5: Aplikujte transformaci

Vytvořte transformační matici pro umístění a otočení textu vodoznaku. V tomto příkladu otočíme text o 45 stupňů.

```java
// Vytvořte objekt třídy Matrix pro transformaci
Matrix matrix = new Matrix();
//Nejdříve posun, pak rotace
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Nastavte Transformaci pomocí Matrixu
graphics.setTransform(matrix);
```

## Krok 6: Nakreslete a uložte

Nyní je čas přidat text do obrázku a uložit obrázek s vodoznakem na požadované místo.

```java
// Nakreslete řetězec na obrázek
graphics.drawString(theString, font, brush, 0, 0, format);

// Uložit výstup na disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Gratulujeme! Úspěšně jste do obrázku přidali diagonální vodoznak pomocí Aspose.Imaging for Java.

## Závěr

V tomto tutoriálu jsme se naučili, jak vylepšit obrázky pomocí diagonálního vodoznaku pomocí Aspose.Imaging pro Java. Je to mocný nástroj pro přidání profesionálního nádechu vašim snímkům. Pomocí několika jednoduchých kroků můžete vytvořit úžasné obrázky s vodoznakem, které vyniknou nad ostatními.

## FAQ

### Q1: Je Aspose.Imaging pro Java vhodný pro začátečníky?

A1: Rozhodně! Aspose.Imaging for Java nabízí uživatelsky přívětivé rozhraní a komplexní dokumentaci. Se zpracováním obrazu mohou rychle začít i začátečníci.

### Q2: Mohu přizpůsobit text a styl vodoznaku?

A2: Ano, můžete snadno přizpůsobit text vodoznaku, písmo, velikost, barvu a úhel otočení tak, aby odpovídaly vašim preferencím a značce.

### Q3: Podporuje Aspose.Imaging for Java jiné formáty obrázků kromě JPG?

Odpověď 3: Ano, Aspose.Imaging for Java podporuje širokou škálu obrazových formátů, včetně BMP, PNG, GIF a dalších.

### Q4: Je k dispozici bezplatná zkušební verze pro Aspose.Imaging pro Java?

 A4: Ano, můžete vyzkoušet Aspose.Imaging pro Java s bezplatnou zkušební verzí. Pochopit to[tady](https://releases.aspose.com/).

### Q5: Kde najdu nápovědu nebo podporu pro Aspose.Imaging for Java?

 Odpověď 5: Pokud máte nějaké dotazy nebo potřebujete pomoc, navštivte fórum podpory Aspose.Imaging for Java[tady](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
