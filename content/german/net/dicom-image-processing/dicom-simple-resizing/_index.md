---
title: Ändern Sie die Größe von DICOM-Bildern mit Aspose.Imaging für .NET
linktitle: Einfache DICOM-Größenänderung in Aspose.Imaging für .NET
second_title: Aspose.Imaging .NET-Bildverarbeitungs-API
description: Erfahren Sie, wie Sie die Größe von DICOM-Bildern mit Aspose.Imaging für .NET ändern, einem leistungsstarken Tool für die medizinische Bildverarbeitung. Einfache Schritte für präzise Ergebnisse.
type: docs
weight: 19
url: /de/net/dicom-image-processing/dicom-simple-resizing/
---
Im sich ständig weiterentwickelnden Bereich der medizinischen Bildgebung ist der Bedarf an Flexibilität und Präzision beim Umgang mit DICOM-Dateien (Digital Imaging and Communications in Medicine) von größter Bedeutung. Aspose.Imaging für .NET erweist sich als leistungsstarke Lösung und bietet einen umfassenden Satz an Tools für die Arbeit mit medizinischen Bildern. In diesem Tutorial untersuchen wir den unkomplizierten Prozess der Größenänderung von DICOM-Bildern mit Aspose.Imaging für .NET. 

## Voraussetzungen

Bevor wir uns mit der Schritt-für-Schritt-Anleitung befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1.  Aspose.Imaging für .NET: In Ihrer Entwicklungsumgebung muss die Aspose.Imaging für .NET-Bibliothek installiert sein. Wenn Sie es noch nicht getan haben, können Sie es hier herunterladen[Hier](https://releases.aspose.com/imaging/net/).

2. .NET-Entwicklungsumgebung: Kenntnisse in C# und einer .NET-Entwicklungsumgebung sind erforderlich.

3. DICOM-Bilddatei: Sie sollten über eine DICOM-Bilddatei verfügen, deren Größe Sie ändern möchten. Wenn Sie zum Testen ein Beispiel-DICOM-Bild benötigen, können Sie eines ganz einfach online finden.

4. Visual Studio (optional): Obwohl dies nicht zwingend erforderlich ist, wird die Verwendung von Visual Studio für dieses Tutorial Ihre Entwicklungserfahrung verbessern.

Lassen Sie uns nun den Prozess der Größenänderung eines DICOM-Bildes in einfache, umsetzbare Schritte unterteilen.

## Schritt 1: Namespaces importieren

Der erste Schritt besteht darin, die notwendigen Namespaces für die Arbeit mit Aspose.Imaging zu importieren. Fügen Sie in Ihr C#-Projekt die folgenden Namespaces ein:

```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

Durch den Import dieser Namensräume erhalten Sie Zugriff auf die für die Verarbeitung von DICOM-Bildern erforderlichen Funktionalitäten.

## Schritt 2: Größenänderung des DICOM-Bildes

Lassen Sie uns nun den DICOM-Bildgrößenänderungsprozess in mehrere überschaubare Schritte unterteilen.

### Schritt 2.1: Legen Sie das Dokumentverzeichnis fest

 Geben Sie in Ihrem C#-Code das Verzeichnis an, in dem sich Ihre DICOM-Datei befindet. Sie sollten ersetzen`"Your Document Directory"` mit dem tatsächlichen Pfad zu Ihrem Dateiverzeichnis.

```csharp
string dataDir = "Your Document Directory";
```

### Schritt 2.2: Öffnen Sie die DICOM-Datei

 Als nächstes öffnen Sie die DICOM-Datei mit a`FileStream` . Stellen Sie sicher, dass Sie ersetzen`"file.dcm"` mit dem Namen Ihrer DICOM-Datei.

```csharp
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
{
    // Ihr Code für die Bildverarbeitung kommt hierher
}
```

### Schritt 2.3: Laden Sie das DICOM-Bild

 Laden Sie das DICOM-Bild von`fileStream`Dadurch können Sie auf das Bild zugreifen und Vorgänge daran ausführen.

```csharp
using (DicomImage image = new DicomImage(fileStream))
{
    // Ihr Code für die Bildverarbeitung kommt hierher
}
```

### Schritt 2.4: Ändern Sie die Größe des DICOM-Bildes

Wenn das DICOM-Bild geladen ist, können Sie es nun auf die gewünschten Abmessungen anpassen. In diesem Beispiel ändern wir die Größe auf 200 x 200 Pixel.

```csharp
image.Resize(200, 200);
```

### Schritt 2.5: Speichern Sie das in der Größe geänderte Bild

Speichern Sie abschließend das DICOM-Bild mit geänderter Größe in Ihrem angegebenen Ausgabeverzeichnis. In diesem Beispiel speichern wir es als BMP-Datei.

```csharp
image.Save(dataDir + "DICOMSimpleResizing_out.bmp", new BmpOptions());
```

## Abschluss

Glückwunsch! Sie haben die Größe eines DICOM-Bildes mit Aspose.Imaging für .NET erfolgreich geändert. Mit diesen einfachen Schritten können Sie medizinische Bilder effizient bearbeiten, um sie an Ihre spezifischen Anforderungen anzupassen.

 Wenn Sie auf Probleme stoßen oder Fragen zu Aspose.Imaging für .NET haben, zögern Sie nicht, Hilfe von der unterstützenden Community unter zu suchen[Aspose-Forum](https://forum.aspose.com/).

## FAQs

### F1: Was ist DICOM?

A1: DICOM steht für Digital Imaging and Communications in Medicine. Es handelt sich um einen Standard zum Speichern, Übertragen und Teilen medizinischer Bilder und zugehöriger Informationen.

### F2: Kann ich Aspose.Imaging auch für andere Bildformate verwenden?

A2: Ja, Aspose.Imaging für .NET unterstützt eine Vielzahl von Bildformaten über DICOM hinaus, einschließlich BMP, JPEG, PNG und mehr.

### F3: Ist ein DICOM-Viewer erforderlich, um das skalierte Bild zu öffnen?

A3: Nein, sobald Sie die Größe eines DICOM-Bildes mit Aspose.Imaging geändert haben, liegt das resultierende Bild in einem Standardbildformat (z. B. BMP) vor und kann mit gängigen Bildbetrachtern angezeigt werden.

### F4: Ist Aspose.Imaging für .NET mit allen Versionen von .NET Framework kompatibel?

A4: Aspose.Imaging für .NET ist mit verschiedenen Versionen des .NET Frameworks kompatibel, einschließlich .NET Core und .NET Standard. Schauen Sie unbedingt in der Dokumentation nach, um Einzelheiten zu erfahren.

### F5: Wo finde ich weitere Aspose.Imaging für .NET-Tutorials?

 A5: Sie können das erkunden[Aspose.Imaging für .NET-Dokumentation](https://reference.aspose.com/imaging/net/) für eine große Auswahl an Tutorials und Beispielen.