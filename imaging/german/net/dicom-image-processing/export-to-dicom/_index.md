---
title: Exportieren Sie Bilder nach DICOM in Aspose.Imaging für .NET
linktitle: Export nach DICOM in Aspose.Imaging für .NET
second_title: Aspose.Imaging .NET-Bildverarbeitungs-API
description: Erfahren Sie, wie Sie mit Aspose.Imaging Bilder in das DICOM-Format in .NET exportieren. Konvertieren Sie medizinische Bilder mühelos.
type: docs
weight: 23
url: /de/net/dicom-image-processing/export-to-dicom/
---
Im Bereich der medizinischen Bildgebung ist das DICOM-Format (Digital Imaging and Communications in Medicine) der unangefochtene König. DICOM-Dateien speichern und verwalten medizinische Bilder und zugehörige Informationen und ermöglichen so den nahtlosen Austausch und die Interpretation medizinischer Bilder über verschiedene Gesundheitssysteme hinweg. Wenn Sie in Ihrer .NET-Anwendung mit DICOM-Dateien arbeiten möchten, sind Sie hier richtig. In diesem Tutorial erfahren Sie, wie Sie Bilder mit Aspose.Imaging für .NET, einer leistungsstarken Bibliothek, die den Prozess vereinfacht, nach DICOM exportieren. Am Ende dieses Leitfadens verfügen Sie über das nötige Wissen, um das Potenzial von Aspose.Imaging für .NET zu nutzen und mühelos DICOM-Dateien zu erstellen.

## Voraussetzungen

Bevor wir uns mit den technischen Aspekten befassen, müssen Sie unbedingt sicherstellen, dass die folgenden Voraussetzungen gegeben sind:

