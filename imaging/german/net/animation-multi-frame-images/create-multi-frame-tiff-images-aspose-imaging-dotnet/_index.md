---
"date": "2025-06-02"
"description": "Erfahren Sie, wie Sie mit Aspose.Imaging in .NET TIFF-Bilder mit mehreren Frames erstellen. Richten Sie Ihre Umgebung ein, konfigurieren Sie TiffOptions, ändern Sie die JPEG-Größe und fügen Sie Frames hinzu."
"title": "So erstellen Sie Multi-Frame-TIFF-Bilder mit Aspose.Imaging für .NET"
"url": "/de/net/animation-multi-frame-images/create-multi-frame-tiff-images-aspose-imaging-dotnet/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# So erstellen Sie Multi-Frame-TIFF-Bilder mit Aspose.Imaging für .NET

## Einführung

Möchten Sie die Erstellung von Multiframe-TIFF-Bildern mit Aspose.Imaging für .NET meistern? Dieses umfassende Tutorial führt Sie mühelos durch die Einrichtung Ihrer Umgebung, die Konfiguration von TiffOptions, die Größenanpassung von JPEG-Dateien und das Hinzufügen von Frames zu einem TIFF-Bild. Ob Sie Dokumentarchive verwalten oder hochwertige Bilder in Softwareanwendungen integrieren – dieser Leitfaden optimiert Ihren Workflow.

**Was Sie lernen werden:**
- So richten Sie Aspose.Imaging für .NET ein
- Konfigurieren von TiffOptions für Schwarzweißbilder mit CCITT Fax Group 3-Komprimierung
- Laden und Ändern der Größe von JPEG-Dateien aus einem Verzeichnis
- Hinzufügen von Rahmen zu einem TIFF-Bild
- Speichern von TIFF-Bildern mit mehreren Frames

Lassen Sie uns zunächst einen Blick auf die Voraussetzungen werfen.

## Voraussetzungen

Bevor Sie mit der Erstellung von TIFF-Bildern mit Aspose.Imaging beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

### Erforderliche Bibliotheken und Abhängigkeiten
- **Aspose.Imaging für .NET**Installieren Sie diese Bibliothek entweder mit NuGet oder Ihrem bevorzugten Paketmanager.
  
### Anforderungen für die Umgebungseinrichtung
- Eine Entwicklungsumgebung, die C# und .NET Core/5+ unterstützt
  
### Voraussetzungen
- Grundlegendes Verständnis der C#-Programmierkonzepte
- Vertrautheit mit der Handhabung von Bilddateien in .NET

## Einrichten von Aspose.Imaging für .NET

Um zu beginnen, müssen Sie Aspose.Imaging installieren. So geht's:

**.NET-CLI**
```shell
dotnet add package Aspose.Imaging
```

**Paketmanager**
```powershell
Install-Package Aspose.Imaging
```

**NuGet-Paket-Manager-Benutzeroberfläche**
Suchen Sie nach „Aspose.Imaging“ und installieren Sie die neueste Version.

