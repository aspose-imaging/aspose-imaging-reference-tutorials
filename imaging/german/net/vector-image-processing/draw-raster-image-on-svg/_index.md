---
title: So zeichnen Sie ein Rasterbild auf SVG in Aspose.Imaging für .NET
linktitle: Zeichnen Sie ein Rasterbild auf SVG in Aspose.Imaging für .NET
second_title: Aspose.Imaging .NET-Bildverarbeitungs-API
description: Erfahren Sie, wie Sie mit Aspose.Imaging für .NET Rasterbilder in SVG zeichnen. Erweitern Sie Ihre .NET-Anwendungen mit dynamischen Bildern.
weight: 11
url: /de/net/vector-image-processing/draw-raster-image-on-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# So zeichnen Sie ein Rasterbild auf SVG in Aspose.Imaging für .NET


In der Welt der .NET-Programmierung gilt Aspose.Imaging als zuverlässige und vielseitige Bibliothek für die Bearbeitung verschiedener bildbezogener Aufgaben. Eine faszinierende Funktion ist die Möglichkeit, ein Rasterbild auf einer SVG-Leinwand zu zeichnen. In dieser Schritt-für-Schritt-Anleitung führen wir Sie durch den Prozess des Zeichnens eines Rasterbilds auf einer SVG-Datei mit Aspose.Imaging für .NET.

## Voraussetzungen

Bevor wir uns mit den Details befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.Imaging für .NET: Die Bibliothek muss installiert sein. Wenn nicht, können Sie es hier herunterladen[Aspose.Imaging für .NET-Downloadseite](https://releases.aspose.com/imaging/net/).

-  Ihr Dokumentenverzeichnis: Ersetzen`"Your Document Directory"` mit dem tatsächlichen Pfad zu Ihrem Arbeitsverzeichnis.

Lassen Sie uns den Prozess nun in einfach zu befolgende Schritte unterteilen:

## Schritt 1: Erforderliche Namespaces importieren

Sie müssen die erforderlichen Namespaces importieren, um mit Aspose.Imaging arbeiten zu können:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Schritt 2: Laden Sie die Bilder

- Laden Sie zunächst das Rasterbild, das Sie zeichnen möchten, auf die SVG-Leinwand.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Laden Sie als Nächstes das SVG-Leinwandbild an die Stelle, an der Sie das Rasterbild zeichnen möchten.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Schritt 3: Zeichnen auf dem SVG-Bild

Jetzt können Sie mit dem Zeichnen auf dem vorhandenen SVG-Bild beginnen. Dazu müssen Sie eine Instanz von erstellen`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Schritt 4: Zeichnen Sie das Rasterbild

- Definieren Sie die Grenzen, an denen Sie das Rasterbild zeichnen möchten, und geben Sie den Quellbereich aus dem Rasterbild an.

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

Glückwunsch! Sie haben mit Aspose.Imaging für .NET erfolgreich ein Rasterbild auf einer SVG-Leinwand gezeichnet. Dies kann unglaublich nützlich sein, um in Ihren .NET-Anwendungen umfangreiche und dynamische Bilder zu erstellen.

 Weitere Informationen und eine ausführliche Dokumentation finden Sie unter[Aspose.Imaging für .NET-Dokumentation](https://reference.aspose.com/imaging/net/).

## Häufig gestellte Fragen

### Was ist Aspose.Imaging für .NET?
   Aspose.Imaging für .NET ist eine leistungsstarke Bildverarbeitungsbibliothek, die es Entwicklern ermöglicht, Bilder in verschiedenen Formaten innerhalb von .NET-Anwendungen zu erstellen, zu bearbeiten und zu konvertieren.

### Kann ich Aspose.Imaging für .NET in kommerziellen Projekten verwenden?
    Ja, Sie können Aspose.Imaging für .NET sowohl in kommerziellen als auch in nichtkommerziellen Projekten verwenden. Lizenzdetails finden Sie auf der[Kaufseite](https://purchase.aspose.com/buy).

### Gibt es eine kostenlose Testversion?
    Ja, Sie können eine kostenlose Testversion von Aspose.Imaging für .NET unter erhalten[Hier](https://releases.aspose.com/).

### Wo kann ich Unterstützung bekommen oder Fragen stellen?
    Wenn Sie Fragen haben oder Unterstützung benötigen, können Sie die besuchen[Aspose.Imaging-Forum](https://forum.aspose.com/).

### Wie kann ich eine temporäre Lizenz für Aspose.Imaging für .NET erhalten?
    Sie können eine temporäre Lizenz erhalten von[Hier](https://purchase.aspose.com/temporary-license/).



{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