1. Aspose.Imaging für .NET

 In Ihrer Entwicklungsumgebung muss Aspose.Imaging für .NET installiert sein. Wenn Sie es noch nicht getan haben, können Sie es von der Aspose-Website herunterladen. Hier ist die[Download-Link](https://releases.aspose.com/imaging/net/)Für Ihren Komfort.

2. .NET-Entwicklungsumgebung

Um mit Aspose.Imaging für .NET arbeiten zu können, benötigen Sie eine .NET-Entwicklungsumgebung. Stellen Sie sicher, dass Visual Studio oder ein anderes .NET-Entwicklungstool Ihrer Wahl installiert ist.

3. Bilddateien

Sammeln Sie die Bilddateien, die Sie in das DICOM-Format konvertieren möchten. In diesem Tutorial wird davon ausgegangen, dass Sie eine Beispielbilddatei (z. B. „sample.jpg“) und eine mehrseitige Bilddatei (z. B. „multipage.tif“) für die Konvertierung bereit haben.

## Namespaces importieren

Stellen Sie in Ihrem C#-Code sicher, dass Sie die erforderlichen Namespaces importieren, um auf die Aspose.Imaging-Bibliothek zuzugreifen. Sie können dies tun, indem Sie am Anfang Ihres Codes die folgenden Zeilen hinzufügen:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Dicom;
```

Lassen Sie uns nun den Prozess des Exportierens von Bildern nach DICOM mit Aspose.Imaging für .NET in eine Reihe überschaubarer Schritte unterteilen.

## Schritt 1: Umgebung einrichten

 Stellen Sie sicher, dass Sie in Ihrer Entwicklungsumgebung ein .NET-Projekt erstellt und Aspose.Imaging für .NET als Referenz hinzugefügt haben. Wenn nicht, lesen Sie die Aspose.Imaging-Dokumentation[Hier](https://reference.aspose.com/imaging/net/) als Orientierungshilfe für den Einstieg.

## Schritt 2: Dateipfade definieren

Definieren Sie in Ihrem C#-Code die Pfade für Ihre Eingabebilddateien (einseitig und mehrseitig) sowie die Pfade für die Ausgabe-DICOM-Dateien. Sie sollten „Ihr Dokumentverzeichnis“ durch den tatsächlichen Verzeichnispfad ersetzen, in dem Ihre Bilddateien gespeichert sind.

```csharp
string dataDir = "Your Document Directory";
string fileName = "sample.jpg";
string inputFileNameSingle = Path.Combine(dataDir, fileName);
string inputFileNameMultipage = Path.Combine(dataDir, "multipage.tif");
string outputFileNameSingleDcm = Path.Combine(dataDir, "output.dcm");
string outputFileNameMultipageDcm = Path.Combine(dataDir, "outputMultipage.dcm");
```

## Schritt 3: Konvertieren Sie ein einzelnes Bild in DICOM

Um ein einzelnes Bild (in diesem Fall „sample.jpg“) in DICOM zu konvertieren, verwenden Sie den folgenden Codeausschnitt:

```csharp
using (var image = Image.Load(inputFileNameSingle))
{
    image.Save(outputFileNameSingleDcm, new DicomOptions());
}
```

Dieser Code lädt das Bild, speichert es als DICOM-Datei und wendet DicomOptions für die Konvertierung an.

## Schritt 4: Mehrseitiges Bild in DICOM konvertieren

Das DICOM-Format unterstützt mehrseitige Bilder. Sie können GIF- oder TIFF-Bilder auf die gleiche Weise wie JPEG-Bilder in DICOM konvertieren. So können Sie es machen:

```csharp
using (var image = Image.Load(inputFileNameMultipage))
{
    image.Save(outputFileNameMultipageDcm, new DicomOptions());
}
```

Dieser Code führt den gleichen Konvertierungsprozess für mehrseitige Bilder durch und stellt so sicher, dass jede Seite in der resultierenden DICOM-Datei erhalten bleibt.

## Abschluss

Der Export von Bildern in das DICOM-Format ist für verschiedene Anwendungen im Gesundheitswesen und in der medizinischen Bildgebung unerlässlich. Aspose.Imaging für .NET vereinfacht diesen Prozess und ermöglicht Entwicklern die effiziente Erstellung von DICOM-Dateien. Wenn Sie dieser Schritt-für-Schritt-Anleitung folgen, können Sie die DICOM-Exportfunktionalität nahtlos in Ihre .NET-Anwendungen integrieren.

 Wenn Sie auf Probleme stoßen oder spezielle Anforderungen haben, sind die Aspose.Imaging-Community und die Support-Foren wertvolle Ressourcen. Hier finden Sie Hilfe und Anleitung[Hier](https://forum.aspose.com/).

## FAQs

### F1: Kann ich Bilder mit Aspose.Imaging für .NET in einer Webanwendung in DICOM konvertieren?

A1: Ja, Aspose.Imaging für .NET kann in Webanwendungen zum Konvertieren von Bildern in DICOM verwendet werden. Stellen Sie sicher, dass Sie die Bibliothek in Ihr Webprojekt integrieren und die gleichen Schritte befolgen, die in diesem Tutorial beschrieben werden.

### F2: Gibt es Lizenzoptionen für Aspose.Imaging für .NET?

A2: Aspose bietet verschiedene Lizenzoptionen an, darunter temporäre Lizenzen zur Evaluierung und kommerzielle Lizenzen für die Produktionsnutzung. Sie können die Lizenzdetails erkunden[Hier](https://purchase.aspose.com/buy) und erhalten Sie eine temporäre Lizenz[Hier](https://purchase.aspose.com/temporary-license/).

### F3: Kann ich neben JPEG, GIF und TIFF auch andere Bildformate in DICOM konvertieren?

A3: Aspose.Imaging für .NET unterstützt eine Vielzahl von Bildformaten, sodass Sie auch Bilder in Formaten wie BMP, PNG und anderen in DICOM konvertieren können. Der Vorgang bleibt für verschiedene Bildtypen ähnlich.

### F4: Wie kann ich beim Konvertieren von Bildern mit DICOM-Metadaten umgehen?

A4: Mit Aspose.Imaging für .NET können Sie DICOM-Metadaten während des Konvertierungsprozesses bearbeiten und anpassen. Detaillierte Informationen zum Umgang mit DICOM-Metadaten finden Sie in der Dokumentation.

### F5: Gibt es eine Testversion von Aspose.Imaging für .NET?

 A5: Ja, Sie können auf eine kostenlose Testversion von Aspose.Imaging für .NET zugreifen, um dessen Funktionen zu testen. Sie können die Testversion herunterladen[Hier](https://releases.aspose.com/).