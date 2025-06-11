---
"description": "Erfahren Sie, wie Sie DICOM-Komprimierung mit Aspose.Imaging für .NET durchführen. Folgen Sie dieser Schritt-für-Schritt-Anleitung, um medizinische Bilder effizient und mit hoher diagnostischer Qualität zu speichern und zu übertragen."
"linktitle": "DICOM-Komprimierung in Aspose.Imaging für .NET"
"second_title": "Aspose.Imaging .NET Bildverarbeitungs-API"
"title": "DICOM-Komprimierung in Aspose.Imaging für .NET"
"url": "/de/net/dicom-image-processing/dicom-compression/"
"weight": 17
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# DICOM-Komprimierung in Aspose.Imaging für .NET

In der medizinischen Bildgebung ist der DICOM-Standard (Digital Imaging and Communications in Medicine) für die Speicherung und Weitergabe medizinischer Bilder von größter Bedeutung. Aspose.Imaging für .NET, eine leistungsstarke .NET-Bibliothek, bietet umfassende Unterstützung für die Arbeit mit DICOM-Bildern. Dieses Tutorial führt Sie durch den Prozess der DICOM-Komprimierung mit Aspose.Imaging für .NET. Wir erklären jeden Schritt detailliert.

## Voraussetzungen

Bevor wir uns mit der DICOM-Komprimierung mit Aspose.Imaging für .NET befassen, müssen Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

1. Visual Studio

Stellen Sie sicher, dass Visual Studio auf Ihrem System installiert ist. Andernfalls können Sie es von der Website herunterladen.

2. Aspose.Imaging für .NET

Sie benötigen die Bibliothek Aspose.Imaging für .NET. Sie erhalten diese Bibliothek über die folgenden Links:

- [Laden Sie Aspose.Imaging für .NET herunter](https://releases.aspose.com/imaging/net/)
- [Aspose.Imaging für .NET kaufen](https://purchase.aspose.com/buy)
- [Holen Sie sich eine kostenlose Testlizenz](https://releases.aspose.com/)
- [Temporäre Lizenz](https://purchase.aspose.com/temporary-license/)

Nachdem diese Voraussetzungen erfüllt sind, können wir mit der Schritt-für-Schritt-Anleitung zur Durchführung der DICOM-Komprimierung mit Aspose.Imaging für .NET beginnen.

## Namespaces importieren

Bevor wir fortfahren, müssen wir die erforderlichen Namespaces importieren, um auf die benötigten Klassen und Methoden zuzugreifen. Öffnen Sie Ihr Visual Studio-Projekt und fügen Sie oben in Ihrer C#-Datei Folgendes hinzu:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

Jetzt können wir mit dem DICOM-Komprimierungsprozess beginnen.

## Schritt 1: Laden Sie das Originalbild

Wir laden zunächst das Originalbild, das Sie in das DICOM-Format konvertieren möchten. Stellen Sie sicher, dass Sie `"Your Document Directory"` durch den tatsächlichen Pfad zu Ihrem Bildverzeichnis.

```csharp
string dataDir = "Your Document Directory";
string inputFile = Path.Combine(dataDir, "original.jpg");

using (var inputImage = Image.Load(inputFile))
{
    // Ihr Code für die DICOM-Komprimierung wird hier eingefügt.
}
```

## Schritt 2: Unkomprimierte DICOM-Komprimierung durchführen

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

## Schritt 3: JPEG-DICOM-Komprimierung durchführen

Fahren wir nun mit der Durchführung der DICOM-Komprimierung im JPEG-Format fort:

```csharp
string output2 = Path.Combine(dataDir, "original_JPEG.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Jpeg }
};

inputImage.Save(output2, options);
```

## Schritt 4: Führen Sie eine JPEG2000 DICOM-Komprimierung durch

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

## Schritt 5: RLE DICOM-Komprimierung durchführen

Lassen Sie uns abschließend eine DICOM-Komprimierung im RLE-Format (Run-Length Encoding) durchführen:

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

In dieser Schritt-für-Schritt-Anleitung haben wir gelernt, wie man DICOM-Komprimierung mit Aspose.Imaging für .NET durchführt. Diese Bibliothek bietet leistungsstarke Tools für die Arbeit mit medizinischen Bildern. Sie können ihre Möglichkeiten weiter erkunden, indem Sie auf die [Dokumentation](https://reference.aspose.com/imaging/net/).

## Häufig gestellte Fragen

### F1: Was ist DICOM-Komprimierung?

A1: DICOM-Komprimierung ist der Prozess, die Größe medizinischer Bilder zu reduzieren und gleichzeitig ihre diagnostische Qualität zu erhalten. Sie ist für die effiziente Speicherung und Übertragung medizinischer Daten unerlässlich.

### F2: Warum Aspose.Imaging für .NET zur DICOM-Komprimierung verwenden?

A2: Aspose.Imaging für .NET bietet einen robusten Funktionsumfang und eine benutzerfreundliche API für die Arbeit mit DICOM-Bildern und ist damit eine ausgezeichnete Wahl für medizinische Bildgebungsanwendungen.

### F3: Kann ich mit Aspose.Imaging für .NET andere Bildverarbeitungsvorgänge in Verbindung mit der DICOM-Komprimierung anwenden?

A3: Ja, Aspose.Imaging für .NET bietet eine breite Palette an Bildverarbeitungsfunktionen, die mit DICOM-Komprimierung kombiniert werden können, um spezifische Anforderungen zu erfüllen.

### F4: Wo kann ich Support erhalten oder Fragen zu Aspose.Imaging für .NET stellen?

A4: Sie können die [Aspose.Imaging-Foren](https://forum.aspose.com/) um Unterstützung zu erhalten, Fragen zu stellen und mit der Aspose.Imaging-Community zu interagieren.

### F5: Gibt es eine Testversion von Aspose.Imaging für .NET zum Testen?

A5: Ja, Sie können eine [kostenlose Testlizenz](https://releases.aspose.com/) um Aspose.Imaging für .NET vor dem Kauf zu testen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}