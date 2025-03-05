---
title: Graustufen-DICOM-Bilder mit Aspose.Imaging für .NET
linktitle: Graustufen auf DICOM in Aspose.Imaging für .NET
second_title: Aspose.Imaging .NET-Bildverarbeitungs-API
description: Erfahren Sie, wie Sie mit Aspose.Imaging für .NET, einer leistungsstarken Bildverarbeitungsbibliothek, eine Grauskalierung von DICOM-Bildern durchführen.
type: docs
weight: 24
url: /de/net/dicom-image-processing/grayscale-on-dicom/
---
Wenn Sie mit medizinischen Bilddaten im DICOM-Format arbeiten und Graustufentransformationen durchführen müssen, bietet Aspose.Imaging für .NET eine leistungsstarke Lösung. In dieser Schritt-für-Schritt-Anleitung führen wir Sie durch den Prozess der Grauskalierung eines DICOM-Bildes mit Aspose.Imaging. Diese Bibliothek ist ein vielseitiges Tool, mit dem Sie in einer .NET-Umgebung mit verschiedenen Bildformaten, einschließlich DICOM, arbeiten können. Lass uns anfangen!

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1.  Aspose.Imaging für .NET: Diese Bibliothek sollte installiert sein. Sie können es hier herunterladen[Aspose.Imaging für .NET-Downloadseite](https://releases.aspose.com/imaging/net/).

2. DICOM-Bild: Sie sollten ein DICOM-Bild haben, das Sie in Graustufen umwandeln möchten. Wenn Sie noch keins haben, können Sie zu Testzwecken Beispiel-DICOM-Bilder finden.

## Namespaces importieren

Importieren wir zunächst die notwendigen Namespaces, um mit Aspose.Imaging zu arbeiten:

```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

Nachdem Sie nun die Voraussetzungen geschaffen und die Namensräume importiert haben, können wir mit dem Grauskalierungsprozess Schritt für Schritt fortfahren.

## Schritt 1: Initialisieren Sie das DICOM-Bild

 Wir beginnen mit der Initialisierung des DICOM-Bildes. In diesem Beispiel gehen wir davon aus, dass die DICOM-Datei den Namen „file.dcm“ trägt und sich in einem von angegebenen Verzeichnis befindet`dataDir`.

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
```

## Schritt 2: Graustufentransformation

 Der nächste Schritt besteht darin, das geladene DICOM-Bild mithilfe von in seine Graustufendarstellung umzuwandeln`Grayscale()` Methode. Diese Methode wandelt das Bild automatisch in Graustufen um.

```csharp
{
    // Bild in seine Graustufendarstellung umwandeln
    image.Grayscale();
}
```

## Schritt 3: Speichern Sie das Graustufenbild

 Nachdem Sie das Bild in Graustufen skaliert haben, können Sie das resultierende Bild speichern. In diesem Beispiel speichern wir es im BMP-Format mit`BmpOptions()`.

```csharp
image.Save(dataDir + "GrayscalingOnDICOM_out.bmp", new BmpOptions());
```

## Abschluss

In diesem Tutorial haben wir gelernt, wie man mit Aspose.Imaging für .NET eine Grauskalierung an einem DICOM-Bild durchführt. Diese Bibliothek vereinfacht die Arbeit mit medizinischen Bilddaten und ermöglicht Ihnen die einfache Durchführung verschiedener Transformationen. Ob Sie an medizinischer Forschung oder an Anwendungen im Gesundheitswesen arbeiten, Aspose.Imaging kann ein wertvolles Werkzeug in Ihrem .NET-Entwicklungs-Toolkit sein.

## FAQs

### F1: Was ist DICOM?

A1: DICOM steht für Digital Imaging and Communications in Medicine. Es handelt sich um einen Standard für die Handhabung, Speicherung, den Druck und die Übertragung medizinischer Bilder.

### F2: Ist Aspose.Imaging für die nichtmedizinische Bildverarbeitung geeignet?

A2: Ja, Aspose.Imaging ist eine vielseitige Bibliothek, die eine breite Palette von Bildformaten für verschiedene Anwendungen über die medizinische Bildgebung hinaus verarbeiten kann.

### F3: Wo finde ich weitere Dokumentation?

 A3: Sie können sich auf die beziehen[Aspose.Imaging für .NET-Dokumentation](https://reference.aspose.com/imaging/net/) Ausführliche Informationen und Beispiele finden Sie hier.

### F4: Gibt es eine kostenlose Testversion?

 A4: Ja, Sie können auf a zugreifen[kostenlose Testversion von Aspose.Imaging](https://releases.aspose.com/) seine Fähigkeiten zu bewerten.

### F5: Wie kann ich Unterstützung für Aspose.Imaging erhalten?

 A5: Wenn Sie Fragen haben oder Hilfe benötigen, können Sie die besuchen[Aspose.Imaging-Forum](https://forum.aspose.com/) um Hilfe von der Community zu suchen oder ihr Support-Team zu kontaktieren.