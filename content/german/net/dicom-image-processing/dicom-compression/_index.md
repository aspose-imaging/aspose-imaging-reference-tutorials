---
title: DICOM-Komprimierung in Aspose.Imaging für .NET
linktitle: DICOM-Komprimierung in Aspose.Imaging für .NET
second_title: Aspose.Imaging .NET-Bildverarbeitungs-API
description: Erfahren Sie, wie Sie eine DICOM-Komprimierung mit Aspose.Imaging für .NET durchführen. Befolgen Sie diese Schritt-für-Schritt-Anleitung, um medizinische Bilder mit hoher diagnostischer Qualität effizient zu speichern und zu übertragen.
type: docs
weight: 17
url: /de/net/dicom-image-processing/dicom-compression/
---
In der Welt der medizinischen Bildgebung ist der DICOM-Standard (Digital Imaging and Communications in Medicine) für die Speicherung und Weitergabe medizinischer Bilder von größter Bedeutung. Aspose.Imaging für .NET, eine leistungsstarke .NET-Bibliothek, bietet umfassende Unterstützung für die Arbeit mit DICOM-Bildern. Dieses Tutorial führt Sie durch den Prozess der DICOM-Komprimierung mit Aspose.Imaging für .NET. Wir werden jeden Schritt aufschlüsseln und den Prozess im Detail erklären.

## Voraussetzungen

Bevor wir uns mit der DICOM-Komprimierung mit Aspose.Imaging für .NET befassen, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

1. Visual Studio

Stellen Sie sicher, dass Visual Studio auf Ihrem System installiert ist. Wenn nicht, können Sie es von der Website herunterladen.

2. Aspose.Imaging für .NET

Sie müssen über die Aspose.Imaging for .NET-Bibliothek verfügen. Sie können diese Bibliothek erhalten, indem Sie den unten angegebenen Links folgen:

- [Laden Sie Aspose.Imaging für .NET herunter](https://releases.aspose.com/imaging/net/)
- [Kaufen Sie Aspose.Imaging für .NET](https://purchase.aspose.com/buy)
- [Holen Sie sich eine kostenlose Testlizenz](https://releases.aspose.com/)
- [Temporäre Lizenz](https://purchase.aspose.com/temporary-license/)

Wenn diese Voraussetzungen erfüllt sind, beginnen wir mit der Schritt-für-Schritt-Anleitung zur Durchführung der DICOM-Komprimierung mit Aspose.Imaging für .NET.

## Namespaces importieren

Bevor wir fortfahren, müssen wir die erforderlichen Namespaces importieren, um auf die erforderlichen Klassen und Methoden zuzugreifen. Öffnen Sie Ihr Visual Studio-Projekt und fügen Sie oben in Ihrer C#-Datei Folgendes hinzu:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

Jetzt können wir mit dem DICOM-Komprimierungsprozess beginnen.

## Schritt 1: Laden Sie das Originalbild

 Wir laden zunächst das Originalbild, das Sie in das DICOM-Format konvertieren möchten. Unbedingt austauschen`"Your Document Directory"` mit dem tatsächlichen Pfad zu Ihrem Bildverzeichnis.

```csharp
string dataDir = "Your Document Directory";
string inputFile = Path.Combine(dataDir, "original.jpg");

using (var inputImage = Image.Load(inputFile))
{
    // Hier finden Sie Ihren Code für die DICOM-Komprimierung.
}
```

## Schritt 2: Führen Sie eine unkomprimierte DICOM-Komprimierung durch

In diesem Schritt führen wir eine unkomprimierte DICOM-Komprimierung durch. Hier ist der Code dafür:

```csharp
string output1 = Path.Combine(dataDir, "original_Uncompressed.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.None }
};

inputImage.Save(output1, options);
```

## Schritt 3: Führen Sie die JPEG-DICOM-Komprimierung durch

Kommen wir nun zur DICOM-Komprimierung im JPEG-Format:

```csharp
string output2 = Path.Combine(dataDir, "original_JPEG.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Jpeg }
};

inputImage.Save(output2, options);
```

## Schritt 4: Führen Sie die JPEG2000-DICOM-Komprimierung durch

In diesem Schritt führen wir eine DICOM-Komprimierung im JPEG2000-Format durch. So geht's:

```csharp
string output3 = Path.Combine(dataDir, "original_JPEG2000.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression
    {
        Type = CompressionType.Jpeg2000,
        Jpeg2000 = new Jpeg2000Options
        {
            Codec = Jpeg2000Codec.Jp2,
            Irreversible = false
        }
    }
};

inputImage.Save(output3, options);
```

## Schritt 5: Führen Sie die RLE-DICOM-Komprimierung durch

Abschließend führen wir die DICOM-Komprimierung mit dem RLE-Format (Run-Length Encoding) durch:

```csharp
string output4 = Path.Combine(dataDir, "original_RLE.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Rle }
};

inputImage.Save(output4, options);
```

## Abschluss

 In dieser Schritt-für-Schritt-Anleitung haben wir gelernt, wie Sie die DICOM-Komprimierung mit Aspose.Imaging für .NET durchführen. Diese Bibliothek stellt einen leistungsstarken Satz an Werkzeugen für die Arbeit mit medizinischen Bildern bereit, und Sie können ihre Fähigkeiten weiter erkunden, indem Sie sich auf die beziehen[Dokumentation](https://reference.aspose.com/imaging/net/).

## FAQs

### F1: Was ist DICOM-Komprimierung?

A1: Bei der DICOM-Komprimierung wird die Größe medizinischer Bilder reduziert und gleichzeitig ihre diagnostische Qualität erhalten. Es ist für die effiziente Speicherung und Übertragung medizinischer Daten unerlässlich.

### F2: Warum Aspose.Imaging für .NET für die DICOM-Komprimierung verwenden?

A2: Aspose.Imaging für .NET bietet eine Reihe robuster Funktionen und eine benutzerfreundliche API für die Arbeit mit DICOM-Bildern und ist damit eine ausgezeichnete Wahl für medizinische Bildgebungsanwendungen.

### F3: Kann ich mit Aspose.Imaging für .NET andere Bildverarbeitungsvorgänge in Verbindung mit der DICOM-Komprimierung anwenden?

A3: Ja, Aspose.Imaging für .NET bietet eine breite Palette an Bildverarbeitungsfunktionen, die mit der DICOM-Komprimierung kombiniert werden können, um spezifische Anforderungen zu erfüllen.

### F4: Wo kann ich Unterstützung erhalten oder Fragen zu Aspose.Imaging für .NET stellen?

 A4: Sie können die besuchen[Aspose.Imaging-Foren](https://forum.aspose.com/) um Unterstützung zu erhalten, Fragen zu stellen und mit der Aspose.Imaging-Community in Kontakt zu treten.

### F5: Gibt es eine Testversion von Aspose.Imaging für .NET zum Testen?

A5: Ja, Sie können eine erhalten[kostenlose Testlizenz](https://releases.aspose.com/) um Aspose.Imaging für .NET vor dem Kauf zu testen.