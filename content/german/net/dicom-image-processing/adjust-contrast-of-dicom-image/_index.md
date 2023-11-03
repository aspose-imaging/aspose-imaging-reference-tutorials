---
title: DICOM-Bildkontrastanpassung mit Aspose.Imaging für .NET
linktitle: Passen Sie den Kontrast des DICOM-Bildes in Aspose.Imaging für .NET an
second_title: Aspose.Imaging .NET-Bildverarbeitungs-API
description: Verbessern Sie medizinische Bilder mit Aspose.Imaging für .NET. Passen Sie den DICOM-Bildkontrast mit einfachen Schritten an.
type: docs
weight: 11
url: /de/net/dicom-image-processing/adjust-contrast-of-dicom-image/
---
In der Welt der medizinischen Bildgebung ist eine präzise Kontrolle der Bildqualität von größter Bedeutung. Aspose.Imaging für .NET bietet eine leistungsstarke Lösung zur einfachen Bearbeitung von DICOM-Bildern. In dieser Schritt-für-Schritt-Anleitung führen wir Sie durch den Prozess der Anpassung des Kontrasts eines DICOM-Bildes mit Aspose.Imaging für .NET. Dieses Tutorial richtet sich an diejenigen, die die Sichtbarkeit medizinischer Bilder für Diagnose- oder Forschungszwecke verbessern möchten. 

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, müssen einige Voraussetzungen erfüllt sein:

1. Aspose.Imaging für .NET-Bibliothek
 Sie sollten die Aspose.Imaging für .NET-Bibliothek installiert haben. Die Bibliothek und ausführliche Dokumentation finden Sie auf der[Aspose.Imaging für .NET-Seite](https://reference.aspose.com/imaging/net/).

2. Entwicklungsumgebung
Stellen Sie sicher, dass Sie eine .NET-Entwicklungsumgebung wie Visual Studio eingerichtet haben.

Nachdem wir nun die Voraussetzungen erfüllt haben, beginnen wir Schritt für Schritt mit der Anpassung des Kontrasts eines DICOM-Bildes.

## Notwendige Namespaces importieren

Zunächst müssen Sie die erforderlichen Namespaces für Ihr Projekt importieren. Dies ermöglicht Ihnen den Zugriff auf die Klassen und Methoden, die für die Arbeit mit DICOM-Bildern erforderlich sind.

### Schritt 1: Namespaces importieren

```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.FileFormats.Dicom.DicomImage;
using Aspose.Imaging.ImageOptions;
```

Stellen Sie sicher, dass Sie diese Namespaces oben in Ihre C#-Codedatei einfügen.

## Schritt für Schritt Anleitung

Nachdem wir nun die erforderlichen Namespaces importiert haben, unterteilen wir den Prozess der Kontrastanpassung eines DICOM-Bildes in mehrere Schritte.

### Schritt 2: Definieren Sie das Dokumentenverzeichnis

Zunächst sollten Sie das Verzeichnis angeben, in dem sich Ihr DICOM-Bild befindet.

```csharp
string dataDir = "Your Document Directory";
```

 Ersetzen`"Your Document Directory"` mit dem tatsächlichen Pfad zu Ihrem DICOM-Bild.

### Schritt 3: Laden Sie das DICOM-Bild

In diesem Schritt laden wir das DICOM-Bild aus dem angegebenen Dateistream.

```csharp
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
```

 Hier,`"file.dcm"` sollte durch den Dateinamen Ihres DICOM-Bildes ersetzt werden.

### Schritt 4: Passen Sie den Kontrast an

Um die Sichtbarkeit des DICOM-Bildes zu verbessern, können Sie den Kontrast anpassen. Die folgende Codezeile erhöht den Kontrast um 50 %.

```csharp
image.AdjustContrast(50);
```

 Sie können den Wert ändern`50` um Ihren spezifischen Kontrastanpassungsanforderungen gerecht zu werden.

### Schritt 5: Speichern Sie das resultierende Bild

 Um das geänderte Bild beizubehalten, sollten Sie es speichern. Erstellen Sie eine Instanz von`BmpOptions` für das resultierende Bild und speichern Sie es dann.

```csharp
image.Save(dataDir + "AdjustContrastDICOM_out.bmp", new BmpOptions());
```

 Ersetzen`"AdjustContrastDICOM_out.bmp"`mit dem gewünschten Namen der Ausgabedatei.

## Abschluss

In diesem Tutorial haben wir untersucht, wie Sie den Kontrast eines DICOM-Bildes mit Aspose.Imaging für .NET anpassen. Mit der Leistungsfähigkeit dieser Bibliothek können Sie medizinische Bilder verfeinern, um sie informativer und für Diagnose- oder Forschungszwecke geeigneter zu machen.

 Weitere Informationen finden Sie unter[Aspose.Imaging für .NET-Dokumentation](https://reference.aspose.com/imaging/net/) . Wenn Sie es noch nicht getan haben, können Sie die Bibliothek unter herunterladen[Hier](https://releases.aspose.com/imaging/net/) oder erhalten Sie eine temporäre Lizenz von[dieser Link](https://purchase.aspose.com/temporary-license/).

Haben Sie Fragen zur Bearbeitung von DICOM-Bildern oder zur Verwendung von Aspose.Imaging für .NET? Lassen Sie uns in den FAQs unten einige häufig gestellte Fragen beantworten.

## FAQs

### F1: Was ist ein DICOM-Bildformat?

A1: DICOM steht für Digital Imaging and Communications in Medicine. Dabei handelt es sich um ein Standardformat, das für die Speicherung und den Austausch medizinischer Bilder wie Röntgenaufnahmen und MRT-Scans verwendet wird.

### F2: Kann ich den Kontrast anderer Bildformate mit Aspose.Imaging für .NET anpassen?

A2: Aspose.Imaging für .NET unterstützt hauptsächlich DICOM-Bilder. Sie können die Dokumentation auf Kompatibilität mit anderen Formaten überprüfen.

### F3: Ist Aspose.Imaging für .NET kostenlos?

 A3: Aspose.Imaging für .NET ist eine kommerzielle Bibliothek, Sie können sie jedoch mit einer kostenlosen Testversion erkunden[Hier](https://releases.aspose.com/).

### F4: Gibt es weitere Bildanpassungen, die ich mit Aspose.Imaging für .NET vornehmen kann?

A4: Ja, Aspose.Imaging für .NET bietet eine breite Palette an Bildbearbeitungsfunktionen, einschließlich Größenänderung, Zuschneiden und Filtern.

### F5: Kann ich Aspose.Imaging für .NET für die nichtmedizinische Bildverarbeitung verwenden?

A5: Auf jeden Fall! Während Aspose.Imaging vielseitig für die medizinische Bildverarbeitung geeignet ist, kann es auch für allgemeine Bildbearbeitungsaufgaben verwendet werden.