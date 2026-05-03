---
date: 2026-05-03
description: Erfahren Sie, wie Sie mehrseitige TIFF-Dateien in das BMP-Format in Java
  mit Aspose.Imaging konvertieren. Folgen Sie dieser Schritt‑für‑Schritt‑Anleitung,
  um TIFF effizient zu konvertieren.
keywords:
- convert multi page tiff
- how to convert tiff
- Aspose.Imaging Java
- TIFF to BMP conversion
- image processing Java
linktitle: TIFF‑Frames in BMP‑Format extrahieren
second_title: Aspose.Imaging Java Image Processing API
title: Mehrseitiges TIFF in BMP konvertieren mit Aspose.Imaging für Java
url: /de/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Mehrseitiges TIFF in BMP konvertieren mit Aspose.Imaging für Java

Wenn Sie **mehrseitige TIFF**‑Dateien in einzelne BMP‑Bilder konvertieren müssen, während Sie in einer Java‑Umgebung arbeiten, sind Sie hier genau richtig. In diesem Tutorial führen wir Sie Schritt für Schritt durch das Extrahieren jedes TIFF‑Frames und das Speichern als BMP‑Datei mithilfe der leistungsstarken Aspose.Imaging‑Bibliothek für Java. Am Ende verstehen Sie nicht nur *wie man TIFF‑Dateien* programmgesteuert konvertiert, sondern auch, warum dieser Ansatz für die stapelweise Bildverarbeitung zuverlässig ist.

## Schnelle Antworten
- **Welche Bibliothek ist am besten für die TIFF‑zu‑BMP‑Konvertierung?** Aspose.Imaging for Java  
- **Wie viele Codezeilen werden benötigt?** Etwa 30 Zeilen über fünf logische Schritte  
- **Benötige ich eine Lizenz für die Produktion?** Ja, eine kommerzielle Lizenz ist erforderlich (Kostenlose Testversion verfügbar)  
- **Kann dies große mehrseitige TIFFs verarbeiten?** Ja, die API streamt Frames effizient  
- **Welche Java‑Version wird unterstützt?** Java 8 und neuer  

## Was bedeutet „mehrseitiges TIFF konvertieren“?
Das Konvertieren eines mehrseitigen TIFF bedeutet, jede Seite (oder jedes Frame) aus einem einzigen TIFF‑Container zu extrahieren und als eigenständige Bilddatei – hier BMP – zu exportieren. Dies ist nützlich für die Dokumentenarchivierung, die medizinische Bildgebung oder jeden Arbeitsablauf, der Rasterbilder für die Weiterverarbeitung benötigt.

## Warum Aspose.Imaging für Java verwenden?
- **Umfassende Formatunterstützung** – Unterstützt TIFF, BMP, JPEG, PNG und viele weitere.  
- **Keine externen Abhängigkeiten** – Reines Java, keine nativen Bibliotheken.  
- **Hohe Leistung** – Gestreamter Zugriff auf Frames reduziert den Speicherverbrauch.  
- **Umfangreiche API** – Bietet feinkörnige Kontrolle über Pixeldaten, Farbtiefe und Metadaten.

## Voraussetzungen

