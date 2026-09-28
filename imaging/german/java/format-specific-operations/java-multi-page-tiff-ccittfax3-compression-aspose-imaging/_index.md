---
date: '2026-09-28'
description: Erfahren Sie, wie Sie ccittfax3 compression java einsetzen, um mehrseitige
  TIFF‑Dateien mit Aspose.Imaging zu erstellen. Scannen, archivieren und die Dateigröße
  für Dokumenten‑Workflows effizient reduzieren.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Entdecken Sie Schritt für Schritt, wie Sie ccittfax3 compression java
  mit Aspose.Imaging nutzen, um effiziente mehrseitige TIFF‑Dateien für das Scannen
  und Archivieren zu erstellen.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: Wie man ein mehrseitiges TIFF mit ccittfax3 compression java erstellt
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: Wie man ein mehrseitiges TIFF mit ccittfax3 compression java erstellt
url: /de/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Meisterung der Erstellung von mehrseitigen TIFFs mit ccittfax3-Kompression in Java unter Verwendung von Aspose.Imaging

## Einleitung

Wenn Sie große Mengen gescannter Dokumente archivieren müssen und dabei die Dateigröße gering halten wollen, ist **ccittfax3 compression java** die bevorzugte Lösung. Dieses Tutorial zeigt Ihnen, wie Sie mehrseitige TIFF‑Dateien mit CCITTFAX3‑Kompression in Java unter Verwendung von Aspose.Imaging erzeugen. Sie erfahren, warum diese Kompression für monochrome Scans so gut funktioniert, wie Sie die Bibliothek konfigurieren und jede Seite als Frame hinzufügen.

**Was Sie lernen werden**
- Wie man Aspose.Imaging zu einem Java‑Projekt hinzufügt.
- Wie man `TiffOptions` für CCITTFAX3‑Kompression konfiguriert.
- Wie man ein `TiffImage` erstellt, Quellbilder skaliert und sie als Frames hinzufügt.
- Wie man das endgültige mehrseitige TIFF effizient speichert.

Lassen Sie uns die vollständige Implementierung durchgehen.

## Schnelle Antworten
- **Was ist der Hauptvorteil der CCITTFAX3‑Kompression?** Bis zu 80 % Reduzierung der Dateigröße bei Schwarz‑weiß‑Scans.  
- **Welche Bibliothek bietet integrierte Unterstützung?** Aspose.Imaging für Java, Version 25.5+.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testlizenz funktioniert für alle Funktionen; für die Produktion ist eine kostenpflichtige Lizenz erforderlich.  
- **Kann ich Hunderte von Seiten verarbeiten?** Ja – Aspose.Imaging streamt Seiten, sodass der Speicherverbrauch gering bleibt.  
- **Ist der Code mit Java 11 und höher kompatibel?** Absolut; die API zielt auf Java 8+ ab.

## Was ist ccittfax3 compression java?
`CCITTFAX3` ist ein verlustfreier, monochromer Kompressionsalgorithmus, der für Fax‑ und gescannte Dokumentenbilder entwickelt wurde. Er kodiert jedes Pixel als einzelnes Bit und liefert hochwertige Ausgaben, während die Dateigröße dramatisch schrumpft – oft um 70‑80 % im Vergleich zu unkomprimierten TIFFs. Das macht ihn ideal für die Archivierung von Schwarz‑weiß‑Dokumenten, bei denen die Treue erhalten bleiben muss.

## Warum Aspose.Imaging für diese Aufgabe verwenden?
Aspose.Imaging unterstützt **100+** Eingabe‑ und Ausgabeformate, darunter PDF, PNG, JPEG und TIFF. Seine Streaming‑Architektur kann **mehrhundertseitige** TIFF‑Dateien verarbeiten, ohne das gesamte Dokument in den Speicher zu laden, was es ideal für groß angelegte Archivierungsprojekte macht.

## Voraussetzungen

- **Java Development Kit (JDK)** 8 oder neuer installiert.
- **IDE** wie IntelliJ IDEA oder Eclipse.
- **Maven** oder **Gradle** für das Abhängigkeitsmanagement.
- Grundlegende Java‑Kenntnisse (Klassen, Objekte, Sammlungen).

