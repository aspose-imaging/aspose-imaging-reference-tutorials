---
date: 2026-01-12
description: Erfahren Sie, wie Sie den Kontrast in DICOM‑Bildern anpassen – eine Schritt‑für‑Schritt‑Anleitung,
  wie Sie den Kontrast mit Aspose.Imaging für Java einstellen und DICOM in BMP konvertieren.
linktitle: DICOM Image Contrast Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: Wie man den Kontrast in DICOM‑Bildern mit Aspose.Imaging für Java anpasst
url: /de/java/image-processing-and-enhancement/dicom-image-contrast-adjustment/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Wie man den Kontrast in DICOM‑Bildern mit Aspose.Imaging für Java anpasst

In der modernen medizinischen Bildgebung kann **wie man den Kontrast anpasst** den Unterschied zwischen einer klaren Diagnose und einem übersehenen Detail ausmachen. Dieses Tutorial führt Sie Schritt für Schritt durch das Anpassen des Kontrasts in DICOM‑Dateien mit Aspose.Imaging für Java und zeigt, wie Sie diese DICOM‑Bilder nach der Anpassung in BMP konvertieren, um sie leicht anzusehen oder weiterzuverarbeiten. Am Ende haben Sie einen einsatzbereiten Code‑Snippet, den Sie in jedes Java‑Projekt einbinden können.

## Schnellantworten
- **Was bewirkt die Kontrastanpassung?** Sie erweitert den Wertebereich zwischen dunklen und hellen Pixeln, sodass Strukturen besser hervortreten.
- **Welche Bibliothek wird benötigt?** Aspose.Imaging für Java.
- **Kann ich als BMP ausgeben?** Ja – Sie können DICOM nach der Kontrastanpassung in BMP konvertieren.
- **Benötige ich eine Lizenz für die Produktion?** Für den Einsatz außerhalb der Evaluation ist eine kommerzielle Lizenz erforderlich.
- **Welche Java‑Version wird unterstützt?** Java 8 und neuer.

## Was ist Kontrastanpassung und warum ist sie wichtig?
Die Kontrastanpassung verbessert die visuelle Unterscheidung zwischen anatomischen Merkmalen und hilft Radiologen, Anomalien schneller zu erkennen. In einem DICOM‑Workflow stellt das Anpassen des Kontrasts vor der Konvertierung sicher, dass die BMP‑Ausgabe die für Berichte oder Archivierung erforderliche diagnostische Qualität behält.

## Voraussetzungen

Bevor Sie in den Code eintauchen, vergewissern Sie sich, dass Sie Folgendes haben:

