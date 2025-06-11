---
"description": "Erfahren Sie, wie Sie mit Aspose.Imaging für .NET Rasterbilder in SVG zeichnen. Verbessern Sie Ihre .NET-Anwendungen mit dynamischen Bildern."
"linktitle": "Zeichnen Sie ein Rasterbild auf SVG in Aspose.Imaging für .NET"
"second_title": "Aspose.Imaging .NET Bildverarbeitungs-API"
"title": "So zeichnen Sie ein Rasterbild auf SVG in Aspose.Imaging für .NET"
"url": "/de/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# So zeichnen Sie ein Rasterbild auf SVG in Aspose.Imaging für .NET


In der Welt der .NET-Programmierung gilt Aspose.Imaging als zuverlässige und vielseitige Bibliothek für verschiedene bildbezogene Aufgaben. Eine faszinierende Funktion ist die Möglichkeit, ein Rasterbild auf einer SVG-Leinwand zu zeichnen. In dieser Schritt-für-Schritt-Anleitung führen wir Sie durch den Prozess des Zeichnens eines Rasterbilds auf einer SVG-Leinwand mit Aspose.Imaging für .NET.

## Voraussetzungen

Bevor wir in die Details eintauchen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Aspose.Imaging für .NET: Sie müssen die Bibliothek installiert haben. Falls nicht, können Sie sie von der [Aspose.Imaging für .NET-Downloadseite](https://releases.aspose.com/imaging/net/).

- Ihr Dokumentverzeichnis: Ersetzen `"Your Document Directory"` durch den tatsächlichen Pfad zu Ihrem Arbeitsverzeichnis.

Lassen Sie uns den Prozess nun in leicht verständliche Schritte unterteilen:

## Schritt 1: Erforderliche Namespaces importieren

Sie müssen die erforderlichen Namespaces importieren, um mit Aspose.Imaging zu arbeiten:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Schritt 2: Laden Sie die Bilder

- Laden Sie zunächst das Rasterbild, das Sie auf der SVG-Leinwand zeichnen möchten.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Laden Sie als Nächstes das SVG-Canvas-Bild dort, wo Sie das Rasterbild zeichnen möchten.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Schritt 3: Zeichnen auf dem SVG-Bild

Jetzt können Sie mit dem Zeichnen auf dem vorhandenen SVG-Bild beginnen. Dazu müssen Sie eine Instanz von `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Schritt 4: Zeichnen Sie das Rasterbild

- Definieren Sie die Grenzen, in denen Sie das Rasterbild zeichnen möchten, und geben Sie die Quellregion aus dem Rasterbild an.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Schritt 5: Speichern Sie das Ergebnis

Nachdem Sie das Rasterbild auf der SVG-Leinwand gezeichnet haben, können Sie das resultierende Bild speichern:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Abschluss

Herzlichen Glückwunsch! Sie haben mit Aspose.Imaging für .NET erfolgreich ein Rasterbild auf einer SVG-Leinwand gezeichnet. Dies kann unglaublich nützlich sein, um ansprechende und dynamische Bilder in Ihren .NET-Anwendungen zu erstellen.

Weitere Informationen und ausführliche Dokumentation finden Sie im [Aspose.Imaging für .NET-Dokumentation](https://reference.aspose.com/imaging/net/).

## Häufig gestellte Fragen

### Was ist Aspose.Imaging für .NET?
   Aspose.Imaging für .NET ist eine leistungsstarke Bildverarbeitungsbibliothek, mit der Entwickler Bilder in verschiedenen Formaten innerhalb von .NET-Anwendungen erstellen, bearbeiten und konvertieren können.

### Kann ich Aspose.Imaging für .NET in kommerziellen Projekten verwenden?
   Ja, Sie können Aspose.Imaging für .NET sowohl in kommerziellen als auch in nicht-kommerziellen Projekten verwenden. Lizenzdetails finden Sie auf der [Kaufseite](https://purchase.aspose.com/buy).

### Gibt es eine kostenlose Testversion?
   Ja, Sie können eine kostenlose Testversion von Aspose.Imaging für .NET erhalten von [Hier](https://releases.aspose.com/).

### Wo kann ich Unterstützung erhalten oder Fragen stellen?
   Wenn Sie Fragen haben oder Unterstützung benötigen, besuchen Sie die [Aspose.Imaging-Forum](https://forum.aspose.com/).

### Wie kann ich eine temporäre Lizenz für Aspose.Imaging für .NET erhalten?
   Eine vorläufige Lizenz erhalten Sie bei [Hier](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}