1. **Java-Entwicklungsumgebung** – JDK 8+ und Ihre bevorzugte IDE.  
2. **Aspose.Imaging für Java** – Laden Sie das neueste JAR von der offiziellen Seite **[hier](https://releases.aspose.com/imaging/java/)** herunter.  
3. **Beispiel‑Mehrseiten‑TIFF** – Legen Sie eine TIFF‑Datei (z. B. `sample.tiff`) in ein bekanntes Verzeichnis, das Ihr Code lesen kann.

## Pakete importieren

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## So konvertieren Sie ein mehrseitiges TIFF in BMP mit Aspose.Imaging

### Schritt 1: Laden des TIFF‑Bildes und Initialisieren des Frame‑Zählers

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // Create an instance of int to keep track of frames in TiffImage
    int frameCounter = 0;
```

### Schritt 2: Durchlaufen der TIFF‑Frames

```java
    // Iterate over the TiffFrames in TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

### Schritt 3: Laden der Pixel des TiffFrames in ein Farb‑Array

```java
        // Load Pixels of TiffFrame into an array of Colors
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

### Schritt 4: BMP‑Optionen erstellen und Bits‑pro‑Pixel festlegen

```java
        // Create an instance of bmpCreateOptions
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

### Schritt 5: BMP‑Bild speichern

```java
            // Set the Source of bmpCreateOptions as FileCreateSource by specifying the location where output will be saved
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // Create a new bmpImage
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // Save the bmpImage with pixels from TiffFrame
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## Häufige Fallstricke & Tipps
- **Speichernutzung:** Bei sehr großen TIFF‑Dateien sollten Sie die Frames einzeln verarbeiten (wie gezeigt), anstatt das gesamte Bild in den Speicher zu laden.  
- **Dateinamen:** Der Aufruf `String.format` erzeugt für jedes Frame einen eindeutigen Dateinamen (`...out0.bmp`, `...out1.bmp` usw.). Passen Sie das Muster an, wenn Sie ein anderes Benennungsschema benötigen.  
- **Bit‑Tiefe:** BMP unterstützt verschiedene Bit‑Tiefen; 24‑Bit (True‑Color) funktioniert in den meisten Fällen. Ändern Sie `setBitsPerPixel`, wenn Sie 8‑Bit‑Graustufen‑Ausgabe benötigen.

## FAQ

### Q1: Was ist Aspose.Imaging für Java?

A1: Aspose.Imaging für Java ist eine Java‑Bibliothek, die umfangreiche Bildverarbeitungsfunktionen bereitstellt und es ermöglicht, mit verschiedenen Bildformaten zu arbeiten sowie Aufgaben wie Konvertierung, Bearbeitung und Manipulation durchzuführen.

### Q2: Kann ich Aspose.Imaging für Java mit verschiedenen Bildformaten verwenden?

A2: Ja, Aspose.Imaging für Java unterstützt eine breite Palette von Bildformaten, darunter TIFF, BMP, JPEG, PNG und viele andere, und ist somit ein vielseitiges Werkzeug für bildbezogene Aufgaben.

### Q3: Wo finde ich die Dokumentation für Aspose.Imaging für Java?

A3: Detaillierte Dokumentation für Aspose.Imaging für Java finden Sie **[hier](https://reference.aspose.com/imaging/java/)**.

### Q4: Gibt es eine kostenlose Testversion für Aspose.Imaging für Java?

A4: Ja, Sie können Aspose.Imaging für Java mit einer kostenlosen Testversion **[hier](https://releases.aspose.com/)** ausprobieren.

### Q5: Wie erhalte ich Support für Aspose.Imaging für Java?

A5: Für Fragen, Probleme oder Support zu Aspose.Imaging für Java können Sie das Support‑Forum **[hier](https://forum.aspose.com/)** besuchen.

## Häufig gestellte Fragen

**Q: Kann ich ein mehrseitiges TIFF mit demselben Ansatz in andere Formate (z. B. PNG) konvertieren?**  
A: Absolut. Ersetzen Sie `BmpOptions` durch die passende Options‑Klasse (z. B. `PngOptions`) und passen Sie die Dateierweiterung im Pfad von `FileCreateSource` an.

**Q: Unterstützt Aspose.Imaging komprimierte TIFFs (LZW, CCITT)?**  
A: Ja, die Bibliothek dekomprimiert unterstützte TIFF‑Kompressionsschemata während der Frame‑Extraktion transparent.

**Q: Ist es möglich, EXIF‑Metadaten beim Konvertieren zu BMP zu erhalten?**  
A: BMP unterstützt keine EXIF‑Metadaten. Wenn Sie Metadaten behalten müssen, sollten Sie in ein Format konvertieren, das dies unterstützt (z. B. PNG) oder die Metadaten nach der Konvertierung manuell kopieren.

**Q: Wie kann ich mehrere TIFF‑Dateien in einem Ordner stapelweise verarbeiten?**  
A: Umwickeln Sie den obigen Code mit einer Schleife, die über `File`‑Objekte in einem Verzeichnis iteriert und für jede Datei `dataDir` sowie den Quelldateinamen aktualisiert.

**Q: Welche Lizenz benötige ich für den kommerziellen Einsatz?**  
A: Für den Produktionseinsatz ist eine kostenpflichtige Aspose.Imaging‑Lizenz für Java erforderlich. Eine temporäre Testlizenz kann während der Entwicklung verwendet werden.

---

**Zuletzt aktualisiert:** 2026-05-03  
**Getestet mit:** Aspose.Imaging for Java 24.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}