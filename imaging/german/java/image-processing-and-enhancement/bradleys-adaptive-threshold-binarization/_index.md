---
date: 2026-01-09
description: Erfahren Sie, wie Sie ein Bild mit Aspose.Imaging für Java binarisieren.
  Dieser Leitfaden behandelt Bildverarbeitungs‑Java‑Techniken für die Konvertierung
  von DICOM zu BMP.
linktitle: Bradley's Adaptive Threshold Binarization
second_title: Aspose.Imaging Java Image Processing API
title: Wie man ein Bild mit Aspose.Imaging für Java binarisiert
url: /de/java/image-processing-and-enhancement/bradleys-adaptive-threshold-binarization/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Wie man ein Bild mit Aspose.Imaging für Java binarisiert

Bilder spielen eine entscheidende Rolle in der digitalen Welt, sei es auf Websites, in Dokumenten oder als Teil verschiedener Anwendungen. Wenn Sie sich fragen, **wie man ein Bild effizient binarisiert**, insbesondere für medizinische Formate wie DICOM, sind Sie hier genau richtig. Die Bildbinarisierung vereinfacht ein Bild, indem es in eine Schwarz‑Weiß‑Darstellung umgewandelt wird, was ideal für nachgelagerte Analysen, OCR oder Speicheroptimierung ist. In diesem Tutorial führen wir Sie durch den gesamten Prozess mithilfe von Aspose.Imaging für Java’s Bradley‑Adaptive‑Threshold‑Binarisierung.

## Schnelle Antworten
- **Was bewirkt die Binarisierung?** Sie wandelt jedes Pixel basierend auf einem Schwellenwert in Schwarz oder Weiß um.
- **Welche Bibliothek ist die beste für die Bildverarbeitung in Java?** Aspose.Imaging für Java bietet robuste, lizenzfreie Testfunktionen.
- **Kann ich DICOM‑Dateien direkt verarbeiten?** Ja, Aspose.Imaging kann DICOM laden und als BMP, PNG usw. ausgeben.
- **Benötige ich eine Lizenz für die Produktion?** Für den Einsatz außerhalb der Testphase ist eine kommerzielle Lizenz erforderlich.
- **Welche Java‑Version wird unterstützt?** Java 8 und neuer sind vollständig kompatibel.

## Was ist Bildbinarisierung?
Bildbinarisierung ist der Vorgang, ein Graustufen‑ oder Farbbild in ein binäres Bild zu transformieren, bei dem jedes Pixel entweder 0 (schwarz) oder 255 (weiß) ist. Dieser Schritt ist häufig die erste Stufe in medizinischen Bildverarbeitungspipelines, beim Dokumentenscannen und in Computer‑Vision‑Aufgaben.

## Warum Aspose.Imaging für Java verwenden?
Aspose.Imaging bietet eine reine Java‑API, die **DICOM lädt**, fortschrittliche Algorithmen wie **Bradley’s Adaptive Threshold** anwendet und das Ergebnis in gängigen Formaten speichert, ohne externe native Bibliotheken zu benötigen. Es ist ideal für **medizinische Bildverarbeitung**, **Konvertierung von DICOM zu BMP** und andere Java‑basierte Workflows.

## Voraussetzungen

Bevor Sie in den Code eintauchen, stellen Sie sicher, dass Sie Folgendes haben:

- **Java‑Entwicklungsumgebung** – JDK 8 oder neuer installiert.
- **Aspose.Imaging für Java** – Download von der offiziellen Seite: [Download Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/).
- **Eine DICOM‑Bilddatei** – Beliebige Beispiel‑DICOM‑Datei, die Sie binarisieren möchten.

Jetzt, wo alles bereit ist, gehen wir zur Implementierung über.

## Wie man ein Bild binarisiert – Schritt‑für‑Schritt‑Anleitung

### Pakete importieren
Zuerst importieren Sie die erforderlichen Aspose.Imaging‑Klassen. Dieses Snippet definiert außerdem die Eingabe‑ und Ausgabepfade.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";

// Load a DICOM image in an instance of DicomImage
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // Binarize image with Bradley's adaptive threshold.
    image.binarizeBradley(10);
    // Save the resultant image.
    image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
}
```

### Schritt 1: Pfade definieren
Legen Sie die Speicherorte für Ihre Quell‑DICOM‑Datei und die Ziel‑BMP‑Datei fest. Ersetzen Sie `"Your Document Directory"` durch den tatsächlichen Ordner auf Ihrem System.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "BinarizationwithBradleyAdaptiveThreshold_out.bmp";
```

