---
date: '2026-07-08'
description: Erfahren Sie, wie Sie TIFF aus DjVu mit Aspose.Imaging für Java exportieren.
  Schritt‑für‑Schritt‑Anleitung zum Laden, Auswählen von Seiten und zu Exportoptionen.
keywords:
- how to export tiff
- java image processing
- maven aspose imaging
- how to load djvu
lastmod: '2026-07-08'
og_description: Entdecken Sie, wie Sie TIFF aus DjVu in Java mit Aspose.Imaging exportieren.
  Folgen Sie unserem Schritt‑für‑Schritt‑Tutorial für schnelle und zuverlässige Bildkonvertierung.
og_image_alt: Guide showing Java code to convert DjVu pages to TIFF with Aspose.Imaging
og_title: Wie man TIFF exportiert – Java‑Leitfaden mit Aspose.Imaging
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: Learn how to export TIFF from DjVu using Aspose.Imaging for Java. Step-by-step
    guide covering loading, page selection, and export options.
  headline: How to Export TIFF – Load and Export DjVu Pages in Java with Aspose.Imaging
  type: TechArticle
- description: Learn how to export TIFF from DjVu using Aspose.Imaging for Java. Step-by-step
    guide covering loading, page selection, and export options.
  name: How to Export TIFF – Load and Export DjVu Pages in Java with Aspose.Imaging
  steps:
  - name: '**Archival Systems** – Preserve scanned documents in a universally accepted
      format.'
    text: '**Archival Systems** – Preserve scanned documents in a universally accepted
      format.'
  - name: '**Document Review Workflows** – Pull out only the pages that need annotation.'
    text: '**Document Review Workflows** – Pull out only the pages that need annotation.'
  - name: '**Integration with DMS** – Feed TIFF images into existing document‑management
      pipelines that do not understand DjVu.'
    text: '**Integration with DMS** – Feed TIFF images into existing document‑management
      pipelines that do not understand DjVu.'
  type: HowTo
- questions:
  - answer: '`DjvuImage` represents a DjVu document in memory.'
    question: What is the main class for DjVu handling?
  - answer: Just two lines after loading the image.
    question: How many lines of code are needed to export a page to TIFF?
  - answer: '`com.aspose:aspose-imaging` (version 25.5+).'
    question: Which Maven artifact provides DjVu support?
  - answer: Yes, use `IntRange` to specify a range.
    question: Can I export multiple pages at once?
  - answer: A full license is required; a temporary trial is available.
    question: Do I need a license for production?
  type: FAQPage
tags:
- convert DjVu
- Aspose.Imaging
- Java image conversion
title: Wie man TIFF exportiert – DjVu‑Seiten in Java mit Aspose.Imaging laden und
  exportieren
url: /de/java/format-conversion-export/load-export-djvu-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Wie man TIFF exportiert – DjVu‑Seiten in Java mit Aspose.Imaging lädt und exportiert

## Einführung

Wenn Sie **how to export TIFF** aus einem DjVu‑Dokument in einer Java‑Anwendung benötigen, sind Sie hier genau richtig. DjVu ist ein kompaktes Format für gescannte Dokumente, aber viele nachgelagerte Systeme benötigen TIFF. Dieses Tutorial führt Sie durch das Laden einer DjVu‑Datei, das Auswählen der benötigten Seiten und das Exportieren dieser als hochqualitative TIFF‑Bilder mit Aspose.Imaging für Java. Am Ende haben Sie ein wiederverwendbares Snippet, das in jede Java‑basierte Bildverarbeitungspipeline passt.

**Was Sie lernen werden**
- Wie man DjVu‑Bilder mit Aspose.Imaging in Java lädt  
- Exportieren bestimmter DjVu‑Seiten in das TIFF‑Format  
- Konfigurieren von Exportoptionen und Verstehen wichtiger Parameter  

Bevor wir beginnen, stellen Sie sicher, dass Ihre Entwicklungsumgebung die unten aufgeführten Voraussetzungen erfüllt.

## Schnelle Antworten
- **Was ist die Hauptklasse für die DjVu‑Verarbeitung?** `DjvuImage` repräsentiert ein DjVu‑Dokument im Speicher.  
- **Wie viele Code‑Zeilen werden benötigt, um eine Seite nach dem Laden des Bildes in TIFF zu exportieren?** Nur zwei Zeilen nach dem Laden des Bildes.  
- **Welches Maven‑Artefakt liefert DjVu‑Unterstützung?** `com.aspose:aspose-imaging` (Version 25.5+).  
- **Kann ich mehrere Seiten gleichzeitig exportieren?** Ja, verwenden Sie `IntRange`, um einen Bereich anzugeben.  
- **Benötige ich eine Lizenz für die Produktion?** Eine Voll‑Lizenz ist erforderlich; ein temporäres Test‑Lizenz ist verfügbar.

