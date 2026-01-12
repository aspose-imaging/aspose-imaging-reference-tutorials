---
date: 2026-01-12
description: Naučte se, jak upravit kontrast v DICOM obrázcích – krok za krokem průvodce,
  jak upravit kontrast pomocí Aspose.Imaging pro Javu a převést DICOM na BMP.
linktitle: DICOM Image Contrast Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: Jak upravit kontrast v DICOM obrázcích pomocí Aspose.Imaging pro Java
url: /cs/java/image-processing-and-enhancement/dicom-image-contrast-adjustment/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Jak upravit kontrast v DICOM obrázcích pomocí Aspose.Imaging pro Java

V moderním lékařském zobrazování může **úprava kontrastu** rozhodnout o jasné diagnóze nebo o přehlédnutém detailu. Tento tutoriál vás provede přesné kroky, jak upravit kontrast v DICOM souborech pomocí Aspose.Imaging pro Java, a ukáže vám, jak převést tyto DICOM obrázky do BMP pro snadné prohlížení nebo další zpracování. Na konci budete mít připravený úryvek kódu, který můžete vložit do libovolného Java projektu.

## Rychlé odpovědi
- **Co dělá úprava kontrastu?** Rozšiřuje rozsah mezi tmavými a světlými pixely, čímž zvýrazňuje struktury.
- **Která knihovna je potřeba?** Aspose.Imaging pro Java.
- **Mohu výstup uložit jako BMP?** Ano – po úpravě kontrastu můžete DICOM převést do BMP.
- **Potřebuji licenci pro produkční použití?** Pro ne‑evaluační použití je vyžadována komerční licence.
- **Jaká verze Javy je podporována?** Java 8 a novější.

## Co je úprava kontrastu a proč je důležitá?
Úprava kontrastu zvyšuje vizuální odlišení mezi anatomickými strukturami, což pomáhá radiologům rychleji odhalit anomálie. V DICOM workflow úprava kontrastu před konverzí zajišťuje, že BMP výstup si zachová diagnostickou kvalitu potřebnou pro zprávy nebo archivaci.

## Předpoklady

Než se pustíte do kódu, ověřte, že máte:

1. **Aspose.Imaging pro Java** – stáhněte si ji z oficiálního webu [zde](https://releases.aspose.com/imaging/java/).  
2. **Vývojové prostředí Javy** – JDK 8+ a vaše oblíbené IDE (IntelliJ, Eclipse, VS Code, atd.).  
3. **DICOM obrázek** – libovolný soubor *.dcm*, který chcete vylepšit; ukázkové soubory jsou k dispozici online nebo můžete použít vlastní klinická data.

## Import balíčků

Tyto importy vám umožní pracovat s DICOM a ukládat do BMP.

```java
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
```

## Jak upravit kontrast v DICOM obrázcích

Níže je kompletní krok‑za‑krokem workflow. Každý krok je vysvětlen srozumitelně, takže můžete postupovat i když jste v Aspose.Imaging nováčkem.

### Krok 1: Zadejte cesty k souborům

Nastavte vstupní umístění DICOM a požadovanou výstupní cestu BMP. Nahraďte zástupný text skutečnou složkou na vašem počítači.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingContrast_out.bmp";
```

### Krok 2: Načtěte DICOM obrázek

Otevřeme DICOM soubor pomocí `FileInputStream`. Blok `try‑with‑resources` zajistí automatické uzavření proudu.

```java
File file = new File(inputFile);

try (FileInputStream fis = new FileInputStream(file)) {
    try (DicomImage image = (DicomImage) Image.load(fis)) {
        // All further processing happens inside this block
    }
} catch (IOException ex) {
    Logger.println(ex.getMessage());
    ex.printStackTrace();
}
```

### Krok 3: Upravit kontrast

Uvnitř vnitřního `try` bloku zavolejte `adjustContrast`. Hodnota může být od **‑100** (snížení) do **+100** (zvýšení). V tomto příkladu zvýšíme kontrast o 50 jednotek.

```java
image.adjustContrast(50);
```

### Krok 4: Převést DICOM na BMP a uložit obrázek

Po úpravě kontrastu vytvoříme instanci `BmpOptions` a výsledek uložíme jako BMP soubor. Tento krok **převádí DICOM na BMP**, čímž získáte široce podporovaný rastrový formát.

```java
image.save(outputFile, new BmpOptions());
```

## Časté problémy a tipy

- **Neplatný DICOM soubor** – Ujistěte se, že soubor *.dcm* není komprimován nepodporovanou přenosovou syntaxí. Aspose.Imaging podporuje většinu standardních DICOM kódování.
- **Hodnota kontrastu mimo rozsah** – Hodnoty mimo ±100 jsou oříznuty; zvolte číslo, které vyhovuje histogramu obrázku.
- **Spotřeba paměti** – Velké DICOM série mohou spotřebovat značné množství RAM. Zpracovávejte jeden řez najednou, pokud narazíte na `OutOfMemoryError`.

## Závěr

Nyní jste se naučili **jak upravit kontrast** v DICOM obrázcích pomocí Aspose.Imaging pro Java a **jak převést DICOM na BMP** pro následné úkoly. Tento workflow je rychlý, spolehlivý a lze jej integrovat do větších pipeline pro medicínské obrazy, ať už budujete PACS prohlížeč, výzkumný nástroj nebo automatizovaný systém reportování.

Aspose.Imaging pro Java abstrahuje nízkoúrovňové zpracování DICOM, takže se můžete soustředit na klinickou hodnotu vašich snímků.

## Často kladené otázky

**Q: Co je DICOM a proč je standardem v medicínském zobrazování?**  
A: DICOM (Digital Imaging and Communications in Medicine) je univerzální formát pro ukládání, přenos a sdílení medicínských obrázků, který zajišťuje interoperabilitu mezi zařízeními a institucemi.

**Q: Mohu upravit jas současně s kontrastem?**  
A: Ano, metoda `adjustBrightness(int value)` funguje podobně a může být řetězena před uložením.

**Q: Podporuje Aspose.Imaging i jiné výstupní formáty kromě BMP?**  
A: Rozhodně – můžete exportovat do PNG, JPEG, TIFF a mnoha dalších pomocí odpovídajících tříd `*Options`.

**Q: Je pro produkční použití vyžadována komerční licence?**  
A: Ano. Licenci můžete zakoupit [zde](https://purchase.aspose.com/buy) nebo získat dočasnou evaluační licenci [zde](https://purchase.aspose.com/temporary-license/).

**Q: Kde najdu další pomoc a příklady?**  
A: Komunitní fórum Aspose.Imaging pro Java poskytuje rozsáhlou dokumentaci a ukázkový kód: [Aspose.Imaging for Java forum](https://forum.aspose.com/).

---

**Poslední aktualizace:** 2026-01-12  
**Testováno s:** Aspose.Imaging pro Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}