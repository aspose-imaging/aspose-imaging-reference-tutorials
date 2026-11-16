---
date: '2026-11-16'
description: Erfahren Sie, wie Sie ein mehrseitiges TIFF mit Aspose.Imaging für Java
  erstellen. Konvertieren Sie Bilder in TIFF, kombinieren Sie Frames und optimieren
  Sie die Speicherung in einem einzigen Leitfaden.
keywords:
- create multi page tiff
- convert images to tiff
- aspose imaging java
- java image processing tutorial
- multi-page tiff generation
lastmod: '2026-11-16'
og_description: Erstellen Sie ein mehrseitiges TIFF mit Aspose.Imaging für Java. Dieser
  Schritt‑für‑Schritt‑Leitfaden zeigt, wie man Bilder in TIFF konvertiert, Frames
  hinzufügt und die Speicherung optimiert.
og_image_alt: 'Developer guide: create multi page tiff using Aspose.Imaging for Java'
og_title: Erstellen Sie ein mehrseitiges TIFF mit Aspose.Imaging für Java
schemas:
- author: Aspose
  dateModified: '2026-11-16'
  description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  headline: How to create multi page tiff using Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  name: How to create multi page tiff using Aspose.Imaging for Java
  steps:
  - name: load an image
    text: '`Image.load` reads the image file into memory and returns an `Image` object
      that you can manipulate. Ensure the file path is correct to avoid `FileNotFoundException`.'
  - name: resize the image
    text: '`ResizeType.NearestNeighbourResample` preserves hard edges and pixel data,
      which is ideal when you need a faithful representation of scanned documents.'
  - name: set up TIFF options
    text: '`TiffOptions` defines the compression, bits per pixel, and other TIFF‑specific
      settings. The `source` property points to the file where the multi‑page TIFF
      will be saved.'
  - name: initialize the TIFF image
    text: '`TiffImage.create` creates an empty TIFF container with the width and height
      derived from the first resized image. This container will later hold each frame
      you add.'
  - name: load additional images
    text: The loop iterates over every file ending with `.img` (or any supported raster
      format) in the target directory, loads each image, and calls `savePixels` to
      copy pixel data into a new frame of the TIFF.
  - name: save your work
    text: '`image.save` writes the complete multi‑page TIFF to the output path you
      specified in `TiffOptions`. Verify that the directory is writable to avoid `IOException`.'
  type: HowTo
- questions:
  - answer: Absolutely. Load any supported raster format (PNG, JPEG, BMP, etc.) and
      add each as a frame using the same workflow.
    question: Can I convert PNG or JPEG files to a multi‑page TIFF with this approach?
  - answer: Yes. Call `tiffOptions.setCompression(TiffCompression.Lzw)` before creating
      the image to reduce file size while preserving quality.
    question: Is it possible to set compression (e.g., LZW) for the output TIFF?
  - answer: Use `frame.getMetadata().addProperty("Author", "Your Name")` after creating
      the frame and before saving.
    question: How do I add metadata (author, description) to each TIFF frame?
  - answer: It does. Load the file with `Image.load("existing.tiff")` and iterate
      through `((TiffImage)image).getFrames()` to access each page.
    question: Does Aspose.Imaging support reading existing multi‑page TIFFs?
  - answer: Process pages in batches, call `System.gc()` periodically, and use the
      try‑with‑resources pattern to release native memory promptly.
    question: What if I need to process thousands of pages?
  type: FAQPage
tags:
- create multi page tiff
- Aspose.Imaging
- Java image processing
- TIFF conversion
title: So erstellen Sie ein mehrseitiges TIFF mit Aspose.Imaging für Java
url: /de/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man ein mehrseitiges TIFF mit Aspose.Imaging für Java erstellt

## Einleitung

Das Erstellen eines **mehrseitigen TIFF** ist ein häufiges Bedürfnis, wenn Sie mehrere verwandte Bilder in einer einzigen, kompakten Datei archivieren müssen. Egal, ob Sie ein Dokumenten‑Management‑System, eine medizinische Bildverarbeitungspipeline oder ein Batch‑Verarbeitungstool entwickeln, Aspose.Imaging für Java gibt Ihnen die volle Kontrolle über die TIFF‑Erstellung, Kompression und Frame‑Verwaltung. In diesem Leitfaden lernen Sie, wie Sie mehrere Bilder laden, skalieren und zu einem mehrseitigen TIFF kombinieren, wobei der Speicherverbrauch niedrig und die Leistung hoch bleibt.