1. **Aspose.Imaging für Java** – laden Sie es von der offiziellen Seite [hier](https://releases.aspose.com/imaging/java/) herunter.  
2. **Java‑Entwicklungsumgebung** – JDK 8+ und Ihre bevorzugte IDE (IntelliJ, Eclipse, VS Code usw.).  
3. **Ein DICOM‑Bild** – jede .dcm‑Datei, die Sie verbessern möchten; Beispiel‑Dateien sind online verfügbar oder Sie verwenden Ihre eigenen klinischen Daten.

## Pakete importieren

Diese Importe geben Ihnen Zugriff auf die DICOM‑Verarbeitung und BMP‑Speicherfunktionen.

```java
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
```

## Wie man den Kontrast in DICOM‑Bildern anpasst

Im Folgenden finden Sie den vollständigen, schrittweisen Workflow. Jeder Schritt wird in einfacher Sprache erklärt, sodass Sie auch dann folgen können, wenn Sie neu bei Aspose.Imaging sind.

### Schritt 1: Dateipfade angeben

Legen Sie den Eingabe‑DICOM‑Ort und den gewünschten Ausgabe‑BMP‑Pfad fest. Ersetzen Sie den Platzhalter durch das tatsächliche Verzeichnis auf Ihrem Rechner.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingContrast_out.bmp";
```

### Schritt 2: DICOM‑Bild laden

Wir öffnen die DICOM‑Datei mit einem `FileInputStream`. Der `try‑with‑resources`‑Block sorgt dafür, dass der Stream automatisch geschlossen wird.

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

### Schritt 3: Kontrast anpassen

Innerhalb des inneren `try`‑Blocks rufen Sie `adjustContrast` auf. Der Wert kann von **‑100** (Verminderung) bis **+100** (Erhöhung) reichen. In diesem Beispiel erhöhen wir den Kontrast um 50 Einheiten.

```java
image.adjustContrast(50);
```

### Schritt 4: DICOM in BMP konvertieren und Bild speichern

Nach der Kontrastanpassung erstellen wir eine `BmpOptions`‑Instanz und speichern das Ergebnis als BMP‑Datei. Dieser Schritt **konvertiert DICOM in BMP** und liefert Ihnen ein weit verbreitetes Rasterformat.

```java
image.save(outputFile, new BmpOptions());
```

## Häufige Probleme & Tipps

- **Ungültige DICOM‑Datei** – Stellen Sie sicher, dass die .dcm‑Datei nicht mit einer nicht unterstützten Transfer‑Syntax komprimiert ist. Aspose.Imaging unterstützt die meisten gängigen DICOM‑Kodierungen.
- **Kontrastwert außerhalb des Bereichs** – Werte jenseits von ±100 werden abgeschnitten; wählen Sie eine Zahl, die zum Histogramm des Bildes passt.
- **Speichernutzung** – Große DICOM‑Serien können viel RAM verbrauchen. Verarbeiten Sie bei Bedarf einen Slice nach dem anderen, um `OutOfMemoryError` zu vermeiden.

## Fazit

Sie haben nun gelernt, **wie man den Kontrast** in DICOM‑Bildern mit Aspose.Imaging für Java anpasst und **wie man DICOM in BMP** für nachgelagerte Aufgaben konvertiert. Dieser Workflow ist schnell, zuverlässig und lässt sich in größere medizinische Bild‑Pipelines integrieren, egal ob Sie einen PACS‑Viewer, ein Forschungstool oder ein automatisiertes Berichtssystem bauen.

Aspose.Imaging für Java abstrahiert die Low‑Level‑DICOM‑Verarbeitung, sodass Sie sich auf den klinischen Mehrwert Ihrer Bilder konzentrieren können.

## Häufig gestellte Fragen

**F: Was ist DICOM und warum ist es der Standard in der medizinischen Bildgebung?**  
A: DICOM (Digital Imaging and Communications in Medicine) ist das universelle Format zum Speichern, Übertragen und Teilen medizinischer Bilder und sorgt für Interoperabilität zwischen Geräten und Institutionen.

**F: Kann ich gleichzeitig die Helligkeit zusammen mit dem Kontrast anpassen?**  
A: Ja, die Methode `adjustBrightness(int value)` funktioniert ähnlich und kann vor dem Speichern verkettet werden.

**F: Unterstützt Aspose.Imaging weitere Ausgabeformate neben BMP?**  
A: Absolut – Sie können zu PNG, JPEG, TIFF und vielen anderen Formaten exportieren, indem Sie die entsprechende `*Options`‑Klasse verwenden.

**F: Ist für den Produktionseinsatz eine kommerzielle Lizenz erforderlich?**  
A: Ja. Sie können eine Lizenz [hier](https://purchase.aspose.com/buy) erwerben oder eine temporäre Evaluationslizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

**F: Wo finde ich weitere Hilfe und Beispiele?**  
A: Das Aspose.Imaging‑Forum für Java bietet umfangreiche Dokumentation und Beispielcode: [Aspose.Imaging for Java forum](https://forum.aspose.com/).

---

**Zuletzt aktualisiert:** 2026-01-12  
**Getestet mit:** Aspose.Imaging für Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}