## Was bedeutet „how to export tiff“?
**„How to export TIFF“** bezieht sich auf den Vorgang, ein Bild oder eine Dokumentenseite in das Tagged Image File Format (TIFF) zu konvertieren, ein verlustfreies Format, das häufig für Archivierung und Druck verwendet wird. Aspose.Imaging führt diese Konvertierung in einem einzigen API‑Aufruf durch und bewahrt Auflösung und Kompressionseinstellungen. Die Konvertierung behält alle visuellen Details bei, wodurch sie sich für hochwertige Archivspeicherung und nachgelagerte Verarbeitung eignet.

## Warum Aspose.Imaging für die Bildverarbeitung in Java verwenden?
Aspose.Imaging unterstützt **150+** Eingabe‑ und Ausgabeformate, verarbeitet Dateien mit bis zu **5.000 Seiten**, ohne das gesamte Dokument in den Speicher zu laden, und bietet thread‑sichere Operationen. Diese quantifizierten Fähigkeiten machen es zu einer zuverlässigen Wahl für hochdurchsatzfähige Java‑Bildverarbeitungs‑Workloads, insbesondere beim Umgang mit großen Dokumentensammlungen, die eine Batch‑Konvertierung und minimalen Speicherverbrauch erfordern.

## Voraussetzungen

- **Aspose.Imaging für Java Bibliothek** – Version 25.5 oder höher.  
- **Java Development Kit (JDK)** – 8 oder neuer, korrekt auf Ihrem Rechner konfiguriert.  
- **Grundlegende Java‑Kenntnisse** – Sie sollten mit Datei‑I/O und Ausnahmebehandlung vertraut sein.

## Wie richtet man Maven Aspose Imaging ein?
Um Aspose.Imaging in ein Maven‑Projekt einzubinden, fügen Sie die Abhängigkeit in die `pom.xml` des Projekts ein. Maven lädt die Bibliothek und ihre transitiven Abhängigkeiten herunter, sodass die API für Kompilierung und Laufzeit verfügbar ist. Nach dem Hinzufügen des Snippets führen Sie `mvn clean install` aus, um sicherzustellen, dass das Artefakt aufgelöst ist und das Projekt erfolgreich gebaut wird.

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

## Wie richtet man Gradle Aspose Imaging ein?
Für Gradle‑Builds deklarieren Sie die Aspose.Imaging‑Abhängigkeit in der Datei `build.gradle`. Gradle holt die Bibliothek von Maven Central, sodass Sie die API in Ihrem Java‑Code verwenden können. Nach dem Aktualisieren des Skripts aktualisieren Sie das Projekt, um das JAR herunterzuladen und die Abhängigkeiten zu synchronisieren.

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