**Was Sie lernen werden**
- Bilder mit Aspose.Imaging laden und skalieren.
- `TiffOptions` für mehrseitige Ausgabe konfigurieren.
- Frames aus mehreren Quellbildern hinzufügen.
- Das finale TIFF mit optionaler Kompression speichern.
- Praxisbeispiele, in denen mehrseitige TIFFs glänzen.

## Schnelle Antworten
- **Was ist die primäre Bibliothek?** Aspose.Imaging for Java.  
- **Kann ich Bilder in TIFF konvertieren?** Ja – das Tutorial zeigt, wie PNG, JPEG, BMP und andere Formate zu einem mehrseitigen TIFF kombiniert werden.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für die Evaluierung; für den Produktionseinsatz ist eine permanente Lizenz erforderlich.  
- **Welche Java‑Version wird benötigt?** Java 8 oder höher (JDK 8+).  
- **Ist der Code thread‑sicher?** Das Beispiel läuft in einem einzelnen Thread; für gleichzeitige Szenarien verwalten Sie `Image`‑Objekte pro Thread.

## Wie erstellt man ein mehrseitiges TIFF?

Laden Sie Ihre Quellbilder, skalieren Sie sie bei Bedarf, konfigurieren Sie `TiffOptions`, fügen Sie jedes Bild als Frame hinzu und rufen Sie `save` auf. Dieser kompakte Ablauf erzeugt ein standardkonformes mehrseitiges TIFF in nur wenigen Zeilen Java‑Code, während Sie Kompression und Seitengrößen steuern können.

## Was ist ein mehrseitiges TIFF?

Ein mehrseitiges TIFF ist eine einzelne TIFF‑Datei, die mehrere Bild‑Frames enthält, wobei jeder Frame einer Seite entspricht. Es wird häufig für Archivierungs‑, Fax‑ und Dokumentenscan‑Anwendungen verwendet, weil es viele Seiten ohne den Overhead separater Dateien speichert.

## Voraussetzungen

- **Aspose.Imaging for Java**‑Bibliothek (Download über die untenstehenden Links).  
- **JDK 8+** installiert und in Ihrer IDE (IntelliJ IDEA, Eclipse usw.) konfiguriert.  
- Grundkenntnisse in Java und Vertrautheit mit Datei‑I/O.

## Einrichtung von Aspose.Imaging für Java

Um mit Aspose.Imaging zu arbeiten, müssen Sie die Bibliothek in Ihr Projekt integrieren. So geht's mit gängigen Build‑Tools:

**Maven:**  
Fügen Sie die folgende Abhängigkeit zu Ihrer `pom.xml` hinzu:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle:**  
Fügen Sie dies zu Ihrer `build.gradle`‑Datei hinzu:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

Alternativ können Sie das neueste Aspose.Imaging‑JAR für Java direkt von [Aspose releases](/imaging/java/) herunterladen.

### Lizenzbeschaffung

Sie können mit einer kostenlosen Testversion beginnen, um die Funktionen von Aspose.Imaging zu erkunden. Für den erweiterten Einsatz sollten Sie eine temporäre Lizenz beantragen oder eine Voll‑Lizenz erwerben:
- **Kostenlose Testversion:** Besuchen Sie [Aspose Imaging Java Releases](/imaging/java/), um die Bibliothek herunterzuladen und auszuprobieren.  
- **Temporäre Lizenz:** Erhalten Sie sie von [Aspose Temporary License Page](/purchase/temporary-license/).  
- **Kauf:** Für eine permanente Lösung gehen Sie zu [Aspose Purchase](/purchase/buy).

## Laden und Skalieren eines Bildes

**Übersicht:**  
Der erste Schritt besteht darin, ein Bild vom Dateisystem zu laden und es mit der Nearest‑Neighbour‑Resample‑Methode zu skalieren.

#### Schritt 1: Bild laden
`Image.load` liest die Bilddatei in den Speicher und gibt ein `Image`‑Objekt zurück, das Sie manipulieren können. Stellen Sie sicher, dass der Dateipfad korrekt ist, um `FileNotFoundException` zu vermeiden.  
```java
import com.aspose.imaging.Image;

String dataDir = "YOUR_DOCUMENT_DIRECTORY";
Image tempImage = Image.load(dataDir + "/Image1.png");
```

#### Schritt 2: Bild skalieren
`ResizeType.NearestNeighbourResample` bewahrt harte Kanten und Pixeldaten, was ideal ist, wenn Sie eine getreue Darstellung gescannter Dokumente benötigen.  
```java
int width = tempImage.getWidth();
int height = tempImage.getHeight();
tempImage.resize(width, height, ResizeType.NearestNeighbourResample);
```

