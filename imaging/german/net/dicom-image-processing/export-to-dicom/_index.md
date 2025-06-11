---
"description": "Erfahren Sie, wie Sie mit Aspose.Imaging Bilder in das DICOM-Format in .NET exportieren. Konvertieren Sie medizinische Bilder mühelos."
"linktitle": "Export nach DICOM in Aspose.Imaging für .NET"
"second_title": "Aspose.Imaging .NET Bildverarbeitungs-API"
"title": "Exportieren Sie Bilder nach DICOM in Aspose.Imaging für .NET"
"url": "/de/net/dicom-image-processing/export-to-dicom/"
"weight": 23
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren Sie Bilder nach DICOM in Aspose.Imaging für .NET

Im Bereich der medizinischen Bildgebung ist das Digital Imaging and Communications in Medicine (DICOM)-Format unangefochtener Marktführer. DICOM-Dateien speichern und verwalten medizinische Bilder und zugehörige Informationen und ermöglichen so den nahtlosen Austausch und die Interpretation medizinischer Bilder zwischen verschiedenen Gesundheitssystemen. Wenn Sie mit DICOM-Dateien in Ihrer .NET-Anwendung arbeiten möchten, sind Sie hier richtig. In diesem Tutorial erfahren Sie, wie Sie Bilder mit Aspose.Imaging für .NET, einer leistungsstarken Bibliothek, die den Prozess vereinfacht, in DICOM exportieren. Am Ende dieses Leitfadens verfügen Sie über das Wissen, das Potenzial von Aspose.Imaging für .NET zu nutzen und mühelos DICOM-Dateien zu erstellen.

## Voraussetzungen

Bevor wir uns mit den technischen Aspekten befassen, müssen Sie unbedingt sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

1. Aspose.Imaging für .NET