### Schritte zum Lizenzerwerb
- **Kostenlose Testversion**: Greifen Sie auf eine Version mit eingeschränkter Funktionalität zu, um die Features zu testen.
- **Temporäre Lizenz**: Erhalten Sie dies für eine erweiterte Testversion ohne Evaluierungsbeschränkungen. Besuchen Sie [Temporäre Lizenz](https://purchase.aspose.com/temporary-license/).
- **Kaufen**: Für den vollständigen Zugriff sollten Sie eine Lizenz erwerben unter [Aspose.Imaging kaufen](https://purchase.aspose.com/buy).

### Grundlegende Initialisierung und Einrichtung

```csharp
// Initialisieren Sie die Bibliothek mit Ihrer Lizenz
Aspose.Imaging.License license = new Aspose.Imaging.License();
license.SetLicense("Path to your license file");
```

## Implementierungshandbuch

Lassen Sie uns die Implementierung in überschaubare Abschnitte unterteilen.

### Erstellen und Konfigurieren von TiffOptions für TIFF-Bilder

#### Überblick
Erstellen eines `TiffOptions` Mit dem Objekt können Sie Einstellungen wie Komprimierung und photometrische Interpretation definieren, die für die Anpassung Ihrer TIFF-Dateien wichtig sind.

#### Schrittweise Implementierung

**1. Importieren Sie die erforderlichen Namespaces**
Stellen Sie sicher, dass Ihre Datei diese Namespaces enthält:

```csharp
using Aspose.Imaging.FileFormats.Tiff;
using Aspose.Imaging.FileFormats.Tiff.Enums;
using Aspose.Imaging.ImageOptions;
```

**2. TiffOptions konfigurieren**
Richten Sie die `TiffOptions` Objekt mit spezifischen Konfigurationen für ein Schwarzweißbild mit CCITT Fax Group 3-Komprimierung.

```csharp
// TiffOptions mit Standardeinstellungen erstellen
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);

// Bits pro Sample auf 1 setzen (schwarz und weiß)
outputSettings.BitsPerSample = new ushort[] { 1 };

// Verwenden Sie die CCITT Fax Group 3-Komprimierung
outputSettings.Compression = TiffCompressions.CcittFax3;

// Definieren Sie die photometrische Interpretation als MinIsWhite
outputSettings.Photometric = TiffPhotometrics.MinIsWhite;

// Legen Sie die Quelle auf einen leeren Stream fest, um ein neues TIFF von Grund auf neu zu erstellen
outputSettings.Source = new Aspose.Imaging.Sources.StreamSource(new System.IO.MemoryStream());
```

### Erstellen und Konfigurieren von TiffImage mit bestimmten Abmessungen

#### Überblick
Erstellen eines `TiffImage` beinhaltet das Festlegen benutzerdefinierter Abmessungen, was bei der Definition der Größe jedes TIFF-Frames von entscheidender Bedeutung ist.

**1. Bildabmessungen definieren**

```csharp
int newWidth = 500; // Breite für jeden TIFF-Frame
int newHeight = 500; // Höhe für jeden TIFF-Frame
string path = "@YOUR_OUTPUT_DIRECTORY\\AddFramesToTIFFImage_out.tif";
```

**2. Erstellen Sie eine TiffImage-Instanz**
Initialisieren Sie den `TiffImage` mit angegebenen Abmessungen und Ausgabeeinstellungen.

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    // Hier wird die Logik zum Hinzufügen von Frames hinzugefügt.
}
```

### JPEG-Dateien aus dem Verzeichnis laden und ihre Größe ändern

#### Überblick
Das Laden von JPEG-Bildern, deren Größenänderung und die Vorbereitung für die Aufnahme in eine TIFF-Datei werden mit Aspose.Imaging optimiert.

**1. JPEG-Bilder laden**

```csharp
string dataDir = "@YOUR_DOCUMENT_DIRECTORY"; // Verzeichnis mit Eingabebildern

foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
{
    using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
    {
        // Passen Sie die Bildgröße an die Abmessungen des TIFF-Rahmens an
        ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
        
        // Hier wird zusätzliche Logik zur Handhabung mehrerer Frames hinzugefügt.
    }
}
```

### Rahmen zum TiffImage hinzufügen und speichern

#### Überblick
Das Hinzufügen von Frames zu einem TIFF-Bild umfasst das Kopieren von JPEG-Pixeln mit geänderter Größe in jeden Frame und das Speichern des vollständigen TIFF mit mehreren Frames.

**1. Initialisieren Sie die TiffImage-Instanz**

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    int index = 0; // Rahmenindex-Tracker
    
    foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
    {
        using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
        {
            ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
            
            TiffFrame frame = tiffImage.ActiveFrame;
            if (index > 0)
            {
                // Für jedes nachfolgende Bild einen neuen Rahmen erstellen
                frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            }
            
            // Kopieren Sie Pixel aus dem skalierten JPEG in den TIFF-Rahmen
            frame.SavePixels(frame.Bounds, ri.LoadPixels(ri.Bounds));
            if (index > 0)
            {
                tiffImage.AddFrame(frame); // Zum TIFF-Bild erst nach dem ersten Frame hinzufügen
            }
            index++;
        }
    }
    
    tiffImage.Save(path); // Speichern Sie das endgültige TIFF mit allen Frames
}
```

## Praktische Anwendungen

Hier sind einige Anwendungsfälle aus der Praxis zum Erstellen von TIFF-Bildern mit mehreren Frames:

1. **Dokumentenarchivierung**: Speichern Sie gescannte Dokumente als einzelne TIFF-Dateien, um die Datenintegrität und einen einfachen Zugriff sicherzustellen.
2. **Medizinische Bildgebung**: Verwenden Sie hochwertige, komprimierte TIFF-Formate zum Speichern medizinischer Scans wie MRTs und CTs.
3. **Grafikdesign**: Kombinieren Sie mehrere Designebenen in einer einzigen Datei für eine effiziente Handhabung in Grafiksoftware.
4. **Fotografie**: Archivieren Sie mehrseitige Fotoalben als einzelne Dateien zum einfachen Teilen und Speichern.
5. **Industrielle Qualitätskontrolle**: Verwenden Sie TIFF-Bilder, um detaillierte Inspektionsdaten über mehrere Frames hinweg aufzuzeichnen.

## Überlegungen zur Leistung

### Tipps zur Leistungsoptimierung
- **Speicherverwaltung**Entsorgen Sie Bildobjekte nach der Verwendung ordnungsgemäß, um Ressourcen freizugeben.
- **Stapelverarbeitung**: Verarbeiten Sie Bilder stapelweise, wenn Sie mit großen Datensätzen arbeiten, um die Speichernutzung effektiv zu verwalten.
- **Effiziente Komprimierung**: Wählen Sie geeignete Komprimierungseinstellungen basierend auf Ihren Qualitäts- und Leistungsanforderungen.

## Abschluss

Dieses Tutorial behandelte die wesentlichen Schritte zum Erstellen von Multi-Frame-TIFF-Bildern mit Aspose.Imaging für .NET. Von der Konfiguration `TiffOptions` Durch das Hinzufügen von Frames verfügen Sie jetzt über eine solide Grundlage für die Integration hochwertiger Bilder in Ihre Anwendungen.

**Nächste Schritte:**
- Experimentieren Sie mit verschiedenen Komprimierungseinstellungen und Bildformaten.
- Entdecken Sie zusätzliche Funktionen von Aspose.Imaging, indem Sie die [offizielle Dokumentation](https://reference.aspose.com/imaging/net/).

Versuchen Sie, diese Schritte in Ihren Projekten zu implementieren, und entdecken Sie, wie Multi-Frame-TIFF-Bilder Ihren Arbeitsablauf verbessern können.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}