---
date: '2026-02-09'
description: Erfahren Sie, wie Sie JPEG in TIFF konvertieren und mehrseitige TIFF‑Bilder
  mit Aspose.Imaging für .NET erstellen. Enthält die Einrichtung, die Konfiguration
  von TiffOptions, das Laden von Bildern aus einem Verzeichnis und die Frame‑Verarbeitung.
keywords:
- create multi-frame tiff images
- Aspose.Imaging for .NET tutorial
- configure TiffOptions in .NET
title: Wie man JPEG in TIFF konvertiert und Multi‑Frame‑TIFF‑Bilder mit Aspose.Imaging
  für .NET erstellt
url: /de/net/animation-multi-frame-images/create-multi-frame-tiff-images-aspose-imaging-dotnet/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# So konvertieren Sie JPEG zu TIFF und erstellen Multi‑Frame‑TIFF‑Bilder mit Aspose.Imaging für .NET

## Einführung

Möchten Sie die Kunst des **JPEG zu TIFF konvertierens** meistern und gleichzeitig Multi‑Frame‑TIFF‑Dateien mit Aspose.Imaging für .NET erstellen? Dieses umfassende Tutorial führt Sie durch die Einrichtung Ihrer Umgebung, die Konfiguration von `TiffOptions`, das Skalieren von JPEG‑Dateien und das Hinzufügen von Frames zu einem TIFF‑Bild – alles ganz einfach. Egal, ob Sie Dokumentenarchive verwalten oder hochwertige Bildverarbeitung in Softwareanwendungen integrieren, dieser Leitfaden ist darauf ausgelegt, Ihren Workflow zu verbessern.

**Was Sie lernen werden:**
- Wie Sie Aspose.Imaging für .NET einrichten
- Konfiguration von `TiffOptions` für Schwarz‑weiß‑Bilder mit CCITT Fax Group 3‑Kompression
- Laden und Skalieren von JPEG‑Dateien aus einem Verzeichnis
- Hinzufügen von Frames zu einem TIFF‑Bild
- Speichern von Multi‑Frame‑TIFF‑Bildern

Lassen Sie uns zu den Voraussetzungen springen, um loszulegen.

## Schnellantworten
- **Was bedeutet „JPEG zu TIFF konvertieren“?** Es bedeutet, ein JPEG‑Rasterbild zu nehmen und es im TIFF‑Format zu speichern, oft mit benutzerdefinierter Kompression oder mehreren Frames.  
- **Welche Bibliothek erledigt das am besten in .NET?** Aspose.Imaging für .NET bietet eine umfangreiche API für Konvertierung, Skalierung und Multi‑Frame‑Erstellung.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für die Evaluierung; eine permanente Lizenz entfernt alle Evaluierungsbeschränkungen.  
- **Kann ich Bilder automatisch aus einem Verzeichnis laden?** Ja – das Tutorial zeigt, wie JPEG‑Dateien aufgelistet und jede einzelne verarbeitet wird.  
- **Ist der Code mit .NET 6+ kompatibel?** Absolut – das Beispiel verwendet .NET Core/5+ APIs, die auf .NET 6 und später laufen.

## Was bedeutet „JPEG zu TIFF konvertieren“?
Das Konvertieren von JPEG zu TIFF beinhaltet das Dekodieren einer JPEG‑Datei, optionales Transformieren (z. B. Skalieren oder Ändern der Farbtiefe) und anschließend das Kodieren des Ergebnisses als TIFF‑Datei. TIFF unterstützt mehrere Frames, verlustfreie Kompression und Metadaten, die JPEG nicht bietet, und ist daher ideal für Archivierungs‑ und Mehrseitenszenarien.

## Warum Aspose.Imaging für diese Konvertierung verwenden?
- **Vollständige Kontrolle** über Kompression, photometrische Interpretation und Pixelformat.  
- **Multi‑Frame‑Unterstützung** – Sie können mehrere JPEG‑Seiten zu einem einzigen TIFF‑Dokument bündeln.  
- **Plattformübergreifend** – funktioniert unter Windows, Linux und macOS mit .NET Core/5+.  
- **Keine externen Abhängigkeiten** – reiner verwalteter Code, keine nativen DLLs.

## Voraussetzungen

Bevor Sie mit der Erstellung von TIFF‑Bildern mit Aspose.Imaging beginnen, stellen Sie sicher, dass Sie Folgendes haben:

### Erforderliche Bibliotheken und Abhängigkeiten
- **Aspose.Imaging für .NET**: Installieren Sie diese Bibliothek über NuGet oder Ihren bevorzugten Paketmanager.
  
### Anforderungen an die Umgebung
- Eine Entwicklungsumgebung, die C# und .NET Core/5+ unterstützt  
  
### Wissensvoraussetzungen
- Grundlegendes Verständnis von C#‑Programmierungskonzepten  
- Vertrautheit mit dem Umgang mit Bilddateien in .NET  

