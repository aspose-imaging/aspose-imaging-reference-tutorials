---
title: Unterstützt das Speichern von XMP-Tags in Aspose.Imaging für .NET
linktitle: Unterstützt das Speichern von XMP-Tags in Aspose.Imaging für .NET
second_title: Aspose.Imaging .NET-Bildverarbeitungs-API
description: Erfahren Sie, wie Sie mit Aspose.Imaging für .NET XMP-Metadaten zu DICOM-Bildern hinzufügen. Optimieren Sie die Bildverwaltung und -organisation mit dieser Schritt-für-Schritt-Anleitung.
weight: 25
url: /de/net/dicom-image-processing/support-storing-xmp-tags/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Unterstützt das Speichern von XMP-Tags in Aspose.Imaging für .NET

Aspose.Imaging für .NET ist eine leistungsstarke Bibliothek, die es Ihnen ermöglicht, mit verschiedenen Bildformaten in der .NET-Umgebung zu arbeiten. In diesem Tutorial erfahren Sie, wie Sie das Speichern von XMP-Tags (Extensible Metadata Platform) in Aspose.Imaging für .NET unterstützen. XMP-Tags sind für das Hinzufügen von Metadateninformationen zu Bildern unerlässlich und erleichtern die Organisation und Verwaltung Ihrer digitalen Assets. Wir unterteilen den Prozess in mehrere Schritte, damit Sie besser verstehen, wie Sie dies erreichen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Aspose.Imaging für .NET: Sie sollten Aspose.Imaging für .NET installiert haben. Sie können es hier herunterladen[Aspose.Imaging für .NET-Website](https://releases.aspose.com/imaging/net/).

## Namespaces importieren

Importieren Sie in Ihrem .NET-Projekt die erforderlichen Namespaces für die Arbeit mit Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Exif;
using Aspose.Imaging.FileFormats.Dicom;
```

Lassen Sie uns nun in die Schritt-für-Schritt-Anleitung zur Unterstützung der Speicherung von XMP-Tags mit Aspose.Imaging für .NET eintauchen.

## Schritt 1: Laden Sie das DICOM-Bild

 Laden Sie zunächst das DICOM-Bild, mit dem Sie arbeiten möchten. Ersetzen`"Your Document Directory"` mit dem tatsächlichen Verzeichnispfad, in dem sich Ihr DICOM-Bild befindet.

```csharp
string dataDir = "Your Document Directory";
using (DicomImage image = (DicomImage)Image.Load(dataDir + "file.dcm"))
{
    // Ihr Code kommt hierher
}
```

## Schritt 2: Erstellen Sie ein XMP-Paket und ein Dicom-Paket

Erstellen Sie einen XmpPacketWrapper und ein DicomPackage zum Speichern Ihrer Metadaten. Sie können verschiedene Metadatenfelder festlegen, z. B. Institution, Hersteller, Patientendetails, Serieninformationen und Studiendetails.

```csharp
XmpPacketWrapper xmpPacketWrapper = new XmpPacketWrapper();
DicomPackage dicomPackage = new DicomPackage();

dicomPackage.SetEquipmentInstitution("Test Institution");
dicomPackage.SetEquipmentManufacturer("Test Manufacturer");
dicomPackage.SetPatientBirthDate("19010101");
dicomPackage.SetPatientId("010101");
dicomPackage.SetPatientName("Test Name");
dicomPackage.SetPatientSex("M");
dicomPackage.SetSeriesDateTime("19020202");
dicomPackage.SetSeriesDescription("Test Series Description");
dicomPackage.SetSeriesModality("Test Modality");
dicomPackage.SetSeriesNumber("01");
dicomPackage.SetStudyDateTime("19030303");
dicomPackage.SetStudyDescription("Test Study Description");
dicomPackage.SetStudyId("02");
dicomPackage.SetStudyPhysician("Test Physician");

xmpPacketWrapper.AddPackage(dicomPackage);
```

## Schritt 3: Speichern Sie das Bild mit XMP-Metadaten

 Speichern Sie nun das Bild mit den hinzugefügten XMP-Metadaten mithilfe von`DicomOptions` Klasse.

```csharp
string outputFile = dataDir + "output.dcm";
image.Save(outputFile, new DicomOptions() { XmpData = xmpPacketWrapper });
```

## Schritt 4: Überprüfen Sie die XMP-Tags

Laden Sie das gespeicherte Bild und vergleichen Sie die DICOM-Informationen vor und nach dem Hinzufügen von XMP-Tags.

```csharp
using (DicomImage imageSaved = (DicomImage)Image.Load(outputFile))
{
    List<string> originalDicomInfo = image.FileInfo.DicomInfo;
    List<string> imageSavedDicomInfo = imageSaved.FileInfo.DicomInfo;
    int tagsCountDiff = Math.Abs(imageSavedDicomInfo.Count - originalDicomInfo.Count);
}
```

## Abschluss

In diesem Tutorial haben wir gelernt, wie man das Speichern von XMP-Tags in DICOM-Bildern mit Aspose.Imaging für .NET unterstützt. Das Hinzufügen von Metadaten zu Ihren Bildern ist für die Organisation und Verwaltung von entscheidender Bedeutung. Aspose.Imaging vereinfacht diesen Prozess und ermöglicht Ihnen die effiziente Arbeit mit Bildmetadaten.

 Weitere Einzelheiten und eine erweiterte Nutzung finden Sie im[Aspose.Imaging für .NET-Dokumentation](https://reference.aspose.com/imaging/net/).

## FAQs

### F1: Was sind XMP-Metadaten?

A1: XMP (Extensible Metadata Platform) ist ein Standard zum Hinzufügen von Metadaten zu digitalen Assets, einschließlich Bildern. Es hilft beim Organisieren und Beschreiben verschiedener Attribute der Datei.

### F2: Kann ich vorhandene XMP-Metadaten mit Aspose.Imaging für .NET bearbeiten?

A2: Ja, Sie können mit Aspose.Imaging vorhandene XMP-Metadaten bearbeiten und neue Metadaten zu Bildern hinzufügen.

### F3: Ist Aspose.Imaging für .NET für professionelle Bildverarbeitungsaufgaben geeignet?

A3: Absolut. Aspose.Imaging für .NET bietet zahlreiche Funktionen zur Bildbearbeitung, -bearbeitung und -konvertierung und eignet sich daher für den professionellen Einsatz.

### F4: Wo kann ich Unterstützung erhalten oder Fragen zu Aspose.Imaging für .NET stellen?

 A4: Sie können die besuchen[Aspose.Imaging für .NET-Forum](https://forum.aspose.com/) um Unterstützung zu erhalten und Ihre Fragen zu stellen.

### F5: Wie kann ich eine temporäre Lizenz für Aspose.Imaging für .NET erhalten?

 A5: Sie können eine temporäre Lizenz für Aspose.Imaging für .NET erhalten, indem Sie hier klicken[dieser Link](https://purchase.aspose.com/temporary-license/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