## Einrichtung von Aspose.Imaging für Java

Fügen Sie die Bibliothek zu Ihrer Build‑Datei hinzu.

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```  

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

### Direkter Download

You can also download the latest JAR from [Aspose.Imaging für Java Releases](https://releases.aspose.com/imaging/java/).

### Lizenzbeschaffung

A free trial license is available from [Aspose Free Trial Seite](https://releases.aspose.com/imaging/java/). For production use, purchase a permanent license or request a temporary one at [Aspose Kauf](https://purchase.aspose.com/temporary-license/).

For detailed API usage, see the Aspose.Imaging for Java [Dokumentation](https://reference.aspose.com/imaging/java/).

### Grundlegende Initialisierung

Nachdem Sie die Abhängigkeit hinzugefügt haben, initialisieren Sie die Bibliothek wie unten gezeigt.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## Wie konfiguriere ich ccittfax3 compression java für ein mehrseitiges TIFF?

`TiffOptions` ist eine Klasse, die das Ausgabeformat und die Kompressionseinstellungen für eine TIFF‑Datei definiert. Laden Sie das `TiffOptions`‑Objekt mit dem Enum `CCITTGroup3FaxCompression` und setzen Sie anschließend die Ausgabedateiquelle. Diese zweistufige Konfiguration bereitet den Writer für monochrome Kompression vor und stellt sicher, dass jede später hinzugefügte Seite mit dem CCITTFAX3‑Algorithmus kodiert wird, was zu einer erheblichen Größenreduktion bei gleichzeitigem Erhalt der Bildqualität führt.

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## Wie erstelle ich eine TiffImage‑Instanz in Java?

`TiffImage` repräsentiert ein mehrseitiges TIFF‑Dokument im Speicher und bietet Methoden zur Manipulation seiner Frames. Definieren Sie zunächst die Breite und Höhe, die alle Seiten gemeinsam haben. Instanziieren Sie dann `TiffImage` mit den zuvor erstellten `TiffOptions`. Das `TiffImage`‑Objekt fungiert als Container für die einzelnen Frames und ermöglicht das Hinzufügen, Entfernen oder Neuordnen von Seiten, bevor die endgültige Datei gespeichert wird.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## Wie lade und skaliere ich Quellbilder aus einem Ordner?

Filtern Sie das Zielverzeichnis nach JPEG‑Dateien, lesen Sie jedes Bild ein und skalieren Sie es, um die TIFF‑Leinwand zu füllen. Das Skalieren vor dem Hinzufügen von Frames reduziert den Speicherverbrauch und beschleunigt den Speichervorgang. Durch die Konvertierung jedes Quellbildes in die erforderlichen Abmessungen und das Pixel‑Format gewährleisten Sie ein konsistentes Seitenlayout und vermeiden Laufzeitfehler, wenn die Frames dem TIFF‑Dokument hinzugefügt werden.

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## Wie füge ich jedes Bild als Frame zum mehrseitigen TIFF hinzu?

`TiffFrame` ist ein Objekt, das ein einzelnes Seitenbild und die zugehörigen Metadaten innerhalb eines TIFFs enthält. Durchlaufen Sie die skalierten Bilder, erstellen Sie ein neues `TiffFrame` und hängen Sie es an das `TiffImage` an. Jeder Frame wird zu einer separaten Seite im endgültigen Dokument, und die Bibliothek übernimmt automatisch die erforderlichen Metadaten‑Updates, wie Seitenzahl und Offsets, um eine gültige mehrseitige TIFF‑Struktur sicherzustellen.

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## Wie speichere ich die endgültige mehrseitige TIFF‑Datei?

Rufen Sie die `save`‑Methode auf der `TiffImage`‑Instanz auf und übergeben Sie den gewünschten Ausgabepfad. Die Bibliothek schreibt automatisch alle Frames mit CCITTFAX3‑Kompression, streamt die Daten effizient auf die Festplatte und schließt alle zugrunde liegenden Ressourcen. Nach Abschluss des Speicher‑Vorgangs enthält die resultierende Datei alle Seiten mit der angegebenen Kompression und ist bereit für die Verteilung oder Archivierung.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## Praktische Anwendungen

- **Dokumentenarchivierung:** Gescannte Verträge, Rechnungen oder Rechtsunterlagen mit minimalem Speicheraufwand speichern.  
- **Medizinische Bildgebung:** Radiologie‑Scans komprimieren und dabei diagnostische Details erhalten.  
- **Druckproduktion:** Mehrseitige Druckaufträge erzeugen, die Drucker direkt verarbeiten können.

## Leistungsüberlegungen

- Verwenden Sie `ResizeOptions`, die das Seitenverhältnis beibehalten, um Verzerrungen zu vermeiden.  
- Schließen Sie jedes `Image`‑Objekt nach dem Hinzufügen seines Frames, um nativen Speicher freizugeben.  
- Bei sehr großen Stapeln verarbeiten Sie Dateien in parallelen Streams und schreiben jedes TIFF‑Segment asynchron.

## Häufige Fallstricke und Fehlersuche

- **Falsches Pixel‑Format:** CCITTFAX3 funktioniert nur mit 1‑Bit (Schwarz‑weiß) Bildern. Konvertieren Sie Farbbilder vor dem Skalieren in Graustufen.  
- **Speicherlecks:** Rufen Sie stets `dispose()` für temporäre `Image`‑Objekte auf; sonst bleiben native Puffer zugewiesen.  
- **Dateigröße nicht reduziert:** Stellen Sie sicher, dass die Kompressionseigenschaft von `TiffOptions` gesetzt ist; andernfalls wird die Standardeinstellung (keine Kompression) verwendet.

## Häufig gestellte Fragen

**Q: Kann ich diesen Ansatz mit Farbbildern verwenden?**  
A: CCITTFAX3 ist auf monochrome Daten beschränkt; für Farbe verwenden Sie stattdessen JPEG‑ oder LZW‑Kompression.

**Q: Unterstützt Aspose.Imaging Streaming für riesige TIFFs?**  
A: Ja – die Bibliothek schreibt jeden Frame direkt in den Ausgabestream, wodurch der Speicherverbrauch selbst bei tausenden Seiten gering bleibt.

**Q: Wie wende ich programmgesteuert eine temporäre Lizenz an?**  
A: Laden Sie die `.lic`‑Datei mit `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.

