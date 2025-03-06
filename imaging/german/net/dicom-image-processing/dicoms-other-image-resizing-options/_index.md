---
title: Weitere DICOM-Optionen zur Größenänderung von Bildern in Aspose.Imaging für .NET
linktitle: Weitere DICOM-Optionen zur Größenänderung von Bildern in Aspose.Imaging für .NET
second_title: Aspose.Imaging .NET-Bildverarbeitungs-API
description: Erfahren Sie, wie Sie die Größe von DICOM-Bildern mit Aspose.Imaging für .NET ändern. Eine Schritt-für-Schritt-Anleitung für eine effiziente medizinische Bildbearbeitung.
weight: 20
url: /de/net/dicom-image-processing/dicoms-other-image-resizing-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Weitere DICOM-Optionen zur Größenänderung von Bildern in Aspose.Imaging für .NET

Möchten Sie mit DICOM-Bildern (Digital Imaging and Communications in Medicine) in Ihrer .NET-Anwendung arbeiten? Aspose.Imaging für .NET bietet leistungsstarke Tools zur effizienten Bearbeitung von DICOM-Bildern. In diesem Tutorial befassen wir uns mit „Anderen DICOM-Optionen zur Größenänderung von Bildern“ mithilfe von Aspose.Imaging für .NET. Wir behandeln die Voraussetzungen, importieren Namensräume und stellen eine Schritt-für-Schritt-Anleitung bereit, die Ihnen hilft, die Größenänderung von DICOM-Bildern effektiv zu verstehen und umzusetzen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. Installieren Sie Aspose.Imaging für .NET
Um mit DICOM-Bildern mit Aspose.Imaging für .NET arbeiten zu können, müssen Sie die Bibliothek installieren. Sie können es von der Website herunterladen.

[Laden Sie Aspose.Imaging für .NET herunter](https://releases.aspose.com/imaging/net/)

2. Richten Sie eine Entwicklungsumgebung ein
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
Zunächst müssen Sie das DICOM-Bild aus Ihrem Dateisystem laden.

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
{
    // Ihr Code hier
}
```

## Schritt 2: Proportionale Größenänderung nach Höhe
Sie können die Größe des DICOM-Bildes proportional ändern, indem Sie die Höhe in Pixel und den Größenänderungstyp angeben. In diesem Beispiel verwenden wir „AdaptiveResample“ als Größenänderungstyp.

```csharp
image.ResizeHeightProportionally(100, ResizeType.AdaptiveResample);
```

## Schritt 3: Speichern Sie das in der Größe geänderte Bild
Nachdem Sie die Größe des Bildes geändert haben, können Sie es im gewünschten Format speichern. Hier speichern wir es als BMP-Bild.

```csharp
image.Save(dataDir + "DICOMSOtherImageResizingOptions_out.bmp", new BmpOptions());
```

## Schritt 4: Proportionale Größenänderung nach Breite
Sie können die Größe des DICOM-Bilds auch proportional ändern, indem Sie die Breite in Pixel und den Größenänderungstyp angeben.

```csharp
image1.ResizeWidthProportionally(150, ResizeType.AdaptiveResample);
```

## Schritt 5: Speichern Sie das geänderte Bild
Speichern Sie das verkleinerte Bild wie im vorherigen Schritt als BMP-Bild.

```csharp
image1.Save(dataDir + "DICOMSOtherImageResizingOptions1_out.bmp", new BmpOptions());
```

Glückwunsch! Sie haben die Größe eines DICOM-Bildes mit Aspose.Imaging für .NET erfolgreich geändert. Diese Bibliothek bietet verschiedene Optionen zur Bearbeitung von DICOM-Bildern und ist damit ein wertvolles Werkzeug für das Gesundheitswesen und medizinische Bildgebungsanwendungen.

## Abschluss

In diesem Tutorial haben wir „Andere DICOM-Optionen zur Größenänderung von Bildern“ mithilfe von Aspose.Imaging für .NET untersucht. Wir haben die Voraussetzungen behandelt, Namespaces importiert und eine Schritt-für-Schritt-Anleitung zur Größenänderung von DICOM-Bildern bereitgestellt. Aspose.Imaging für .NET vereinfacht die Arbeit mit medizinischen Bildern und bietet eine breite Palette von Funktionen für Anwendungen im Gesundheitswesen.

Haben Sie weitere Fragen oder benötigen Sie Hilfe zu Aspose.Imaging für .NET? Sehen Sie sich die Dokumentation an oder besuchen Sie das Aspose-Community-Forum, um Unterstützung zu erhalten:

- [Aspose.Imaging für .NET-Dokumentation](https://reference.aspose.com/imaging/net/)
- [Aspose.Imaging für .NET-Unterstützung](https://forum.aspose.com/)

## FAQs

### F1: Was ist DICOM?

A1: DICOM steht für Digital Imaging and Communications in Medicine. Es handelt sich um einen Standard für die Übertragung, Speicherung und Weitergabe medizinischer Bilder wie Röntgen-, MRT- und CT-Scans in einem digitalen Format.

### F2: Kann ich Aspose.Imaging für .NET kostenlos nutzen?

A2: Aspose.Imaging für .NET ist eine kommerzielle Bibliothek. Sie können eine kostenlose Testversion herunterladen, um die Funktionen auszuprobieren. Für die vollständige Nutzung ist jedoch eine Lizenz erforderlich.

### F3: Welche weiteren Bildbearbeitungsoptionen bietet Aspose.Imaging für .NET?

A3: Aspose.Imaging für .NET bietet eine breite Palette an Bildverarbeitungsoptionen, einschließlich Formatkonvertierung, Bildverbesserung und Zeichnen auf Bildern. Sie können den gesamten Funktionsumfang in der Dokumentation erkunden.

### F4: Ist Aspose.Imaging für .NET für Anwendungen im Gesundheitswesen geeignet?

A4: Ja, Aspose.Imaging für .NET wird häufig in Gesundheitsanwendungen für die Verarbeitung von DICOM-Bildern verwendet, was es zu einem wertvollen Werkzeug für die Entwicklung medizinischer Bildgebungssoftware macht.

### F5: Kann ich eine temporäre Lizenz für Aspose.Imaging für .NET erhalten?
w
 A5: Ja, Sie können eine temporäre Lizenz zu Test- und Evaluierungszwecken erwerben. Besuchen[Asposes temporäre Lizenzseite](https://purchase.aspose.com/temporary-license/) für mehr Informationen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