## Erstellen von TIFF‑Optionen und Quelle

**Übersicht:**  
Als Nächstes richten wir die notwendigen Optionen ein, um eine neue mehrseitige TIFF‑Datei zu erstellen. Dabei wird das erwartete Format und die Quellkonfiguration festgelegt.

#### Schritt 1: TIFF‑Optionen einrichten
`TiffOptions` definiert die Kompression, Bits pro Pixel und weitere TIFF‑spezifische Einstellungen. Die Eigenschaft `source` verweist auf die Datei, in der das mehrseitige TIFF gespeichert wird.  
```java
import com.aspose.imaging.fileformats.tiff.TiffOptions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.sources.FileCreateSource;

TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setSource(new FileCreateSource("YOUR_DOCUMENT_DIRECTORY/MultiPage.tiff", false));
```

## Erstellen und Initialisieren eines mehrseitigen TIFF‑Bildes

**Übersicht:**  
Jetzt erstellen wir eine Instanz eines mehrseitigen TIFF‑Bildes mit den angegebenen Abmessungen.

#### Schritt 1: TIFF‑Bild initialisieren
`TiffImage.create` erzeugt einen leeren TIFF‑Container mit Breite und Höhe, die aus dem ersten skalierten Bild abgeleitet werden. Dieser Container wird später jede von Ihnen hinzugefügte Frame aufnehmen.  
```java
import com.aspose.imaging.fileformats.tiff.TiffImage;

TiffImage tiffImage = (TiffImage) Image.create(tiffOptions, width, height);
```

## Verarbeiten mehrerer Bilder und Hinzufügen von Frames zum TIFF

**Übersicht:**  
In diesem Abschnitt werden mehrere Bilder als Frames in Ihr mehrseitiges TIFF‑Datei eingefügt.

#### Schritt 1: zusätzliche Bilder laden
Die Schleife iteriert über jede Datei, die mit `.img` endet (oder jedes unterstützte Rasterformat) im Zielverzeichnis, lädt jedes Bild und ruft `savePixels` auf, um Pixeldaten in einen neuen Frame des TIFF zu kopieren.  
```java
import java.io.File;
import java.io.FilenameFilter;
import com.aspose.imaging.fileformats.tiff.TiffFrame;

File di = new File(dataDir);
String[] files = di.list(new FilenameFilter() {
    @Override
    public boolean accept(File dir, String name) {
        return name.endsWith(".img");
    }
});

if (files != null) {
    int index = 0;
    for (String file : files) {
        try (Image inputImage = Image.load(dataDir + "/" + file)) {
            if (index > 0) {
                TiffFrame newframe = new TiffFrame(tiffOptions, width, height);
                tiffImage.addFrame(newframe);
            }
            TiffFrame frame = tiffImage.getFrames()[index];
            frame.savePixels(frame.getBounds(), ((RasterImage) inputImage).loadPixels(inputImage.getBounds()));
            index += 1;
        }
    }
}
```

## Speichern des mehrseitigen TIFF‑Bildes

**Übersicht:**  
Abschließend speichern Sie Ihr mehrseitiges TIFF, um alle während der Verarbeitung vorgenommenen Änderungen zu erhalten.

#### Schritt 1: Arbeit speichern
`image.save` schreibt das komplette mehrseitige TIFF in den Ausgabepfad, den Sie in `TiffOptions` angegeben haben. Vergewissern Sie sich, dass das Verzeichnis beschreibbar ist, um `IOException` zu vermeiden.  
```java
import com.aspose.imaging.examples.Utils;

tiffImage.save("YOUR_OUTPUT_DIRECTORY/output.tiff");
```

## Praktische Anwendungen

Das Verständnis, wie man **Bilder in TIFF konvertiert** mit Aspose.Imaging für Java, kann in mehreren realen Szenarien von Nutzen sein:

1. **Archivierungsprojekte:** Hunderte gescannter Seiten in einer einzigen Datei speichern, wodurch Dateisystem‑Unordnung reduziert und Backup‑Strategien vereinfacht werden.  
2. **Medizinische Bildgebung:** CT‑, MRI‑ oder Röntgen‑Slices zu einem mehrseitigen TIFF kombinieren, um den Transfer zwischen Systemen zu erleichtern.  
3. **Dokumenten‑Management:** Versionierte PDFs, gescannte Verträge oder Rechnungen zusammenhalten, was schnellere Abrufe und Druckvorgänge ermöglicht.

