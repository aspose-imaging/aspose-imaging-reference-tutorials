---
date: '2026-06-28'
description: Naučte se, jak převést ODP na PNG pomocí Aspose.Imaging for Java, nastavit
  vlastní fonty a zakázat systémové fonty pro přesné vykreslení.
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: Jak převést ODP na PNG pomocí Aspose.Imaging for Java – Průvodce vlastními
  fonty a exportem
url: /cs/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Jak převést ODP na PNG pomocí Aspose.Imaging pro Java – Vlastní písma a průvodce exportem

V moderních Java aplikacích je převod souborů OpenDocument Presentation (ODP) na vysoce kvalitní PNG obrázky běžnou požadavkem—zejména když potřebujete zachovat značku pomocí vlastních písem. Tento tutoriál ukazuje **jak převést ODP** na PNG pomocí Aspose.Imaging pro Java, provádí vás nastavením složky s vlastními písmy, vypnutím systémových náhradních písem a jemným laděním možností rasterizace pro optimální výkon.

**Co se naučíte**
- Jak nastavit vlastní adresář písem pro převod ODP.
- Jak zakázat systémová alternativní písma, aby byla použita pouze vámi vybraná písma.
- Jak exportovat soubor ODP do PNG s přesnými rozměry a nastavením písem.
- Tipy pro zlepšení rychlosti a využití paměti při zpracování velkých prezentací.

## Rychlé odpovědi
- **Mohu použít Maven k přidání Aspose.Imaging?** Ano, přidejte Maven závislost a spusťte `mvn install`.  
- **Potřebuji licenci pro produkci?** Platná licence Aspose.Imaging je vyžadována pro neomezené používání.  
- **Budou moje vlastní písma respektována?** Nastavte složku s písmy a zakažte systémové alternativy, aby byla vynucena.  
- **Jaké formáty obrázků jsou podporovány?** Aspose.Imaging podporuje více než 120 rastrových a vektorových formátů, včetně PNG, JPEG, TIFF a WebP.  
- **Je API thread‑safe?** Ano, většina tříd Aspose.Imaging je bezpečná pro souběžné použití, pokud vytvoříte samostatné instance pro každý vlákno.

## Co je “how to convert odp”?
*“How to convert odp”* odkazuje na proces převodu souboru OpenDocument Presentation do jiného formátu—často PNG—při zachování rozvržení, písem a vizuální věrnosti. Aspose.Imaging pro Java poskytuje jednofázový workflow, který tento převod provádí bez potřeby externích nástrojů, což vývojářům umožňuje integrovat převod přímo do svých aplikací s minimálním kódem.

## Proč použít Aspose.Imaging pro Java?
Aspose.Imaging podporuje **více než 120 výstupních formátů** a dokáže rasterizovat více‑stránkové ODP soubory bez načítání celého dokumentu do paměti, čímž snižuje špičkovou spotřebu RAM až o 70 % u velkých prezentací. Knihovna také nabízí vestavěnou správu písem, čímž eliminuje potřebu třetích stran renderovacích engine.

## Předpoklady
- **Knihovny**: Aspose.Imaging pro Java ≥ 25.5.  
- **JDK**: Verze 8 nebo novější.  
- **IDE**: IntelliJ IDEA, Eclipse nebo jakýkoli Java‑kompatibilní editor.  
- **Základní znalosti**: Java I/O, objektově orientované programování a koncepty obrázků.

## Pokyny k instalaci