## Aspose.Imaging für .NET einrichten

Um zu beginnen, müssen Sie Aspose.Imaging installieren. So geht’s:

**.NET CLI**
```shell
dotnet add package Aspose.Imaging
```

**Package Manager**
```powershell
Install-Package Aspose.Imaging
```

**NuGet Package Manager UI**  
Suchen Sie nach „Aspose.Imaging“ und installieren Sie die neueste Version.

### Schritte zum Erwerb einer Lizenz
- **Kostenlose Testversion**: Zugriff auf eine funktionsbeschränkte Version, um Features zu testen.  
- **Temporäre Lizenz**: Erhalten Sie diese für eine erweiterte Testphase ohne Evaluierungsbeschränkungen. Besuchen Sie [Temporary License](https://purchase.aspose.com/temporary-license/).  
- **Kauf**: Für vollen Zugriff sollten Sie eine Lizenz unter [Purchase Aspose.Imaging](https://purchase.aspose.com/buy) erwerben.

### Grundlegende Initialisierung und Einrichtung

```csharp
// Initialize the library with your license
Aspose.Imaging.License license = new Aspose.Imaging.License();
license.SetLicense("Path to your license file");
```

## Wie man JPEG zu TIFF konvertiert und mehrere Frames hinzufügt

Lassen Sie uns die Implementierung in handhabbare Abschnitte unterteilen.

### Erstellen und Konfigurieren von TiffOptions für das TIFF‑Bild

#### Überblick
Das Erstellen eines `TiffOptions`‑Objekts ermöglicht es Ihnen, Einstellungen wie Kompression und photometrische Interpretation festzulegen – entscheidend für die Anpassung Ihrer TIFF‑Dateien.

#### Schritt‑für‑Schritt‑Implementierung

**1. Notwendige Namespaces importieren**  
Stellen Sie sicher, dass Sie diese Namespaces in Ihrer Datei eingebunden haben:

```csharp
using Aspose.Imaging.FileFormats.Tiff;
using Aspose.Imaging.FileFormats.Tiff.Enums;
using Aspose.Imaging.ImageOptions;
```

**2. TiffOptions konfigurieren**  
Richten Sie das `TiffOptions`‑Objekt mit spezifischen Konfigurationen für ein Schwarz‑weiß‑Bild unter Verwendung der CCITT Fax Group 3‑Kompression ein.

```csharp
// Create TiffOptions with default settings
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);

// Set bits per sample to 1 (black and white)
outputSettings.BitsPerSample = new ushort[] { 1 };

// Use CCITT Fax Group 3 compression
outputSettings.Compression = TiffCompressions.CcittFax3;

// Define photometric interpretation as MinIsWhite
outputSettings.Photometric = TiffPhotometrics.MinIsWhite;

// Set source to an empty stream for creating new TIFF from scratch
outputSettings.Source = new Aspose.Imaging.Sources.StreamSource(new System.IO.MemoryStream());
```

### Erstellen und Konfigurieren von TiffImage mit spezifischen Abmessungen

#### Überblick
Das Erstellen eines `TiffImage` beinhaltet das Festlegen benutzerdefinierter Abmessungen, was wichtig ist, wenn Sie die Größe jedes TIFF‑Frames definieren.

**1. Bildabmessungen festlegen**

```csharp
int newWidth = 500; // Width for each TIFF frame
int newHeight = 500; // Height for each TIFF frame
string path = "@YOUR_OUTPUT_DIRECTORY\\AddFramesToTIFFImage_out.tif";
```

**2. TiffImage‑Instanz erstellen**  
Initialisieren Sie das `TiffImage` mit den angegebenen Abmessungen und Ausgabeeinstellungen.

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    // Logic to add frames will be added here.
}
```

### JPEG‑Dateien aus Verzeichnis laden und skalieren

#### Überblick
Das Laden von JPEG‑Bildern, deren Skalierung und die Vorbereitung für die Einbindung in eine TIFF‑Datei wird mit Aspose.Imaging vereinfacht.

**1. JPEG‑Bilder laden**

```csharp
string dataDir = "@YOUR_DOCUMENT_DIRECTORY"; // Directory containing input images

foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
{
    using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
    {
        // Resize image to match TIFF frame dimensions
        ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
        
        // Additional logic for handling multiple frames will be added here.
    }
}
```

> **Pro‑Tipp:** Der Ausdruck **load images from directory** beschreibt exakt das, was die obige Schleife tut – sie enumeriert jede JPEG‑Datei im Zielordner.

### Frame zu TiffImage hinzufügen und speichern

#### Überblick
Das Hinzufügen von Frames zu einem TIFF‑Bild beinhaltet das Kopieren der skalierten JPEG‑Pixel in jeden Frame und das Speichern des kompletten Multi‑Frame‑TIFFs.

**1. TiffImage‑Instanz initialisieren**

```csharp
using (TiffImage tiffImage = (TiffImage)Aspose.Imaging.Image.Create(outputSettings, newWidth, newHeight))
{
    int index = 0; // Frame index tracker
    
    foreach (var file in Directory.GetFiles(dataDir, "*.jpg"))
    {
        using (Aspose.Imaging.RasterImage ri = (Aspose.Imaging.RasterImage)Aspose.Imaging.Image.Load(file))
        {
            ri.Resize(newWidth, newHeight, Aspose.Imaging.ResizeType.NearestNeighbourResample);
            
            TiffFrame frame = tiffImage.ActiveFrame;
            if (index > 0)
            {
                // Create a new frame for each subsequent image
                frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            }
            
            // Copy pixels from the resized JPEG into the TIFF frame
            frame.SavePixels(frame.Bounds, ri.LoadPixels(ri.Bounds));
            if (index > 0)
            {
                tiffImage.AddFrame(frame); // Add to TIFF image only after the first frame
            }
            index++;
        }
    }
    
    tiffImage.Save(path); // Save the final TIFF with all frames
}
```

## Praktische Anwendungen

Hier einige reale Anwendungsfälle für das Erstellen von Multi‑Frame‑TIFF‑Bildern:

1. **Dokumentenarchivierung** – Gescannte Dokumente als einzelne TIFF‑Datei speichern, um Datenintegrität und einfachen Zugriff zu gewährleisten.  
2. **Medizinische Bildgebung** – Hochwertige, komprimierte TIFF‑Formate für die Speicherung von Scans wie MRTs und CTs verwenden.  
3. **Grafikdesign** – Mehrere Design‑Ebenen zu einer einzigen Datei kombinieren für effizientes Arbeiten in Grafiksoftware.  
4. **Fotografie** – Mehrseitige Fotoalben als einzelne Dateien archivieren, um einfaches Teilen und Speichern zu ermöglichen.  
5. **Industrielle Qualitätskontrolle** – Detaillierte Prüfdaten über mehrere Frames in einem TIFF‑Bild festhalten.

## Leistungsüberlegungen

### Tipps zur Optimierung der Performance
- **Speichermanagement** – Bildobjekte sofort freigeben (`using`‑Anweisungen), um Ressourcen zu schonen.  
- **Batch‑Verarbeitung** – Bilder in Chargen verarbeiten, wenn Sie große Datenmengen bearbeiten, um den Speicherverbrauch vorhersehbar zu halten.  
- **Effiziente Kompression** – Kompressionseinstellungen wählen, die Qualität und Geschwindigkeit für Ihr Szenario ausbalancieren.

## Häufig gestellte Fragen

**F: Kann ich JPEG zu TIFF konvertieren, ohne Qualitätsverlust?**  
A: Ja. Durch die Verwendung verlustfreier Kompressionsoptionen (z. B. LZW oder CCITT Fax) und das Beibehalten der Original‑Pixeldaten kann die Konvertierung verlustfrei erfolgen.

**F: Muss ich Bilder vor dem Hinzufügen als Frames skalieren?**  
A: Alle Frames in einem TIFF müssen dieselben Abmessungen besitzen, daher ist das Skalieren jedes JPEGs auf die Ziel‑Breite und -Höhe erforderlich.

**F: Wie viele Frames kann eine TIFF‑Datei enthalten?**  
A: Praktisch unbegrenzt; die Grenze wird durch Dateigröße und verfügbaren Speicher bestimmt.

**F: Ist das erzeugte TIFF mit gängigen Betrachtern kompatibel?**  
A: Das Beispiel verwendet die standardmäßige CCITT Fax Group 3‑Kompression, die von den meisten TIFF‑Betrachtern und -Editoren breit unterstützt wird.

**F: Was, wenn ich eine andere Kompression für Farbbilder verwenden möchte?**  
A: Ersetzen Sie `TiffCompressions.CcittFax3` durch `TiffCompressions.Lzw` oder `TiffCompressions.Jpeg` und passen Sie `BitsPerSample` entsprechend an.

## Fazit

Dieses Tutorial hat die wesentlichen Schritte zum **JPEG zu TIFF konvertieren** und zum Erstellen von Multi‑Frame‑TIFF‑Bildern mit Aspose.Imaging für .NET behandelt. Von der Konfiguration von `TiffOptions` bis zum Hinzufügen von Frames haben Sie nun eine solide Grundlage, um hochwertige Bildverarbeitung in Ihre Anwendungen zu integrieren.

**Nächste Schritte**  
- Experimentieren Sie mit anderen Kompressionstypen und Farbtiefen.  
- Erkunden Sie weitere Aspose.Imaging‑Funktionen wie Metadaten‑Handling oder PDF‑Konvertierung.  
- Konsultieren Sie die [offizielle Dokumentation](https://reference.aspose.com/imaging/net/) für tiefere Einblicke.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Zuletzt aktualisiert:** 2026-02-09  
**Getestet mit:** Aspose.Imaging für .NET (neueste stabile Version)  
**Autor:** Aspose