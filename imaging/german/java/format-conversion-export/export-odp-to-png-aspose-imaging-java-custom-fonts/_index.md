---
date: '2026-06-28'
description: Erfahren Sie, wie Sie ODP mit Aspose.Imaging für Java in PNG konvertieren,
  benutzerdefinierte Schriftarten festlegen und Systemschriftarten deaktivieren, um
  eine genaue Darstellung zu gewährleisten.
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
title: Wie man ODP in PNG mit Aspose.Imaging für Java konvertiert – Leitfaden für
  benutzerdefinierte Schriftarten und Export
url: /de/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Wie man ODP in PNG mit Aspose.Imaging für Java konvertiert – Benutzerdefinierte Schriften & Export‑Leitfaden

In modernen Java‑Anwendungen ist die Konvertierung von OpenDocument Presentation (ODP)‑Dateien in hochwertige PNG‑Bilder ein gängiges Bedürfnis – insbesondere, wenn das Branding durch benutzerdefinierte Schriften erhalten bleiben soll. Dieses Tutorial zeigt **wie man ODP** nach PNG mit Aspose.Imaging für Java konvertiert, führt Sie durch das Festlegen eines benutzerdefinierten Schriftartenordners, das Deaktivieren von System‑Fallback‑Schriften und das Feinabstimmen von Rasterisierungsoptionen für optimale Leistung.

**Was Sie lernen werden**
- Wie Sie ein benutzerdefiniertes Schriftartenverzeichnis für die ODP‑Konvertierung festlegen.  
- Wie Sie systemweite alternative Schriften deaktivieren, sodass nur Ihre ausgewählten Schriftarten verwendet werden.  
- Wie Sie eine ODP‑Datei mit genauen Abmessungen und Schriftarteinstellungen nach PNG exportieren.  
- Tipps zur Verbesserung von Geschwindigkeit und Speicherverbrauch bei der Verarbeitung großer Präsentationen.

## Schnelle Antworten
- **Kann ich Maven verwenden, um Aspose.Imaging hinzuzufügen?** Ja, fügen Sie die Maven‑Abhängigkeit hinzu und führen Sie `mvn install` aus.  
- **Benötige ich eine Lizenz für die Produktion?** Eine gültige Aspose.Imaging‑Lizenz ist für uneingeschränkte Nutzung erforderlich.  
- **Werden meine benutzerdefinierten Schriften berücksichtigt?** Legen Sie den Schriftartenordner fest und deaktivieren Sie systemweite Alternativen, um sie durchzusetzen.  
- **Welche Bildformate werden unterstützt?** Aspose.Imaging unterstützt über 120 Raster‑ und Vektorformate, darunter PNG, JPEG, TIFF und WebP.  
- **Ist die API thread‑sicher?** Ja, die meisten Aspose.Imaging‑Klassen sind sicher für gleichzeitige Nutzung, wenn Sie separate Instanzen pro Thread erstellen.

## Was bedeutet „how to convert odp“?
*„How to convert odp“* bezieht sich auf den Vorgang, eine OpenDocument Presentation‑Datei in ein anderes Format zu transformieren – typischerweise PNG – wobei Layout, Schriften und visuelle Treue erhalten bleiben. Aspose.Imaging für Java bietet einen einstufigen Workflow, der diese Konvertierung ohne externe Werkzeuge erledigt und Entwicklern ermöglicht, die Umwandlung direkt in ihre Anwendungen zu integrieren, mit minimalem Code.

## Warum Aspose.Imaging für Java verwenden?
Aspose.Imaging unterstützt **über 120 Ausgabeformate** und kann mehrseitige ODP‑Dateien rasterisieren, ohne das gesamte Dokument in den Speicher zu laden, wodurch der maximale RAM‑Verbrauch bei großen Präsentationen um bis zu 70 % reduziert wird. Die Bibliothek bietet zudem integriertes Schriftarten‑Management und eliminiert damit die Notwendigkeit von Drittanbieter‑Rendering‑Engines.