Sie müssen Aspose.Imaging für .NET in Ihrer Entwicklungsumgebung installiert haben. Falls noch nicht geschehen, können Sie es von der Aspose-Website herunterladen. Hier ist die [Download-Link](https://releases.aspose.com/imaging/net/) für Ihre Bequemlichkeit.

2. .NET-Entwicklungsumgebung

Um mit Aspose.Imaging für .NET arbeiten zu können, benötigen Sie eine .NET-Entwicklungsumgebung. Stellen Sie sicher, dass Sie Visual Studio oder ein anderes .NET-Entwicklungstool Ihrer Wahl installiert haben.

3. Bilddateien

Stellen Sie die Bilddateien zusammen, die Sie in das DICOM-Format konvertieren möchten. Dieses Tutorial setzt voraus, dass Sie eine Beispielbilddatei (z. B. „sample.jpg“) und eine mehrseitige Bilddatei (z. B. „multipage.tif“) für die Konvertierung bereithalten.

## Namespaces importieren

Stellen Sie sicher, dass Sie in Ihrem C#-Code die erforderlichen Namespaces für den Zugriff auf die Aspose.Imaging-Bibliothek importieren. Fügen Sie dazu am Anfang Ihres Codes die folgenden Zeilen hinzu:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Dicom;
```

Lassen Sie uns nun den Prozess des Bilderexports nach DICOM mit Aspose.Imaging für .NET in eine Reihe überschaubarer Schritte aufteilen.

## Schritt 1: Einrichten der Umgebung

Stellen Sie sicher, dass Sie in Ihrer Entwicklungsumgebung ein .NET-Projekt erstellt und Aspose.Imaging für .NET als Referenz hinzugefügt haben. Falls nicht, lesen Sie die Aspose.Imaging-Dokumentation. [Hier](https://reference.aspose.com/imaging/net/) für eine Anleitung zum Einstieg.

## Schritt 2: Dateipfade definieren

Definieren Sie in Ihrem C#-Code die Pfade für Ihre Eingabebilddateien (einzeln und mehrseitig) sowie die Pfade für die Ausgabe-DICOM-Dateien. Ersetzen Sie „Ihr Dokumentverzeichnis“ durch den tatsächlichen Verzeichnispfad, in dem Ihre Bilddateien gespeichert sind.

```csharp
string dataDir = "Your Document Directory";
string fileName = "sample.jpg";
string inputFileNameSingle = Path.Combine(dataDir, fileName);
string inputFileNameMultipage = Path.Combine(dataDir, "multipage.tif");
string outputFileNameSingleDcm = Path.Combine(dataDir, "output.dcm");
string outputFileNameMultipageDcm = Path.Combine(dataDir, "outputMultipage.dcm");
```

## Schritt 3: Einzelnes Bild in DICOM konvertieren

Um ein einzelnes Bild (in diesem Fall „sample.jpg“) in DICOM zu konvertieren, verwenden Sie den folgenden Codeausschnitt:

```csharp
using (var image = Image.Load(inputFileNameSingle))
{
    image.Save(outputFileNameSingleDcm, new DicomOptions());
}
```

Dieser Code lädt das Bild, speichert es als DICOM-Datei und wendet DicomOptions für die Konvertierung an.

## Schritt 4: Mehrseitiges Bild in DICOM konvertieren

Das DICOM-Format unterstützt mehrseitige Bilder. Sie können GIF- oder TIFF-Bilder genauso wie JPEG-Bilder in DICOM konvertieren. So geht's:

```csharp
using (var image = Image.Load(inputFileNameMultipage))
{
    image.Save(outputFileNameMultipageDcm, new DicomOptions());
}
```

Dieser Code führt denselben Konvertierungsprozess für mehrseitige Bilder durch und stellt sicher, dass jede Seite in der resultierenden DICOM-Datei erhalten bleibt.

## Abschluss

Der Export von Bildern ins DICOM-Format ist für verschiedene Anwendungen im Gesundheitswesen und in der medizinischen Bildgebung unerlässlich. Aspose.Imaging für .NET vereinfacht diesen Prozess und ermöglicht Entwicklern die effiziente Erstellung von DICOM-Dateien. Mit dieser Schritt-für-Schritt-Anleitung können Sie die DICOM-Exportfunktion nahtlos in Ihre .NET-Anwendungen integrieren.

Wenn Sie auf Probleme stoßen oder spezielle Anforderungen haben, sind die Aspose.Imaging-Community und die Support-Foren wertvolle Ressourcen. Sie finden Hilfe und Anleitung [Hier](https://forum.aspose.com/).

## Häufig gestellte Fragen

### F1: Kann ich Bilder mit Aspose.Imaging für .NET in einer Webanwendung in DICOM konvertieren?

A1: Ja, Aspose.Imaging für .NET kann in Webanwendungen verwendet werden, um Bilder in DICOM zu konvertieren. Integrieren Sie die Bibliothek in Ihr Webprojekt und befolgen Sie die in diesem Tutorial beschriebenen Schritte.

### F2: Gibt es Lizenzierungsoptionen für Aspose.Imaging für .NET?

A2: Aspose bietet verschiedene Lizenzoptionen an, darunter temporäre Lizenzen zur Evaluierung und kommerzielle Lizenzen für den Produktionseinsatz. Sie können die Lizenzdetails erkunden [Hier](https://purchase.aspose.com/buy) und erhalten Sie eine vorübergehende Lizenz [Hier](https://purchase.aspose.com/temporary-license/).

### F3: Kann ich außer JPEG, GIF und TIFF auch andere Bildformate in DICOM konvertieren?

A3: Aspose.Imaging für .NET unterstützt eine Vielzahl von Bildformaten, sodass Sie Bilder in Formaten wie BMP, PNG und anderen auch in DICOM konvertieren können. Der Prozess bleibt für verschiedene Bildtypen ähnlich.

### F4: Wie kann ich beim Konvertieren von Bildern mit DICOM-Metadaten umgehen?

A4: Mit Aspose.Imaging für .NET können Sie DICOM-Metadaten während des Konvertierungsprozesses bearbeiten und anpassen. Detaillierte Informationen zum Umgang mit DICOM-Metadaten finden Sie in der Dokumentation.

### F5: Gibt es eine Testversion von Aspose.Imaging für .NET?

A5: Ja, Sie können auf eine kostenlose Testversion von Aspose.Imaging für .NET zugreifen, um dessen Funktionen zu testen. Sie können die Testversion herunterladen [Hier](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}