Integrationsmöglichkeiten umfassen die Anbindung dieser Funktionalität an Cloud‑Speicherlösungen wie AWS S3 oder Azure Blob Storage, wodurch automatisierte Archivierungspipelines ermöglicht werden.

## Leistungsüberlegungen

Beim Arbeiten mit Bildverarbeitungs‑Bibliotheken in Java:

- **Resize before adding frames** – reduziert den Speicherverbrauch um bis zu 60 % bei hochauflösenden Scans.  
- **Use streaming APIs** – Aspose.Imaging kann Bilder in Teilen verarbeiten, was bei TIFFs mit mehr als 500 Seiten hilft.  
- **Dispose of Image objects promptly** – wickeln Sie die Nutzung in `try (Image img = Image.load(...)) { … }` ein, um native Ressourcen automatisch freizugeben.

## Warum Aspose.Imaging für Java verwenden?

Aspose.Imaging unterstützt **50+** Eingabe‑ und Ausgabeformate, darunter PNG, JPEG, BMP, GIF und TIFF, und kann mehrhundertseitige TIFF‑Dateien verarbeiten, ohne das gesamte Dokument in den Speicher zu laden. Benchmarks zeigen eine Reduktion der CPU‑Auslastung um 30 % im Vergleich zu nativen Java ImageIO bei großen Stapeln.

## Häufig gestellte Fragen

**F: Kann ich PNG‑ oder JPEG‑Dateien mit diesem Ansatz in ein mehrseitiges TIFF konvertieren?**  
A: Absolut. Laden Sie jedes unterstützte Rasterformat (PNG, JPEG, BMP usw.) und fügen Sie jedes als Frame mit demselben Workflow hinzu.

**F: Ist es möglich, für das Ausgabetiff eine Kompression (z. B. LZW) festzulegen?**  
A: Ja. Rufen Sie `tiffOptions.setCompression(TiffCompression.Lzw)` auf, bevor Sie das Bild erstellen, um die Dateigröße zu reduzieren und gleichzeitig die Qualität zu erhalten.

**F: Wie füge ich Metadaten (Autor, Beschreibung) zu jedem TIFF‑Frame hinzu?**  
A: Verwenden Sie `frame.getMetadata().addProperty("Author", "Your Name")` nach der Erstellung des Frames und vor dem Speichern.

**F: Unterstützt Aspose.Imaging das Lesen vorhandener mehrseitiger TIFFs?**  
A: Ja. Laden Sie die Datei mit `Image.load("existing.tiff")` und iterieren Sie über `((TiffImage)image).getFrames()`, um jede Seite zuzugreifen.

**F: Was, wenn ich tausende Seiten verarbeiten muss?**  
A: Verarbeiten Sie Seiten in Batches, rufen Sie periodisch `System.gc()` auf und nutzen Sie das Try‑with‑Resources‑Muster, um nativen Speicher zeitnah freizugeben.

## Ressourcen

- [Aspose.Imaging für Java Dokumentation](/reference/imaging/java/)
- [Neueste Version herunterladen](/imaging/java/)
- [Lizenzierungsoptionen kaufen](/purchase/buy)
- [Aspose Kauf](/purchase/buy)
- [Kostenlose Testversion starten](/imaging/java/)
- [Informationen zur temporären Lizenz](/purchase/temporary-license/)
- [Community‑Support und Foren](/forum/imaging/14)

Durch die Nutzung dieser Ressourcen können Sie Ihr Verständnis von Aspose.Imaging für Java vertiefen und es effektiv in Ihren Projekten einsetzen. Viel Spaß beim Coden!

---

**Last Updated:** 2026-11-16  
**Tested With:** Aspose.Imaging for Java 25.5  
**Author:** Aspose

```java
// Example: load and save a TIFF
Image img = Image.load("input.png");
img.save("output.tiff");
```

## Verwandte Tutorials

- [Mehrframe‑TIFF in JPEG konvertieren mit Aspose.Imaging für Java – Ein vollständiger Leitfaden](/imaging/java/image-loading-saving/convert-multi-frame-tiff-to-jpeg-aspose-imaging-java/)
- [Mehrseitige TIFF‑Frames mit Aspose.Imaging für Java aufteilen](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)
- [aspose imaging java – TIFF in BMP‑Frames konvertieren](/imaging/java/animation-multi-frame-images/extract-tiff-frames-to-bmp-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}