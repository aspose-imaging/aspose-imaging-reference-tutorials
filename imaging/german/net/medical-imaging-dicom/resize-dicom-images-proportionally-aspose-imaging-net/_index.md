---
"date": "2025-06-03"
"description": "Erfahren Sie, wie Sie mit Aspose.Imaging für .NET die Größe von DICOM-Bildern proportional ändern und so die Qualität und Effizienz in medizinischen Bildgebungs-Workflows aufrechterhalten."
"title": "Proportionale DICOM-Bildgrößenänderung mit Aspose.Imaging für .NET – Eine vollständige Anleitung"
"url": "/de/net/medical-imaging-dicom/resize-dicom-images-proportionally-aspose-imaging-net/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Proportionale DICOM-Bildgrößenänderung mit Aspose.Imaging für .NET: Eine vollständige Anleitung

## Einführung
Im Bereich der medizinischen Bildgebung sind DICOM-Bilder (Digital Imaging and Communications in Medicine) für Diagnose und Analyse unerlässlich. Diese hochauflösenden Dateien können jedoch bei Speicherung und Übertragung umständlich sein. Dieses Tutorial führt Sie durch die proportionale Größenanpassung von DICOM-Bildern mit Aspose.Imaging für .NET – einer vielseitigen Bibliothek, die Bildverarbeitungsaufgaben vereinfacht.

**Was Sie lernen werden:**
- Installieren und Einrichten von Aspose.Imaging für .NET
- Ändern der Größe von DICOM-Bildern nach Höhe und Breite unter Beibehaltung der Proportionen
- Praktische Anwendungen dieser Techniken in medizinischen Bildgebungs-Workflows

Sehen wir uns an, wie Sie diese Funktionalität nahtlos in Ihre Projekte integrieren können. Bevor wir beginnen, stellen wir sicher, dass Sie alles haben, was Sie brauchen.

## Voraussetzungen
Bevor Sie mit Aspose.Imaging für .NET beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. **Erforderliche Bibliotheken und Versionen:**
   - Sie benötigen die Aspose.Imaging-Bibliothek für .NET.
   - Stellen Sie sicher, dass Ihr Projekt auf eine kompatible Version des .NET-Frameworks abzielt (z. B. .NET Core 3.1 oder höher).

2. **Umgebungs-Setup:**
   - AC#-Entwicklungsumgebung wie Visual Studio.

3. **Erforderliche Kenntnisse:**
   - Grundlegende Kenntnisse der C#-Programmierung und Vertrautheit mit Konzepten der Bildverarbeitung.

## Einrichten von Aspose.Imaging für .NET
Um zu beginnen, müssen Sie die Aspose.Imaging-Bibliothek in Ihrem Projekt installieren. Hier sind die Installationsschritte mit verschiedenen Paketmanagern:

**.NET-CLI:**
```shell
dotnet add package Aspose.Imaging
```

**Paketmanager-Konsole:**
```shell
Install-Package Aspose.Imaging
```

**NuGet-Paket-Manager-Benutzeroberfläche:**
- Suchen Sie nach „Aspose.Imaging“ und installieren Sie die neueste Version.

### Lizenzerwerb
Um alle Funktionen von Aspose.Imaging freizuschalten, benötigen Sie möglicherweise eine Lizenz. So geht's:

- **Kostenlose Testversion:** Beginnen Sie mit einer kostenlosen Testversion, um die grundlegenden Funktionen kennenzulernen.
- **Temporäre Lizenz:** Erhalten Sie eine temporäre Lizenz von [Hier](https://purchase.aspose.com/temporary-license/) für erweiterten Zugriff während der Entwicklung.
- **Kaufen:** Wenn Sie zufrieden sind, erwerben Sie eine Volllizenz bei [dieser Link](https://purchase.aspose.com/buy).

Initialisieren Sie die Bibliothek nach der Installation, indem Sie in Ihren Projektdateien darauf verweisen.

## Implementierungshandbuch
Wir zeigen Ihnen, wie Sie die proportionale Größenanpassung von DICOM-Bildern mit Aspose.Imaging für .NET implementieren. Wir behandeln sowohl die Höhen- als auch die Breitenanpassung mit detaillierten Erklärungen.

### Proportionale Größenänderung von DICOM-Bildern nach Höhe
In diesem Abschnitt wird die Größenänderung eines DICOM-Bilds anhand seiner Höhe demonstriert, wobei sichergestellt wird, dass das Seitenverhältnis erhalten bleibt.

#### Überblick
Bei der proportionalen Größenanpassung nach Höhe bleibt das ursprüngliche Seitenverhältnis erhalten, während die Höhe des Bilds auf eine bestimmte Größe angepasst wird – ideal, um die visuelle Integrität über verschiedene Anzeigeformate hinweg aufrechtzuerhalten.

#### Implementierungsschritte

**Schritt 1: Laden Sie das DICOM-Bild**
Öffnen und laden Sie zunächst Ihre DICOM-Datei mit Aspose.Imaging's `DicomImage` Klasse.
```csharp
using System;
using System.IO;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;

string dataDir = "YOUR_DOCUMENT_DIRECTORY";
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Öffnen Sie eine DICOM-Datei zum Lesen
using (var fileStream = new FileStream(dataDir + "/file.dcm\

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}