**Q: Gibt es eine Möglichkeit, das TIFF vor dem Speichern vorzusehen?**  
A: Sie können jeden `TiffFrame` in ein `BufferedImage` rendern und in einer Swing‑Komponente anzeigen.

**Q: Welche Java‑Versionen werden offiziell unterstützt?**  
A: Aspose.Imaging unterstützt Java 8 bis Java 21, einschließlich LTS‑Versionen.

## Fazit

Sie haben nun einen vollständigen, produktionsbereiten Workflow zur Erstellung mehrseitiger TIFF‑Dateien mit **ccittfax3 compression java** unter Verwendung von Aspose.Imaging. Durch Befolgen der obigen Schritte können Sie massive Dokumentensammlungen effizient archivieren, dabei die Speicherkosten niedrig und die Bildqualität hoch halten. Erkunden Sie weitere Aspose.Imaging‑Funktionen – wie OCR, Metadaten‑Verarbeitung und Formatkonvertierung – um Ihre Dokumenten‑Verarbeitungspipeline weiter zu verbessern.

---

**Zuletzt aktualisiert:** 2026-09-28  
**Getestet mit:** Aspose.Imaging 25.5 für Java  
**Autor:** Aspose

## Verwandte Tutorials

- [Wie man ein mehrseitiges TIFF mit Aspose.Imaging für Java erstellt – Ein vollständiger Leitfaden](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Wie man die Bilddateigröße mit LZW‑Kompression in Java reduziert](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Mehrseitige TIFF‑Frames mit Aspose.Imaging für Java aufteilen](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}