## Direkter Download
Sie können das neueste JAR auch von [Aspose.Imaging releases](https://releases.aspose.com/imaging/java/) herunterladen.

### Lizenzbeschaffung
- **Kostenlose Testversion** – erhalten Sie eine temporäre Lizenz zur Evaluierung.  
- **Kauf** – erwägen Sie den Kauf einer Voll‑Lizenz für den Produktionseinsatz.

## Initialisierung und Einrichtung
Bevor Sie irgendeine API verwenden, müssen Sie die Bibliothek initialisieren. `License` ist eine Klasse, die verwendet wird, um Ihre Aspose.Imaging‑Lizenzdatei auf die Bibliothek anzuwenden und damit die volle Funktionalität ohne Evaluationsbeschränkungen sicherzustellen.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path/to/your/license.lic");
```

## Wie lädt man DjVu?
DjvuImage ist das oberste Objekt, das eine DjVu‑Datei im Speicher repräsentiert. Um ein DjVu‑Dokument zu lesen, rufen Sie die statische Methode `Image.load()` mit dem Dateipfad auf; diese Methode gibt eine `Image`‑Instanz zurück, die Sie zu `DjvuImage` casten. `Image.load()` ist eine statische Methode, die eine Bilddatei liest und ein `Image`‑Objekt zurückgibt, das den geladenen Inhalt darstellt.

```java
   String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "/Sample.djvu";
   ```

```java
   try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
       // The image is now loaded and ready for further processing.
   }
   ```

### Fehlerbehebung
- Stellen Sie sicher, dass der Dateipfad korrekt und zugänglich ist.  
- Umwickeln Sie den Ladevorgang mit einem try‑catch‑Block, um `IOException` oder `ImageLoadException` zu behandeln.

## Wie exportiert man TIFF?
Der Export einer DjVu‑Seite nach TIFF beinhaltet das Erstellen eines `TiffOptions`‑Objekts, das Kompression, Auflösung und weitere Einstellungen festlegt, gefolgt vom Aufruf der `save()`‑Methode auf der gewünschten Seite. `TiffOptions` ist eine Klasse, die die Konfiguration für die TIFF‑Ausgabe enthält, wie Kompressionstyp und Farbtiefe. Verwenden Sie ein `IntRange`, um die zu konvertierenden Seiten auszuwählen, und iterieren Sie dann, um jede Seite als separate TIFF‑Datei zu speichern.

Erstellen Sie das Ausgabeverzeichnis, richten Sie `TiffOptions` ein, wählen Sie die Seiten mit `IntRange` aus und speichern Sie schließlich jede Seite als TIFF‑Datei.

```java
   String outputDir = "YOUR_OUTPUT_DIRECTORY" + "/ConvertDjvuPagesToTiff_out.tiff";
   ```

```java
   TiffOptions exportOptions = new TiffOptions(TiffExpectedFormat.TiffDeflateBw);
   ```

```java
   IntRange range = new IntRange(0, 2); // Export the first three pages.
   exportOptions.setMultiPageOptions(new DjvuMultiPageOptions(range));
   ```

```java
   try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
       image.save(outputDir, exportOptions);
   }
   ```

### Häufige Fallstricke
- Stellen Sie sicher, dass `outputDir` existiert; andernfalls wirft `save()` eine Ausnahme.  
- Denken Sie daran, dass Seitenindizes **nullbasiert** sind; Seite 1 hat den Index 0.

## Praktische Anwendungen
Der Export von DjVu‑Seiten nach TIFF ist in vielen Szenarien nützlich:

1. **Archivsysteme** – Bewahren Sie gescannte Dokumente in einem universell akzeptierten Format auf.  
2. **Dokumenten‑Review‑Workflows** – Extrahieren Sie nur die Seiten, die annotiert werden müssen.  
3. **Integration mit DMS** – Speisen Sie TIFF‑Bilder in bestehende Dokumenten‑Management‑Pipelines ein, die DjVu nicht verstehen.

## Leistungsüberlegungen
Wenn Sie große DjVu‑Dateien verarbeiten:

- Verwenden Sie **try‑with‑resources**, um Streams automatisch zu schließen und Speicher freizugeben.  
- Verarbeiten Sie Dateien in Stapeln (z. B. 10 Seiten gleichzeitig), um den Heap‑Fußabdruck gering zu halten.  
- Bevorzugen Sie `TiffCompression.CCITT4` für Schwarz‑Weiß‑Scans, um die Dateigröße ohne Qualitätsverlust zu reduzieren.

## Häufig gestellte Fragen
**Q:** Wie installiere ich Aspose.Imaging für Java in meinem Projekt?  
**A:** Verwenden Sie Maven oder Gradle wie oben gezeigt, oder laden Sie direkt von der [Aspose releases page](https://releases.aspose.com/imaging/java/) herunter.

**Q:** Kann ich DjVu‑Bilder in andere Formate als TIFF exportieren?  
**A:** Ja, Aspose.Imaging unterstützt auch PNG, JPEG, BMP und viele weitere Formate.

**Q:** Was soll ich tun, wenn meine Lizenzdatei nicht erkannt wird?  
**A:** Vergewissern Sie sich, dass der Lizenzpfad korrekt ist und dass Sie `License.setLicense()` vor jeglicher anderer API‑Nutzung aufrufen.

**Q:** Wie kann ich sehr große DjVu‑Dateien effizient verarbeiten?  
**A:** Verarbeiten Sie das Dokument in kleineren Seitenbereichen und geben Sie jede `DjvuImage`‑Instanz zeitnah frei, um Speicherbelastungen zu vermeiden.

**Q:** Ist Aspose.Imaging für die kommerzielle Nutzung kostenlos?  
**A:** Eine temporäre Test‑Lizenz ist kostenlos, aber für den Produktionseinsatz ist eine gekaufte Lizenz erforderlich.

## Ressourcen
- **Dokumentation**: [Aspose.Imaging Java API Reference](https://reference.aspose.com/imaging/java/)  
- **Download**: [Aspose.Imaging for Java Releases](https://releases.aspose.com/imaging/java/)  
- **Kauf**: [Buy Aspose.Imaging](https://purchase.aspose.com/buy)  
- **Kostenlose Lizenz**: [Get a Free License](https://releases.aspose.com/imaging/java/)  
- **Temporäre Lizenz**: [Request a Temporary License](https://purchase.aspose.com/temporary-license/)  
- **Support**: [Aspose Community Forum](https://forum.aspose.com/c/imaging/14)

Durch das Beherrschen der obigen Schritte können Sie zuverlässig **how to export TIFF** aus DjVu‑Dateien in jeder Java‑basierten Lösung exportieren. Viel Spaß beim Programmieren!

---

**Zuletzt aktualisiert:** 2026-07-08  
**Getestet mit:** Aspose.Imaging 25.5 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials
- [Mehrseitiges TIFF mit Aspose.Imaging für Java erstellen: Ein vollständiger Leitfaden](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [DjVu nach PDF mit Aspose.Imaging für Java konvertieren – Schritt‑für‑Schritt‑Leitfaden](/imaging/java/image-loading-saving/convert-djvu-to-pdf-aspose-imaging-java/)
- [DJVU nach BMP in Java mit Aspose.Imaging konvertieren: Schritt‑für‑Schritt‑Leitfaden](/imaging/java/format-conversion-export/export-djvu-pages-bmp-aspose-imaging-java/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}