### Maven
Přidejte následující závislost do svého `pom.xml` a spusťte `mvn clean install`:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
Zahrňte knihovnu do souboru `build.gradle` a obnovte projekt:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Direct Download
Stáhněte nejnovější JAR z [vydání Aspose.Imaging pro Java](https://releases.aspose.com/imaging/java/).

## Kroky získání licence
Pro odemčení plné funkčnosti použijte dočasnou nebo trvalou licenci:

1. **Free Trial** – Licence není vyžadována, omezené funkce.  
2. **Temporary License** – Požádejte o ni na [Aspose webu](https://purchase.aspose.com/temporary-license/).  
3. **Purchase** – Kupte předplatné nebo trvalou licenci na [stránce nákupu Aspose](https://purchase.aspose.com/buy).

Inicializujte knihovnu pomocí souboru licence:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## Jak nastavit vlastní adresář písem pro převod ODP?
`FontSettings` je třída, která spravuje zdroje písem pro Aspose.Imaging. Načtěte své vlastní písma před zahájením jakéhokoli zpracování obrázku. Tím zajistíte, že každá snímek použije přesně písma, která poskytnete.

Nastavte cestu ke složce s písmy pomocí `FontSettings` Aspose.Imaging:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Definice*: `FontSettings.setFontsFolder` říká Aspose.Imaging, kde hledat TrueType a OpenType písma v souborovém systému.

## Jak zakázat systémová alternativní písma během převodu ODP?
Zakázání systémových alternativ nutí renderovací engine ignorovat písma nainstalovaná v operačním systému, což zaručuje, že budou použita pouze písma, která poskytnete. Tím se eliminuje neočekávaná náhrada písem, která může změnit vizuální vzhled vašich snímků.

Zakázat systémové alternativy pomocí následujícího volání:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Definice*: `FontSettings.setGetSystemAlternativeFont(false)` nutí engine používat pouze písma umístěná ve složce, kterou jste definovali, čímž eliminuje neočekávané náhrady.

## Jak exportovat soubor ODP do PNG s určeným písmem?
`RasterizationOptions` určuje, jak jsou vektorové stránky rasterizovány do bitmapových obrázků. Kombinací nastavení písem s nastavením rasterizace můžete řídit DPI, barvu pozadí a velikost stránky pro každý exportovaný PNG.

Implementujte exportní metodu, jak je ukázáno níže:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*Definice*: Třída `RasterizationOptions` řídí DPI, velikost stránky a barvu pozadí pro generované PNG soubory.

### Časté úskalí a řešení
- **Chybějící soubory písem** – Ověřte, že každý `.ttf` nebo `.otf` odkazovaný v ODP je přítomen ve složce, kterou jste nastavili.  
- **Nesprávné cesty k souborům** – Použijte absolutní cesty nebo řešte relativní cesty vůči `System.getProperty("user.dir")`.  
- **Nedostatečná oprávnění** – Zajistěte, aby Java proces mohl číst složku s písmy a zapisovat do výstupní složky.

## Praktické aplikace
1. **Prezentace s konzistentní značkou** – Exportujte prezentace jako PNG pro webové publikování při zachování firemních písem.  
2. **Automatizovaná tvorba reportů** – Převádějte každý snímek na obrázek pro zahrnutí do PDF reportů nebo e‑mailových newsletterů.  
3. **Vytváření archivů starších verzí** – Ukládejte obsah ODP jako PNG, aby byla zajištěna budoucí přístupnost bez potřeby prohlížečů ODP.

## Úvahy o výkonu
- Používejte nejnovější verzi Aspose.Imaging, abyste získali výhody vylepšení multi‑threaded rasterizace (až 2× rychlejší na 8‑jádrových CPU).  
- Zabalte zpracování obrázků do bloku try‑with‑resources, aby bylo zajištěno včasné uvolnění nativních zdrojů.  
- Upravit `RasterizationOptions` (např. nižší DPI) při zpracování tisíců snímků, aby se vyvážila kvalita a využití paměti.

## Často kladené otázky

**Q: Jaká je minimální verze Javy požadovaná?**  
A: Aspose.Imaging pro Java funguje s JDK 8 a novějšími; JDK 11 je doporučená pro dlouhodobou podporu.

**Q: Mohu převést pouze vybrané snímky?**  
A: Ano, nastavte `rasterizationOptions.setPageNumber(specificSlideIndex)` před voláním `save`.

**Q: Jak zacházet se soubory ODP chráněnými heslem?**  
A: Načtěte soubor pomocí `LoadOptions`, který obsahuje heslo, a poté pokračujte se stejným nastavením písem.

**Q: Ovlivňuje zakázání systémových písem výkon?**  
A: Mírně zvyšuje rychlost, protože engine přeskočí vyhledávání systémových písem, což je zvláště patrné na strojích s velkými kolekcemi písem.

**Q: Kde najdu více ukázek kódu?**  
A: Prozkoumejte oficiální [dokumentaci Aspose.Imaging](https://reference.aspose.com/imaging/java/) pro další scénáře, jako je hromadná konverze a transformace obrázků.

## Další zdroje
- [Vydání Aspose.Imaging pro Java](https://releases.aspose.com/imaging/java/)  
- [Vydání Aspose.Imaging](https://releases.aspose.com/imaging/java/)  
- [Začněte svou bezplatnou zkušební verzi](https://releases.aspose.com/imaging/java/)  
- [Dokumentace Aspose.Imaging](https://reference.aspose.com/imaging/java/)  
- [Fórum Aspose.Imaging](https://forum.aspose.com/c/imaging/14)  
- [Koupit licenci Aspose](https://purchase.aspose.com/buy)  
- [Požádat o dočasnou licenci](https://purchase.aspose.com/temporary-license/)  

---

**Last Updated:** 2026-06-28  
**Tested With:** Aspose.Imaging for Java 25.5  
**Author:** Aspose

## Související tutoriály

- [Převod ODG na PNG pomocí Aspose.Imaging pro Java: Kompletní průvodce](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Efektivní konverze obrázků v Javě s Aspose.Imaging: Kompletní průvodce](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}