### Schritt 2: DICOM‑Bild laden
Verwenden Sie Aspose.Imaging, um das **dicom image** in ein `DicomImage`‑Objekt **zu laden**. Dieses Objekt gibt Ihnen vollen Zugriff auf Pixeldaten und Verarbeitungsmethoden.

```java
try (com.aspose.imaging.fileformats.dicom.DicomImage image = (com.aspose.imaging.fileformats.dicom.DicomImage) Image.load(inputFile))
{
    // The image processing steps will go here.
}
```

### Schritt 3: Binarisierung durchführen
Wenden Sie den Bradley‑Adaptive‑Threshold‑Algorithmus an. Der Parameter (`10` in diesem Beispiel) steuert die Empfindlichkeit des Schwellenwerts; Sie können mit verschiedenen Werten experimentieren, um optimale Ergebnisse zu erzielen.

```java
image.binarizeBradley(10);
```

### Schritt 4: Binarisiertes Bild speichern
Exportieren Sie schließlich das verarbeitete Bild. Hier verwenden wir das BMP‑Format, aber Aspose.Imaging unterstützt PNG, JPEG, TIFF und viele weitere Formate.

```java
image.save(outputFile, new com.aspose.imaging.imageoptions.BmpOptions());
```

## Häufige Probleme & Fehlersuche

- **FileNotFoundException** – Stellen Sie sicher, dass der `dataDir`‑Pfad mit einem Schrägstrich endet und der DICOM‑Dateiname exakt übereinstimmt.
- **OutOfMemoryError** – Sehr große DICOM‑Dateien können erfordern, dass Sie den JVM‑Heap‑Speicher erhöhen (`-Xmx2g` oder mehr).
- **Falscher Schwellenwert** – Wenn das Ergebnis zu dunkel oder zu hell wirkt, passen Sie die an `binarizeBradley()` übergebene Ganzzahl an (z. B. 5‑15).

## Häufig gestellte Fragen

### Q1: Was ist DICOM und warum ist es in der medizinischen Bildgebung wichtig?
**A:** DICOM steht für *Digital Imaging and Communications in Medicine*. Es ist der universelle Standard zum Speichern, Übertragen und Verwalten medizinischer Bilder und ermöglicht die Interoperabilität zwischen Geräten und Systemen.

### Q2: Kann ich Aspose.Imaging für Java in kommerziellen Projekten verwenden?
**A:** Ja, Aspose.Imaging für Java bietet sowohl kostenlose Testversionen als auch kommerzielle Lizenzen. Sie können Ihre Optionen prüfen und die erforderliche Lizenz über [Aspose's Website](https://purchase.aspose.com/buy) erwerben.

### Q3: Gibt es temporäre Lizenzen für Testzwecke?
**A:** Ja, Sie können eine temporäre Lizenz für Test‑ und Evaluierungszwecke von Aspose.Imaging für Java erhalten. Weitere Informationen finden Sie unter [diesem Link](https://purchase.aspose.com/temporary-license/).

### Q4: Wo kann ich Hilfe erhalten oder Themen zu Aspose.Imaging für Java diskutieren?
**A:** Für Community‑Support und Diskussionen besuchen Sie das [Aspose.Imaging‑Forum](https://forum.aspose.com/). Dort finden Sie Antworten auf Ihre Fragen und können sich mit anderen Nutzern austauschen.

### Q5: Ist Aspose.Imaging für Java für die Bildverarbeitung in anderen Java‑basierten Anwendungen geeignet?
**A:** Absolut. Die Bibliothek funktioniert gut in Web‑Anwendungen, Desktop‑Software, Batch‑Verarbeitungstools und mehr und bietet eine konsistente API über alle Plattformen hinweg.

## Fazit
Sie haben nun gelernt, **wie man ein Bild mit Aspose.Imaging für Java und Bradley’s Adaptive Threshold binarisiert**. Diese Technik ist besonders wertvoll für **medizinische Bildverarbeitung**, da Sie DICOM‑Dateien in leichte BMP‑ (oder andere) Formate für Analyse oder Speicherung umwandeln können. Experimentieren Sie weiter mit unterschiedlichen Schwellenwerten und entdecken Sie das umfangreiche Funktionsspektrum von Aspose.Imaging.

Für weiterführende Informationen zur Bildmanipulation schauen Sie in die offizielle Dokumentation: [Aspose.Imaging for Java Documentation](https://reference.aspose.com/imaging/java/).

---

**Zuletzt aktualisiert:** 2026-01-09  
**Getestet mit:** Aspose.Imaging für Java 24.12 (zum Zeitpunkt der Erstellung)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}