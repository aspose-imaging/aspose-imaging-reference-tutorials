---
"description": "Erfahren Sie, wie Sie die Größe von DICOM-Bildern mit Aspose.Imaging für .NET, einem leistungsstarken Tool für die medizinische Bildverarbeitung, ändern. Einfache Schritte für präzise Ergebnisse."
"linktitle": "Einfache DICOM-Größenänderung in Aspose.Imaging für .NET"
"second_title": "Aspose.Imaging .NET Bildverarbeitungs-API"
"title": "Ändern Sie die Größe von DICOM-Bildern mit Aspose.Imaging für .NET"
"url": "/de/net/dicom-image-processing/dicom-simple-resizing/"
"weight": 19
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Ändern Sie die Größe von DICOM-Bildern mit Aspose.Imaging für .NET

Im sich ständig weiterentwickelnden Bereich der medizinischen Bildgebung ist Flexibilität und Präzision im Umgang mit DICOM-Dateien (Digital Imaging and Communications in Medicine) von größter Bedeutung. Aspose.Imaging für .NET erweist sich als leistungsstarke Lösung und bietet umfassende Tools für die Arbeit mit medizinischen Bildern. In diesem Tutorial erkunden wir die einfache Größenänderung von DICOM-Bildern mit Aspose.Imaging für .NET. 

## Voraussetzungen

Bevor wir in die Schritt-für-Schritt-Anleitung eintauchen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. Aspose.Imaging für .NET: Sie müssen die Bibliothek Aspose.Imaging für .NET in Ihrer Entwicklungsumgebung installiert haben. Falls noch nicht geschehen, können Sie sie hier herunterladen: [Hier](https://releases.aspose.com/imaging/net/).

2. .NET-Entwicklungsumgebung: Gute Kenntnisse in C# und einer .NET-Entwicklungsumgebung sind erforderlich.

3. DICOM-Bilddatei: Sie benötigen eine DICOM-Bilddatei, deren Größe Sie ändern möchten. Wenn Sie ein DICOM-Beispielbild zum Testen benötigen, finden Sie es problemlos online.

4. Visual Studio (optional): Obwohl nicht zwingend erforderlich, verbessert die Verwendung von Visual Studio für dieses Lernprogramm Ihre Entwicklungserfahrung.

Lassen Sie uns nun den Vorgang der Größenänderung eines DICOM-Bildes in einfache, umsetzbare Schritte unterteilen.

## Schritt 1: Namespaces importieren

Der erste Schritt besteht darin, die erforderlichen Namespaces für die Arbeit mit Aspose.Imaging zu importieren. Fügen Sie in Ihr C#-Projekt die folgenden Namespaces ein:

```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

Durch den Import dieser Namespaces erhalten Sie Zugriff auf die Funktionen, die für die Verarbeitung von DICOM-Bildern erforderlich sind.

## Schritt 2: Größenänderung des DICOM-Bilds

Lassen Sie uns nun den Prozess der Größenänderung von DICOM-Bildern in mehrere überschaubare Schritte unterteilen.

### Schritt 2.1: Festlegen des Dokumentverzeichnisses

Geben Sie in Ihrem C#-Code das Verzeichnis an, in dem sich Ihre DICOM-Datei befindet. Sie sollten ersetzen `"Your Document Directory"` durch den tatsächlichen Pfad zu Ihrem Dateiverzeichnis.

```csharp
string dataDir = "Your Document Directory";
```

### Schritt 2.2: Öffnen Sie die DICOM-Datei

Öffnen Sie anschließend die DICOM-Datei mit einem `FileStream`. Stellen Sie sicher, dass Sie ersetzen `"file.dcm"` durch den Namen Ihrer DICOM-Datei.

```csharp
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
{
    // Hier kommt Ihr Code zur Bildverarbeitung hin
}
```

### Schritt 2.3: Laden Sie das DICOM-Bild

Laden Sie das DICOM-Bild vom `fileStream`. Dadurch können Sie auf das Bild zugreifen und Vorgänge daran ausführen.

```csharp
using (DicomImage image = new DicomImage(fileStream))
{
    // Hier kommt Ihr Code zur Bildverarbeitung hin
}
```

### Schritt 2.4: Größe des DICOM-Bildes ändern

Nachdem das DICOM-Bild geladen wurde, können Sie es nun auf die gewünschten Abmessungen skalieren. In diesem Beispiel wird die Größe auf 200 x 200 Pixel geändert.

```csharp
image.Resize(200, 200);
```

### Schritt 2.5: Speichern Sie das skalierte Bild

Speichern Sie abschließend das skalierte DICOM-Bild im angegebenen Ausgabeverzeichnis. In diesem Beispiel speichern wir es als BMP-Datei.

```csharp
image.Save(dataDir + "DICOMSimpleResizing_out.bmp", new BmpOptions());
```

## Abschluss

Herzlichen Glückwunsch! Sie haben die Größe eines DICOM-Bildes mit Aspose.Imaging für .NET erfolgreich geändert. Mit diesen einfachen Schritten können Sie medizinische Bilder effizient bearbeiten, um Ihren spezifischen Anforderungen gerecht zu werden.

Wenn Sie auf Probleme stoßen oder Fragen zu Aspose.Imaging für .NET haben, zögern Sie nicht, Hilfe von der Support-Community unter der [Aspose Forum](https://forum.aspose.com/).

## Häufig gestellte Fragen

### F1: Was ist DICOM?

A1: DICOM steht für Digital Imaging and Communications in Medicine. Es handelt sich um einen Standard für die Speicherung, Übertragung und Weitergabe medizinischer Bilder und zugehöriger Informationen.

### F2: Kann ich Aspose.Imaging auch für andere Bildformate verwenden?

A2: Ja, Aspose.Imaging für .NET unterstützt neben DICOM eine Vielzahl von Bildformaten, darunter BMP, JPEG, PNG und mehr.

### F3: Ist zum Öffnen des skalierten Bildes ein DICOM-Viewer erforderlich?

A3: Nein, sobald Sie die Größe eines DICOM-Bildes mit Aspose.Imaging geändert haben, liegt das resultierende Bild in einem Standardbildformat (z. B. BMP) vor und kann mit gängigen Bildbetrachtern angezeigt werden.

### F4: Ist Aspose.Imaging für .NET mit allen Versionen von .NET Framework kompatibel?

A4: Aspose.Imaging für .NET ist mit verschiedenen Versionen des .NET Frameworks kompatibel, einschließlich .NET Core und .NET Standard. Weitere Informationen finden Sie in der Dokumentation.

### F5: Wo finde ich weitere Aspose.Imaging-Tutorials für .NET?

A5: Sie können die   [Aspose.Imaging für .NET-Dokumentation](https://reference.aspose.com/imaging/net/) für eine große Auswahl an Tutorials und Beispielen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}