## Voraussetzungen
- **Bibliotheken**: Aspose.Imaging für Java ≥ 25.5.  
- **JDK**: Version 8 oder neuer.  
- **IDE**: IntelliJ IDEA, Eclipse oder ein beliebiger Java‑kompatibler Editor.  
- **Grundkenntnisse**: Java‑I/O, objektorientierte Programmierung und Bildkonzepte.

## Installationsanleitung

### Maven
Fügen Sie die folgende Abhängigkeit zu Ihrer `pom.xml` hinzu und führen Sie `mvn clean install` aus:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
Binden Sie die Bibliothek in Ihre `build.gradle`‑Datei ein und aktualisieren Sie das Projekt:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Direkter Download
Laden Sie die neueste JAR von [Aspose.Imaging für Java Releases](https://releases.aspose.com/imaging/java/) herunter.

## Schritte zum Erwerb einer Lizenz
Um die volle Funktionalität freizuschalten, wenden Sie eine temporäre oder permanente Lizenz an:

1. **Kostenlose Testversion** – Keine Lizenz erforderlich, eingeschränkte Funktionen.  
2. **Temporäre Lizenz** – Fordern Sie eine auf der [Aspose‑Website](https://purchase.aspose.com/temporary-license/) an.  
3. **Kauf** – Kaufen Sie ein Abonnement oder eine Dauerlizenz über die [Aspose‑Kaufseite](https://purchase.aspose.com/buy).

Initialisieren Sie die Bibliothek mit Ihrer Lizenzdatei:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## Wie man ein benutzerdefiniertes Schriftartenverzeichnis für die ODP‑Konvertierung festlegt?
`FontSettings` ist eine Klasse, die Schriftressourcen für Aspose.Imaging verwaltet. Laden Sie Ihre benutzerdefinierten Schriften, bevor irgendeine Bildverarbeitung beginnt. So wird sichergestellt, dass jede Folie die exakt von Ihnen bereitgestellten Schriftarten verwendet.

Legen Sie den Pfad des Schriftartenordners mit Aspose.Imaging’s `FontSettings` fest:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Definition anchor*: `FontSettings.setFontsFolder` gibt Aspose.Imaging an, wo im Dateisystem nach TrueType‑ und OpenType‑Schriften gesucht werden soll.

## Wie man systemweite alternative Schriften während der ODP‑Konvertierung deaktiviert?
Das Deaktivieren systemweiter Alternativen zwingt die Rendering‑Engine, die im Betriebssystem installierten Schriften zu ignorieren, sodass ausschließlich die von Ihnen bereitgestellten Schriften verwendet werden. Das verhindert unerwartete Schrift­substitutionen, die das Aussehen Ihrer Folien verändern können.

Deaktivieren Sie systemweite Alternativen mit dem folgenden Aufruf:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Definition anchor*: `FontSettings.setGetSystemAlternativeFont(false)` zwingt die Engine, nur die im definierten Ordner befindlichen Schriften zu nutzen und eliminiert unerwartete Substitutionen.

## Wie man eine ODP‑Datei mit einer angegebenen Schriftart in PNG exportiert?
`RasterizationOptions` definiert, wie Vektorseiten in Bitmap‑Bilder rasterisiert werden. Durch die Kombination von Schriftkonfiguration und Rasterisierungseinstellungen können Sie DPI, Hintergrundfarbe und Seitengröße für jedes exportierte PNG steuern.

Implementieren Sie die Export‑Methode wie unten gezeigt:

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

*Definition anchor*: Die Klasse `RasterizationOptions` steuert DPI, Seitengröße und Hintergrundfarbe für die erzeugten PNG‑Dateien.

### Häufige Fallstricke & Lösungen
- **Fehlende Schriftdateien** – Vergewissern Sie sich, dass jede in der ODP referenzierte `.ttf`‑ oder `.otf`‑Datei im von Ihnen festgelegten Ordner vorhanden ist.  
- **Falsche Dateipfade** – Verwenden Sie absolute Pfade oder lösen Sie relative Pfade relativ zu `System.getProperty("user.dir")` auf.  
- **Unzureichende Berechtigungen** – Stellen Sie sicher, dass der Java‑Prozess das Schriftartenverzeichnis lesen und in den Ausgabepfad schreiben kann.

## Praktische Anwendungen
1. **Markenkonforme Folien** – Exportieren Sie Präsentationen als PNG für die Web‑Veröffentlichung, wobei Unternehmensschriften erhalten bleiben.  
2. **Automatisierte Berichtserstellung** – Konvertieren Sie jede Folie in ein Bild zur Einbindung in PDF‑Berichte oder E‑Mail‑Newsletter.  
3. **Legacy‑Archivierung** – Speichern Sie ODP‑Inhalte als PNG, um zukünftige Zugänglichkeit ohne ODP‑Viewer zu gewährleisten.

## Leistungsüberlegungen
- Verwenden Sie die neueste Aspose.Imaging‑Version, um von Verbesserungen bei der mehr‑threadigen Rasterisierung zu profitieren (bis zu 2× schneller auf 8‑Kern‑CPUs).  
- Verpacken Sie die Bildverarbeitung in einen `try‑with‑resources`‑Block, um die rechtzeitige Freigabe nativer Ressourcen zu garantieren.  
- Passen Sie `RasterizationOptions` (z. B. niedrigere DPI) an, wenn Sie Tausende von Folien verarbeiten, um Qualität und Speicherverbrauch auszubalancieren.

## Häufig gestellte Fragen

**Q: Was ist die minimale Java‑Version, die erforderlich ist?**  
A: Aspose.Imaging für Java funktioniert mit JDK 8 und neuer; JDK 11 wird für langfristigen Support empfohlen.

**Q: Kann ich nur ausgewählte Folien konvertieren?**  
A: Ja, setzen Sie `rasterizationOptions.setPageNumber(specificSlideIndex)` bevor Sie `save` aufrufen.

**Q: Wie gehe ich mit passwortgeschützten ODP‑Dateien um?**  
A: Laden Sie die Datei mit `LoadOptions`, das das Passwort enthält, und fahren Sie dann mit denselben Schriftarteinstellungen fort.

**Q: Beeinflusst das Deaktivieren systemweiter Schriften die Leistung?**  
A: Es verbessert die Geschwindigkeit geringfügig, da die Engine die Suche nach System‑Schriften überspringt, was besonders bei Maschinen mit umfangreichen Schriftbibliotheken auffällt.

**Q: Wo finde ich weitere Code‑Beispiele?**  
A: Durchstöbern Sie die offizielle [Aspose.Imaging Dokumentation](https://reference.aspose.com/imaging/java/) für zusätzliche Szenarien wie Batch‑Konvertierung und Bildtransformationen.

## Zusätzliche Ressourcen
- [Aspose.Imaging für Java Releases](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/)  
- [Starten Sie Ihre kostenlose Testversion](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Dokumentation](https://reference.aspose.com/imaging/java/)  
- [Aspose.Imaging Forum](https://forum.aspose.com/c/imaging/14)  
- [Aspose Lizenz kaufen](https://purchase.aspose.com/buy)  
- [Bewerben Sie sich für eine temporäre Lizenz](https://purchase.aspose.com/temporary-license/)  

---

**Last Updated:** 2026-06-28  
**Tested With:** Aspose.Imaging für Java 25.5  
**Author:** Aspose

## Verwandte Tutorials

- [ODG in PNG konvertieren mit Aspose.Imaging für Java: Ein vollständiger Leitfaden](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Effiziente Bildkonvertierung in Java mit Aspose.Imaging: Ein vollständiger Leitfaden](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}