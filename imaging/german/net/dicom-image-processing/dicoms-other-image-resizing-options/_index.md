---
"description": "Erfahren Sie, wie Sie die Größe von DICOM-Bildern mit Aspose.Imaging für .NET ändern. Eine Schritt-für-Schritt-Anleitung zur effizienten medizinischen Bildbearbeitung."
"linktitle": "Weitere Optionen zur Bildgrößenänderung von DICOM in Aspose.Imaging für .NET"
"second_title": "Aspose.Imaging .NET Bildverarbeitungs-API"
"title": "Weitere Optionen zur Bildgrößenänderung von DICOM in Aspose.Imaging für .NET"
"url": "/de/net/dicom-image-processing/dicoms-other-image-resizing-options/"
"weight": 20
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Weitere Optionen zur Bildgrößenänderung von DICOM in Aspose.Imaging für .NET

Möchten Sie mit DICOM-Bildern (Digital Imaging and Communications in Medicine) in Ihrer .NET-Anwendung arbeiten? Aspose.Imaging für .NET bietet leistungsstarke Tools zur effizienten Bearbeitung von DICOM-Bildern. In diesem Tutorial befassen wir uns mit „Weiteren Optionen zur Bildgrößenänderung in DICOM“ mithilfe von Aspose.Imaging für .NET. Wir behandeln die Voraussetzungen, importieren Namespaces und bieten eine Schritt-für-Schritt-Anleitung, die Ihnen hilft, die DICOM-Bildgrößenänderung effektiv zu verstehen und umzusetzen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. Installieren Sie Aspose.Imaging für .NET
Um mit DICOM-Bildern mit Aspose.Imaging für .NET zu arbeiten, müssen Sie die Bibliothek installieren. Sie können sie von der Website herunterladen.

[Laden Sie Aspose.Imaging für .NET herunter](https://releases.aspose.com/imaging/net/)

2. Einrichten einer Entwicklungsumgebung
Stellen Sie sicher, dass Sie eine .NET-Entwicklungsumgebung eingerichtet haben, einschließlich Visual Studio oder einer anderen kompatiblen IDE.

3. DICOM-Bild
Sie sollten über eine DICOM-Bilddatei (z. B. „file.dcm“) verfügen, deren Größe Sie mit Aspose.Imaging für .NET ändern möchten.

## Namespaces importieren

In Ihrem C#-Code müssen Sie die erforderlichen Namespaces importieren, um Aspose.Imaging zu verwenden. So geht's:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
```

Lassen Sie uns nun den Prozess der Bildgrößenänderung in mehrere Schritte unterteilen.

## Schritt 1: Laden Sie das DICOM-Bild
Zu Beginn müssen Sie das DICOM-Bild aus Ihrem Dateisystem laden.

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
{
    // Ihr Code hier
}
```

## Schritt 2: Größe proportional nach Höhe anpassen
Sie können die Größe des DICOM-Bildes proportional anpassen, indem Sie die Höhe in Pixeln und den Größenänderungstyp angeben. In diesem Beispiel verwenden wir „AdaptiveResample“ als Größenänderungstyp.

```csharp
image.ResizeHeightProportionally(100, ResizeType.AdaptiveResample);
```

## Schritt 3: Speichern Sie das skalierte Bild
Nachdem Sie die Größe des Bildes geändert haben, können Sie es im gewünschten Format speichern. Hier speichern wir es als BMP-Bild.

```csharp
image.Save(dataDir + "DICOMSOtherImageResizingOptions_out.bmp", new BmpOptions());
```

## Schritt 4: Größe proportional nach Breite anpassen
Sie können die Größe des DICOM-Bildes auch proportional ändern, indem Sie die Breite in Pixeln und den Größenänderungstyp angeben.

```csharp
image1.ResizeWidthProportionally(150, ResizeType.AdaptiveResample);
```

## Schritt 5: Speichern Sie das skalierte Bild
Speichern Sie das skalierte Bild wie im vorherigen Schritt als BMP-Bild.

```csharp
image1.Save(dataDir + "DICOMSOtherImageResizingOptions1_out.bmp", new BmpOptions());
```

Herzlichen Glückwunsch! Sie haben die Größe eines DICOM-Bildes mit Aspose.Imaging für .NET erfolgreich geändert. Diese Bibliothek bietet verschiedene Optionen zur Bearbeitung von DICOM-Bildern und ist damit ein wertvolles Werkzeug für Anwendungen im Gesundheitswesen und in der medizinischen Bildgebung.

## Abschluss

In diesem Tutorial haben wir die weiteren Möglichkeiten zur Bildgrößenänderung in DICOM mit Aspose.Imaging für .NET untersucht. Wir haben die Voraussetzungen erläutert, Namespaces importiert und eine Schritt-für-Schritt-Anleitung zur Größenänderung von DICOM-Bildern bereitgestellt. Aspose.Imaging für .NET vereinfacht die Arbeit mit medizinischen Bildern und bietet eine breite Palette an Funktionen für Anwendungen im Gesundheitswesen.

Haben Sie weitere Fragen oder benötigen Sie Hilfe zu Aspose.Imaging für .NET? Lesen Sie die Dokumentation oder besuchen Sie das Aspose-Community-Forum für Unterstützung:

- [Aspose.Imaging für .NET Dokumentation](https://reference.aspose.com/imaging/net/)
- [Aspose.Imaging für .NET-Unterstützung](https://forum.aspose.com/)

## Häufig gestellte Fragen

### F1: Was ist DICOM?

A1: DICOM steht für Digital Imaging and Communications in Medicine. Es handelt sich um einen Standard für die Übertragung, Speicherung und Weitergabe medizinischer Bilder wie Röntgenaufnahmen, MRTs und CT-Scans in einem digitalen Format.

### F2: Kann ich Aspose.Imaging für .NET kostenlos nutzen?

A2: Aspose.Imaging für .NET ist eine kommerzielle Bibliothek. Sie können eine kostenlose Testversion herunterladen, um die Funktionen zu testen. Für die vollständige Nutzung ist jedoch eine Lizenz erforderlich.

### F3: Welche anderen Bildbearbeitungsoptionen bietet Aspose.Imaging für .NET?

A3: Aspose.Imaging für .NET bietet eine breite Palette an Bildverarbeitungsoptionen, darunter Formatkonvertierung, Bildoptimierung und Zeichnen auf Bildern. Alle Funktionen finden Sie in der Dokumentation.

### F4: Ist Aspose.Imaging für .NET für Anwendungen im Gesundheitswesen geeignet?

A4: Ja, Aspose.Imaging für .NET wird häufig in Gesundheitsanwendungen zur Verarbeitung von DICOM-Bildern verwendet und ist daher ein wertvolles Tool für die Entwicklung medizinischer Bildgebungssoftware.

### F5: Kann ich eine temporäre Lizenz für Aspose.Imaging für .NET erhalten?
w
A5: Ja, Sie können eine temporäre Lizenz für Test- und Evaluierungszwecke erhalten. Besuchen Sie [Asposes temporäre Lizenzseite](https://purchase.aspose.com/temporary-license/) für weitere Informationen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}